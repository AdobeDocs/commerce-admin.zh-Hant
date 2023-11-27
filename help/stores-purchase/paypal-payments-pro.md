---
title: PayPal Payments Pro
description: 瞭解如何在商店上將PayPal Payments Pro設定為線上付款解決方案。
exl-id: 9cc5c3a6-d471-4198-85a2-c4cf9dfd378b
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '2242'
ht-degree: 0%

---

# PayPal Payments Pro

[PayPal Payments Pro][3] 將商家帳戶與付款閘道集於一身，讓您建立自己的完整自訂結帳體驗。 PayPal Express Checkout會自動透過PayPal Payments Pro啟用，因此您可以利用超過1.1億位作用中的PayPal使用者。

![迷你購物車中顯示的PayPal Payments Pro](./assets/storefront-mini-cart-payments-pro-racer-tank.png){width="700" zoomable="yes"}

>[!IMPORTANT]
>
>**PSD2需求：** <br/>
>自2019年9月14日起，歐洲銀行可能會拒絕不符合規定的付款 [PSD2](../getting-started/compliance-payment-services-directive.md) 需求。 為了遵循PSD2，PayPal Payments Pro必須與協力廠商外掛程式整合。

>[!NOTE]
>
>目前，PayPal Payments Pro在美國、英國和加拿大均提供使用。

## 需求

- [PayPal商家帳戶][1] （啟用直接付款）

## 簽出工作流程

1. **客戶前往結帳**  — 客戶新增產品至購物車，然後按一下/點選 _繼續結帳_.|
1. **客戶選擇付款方式**  — 結帳時，客戶選擇 _PayPal直接付款_ 選項，然後輸入信用卡資訊。
   - 如果透過PayPal Payments Pro付款，客戶會在結帳過程中留在您的網站。
   - 如果透過PayPal Express Checkout付款，客戶會被重新導向至PayPal網站，以完成交易。

應客戶要求，商店管理員也可以從管理員建立訂單，並使用PayPal Payments Pro處理交易。

## 訂單處理工作流程

1. **已下訂單**  — 訂單可在商店管理員或PayPal商家帳戶中處理。

1. **[!UICONTROL Payment Action]**  — 組態中指定的付款動作會套用至訂單。 選項包括：

   - **授權** - Commerce會使用建立銷售訂單 _處理中_ 狀態。 在此情況下，將授權的金額正在等待核准。
   - **銷售** - Commerce會建立銷售訂單與商業發票。
   - **Capture** - PayPal會將訂單金額從客戶餘額、銀行帳戶或信用卡轉帳至商家帳戶。

1. **開立發票** - PayPal傳送立即付款通知訊息至Commerce後，會在Commerce中建立發票。

   請確定您的PayPal商家帳戶已啟用立即付款通知。

   >[!NOTE]
   >
   >必要時，可以針對指定數量的產品對訂單進行部份開立商業發票。 對於提交的每張部份商業發票，具有唯一ID的個別「擷取」交易會變為可用，並產生個別商業發票。

   僅授權付款交易只有在擷取全部訂單金額後才會關閉。

   您可以隨時線上作廢訂單，直到完全開立訂單金額為止。

1. **傳回**  — 如果客戶退回採購的產品並申請退款（如抓取訂單金額與建立商業發票一樣），您可以從管理員或您的PayPal商家帳戶建立線上退款。

## 設定您的PayPal帳戶

在Commerce中設定PayPal Payments Pro之前，您必須在PayPal網站上設定您的商家帳戶。

1. 登入您的 [PayPal企業帳戶](https://manager.paypal.com/).

1. 在PayPal管理員功能表中，選擇 **[!UICONTROL Service Settings]**.

1. 在 **[!UICONTROL Hosted Checkout Pages]**，按一下 **[!UICONTROL Set Up]**.

1. 在 **[!UICONTROL Choose your settings]**，設定 **[!UICONTROL Transaction Process Mode]** 至 `Live`.

1. 在 **[!UICONTROL Display options on payment page]**，設定 **[!UICONTROL Cancel URL Method]** 至 `POST`.

1. 在 **[!UICONTROL Billing Information]**，選取卡片安全碼 **[!UICONTROL CSC]** 必填欄位和可編輯欄位的核取方塊。

1. 在 **[!UICONTROL Payment Confirmation]**，設定 **[!UICONTROL Return URL Method]** 至 `POST`.

1. 在 **[!UICONTROL Security Options]**，設定下列專案：

   - **[!UICONTROL AVS]**: `No`
   - **[!UICONTROL CSC]**: `No`
   - **[!UICONTROL Enable Secure Token]**: `Yes`

1. 按一下 **[!UICONTROL Save Changes]**.

1. 在 _PayPal管理員_ 功能表，選擇 **[!UICONTROL Service Settings]** 和下 _託管的簽出頁面_，選擇 **[!UICONTROL Customize]**.

1. 選擇 **[!UICONTROL Layout C]**.

   版面C只會顯示信用卡和借記卡欄位，而且可以在您的網站上設定框架，或作為獨立的快顯視窗使用。 大小固定為490 x 565畫素，並額外留出空間以儲存錯誤訊息。 在某些系統上，此設定可更正透明重新導向的問題。

1. 按一下 **[!UICONTROL Save and Publish]**.

1. 在PayPal管理員功能表中，選擇 **[!UICONTROL Account Administration]**. 在 **[!UICONTROL Manage Security]**，按一下 **[!UICONTROL Transaction Settings]**.

1. 設定 **[!UICONTROL Allow reference transactions]** 至 `Yes`.

1. 按一下 **[!UICONTROL Confirm]**.

   >[!NOTE]
   >
   >如果您有多個Commerce網站，則必須為每個網站建立個別的PayPal Payments Pro帳戶。

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

## 在Commerce中設定PayPal Payments Pro

>[!NOTE]
>
>您可以同時啟用兩個PayPal解決方案： [PayPal Express簽出](paypal-express-checkout.md)，加上 [多合一解決方案](paypal.md#paypal-all-in-one-payment-solutions). 如果您變更付款解決方案，先前使用的解決方案會自動停用。

>[!TIP]
>
>按一下 **[!UICONTROL Save Config]** 隨時儲存進度。

### 步驟1：開始設定

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Sales]** 並選擇 **[!UICONTROL Payment Methods]**.

1. 如果您的Commerce安裝有多個網站、商店或檢視，設定 **[!UICONTROL Store View]** 到您要套用此設定的存放區檢視。

1. 在 _[!UICONTROL Merchant Location]_區段，選取&#x200B;**[!UICONTROL Merchant Country]**您的企業所在位置。

   此設定會決定要選取顯示在設定中的PayPal解決方案。

   ![商戶國家](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. 展開 **[!UICONTROL PayPal All-in-One Payment Solution]** 並按一下 **[!UICONTROL Configure]** 的 **[!UICONTROL Payments Pro]**.

   ![PayPal Payments Pro](./assets/paypal-payments-pro.png){width="600" zoomable="yes"}

### 步驟2：完成必要的PayPal設定

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Payments Pro and Express Checkout]** 區段。

   ![PayPal Payments Pro必要設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-pro-required.png){width="600" zoomable="yes"}

1. （選擇性）輸入 **[!UICONTROL Email Associated with your PayPal Merchant Account]**.

   >[!IMPORTANT]
   >
   >電子郵件地址區分大小寫。 若要接收付款，電子郵件地址必須與您PayPal商家帳戶中指定的電子郵件地址相符。

   如果您沒有PayPal帳戶，請按一下 **[!UICONTROL Start accepting payments via PayPal]**.

1. 輸入下列其中一個憑證，您可用來登入PayPal商家帳戶：

   - **[!UICONTROL Partner]**  — 您的PayPal合作夥伴ID。
   - **[!UICONTROL Vendor]**  — 您的PayPal使用者登入名稱
   - **[!UICONTROL User]**  — 在您的PayPal帳戶中設定的其他使用者ID。

1. 輸入 **[!UICONTROL Password]** 和您的PayPal帳戶相關聯的專案。

1. 若要執行測試交易，請設定 **[!UICONTROL Test Mode]** 至 `Yes`.

   在沙箱中測試設定時，僅使用 [信用卡號碼][2] 由PayPal建議。 當您準備好要前往生產環境時，請返回設定並將測試模式設定為 `No`.

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
   - **[!UICONTROL Checkout Payment Step]**
   - **[!UICONTROL Catalog Category Page]**

### 步驟4：完成基本設定

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Basic Settings - PayPal Payments Pro]** 區段。

   ![PayPal Payment Pro基本設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-pro-basic-settings.png){width="600" zoomable="yes"}

1. 的 **[!UICONTROL Title]**，輸入在結帳時識別PayPal Payments Pro的標題。

   建議您使用標題 _借記卡或信用卡_.

1. 如果您提供多種付款方式，請輸入數字 **[!UICONTROL Sort Order]** 以決定結帳時與其他付款方式一起列出PayPal Payments Pro時出現的順序。

   此數字與其他付款方式相關。 (`0` =第一個， `1` =秒， `2` =第三個，依此類推。)

1. 設定 **[!UICONTROL Payment Action]** 變更為下列其中一項：

   - `Authorization`  — 核准購買，但保留資金。 金額必須等到提取後才會提取 _已擷取_ 由商家提供。
   - `Sale`  — 採購金額已獲授權，並立即從客戶帳戶中提取。

1. 的 **[!UICONTROL Credit Card Settings]**，選取您接受在商店付款的信用卡。

   若要選取多個卡片，請按住Ctrl鍵(PC)或Command鍵(Mac)，然後按一下每個卡片。

   >[!NOTE]
   >
   >American Express需要額外的合約。

### 步驟5：完成進階設定

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Advanced Settings]** 區段。

   ![PayPal Payments Pro進階設定](./assets/paypal-payments-pro-advanced-settings.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Payment Applicable From]** 變更為下列其中一項：

   - `All Allowed Countries`  — 來自所有客戶的客戶 [國家/地區](../getting-started/store-details.md#country-options) 在商店設定中指定的可使用此付款方式。
   - `Specific Countries`  — 選擇此選項後， _[!UICONTROL Payment from Specific Countries]_清單隨即顯示。 按住Ctrl鍵(PC)或Command鍵(Mac)，並在清單中選取客戶可在您的商店購買產品的國家/地區。

1. 若要將與付款系統的通訊寫入記錄檔，請設定 **[!UICONTROL Debug Mode]** 至 `Yes`.

   >[!NOTE]
   >
   >根據PCI資料安全性標準，記錄檔中不會記錄信用卡資訊。

1. 若要啟用主機驗證功能，請設定 **[!UICONTROL Enable SSL Verification]** 至 `Yes`.

1. 若要要求客戶輸入CVV代碼，請設定 **[!UICONTROL Require CVV Entry]** 至 `Yes`.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL CVV and AVS Settings]** 區段。

1. 若要在「位址驗證系統」識別不符時決定何時應拒絕交易，請指定如何處理下列各情形：

   - 若要根據不符合的街道不符來拒絕交易，請設定 **[!UICONTROL AVS Street Does Not Match]** 至 `Yes`.

   - 若要根據不相符的郵遞區號拒絕交易，請設定 **[!UICONTROL AVS Zip Does Not Match]** 至 `Yes`.

   - 若要根據不相符的國家識別碼拒絕交易，請設定 **[!UICONTROL International AVS Indicator Does Not Match]** 至 `Yes`.

   - 若要根據不相符的CVV代碼拒絕交易，請設定 **[!UICONTROL International Card Security Code Does Not Match]** 至 `Yes`.

   ![PayPal Payments Pro必要設定 — CVV和AVS](./assets/paypal-payments-pro-cvv-avs-settings.png){width="600" zoomable="yes"}

1. 視您的商店需求，完成下列章節：

   - [結算報表設定](#settlement-report-settings)
   - [前端體驗設定](#frontend-experience-settings)

#### 結算報表設定

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Settlement Report Settings]** 區段。

   ![PayPal結算報表設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

1. 的 **[!UICONTROL SFTP Credentials]**，請執行下列動作：

   - 如果您已註冊PayPal的安全FTP伺服器，請輸入下列SFTP登入認證：

      - 登入
      - 密碼

   - 若要在網站上使用Payments Pro前執行測試報告，請設定 **[!UICONTROL Sandbox Mode]** 至 `Yes`.

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

1. 若要自訂PayPal商家頁面的外觀，請執行下列動作：

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

   - `All Allowed Countries`  — 來自所有客戶的客戶 [國家/地區](../getting-started/store-details.md#country-options) 在商店設定中指定的可使用此付款方式。
   - `Specific Countries`  — 選擇此選項後， _[!UICONTROL Payment from Specific Countries]_清單隨即顯示。 若要選取多個國家/地區，請按住Ctrl鍵(PC)或Command鍵(Mac)，然後按一下每個專案。

1. 若要將與付款系統的通訊寫入記錄檔，請設定 **[!UICONTROL Debug Mode]** 至 `Yes`.

   >[!NOTE]
   >
   >根據PCI資料安全性標準，記錄檔中不會記錄信用卡資訊。

1. 若要啟用主機驗證功能，請設定 **[!UICONTROL Enable SSL Verification]** 至 `Yes`.

1. 若要從PayPal網站依明細專案顯示客戶訂單的完整摘要，請設定 **[!UICONTROL Transfer Cart Line Items]** 至 `Yes`.

1. 若要允許客戶從PayPal網站完成交易，而不返回您的商店進行訂單審查，請設定 **[!UICONTROL Skip Order Review Step]** 至 `Yes`.

1. 完成後，按一下 **[!UICONTROL Save Config]**.

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[3]: https://developer.paypal.com/docs/paypal-payments-pro/
