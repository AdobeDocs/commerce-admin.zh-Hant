---
title: 設定同步化服務
description: 「瞭解如何使用Assets規則引擎服務連線您的Adobe Commerce和Experience Manager Assets專案，以啟用這兩個系統之間的資產同步。」
feature: CMS, Media
source-git-commit: 939fa5caeeb7a8913457c3492484362a1d3471be
workflow-type: tm+mt
source-wordcount: '1309'
ht-degree: 0%

---


# 設定同步化服務

資產規則引擎服務(ARES)是整合AEM Assets與Adobe Commerce的多租使用者服務。 此服務會在Adobe Commerce和Experience Manager之間同步資產。 ARES服務會根據SKU或其他關鍵屬性，自動比對AEM中的資產與Adobe Commerce中的產品。 它也能確保電子商務網站上一律可以使用最新的產品資產和變數。

若要設定服務，您需要使用ARES GraphQL API註冊您的租使用者ID，並選取用於同步資產的相符規則。

## 選擇比對策略

適用於Commerce的AEM Assets整合支援在Adobe Commerce和AEM Assets之間同步資產的兩種比對策略。

- **MatchBySku** — 此為預設比對規則，會根據產品的庫存單位(SKU)比對資產。 SKU是每個產品的唯一識別碼。 此規則會比對資產中繼資料中的SKU與Commerce產品SKU，以確保資產與正確的產品相關聯。

- **ExternalMatcher** — 此比對規則適用於需要自訂比對邏輯的較複雜案例或特定業務需求。 若要使用此規則，您必須在Adobe Developer App Builder中實作自訂程式碼，以定義資產與產品的比對方式。

對於初始入門，請使用`MatchBySku`策略。 如有需要，您稍後可以變更比對策略。

## 註冊租使用者

>[!BEGINSHADEBOX]

**先決條件**

- [AEM Assets專案已設定對應資產所需的Commerce中繼資料](aem-assets-configure-aem.md)。

- [在Adobe Commerce中安裝並設定Experience Manager Assets整合](aem-assets-configure-commerce.md)。

>[!ENDSHADEBOX]

## 收集認證

您需要以下憑證來驗證並連線您的Commerce專案環境和AEM Assets專案環境與Commerce SaaS服務。

| 必要資料 | Source | 在哪裡可以找到它 |
| ---------- | ------ | ------------- |
| 來自Magento帳戶的API金鑰 | Commerce | 提供您正在使用、測試或生產環境的Commerce環境的公開API金鑰。 您可以在[Commerce Service Connector設定](aem-assets-configure-commerce.md#configure-the-commerce-services-connector)頁面的管理員頁面或[!UICONTROL My Account]頁面的[!UICONTROL API Portal]區段中，找到生產和中繼環境的API金鑰。 |
| Commerce SaaS專案識別碼 <ul><li>`magento-environment-Id`</li><li>`Project ID`</li></ul> | Commerce管理員 | 這些值會識別要連線的Commerce環境和SaaS資料空間和專案。 值來自[Commerce服務聯結器SaaS識別碼組態](aem-assets-configure-commerce.md#configure-the-commerce-services-connector)。 |
| AEM `programId`和<br>`environmentId` | [AEM Assets製作環境](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start) | 開啟AEM Sites頁面，然後選取&#x200B;**[!UICONTROL Assets]**。  從URL複製專案和環境ID： <br>`https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/` |
| 基底URL | Commerce店面 | 您的Commerce店面的[基底URL](../stores-purchase/store-urls.md)。 |
| API存取的OAuth認證 | Commerce管理員 | 您可以在Assets整合的Commerce [組態設定](aem-assets-configure-commerce.md#experience-manager-assets-integration-for-adobe-commerce-10-release)中找到這些認證。 |

## 註冊租使用者

透過向Assets規則引擎服務提交請求以新增驗證憑證和租使用者ID，以完成租使用者註冊。 此請求包含建立服務、Commerce專案和Experience Manager Assets專案之間連線所需的憑證和專案識別碼。

使用GraphQL使用者端或cURL傳送請求。

>[!BEGINTABS]

>[!TAB GraphQL要求]

使用GraphQL使用者端傳送POST要求至API端點`https://commerce.adobe.io/assets-integration/graphql`

**必要的標頭**

為請求指定以下HTTP標頭：

- `x-api-key`：來自您Magento帳戶的API金鑰
- `magento-environment-Id`： SaaS識別碼
- `x-gw-signature`：與MAGEID關聯的JWT權杖

**要求：**

**語法**

```graphql
mutation registerTenant($tenantInput: TenantInput!) {
   registerTenant(tenantInput: $tenantInput) {
      tenantId
      userErrors {
         message
         path
      }
    }
}
```

**範例使用方式**

註冊租使用者並選取`matchBySku`規則，以便在Adobe Commerce和AEM Assets專案之間對應資產。

**要求：**

```graphql
   {
      "tenantInput": {
         "enabled": true,
         "projectId": "8231afb6-90cd-65e8-84ba-d9abac0f94e6",
         "aem": {
               "programId": "11111",
               "environmentId": "222222"
         },
         "commerce": {
               "baseUrl": "***",
               "credentials": {
                  "consumerKey": "***",
                  "consumerSecret": "***",
                  "accessToken": "***",
                  "accessTokenSecret": "***"
               }
         },
         "rule": {
            "type": "matchBySKU"
            "matchBySkuRule": {
               "metadataField": "commerce:skus"
            }
         }
      }
   }
```

**回應**

```graphql
{
    "data": {
        "registerTenant": {
            "tenantId": "b65d5da7-2756-46a1-9ff1-14fb5d925fee",
            "userErrors": []
        }
    }
}
```

>[!TAB cURL要求]

```shell
curl --request POST \
  --url https://commerce.adobe.io/assets-integration/graphql \
  --header 'Content-Type: application/json' \
  --header 'Magento-Environment-Id: ****' \
  --header 'x-api-key: ****' \
  --header 'x-gw-signature: *****' \
  --data '{"query":"mutation registerTenant($tenantInput: TenantInput!) {\n\tregisterTenant(tenantInput: $tenantInput) {\n\t\ttenantId\n\t\tuserErrors {\n\t\t\tmessage\n\t\t\tpath\n\t\t}\n\t}\n}\n","operationName":"registerTenant","variables":{"tenantInput":{"enabled":true,"threshold":100,"projectId":"5d6faa03-e200-4623-9008-da144e4eefd8","aem":{"programId":"***","environmentId":"***"},"commerce":{"version":"2.4.6-p2","extensionVersion":"0.0.1","baseUrl":"***","credentials":{"consumerKey":"***","consumerSecret":"***","accessToken":"***","accessTokenSecret":"***"}},"rule":{"type":"matchBySKU","matchBySkuRule":{"metadataField":"commerce:skus"}}}}}'
```

>[!ENDTABS]

### 輸入欄位

#### AemInput

識別用於儲存Commerce資產的AEM Assets執行個體。 您可以從Cloud Manager的「我的程式」檢視或內容製作URL取得此資訊。

| 欄位 | 資料型別 | 說明 |
| ----- | --------- | ----------- |
| `programId` | 字串！ | AEM Cloud Service中專案的唯一識別碼 |
| `environmentId` | 字串！ | 您正在使用的專案環境識別碼，例如，生產、測試或開發 |

#### 商務輸入

此輸入欄位提供用於存取Commerce目錄的API的OAuth驗證認證。 您可以在Assets整合的Commerce [組態設定](aem-assets-configure-commerce.md#experience-manager-assets-integration-for-adobe-commerce-10-release)中找到這些認證。

| 欄位 | 資料型別 | 說明 |
| ----- | --------- | ----------- |
| `baseUrl` | 字串 | 您的Commerce店面的[基底URL](../stores-purchase/store-urls.md)。 |
| `credentials` | [CommerceCredentialsInput](#commercecredentialsinput)！ | 指定存取Commerce執行個體的認證。 |
| `extensionVersion` | 字串 | 選填。 安裝在AEM Assets執行個體上，適用於Commerce擴充功能的Commerce整合版本。 |
| `version` | 字串 | 選填。 Commerce執行個體上安裝的Commerce應用程式版本。 |

#### CommerceCredentialsInput

此輸入欄位提供用於存取Commerce目錄的API的OAuth認證。 您可以在Assets整合的Commerce [組態設定](aem-assets-configure-commerce.md#experience-manager-assets-integration-for-adobe-commerce-10-release)中找到這些認證。

| 欄位 | 資料型別 | 說明 |
| ----- | --------- | ----------- |
| `accessToken` | 字串！ | 為Assets整合產生的存取權杖。 |
| `accessTokenSecret` | 字串！ | 為Assets整合產生的存取權杖密碼。 |
| `consumerKey` | 字串！ | 為Assets整合產生的消費者金鑰。 |
| `consumerSecret` | 字串！ | 為Assets整合產生的消費者機密。 |

#### ExternalMatcherInput

| 欄位 | 資料型別 | 說明 |
| ----- | --------- | ----------- |
| assetToProductUrl | 字串！ | <!--Add field description--> |
| productToAssetUrl | 字串！ | <!--Add field description--> |
| 認證 | [ExternalMatcherCredentialsInput](#externalmatchercredentials)！ | 用於存取App Builder專案，以進行Commerce的AEM Assets整合的認證。 |

#### ExternalMatcherCredentials

| 欄位 | 資料型別 | 說明 |
| ----- | --------- | ----------- |
| `oauthServerUrl` | 字串！ |    |
| `clientId` | 字串！ |      |
| `clientSecret` | 字串！ |    |
| `imsOrgId` | 字串！ | 布建AEM Assets和Adobe Commerce的IMS組織。 |

#### MatchBySkuRuleInput

| 欄位 | 資料型別 | 說明 |
| ----- | --------- | ----------- |
| metadataField | 字串！ | 指定用於比對的資產中繼資料欄位。 使用`commerce:skus` |

#### 規則輸入

指定用於在Adobe Commerce和AEM Assets之間同步資產的比對規則。

| 欄位 | 資料型別 | 說明 |
| ----- | --------- | ----------- |
| externalMatcher | [ExternalMatcherInput](#externalmatcherinput) | 選取externalMatcher規則以進行資產比對，並指定使用該規則所需的資料。 |
| MatchBySkuRule | [MatchBySkuRuleInput](#matchbyskuruleinput) | 選取MatchBySkuRule以進行資產比對，並指定使用該比對所需的資料。 |

#### RuleTypeInput

| 欄位 | 資料型別 | 說明 |
| ----- | --------- | ----------- |
| 規則型別 | 列舉 | 指定可用於Commerce的AEM Assets整合的資產比對規則清單。 可用的值為`matchBySKU`或`externalMatcher`。 |

#### TenantInput

| 欄位 | 資料型別 | 說明 |
| ----- | --------- | ----------- |
| `aem` | [AemInput！](#aeminput) | 在AEM Cloud Service中識別您儲存AEM Assets資產的Commerce執行個體。 |
| `commerce` | [商務輸入！](#commerceinput) | 提供Commerce專案資訊和API存取認證 |
| `enabled` | 布林值！ | 啟用或停用Adobe Commerce與AEM Assets之間的資產同步。 |
| `projectId` | 字串！ | 來自[Commerce服務聯結器SaaS識別碼組態](aem-assets-configure-commerce.md#configure-the-commerce-services-connector)的SaaS專案Id。 |
| `rule` | [規則輸入！](#ruleinput) | 指定用於在Adobe Commerce和AEM Assets之間同步資產的比對規則。 指定`[matchBySkuRule](#matchbyskuruleinput)`或`[externalMatcher](#externalmatcherinput)`。 |

### 輸出欄位

| 欄位 | 資料型別 | 說明 |
| ----- | --------- | ----------- |
| 資料 | [registerTenant] | 傳回租使用者註冊資訊和來自伺服器的任何錯誤訊息。 |

#### RegisterTenantResponse

| 欄位 | 資料型別 | 說明 |
| ----- | --------- | ----------- |
| tenantId | 字串！ | 傳回已註冊的租使用者ID。 此ID可確保從與Commerce環境相關聯的SaaS資料空間中，儲存及擷取Commerce適用的AEM Assets整合資料。 |
| userError | [[使用者錯誤！]！](#usererror) | 傳回要求產生的任何錯誤訊息。 |

#### 使用者錯誤

| 錯誤 | 說明 |
|:------|:------------|
| `IMS Org ID not associated to this Commerce` | 如果未將`Magento-Environment-Id`標頭中指定的環境ID指派給IMS帳戶，則會發生此錯誤。 發生此錯誤的原因可能是，為Commerce執行個體設定[Commerce服務聯結器](aem-assets-configure-commerce.md#configure-the-commerce-services-connector)時，IMS帳戶未連線。 |
| `Client ID is invalid` | `x-api-key`標頭不正確。 |
| `Client ID is missing` | 未提供`x-api-key`標頭。 |
| `JWT is required` | 未提供`x-gw-signature`標頭。 |
| `JWT is invalid` | 未提供`x-gw-signature`標頭。 |
| `Tenant already exists` | 具有特定`mageID` （取自JWT權杖）和`saasId` （由`Magento-Environment-Id`標頭提供）的租使用者已註冊。 |
| `Unexpected error when connecting with AEM Assets` | 發生此錯誤的原因是`programId`或`environmentId`值無效或不存在。 |
| `Unable to connect with AEM Assets` | 這個錯誤有兩個可能的原因：<br>1。 AEM資產帳戶與Adobe Commerce所提供的IMS組織ID不同，而是與該IMS組織ID相關聯。<br>2。 `commerce:isCommerce`中繼資料不存在於AEM Assets中，這表示沒有任何核准的資產可從AEM Assets傳送至Commerce執行個體。 |
| `Unexpected error when connecting with Commerce` | 當提供無效的商務`baseURL`時，就會發生此錯誤。 |
| `Unable to connect with Commerce, unauthorized` | 提供的商務認證無效，導致未獲授權的存取。 |
| `Invalid rule. The value must be matchBySKU or externalMatcher` | `Rule`欄位包含不正確的值。 對於RegisterTenant要求，可用的規則型別由[RuleTypeInput](#ruletypeinput)列舉定義。 |

## 啟用Experience Manager Assets整合

註冊租使用者後，上線流程的最後一步是在管理員中啟用Commerce適用的Experience Manager Assets整合擴充功能。

1. 啟用擴充功能。

   1. 移至&#x200B;**商店** >設定> **設定** > **目錄**。

   1. 選取&#x200B;**[!UICONTROL Catalog]**&#x200B;以開啟目錄組態。

   1. 展開&#x200B;**[!UICONTROL AEM Assets integration]**。

   1. 將&#x200B;**[!UICONTROL Integration enabled]**&#x200B;設為`yes`。

      適用於Commerce管理員設定的![AEM Assets整合](assets/aem-integration-admin-enable.png){width="600" zoomable="yes"}
