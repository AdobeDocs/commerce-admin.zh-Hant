---
title: '[!UICONTROL Sales] &amp；gt； [!UICONTROL Payment Methods] &amp；gt； [!UICONTROL PayPal Payments Standard]'
description: 檢閱Commerce管理員[!UICONTROL Sales] &amp；gt； [!UICONTROL Payment Methods]頁面上[!UICONTROL PayPal Payments Standard]區段中的組態設定。
exl-id: 846d9b6f-92b9-4610-b894-625f67f4cff8
feature: Configuration, Payments
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '1291'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL PayPal Payments Standard]

>[!IMPORTANT]
>
>**PSD2需求：**<br/>
>自2019年9月14日起，歐洲銀行可能會拒絕不符合[PSD2](../../getting-started/compliance-payment-services-directive.md)要求的付款。 [!DNL PayPal Payments Standard]不需要任何動作即可符合PSD2，因為所有要求都由PayPal處理。

{{config}}

## [!UICONTROL Required Settings]

![必要的設定](./assets/payment-methods-paypal-payments-standard-required.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Email Associated with PayPal Merchant Account] | 網站 | （選用）與您的PayPal商家帳戶相關聯的任何電子郵件地址。 電子郵件地址區分大小寫，且必須與您帳戶中的地址完全相符。 |
| [!UICONTROL Partner] | 網站 | 您的PayPal合作夥伴ID （如適用）。 |
| [!UICONTROL Vendor] | 網站 | 您的PayPal使用者登入名稱 |
| 使用者 | 網站 | 您PayPal帳戶上其他使用者的ID。 |
| [!UICONTROL Password] | 網站 | 與您的PayPal商家帳戶關聯的密碼。 |
| [!UICONTROL Test Mode] | 網站 | 啟用後，會在測試環境中執行PayPal Payments Pro。 當您準備好要在生產模式下「上線」時，請關閉測試模式。 選項： `Yes` / `No` |
| [!UICONTROL Use Proxy] | 網站 | 當伺服器防火牆阻止直接存取PayPal伺服器時，可以使用Proxy來重新導向流量。 如果適用，會識別用來與PayPal伺服器建立連線的Proxy伺服器。 選項： `Yes` / `No` <br/><br/>如果已啟用，請設定選項： <br/>**`Proxy Host`**- Proxy主機的IP位址。<br/>**`Proxy Port`** - Proxy連線埠的數目。 |
| [!UICONTROL Enable this Solution] | 網站 | 決定PayPal Payments Pro是否可作為付款方式提供給您的客戶。 |
| [!UICONTROL Enable PayPal Credit] | 網站 | 決定您的客戶是否可將PayPal信用作為付款選項。 |

{style="table-layout:auto"}

## 廣告PayPal點數

![廣告PayPal點數](./assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Publisher ID] | 網站 | 與您的PayPal信用帳戶相關聯的發行者ID。 |
| [!UICONTROL Get Publisher ID from PayPal] |  | 從PayPal擷取您的發行者ID。 |
| [!UICONTROL Home Page] | 網站 | 決定首頁上[!DNL PayPal Credit]橫幅的位置和大小。 選項： <br/>**`Display`**— 決定您的商店首頁上是否顯示[!DNL PayPal Credit]橫幅。 選項： `Yes` / `No`<br/>**`Position`** — 決定首頁上[!DNL PayPal Credit]橫幅的位置。 選項： `Header (center)` / `Sidebar (right)` <br/>**`Size`**— 決定首頁上[!DNL PayPal Credit]橫幅的大小。 選項： `190 x 100` / `234 x 60` / `300 x 50` / `468 x 60` / `728 x 90` /` 800 x 66` |
| [!UICONTROL Catalog Category Page] | 網站 | 決定類別頁面上[!DNL PayPal Credit]橫幅的位置和大小。 選項： （與[!UICONTROL Home Page]相同） |
| [!UICONTROL Catalog Product Page] | 網站 | 決定產品頁面上[!DNL PayPal Credit]橫幅的位置和大小。 選項： （與[!UICONTROL Home Page]相同） |
| [!UICONTROL Checkout Cart Page] | 網站 | 決定購物車頁面上[!DNL PayPal Credit]橫幅的位置和大小。 選項： （與[!UICONTROL Home Page]相同） |

{style="table-layout:auto"}

## [!UICONTROL Basic Settings - PayPal Payments Standard]

![基本設定](./assets/paypal-standard-basic-settings.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Title] | 存放區檢視 | 在結帳時將PayPal Payments Pro識別為付款方法的名稱。 |
| [!UICONTROL Sort Order] | 存放區檢視 | 一個數字，可決定PayPal Payments Pro在結帳期間與其他付款方式一起列出時的顯示順序。 |
| [!UICONTROL Payment Action] | 網站 | 決定PayPal在提交訂單時所採取的動作。 選項： <br/>**`Authorization`**— 核准購買，但保留資金。 此金額必須等到商家「擷取」後才會提取。<br/>**`Sale`** — 已授權並立即從客戶帳戶中取用購買的金額。 |
| [!UICONTROL Credit Card Settings] |  |  |
| [!UICONTROL Allowed Credit Cart Types] | 網站 | 決定客戶在結帳時可使用的信用卡。 選取每個支援的卡片。 選項： `American Express` （需要額外的合約） / `Visa` / `MasterCard` / `Discover` / `JCB` |

{style="table-layout:auto"}

## [!UICONTROL Advanced Settings]

![進階設定](./assets/payment-methods-paypal-payment-standard-advanced.png)<!-- zoom -->

| 欄位 | 範圍 | 說明 |
|--- |--- |--- |
| [!UICONTROL Display on Shopping Cart] | 存放區檢視 | 決定PayPal Express結帳是否顯示為購物車中的付款選項。 選項： `Yes` （建議） / `No` |
| [!UICONTROL Payment Action Applicable From] | 網站 | 決定適用的國家/地區選取範圍。 選項： `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Countries Payment Applicable From] | 網站 | 識別接受付款的每個國家/地區。 只有帳單地址在選定國家/地區的客戶才能使用此付款方式進行購買。 |
| [!UICONTROL Debug Mode] | 網站 | 將商店與PayPal支付系統之間傳送的訊息記錄到記錄檔中。 選項： `Yes` / `No` <br/><br/>**_注意：_**&#x200B;記錄檔儲存在伺服器上，只有開發人員才能存取。 根據PCI資料安全性標準，記錄檔中不會記錄信用卡資訊。 |
| [!UICONTROL Enable SSL Verification] | 網站 | 啟用主機安全性憑證的驗證。 選項： `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | 網站 | 顯示PayPal網站上客戶購物車的條列專案完整摘要。 選項： `Yes` / `No` |
| [!UICONTROL Transfer Shipping Options] | 網站 | 包括PayPal網站上最多十個送貨選項。 選項： `Yes` / `No` |
| [!UICONTROL Shortcut Buttons Flavor] | 存放區檢視 | 決定用於PayPal接受按鈕的影像型別。 選項： <br/>**`Dynamic`**- （建議）顯示可從PayPal伺服器動態變更的影像。<br/>**`Static`** — 顯示無法動態變更的靜態影像。 |
| [!UICONTROL Enable PayPal Guest Checkout] | 網站 | 允許沒有PayPal帳戶的客戶透過PayPal Express結帳進行購買。 選項： `Yes` / `No` |
| [!UICONTROL Require Customer's Billing Address] | 網站 | 決定是否需要客戶帳單地址。 選項： `Yes` / `No` / `For Virtual Quotes Only` |
| [!UICONTROL Billing Agreement Signup] | 網站 | 決定客戶是否能與您的商店簽訂[帳單合約](../../stores-purchase/paypal-billing-agreements.md)。 選項： <br/>**`Auto`**— 客戶可以在快速結帳期間註冊帳單合約。<br/>**`Ask Customer`** — 詢問客戶是否要註冊帳單合約。 <br/>**`Never`**— 不提供客戶註冊付費合約的選項。 |
| [!UICONTROL Skip Order Review Step] | 網站 | 決定客戶是否可以從PayPal網站完成交易，或是必須返回您的商店並在提交訂單前完成「訂單複查」步驟。 選項： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Billing Agreement Setting]

![帳單協定設定](./assets/payment-methods-paypal-express-checkout-billing-agreement-settings.png)<!-- zoom -->

| 欄位 | 範圍 | 說明 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 網站 | 啟用後，帳單協定在結帳期間會對客戶顯示為付款選項。 選項： `Yes` / `No` |
| [!UICONTROL Title] | 存放區檢視 | PayPal帳單合約選項的標籤，會在結帳時顯示為付款選項。 |
| [!UICONTROL Sort Order] | 存放區檢視 | 決定結帳時帳單協定與其他付款方式一起列出的順序。 |
| [!UICONTROL Payment Action] | 網站 | 決定PayPal管理交易的方式：選項： <br/>**`Authorization`**— 核准購買，但保留資金。 此金額必須等到商家「擷取」後才會提取。<br/>**`Sale`** — 已授權並立即從客戶帳戶中取用購買的金額。 |
| [!UICONTROL Payment Applicable From] | 網站 | 決定適用的國家/地區選取範圍。 選項： `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Countries Payment Applicable From] | 網站 | 識別接受付款的每個國家/地區。 只有帳單地址在選定國家/地區的客戶才能使用此付款方式進行購買。 |
| [!UICONTROL Debug Mode] | 網站 | 在記錄檔中記錄與付款系統的通訊。 選項： `Yes` / `No` <br/><br/>**_注意：_**&#x200B;記錄檔儲存在伺服器上，只有開發人員才能存取。 根據PCI資料安全性標準，記錄檔中不會記錄信用卡資訊。 |
| [!UICONTROL Enable SSL Verification] | 網站 | 啟用驗證步驟，以確保透過加密的SSL通道進行交易。 選項： `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | 網站 | 啟用後，會在您的PayPal付款頁面上顯示購物車的明細專案摘要。 選項： `Yes` / `No` |
| [!UICONTROL Allow in Billing Agreement Wizard] | 網站 | 啟用後，客戶可以從其客戶帳戶的儀表板啟動帳單協定。 |

{style="table-layout:auto"}

## [!UICONTROL Settlement Report Settings]

![結算報告設定](./assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Login] | 網站 | 您登入PayPal安全FTP伺服器所需的使用者名稱。 |
| [!UICONTROL Password] | 網站 | 您登入PayPal安全FTP伺服器所需的密碼。 |
| [!UICONTROL Sandbox Mode] | 網站 | 啟用後，會在生產環境中「上線」之前，先在測試環境中執行報表。 選項： `Yes` / `No` |
| [!UICONTROL Custom Endpoint Hostname or IP-Address] | 網站 | 管理結算報表的URL。 預設值： `reports.paypal.com` |
| [!UICONTROL Custom Path] | 網站 | 結算報表儲存在伺服器上的路徑。 預設值： `/ppreports/outgoing` |
| [!UICONTROL Scheduled Fetching] |  |  |
| [!UICONTROL Enable Automatic Fetching] | 網站 | 啟用時，會依排程自動擷取結算報表。 選項： `Yes` / `No` |
| [!UICONTROL Schedule] | 全域 | 決定PayPal產生結算報表的頻率。 選項： `Daily` / `Every 3 days` / `Every 7 days` / `Every 10 days` / `Every 14 days` / `Every 30 days` / `Every 40 days` |
| [!UICONTROL Time of Day] | 全域 | 決定產生結算報表的小時、分鐘和秒。 |

{style="table-layout:auto"}

## [!UICONTROL Frontend Experience Settings]

![前端體驗設定](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL PayPal Product Logo] | 存放區檢視 | 決定出現在您商店中的PayPal標誌。 有兩種大小的4種基本樣式。 選項： `No Logo` / `We prefer PayPal (150 x 60)` / `We prefer PayPal (150 x 40)` / `Now accepting PayPal (150 x 60)` / `Now accepting PayPal (150 x 40)` / `Payments by PayPal (150 x 60)` / `Payments by PayPal (150 x 40)` / `Shop now using (150 x 60)` / `Shop now using (150 x 40)` |
| [!UICONTROL PayPal Merchant Pages Style] |  |  |
| [!UICONTROL Page Style] | 存放區檢視 | 決定您的PayPal商家頁面外觀。 允許的值： <br/>**`paypal`**— 使用PayPal頁面樣式。<br/>**`primary`** — 使用您在帳戶設定檔中識別為「主要」樣式的頁面樣式。 <br/>**`your_custom_value`**— 使用帳戶設定檔中指定的自訂付款頁面樣式。 |
| [!UICONTROL Header Image URL] | 存放區檢視 | 顯示在結帳頁面左上角的影像URL。 大小上限為750 x 90畫素。 <br/><br/>**_注意：_**&#x200B;PayPal建議將影像儲存在安全(https)伺服器上。 否則，客戶的瀏覽器可能會警告「頁面包含安全及不安全的專案」。 |
| [!UICONTROL Header Image Background Color] | 存放區檢視 | 結帳頁面上頁首的背景顏色的六字元[十六進位色彩](https://en.wikipedia.org/wiki/Web_colors)代碼。 您可以用大寫和小寫字元輸入代碼。 |
| [!UICONTROL Header Image Border Color] | 存放區檢視 | 標頭周圍兩畫素邊框的六字元十六進位色彩代碼。 |
| [!UICONTROL Page Background Color] | 存放區檢視 | 結帳頁面背景顏色的六字元十六進位顏色代碼，會顯示在頁首與付款表單後面。 |

{style="table-layout:auto"}
