---
title: '[!UICONTROL Security] &amp；gt； [!UICONTROL Google reCAPTCHA Storefront]'
description: 檢閱Commerce管理員的[!UICONTROL Security] &amp；gt； [!UICONTROL Google reCAPTCHA Storefront]頁面上的組態設定。
exl-id: 6c03ee68-7421-4c74-bdc1-0855f088b7f9
feature: Configuration, Security
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1283'
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL Google reCAPTCHA Storefront]

>[!IMPORTANT]
>
>在設定Google reCAPTCHA之前，您必須確定您的`PHP.ini`檔案包含下列設定： `allow_url_fopen = 1`。 這可能需要開發人員協助。 請參閱&#x200B;_安裝指南_&#x200B;中的[PHP設定](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html?lang=zh-Hant)。

{{config}}

如需使用Google reCAPTCHA來保護存放區的詳細資訊，請參閱&#x200B;_系統管理系統指南_&#x200B;中的Google [reCAPTCHA](../../systems/security-google-recaptcha.md)。

## [!UICONTROL reCAPTCHA v2 ("I am not a robot")]

![reCAPTCHA v2 （「我不是機器人」）](./assets/recaptcha-storefront-v2-not-robot.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--|--|--|
| [!UICONTROL Google API Website Key] | 網站 | 註冊Google reCAPTCHA帳戶時建立的網站金鑰。 |
| [!UICONTROL Google API Secret Key] | 網站 | 與您的Google reCAPTCHA帳戶相關聯的秘密金鑰。 |
| [!UICONTROL Size] | 網站 | 客戶登入帳戶時顯示的Google reCAPTCHA方塊大小。 選項： `Normal` （預設） / `Compact` |
| [!UICONTROL Theme] | 網站 | 決定Google reCAPTCHA方塊的樣式。 選項： `Light Theme` （預設） / `Dark Theme` |
| [!UICONTROL Language Code] | 存放區檢視 | [雙字元代碼](https://developers.google.com/recaptcha/docs/language)，指定用於Google reCAPTCHA文字與訊息的語言。 |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v2 Invisible]

![reCAPTCHA v2隱藏](./assets/recaptcha-storefront-v2-invisible.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--|--|--|
| [!UICONTROL Google API Website Key] | 網站 | 註冊Google reCAPTCHA帳戶時建立的網站金鑰。 |
| [!UICONTROL Google API Secret Key] | 網站 | 與您的Google reCAPTCHA帳戶相關聯的秘密金鑰。 |
| [!UICONTROL Invisible Badge Position] | 網站 | 每個頁面上隱藏的reCAPTCHA徽章的位置。 選項： `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | 全域 | 決定Google reCAPTCHA方塊的樣式。 選項： `Light Theme` （預設） / `Dark Theme` |
| [!UICONTROL Language Code] | 存放區檢視 | [雙字元代碼](https://developers.google.com/recaptcha/docs/language)，指定用於Google reCAPTCHA文字與訊息的語言。 |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v3 Invisible]

![reCAPTCHA v3隱藏](./assets/recaptcha-storefront-v3-invisible.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--|--|--|
| [!UICONTROL Google API Website Key] | 網站 | 註冊Google reCAPTCHA帳戶時建立的網站金鑰。 |
| [!UICONTROL Google API Secret Key] | 網站 | 與您的Google reCAPTCHA帳戶相關聯的秘密金鑰。 |
| [!UICONTROL Minimum Score Threshold] | 全域 | 將使用者互動識別為潛在風險的最低分數，其中1.0是典型的使用者互動，0.0可能是機器人。 預設： `0.5` |
| [!UICONTROL Invisible Badge Position] | 網站 | 每個頁面上隱藏的reCAPTCHA徽章的位置。 選項： `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | 網站 | 決定Google reCAPTCHA方塊的樣式。 選項： `Light Theme` （預設） / `Dark Theme` |
| [!UICONTROL Language Code] | 存放區檢視 | [雙字元代碼](https://developers.google.com/recaptcha/docs/language)，指定用於Google reCAPTCHA文字與訊息的語言。 |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA Failure Messages]

![失敗訊息](./assets/recaptcha-storefront-failure-messages.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--|--|--|
| [!UICONTROL reCAPTCHA Validation Failure Message] | 存放區檢視 | 驗證失敗時顯示在店面中的訊息。 預設文字： `reCAPTCHA verification failed.` |
| [!UICONTROL reCAPTCHA Technical Failure Message] | 存放區檢視 | 如果reCAPTCHA無法傳回驗證結果，在店面中顯示的訊息。 預設文字： `Something went wrong with reCAPTCHA. Please contact the store owner.` |

{style="table-layout:auto"}

## [!UICONTROL Storefront]

![店面](./assets/recaptcha-storefront.png)<!-- zoom -->

>[!NOTE]
>
>您選擇的reCAPTCHA型別必須符合與Google reCAPTCHA帳戶中的API金鑰相關聯的型別。

>[!WARNING]
>
>使用reCAPTCHA版本3時，低分數的正版使用者無法繼續。 對於版本2，分數較低的正版使用者會收到挑戰。 若是低分的真正使用者應該有機會解決挑戰（版本2）或遭到封鎖（版本3），請仔細考慮。

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--|--|--|
| [!UICONTROL Enable for Customer Login] | 網站 | 指定客戶[登入](../../customers/customer-sign-in.md)帳戶時所使用的reCAPTCHA型別。 選項：<br/>**`No`**- （預設）不會驗證登入要求。<br />**`reCAPTCHA v2 ("I am not a robot")`** — 要求使用者選取&#x200B;_我不是自動機制_&#x200B;核取方塊。<br />**`Invisible reCAPTCHA v2`**— 在背景驗證使用者行為，不需要根據分數進行互動。<br/>**`Invisible reCAPTCHA v3`** - （建議）根據互動分數，驗證背景的使用者行為。 |
| [!UICONTROL Enable for Forgot Password] | 網站 | 指定客戶要求[密碼重設](../../customers/password-reset.md)時所使用的reCAPTCHA型別。 選項： <br/>**`No`**- （預設）不會驗證密碼重設要求。<br />**`reCAPTCHA v2 ("I am not a robot")`** — 要求使用者選取&#x200B;_我不是自動機制_&#x200B;核取方塊。<br />**`Invisible reCAPTCHA v2`**— 在背景驗證使用者行為，不需要根據分數進行互動。<br/>**`Invisible reCAPTCHA v3`** - （建議）根據互動分數，驗證背景的使用者行為。 |
| [!UICONTROL Enable for Create New Customer Account] | 網站 | 指定客戶註冊[新帳戶](../../customers/account-create.md)時所使用的reCAPTCHA型別。 選項：<br/>**`No`**- （預設）不會驗證帳戶要求。<br />**`reCAPTCHA v2 ("I am not a robot")`** — 要求使用者選取&#x200B;_我不是自動機制_&#x200B;核取方塊。<br />**`Invisible reCAPTCHA v2`**— 在背景驗證使用者行為，不需要根據分數進行互動。<br/>**`Invisible reCAPTCHA v3`** - （建議）根據互動分數，驗證背景的使用者行為。 |
| [!UICONTROL Enable for Edit Customer Account] | 網站 | 指定客戶變更其[帳戶資訊](../../customers/account-dashboard-account-information.md)時所使用的reCAPTCHA型別。 選項：<br/>**`No`**- （預設）不會驗證帳戶要求。<br />**`reCAPTCHA v2 ("I am not a robot")`** — 要求使用者選取&#x200B;_我不是自動機制_&#x200B;核取方塊。<br />**`Invisible reCAPTCHA v2`**— 在背景驗證使用者行為，不需要根據分數進行互動。<br/>**`Invisible reCAPTCHA v3`** - （建議）根據互動分數，驗證背景的使用者行為。 |
| [!UICONTROL Enable for Create New Company Account] | 網站 | ![Adobe Commerce B2B](../../assets/b2b.svg) (僅適用於Adobe Commerce B2B)指定建立新[公司帳戶](../../b2b/account-company-create.md)時所使用的reCAPTCHA型別。 選項：<br/>**`No`**- （預設）不會驗證帳戶要求。<br />**`reCAPTCHA v2 ("I am not a robot")`** — 要求使用者選取&#x200B;_我不是自動機制_&#x200B;核取方塊。<br />**`Invisible reCAPTCHA v2`**— 在背景驗證使用者行為，不需要根據分數進行互動。<br/>**`Invisible reCAPTCHA v3`** - （建議）根據互動分數，驗證背景的使用者行為。 |
| [!UICONTROL Enable for Contact Us] | 網站 | 指定用來從您商店的[聯絡我們](../../getting-started/store-details.md#contact-us-form)頁面傳送訊息的reCAPTCHA型別。 選項：<br/>**`No`**- （預設）不會驗證訊息要求。<br />**`reCAPTCHA v2 ("I am not a robot")`** — 要求使用者選取&#x200B;_我不是自動機制_&#x200B;核取方塊。<br />**`Invisible reCAPTCHA v2`**— 在背景驗證使用者行為，不需要根據分數進行互動。<br/>**`Invisible reCAPTCHA v3`** - （建議）根據互動分數，驗證背景的使用者行為。 |
| [!UICONTROL Enable for Product Review] | 網站 | 指定客戶提交[產品評論](../../merchandising-promotions/product-reviews.md)時所使用的reCAPTCHA型別。 選項：<br/>**`No`**- （預設）不會驗證產品檢閱要求。<br />**`reCAPTCHA v2 ("I am not a robot")`** — 要求使用者選取&#x200B;_我不是自動機制_&#x200B;核取方塊。<br />**`Invisible reCAPTCHA v2`**— 在背景驗證使用者行為，不需要根據分數進行互動。<br/>**`Invisible reCAPTCHA v3`** - （建議）根據互動分數，驗證背景的使用者行為。 |
| [!UICONTROL Enable for Newsletter Subscription] | 網站 | 指定當客戶註冊[電子報訂閱](../../merchandising-promotions/newsletter-subscribers.md)時所使用之隱藏的reCAPTCHA型別。 選項：<br/>**`No`**- （預設）不會驗證Newsletter訂閱要求。<br />**`reCAPTCHA v2 ("I am not a robot")`** — 要求使用者選取&#x200B;_我不是自動機制_&#x200B;核取方塊。<br />**`Invisible reCAPTCHA v2`**— 在背景驗證使用者行為，不需要根據分數進行互動。<br/>**`Invisible reCAPTCHA v3`** - （建議）根據互動分數，驗證背景的使用者行為。 |
| [!UICONTROL Enable for Gift Card] | 網站 | ![Adobe Commerce](../../assets/adobe-logo.svg) (僅限Adobe Commerce)指定客戶輸入[禮卡](../../catalog/product-gift-card-create.md)代碼時所使用的reCAPTCHA型別。 選項：<br/>**`No`**- （預設）不會驗證禮品卡代碼提交。<br />**`reCAPTCHA v2 ("I am not a robot")`** — 要求使用者選取&#x200B;_我不是自動機制_&#x200B;核取方塊。<br />**`Invisible reCAPTCHA v2`**— 在背景驗證使用者行為，不需要根據分數進行互動。<br/>**`Invisible reCAPTCHA v3`** - （建議）根據互動分數，驗證背景的使用者行為。 |
| [!UICONTROL Enable for Invitation Create Account] | 網站 | 指定當客戶傳送帳戶建立[邀請](../../merchandising-promotions/invitations.md)代碼時所使用的reCAPTCHA型別。 選項：<br/>**`No`**- （預設）不會驗證邀請電子郵件提交。<br />**`reCAPTCHA v2 ("I am not a robot")`** — 要求使用者選取&#x200B;_我不是自動機制_&#x200B;核取方塊。<br />**`Invisible reCAPTCHA v2`**— 在背景驗證使用者行為，不需要根據分數進行互動。<br/>**`Invisible reCAPTCHA v3`** - （建議）根據互動分數，驗證背景的使用者行為。 |
| [!UICONTROL Enable for Send to Friend] | 網站 | 指定客戶[與朋友共用產品](../../stores-purchase/email-a-friend.md)時所使用的reCAPTCHA型別。 選項：<br/>**`No`**- （預設）不會驗證電子郵件提交。<br />**`reCAPTCHA v2 ("I am not a robot")`** — 要求使用者選取&#x200B;_我不是自動機制_&#x200B;核取方塊。<br />**`Invisible reCAPTCHA v2`**— 在背景驗證使用者行為，不需要根據分數進行互動。<br/>**`Invisible reCAPTCHA v3`** - （建議）根據互動分數，驗證背景的使用者行為。 |
| [!UICONTROL Enable for Wishlist Sharing] | 網站 | 指定客戶[共用願望清單](../../stores-purchase/wishlist-storefront.md#share-the-wish-list)時所使用的reCAPTCHA型別。 選項：<br/>**`No`**- （預設）不會驗證郵件和電子郵件提交。<br />**`reCAPTCHA v2 ("I am not a robot")`** — 要求使用者選取&#x200B;_我不是自動機制_&#x200B;核取方塊。<br />**`Invisible reCAPTCHA v2`**— 在背景驗證使用者行為，不需要根據分數進行互動。<br/>**`Invisible reCAPTCHA v3`** - （建議）根據互動分數，驗證背景的使用者行為。 |
| [!UICONTROL Enable for Coupon Codes] | 網站 | 指定當客戶輸入[優惠券代碼](../../merchandising-promotions/price-rules-cart-coupon.md)時所使用的reCAPTCHA型別。 選項：<br/>**`No`**- （預設）不會驗證優惠券代碼提交。<br />**`reCAPTCHA v2 ("I am not a robot")`** — 要求使用者選取&#x200B;_我不是自動機制_&#x200B;核取方塊。<br />**`Invisible reCAPTCHA v2`**— 在背景驗證使用者行為，不需要根據分數進行互動。<br/>**`Invisible reCAPTCHA v3`** - （建議）根據互動分數，驗證背景的使用者行為。 |
| [!UICONTROL Enable for PayPal Payflow Pro payment form] | 網站 | 指定當客戶使用[PayPal Payflow Pro](../../stores-purchase/paypal-payflow-pro.md)支付購買費用時，所使用的reCAPTCHA型別。 選項： <br/>**`No`**- （預設）不會驗證密碼重設要求。<br />**`reCAPTCHA v2 ("I am not a robot")`** — 要求使用者選取&#x200B;_我不是自動機制_&#x200B;核取方塊。<br />**`Invisible reCAPTCHA v2`**— 在背景驗證使用者行為，不需要根據分數進行互動。<br/>**`Invisible reCAPTCHA v3`** - （建議）根據互動分數，驗證背景的使用者行為。 |

{style="table-layout:auto"}
