---
title: PayPal Express簽出
description: 瞭解如何將PayPal Express Checkout設定為商店上的線上付款解決方案。
exl-id: 0cd90306-cf47-4a5f-8994-6ae96904ae2f
feature: Payments
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hant/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"
source-git-commit: cd5b5ebec6e72ab4ba9de775bcfe8f8a89fbbb93
workflow-type: tm+mt
source-wordcount: '3110'
ht-degree: 0%

---

# PayPal Express簽出

PayPal Express Checkout讓您的客戶能夠透過信用卡或透過其個人PayPal帳戶的安全性付款，有助於提高銷售額。 結帳時，系統會將客戶重新導向安全的PayPal網站，以完成付款資訊。 然後，客戶會回到您的商店，以完成剩餘的結帳程式。 選擇「快速結帳」會將您熟悉的PayPal按鈕新增至商店，據報會增加銷售額。

>[!IMPORTANT]
>
>**PSD2需求：** <br/>
>自2019年9月14日起，歐洲銀行可能會拒絕不符合[PSD2](../getting-started/compliance-payment-services-directive.md)要求的付款。 PayPal Express Checkout不需要採取任何動作即可符合PSD2，因為所有要求都由PayPal處理。

目前擁有PayPal帳戶的客戶可以按一下&#x200B;_[!UICONTROL Check out with PayPal]_&#x200B;按鈕，在單一步驟中完成購買。 Express Checkout可作為獨立使用，或搭配其中一個PayPal多合一解決方案使用。 如果您已線上上接受信用卡，您可以提供「快速結帳」作為額外選項，以吸引偏好使用PayPal付款的新客戶。

>[!NOTE]
>
>PayPal已停止支援透過PayPal Express Checkout銷售數位商品，建議您使用[PayPal Payments Standard](paypal-payments-standard.md)或其他PayPal付款閘道來處理任何包含[虛擬產品](../catalog/product-create-virtual.md)的訂單。

## 需求

- 商家： [企業PayPal帳戶][1]
- 客戶： [個人PayPal帳戶][2]

## 快速簽出工作流程

與其他付款方式不同，PayPal Express結帳可讓客戶在一般結帳工作流程的開頭從產品頁面、迷你購物車和購物車結帳。

1. **客戶下訂單** — 客戶按一下/點選&#x200B;_[!UICONTROL Check out with PayPal]_&#x200B;按鈕。
1. **客戶被重新導向至PayPal網站** — 客戶被重新導向至PayPal網站以完成交易。
1. **客戶登入其PayPal帳戶** — 客戶必須登入其PayPal帳戶才能完成交易。 付款系統使用來自其PayPal帳戶的帳單和送貨資訊。
1. **客戶回到結帳頁面** — 客戶被重新導向回到您商店中的結帳頁面以檢閱訂單。
1. **客戶下訂單** — 客戶下訂單，並將訂單資訊提交給PayPal。
1. **PayPal結算交易** - PayPal會收到訂單並結算交易。

>[!NOTE]
>
>PayPal Express Checkout不支援具有多個地址的訂單。

## 內文中籤出

PayPal的&#x200B;_In-Context Checkout_&#x200B;讓線上付款變得前所未有的簡單。 透過簡化的一鍵或兩鍵順暢結帳，客戶永遠不會忘記您的商店。 內容結帳功能在Mac和PC上同樣運作良好，且在桌上型電腦、平板電腦和行動裝置上提供一致的體驗。 若要深入瞭解，請參閱[In-Context Checkout in Express簽出][5]。

![PayPal in-context簽出示範](./assets/storefront-paypal-in-context.png){width="700" zoomable="yes"}

[_PayPal in-context簽出示範_][6]

當您設定[!DNL PayPal Express Checkout]的存放區時，可以啟用此選項。

## 設定您的PayPal帳戶

在「Commerce管理員」中設定PayPal Express Checkout之前，您必須先在PayPal網站上設定商家帳戶。

1. 在[manager.paypal.com][3]登入您的PayPal進階帳戶。

1. 前往「**[!UICONTROL Service Settings]** > **[!UICONTROL Hosted Checkout Pages]** > **[!UICONTROL Set Up]**」並進行下列設定：

   - **[!UICONTROL AVS]**： `No`
   - **[!UICONTROL CSC]**： `No`
   - **[!UICONTROL Enable Secure Token]**： `Yes`

1. 按一下&#x200B;**[!UICONTROL Save Changes]**。

1. 設定其他使用者（由PayPal建議）：

   - 前往[manager.paypal.com][3]並登入您的帳戶。

   - 若要設定其他使用者，請依照指示操作。

   - 按一下&#x200B;**[!UICONTROL Update]**。

## 在Commerce中設定PayPal Express簽出

您可以同時啟用兩個PayPal解決方案：PayPal Express Checkout，以及多合一解決方案。 如果您啟用不同的解決方案，先前使用的解決方案會自動停用。

>[!NOTE]
>
>隨時按一下「**[!UICONTROL Save Config]**」以儲存進度。

### 步驟1：開始設定

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Sales]**&#x200B;並選擇&#x200B;**[!UICONTROL Payment Methods]**。

1. 如果您的安裝有多個網站、商店或檢視，請將&#x200B;**[!UICONTROL Store View]**&#x200B;設定為您要套用此設定的商店檢視。

1. 在&#x200B;_[!UICONTROL Merchant Location]_&#x200B;區段中，選取您的企業所在的&#x200B;**[!UICONTROL Merchant Country]**。

   此設定會決定要選取顯示在設定中的PayPal解決方案。

   ![商家國家](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. 在&#x200B;_[!UICONTROL Recommended Solutions]_&#x200B;底下，按一下&#x200B;**[!UICONTROL PayPal Express Checkout]**&#x200B;的&#x200B;**[!UICONTROL Configure]**。

   ![設定PayPal Express簽出](./assets/paypal-express-checkout.png){width="600"}

### 步驟2：啟用並連線您的PayPal帳戶

1. 如有需要，請展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Required PayPal Settings]**&#x200B;區段。

   ![連線您的PayPal帳戶](./assets/paypal-express-required.png){width="600" zoomable="yes"}

1. 連線您的帳戶以進行測試或生產：

   - 若要測試（開發）模式，請按一下&#x200B;**[!UICONTROL Sandbox Credentials]**&#x200B;並輸入您的[PayPal沙箱][7]認證。
   - 在生產模式中，按一下&#x200B;**[!UICONTROL Connect with PayPal]**&#x200B;並輸入您的生產帳戶認證。

   當您的連線通過驗證時，您可以繼續。

1. 將&#x200B;**[!UICONTROL Enable this Solution]**&#x200B;設為`Yes`。

1. 若要啟用[PayPal In-Context簽出](#in-context-checkout)：

   - 將&#x200B;**[!UICONTROL Enable In-Context Checkout Experience]**&#x200B;設為`Yes`。

   - 輸入您的PayPal **[!UICONTROL Merchant Account ID]**。

     您的商家帳戶ID位於您的PayPal企業帳戶個人資料中。

>[!NOTE]
>
>此付款選項預設啟用[PayPal信用額度](paypal.md#paypal-credit-and-pay-later)。

### 步驟3：完成必要的PayPal設定

1. 如有需要，請展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Express Checkout]**&#x200B;區段。

   ![PayPal Express簽出必要的設定](./assets/paypal-express-settings.png){width="600" zoomable="yes"}

1. （選擇性）輸入&#x200B;**[!UICONTROL Email Associated with PayPal Merchant Account]**。

   >[!IMPORTANT]
   >
   >電子郵件地址區分大小寫。 若要接收付款，您輸入的電子郵件地址必須符合您在PayPal商家帳戶中指定的電子郵件地址。

   如果您沒有PayPal帳戶，請按一下&#x200B;**[!UICONTROL Start accepting payments via PayPal]**。

1. 將&#x200B;**[!UICONTROL API Authentication Methods]**&#x200B;設定為下列其中一項：

   - `API Signature` — 此PayPal驗證方法最容易實作，而且是以您的使用者名稱、密碼以及識別您帳戶的唯一字元與數字字串為基礎。 API簽章認證不會過期。
   - `API Certificate` — 此PayPal驗證方法較安全，是以您的使用者名稱、密碼和可下載的憑證為基礎。 API憑證會在三年後到期，且必須續約。

   如有需要，請完成下列作業：

   - **[!UICONTROL API Username]**
   - **[!UICONTROL API Password]**
   - **[!UICONTROL API Signature]**

1. 如果您使用來自沙箱帳戶的認證，請將&#x200B;**[!UICONTROL Sandbox Mode]**&#x200B;設為`Yes`。

   在沙箱中測試設定時，只能使用PayPal建議的[信用卡號碼][4]。 當您準備好要前往生產時，請返回設定並將沙箱模式設定為`No`並連線到您的生產PayPal帳戶。

1. 如果您的系統使用Proxy伺服器來建立Commerce與PayPal付款系統之間的連線，請將&#x200B;**[!UICONTROL API Uses Proxy]**&#x200B;設為`Yes`並完成下列作業：

   - **[!UICONTROL Proxy Host]**
   - **[!UICONTROL Proxy Port]**

在此步驟順序的結尾，已完成必要的PayPal設定。 您可以繼續使用基本和進階設定，或按一下「**[!UICONTROL Save Config]**」稍後再返回以調整設定

### 步驟4：設定廣告PayPal Credit /廣告PayPal PayLater （選擇性）

從2.4.3版開始，在包含PayPal的部署中支援PayPal PayLater。 此功能可讓購物者以雙週分期付款的方式支付訂單，而不需在購買時支付全額。 已棄用PayPal點數體驗。

將&#x200B;**[!UICONTROL Enable PayPal PayLater Experience]**&#x200B;設定為下列其中一項：

- `Yes` — 若要設定PayPal PayLater廣告
- `No` — 若要設定廣告PayPal點數

>[!NOTE]
>
>**[!UICONTROL Enable PayPal PayLater Experience]**&#x200B;設定不會停用[!DNL PayPal PayLater]功能，也不會從店面移除&#x200B;**_[!UICONTROL PayPal PayLater]_**&#x200B;按鈕。 若要停用店面上的&#x200B;**_[!UICONTROL PayPal PayLater]_**&#x200B;和&#x200B;**_[!UICONTROL PayPal Credit]_**&#x200B;按鈕，您必須選取&#x200B;**[!UICONTROL Disable Funding Options]**&#x200B;設定的`PayPal Credit`值（[!UICONTROL Frontend Experience Settings]下的[!UICONTROL Advanced Settings]）。

#### 廣告PayPal點數

1. 展開&#x200B;**[!UICONTROL Advertise PayPal Credit]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

1. 若要取得您的帳戶資訊，請按一下&#x200B;**[!UICONTROL Get Publisher ID from PayPal]**&#x200B;並依照指示進行。

1. 輸入您的&#x200B;**[!UICONTROL Publisher ID]**。

   ![廣告PayPal點數](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png){width="600" zoomable="yes"}

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

   - [!UICONTROL Catalog Category Page]
   - [!UICONTROL Catalog Product Page]
   - [!UICONTROL Checkout Cart Page]

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

   - [!UICONTROL Catalog Product Page]
   - [!UICONTROL Checkout Cart Page]
   - [!UICONTROL Checkout Payment Step]
   - [!UICONTROL Catalog Category Page]

### 步驟5：完成基本設定

1. 展開&#x200B;**[!UICONTROL Basic Settings - PayPal Express Checkout]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![基本設定](../configuration-reference/sales/assets/payment-methods-paypal-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. 針對&#x200B;**[!UICONTROL Title]**，輸入在結帳時識別此付款方式的標題。

   建議您將標題&#x200B;_PayPal_&#x200B;用於所有商店檢視。

1. 如果您提供多種付款方式，請輸入&#x200B;**[!UICONTROL Sort Order]**&#x200B;的數字，以決定與其他付款方式列示時，PayPal Express Checkout出現的順序。

   此數字與其他付款方式相關。 （`0` =第一個，`1` =第二個，`2` =第三個，依此類推。）

1. 將&#x200B;**[!UICONTROL Payment Action]**&#x200B;設定為下列其中一項：

   - `Authorization` — 核准購買並保留資金。 此金額必須等到商戶擷取&#x200B;_到_&#x200B;後才會撤回。
   - `Sale` — 已授權並立即從客戶帳戶中取用購買的金額。
   - `Order` - PayPal的客戶餘額、銀行帳戶或信用卡未擷取或授權訂單金額。 「訂單」付款動作代表PayPal付款系統與商家之間的協定。 它可讓商家在長達29天的期間內，從客戶採購員帳戶抓取一或多項最高至訂購總金額的金額。 在訂購資金後，商家可以在接下來的29天期間內隨時抓取資金。 擷取訂單金額只能透過建立一張或多張商業發票從Commerce管理員完成。

1. 若要在產品頁面上顯示&#x200B;_[!UICONTROL Check out with PayPal]_&#x200B;按鈕，請將&#x200B;**[!UICONTROL Display on Product Details Page]**&#x200B;設為`Yes`。

1. 如果付款動作設為`Order`，請完成下列作業

   - **[!UICONTROL Authorization Honor Period (days)]** — 決定主要授權保持有效的時間。 該值應等於您PayPal商家帳戶中的對應值。 您的PayPal商家帳戶中的預設值為`3`。 若要增加此數目，您必須聯絡PayPal。 授權在美國太平洋時間最後一天的晚上11點49分失效。

   - **[!UICONTROL Order Valid Period (days)]** — 決定訂單的有效時間。 訂單無效時，您將無法再為其建立商業發票。 指定等於您PayPal商家帳戶中「訂單有效期間」值的值。 您的PayPal商家帳戶中的預設值為`29`。 若要變更此號碼，您必須連絡PayPal。

   - **[!UICONTROL Number of Child Authorizations]** — 指定單一訂單的最大授權數目，此數目決定您可以為訂單建立的線上部份商業發票數目上限。 此值應等於您PayPal商家帳戶中的對應設定。 您的PayPal帳戶預設的子授權數量為`1`。 若要增加此數目，您必須聯絡PayPal。

### 步驟6：完成進階設定

1. 展開&#x200B;**[!UICONTROL Advanced Settings]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![進階設定 — PayPal Express簽出](../configuration-reference/sales/assets/payment-methods-paypal-express-checkout-advanced-settings.png){width="600" zoomable="yes"}

1. 將&#x200B;**[!UICONTROL Display on Shopping Cart]**&#x200B;設為`Yes`。

1. 將&#x200B;**[!UICONTROL Payment Applicable From]**&#x200B;設定為下列其中一項：

   - `All Allowed Countries` — 來自您商店組態中所指定之所有國家/地區的客戶可以使用此付款方式。
   - `Specific Countries` — 選擇此選項後，_[!UICONTROL Payment from Specific Countries]_&#x200B;清單會出現。 若要選取多個國家/地區，請按住Ctrl鍵(PC)或Command鍵(Mac)，然後按一下每個專案。

1. 若要將與付款系統的通訊寫入記錄檔，請將&#x200B;**[!UICONTROL Debug Mode]**&#x200B;設為`Yes`。

   PayPal付款進階的記錄檔為`_payflow_advanced.log`。

   >[!NOTE]
   >
   >根據PCI資料安全性標準，記錄檔中不會記錄信用卡資訊。

1. 若要啟用主機認證驗證，請將&#x200B;**[!UICONTROL Enable SSL Verification]**&#x200B;設為`Yes`。

1. 若要顯示PayPal網站中明細專案的客戶訂單完整摘要，請將&#x200B;**[!UICONTROL Transfer Cart Line Items]**&#x200B;設為`Yes`。

1. 若要在摘要中包含最多十個送貨選項，請將&#x200B;**[!UICONTROL Transfer Shipping Options]**&#x200B;設為`Yes`。 （只有行專案設為移轉時，才會顯示此選項。）

1. 若要判斷用於PayPal接受按鈕的影像型別，請將&#x200B;**[!UICONTROL Shortcut Buttons Flavor]**&#x200B;設定為下列其中一項：

   - `Dynamic` - （建議）顯示可從PayPal伺服器動態變更的影像。
   - `Static` — 顯示無法動態變更的特定影像。

1. 若要允許沒有PayPal帳戶的客戶使用此方法購物，請將&#x200B;**[!UICONTROL Enable PayPal Guest Checkout]**&#x200B;設為`Yes`。

1. 將&#x200B;**[!UICONTROL Require Customer's Billing Address]**&#x200B;設定為下列其中一項：

   - `Yes` — 所有購買都需要客戶的帳單地址。
   - `No` — 購買時不需要客戶的帳單地址。
   - `For Virtual Quotes Only` — 僅需虛擬報價單的客戶帳單地址。

   >[!NOTE]
   >
   >必須透過PayPal技術支援為商家帳戶啟用此功能。

1. （選擇性）設定&#x200B;**[!UICONTROL Billing Agreement Signup]**&#x200B;以允許客戶在客戶帳戶中沒有可用的有效帳單協定時，與您在PayPal付款系統中的商店簽署[帳單協定](paypal-billing-agreements.md)：

   - `Auto` — 客戶可在快速結帳流程中簽署帳單合約，或使用其他付款方式。
   - `Ask Customer` — 客戶可在快速結帳流程中決定是否簽署帳單合約。
   - `Never` — 客戶無法在快速結帳流程中簽署帳單合約。

   >[!NOTE]
   >
   >商家必須要求[PayPal商家技術支援](https://developer.paypal.com/support/)在其帳戶中啟用帳單合約。 _帳單合約註冊_&#x200B;引數僅在PayPal確認您的商家帳戶已啟用帳單合約之後啟用。

1. 若要允許客戶從PayPal網站完成交易，而不返回您的商店進行訂單稽核，請將&#x200B;**[!UICONTROL Skip Order Review Step]**&#x200B;設為`Yes`。

1. 視需要為商店完成其他章節：

   - [PayPall帳單協定設定](#paypal-billing-agreement-settings)
   - [結算報表設定](#settlement-report-settings)
   - [前端體驗設定](#frontend-experience-settings)
   - [自訂智慧按鈕](#customize-smart-buttons)
   - [功能](#features)

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

#### PayPal帳單協定設定

[帳單合約](paypal-billing-agreements.md)是商家與客戶之間的銷售合約，已獲得PayPal授權可搭配多份訂單使用。 在結帳程式中，「帳單協定」付款選項只會針對已與貴公司簽訂帳單協定的客戶顯示。 在PayPal授權合約之後，付款系統就會發出唯一的參考ID，以識別與合約相關聯的每張訂單。 與採購單類似，客戶可與貴公司設定的帳單協定數並無限制。

1. 展開&#x200B;**[!UICONTROL PayPal Billing Agreement Settings]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![帳單協定設定](../configuration-reference/sales/assets/payment-methods-paypal-express-checkout-billing-agreement-settings.png){width="600" zoomable="yes"}

1. 將&#x200B;**[!UICONTROL Enabled]**&#x200B;設為`Yes`。

1. 針對&#x200B;**[!UICONTROL Title]**，輸入在結帳時識別PayPal帳單合約方式的標題。

1. 如果您提供多種付款方式，請在&#x200B;**[!UICONTROL Sort Order]**&#x200B;欄位中輸入數字，以決定結帳期間與其他付款方式一起列出時，「帳單協定」出現的順序。

1. 將&#x200B;**[!UICONTROL Payment Action]**&#x200B;設定為下列其中一項：

   - `Authorization` — 核准購買並保留資金。 此金額必須等到商家「擷取」後才會提取。
   - `Sale` — 已授權並立即從客戶帳戶中取用購買的金額。

1. 將&#x200B;**[!UICONTROL Payment Applicable From]**&#x200B;設定為下列其中一項：

   - `All Allowed Countries` — 來自您商店組態中所指定之所有國家/地區的客戶可以使用此付款方式。
   - `Specific Countries` — 選擇此選項後，_[!UICONTROL Payment from Specific Countries]_&#x200B;清單會出現。 若要選取多個國家/地區，請按住Ctrl鍵(PC)或Command鍵(Mac)並按一下每個國家/地區。

1. 若要在記錄檔中記錄與付款系統的通訊，請將&#x200B;**[!UICONTROL Debug Mode]**&#x200B;設為`Yes`。

   >[!NOTE]
   >
   >記錄檔儲存在伺服器上，只有開發人員才能存取。 根據PCI資料安全性標準，記錄檔中不會記錄信用卡資訊。

1. 若要啟用SSL驗證，請將&#x200B;**[!UICONTROL Enable SSL Verification]**&#x200B;設為`Yes`。

1. 若要在您的PayPal付款頁面上顯示客戶訂單中每個明細專案的摘要，請將&#x200B;**[!UICONTROL Transfer Cart Line Items]**&#x200B;設為`Yes`。

1. 若要允許客戶從其客戶帳戶的儀表板啟動帳單協定，請將&#x200B;**[!UICONTROL Allow in Billing Agreement Wizard]**&#x200B;設為`Yes`。

#### 結算報表設定

1. 展開&#x200B;**[!UICONTROL Settlement Report Settings]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![結算報告設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

1. 針對&#x200B;**[!UICONTROL SFTP Credentials]**，請執行下列動作：

   - 如果您已註冊PayPal安全FTP伺服器，請輸入下列SFTP登入認證：

      - 登入
      - 密碼

   - 若要在您的網站上以Express Checkout在&#x200B;_上線_&#x200B;之前執行測試報告，請將&#x200B;**[!UICONTROL Sandbox Mode]**&#x200B;設為`Yes`。

   - 輸入&#x200B;**[!UICONTROL Custom Endpoint Hostname or IP Address]**。

     預設值為： `reports.paypal.com`

   - 輸入儲存報告的&#x200B;**[!UICONTROL Custom Path]**。

     預設值為： `/ppreports/outgoing`

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

使用「前端體驗設定」來選擇要在您的網站上顯示的PayPal標誌，以及自訂PayPal商家頁面的外觀。

1. 展開&#x200B;**[!UICONTROL Frontend Experience Settings]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![前端體驗設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png){width="600" zoomable="yes"}

1. 選取您要在商店的PayPal區塊中顯示的&#x200B;**[!UICONTROL PayPal Product Logo]**。

   PayPal標誌有四種樣式和兩種尺寸：

   - `No Logo`
   - `We Prefer PayPal (150 x 60 or 150 x 40)`
   - `Now Accepting PayPal (150 x 60 or 150 x 40)`
   - `Payments by PayPal (150 x 60 or 150 x 40)`
   - `Shop Now Using PayPal (150 x 60 or 150 x 40)`

1. 若要自訂PayPal商家頁面的外觀，請執行下列動作：

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

#### 自訂智慧按鈕

_智慧型付款按鈕_&#x200B;功能可讓您自訂PayPal按鈕，該按鈕可顯示在「結帳」、「產品詳細資料」、「購物車」和「迷你購物車」頁面上。 PayPal的內部研究顯示，預設選項具有高度認知度，可能導致購買率提高，但其預設值可能與您的商店風格不符。 您可以選擇：

- PayPal按鈕的大小、顏色和形狀
- 顯示在PayPal按鈕上的文字
- 顯示多個按鈕時的版面（水平或垂直）

若要自訂按鈕，請展開![展開選取器](../assets/icon-display-expand.png)下列每個區段，並調整設定：

- **[!UICONTROL Checkout Page]**
- **[!UICONTROL Product Pages]**
- **[!UICONTROL Cart Page]**
- **[!UICONTROL Mini Cart]**

![簽出頁面設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings2.png){width="600" zoomable="yes"}

**_若要設定每個頁面型別的按鈕顯示：_**

1. 展開![展開選取器](../assets/icon-display-expand.png)區段。

1. 將&#x200B;**[!UICONTROL Customize Button]**&#x200B;設為`Yes`。

1. 若要設定PayPal在「智慧型付款」按鈕上顯示的文字，請將&#x200B;**[!UICONTROL Label]**&#x200B;設定為下列其中一項：

   - `Checkout` - PayPal簽出
   - `Pay` - PayPal簽出
   - `Buy Now` — 使用PayPal立即購買
   - `PayPal` - PayPal
   - `Installment` - PayPal
   - `Credit` - PayPal點數

1. 將&#x200B;**[!UICONTROL Layout]**&#x200B;設定為下列其中一項：

   - `Vertical` - （預設）垂直顯示PayPal智慧型按鈕。 無論是否選取&#x200B;**[!UICONTROL Enable Guest Checkout]**，購買者都必須登入PayPal或建立PayPal帳戶。
   - `Horizontal` — 水準顯示PayPal智慧型按鈕。 選取&#x200B;**[!UICONTROL Enable Guest Checkout]**&#x200B;時，**[!UICONTROL Pay with Debit Card or Credit Card]**&#x200B;按鈕會顯示在PayPal快顯視窗中。 否則，購買者必須登入PayPal或建立PayPal帳戶。

1. 將&#x200B;**[!UICONTROL Size]**&#x200B;設定為下列其中一項：

   - `Medium` - 250 x 35畫素。
   - `Large` - 350 x 40畫素。
   - `Responsive` - （預設）調整為容器的寬度。 最小寬度是100畫素，最大寬度是500畫素。 高度會根據寬度動態調整。

1. 將&#x200B;**[!UICONTROL Shape]**&#x200B;設定為下列其中一項：

   - `Pill` - （預設）按鈕的形狀像藥丸（中央較長，端部彎曲）。
   - `Rectangle` — 矩形中的方形形狀，不含曲線。

1. 將&#x200B;**[!UICONTROL Color]**&#x200B;設定為下列其中一項：

   - `Gold` （預設）
   - `Blue`
   - `Silver`
   - `Black`

#### 功能

功能設定可讓您停用與此PayPal解決方案相關的特定功能。

1. 展開&#x200B;**[!UICONTROL Features]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![簽出頁面設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings3.png){width="600" zoomable="yes"}

1. 設定&#x200B;**[!UICONTROL Disable Funding Options]**&#x200B;以決定在&#x200B;_結帳_&#x200B;頁面上顯示哪些其他PayPal資金選項。

   選取的選項不會顯示在&#x200B;_簽出_&#x200B;頁面上。 未選取的選項僅在PayPal支援商店幣別與購買者地點時才會顯示。 選項包括：

   - PayPal點數
   - Venmo
   - PayPal來賓結帳信用卡圖示
   - Elektronisches Lastschriftverfahren — 德文ELV

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://www.paypal.com/webapps/mpp/buying-online
[3]: https://manager.paypal.com/
[4]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[5]: https://www.paypal.com/rs/webapps/mpp/express-checkout
[6]: https://demo.paypal.com/us/demo/navigation?merchant=bigbox&page=incontextProductCheckout
[7]: https://developer.paypal.com/docs/api-basics/sandbox/
