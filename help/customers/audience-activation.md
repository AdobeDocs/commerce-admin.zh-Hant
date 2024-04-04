---
title: "[!DNL Audience Activation]"
description: 瞭解如何在Adobe Commerce中啟用Real-Time CDP對象，以推動商店中的個人化。
exl-id: b53908f2-c0c1-42ad-bb9e-c762804a744b
feature: Customers, Configuration, Personalization
topic: Commerce, Personalization
level: Experienced
source-git-commit: d1079c8eac20c08a17af1f72bf49b6cb859c0699
workflow-type: tm+mt
source-wordcount: '1422'
ht-degree: 0%

---

# [!DNL Audience Activation]

此 [!DNL Audience Activation] 擴充功能可讓您在Adobe Commerce中啟用Real-Time CDP對象，以在購物車中建立唯一優惠方案。 這些優惠和獎勵包括常見的電子商務銷售技術，例如 _購買2得到1免費_、以該客戶為目標的英雄橫幅，以及透過各種選件修改產品定價。 在Real-Time CDP中建立的受眾是以來自各種企業系統的資料為基礎，例如企業資源規劃(ERP)、客戶關係管理(CRM)、銷售點和行銷系統。 由於客戶區段資訊會持續更新，因此當客戶在您的商店購物時，他們可能會與區段建立關聯或解除關聯。

您可以在Luma店面中啟用受眾或 [headless](#headless-support) 店面。 在Luma店面中，對象資訊（區段會籍）會儲存在商務端的Cookie中。 在Headless店面中，受眾資訊會作為引數傳遞到GraphQL API標題，命名為： `aep-segments-membership`.

## 發行說明

本節包含Audience Activation擴充功能更新的相關資訊，並包含：

![新增](../assets/new.svg)  — 新功能
![修正](../assets/fix.svg)  — 修正和改良
![錯誤](../assets/bug.svg)  — 已知問題

另請參閱 [即將發行的版本](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) 以瞭解發行排程和支援。

請參閱開發人員檔案以 [瞭解產品相容性](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html).

## 支援的服務更新

以下發行說明說明說明說明Audience Activation所用擴充功能的相關功能變更和修正。

+++支援的服務更新

_2023年8月15日_

![修正](../assets/fix.svg)  — 已更新 [Real-Time CDP Audiences控制面板](#real-time-cdp-audiences-dashboard) 以簡化篩選。

_2023年6月27日_

![修正](../assets/fix.svg)  — 在中新增PHP 8.2支援 `magento/module-data-services-graphql` 封裝。

_2023年5月30日_

![新增](../assets/new.svg)  — 已更新 [Real-Time CDP Audiences控制面板](#real-time-cdp-audiences-dashboard) 包含在Adobe Commerce例項中排序、搜尋及篩選作用中對象的能力。

+++

### 2.1.1

[!BADGE 相容性]{type=Informative tooltip="相容性"}

_2024年4月4日_

![新增](../assets/new.svg)  — 新增對PHP 8.3的支援。

### 2.2.0-beta1

[!BADGE 相容性]{type=Informative tooltip="相容性"}

_2024年2月16日_

![新增](../assets/new.svg)  — 如果您正在參與Beta版測試，請確定您的 `composer.json` 檔案的根層級如下： ` "minimum-stability": "beta"`.
![新增](../assets/new.svg) - (**測試版**)已新增建立功能 [相關產品規則](../merchandising-promotions/product-related-rule-create.md) 由受眾通知。

### 2.1.0

[!BADGE 相容性]{type=Informative tooltip="相容性"}

_2024年1月24日_

![新增](../assets/new.svg)  — 已更新 [Real-Time CDP Audiences控制面板](#real-time-cdp-audiences-dashboard) 以納入包含對象的網站，並指定要將哪些動態區塊和購物車價格規則設定為使用這些對象。

### 2.0.1

[!BADGE 相容性]{type=Informative tooltip="相容性"}

_2023年11月16日_

![修正](../assets/fix.svg)  — 改善穩定性。

### 2.0.0

[!BADGE 相容性]{type=Informative tooltip="相容性"}

_2023年10月10日_

![新增](../assets/new.svg)  — 新增當您使用OAuth 2.0時 [設定](#configure-the-extension) Audience Activation擴充功能。
![修正](../assets/fix.svg)  — 改善穩定性。

### 1.2.0

[!BADGE 相容性]{type=Informative tooltip="相容性"}

_2023年8月15日_

![修正](../assets/fix.svg)  — 更新UI元件版本。

### 1.1.0

_2023年5月30日_

[!BADGE 相容性]{type=Informative tooltip="相容性"}

![新增](../assets/new.svg)  — 新增的支援 [動態區塊](#headless-support) 在headless店面。

### 1.0.1

_2023年5月11日_

[!BADGE 相容性]{type=Informative tooltip="相容性"}

![修正](../assets/fix.svg)  — 修正動態區塊或購物車價格規則未套用至店面的問題。
![修正](../assets/fix.svg)  — 修正商戶嘗試建立或更新動態區塊時，未設定的Audience Activation擴充功能安裝導致錯誤的問題。

### 1.0.0

_2023年3月31日_

[!BADGE 相容性]{type=Informative tooltip="相容性"}

![新增](../assets/new.svg)  — 正式發行版本

## 實施

以下工作同時適用於Luma和Headless店面實施。 若要在Adobe Commerce中啟用對象，您必須：

- 安裝Adobe Commerce 2.4.4版或更高版本
- [啟動](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html) Adobe Commerce作為Real-Time CDP中的目的地
- [安裝](#install-the-extension) 此 [!DNL Audience Activation] Admin中的擴充功能
- [設定](#configure-the-extension) 此 [!DNL Audience Activation] Admin中的擴充功能

### 安裝擴充功能

安裝 [!DNL Audience Activation] 擴充功能來自 [marketplace](https://commercemarketplace.adobe.com/magento-audiences.html)，或執行以下命令：

```bash
composer require magento/audiences
```

### 設定擴充功能

安裝之後 [!DNL Audience Activation] 擴充功能上，您必須登入Commerce管理員並完成下列專案：

1. 在 _管理員_ 側欄，前往 **[!UICONTROL System]** > _[!UICONTROL Services]_>**[!UICONTROL Commerce Services Connector]**.

1. [登入](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html#organizationid) 至您的Adobe帳戶，並選取您的組織ID。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL System]** > _[!UICONTROL Services]_>**[!UICONTROL [!DNL Data Connection]]**.

1. 在 **[!UICONTROL Datastream ID]** 欄位，貼上您建立之資料流的ID。 [已啟用](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html#parameters) Adobe Commerce作為Real-Time CDP中的目的地。

   此資料流會從您的Commerce網站傳送資料至Real-Time CDP，以判斷購物者是否屬於對象。 如果您尚未建立資料串流， [建立](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html#create) 一個Experience Platform， [新增](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html) 前往Real-Time CDP中的Commerce目的地，然後前往 [[!DNL Data Connection]](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#data-collection) Admin中的擴充功能。

   >[!NOTE]
   >
   >當您指定資料串流ID時， [將其與特定網站建立關聯](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#data-collection) 在 [!DNL Data Connection] 副檔名。 如果您的Commerce商店有多個網站， [建立目的地](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html) Real-Time CDP中的每一個網站，並為每個網站使用不同的資料流ID。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 展開 **[!UICONTROL Services]** 並選取 **[!UICONTROL [!DNL Data Connection]]**.

1. [新增](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#add-service-account-and-credential-details) 服務帳戶和認證詳細資料。

## 在Commerce中的何處使用Real-Time CDP受眾

使用 [!DNL Audience Activation] 擴充功能已啟用，您可以：

- [建立購物車價格規則](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences) 由受眾通知
- [建立動態區塊](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks) 由受眾通知
- [(**測試版**)建立相關的產品規則](../merchandising-promotions/product-related-rule-create.md) 由受眾通知

## Real-Time CDP受眾控制面板

您可以檢視全部 [主要](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-edge-personalization-destinations.html) 可在您的Adobe Commerce執行個體中使用 **Real-Time CDP受眾** 儀表板。

若要存取 **Real-Time CDP受眾** 儀表板，前往 _管理員_ 側欄，然後前往 **[!UICONTROL Customers]** > **[!UICONTROL Real-time CDP Audience]**.

![Real-Time CDP受眾控制面板](./assets/real-time-cdp-dashboard.png){width="700" zoomable="yes"}

儀表板包含下列欄位：

| 欄 | 說明 |
|--- |--- |
| `Hide filters` | 可讓您顯示或隱藏可套用至控制面板的任何篩選器。 目前，您唯一可套用的篩選器是 `Last updated`. 此篩選器可讓您根據上次更新對象的時間來選取對象的日期範圍。 |
| `Search` | 可讓您在商務例項中搜尋作用中對象。 |
| `Name` | 在Real-Time CDP中提供給對象的名稱。 |
| `Origin` | 指出受眾來源，例如 `Experience Platform`. |
| `Websites` | 指出哪些網站已設定為可使用對象。 |
| `Dynamic Blocks` | 指出哪些動態區塊已設定為可使用對象。 |
| `Cart Price Rules` | 指出哪些購物車價格規則已設定為使用對象。 |
| `Last updated` | 表示對象在Real-Time CDP中的修改時間。 |
| `Sync now` | 從Real-Time CDP擷取新的或更新對象。 |
| `Customize table` | 可讓您顯示或隱藏 `Origin`， `Websites`， `Dynamic Blocks`， `Cart Price Rules`、和 `Last updated` 欄。 |

{style="table-layout:auto"}

## Headless支援

您可以在Headless Adobe Commerce例項(例如AEM和PWA)中啟用對象，以根據對象顯示購物車價格規則、相關產品規則或動態區塊。

### 購物車價格規則和相關產品規則

Experience Platform針對購物車價格規則和相關產品規則，Headless店面會透過 [Commerce integration framework(CIF)](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/content-and-commerce/integrations/magento.html). 此架構提供使用GraphQL實作的伺服器端API。 對象資訊（例如購物者的區段）會透過名為的GraphQL標題引數傳遞至Commerce： `aep-segments-membership`.

整體架構如下：

![將資料從Headless店面傳送到後端](./assets/aem-commerce-architecture.png){width="700" zoomable="yes"}

在您之後 [安裝](#install-the-extension) 和 [設定](#configure-the-extension) 擴充功能Experience Platform Web SDK包含對象資訊，其形式為區段會籍。

若要從SDK擷取這些區段會籍，請參閱此 [程式碼片段](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/custom-personalization.html#example-response-for-custom-personalization-with-attributes).

擷取區段後，您可以在GraphQL標題中將這些區段傳遞至Commerce。 例如：

```bash
curl 'http://magento.config/graphql' -H 'Authorization: Bearer abc123' -H 'aep-segments-membership: urlencoded_list_of_segments' -H 'Content-Type: application/json' --data-binary '{"query":"query {\ncustomer {\nfirstname\nlastname\nemail\n}\n}"}'
```

### 動態區塊

對於動態區塊，請使用GraphQL `dynamicBlocks` 查詢可包含 `audience_id` 輸入屬性。 如果您指定一或多個 `audience_id` 中的值 `dynamicBlocks` 查詢後，系統會傳回指派給這些對象的動態區塊清單。

#### 使用範例

下列查詢會傳回與多個對象ID相關聯的所有動態區塊。

**要求：**

```graphql
{
  dynamicBlocks(input:
  {
    type: SPECIFIED
    audience_id: {
      in: [
        "cd29a789-9be8-40ad-a1ef-640c33b3742e"
        "92c3e14d-c72b-40d0-96b7-b96801dcc135"
      ]
    }
  })
  {
    items {
      uid
      audience_id
      content {
        html
      }
    }
    page_info {
      current_page
      page_size
      total_pages
    }
    total_count
  }
}
```

**回應：**

```json
{
  "data": {
    "dynamicBlocks": {
      "items": [
        {
          "uid": "MQ==",
          "audience_id": [
            "cd29a789-9be8-40ad-a1ef-640c33b3742e"
          ],
          "content": {
            "html": "<h2><strong>SAVE 20%</strong></h2>\r\n<p>(some restrictions apply)</p>\r\n<p>&nbsp;</p>"
          }
        },
        {
          "uid": "Mg==",
          "audience_id": [
            "cd29a789-9be8-40ad-a1ef-640c33b3742e",
            "92c3e14d-c72b-40d0-96b7-b96801dcc135"
          ],
          "content": {
            "html": "<p><img src=\"{{media url=&quot;wysiwyg/save20.png&quot;}}\" alt=\"save 20% red\"></p>"
          }
        }
      ],
      "page_info": {
        "current_page": 1,
        "page_size": 20,
        "total_pages": 1
      },
      "total_count": 2
    }
  }
}
```

進一步瞭解 `dynamicBlocks` 中的GraphQL查詢 [開發人員檔案](https://developer.adobe.com/commerce/webapi/graphql/schema/store/queries/dynamic-blocks/).

## 使用Adobe Experience Platform Mobile SDK擷取對象

您可以使用Adobe Experience Platform Mobile SDK擷取Real-Time CDP閱聽眾。

1. [安裝](#install-the-extension) Audience Activation擴充功能。
1. [為您的行動Commerce網站安裝並設定SDK](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/mobile-sdk-epc.html).

>[!IMPORTANT]
>
>適用於iOS的Adobe Experience Platform Mobile SDK支援iOS 11或更新版本。

完成設定後，請使用行動SDK操作來擷取受眾資料。 例如：

```swift
Edge.sendEvent(experienceEvent: experienceEvent) { (handles: [EdgeEventHandle]) in
    for handle in handles {
        if handle.type == "activation:pull" {
        let payloadItems = handle.payload ?? []
            for payloadItem in payloadItems {
                if let segments = payloadItem["segments"] as? any Sequence {
                    var segmentsArr = [Any]()
                    for segment in segments {
                        let response = segment as AnyObject?
                        segmentsArr.append(response?.object(forKey: "id")! ?? "")
                    }
                    print("Saving segments ->  \(segments)")
                    storage.set(segmentsArr, forKey: "segments")
                    print("End saving segments")
                }
         
                // Show segments
                let rSegments = storage.object(forKey: "segments") ?? nil;
                print("Retrieving segments -> \(rSegments)")
            }
        }
    }
}
```

擷取資料後，您可使用資料建立受眾資訊 [購物車價格規則](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences)， [動態區塊](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks) 和  [相關產品規則](../merchandising-promotions/product-related-rule-create.md) 在商務應用程式中。

## 對象不會顯示在商務中

如果Real-Time CDP對象未顯示在Commerce中，原因可能是：

- 在中選取的驗證型別不正確 **資料連線** 設定頁面
- 產生的權杖上的許可權不足

以下兩節說明如何疑難排解任一案例。

### 設定中選取的驗證型別不正確

1. 開啟您的Commerce例項。
1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.
1. 展開 **[!UICONTROL Services]** 並選取 **[!UICONTROL [!DNL Data Connection]]**.
1. 確定您指定的伺服器對伺服器授權方法 **[!UICONTROL Authentication Type]** 欄位正確。 Adobe建議使用 **OAuth**. 已棄用JWT。 [瞭解更多](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/).

### 產生的權杖上的許可權不足

此問題可能是由於所產生Token的API許可權不足所導致。 若要確保權杖具有正確的許可權：

1. 識別組織中Adobe Experience Platform的系統管理員。
1. 尋找您將使用的專案和認證。
1. 識別技術帳戶電子郵件，例如： `fe3c9476-1234-1234-abcd-2a51a785009a@techacct.adobe.com`.
1. 請系統管理員啟動Adobe Experience Platform並前往 **[!UICONTROL Permissions]** -> **[!UICONTROL Users]** -> **[!UICONTROL API credentials]**.
1. 使用上方的技術帳戶電子郵件，搜尋要修改的認證。
1. 開啟認證，然後選取 **[!UICONTROL Roles]** -> **[!UICONTROL Add roles]**.
1. 新增 **全部生產存取權**.
1. 按一下 **[!UICONTROL Save]**.
1. [重新產生](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html#generate-access-token) 控制檯中的存取權杖。
1. 使用，驗證權杖是否提供有效的回應 [Target連線API](https://developer.adobe.com/experience-platform-apis/references/destinations/#tag/Target-connections/operation/getTargetConnections).
