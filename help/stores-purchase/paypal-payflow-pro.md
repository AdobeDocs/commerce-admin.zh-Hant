---
title: PayPal Payflow Pro
description: 瞭解如何將PayPal Payflow Pro設定為商店上的線上支付解決方案。
exl-id: c720b33c-44e1-4954-b5be-38932393a43c
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '2173'
ht-degree: 0%

---

# PayPal Payflow Pro

PayPal Payflow Pro閘道(先前稱為 _驗證_，適用於美國、加拿大、澳洲和紐西蘭的客戶。 與其他PayPal付款方式不同，商戶每月收取固定費用，另加每項交易的固定費用（無論數量為何）。

![使用PayPal結帳](./assets/storefront-cart-paypal.png){width="700" zoomable="yes"}

>[!IMPORTANT]
>
>**PSD2需求：** <br/>
>自2019年9月14日起，歐洲銀行可能會拒絕不符合規定的付款 [PSD2](../getting-started/compliance-payment-services-directive.md) 需求。 為了遵循PSD2，PayPal Payflow Pro必須與協力廠商外掛程式整合。 若要深入瞭解，請參閱 [Payflow的3-D安全](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-mpi/).

## 需求

- [PayPal企業帳戶][1] - PayPal Payflow Pro閘道將PayPal的商家帳戶與商家網站連結，同時充當閘道與商家帳戶。

- 如果您管理多個Adobe Commerce和Magento Open Source網站，每個網站都必須有個別的PayPal商家帳戶。

## 客戶工作流程

1. **客戶前往結帳**  — 結帳時，客戶選擇使用PayPal Payflow Pro付款，並輸入信用卡資訊。 客戶無須擁有個人PayPal帳戶。 不過，根據商家所在的國家/地區，客戶也可以使用個人PayPal帳戶支付訂單。
1. **客戶提交訂單**  — 客戶提交訂單，並將訂單資訊傳送至PayPal進行處理。 客戶不會離開您網站的結帳頁面。
1. **PayPal完成交易**  — 在下單時接受付款。 視組態中指定的付款作業而定，將會建立銷售訂單或銷售訂單與商業發票。

## 線上訂單處理工作流程

1. **管理員提交線上發票**  — 商店管理員會提交線上發票，因此會建立對應的交易與發票。
1. **PayPal接收交易**  — 訂單資訊會傳送至PayPal。 已產生交易與商業發票的記錄。 您可以檢視您的所有「Payflow Pro閘道」交易 [PayPal商家帳戶][2].

>[!NOTE]
>
>PayPal Payflow Pro不支援部份商業發票與部份退款。

## 設定您的PayPal帳戶

1. 登入您的 [PayPal企業帳戶][2].

1. 設定 [託管的簽出頁面][4] 搭配使用PayPal Manager及下列設定：

   - 在 **[!UICONTROL Choose your settings]**，設定 **[!UICONTROL Transaction Process Mode]** 至 `Live`.

   - 在 **[!UICONTROL Display options on payment page]**，設定 **取消URL** 至 `POST`.

   - 在 **[!UICONTROL Billing Information]**，選取卡片安全碼 **[!UICONTROL CSC]** 必填欄位和可編輯欄位的核取方塊。

   - 在 **[!UICONTROL Payment Confirmation]**，設定 **[!UICONTROL Return URL Method]** 至 `POST`.

   - 在 **[!UICONTROL Security Options]**，完成下列設定：

      - **[!UICONTROL AVS]**: `No`
      - **[!UICONTROL CSC]**: `No`
      - **[!UICONTROL Enable Secure Token]**: `Yes`

   - 選擇 **[!UICONTROL Customize]**，然後選擇 **[!UICONTROL Layout C]**.

     版面C只會顯示信用卡和借記卡欄位，而且可以在您的網站上設定框架，或作為獨立的快顯視窗使用。 大小固定為490 x 565畫素，並額外留出空間以儲存錯誤訊息。 在某些系統上，此設定可更正透明重新導向的問題。

1. 組態設定完成後，按一下 **[!UICONTROL Save and Publish]**.

1. 在PayPal管理員功能表中，選擇 **[!UICONTROL Account Administration]**.

1. 在 **[!UICONTROL Manage Security]**，按一下 **[!UICONTROL Transaction Settings]** 並執行下列動作：

   - 設定 **[!UICONTROL Allow reference transactions]** 至 `Yes`.

   - 按一下 **[!UICONTROL Confirm]**.

     >[!NOTE]
     >
     >如果您有多個Commerce網站，則必須為每個網站建立個別的PayPal付款進階帳戶。

1. 設定其他使用者（由PayPal建議）：

   - 在主功能表的第二列，按一下 **[!UICONTROL Manage Users]**.

   - 若要將其他使用者新增至帳戶，請按一下 **[!UICONTROL Add User]**. 此連結位於「管理使用者」標題的正上方。

   - 填妥以下章節的必要欄位 _[!UICONTROL Add User]_表單：

      - [!UICONTROL Admin Confirmation]
      - [!UICONTROL User Information]
      - [!UICONTROL User Login Information]
      - [!UICONTROL Assign Privilege to User]

   - 按一下 **[!UICONTROL Update]**.

1. 請務必登出您的PayPal帳戶。

## 在Commerce中設定PayPal Payflow Pro

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

1. 展開 **[!UICONTROL PayPal Payment Gateways]** （如有需要），然後按一下 **[!UICONTROL Configure]** 的 **[!UICONTROL Payflow Pro]**.

   ![設定 — Payflow Pro](./assets/payflow-pro.png){width="600" zoomable="yes"}

### 步驟2：完成必要的PayPal設定

![必要設定 — PayPal Payflow Pro](./assets/payflow-pro-required-a.png){width="600" zoomable="yes"}

1. （選擇性）輸入 **[!UICONTROL Email Associated with your PayPal Merchant Account]**.

   >[!IMPORTANT]
   >
   >電子郵件地址區分大小寫。 若要接收付款，電子郵件地址必須與您PayPal商家帳戶中指定的電子郵件地址相符。

1. 輸入下列其中一個憑證，您可用來登入PayPal商家帳戶：

   - **[!UICONTROL Partner]**  — 您的PayPal合作夥伴ID。
   - **[!UICONTROL User]**  — 在您的PayPal帳戶中設定的其他使用者ID。
   - **[!UICONTROL Vendor]**  — 您的PayPal使用者登入名稱

1. 輸入 **[!UICONTROL Password]** 和您的PayPal帳戶相關聯的專案。

1. 若要執行測試交易，請設定 **[!UICONTROL Test Mode]** 至 `Yes`.

   在沙箱中測試設定時，僅使用 [信用卡號碼][3] 由PayPal建議。 當您準備好要前往生產環境時，請返回設定並將測試模式設定為 `No`.

1. 如果您的系統使用Proxy伺服器來建立與PayPal系統的連線，請設定 **[!UICONTROL Use Proxy]** 至 `Yes` 並執行下列動作：

   - 輸入IP位址 **[!UICONTROL Proxy Host]**.

   - 輸入連線埠號碼 **[!UICONTROL Proxy Port]**.

     當伺服器防火牆阻止直接存取PayPal伺服器時，就會使用Proxy。 在這種情況下，會使用協力廠商伺服器來轉送流量。

1. 設定 **[!UICONTROL Enable this Solution]** 至 `Yes`.

1. 如果您想要提供 [PayPal點數](paypal.md#paypal-credit-and-pay-later) 對您的客戶，設定 **[!UICONTROL Enable PayPal Credit]** 至 `Yes`.

1. 如果您想要安全地儲存客戶付款/信用卡詳細資料，以便客戶不需要每次都重新輸入付款資訊，請設定 **[!UICONTROL Vault Enabled]** 至 `Yes`.

### 步驟3：設定廣告PayPal信用/廣告PayPal PayLater （選擇性）

從2.4.3版開始，在包含PayPal的部署中支援PayPal PayLater。 此功能可讓購物者以雙週分期付款的方式支付訂單，而不需在購買時支付全額。 已棄用PayPal點數體驗。

設定 **[!UICONTROL Enable PayPal PayLater Experience]** 變更為下列其中一項：

- `Yes`  — 設定廣告PayPal PayLater
- `No`  — 若要設定廣告PayPal信用

#### 廣告PayPal點數

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Advertise PayPal Credit]** 區段。

   ![廣告PayPal點數](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png){width="600" zoomable="yes"}

1. 若要取得您的帳戶資訊，請按一下 **[!UICONTROL Get Publisher ID from PayPal]** 並依照指示操作。

1. 輸入您的 **[!UICONTROL Publisher ID]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Home Page]** 區段。

   ![廣告PayPal信用首頁設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

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

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 其餘的段落，並重複前面的步驟來設定首頁：

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
   - **[!UICONTROL Checkout Payment Step]**
   - **[!UICONTROL Catalog Category Page]**

### 步驟4：完成基本設定

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Basic Settings - PayPal Payflow Pro]** 區段。

   ![基本設定 — PayPal Payflow Pro_](../configuration-reference/sales/assets/payment-methods-paypal-payflow-pro-basic-settings.png){width="600" zoomable="yes"}

1. 的 **[!UICONTROL Title]**，輸入在結帳時識別PayPal Payflow Pro的標題。

   建議您使用標題 _借記卡或信用卡_.

1. 如果您提供多種付款方式，請輸入數字 **[!UICONTROL Sort Order]** 決定與其他付款方式一起列出時，Payflow Pro出現的順序。

   此數字與其他付款方式相關。 (`0` =第一個， `1` =秒， `2` =第三個，依此類推。)

1. 設定 **[!UICONTROL Payment Action]** 變更為下列其中一項：

   - `Authorization`  — 核准購買並保留資金。 此金額必須等到商戶擷取後才會提取。
   - `Sale`  — 採購金額已獲授權，並立即從客戶帳戶中提取。

1. 的 **[!UICONTROL Credit Card Settings]**，選取您接受在商店付款的信用卡。

   若要選取多個卡片，請按住Ctrl鍵(PC)或Command鍵(Mac)，然後按一下每個卡片。

   >[!NOTE]
   >
   >American Express需要額外的合約。

### 步驟5：完成進階設定

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Advanced Settings]** 區段。

   ![進階設定 — PayPal Payflow Pro](../configuration-reference/sales/assets/payment-methods-paypal-payflow-pro-advanced-settings.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Payment Applicable From]** 變更為下列其中一項：

   - `All Allowed Countries`  — 來自所有客戶的客戶 [國家/地區](../getting-started/store-details.md#country-options) 在商店設定中指定的可使用此付款方式。
   - `Specific Countries`  — 選擇此選項後， _[!UICONTROL Payment from Specific Countries]_清單隨即顯示。 按住Ctrl鍵(PC)或Command鍵(Mac)，並在清單中選取客戶可在您的商店購買產品的國家/地區。

1. 若要將與付款系統的通訊寫入記錄檔，請設定 **[!UICONTROL Debug Mode]** 至 `Yes`.

   >[!NOTE]
   >
   >根據PCI資料安全性標準，記錄檔中不會記錄信用卡資訊。

1. 若要啟用主機驗證功能，請設定 **[!UICONTROL Enable SSL Verification]** 至 `Yes`.

1. 若要要求客戶輸入CVV代碼，請設定 **[!UICONTROL Require CVV Entry]** 至 `Yes`.

1. 視您的商店需求，完成下列章節：

   - [CVV和AVS設定](#cvv-and-avs-settings)
   - [結算報表設定](#settlement-report-settings)
   - [前端體驗設定](#frontend-experience-settings)

#### CVV和AVS設定

若要在「位址驗證系統」識別不符狀況時，決定何時應拒絕交易，請指定如何處理各種狀況。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL CVV and AVS Settings]** 區段。

   ![CVV和AVS設定 — PayPal Payflow Pro](./assets/payflow-pro-cvv-avs.png){width="600" zoomable="yes"}

1. 若要根據不符合的街道不符來拒絕交易，請設定 **[!UICONTROL AVS Street Does Not Match]** 至 `Yes`.

1. 若要根據不相符的郵遞區號拒絕交易，請設定 **[!UICONTROL AVS Zip Does Not Match]** 至 `Yes`.

1. 若要根據不相符的國家識別碼拒絕交易，請設定 **[!UICONTROL International AVS Indicator Does Not Match]** 至 `Yes`.

1. 若要根據不相符的CVV代碼拒絕交易，請設定 **[!UICONTROL International Card Security Code Does Not Match]** 至 `Yes`.

#### 結算報表設定

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Settlement Report Settings]** 區段。

   ![結算報表設定 — PayPal Payflow Pro](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

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

使用「前端體驗設定」來選擇要在您的網站上顯示的PayPal標誌，以及自訂PayPal商家頁面的外觀。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Frontend Experience Settings]** 區段。

   ![前端體驗設定 — PayPal Payflow Pro](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png){width="600" zoomable="yes"}

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

### 步驟6：完成PayPal Express結帳的基本設定

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Basic Settings - PayPal Express Checkout]** 區段。

   ![快速簽出基本設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-pro-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. 的 **[!UICONTROL Title]**，輸入在結帳時識別此付款方式的標題。

   將標題設為 _PayPal_ 建議每個商店檢視使用。

1. 如果您提供多種付款方式，請輸入數字 **[!UICONTROL Sort Order]** 決定與其他付款方式一起列出時，PayPal Express結帳的順序。

   此數字與其他付款方式相關。 (`0` =第一個， `1` =秒， `2` =第三個，依此類推。)

1. 設定 **[!UICONTROL Payment Action]** 變更為下列其中一項：

   - `Authorization`  — 核准購買並保留資金。 金額必須等到提取後才會提取 _已擷取_ 由商家提供。
   - `Sale`  — 採購金額已獲授權，並立即從客戶帳戶中提取。

1. 若要顯示 _[!UICONTROL Check out with PayPal]_產品頁面上的按鈕，設定&#x200B;**[!UICONTROL Display on Product Details Page]**至 `Yes`.

### 步驟7：完成PayPal Express簽出的進階設定

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Advanced Settings]** 區段。

   ![快速簽出進階設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-pro-express-checkout-advanced-settings.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Display on Shopping Cart]** 至 `Yes`.

1. 設定 **[!UICONTROL Payment Applicable From]** 變更為下列其中一項：

   - `All Allowed Countries`  — 來自您商店設定中所指定之所有國家/地區的客戶均可以使用此付款方式。
   - `Specific Countries`  — 選擇此選項後， _[!UICONTROL Payment from Specific Countries]_清單隨即顯示。 若要選取多個國家/地區，請按住Ctrl鍵(PC)或Command鍵(Mac)，然後按一下每個專案。

1. 若要將與付款系統的通訊寫入記錄檔，請設定 **[!UICONTROL Debug Mode]** 至 `Yes`.

   >[!NOTE]
   >
   >根據PCI資料安全性標準，記錄檔中不會記錄信用卡資訊。

1. 若要啟用主機驗證功能，請設定 **[!UICONTROL Enable SSL Verification]** 至 `Yes`.

1. 若要從PayPal網站依明細專案顯示客戶訂單的完整摘要，請設定 **[!UICONTROL Transfer Cart Line Items]** 至 `Yes`.

1. 若要允許客戶從PayPal網站完成交易，而不返回您的商店進行訂單審查，請設定 **[!UICONTROL Skip Order Review Step]** 至 `Yes`.

1. 完成後，按一下 **[!UICONTROL Save Config]**.

### 步驟8：新增Google reCAPTCHA

為了更能保護PayPal Payflow Pro結帳，請啟用Google reCAPTCHA。 它包含使用可點按介面或隱藏檢查來驗證客戶的重新驗證碼選項。 建議使用隱藏選項，以提高銷售轉換率並保護您的商店。 如需詳細資訊，請參閱 [Google reCAPTCHA](../systems/security-google-recaptcha.md).

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://manager.paypal.com/
[3]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[4]: https://developer.paypal.com/docs/payflow/integration-guide/configure-hosted-checkout/#configuring-hosted-pages-using-paypal-manager
