---
title: Google reCAPTCHA V3和V2
description: 瞭解如何設定Google reCAPTCHA以進行管理員存取及註冊客戶所啟動的各種店面動作。
exl-id: c3b53702-0882-4ac4-9cf5-39fefc90005e
role: Admin
feature: Configuration, Security
source-git-commit: 80b2ecc9fddd7a20d6824182f41f0d19f6d51003
workflow-type: tm+mt
source-wordcount: '1053'
ht-degree: 0%

---

# Google reCAPTCHA V3和V2

[Google reCAPTCHA](https://developers.google.com/recaptcha)可確保人(而非電腦（或「機器人」）)與您的網站互動。 與標準Adobe Commerce和Magento Open Source [CAPTCHA](security-captcha.md)不同，Google reCAPTCHA透過選取不同的顯示選項和方法，提供增強式安全性。 您可在Google reCAPTCHA帳戶的控制面板中取得其他網站流量資訊。

Google reCAPTCHA已針對管理員和店面分別設定。

- 針對管理員，Google reCAPTCHA可用於[登入](../getting-started/admin-signin.md)頁面以及使用者要求重設密碼時。 如果標準Commerce [CAPTCHA](security-captcha.md)也已啟用，則可同時使用Google reCAPTCHA而不會發生任何問題。

- 對於店面，Google reCAPTCHA可用於登入[客戶帳戶](../customers/customer-sign-in.md)、從[聯絡我們](../getting-started/store-details.md#contact-us-form)頁面及許多其他店面位置傳送訊息。

  ![Google reCAPTCHA — 客戶登入](./assets/customer-account-login-recaptcha.png){width="700" zoomable="yes"}

Google reCAPTCHA可透過數種方式實作：

- _reCAPTCHA v3不可見_ — 使用演演算法來評估使用者互動，並根據分數判斷使用者是否為人類的可能性。

- _reCAPTCHA v2不可見_ — 執行背景驗證而不需使用者互動。 使用者和客戶會自動驗證，但可能需要選取特定影像以完成挑戰。

- _reCAPTCHA v2 （「我不是機器人」）_ — 使用&#x200B;_「我不是機器人」_&#x200B;核取方塊驗證要求。

>[!IMPORTANT]
>
>設定Google reCAPTCHA之前，請確定您的`PHP.ini`檔案包含下列設定： `allow_url_fopen = 1`。 這可能需要開發人員協助。 請參閱安裝指南中的[必要的PHP設定](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html?lang=zh-Hant){:target="_blank"}。

## 步驟1：產生Google reCAPTCHA金鑰

Google reCAPTCHA需要一對API金鑰才能啟用。 您可以透過reCAPTCHA網站免費取得這些金鑰。 在產生金鑰之前，您必須知道您要使用的reCAPTCHA型別。

1. 開啟Google reCAPTCHA頁面並登入您的帳戶。

1. 針對&#x200B;**[!UICONTROL Label]**，輸入名稱以識別內部參考的索引鍵。

   Adobe Commerce或Magento Open Source安裝中所使用的每個reCAPTCHA型別，都需要一組金鑰。 例如： `Commerce Invisible`

1. 針對&#x200B;**[!UICONTROL reCAPTCHA type]**，選擇您要使用的方法。

   - _reCAPTCHA v3隱藏_
   - _reCAPTCHA v2隱藏_
   - _reCAPTCHA v2 （「我不是機器人」）_

1. 針對&#x200B;**[!UICONTROL Domain]**，輸入您商店的網域。 例如： mystore.com

   如果您有多個不同網域的商店，請在單獨的行中輸入每個網域。

   - 新增您的商店網域及任何子網域。
   - 您可以視測試需要新增`localhost`、其他本機VM網域和暫存網域。

1. 選取&#x200B;**[!UICONTROL Accept the reCAPTCHA Terms of Service]**&#x200B;的核取方塊。

1. （選擇性）選取&#x200B;**[!UICONTROL Send alerts to owners]**&#x200B;核取方塊，以在Google偵測到問題或可疑流量時傳送通知。

1. 按一下&#x200B;**[!UICONTROL Submit]**&#x200B;完成註冊並接收金鑰。

   >[!IMPORTANT]
   >
   >並非所有金鑰都適用於所有型別的reCAPTCHA，若未套用這些金鑰可能會導致非預期的行為。 例如，為reCAPTCHA v2 「我不是機器人」產生的Google reCAPTCHA金鑰無法搭配&#x200B;_reCAPTCHA v2 Invisible_&#x200B;使用，且可能會封鎖啟用reCAPTCHA的功能。

## 步驟2：為管理員設定Google reCAPTCHA

僅[!BADGE 個PaaS]{type=Informative url="https://experienceleague.adobe.com/zh-hant/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"}

1. 登入您的管理員帳戶。

1. 在管理員側邊欄上，前往&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在右上角，將&#x200B;**[!UICONTROL Store View]**&#x200B;設為`Default Config`。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Security]**&#x200B;並按一下&#x200B;**[!UICONTROL Google reCAPTCHA Admin Panel]**。

   >[!NOTE]
   >
   >清除您要設定的每個欄位的&#x200B;**[!UICONTROL Use system value]**&#x200B;核取方塊。

1. 若要使用&#x200B;_[!DNL reCAPTCHA v2 ("I am not a robot")]_，請展開&#x200B;**[!UICONTROL reCAPTCHA v2 ("I am not a robot")]**&#x200B;區段並執行下列動作：

   - 針對&#x200B;**[!UICONTROL Google API Website Key]**，輸入在您註冊Google reCAPTCHA帳戶時為此reCAPTCHA型別建立的網站金鑰。

   - 針對&#x200B;**[!UICONTROL Google API Secret Key]**，輸入與您的Google reCAPTCHA帳戶相關聯的秘密金鑰。

   - 針對&#x200B;**[!UICONTROL Size]**，選擇您要顯示的Google reCAPTCHA方塊大小。 選項： `Normal (default)` / `Compact`

   - 針對&#x200B;**[!UICONTROL Theme]**，選擇您要用來設定Google reCAPTCHA方塊樣式的佈景主題。 選項： `Light Theme (default)` / `Dark Theme`

   - 針對&#x200B;**[!UICONTROL Language Code]**，輸入雙字元代碼，以指定用於Google reCAPTCHA文字與傳訊[的](https://developers.google.com/recaptcha/docs/language)語言。

   ![reCAPTCHA v2 - 「我不是機器人」](../configuration-reference/security/assets/recaptcha-admin-v2-not-robot.png){width="600" zoomable="yes"}

1. 若要使用&#x200B;_[!DNL reCAPTCHA v2 Invisible]_，請展開&#x200B;**[!UICONTROL reCAPTCHA v2 Invisible]**&#x200B;區段並執行下列動作：

   - 針對&#x200B;**[!UICONTROL Google API Website Key]**，輸入在您註冊Google reCAPTCHA帳戶時為此reCAPTCHA型別建立的網站金鑰。

   - 針對&#x200B;**[!UICONTROL Google API Secret Key]**，輸入與您的Google reCAPTCHA帳戶相關聯的秘密金鑰。

   - 針對&#x200B;**[!UICONTROL Invisible Badge Position]**，選擇要在每個頁面上使用的徽章位置。 選項： `Inline` / `Bottom Right` / `Bottom Left`

   - 針對&#x200B;**[!UICONTROL Theme]**，選擇要用來設定Google reCAPTCHA方塊樣式的佈景主題。 選項： `Light Theme (default)` / `Dark Theme`

   - 針對&#x200B;**[!UICONTROL Language Code]**，輸入雙字元代碼，指定用於Google reCAPTCHA文字與訊息的[語言](https://developers.google.com/recaptcha/docs/language)。

   ![reCAPTCHA v2隱藏](../configuration-reference/security/assets/recaptcha-admin-v2-invisible.png){width="600" zoomable="yes"}

1. 若要使用&#x200B;_[!DNL reCAPTCHA v3 Invisible]_，請展開&#x200B;**[!UICONTROL reCAPTCHA v3 Invisible]**&#x200B;區段並執行下列動作：

   - 針對&#x200B;**[!UICONTROL Google API Website Key]**，輸入在您註冊Google reCAPTCHA帳戶時為此reCAPTCHA型別建立的網站金鑰。

   - 針對&#x200B;**[!UICONTROL Google API Secret Key]**，輸入與您的Google reCAPTCHA帳戶相關聯的秘密金鑰。

   - 輸入&#x200B;**[!UICONTROL Minimum Score Threshold]**&#x200B;以識別何時將使用者互動標籤為潛在風險；其中1.0是典型的使用者互動，而0.0可能是機器人。 預設： `0.5`

   - 針對&#x200B;**[!UICONTROL Invisible Badge Position]**，選擇要在每個頁面上使用的位置。 選項： `Inline` / `Bottom Right` / `Bottom Left`

   - 針對&#x200B;**[!UICONTROL Theme]**，選擇要用來設定Google reCAPTCHA方塊樣式的佈景主題。 選項： `Light Theme (default)` / `Dark Theme`

   - 針對&#x200B;**[!UICONTROL Language Code]**，輸入雙字元代碼，指定用於Google reCAPTCHA文字與訊息的[語言](https://developers.google.com/recaptcha/docs/language)。

   ![reCAPTCHA v3隱藏](../configuration-reference/security/assets/recaptcha-admin-v3-invisible.png){width="600" zoomable="yes"}

1. 展開&#x200B;**[!UICONTROL reCAPTCHA Validation Failure Messages]**&#x200B;並輸入在驗證失敗或無法完成時顯示在管理員中的訊息。

   ![reCAPTCHA失敗訊息](../configuration-reference/security/assets/recaptcha-admin-failure-messages.png){width="600" zoomable="yes"}

1. 展開&#x200B;**[!UICONTROL Admin Panel]**&#x200B;區段，並視需要設定下列專案：

   - 將&#x200B;**[!UICONTROL Enable for Login]**&#x200B;設為您要用於管理員登入頁面的reCAPTCHA型別。

   - 將&#x200B;**[!UICONTROL Enable for Forgot Password]**&#x200B;設為您要用於密碼重設要求的reCAPTCHA型別。

   ![reCAPTCHA管理選項](../configuration-reference/security/assets/recaptcha-admin-panel.png){width="600" zoomable="yes"}

## 步驟3：為店面設定Google reCAPTCHA

1. 在左側面板的&#x200B;_[!UICONTROL Security]_&#x200B;下，選擇&#x200B;**[!UICONTROL Google reCAPTCHA Storefront]**。

1. 針對您要在店面中使用的每個reCAPTCHA型別，完成區段。

   請參閱&#x200B;_步驟2：為管理員設定Google reCAPTCHA中的資訊_，以取得有關每個reCAPTCHA型別的選項的詳細資訊。

1. 展開&#x200B;**[!UICONTROL reCAPTCHA Validation Failure Messages]**&#x200B;並輸入在驗證失敗或無法完成時顯示在店面中的訊息。

1. 展開&#x200B;**[!UICONTROL Storefront]**&#x200B;區段。

   >[!NOTE]
   >
   >清除您要設定的每個欄位的&#x200B;**[!UICONTROL Use system value]**&#x200B;核取方塊。

1. 將每個店面位置欄位設定為您已設定要使用的reCAPTCHA型別。

   {{recaptcha-forms-list}}

   ![店面選項組態](../configuration-reference/security/assets/recaptcha-storefront.png){width="600" zoomable="yes"}

## 步驟4：儲存設定

1. 組態設定完成後，按一下&#x200B;**[!UICONTROL Save Config]**。

1. 在工作區頂端的訊息中，按一下&#x200B;**[!UICONTROL Cache Management]**&#x200B;並重新整理每個無效的快取。
