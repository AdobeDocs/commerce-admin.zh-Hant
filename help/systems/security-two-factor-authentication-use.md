---
title: 使用者帳戶的雙因素驗證設定
description: 瞭解如何在管理員初次登入期間設定雙因素驗證，並使用支援的裝置應用程式驗證您的身分。
exl-id: 1ea7f09e-4753-40fa-b9d4-376ba5d8f58f
role: Admin, User
feature: Configuration, Security, User Account
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hant/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 0%

---

# 使用者帳戶的雙因素驗證設定

這些指示顯示如何在您首次登入Adobe Commerce或Magento Open Source期間設定雙因素驗證，以及如何使用下列應用程式和裝置驗證您的身分。

如需完整的指示，請參閱[管理員登入](../getting-started/admin-signin.md)。

>[!NOTE]
>
>已啟用[!DNL Adobe Identity Management Services] (IMS)驗證的存放區已停用原生Adobe Commerce和Magento Open Source 2FA。 使用其Adobe憑證登入其Commerce執行個體的管理員使用者，不需要重新驗證許多管理員工作。 當管理員使用者登入目前的工作階段時，驗證會由Adobe IMS處理。 請參閱[[!DNL Adobe Identity Management Service] (IMS)整合概述](../getting-started/adobe-ims-integration-overview.md)。

## [!DNL Google Authenticator]

### 步驟1：設定[!DNL Google Authenticator]

1. 輸入您的帳戶認證，並登入&#x200B;_管理員_。 會出現一個包含QR碼的新驗證器畫面。

1. 在您的行動裝置上開啟&#x200B;**[!UICONTROL Google Authenticator]**&#x200B;應用程式。

1. 按一下加號( **+** )以新增專案，並將紅色方塊與QR碼對齊，以便使用智慧型手機上的相機進行掃描。

1. 當您的電話辨識QR碼並新增專案時，請在&#x200B;_管理員_ **[!UICONTROL Authenticator code]**&#x200B;欄位中輸入該6位數的代碼。

1. 完成時，按一下&#x200B;**[!UICONTROL Confirm]**。

   ![Google Authenticator QR碼](./assets/storefront-2fa-google-qrcode.png){width="300"}

### 步驟2：使用[!DNL Google Authenticator]登入

1. 輸入您的帳戶認證，並登入Commerce _管理員_。

   ![Google Authenticator — 登入](./assets/storefront-2fa-google-code.png){width="300"}

1. 在您的行動裝置上開啟[!DNL Google Authenticator]。

1. 出現提示時，請輸入六位數的驗證代碼。

1. 若要儲存驗證以供日後登入，請選取&#x200B;**[!UICONTROL Trust this device, do not ask again]**&#x200B;核取方塊。

1. 完成時，按一下&#x200B;**[!UICONTROL Confirm]**。

## [!DNL Duo Security]

[!DNL Duo]提供免費試用版，並根據帳戶相關聯的使用者人數收費。 按照他們的[指示設定您的帳戶並下載應用程式](https://duo.com/product/multi-factor-authentication-mfa/duo-mobile-app)。

### 步驟1：設定[!DNL Duo Security]

1. 輸入您的帳戶認證，並登入&#x200B;_管理員_。

1. 當[!DNL Duo]設定頁面出現時，按一下&#x200B;**[!UICONTROL Get Started]**&#x200B;並執行下列動作：

   ![店面範例 — Duo設定](./assets/storefront-2fa-duo-setup-options.png){width="300"}

1. 選取您的選項。 您可以選擇Touch ID、Duo Mobile、安全金鑰或電話號碼。 此範例顯示Duo行動或電話號碼選項。

1. 出現提示時，輸入您的電話號碼並按一下&#x200B;**[!UICONTROL Continue]**。

   透過在電話號碼上傳送及驗證密碼來確認擁有權。

1. 當提示您為電話型別安裝[!DNL Duo Mobile]時，請按一下&#x200B;**[!UICONTROL I have Duo Mobile]**。

1. 開啟[!DNL Duo Mobile]並掃描QR碼，以將驗證器與Adobe Commerce同步。 啟動完成後，會出現核取記號。

1. 您可以新增更多裝置（如有必要）或略過。 您的設定現已完成，您可以使用Duo登入。

   ![雙核心驗證動作](./assets/storefront-2fa-duo-setup-complete.png){width="300"}

### 步驟2：使用[!DNL Duo Security]登入

下列範例顯示`Ask me to choose an authenticator method`的選項：

1. 出現提示時，請輸入您的&#x200B;_管理員_&#x200B;認證以登入。

   ![雙核心 — 登入](./assets/storefront-2fa-duo-auth.png){width="300"}

1. 選擇使用Duo登入，即可在Duo行動應用程式上取得推播通知、使用Touch ID登入，或繼續使用您在設定期間設定的其他選項。

1. 核准Duo應用程式/觸控式ID/文字訊息的請求，您將會成功登入。

   ![雙核心 — 登入](./assets/storefront-2fa-duo-success.png){width="300"}

## [!DNL Authy]

[!DNL Authy]免費為使用者提供其應用程式和服務。 按照他們的指示，下載並設定您裝置或瀏覽器的應用程式。 若要深入瞭解，請參閱[[!DNL Authy] 檔案](https://authy.com/features/setup/)。

### 步驟1：設定Authy

1. 輸入您的帳戶認證，並登入&#x200B;_管理員_。

   ![[!DNL Authy]註冊](./assets/storefront-2fa-authy-auth.png){width="300"}

1. 當系統提示您向Authy註冊時，請執行下列動作：

   - 選取您的國家/地區。

   - 輸入您的電話號碼。

   - 選取&#x200B;**[!UICONTROL Verification method]**： `SMS`或`Call Me`

   按一下&#x200B;**[!UICONTROL Continue]**。 訊息會透過簡訊或電話傳送至您的電話。

1. 輸入您收到的驗證碼並按一下&#x200B;**[!UICONTROL Verify]**。

1. 完成時，按一下&#x200B;**[!UICONTROL Confirm]**。

   ![[!DNL Authy]驗證碼](./assets/storefront-2fa-authy-verify.png){width="300"}

### 步驟2：使用[!DNL Authy]登入

1. 輸入您的帳戶認證，並登入&#x200B;_管理員_。

   ![[!DNL Authy] — 登入](./assets/storefront-2fa-authy-access.png){width="300"}

1. 選擇下列其中一種驗證方法：

   - `Use one touch` — 傳送警示至您的[!DNL Authy]應用程式。 在應用程式中，接受存取。
   - `Use authy token` — 提示輸入您[!DNL Authy]應用程式的程式碼。

1. 如果您無法登入，請選擇您要用來接收程式碼的方法。 然後，輸入您收到的存取&#x200B;_管理員_&#x200B;的代碼。

   應用程式包含這些額外的緊急方法。

   - `Send me a code via SMS` — 文字SMS訊息會傳送至已設定的行動裝置。
   - `Send me a code via phone call` — 使用者收到包含程式碼的電話。

   您的帳戶已驗證並開啟。

## U2F （[!DNL Yubikey]和其他裝置）

依照解決方案提供者的指示，設定您的U2F裝置。 如需詳細資訊，請參閱廠商檔案，例如[!UICONTROL Yubico]的[[!DNL YubiKey]](https://support.yubico.com/hc/en-us/articles/360013790339-Getting-Started-with-Your-YubiKey)。

1. 輸入您的帳戶認證，並登入&#x200B;_管理員_。

   ![U2F金鑰存取](./assets/storefront-2fa-u2f.png){width="300"}

1. 按下按鍵上的按鈕。

   驗證會立即觸發並開啟&#x200B;_管理員_。

1. 將&#x200B;**[!UICONTROL U2F key]**&#x200B;插入電腦的USB連線埠。
