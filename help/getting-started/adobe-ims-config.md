---
title: 使用ID設定Commerce管理整合
description: 請依照此選擇性程式，將Adobe Commerce管理員使用者帳戶登入與Adobe ID整合。
exl-id: 518b7c21-e6b3-47d7-81a5-c34fbe0f197c
feature: Identity Management
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"
source-git-commit: a71f3ba94229c402421ee476c37cfcbfd88a26c7
workflow-type: tm+mt
source-wordcount: '817'
ht-degree: 0%

---

# 使用Adobe ID設定Commerce管理整合

{{ee-feature}}

這項整合可支援具有Adobe ID且想要簡化登入Commerce和Adobe商業產品之管理員使用者的Adobe Commerce商家。 這是選用專案，會根據執行個體來啟用。 啟用時，只有管理員使用者工作流程會受到影響。 

>[!IMPORTANT]
>
>管理員使用者在啟用這項整合之前，應儲存其Commerce管理員憑證（使用者名稱和密碼）和2FA憑證。 如果停用IMS整合，則需要這些認證。

## 先決條件

* Adobe Commerce 2.4.5或更新版本
* 具有存取[Adobe Admin Console](https://adminconsole.adobe.com/)許可權的Adobe.com帳戶。

設定此整合的管理員在啟用模組期間需要下列認證：

* 組織ID (取自[Adobe Admin Console](https://adminconsole.adobe.com/))，長度必須至少為24個字元。 已驗證的使用者必須屬於此IMS組織。 如需尋找組織ID的相關資訊，請參閱[Experience Cloud中的組織](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html)。
* 2FA應在Adobe Admin Console中的組織層級強制執行，以啟用此模組。 檢查[驗證設定](https://helpx.adobe.com/enterprise/using/authentication-settings.html#two-step-verification)。
* 使用者端ID
* 使用者端密碼
* 從[Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/credentials/)擷取API金鑰後，即可使用使用者端ID和使用者端密碼。

Commerce管理員使用者必須以Adobe ID建立帳戶才能登入。

## 一般步驟

* 從[Adobe Admin Console](https://adminconsole.adobe.com/)取得Adobe組織ID
* 從[Adobe Developer Console](https://developer.adobe.com/)產生新專案、IMS API金鑰和密碼
* 在Adobe Admin Console中設定Adobe Commerce使用者
* 啟用`AdminAdobeIms`模組。

若要成功整合，所有Adobe Commerce使用者都必須擁有具有相同名稱和主要電子郵件地址的管理員使用者帳戶。 如果相符的管理員使用者帳戶不存在，則具有所需許可權（通常指派為管理員角色）的使用者必須手動[建立具有相同名稱和電子郵件的管理員使用者帳戶](../systems/permissions-users-all.md#create-a-user)。

## 設定整合

具有系統存取權的管理員或開發人員完成下列步驟後，_[!UICONTROL Sign into Adobe Commerce with Adobe IMS]_&#x200B;按鈕會顯示在所有管理員使用者的Commerce管理員登入頁面中。

### 步驟1：取得Adobe組織ID

至少需要一個IMS組織的成員資格才能啟用此功能。 如果您有Adobe ID，依預設您至少屬於一個Adobe組織。 登入[Adobe Admin Console](https://adminconsole.adobe.com/)以擷取您的組織識別碼。

### 步驟2：產生新專案、IMS API金鑰和密碼

若要為組織建立專案，組織的Adobe管理員帳戶必須具有系統管理員或開發人員角色。 請參閱[Developer Console指南](https://developer.adobe.com/developer-console/docs/guides/projects/)。

1. 登入[Adobe Developer Console](https://developer.adobe.com/)。
1. 前往&#x200B;**[!UICONTROL Projects]**&#x200B;標籤(adobe.io/projects)並按一下&#x200B;**[!UICONTROL Create a new project]**。
1. 在新建立的專案頁面上按一下&#x200B;**[!UICONTROL Add API]**。
1. 選取&#x200B;**[!UICONTROL Adobe Services]** > **[!UICONTROL Adobe Commerce with Adobe ID]**。
1. 選取&#x200B;**[!UICONTROL Oauth 2.0 Web]**。
1. 指定&#x200B;**[!UICONTROL Redirect URI]**： `https://<commerce_base_url>/`
1. 指定&#x200B;**[!UICONTROL Redirect URI pattern]**： `https://<commerce_base_url>/.*`

   藉由在點前面加上`\\`來逸出主機名稱中的任何點。 在URL結尾新增萬用字元可支援Adobe Commerce管理員秘密金鑰。

1. 按一下&#x200B;**[!UICONTROL Save configured API]**。
1. 從建立的專案複製[!UICONTROL Client ID]和[!UICONTROL Client Secret]金鑰。

### 步驟3：在Adobe Admin Console中設定Adobe Commerce使用者

在啟用整合之前，請確認每個Adobe Commerce管理員使用者帳戶都有對應的Adobe IMS帳戶。 Adobe Commerce使用者必須屬於特定的Adobe組織，才能使用Adobe ID登入。

>[!TIP]
>
>您可以從CSV檔案上傳使用者資訊，以建立多個使用者帳戶。 請參閱[管理多個使用者](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html)。

1. 在[Adobe Admin Console](https://helpx.adobe.com/tw/enterprise/using/admin-console.html)中，導覽至&#x200B;**[!UICONTROL Users]** > **[!UICONTROL Users]**。

1. 按一下&#x200B;**[!UICONTROL Add User]**。

1. 輸入使用者的電子郵件地址。

   如果適用，系統會自動填入建議的ID型別。 您可以根據貴組織的購買計畫，將此設定變更為清單中的其中一個產品ID。

   您一次最多可以新增10個使用者。 若要新增更多變更，請在儲存變更後重複上述步驟。

1. 按一下&#x200B;**[!UICONTROL Save]**。

使用者已新增並顯示在[!UICONTROL Users]清單中。

### 步驟4：啟用AdminAdobeIms模組

`AdminAdobeIms`模組負責Adobe Commerce/Adobe IMS整合。 設定新專案並複製您的組織ID、使用者端ID和使用者端密碼後，您可以啟用`AdminAdobeIms`模組。

輸入`bin/magento admin:adobe-ims:enable`。 系統會提示您輸入下列引數。 使用專案建立期間產生的值。

* 組織ID
* 使用者端ID
* 使用者端密碼
* 2FA已啟用

Adobe Commerce會顯示訊息，指出啟用是成功還是失敗。

成功啟用此功能後，您可以將其他Adobe Commerce使用者帳戶轉移至Adobe IMS帳戶。 Adobe Commerce使用者必須屬於已設定的Adobe組織，才能使用Adobe ID登入。

## 身分識別與單一登入

如需有關身分設定選項(包括Adobe ID、Enterprise ID和Federated ID)的資訊，以及設定單一登入(SSO)以安全存取Adobe應用程式的指示，請參閱[企業Admin Console](https://helpx.adobe.com/enterprise/using/set-up-identity.html)檔案中的&#x200B;*設定身分和單一登入*。
