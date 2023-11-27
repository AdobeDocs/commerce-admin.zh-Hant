---
title: PayPal支付標準
description: 瞭解如何將PayPal Payments Standard設定為商店上的線上付款解決方案。
exl-id: b4024dac-34d7-4f1a-ad9d-0fc406194609
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '2073'
ht-degree: 0%

---

# PayPal支付標準

[PayPal支付標準][4] 是接受線上付款的最簡單方式。 只要在商店中新增結帳按鈕，您就可以讓客戶享有信用卡和PayPal付款的便利性。

>[!NOTE]
>
>對於美國以外的商家，則稱為 _PayPal網站支付標準_.

有了PayPal Payments Standard，您可以在行動裝置上刷信用卡。 不需每月付費，您可透過eBay支付。 支援的信用卡包括Visa、MasterCard、Discover和American Express。 此外，客戶可以直接從其個人PayPal帳戶付款。 PayPal支付標準可在PayPal全球參考清單的所有國家/地區使用。

>[!IMPORTANT]
>
>**PSD2需求：** <br/>
>自2019年9月14日起，歐洲銀行可能會拒絕不符合規定的付款 [PSD2](../getting-started/compliance-payment-services-directive.md) 需求。 PayPal Payments Standard不需採取任何動作即可符合PSD2，因為所有要求都由PayPal處理。

## 商家需求

- [PayPal企業帳戶][1]

## 簽出工作流程

對於客戶而言，如果個人PayPal帳戶上的信用卡資訊是最新的，則PayPal Payments Standard為一步驟流程。

1. **客戶下訂單**  — 客戶按一下/點選 _立即付款_ 按鈕以完成購買。

1. **PayPal處理交易**  — 將客戶重新導向至PayPal網站以完成交易。

## 設定PayPal付款標準

>[!NOTE]
>
>PayPal Payments Standard不能與任何其他PayPal方法同時使用，包括Express Checkout。 如果您變更付款解決方案，先前使用的解決方案會停用。

>[!TIP]
>
>按一下 **[!UICONTROL Save Config]** 隨時儲存進度。

### 步驟1：開始設定

此設定方法假設您有現有的PayPal帳戶。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Sales]** 並選擇 **[!UICONTROL Payment Methods]**.

1. 如果您的Commerce安裝有多個網站、商店或檢視，設定 **[!UICONTROL Store View]** 到您要套用此設定的存放區檢視。

1. 在 _[!UICONTROL Merchant Location]_區段，選取&#x200B;**[!UICONTROL Merchant Country]**您的企業所在位置。

   此設定會決定要選取顯示在設定中的PayPal解決方案。

   ![商戶國家](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. 展開 **[!UICONTROL PayPal All-in-One Payment Solutions]** 並按一下 **[!UICONTROL Configure]** 的 **[!UICONTROL Payments Standard]**.

   ![PayPal支付標準](./assets/paypal-payments-standard.png){width="700" zoomable="yes"}

### 步驟2：啟用並連線您的PayPal帳戶

![PayPal支付標準組態](./assets/paypal-payments-display.png){width="600" zoomable="yes"}

1. 連線您的帳戶以進行測試或生產：

   - 若要測試（開發）模式，請按一下 **[!UICONTROL Sandbox Credentials]** 並輸入您的 [PayPal沙箱][3] 認證。
   - 在生產模式中，按一下 **[!UICONTROL Connect with PayPal]** 並輸入您的生產帳戶認證。

   當您的連線通過驗證時，您可以繼續。

1. 設定 **[!UICONTROL Enable this Solution]** 至 `Yes`.

1. 如果您想要提供 [PayPal點數](paypal.md#paypal-credit-and-pay-later) 對您的客戶，設定 **[!UICONTROL Enable PayPal Credit]** 至 `Yes`.

### 步驟3：完成「付款標準」設定

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Payments Standard]** 區段。

   ![必要設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-standard-required.png){width="600" zoomable="yes"}

1. 輸入 **[!UICONTROL Email Associated with your PayPal Merchant Account]**.

   >[!IMPORTANT]
   >
   >電子郵件地址區分大小寫。 若要接收付款，您輸入的電子郵件地址必須符合您在PayPal商家帳戶中指定的電子郵件地址。

   如果您沒有PayPal帳戶，請按一下 **[!UICONTROL Start accepting payments via PayPal]**.

1. 設定 **[!UICONTROL API Authentication Methods]** 變更為下列其中一項：

   - `API Signature`  — 此PayPal驗證方法最容易實作，而且是以您的使用者名稱、密碼以及可識別您帳戶的唯一字元與數字字串為基礎。 API簽章認證不會過期。
   - `API Certificate`  — 此PayPal驗證方法比較安全，是以您的使用者名稱、密碼和可下載的憑證為基礎。 API憑證會在三年後到期，且必須續約。

   如有需要，請完成下列作業：

   - **[!UICONTROL API Username]**
   - **[!UICONTROL API Password]**
   - **[!UICONTROL API Signature]**

1. 如果您使用來自沙箱帳戶的認證，請設定 **[!UICONTROL Sandbox Mode]** 至 `Yes`.

   在沙箱中測試設定時，僅使用 [信用卡號碼][2] 由PayPal建議。 當您準備好進入生產環境時，請返回設定並將沙箱模式設定為 `No` 並連線至您的生產PayPal帳戶。

1. 如果您的系統使用Proxy伺服器來建立Adobe Commerce或Magento Open Source與PayPal支付系統之間的連線，請設定 **[!UICONTROL API Uses Proxy]** 至 `Yes` 並完成下列作業：

   - **[!UICONTROL Proxy Host]**
   - **[!UICONTROL Proxy Port]**

### 步驟4：設定廣告PayPal Credit /廣告PayPal PayLater （選擇性）

從2.4.3版開始，在包含PayPal的部署中支援PayPal PayLater。 此功能可讓購物者以雙週分期付款的方式支付訂單，而不需在購買時支付全額。 已棄用PayPal點數體驗。

設定 **[!UICONTROL Enable PayPal PayLater Experience]** 變更為下列其中一項：

- `Yes`  — 設定廣告PayPal PayLater
- `No`  — 若要設定廣告PayPal信用

#### 廣告PayPal點數

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Advertise PayPal Credit]** 區段。

   ![廣告PayPal信用首頁設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

1. 若要取得您的帳戶資訊，請按一下 **[!UICONTROL Get Publisher ID from PayPal]** 並依照指示操作。

1. 輸入您的 **[!UICONTROL Publisher ID]**.

   ![廣告PayPal點數](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png){width="600" zoomable="yes"}

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Home Page]** 區段。

1. 若要在頁面上放置橫幅，請設定 **[!UICONTROL Display]** 至 `Yes`.

1. 設定 **[!UICONTROL Position]** 變更為下列其中一項：

   - `Header (center)`
   - `Sidebar (right)`

1. 設定 **[!UICONTROL Size]** 變更為下列其中一項：

   - `190 x 100`
   - `234 x 60`
   - `300 x 50`
   - `468 x 60`
   - `728 x 90`
   - `800 x 66`

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 其餘部分並重複上述步驟：

   - **[!UICONTROL Catalog Category Page]**
   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**

#### 廣告PayPal PayLater

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Advertise PayPal PayLater]** 區段。

1. 設定 **[!UICONTROL Enable PayPal PayLater]** 至 `Yes`.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Home Page]** 區段。

   ![廣告PayPal信用首頁設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-paylater-home-page.png){width="600" zoomable="yes"}

1. 若要在頁面上放置橫幅，請設定 **[!UICONTROL Display]** 至 `Yes`.

1. 設定 **[!UICONTROL Position]** 變更為下列其中一項：

   - `Header (center)`
   - `Sidebar`

1. 設定 **[!UICONTROL Style Layout]** 變更為下列其中一項：

   - `Text`
   - `Flex`

1. 的 [!UICONTROL Style Layout] **[!UICONTROL Text]** 僅限，設定 **[!UICONTROL Logo Type]** 變更為下列其中一項：

   - `Primary`
   - `Alternative`
   - `Inline`
   - `None`

1. 的 [!UICONTROL Style Layout] **[!UICONTROL Text]** 僅限，設定 **[!UICONTROL Logo Position]** 變更為下列其中一項：

   - `Left`
   - `Right`
   - `Top`

1. 的 [!UICONTROL Style Layout] **[!UICONTROL Text]** 僅限，設定 **[!UICONTROL Text Color]** 變更為下列其中一項：

   - `Black`
   - `White`
   - `Monochrome`
   - `Grayscale`

1. 的 [!UICONTROL Style Layout] **[!UICONTROL Text]** 僅限，設定 **[!UICONTROL Text Size]** 變更為下列其中一項：

   - `10px`
   - `11px`
   - `12px`
   - `13px`
   - `14px`
   - `15px`
   - `16px`

1. 的 [!UICONTROL Style Layout] **[!UICONTROL Flex]** 僅限，設定 **[!UICONTROL Ratio]** 變更為下列其中一項：

   - `1x1`
   - `1x4`
   - `8x1`
   - `20x1`

1. 的 [!UICONTROL Style Layout] **[!UICONTROL Flex]** 僅限，設定 **[!UICONTROL Color]** 變更為下列其中一項：

   - `Blue`
   - `Black`
   - `White`
   - `White No Border`
   - `Gray`
   - `Monochrome`
   - `Grayscale`

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 其餘部分並重複上述步驟：

   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**
   - **結帳付款步驟**
   - **[!UICONTROL Catalog Category Page]**

### 步驟5：完成基本設定

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Basic Settings - PayPal Website Payments Standard]** 區段。

   ![基本設定](./assets/paypal-payments-basic.png){width="600" zoomable="yes"}

1. 的 **[!UICONTROL Title]**，輸入在結帳時識別此付款方式的標題。

   建議您使用標題 _PayPal_ 用於所有商店檢視。

1. 如果您提供多種付款方式，請輸入數字 **[!UICONTROL Sort Order]** 以決定與其他付款方式一起列出時，PayPal Payments Standard出現的順序。

   此數字與其他付款方式相關。 (`0` =第一個， `1` =秒， `2` =第三個，依此類推。)

1. 設定 **[!UICONTROL Payment Action]** 變更為下列其中一項：

   - `Authorization`  — 核准購買並保留資金。 此金額必須等到商戶擷取後才會提取。
   - `Sale`  — 採購金額已獲授權，並立即從客戶帳戶中提取。

1. 若要顯示 _[!UICONTROL Check out with PayPal]_產品頁面上的按鈕，設定&#x200B;**[!UICONTROL Display on Product Details Page]**至 `Yes`.

### 步驟6：完成進階設定

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Advanced Settings]** 區段。

   ![進階設定](../configuration-reference/sales/assets/payment-methods-paypal-payment-standard-advanced.png){width="600" zoomable="yes"}

1. 若要讓PayPal Payments Standard可從購物車和迷你購物車使用，請設定 **[!UICONTROL Display on Shopping Cart]** 至 `Yes`.

1. 設定 **[!UICONTROL Payment from Applicable Countries]** 變更為下列其中一項：

   - `All Allowed Countries`  — 來自所有客戶的客戶 [國家/地區](../getting-started/store-details.md#country-options) 在商店設定中指定的可使用此付款方式。
   - `Specific Countries`  — 選擇此選項後， _[!UICONTROL Payment from Specific Countries]_清單隨即顯示。 若要選取多個國家/地區，請按住Ctrl鍵(PC)或Command鍵(Mac)，然後按一下每個選項。

1. 若要在記錄檔中記錄與付款系統的通訊，請設定 **[!UICONTROL Debug Mode]** 至 `Yes`.

   >[!NOTE]
   >
   >記錄檔儲存在伺服器上，只有開發人員才能存取。 根據PCI資料安全性標準，記錄檔中不會記錄信用卡資訊。

1. 若要啟用SSL驗證，請設定 **[!UICONTROL Enable SSL Verification]** 至 `Yes`.

1. 若要在PayPal付款頁面的訂單中顯示每個明細專案的摘要，請設定 **[!UICONTROL Transfer Cart Line Items]** 至 `Yes`.

   若要在摘要中包含最多十個送貨選項，請設定 **[!UICONTROL Transfer Shipping Options]** 至 `Yes`. （只有行專案設為移轉時，才會顯示此選項。）

1. 若要判斷用於PayPal接受按鈕的影像型別，請設定 **[!UICONTROL Shortcut Buttons Flavor]** 變更為下列其中一項：

   - `Dynamic` - （建議）顯示可從PayPal伺服器動態變更的影像。
   - `Static`  — 顯示無法動態變更的特定影像。

1. 若要允許沒有PayPal帳戶的客戶使用此方法購買，請設定 **[!UICONTROL Enable PayPal Guest Checkout]** 至 `Yes`.

1. 設定 **[!UICONTROL Require Customer's Billing Address]** 變更為下列其中一項：

   - `Yes`  — 所有購買都需要客戶帳單地址。
   - `No`  — 任何購買均不需要客戶帳單地址。
   - `For Virtual Quotes Only`  — 僅需虛擬報價的客戶帳單地址。

1. 若要允許客戶進入 [PayPal帳單合約](paypal-billing-agreements.md) 當客戶帳戶中無可用的有效帳單協定時，透過您的商店，設定 **[!UICONTROL Billing Agreement Signup]** 變更為下列其中一項：

   - `Auto`  — 客戶可在「快速結帳」流程期間輸入帳單協定，或使用其他付款方式。
   - `Ask Customer`  — 客戶可決定是否在「快速結帳」工作流程期間訂立帳單協定。
   - `Never`  — 客戶無法在「快速結帳」工作流程期間輸入帳單協定。

   >[!NOTE]
   >
   >商家必須要求PayPal商家技術支援以在其帳戶中啟用帳單協定。 此 _帳單協定註冊_ 只有在PayPal確認已針對您的商家帳戶啟用帳單協定之後，才能啟用引數。

1. 若要允許客戶從PayPal網站完成交易，而不返回您的商店進行訂單審查，請設定 **[!UICONTROL Skip Order Review Step]** 至 `Yes`.

### 步驟7：完成並儲存組態設定

1. 視您的商店需求，完成下列章節：

   - [PayPal帳單協定設定](#paypal-billing-agreement-settings)
   - [結算報表設定](#settlement-report-settings)
   - [前端體驗設定](#frontend-experience-settings)

1. 完成後，按一下 **[!UICONTROL Save Config]**.

#### PayPal帳單協定設定

A [帳單協定](paypal-billing-agreements.md) 是商戶與客戶之間的銷售協定，已獲得PayPal授權用於多份訂單。 在結帳程式中，「帳單協定」付款選項只會針對已與貴公司簽訂帳單協定的客戶顯示。 在PayPal授權合約之後，付款系統就會發出唯一的參考ID，以識別與合約相關聯的每張訂單。 與採購單類似，客戶可與貴公司設定的帳單協定數並無限制。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL PayPal Billing Agreement Settings]** 區段。

   ![帳單協定設定](../configuration-reference/sales/assets/payment-methods-paypal-express-checkout-billing-agreement-settings.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Enabled]** 至 `Yes`.

1. 的 **[!UICONTROL Title]**，輸入在結帳時識別PayPal帳單協定方法的標題。

1. 如果您提供多種付款方式，請在 **[!UICONTROL Sort Order]** 在結帳期間與其他付款方式一起列出時，用來決定「帳單協定」顯示順序的欄位。

1. 設定 **[!UICONTROL Payment Action]** 變更為下列其中一項：

   - `Authorization`  — 核准購買並保留資金。 此金額必須等到商家「擷取」後才會提取。
   - `Sale`  — 採購金額已獲授權，並立即從客戶帳戶中提取。

1. 設定 **[!UICONTROL Payment Applicable From]** 變更為下列其中一項：

   - `All Allowed Countries`  — 來自您商店設定中所指定之所有國家/地區的客戶均可以使用此付款方式。
   - `Specific Countries`  — 選擇此選項後， _[!UICONTROL Payment from Specific Countries]_清單隨即顯示。 若要選取多個國家/地區，請按住Ctrl鍵(PC)或Command鍵(Mac)並按一下每個國家/地區。

1. 若要在記錄檔中記錄與付款系統的通訊，請設定 **[!UICONTROL Debug Mode]** 至 `Yes`.

   >[!NOTE]
   >
   >記錄檔儲存在伺服器上，只有開發人員才能存取。 根據PCI資料安全性標準，記錄檔中不會記錄信用卡資訊。

1. 若要啟用SSL驗證，請設定 **[!UICONTROL Enable SSL Verification]** 至 `Yes`.

1. 若要在PayPal付款頁面上顯示客戶訂單中每個明細專案的摘要，請設定 **[!UICONTROL Transfer Cart Line Items]** 至 `Yes`.

1. 若要允許客戶從其客戶帳戶的控制面板啟動帳單協定，請設定 **[!UICONTROL Allow in Billing Agreement Wizard]** 至 `Yes`.

#### 結算報表設定

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Settlement Report Settings]** 區段。

   ![結算報表設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

1. 的 **[!UICONTROL SFTP Credentials]**，請執行下列動作：

   - 如果您已註冊PayPal安全FTP伺服器，請輸入下列SFTP登入認證：

      - 登入
      - 密碼

   - 若要使用「快速簽出」在您的網站上線之前執行測試報告，請設定 **[!UICONTROL Sandbox Mode]** 至 `Yes`.

   - 輸入 **[!UICONTROL Custom Endpoint Hostname or IP Address]**.

     預設值為 `reports.paypal.com`.

   - 輸入 **[!UICONTROL Custom Path]** 報告儲存的位置。

     預設值為 `/ppreports/outgoing`.

1. 若要根據排程產生報表，請填妥 **[!UICONTROL Scheduled Fetching]** 設定：

   - 設定 **[!UICONTROL Enable Automatic Fetching]** 至 `Yes`.

   - 設定 **[!UICONTROL Schedule]** 變更為下列其中一項：

      - `Daily`
      - `Every 3 Days`
      - `Every 7 Days`
      - `Every 10 Days`
      - `Every 14 Days`
      - `Every 30 Days`
      - `Every 40 Days`

     PayPal會保留每個報表45天。

   - 設定 **[!UICONTROL Time of Day]** 到您想要產生報告時的小時、分鐘和秒。

#### 前端體驗設定

使用 _[!UICONTROL Frontend Experience Settings]_選擇要在您的網站上顯示的PayPal標誌，以及自訂PayPal商家頁面的外觀。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Frontend Experience Settings]** 區段。

   ![前端體驗設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png){width="600" zoomable="yes"}

1. 選取 **[!UICONTROL PayPal Product Logo]** 出現在商店的PayPal區塊中。

   PayPal標誌有四種樣式和兩種尺寸：

   - `No Logo`
   - `We Prefer PayPal (150 x 60 or 150 x 40)`
   - `Now Accepting PayPal (150 x 60 or 150 x 40)`
   - `Payments by PayPal (150 x 60 or 150 x 40)`
   - `Shop Now Using PayPal (150 x 60 or 150 x 40)`

1. 若要自訂PayPal商家頁面的外觀：

   - 輸入 **[!UICONTROL Page Style]** 要套用至PayPal商家頁面的專案：

      - `paypal`  — 使用PayPal頁面樣式。
      - `primary`  — 使用您識別為 _主要_ 帳戶設定檔中的樣式。
      - `your_custom_value`  — 使用帳戶設定檔中指定的自訂付款頁面樣式。

   - 的 **[!UICONTROL Header Image URL]**，輸入您要在付款頁面左上角顯示的影像URL。 檔案大小上限為750畫素寬x 90畫素高。

     >[!NOTE]
     >
     >PayPal建議將影像存放在安全(https)伺服器上。 否則，瀏覽器可能會警告 _此頁面包含安全和非安全專案_.

   - 若要設定頁面的顏色，請輸入六個字元的十六進位代碼，不使用 `#` 符號，代表下列各項：

      - **[!UICONTROL Header Background Color]**  — 結帳頁面標頭的背景顏色。
      - **[!UICONTROL Header Border Color]**  — 標頭周圍兩畫素邊框的色彩。
      - **[!UICONTROL Page Background Color]**  — 結帳頁面以及頁首與付款表單周圍的背景顏色。

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[3]: https://developer.paypal.com/docs/api-basics/sandbox/
[4]: https://developer.paypal.com/docs/paypal-payments-standard/mobile-paypal-payments-standard/
