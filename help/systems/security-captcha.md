---
title: 驗證碼
description: 瞭解如何設定驗證碼以供管理員存取及註冊客戶所啟動的各種店面動作。
exl-id: b2867ad5-7d48-4e9f-b84e-3cf0a14ec16f
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 0%

---

# 驗證碼

驗證碼是一種視覺裝置，可確保人(而不是電腦（或「機器人」）)與網站互動。 CAPTCHA是 _完全自動化的公用圖靈測試，將電腦和人類區分開來_. 它可用於管理員存取和註冊客戶啟動的各種店面動作。 Adobe Commerce和Magento Open Source支援本主題所述的標準驗證碼和 [Google reCAPTCHA](security-google-recaptcha.md).

您可以按一下影像右上角的「重新載入」圖示，視需要多次重新載入驗證碼。 驗證碼是完全可設定的，並且可設定為每次都出現，或僅在已定義的失敗登入嘗試次數後出現。

![以驗證碼登入](./assets/customer-account-login-captcha.png){width="700" zoomable="yes"}

## 為管理員設定驗證碼

如需額外的安全性，您可以將驗證碼新增至「管理員登入及忘記密碼」頁面。 管理員使用者可按一下 _重新載入_ ![重新載入圖示](./assets/CAPTCHA-icon-reload.png) 圖示加以顯示。 重新載入的次數沒有限制。

![管理員 — 使用驗證碼登入](./assets/security-captcha-admin.png){width="300"}

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Advanced]** 並選擇 **[!UICONTROL Admin]**.

1. 在右上角，設定 **[!UICONTROL Store View]** 至 `Default`.

   如果 [範圍](../getting-started/websites-stores-views.md#scope-settings) ，請選擇您要套用驗證碼設定的網站。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL CAPTCHA]** 區段。

1. 設定 **[!UICONTROL Enable CAPTCHA in Admin]** 至 `Yes`. 然後完成其餘的選項，如下所示：

   ![管理員 — 驗證碼組態](../configuration-reference/advanced/assets/admin-captcha.png){width="600" zoomable="yes"}

   - 輸入 **[!UICONTROL Font]** 用於驗證碼符號(預設： `LinLibertine`)。

     若要新增您自己的字型，字型檔案必須位於與您的Commerce安裝相同的目錄中，並且必須在中宣告 `config.xml` 驗證碼模組的檔案，位於 `app/code/Magento/Captcha/etc`.

   - 選取下列任一項 **[!UICONTROL Forms]** 將使用CAPTCHA的位置。 若要選擇多個表單，請按住Ctrl鍵(PC)或Command鍵(Mac)。

      - `Admin Login`
      - `Admin Forgot Password`

   - 設定 **[!UICONTROL Displaying Modes]** 變更為下列其中一項：

      - `Always`  — 永遠都需要CAPTCHA才能登入管理員。
      - `After number of attempts to login`  — 此選項僅適用於「管理員登入」表單。 選取時， _[!UICONTROL Number of Unsuccessful Attempts to Login]_欄位隨即顯示。 輸入您要允許的登入嘗試次數。 值0 （零）類似於將「顯示模式」設定為 `Always`.

     若要追蹤失敗的登入嘗試次數，每次嘗試以一個電子郵件地址登入，以及從一個IP位址登入都會計算在內。 允許來自相同IP位址的登入嘗試次數上限為1,000。 此限制僅在啟用驗證碼時適用。

   - 的 **[!UICONTROL Number of Unsuccessful Attempts to Login]**，輸入在驗證碼出現之前，管理員可以嘗試登入的次數。 如果設定為零(`0`)，一律須要驗證碼。

   - 的 **[!UICONTROL CAPTCHA Timeout (minutes)]**，輸入驗證碼過期之前的分鐘數。 驗證碼過期時，管理員必須重新載入頁面。

   - 輸入 **[!UICONTROL Number of Symbols]** 以顯示在驗證碼中。 最多八個(`8`)符號。 對於隨每個CAPTCHA而變更的符號數量變數，請輸入一個範圍(例如 `5-8`)。

   - 的 **[!UICONTROL Symbols Used in CAPTCHA]**，請輸入您要在驗證碼中隨機出現的字母（a-z和A-Z）和數字(0-9)。 難以與其他符號區分的符號，例如 `i`， `l`，或 `1`的預設驗證碼符號集中不包含。

   - 設定 **[!UICONTROL Case Sensitive]** 至 `Yes` 如果您希望要求管理員完全按照驗證碼中的顯示方式，以大寫或小寫輸入字元。

1. 完成後，按一下 **[!UICONTROL Save Config]**.

## 為店面設定驗證碼

客戶每次登入帳戶時，或幾次嘗試登入失敗後，都需輸入驗證碼。 此外，店面中使用的許多表單可設定為需要由驗證碼驗證。

![結帳時進行驗證碼](./assets/storefront-checkout-payment-captcha.png){width="700" zoomable="yes"}

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Customers]** 並選擇 **[!UICONTROL Customer Configuration]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL CAPTCHA]** 區段。

![客戶驗證碼組態](../configuration-reference/customers/assets/customer-configuration-captcha.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Enable CAPTCHA on Storefront]** 至 `Yes`. 然後完成其餘的選項，如下所示：

   - 輸入 **[!UICONTROL Font]** 用於驗證碼符號(預設： `LinLibertine`)。

     若要新增您自己的字型，字型檔案必須位於與您的Commerce安裝相同的目錄中，並且必須在中宣告 `config.xml` 驗證碼模組的檔案。

   - 選取下列任一項 **[!UICONTROL Forms]** 將使用CAPTCHA的位置。 若要選擇多個表單，請按住Ctrl鍵(PC)或Command鍵(Mac)。

      - `Applying coupon code`
      - `Checkout/Placing Order`
      - `Create user`
      - `Login`
      - `Forgot password`
      - `Contact Us`
      - `Change password`
      - `Share Wishlist Form`
      - `Payflow Pro` (請參閱 [安全性修補程式](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/paypal-payflow-pro-active-carding-activity.html) _知識庫_ article)
      - `Send to Friend Form` ![Magento Open Source](../assets/open-source.svg) (僅限Magento Open Source)
      - `Add Gift Card Code` ![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)
      - `Create company` ![適用於Adobe Commerce的B2B](../assets/b2b.svg) (僅適用於Adobe Commerce的B2B)

   - 設定 **[!UICONTROL Displaying Mode]** 變更為下列其中一項：

      - `Always`  — 存取選取的表單一律需要驗證碼。
      - `After number of attempts to login`  — 輸入驗證碼出現之前的登入嘗試次數。 0的值（零）類似於「一律」。 選取後，會顯示失敗的登入嘗試次數。 此選項不適用於「忘記密碼」表單，如果啟用此表單，將一律顯示CAPTCHA。

   - 的 **[!UICONTROL Number of Unsuccessful Attempts to Login]**，輸入在驗證碼出現之前，客戶登入失敗的次數。 如果設定為零(`0`)，一律使用驗證碼。

   - 的 **[!UICONTROL CAPTCHA Timeout (minutes)]**，輸入驗證碼過期之前的分鐘數。 驗證碼過期時，客戶必須重新載入頁面才能產生新的驗證碼。

   - 輸入 **[!UICONTROL Number of Symbols]** 以顯示在驗證碼中。 最多八個(`8`)符號。 對於隨每個CAPTCHA而變更的符號數量變數，請輸入一個範圍(例如 `5-8`)。

   - 的 **[!UICONTROL Symbols Used in CAPTCHA]**，請輸入您要在驗證碼中隨機出現的字母（a-z和A-Z）和數字(0-9)。 預設字元集不包含類似的符號，例如 `I` 或 `1`. 為了獲得最佳效果，請使用使用者容易識別的符號。

   - 設定 **[!UICONTROL Case Sensitive]** 至 `Yes` 如果您想要求客戶完全依照驗證碼中所示輸入大寫或小寫字元。

1. 完成後，按一下 **[!UICONTROL Save Config]**.
