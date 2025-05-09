---
title: PayPal付款進階
description: 瞭解如何在商店上將PayPal Payments Advanced設定為線上付款解決方案。
exl-id: 018dd999-2f17-4650-8f61-624809ae76c6
feature: Payments
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hant/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"
source-git-commit: cd5b5ebec6e72ab4ba9de775bcfe8f8a89fbbb93
workflow-type: tm+mt
source-wordcount: '2161'
ht-degree: 0%

---

# PayPal付款進階

[PayPal Payments Advanced][4]是符合[PCI規範](../getting-started/compliance-pci.md)的解決方案，可讓您的客戶以扣款或信用卡付款，而不需離開您的網站。 其中包含可自訂的內嵌簽出頁面，以建立順暢且安全的簽出體驗。

即使客戶沒有PayPal帳戶，也可以透過PayPal安全付款閘道進行購買。 接受的卡片包括美國和英國的Visa、MasterCard、Switch/Maestro和Solo信用卡。 為方便起見，PayPal Express結帳功能包含在PayPal Payments Advanced中。

>[!IMPORTANT]
>
>**PSD2需求：** <br/>
>自2019年9月14日起，歐洲銀行可能會拒絕不符合[PSD2](../getting-started/compliance-payment-services-directive.md)要求的付款。 為了遵循PSD2，PayPal Payments Advanced必須與協力廠商外掛程式整合。 若要深入瞭解，請參閱[Payflow](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-mpi/)的3D安全。

>[!NOTE]
>
>PayPal Payments Advanced不能用於從商店管理員建立的訂單。

## 需求

- [PayPal企業帳戶][1]
- 如果您管理多個Adobe Commerce和Magento Open Source網站，每個網站都必須有個別的PayPal商家帳戶。

## 簽出工作流程

1. **客戶選擇付款方式** — 在結帳期間，客戶選擇以PayPal付款進階方式付款。 此時會出現「立即付款」按鈕，而非「下訂單」按鈕。

1. **立即付款** — 客戶點按/點選&#x200B;_立即付款_，並顯示PayPal代管表單。 客戶輸入卡片資訊，並驗證卡片。 如果成功，則會顯示訂單確認頁面。

   **使用PayPal付款** — 表單也包含&#x200B;_使用PayPal付款_&#x200B;按鈕，此按鈕會將客戶重新導向至PayPal網站，透過PayPal Express結帳進行付款。

1. **疑難排解** — 如果交易因任何原因而失敗，則結帳頁面上會顯示錯誤訊息，並指示客戶再試一次。 任何問題都由PayPal管理。

## 訂單處理工作流程

使用PayPal Payments Advanced處理訂單的方式與任何一般PayPal訂單相同。 系統會針對線上與離線退款，對訂單開立商業發票與出貨，以及產生銷退折讓單。 不過，使用「PayPal付款進階」支付的訂單無法取得多重線上退款。

1. **客戶下訂單** — 在結帳的最後階段，客戶點選「下訂單」按鈕。

1. **PayPal回應** - PayPal會評估要求。 如果發現有效，PayPal會處理交易。

1. **Commerce設定訂單狀態** - Commerce會收到PayPal的回應，並將訂單狀態設定為下列其中一項：

   - **正在處理** — 交易成功。
   - **未決付款** — 系統未收到PayPal的任何回應。
   - **已取消** — 交易由於某些原因未成功
   - **疑似詐騙** — 交易未通過某些[PayPal詐騙篩選器](paypal.md#paypal-fraud-management-filters)。 系統會收到PayPal的回應，告知交易正由Fraud Service稽核。

1. **商家履行訂單** — 商家發票與運送訂單。

## 設定您的PayPal帳戶

在Commerce中設定PayPal Payments Advanced之前，您必須在PayPal網站上設定帳戶。

1. 登入您的[PayPal企業帳戶][2]。

1. 前往「**[!UICONTROL Service Settings]** > **[!UICONTROL Hosted Checkout Pages]** > **[!UICONTROL Set Up Menu]**」並完成下列設定：

   - **[!UICONTROL AVS]**： `No`
   - **[!UICONTROL CSC]**： `No`
   - **[!UICONTROL Enable Secure Token]**： `Yes`

1. **[!UICONTROL Save]**&#x200B;設定。

   >[!NOTE]
   >
   >如果您有多個Commerce網站，則必須為每個網站建立個別的PayPal付款進階帳戶。

1. 當系統提示您建立版面時，請執行下列動作：

   - 按一下頁面頂端的&#x200B;**[!UICONTROL Customize]**。

   - 選擇&#x200B;**[!UICONTROL Layout C]**。

   - 按一下&#x200B;**[!UICONTROL Save and Publish]**。

1. 設定其他使用者（由PayPal建議）：

   - 登入您的[PayPal企業帳戶][2]。

   - 若要設定其他使用者，請依照指示操作。

   - **[!UICONTROL Save]**&#x200B;變更。

## 在Commerce中設定PayPal付款進階

>[!NOTE]
>
>您可以同時啟用兩個PayPal解決方案：快速結帳，以及任何多合一或付款閘道解決方案。 如果您變更付款解決方案，先前使用的解決方案會停用。

>[!TIP]
>
>隨時按一下「**[!UICONTROL Save Config]**」以儲存進度。

### 步驟1：開始設定

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Sales]**&#x200B;並選擇&#x200B;**[!UICONTROL Payment Methods]**。

1. 如果您的Commerce安裝有多個網站、商店或檢視，請將&#x200B;**[!UICONTROL Store View]**&#x200B;設定為您要套用此設定的商店檢視。

1. 在&#x200B;_[!UICONTROL Merchant Location]_&#x200B;區段中，選取您的企業所在的&#x200B;**[!UICONTROL Merchant Country]**。

   此設定會決定要選取顯示在設定中的PayPal解決方案。

   ![商家國家](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. 展開&#x200B;**[!UICONTROL PayPal All-in-One Payment Solution]**&#x200B;並按一下&#x200B;**[!UICONTROL Payments Advanced]**&#x200B;的&#x200B;**[!UICONTROL Configure]**。

   ![進階PayPal付款](./assets/paypal-payments-advanced.png){width="600" zoomable="yes"}

### 步驟2：完成必要的設定

1. 視需要展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Required PayPal Settings]**&#x200B;區段。

   ![進階必要設定 — PayPal付款進階](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-required.png){width="600" zoomable="yes"}

1. （選擇性）輸入&#x200B;**[!UICONTROL Email Associated with your PayPal Merchant Account]**。

   >[!IMPORTANT]
   >
   >電子郵件地址區分大小寫。 若要接收付款，電子郵件地址必須與您PayPal商家帳戶中指定的電子郵件地址相符。

   如果您沒有PayPal帳戶，請按一下&#x200B;**[!UICONTROL Start accepting payments via PayPal]**。

1. 輸入下列其中一個憑證，您可用來登入PayPal商家帳戶：

   - **[!UICONTROL Partner]** — 您的PayPal合作夥伴識別碼。
   - **[!UICONTROL Vendor]** — 您的PayPal使用者登入名稱。
   - **[!UICONTROL User]** — 在您的PayPal帳戶中設定的其他使用者識別碼。

1. 輸入與您的PayPal帳戶相關聯的&#x200B;**[!UICONTROL Password]**。

1. 若要執行測試交易，請將&#x200B;**[!UICONTROL Test Mode]**&#x200B;設定為`Yes`。

   在沙箱中測試設定時，只能使用PayPal建議的[信用卡號碼][3]。 當您準備好要前往生產環境時，請返回設定並將測試模式設定為`No`。

1. 如果您的系統使用Proxy伺服器來建立與PayPal系統的連線，請將&#x200B;**[!UICONTROL Use Proxy]**&#x200B;設定為`Yes`並執行下列動作：

   - 輸入&#x200B;**[!UICONTROL Proxy Host]**&#x200B;的IP位址。

   - 輸入&#x200B;**[!UICONTROL Proxy Port]**&#x200B;的連線埠號碼。

     當伺服器防火牆阻止直接存取PayPal伺服器時，就會使用Proxy。 在這種情況下，會使用協力廠商伺服器來轉送流量。

1. 將&#x200B;**[!UICONTROL Enable this Solution]**&#x200B;設為`Yes`。

1. 如果您想要提供[PayPal信用額度](paypal.md#paypal-credit-and-pay-later)給您的客戶，請將&#x200B;**[!UICONTROL Enable PayPal Credit]**&#x200B;設為`Yes`。

### 步驟3：設定廣告PayPal信用/廣告PayPal PayLater （選擇性）

從2.4.3版開始，在包含PayPal的部署中支援PayPal PayLater。 此功能可讓購物者以雙週分期付款的方式支付訂單，而不需在購買時支付全額。 已棄用PayPal點數體驗。

將&#x200B;**[!UICONTROL Enable PayPal PayLater Experience]**&#x200B;設定為下列其中一項：

- `Yes` — 若要設定PayPal PayLater廣告
- `No` — 若要設定廣告PayPal點數

#### 廣告PayPal點數

1. 展開&#x200B;**[!UICONTROL Advertise PayPal Credit]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![廣告PayPal點數](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png){width="600" zoomable="yes"}

1. 若要取得您的帳戶資訊，請按一下&#x200B;**[!UICONTROL Get Publisher ID from PayPal]**&#x200B;並依照指示進行。

1. 輸入您的&#x200B;**[!UICONTROL Publisher ID]**。

1. 展開&#x200B;**[!UICONTROL Home Page]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

1. 若要在頁面上放置橫幅，請將&#x200B;**[!UICONTROL Display]**&#x200B;設為`Yes`。

1. 將&#x200B;**[!UICONTROL Position]**&#x200B;設定為下列其中一項：

   - `Header (center)`
   - `Sidebar (right)`

1. 將&#x200B;**[!UICONTROL Size]**&#x200B;設定為下列其中一項：

   - `190 x 100`
   - `234 x 60`
   - `300 x 50`
   - `468 x 60`
   - `728 x 90`
   - `800 x 66`

   ![廣告PayPal點數首頁設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

1. 展開![展開選取器](../assets/icon-display-expand.png)其餘的區段，並重複之前的步驟：

   - **[!UICONTROL Catalog Category Page]**
   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**

#### 廣告PayPal PayLater

1. 展開&#x200B;**[!UICONTROL Advertise PayPal PayLater]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

1. 將&#x200B;**[!UICONTROL Enable PayPal PayLater]**&#x200B;設為`Yes`。

1. 展開&#x200B;**[!UICONTROL Home Page]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

1. 若要在頁面上放置橫幅，請將&#x200B;**[!UICONTROL Display]**&#x200B;設為`Yes`。

1. 將&#x200B;**[!UICONTROL Position]**&#x200B;設定為下列其中一項：

   - `Header (center)`
   - `Sidebar`

1. 將&#x200B;**[!UICONTROL Style Layout]**&#x200B;設定為下列其中一項：

   - `Text`
   - `Flex`

1. 僅針對[!UICONTROL Style Layout] **[!UICONTROL Text]**，將&#x200B;**[!UICONTROL Logo Type]**&#x200B;設定為下列其中一項：

   - `Primary`
   - `Alternative`
   - `Inline`
   - `None`

1. 僅針對[!UICONTROL Style Layout] **[!UICONTROL Text]**，將&#x200B;**[!UICONTROL Logo Position]**&#x200B;設定為下列其中一項：

   - `Left`
   - `Right`
   - `Top`

1. 僅針對[!UICONTROL Style Layout] **[!UICONTROL Text]**，將&#x200B;**[!UICONTROL Text Color]**&#x200B;設定為下列其中一項：

   - `Black`
   - `White`
   - `Monochrome`
   - `Grayscale`

1. 僅針對[!UICONTROL Style Layout] **[!UICONTROL Text]**，將&#x200B;**[!UICONTROL Text Size]**&#x200B;設定為下列其中一項：

   - `10px`
   - `11px`
   - `12px`
   - `13px`
   - `14px`
   - `15px`
   - `16px`

1. 僅針對[!UICONTROL Style Layout] **[!UICONTROL Flex]**，將&#x200B;**[!UICONTROL Ratio]**&#x200B;設定為下列其中一項：

   - `1x1`
   - `1x4`
   - `8x1`
   - `20x1`

1. 僅針對[!UICONTROL Style Layout] **[!UICONTROL Flex]**，將&#x200B;**[!UICONTROL Color]**&#x200B;設定為下列其中一項：

   - `Blue`
   - `Black`
   - `White`
   - `White No Border`
   - `Gray`
   - `Monochrome`
   - `Grayscale`

   ![廣告PayPal點數首頁設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-paylater-home-page.png){width="600" zoomable="yes"}

1. 展開![展開選取器](../assets/icon-display-expand.png)其餘的區段，並重複之前的步驟：

   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**
   - **[!UICONTROL Checkout Payment Step]**
   - **[!UICONTROL Catalog Category Page]**

### 步驟4：完成基本設定

1. 視需要展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Basic Settings - PayPal Payments Advanced]**&#x200B;區段。

   ![PayPal付款進階基本設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-basic-settings.png){width="600" zoomable="yes"}

1. 若要在結帳時識別PayPal Payments Advanced，請輸入&#x200B;**[!UICONTROL Title]**。

   建議您使用標題&#x200B;_借記卡或信用卡_。

1. 如果您提供多種付款方式，請輸入&#x200B;**[!UICONTROL Sort Order]**&#x200B;的數字，以決定結帳期間與其他付款方式一起列出時，PayPal付款進階的顯示順序。

   此數字與其他付款方式相關。 （`0` =第一個，`1` =第二個，`2` =第三個，依此類推。）

1. 將&#x200B;**[!UICONTROL Payment Action]**&#x200B;設定為下列其中一項：

   - `Authorization` — 核准購買，但保留資金。 此金額必須等到商戶擷取&#x200B;_到_&#x200B;後才會撤回。
   - `Sale` — 已授權並立即從客戶帳戶中取用購買的金額。

### 步驟5：完成進階設定

1. 展開&#x200B;**[!UICONTROL Advanced Settings]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![進階設定 — PayPal付款進階](./assets/paypal-payments-advanced2.png){width="600" zoomable="yes"}

1. 將&#x200B;**[!UICONTROL Payment Applicable From]**&#x200B;設定為下列其中一項：

   - `All Allowed Countries` — 來自您商店組態中指定的所有[國家/地區](../getting-started/store-details.md#country-options)的客戶都可以使用此付款方式。
   - `Specific Countries` — 選擇此選項後，_[!UICONTROL Payment from Specific Countries]_&#x200B;清單會出現。 按住Ctrl鍵(PC)或Command鍵(Mac)，並在清單中選取客戶可在您的商店購買產品的國家/地區。

1. 若要將與付款系統的通訊寫入記錄檔，請將&#x200B;**[!UICONTROL Debug Mode]**&#x200B;設為`Yes`。

   PayPal付款進階的記錄檔為`payments_payflow_advanced.log`。

   >[!NOTE]
   >
   >根據PCI資料安全性標準，記錄檔中不會記錄信用卡資訊。

1. 若要啟用主機認證驗證，請將&#x200B;**[!UICONTROL Enable SSL Verification]**&#x200B;設為`Yes`。

1. 若要允許客戶從信用卡背面更正其輸入的3位數CVV安全性代碼，請將&#x200B;**[!UICONTROL CVV Entry is Editable]**&#x200B;設為`Yes`。

1. 若要要求客戶輸入CVV代碼，請將&#x200B;**[!UICONTROL Require CVV Entry]**&#x200B;設為`Yes`。

1. 若要傳送付款確認給客戶，請將&#x200B;**[!UICONTROL Send Email Confirmation]**&#x200B;設為`Yes`。

1. 若要決定在交易期間與PayPal伺服器交換資訊的方法，請將&#x200B;**[!UICONTROL URL method for Cancel URL and Return URL]**&#x200B;設定為下列其中一項：

   - `GET` - （預設）擷取程式結果的資訊。
   - `POST` — 為資料處理程式提供資料區塊，例如輸入到表單中的資料。

   _取消URL_&#x200B;與&#x200B;_回訪URL_&#x200B;參考客戶在PayPal伺服器上完成或取消結帳程式的付款部分後回訪的頁面。

1. 視您的商店需求，完成下列章節：

   - [結算報表設定](#settlement-report-settings)
   - [前端體驗設定](#frontend-experience-settings)

#### 結算報表設定

1. 展開&#x200B;**[!UICONTROL Settlement Report Settings]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![PayPal結算報告設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

1. 針對&#x200B;**[!UICONTROL SFTP Credentials]**，請執行下列動作：

   - 如果您已註冊PayPal的安全FTP伺服器，請輸入下列SFTP登入認證：

      - 登入
      - 密碼

   - 若要在上線前執行測試報告，請將&#x200B;**[!UICONTROL Sandbox Mode]**&#x200B;設為`Yes`。

   - 輸入&#x200B;**[!UICONTROL Custom Endpoint Hostname or IP Address]**。

     預設值為`reports.paypal.com`。

   - 輸入儲存報告的&#x200B;**[!UICONTROL Custom Path]**。

     預設值為`/ppreports/outgoing`。

1. 若要根據排程產生報表，請完成&#x200B;**[!UICONTROL Scheduled Fetching]**&#x200B;設定：

   - 將&#x200B;**[!UICONTROL Enable Automatic Fetching]**&#x200B;設為`Yes`。

   - 將&#x200B;**[!UICONTROL Schedule]**&#x200B;設定為下列其中一項：

      - `Daily`
      - `Every 3 Days`
      - `Every 7 Days`
      - `Every 10 Days`
      - `Every 14 Days`
      - `Every 30 Days`
      - `Every 40 Days`

     PayPal會保留每個報表45天。

   - 將&#x200B;**[!UICONTROL Time of Day]**&#x200B;設為您要產生報告時的小時、分鐘和秒。

#### 前端體驗設定

使用&#x200B;_[!UICONTROL Frontend Experience Settings]_&#x200B;選擇要在您的網站上顯示的PayPal標誌，並自訂PayPal商家頁面的外觀。

1. 展開&#x200B;**[!UICONTROL Frontend Experience Settings]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![PayPal前端體驗設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings.png){width="600" zoomable="yes"}

1. 選取您要在商店的PayPal區塊中顯示的&#x200B;**[!UICONTROL PayPal Product Logo]**。

   PayPal標誌有四種樣式和兩種尺寸：

   - `No Logo`
   - `We Prefer PayPal (150 x 60 or 150 x 40)`
   - `Now Accepting PayPal (150 x 60 or 150 x 40)`
   - `Payments by PayPal (150 x 60 or 150 x 40)`
   - `Shop Now Using PayPal (150 x 60 or 150 x 40)`

1. 若要自訂PayPal商家頁面的外觀：

   - 輸入您要套用至PayPal商家頁面的&#x200B;**[!UICONTROL Page Style]**&#x200B;名稱：

      - `paypal` — 使用PayPal頁面樣式。
      - `primary` — 使用您在帳戶設定檔中識別為&#x200B;_主要_&#x200B;樣式的頁面樣式。
      - `your_custom_value` — 使用帳戶設定檔中指定的自訂付款頁面樣式。

   - 針對&#x200B;**[!UICONTROL Header Image URL]**，輸入您要顯示在付款頁面左上角的影像URL。 檔案大小上限為750畫素寬x 90畫素高。

   >[!NOTE]
   >
   >PayPal建議將影像存放在安全(https)伺服器上。 否則，瀏覽器可能會警告此頁面&#x200B;_包含安全和非安全專案_。

   - 若要設定頁面的顏色，請針對下列各項，輸入6個字元的十六進位代碼（不含`#`符號）：

      - **[!UICONTROL Header Background Color]** — 結帳頁面標頭的背景顏色。
      - **[!UICONTROL Header Border Color]** — 標頭周圍兩畫素框線的色彩。
      - **[!UICONTROL Page Background Color]** — 結帳頁面及頁首與付款表單周圍的背景顏色。

### 步驟6：完成PayPal Express結帳的基本設定

1. 展開&#x200B;**[!UICONTROL Basic Settings - PayPal Express Checkout]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![PayPal Express簽出基本設定](../configuration-reference/sales/assets/payment-methods-paypal-advanced-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. 針對&#x200B;**[!UICONTROL Title]**，輸入在結帳時識別此付款方式的標題。

   建議為每個商店檢視將標題設定為&#x200B;_PayPal_。

1. 如果您提供多種付款方式，請輸入&#x200B;**[!UICONTROL Sort Order]**&#x200B;的數字，以決定與其他付款方式列示時，PayPal Express Checkout出現的順序。

   此數字與其他付款方式相關。 （`0` =第一個，`1` =第二個，`2` =第三個，依此類推。）

1. 將&#x200B;**[!UICONTROL Payment Action]**&#x200B;設定為下列其中一項：

   - `Authorization` — 核准購買並保留資金。 此金額必須等到商戶擷取&#x200B;_到_&#x200B;後才會撤回。
   - `Sale` — 已授權並立即從客戶帳戶中取用購買的金額。

1. 若要在產品頁面上顯示&#x200B;_[!UICONTROL Check out with PayPal]_&#x200B;按鈕，請將&#x200B;**[!UICONTROL Display on Product Details Page]**&#x200B;設為`Yes`。

### 步驟7：完成進階設定 — PayPal Express簽出

1. 展開&#x200B;**[!UICONTROL Advanced Settings]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![PayPal Express簽出進階設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-express-checkout-advanced.png){width="600" zoomable="yes"}

1. 若要讓PayPal Express結帳功能可從購物車和迷你購物車使用，請將&#x200B;**[!UICONTROL Display on Shopping Cart]**&#x200B;設為`Yes`。

1. 將&#x200B;**[!UICONTROL Payment Applicable From]**&#x200B;設定為下列其中一項：

   - `All Allowed Countries` — 來自您商店組態中指定的所有[國家/地區](../getting-started/store-details.md#country-options)的客戶都可以使用此付款方式。
   - `Specific Countries` |選擇此選項後，會顯示&#x200B;_特定國家的付款清單_。 按住Ctrl鍵(PC)或Command鍵(Mac)，然後按一下清單中可供客戶在您商店購買產品的國家/地區。

1. 若要將與付款系統的通訊寫入記錄檔，請將&#x200B;**[!UICONTROL Debug Mode]**&#x200B;設為`Yes`。

   >[!NOTE]
   >
   >根據[PCI資料安全性標準](../getting-started/compliance-pci.md)，記錄檔中不會記錄信用卡資訊。

1. 若要啟用主機認證驗證，請將&#x200B;**[!UICONTROL Enable SSL Verification]**&#x200B;設為`Yes`。

1. 若要從PayPal網站依條列專案顯示客戶訂單的完整摘要，請將&#x200B;**[!UICONTROL Transfer Cart Line Items]**&#x200B;設為`Yes`。

1. 若要允許客戶從PayPal網站完成交易，而不返回您的商店進行訂單稽核，請將&#x200B;**[!UICONTROL Skip Order Review Step]**&#x200B;設為`Yes`。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://manager.paypal.com/
[3]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[4]: https://developer.paypal.com/docs/payflow/gs-ppa-hosted-pages/
