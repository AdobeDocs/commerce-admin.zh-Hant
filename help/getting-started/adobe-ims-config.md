---
title: 使用ID設定Commerce管理整合
description: 請依照此選擇性程式，將Adobe Commerce管理員使用者帳戶登入與Adobe ID整合。
exl-id: 518b7c21-e6b3-47d7-81a5-c34fbe0f197c
feature: Identity Management
source-git-commit: 20b2560ce2b8071c740907292544519f8b1c3ddf
workflow-type: tm+mt
source-wordcount: '758'
ht-degree: 1%

---

# 使用Adobe ID設定Commerce管理整合

{{ee-feature}}

這項整合可支援具有Adobe ID且想要簡化登入Adobe Commerce和Adobe商業產品之管理員使用者的Commerce商家。 這是選用專案，會根據執行個體來啟用。 啟用時，只有管理員使用者工作流程會受到影響。 

>[!IMPORTANT]
>
>管理員使用者在啟用這項整合之前，應儲存其Commerce管理員憑證（使用者名稱和密碼）和2FA憑證。 如果停用IMS整合，則需要這些認證。

## 必要條件

* Adobe Commerce 2.4.5或更新版本
* Adobe.com帳戶，可存取 [Adobe Admin Console](https://adminconsole.adobe.com/).

設定此整合的管理員在啟用模組期間需要下列認證：

* 組織ID (取得自 [Adobe Admin Console](https://adminconsole.adobe.com/))，長度必須至少為24個字元。 已驗證的使用者必須屬於此IMS組織。 如需尋找組織ID的相關資訊，請參閱 [Experience Cloud中的組織](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html).
* 2FA應在Adobe Admin Console中的組織層級強制執行，以啟用此模組。 檢查 [驗證設定](https://helpx.adobe.com/enterprise/using/authentication-settings.html#two-step-verification).
* 使用者端ID
* 使用者端密碼
* 從擷取API金鑰後，即可使用使用者端ID和使用者端密碼 [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/credentials/).

Commerce管理員使用者必須以Adobe ID建立帳戶才能登入。

## 一般步驟

* 從取得Adobe組織ID [Adobe Admin Console](https://adminconsole.adobe.com/)
* 從產生新專案、IMS API金鑰和密碼 [Adobe Developer Console](https://developer.adobe.com/)
* 啟用 `AdminAdobeIms` 模組
* 在Adobe Admin Console中設定Adobe Commerce使用者。

若要成功整合，所有Adobe Commerce使用者都必須擁有具有相同名稱和主要電子郵件地址的管理員使用者帳戶。 如果相符的Admin使用者帳戶不存在，則具有所需許可權（通常被指派為Administrator角色）的使用者必須手動進行 [建立管理員使用者帳戶](../systems/permissions-users-all.md#create-a-user) 和電子郵件相同名稱。

## 設定整合

具有系統存取權的管理員或開發人員完成下列步驟後， _[!UICONTROL Sign into Adobe Commerce with Adobe IMS]_按鈕會顯示在所有管理員使用者的Commerce管理員登入頁面中。

### 步驟1：取得Adobe組織ID

至少需要一個IMS組織的成員資格才能啟用此功能。 如果您有Adobe ID，依預設您至少屬於一個Adobe組織。 登入 [Adobe Admin Console](https://adminconsole.adobe.com/) 以擷取您的組織ID。

### 步驟2：產生新專案、IMS API金鑰和密碼

若要為組織建立專案，組織的Adobe管理員帳戶必須具有系統管理員或開發人員角色。 請參閱 [開發人員控制檯指南](https://developer.adobe.com/developer-console/docs/guides/projects/).

1. 登入 [Adobe Developer Console](https://developer.adobe.com/).
1. 前往 **[!UICONTROL Projects]** 索引標籤(adobe.io/projects)並按一下 **[!UICONTROL Create a new project]**.
1. 按一下 **[!UICONTROL Add API]** 在新建立的專案頁面上。
1. 選取 **[!UICONTROL Adobe Services]** > **[!UICONTROL Adobe Commerce with Adobe ID]**.
1. 選取 **[!UICONTROL Oauth 2.0 Web]**.
1. 指定 **[!UICONTROL Redirect URI]**： `https://<hostname>/`
1. 指定 **[!UICONTROL Redirect URI pattern]**： `https://<hostname>/.*`

   在主機名稱前面加上句點，以逸出任何句點 `\\`. 在URL結尾新增萬用字元可支援Adobe Commerce管理員秘密金鑰。

1. 按一下 **[!UICONTROL Save configured API]**.
1. 複製 [!UICONTROL Client ID] 和 [!UICONTROL Client Secret] 金鑰從建立的專案中。

### 步驟3：啟用AdminAdobeIms模組

此 `AdminAdobeIms` 模組負責Adobe Commerce/Adobe IMS整合。 設定新專案並複製組織ID、使用者端ID和使用者端密碼後，您可以啟用 `AdminAdobeIms` 模組。

輸入 `bin/magento admin:adobe-ims:enable`. 系統會提示您輸入下列引數。 使用專案建立期間產生的值。

* 組織ID
* 使用者端ID
* 使用者端密碼
* 2FA已啟用

Adobe Commerce會顯示訊息，指出啟用是成功還是失敗。

成功啟用此功能後，您可以將其他Adobe Commerce使用者帳戶轉移至Adobe IMS帳戶。 Adobe Commerce使用者必須屬於已設定的Adobe組織，才能使用Adobe ID登入。

### 步驟4：在Adobe Admin Console中設定Adobe Commerce使用者

成功啟用此功能後，您可以將其他Adobe Commerce使用者帳戶轉移至Adobe IMS帳戶。 Adobe Commerce使用者必須至少屬於一個Adobe組織，才能使用Adobe ID登入。

1. 在 [Admin Console](https://helpx.adobe.com/tw/enterprise/using/admin-console.html)，導覽至 **[!UICONTROL Users]**  > **[!UICONTROL Users]**.

1. 按一下 **[!UICONTROL Add User]**.

1. 輸入使用者的電子郵件地址。

   如果適用，系統會自動填入建議的ID型別。 您可以根據貴組織的購買計畫，將此設定變更為清單中的其中一個產品ID。

   您一次最多可以新增10個使用者。 若要新增更多變更，請在儲存變更後重複上述步驟。

1. 按一下 **[!UICONTROL Save]**.

使用者新增並顯示在 [!UICONTROL Users] 清單。
