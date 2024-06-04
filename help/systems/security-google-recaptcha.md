---
title: Google reCAPTCHA
description: 瞭解如何設定Google reCAPTCHA以進行管理員存取及註冊客戶所啟動的各種店面動作。
exl-id: c3b53702-0882-4ac4-9cf5-39fefc90005e
role: Admin
feature: Configuration, Security
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1046'
ht-degree: 0%

---

# Google reCAPTCHA

[Google reCAPTCHA](https://developers.google.com/recaptcha) 確保人類(而非電腦（或「機器人」）)與您的網站互動。 有別於標準Adobe Commerce和Magento Open Source [驗證碼](security-captcha.md)，Google reCAPTCHA透過選取不同的顯示選項和方法提供增強式安全性。 您可在Google reCAPTCHA帳戶的控制面板中取得其他網站流量資訊。

Google reCAPTCHA已針對管理員和店面分別設定。

- 對於管理員，Google reCAPTCHA可用於 [登入](../getting-started/admin-signin.md) 頁面，以及使用者要求重設密碼時。 如果標準Commerce [驗證碼](security-captcha.md) Google reCAPTCHA亦可順利同時使用。

- 對於店面，Google reCAPTCHA可用於登入 [客戶帳戶](../customers/customer-sign-in.md)，傳送來自 [聯絡我們](../getting-started/store-details.md#contact-us-form) 頁面，以及許多其他店面位置。

  ![Google reCAPTCHA — 客戶登入](./assets/customer-account-login-recaptcha.png){width="700" zoomable="yes"}

Google reCAPTCHA可透過數種方式實作：

- _reCAPTCHA v3隱藏_  — 使用演演算法來評估使用者互動，並根據分數來判斷使用者是否為人類的可能性。

- _reCAPTCHA v2隱藏_  — 執行背景驗證而不需使用者互動。 使用者和客戶會自動驗證，但可能需要選取特定影像以完成挑戰。

- _reCAPTCHA v2 （「我不是機器人」）_  — 驗證要求 _「我不是機器人」_ 核取方塊。

>[!IMPORTANT]
>
>在設定Google reCAPTCHA之前，請確定 `PHP.ini` 檔案包含下列設定： `allow_url_fopen = 1`. 這可能需要開發人員協助。 另請參閱 [必要的PHP設定](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html)安裝指南中的{：target=&quot;_blank&quot;}。

## 步驟1：產生Google reCAPTCHA金鑰

Google reCAPTCHA需要一對API金鑰才能啟用。 您可以透過reCAPTCHA網站免費取得這些金鑰。 在產生金鑰之前，您必須知道您要使用的reCAPTCHA型別。

1. 開啟Google reCAPTCHA頁面並登入您的帳戶。

1. 的 **[!UICONTROL Label]**，輸入名稱以識別供內部參考的金鑰。

   在Adobe Commerce或Magento Open Source安裝中使用的每個reCAPTCHA型別，都需要一組金鑰。 例如： `Commerce Invisible`

1. 的 **[!UICONTROL reCAPTCHA type]**，選擇您要使用的方法。

   - _reCAPTCHA v3隱藏_
   - _reCAPTCHA v2隱藏_
   - _reCAPTCHA v2 （「我不是機器人」）_

1. 的 **[!UICONTROL Domain]**，輸入您商店的網域。 例如： mystore.com

   如果您有多個不同網域的商店，請在單獨的行中輸入每個網域。

   - 新增您的商店網域及任何子網域。
   - 您可以新增 `localhost`、其他本機VM網域，以及測試所需的中繼網域。

1. 選取核取方塊以 **[!UICONTROL Accept the reCAPTCHA Terms of Service]**.

1. （可選）選取 **[!UICONTROL Send alerts to owners]** 此核取方塊會在Google偵測到問題或可疑流量時傳送通知。

1. 按一下 **[!UICONTROL Submit]** 完成註冊並接收金鑰。

   >[!IMPORTANT]
   >
   >並非所有金鑰都適用於所有型別的reCAPTCHA，若未套用這些金鑰可能會導致非預期的行為。 例如，為reCAPTCHA v2 「我不是機器人」產生的Google reCAPTCHA金鑰無法搭配使用 _reCAPTCHA v2隱藏_ 和可能會封鎖已啟用reCAPTCHA的功能。

## 步驟2：為管理員設定Google reCAPTCHA

1. 登入您的管理員帳戶。

1. 在管理員側邊欄上，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在右上角，設定 **[!UICONTROL Store View]** 至 `Default Config`.

1. 在左側面板中，展開 **[!UICONTROL Security]** 並按一下 **[!UICONTROL Google reCAPTCHA Admin Panel]**.

   >[!NOTE]
   >
   >清除 **[!UICONTROL Use system value]** 核取方塊來選取您要設定的每個欄位。

1. 使用 _[!DNL reCAPTCHA v2 ("I am not a robot")]_，展開&#x200B;**[!UICONTROL reCAPTCHA v2 ("I am not a robot")]**並執行下列動作：

   - 的 **[!UICONTROL Google API Website Key]**，輸入您在註冊Google reCAPTCHA帳戶時，針對此reCAPTCHA型別建立的網站金鑰。

   - 的 **[!UICONTROL Google API Secret Key]**，輸入與您的Google reCAPTCHA帳戶相關聯的秘密金鑰。

   - 的 **[!UICONTROL Size]**，選取您要顯示的Google reCAPTCHA方塊大小。 選項： `Normal (default)` / `Compact`

   - 的 **[!UICONTROL Theme]**，選擇您要用來設定Google reCAPTCHA方塊樣式的佈景主題。 選項： `Light Theme (default)` / `Dark Theme`

   - 的 **[!UICONTROL Language Code]**，輸入兩個字元的程式碼，以指定 [用於Google reCAPTCHA文字和傳訊的語言](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v2 - 「我不是機器人」](../configuration-reference/security/assets/recaptcha-admin-v2-not-robot.png){width="600" zoomable="yes"}

1. 使用 _[!DNL reCAPTCHA v2 Invisible]_，展開&#x200B;**[!UICONTROL reCAPTCHA v2 Invisible]**並執行下列動作：

   - 的 **[!UICONTROL Google API Website Key]**，輸入您在註冊Google reCAPTCHA帳戶時，針對此reCAPTCHA型別建立的網站金鑰。

   - 的 **[!UICONTROL Google API Secret Key]**，輸入與您的Google reCAPTCHA帳戶相關聯的秘密金鑰。

   - 的 **[!UICONTROL Invisible Badge Position]**，選擇要在每個頁面上使用的徽章位置。 選項： `Inline` / `Bottom Right` / `Bottom Left`

   - 的 **[!UICONTROL Theme]**，選擇要用於設定Google reCAPTCHA方塊樣式的佈景主題。 選項： `Light Theme (default)` / `Dark Theme`

   - 的 **[!UICONTROL Language Code]**，請輸入兩個字元的程式碼，指定 [用於Google reCAPTCHA文字和傳訊的語言](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v2隱藏](../configuration-reference/security/assets/recaptcha-admin-v2-invisible.png){width="600" zoomable="yes"}

1. 使用 _[!DNL reCAPTCHA v3 Invisible]_，展開&#x200B;**[!UICONTROL reCAPTCHA v3 Invisible]**並執行下列動作：

   - 的 **[!UICONTROL Google API Website Key]**，輸入您在註冊Google reCAPTCHA帳戶時，針對此reCAPTCHA型別建立的網站金鑰。

   - 的 **[!UICONTROL Google API Secret Key]**，輸入與您的Google reCAPTCHA帳戶相關聯的秘密金鑰。

   - 輸入 **[!UICONTROL Minimum Score Threshold]** 識別何時將使用者互動標籤為潛在風險；其中1.0是典型的使用者互動，0.0可能是機器人。 預設： `0.5`

   - 的 **[!UICONTROL Invisible Badge Position]**，選擇要在每個頁面上使用的位置。 選項： `Inline` / `Bottom Right` / `Bottom Left`

   - 的 **[!UICONTROL Theme]**，選擇要用於設定Google reCAPTCHA方塊樣式的佈景主題。 選項： `Light Theme (default)` / `Dark Theme`

   - 的 **[!UICONTROL Language Code]**，請輸入兩個字元的程式碼，指定 [用於Google reCAPTCHA文字和傳訊的語言](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v3隱藏](../configuration-reference/security/assets/recaptcha-admin-v3-invisible.png){width="600" zoomable="yes"}

1. 展開 **[!UICONTROL reCAPTCHA Validation Failure Messages]** 並輸入在驗證失敗或無法完成時顯示在管理員中的訊息。

   ![reCAPTCHA失敗訊息](../configuration-reference/security/assets/recaptcha-admin-failure-messages.png){width="600" zoomable="yes"}

1. 展開 **[!UICONTROL Admin Panel]** 區段，並視需要設定下列專案：

   - 設定 **[!UICONTROL Enable for Login]** 重新命名為reCAPTCHA型別，以用於管理員登入頁面。

   - 設定 **[!UICONTROL Enable for Forgot Password]** 重新設定為要用於密碼重設請求的reCAPTCHA型別。

   ![reCAPTCHA管理選項](../configuration-reference/security/assets/recaptcha-admin-panel.png){width="600" zoomable="yes"}

## 步驟3：為店面設定Google reCAPTCHA

1. 在左側面板中的 _[!UICONTROL Security]_，選擇&#x200B;**[!UICONTROL Google reCAPTCHA Storefront]**.

1. 針對您要在店面中使用的每個reCAPTCHA型別，完成區段。

   請參閱以下連結中的資訊： _步驟2：為管理員設定Google reCAPTCHA_ 以取得每個reCAPTCHA型別之選項的詳細資訊。

1. 展開 **[!UICONTROL reCAPTCHA Validation Failure Messages]** 並輸入在驗證失敗或無法完成時顯示在店面中的訊息。

1. 展開 **[!UICONTROL Storefront]** 區段。

   >[!NOTE]
   >
   >清除 **[!UICONTROL Use system value]** 核取方塊來選取您要設定的每個欄位。

1. 將每個店面位置欄位設定為您已設定要使用的reCAPTCHA型別。

   - [!UICONTROL Enable for Customer Login]
   - [!UICONTROL Enable for Forgot Password]
   - [!UICONTROL Enable for Create New Customer Account]
   - [!UICONTROL Enable for Edit Customer Account]
   - [!UICONTROL Enable for Create New Company Account] ![Adobe Commerce B2B](../assets/b2b.svg) (僅適用於Adobe Commerce B2B)
   - [!UICONTROL Enable for Contact Us]
   - [!UICONTROL Enable for Product Review]
   - [!UICONTROL Enable for Newsletter Subscription]
   - [!UICONTROL Enable for Gift Card] ![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)
   - [!UICONTROL Enable for Invitation Create Account]
   - [!UICONTROL Enable for Send To Friend]
   - [!UICONTROL Enable for Checkout/Placing Order]
   - [!UICONTROL Enable for Wishlist Sharing]
   - [!UICONTROL Enable for Coupon Codes]
   - [!UICONTROL Enable for PayPal PayflowPro payment form]

   ![店面選項設定](../configuration-reference/security/assets/recaptcha-storefront.png){width="600" zoomable="yes"}

## 步驟4：儲存設定

1. 組態設定完成後，按一下 **[!UICONTROL Save Config]**.

1. 在工作區頂端的訊息中，按一下 **[!UICONTROL Cache Management]** 並重新整理每個無效的快取。
