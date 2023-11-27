---
title: 『[!UICONTROL Sales] &gt； [!UICONTROL Payment Methods] &gt； [!UICONTROL PayPal Payments Advanced]『
description: 檢閱中的組態設定 [!UICONTROL PayPal Payments Advanced] 區段於 [!UICONTROL Sales] &gt； [!UICONTROL Payment Methods] 商務管理員頁面。
exl-id: c9159408-fbdf-4146-8292-9952cd5d01fa
feature: Configuration, Payments
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '1310'
ht-degree: 2%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL PayPal Payments Advanced]

>[!IMPORTANT]
>
>**PSD2需求：** <br/>
>自2019年9月14日起，歐洲銀行可能會拒絕不符合規定的付款 [PSD2](../../getting-started/compliance-payment-services-directive.md) 需求。 為了遵循PSD2， [!DNL PayPal Payments Advanced] 必須與 [!DNL Cardinal Commerce]. 若要深入瞭解，請參閱 [Payflow的3-D安全](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-overview/).

{{config}}

## [!UICONTROL Required Settings]

![必要設定](./assets/payment-methods-paypal-payments-advanced-required.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Email Associated with PayPal Merchant Account] | 網站 | （選用）與您的PayPal商家帳戶相關聯的任何電子郵件地址。 電子郵件地址區分大小寫，且必須與您帳戶中的地址完全相符。 |
| [!UICONTROL Partner] | 網站 | 您的PayPal合作夥伴ID （如適用）。 |
| [!UICONTROL Vendor] | 網站 | 您的PayPal使用者登入名稱 |
| 使用者 | 網站 | 您PayPal帳戶上其他使用者的ID。 |
| [!UICONTROL Password] | 網站 | 與您的PayPal商家帳戶關聯的密碼。 |
| [!UICONTROL Test Mode] | 網站 | 啟用後，會在測試環境中執行PayPal Payments Advanced。 當您準備好要在生產模式下「上線」時，請關閉測試模式。 選項： `Yes` / `No` |
| [!UICONTROL Use Proxy] | 網站 | 當伺服器防火牆阻止直接存取PayPal伺服器時，可以使用Proxy來重新導向流量。 如果適用，會識別用來與PayPal伺服器建立連線的Proxy伺服器。 選項： `Yes` / `No` <br/><br/>如果已啟用，請設定選項： <br/>**`Proxy Host`**— 代理主機的IP位址。<br/>**`Proxy Port`**  — 代理主機連線埠的號碼。 |
| [!UICONTROL Enable this Solution] | 網站 | 決定客戶是否可以使用「PayPal付款進階管理系統」作為付款方式。 |
| [!UICONTROL Enable PayPal Credit] | 網站 | 決定您的客戶是否可將PayPal信用作為付款選項。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Advertise PayPal Credit]

![廣告PayPal點數](./assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Publisher ID] | 網站 | 與您的PayPal信用帳戶相關聯的發行者ID。 |
| [!UICONTROL Get Publisher ID from PayPal] |  | 從PayPal擷取您的發行者ID。 |
| [!UICONTROL Home Page] | 網站 | 決定位置與大小 [!DNL PayPal Credit] 首頁上的橫幅。 選項： <br/>**`Display`**— 決定要否[!DNL PayPal Credit] 橫幅會顯示在商店的首頁上。 選項： `Yes` / `No`<br/>**`Position`**  — 決定 [!DNL PayPal Credit] 首頁上的橫幅。 選項：頁首（中央） /側欄（右側） <br/>**`Size`**— 決定 [!DNL PayPal Credit] 首頁上的橫幅。 選項： `190 x 100` / `234 x 60` / `300 x 50` / `468 x 60` / `728 x 90` /` 800 x 66` |
| [!UICONTROL Catalog Category Page] | 網站 | 決定位置與大小 [!DNL PayPal Credit] 類別頁面上的橫幅。 選項： (與相同 [!UICONTROL Home Page]) |
| [!UICONTROL Catalog Product Page] | 網站 | 決定位置與大小 [!DNL PayPal Credit] 產品頁面上的橫幅。 選項： (與相同 [!UICONTROL Home Page]) |
| [!UICONTROL Checkout Cart Page] | 網站 | 決定位置與大小 [!DNL PayPal Credit] 購物車頁面上的橫幅。 選項： (與相同 [!UICONTROL Home Page]) |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Basic Settings]

![基本設定](./assets/payment-methods-paypal-payments-advanced-basic-settings.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Title] | 存放區檢視 | 在結帳時，將「PayPal付款進階管理系統」識別為付款方式的名稱。 |
| [!UICONTROL Sort Order] | 存放區檢視 | 一個數字，當在結帳期間與其他付款方式一起列出時，決定「PayPal付款進階」出現的順序。 |
| [!UICONTROL Payment Action] | 網站 | 決定PayPal在提交訂單時所採取的動作。 選項： <br/>**`Authorization`**— 核准購買，但保留資金。 此金額必須等到商家「擷取」後才會提取。<br/>**`Sale`**  — 採購金額已獲授權，並立即從客戶帳戶中提取。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Advanced Settings]

![進階設定](./assets/paypal-advanced-settings2.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Payment Applicable From] | 網站 | 決定適用的國家/地區選取範圍。 選項： `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Countries Payment Applicable From] | 網站 | 識別接受付款的每個國家/地區。 只有帳單地址在選定國家/地區的客戶才能使用此付款方式進行購買。 |
| [!UICONTROL Debug Mode] | 網站 | 將商店和支付系統之間傳送的訊息記錄到記錄檔中。 選項： `Yes` / `No` <br/><br/>**_注意：_**記錄檔儲存在伺服器上，只有開發人員才能存取。 根據PCI資料安全性標準，記錄檔中不會記錄信用卡資訊。 |
| [!UICONTROL Enable SSL Verification] | 網站 | 決定是否在交易發生之前驗證主機上的安全通道。 選項： `Yes` / `No` |
| [!UICONTROL CVV Entry is Editable] | 網站 | 決定輸入後，客戶是否可以編輯CVV。 選項： `Yes` / `No` |
| [!UICONTROL Require CVV Entry] | 網站 | 決定是否要求客戶從信用卡背面輸入CVV代碼。 選項： `Yes` / `No` |
| [!UICONTROL Send Email Confirmation] | 網站 | 決定客戶是否收到付款的電子郵件確認。 選項： `Yes` / `No` |
| [!UICONTROL URL Method for Cancel URL and Return URL] | 網站 | 決定在交易期間與PayPal伺服器交換資訊的方法。 選項： <br/>**`GET`**— 擷取程式結果的資訊。 （這是預設方法。）<br/>**`POST`**  — 將資料區塊（例如輸入表單中的資料）傳送至資料處理流程。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Settlement Report Settings]

![結算報表設定](./assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| **[!UICONTROL SFTP Credentials]** |  |  |
| [!UICONTROL Login] | 網站 | 您登入PayPal安全FTP伺服器所需的使用者名稱。 |
| [!UICONTROL Password] | 網站 | 您登入PayPal安全FTP伺服器所需的密碼。 |
| [!UICONTROL Sandbox Mode] | 網站 | 啟用後，會在生產環境中「上線」之前，先在測試環境中執行報表。 選項： `Yes` / `No` |
| [!UICONTROL Custom Endpoint Hostname or IP-Address] | 網站 | 管理結算報表的URL。 預設值： `reports.paypal.com` |
| [!UICONTROL Custom Path] | 網站 | 結算報表儲存在伺服器上的路徑。 預設值： `/ppreports/outgoing` |
| **[!UICONTROL Scheduled Fetching]** |  |  |
| [!UICONTROL Enable Automatic Fetching] | 網站 | 啟用時，會依排程自動擷取結算報表。 選項： `Yes` / `No` |
| [!UICONTROL Schedule] | 全域 | 決定PayPal產生結算報表的頻率。 選項： `Daily` / `Every 3 days` / `Every 7 days` / `Every 10 days` / `Every 14 days` / `Every 30 days` / `Every 40 days` |
| [!UICONTROL Time of Day] | 全域 | 決定產生結算報表的小時、分鐘和秒。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Frontend Experience Settings]

![前端體驗設定](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL PayPal Product Logo] | 存放區檢視 | 決定出現在您商店中的PayPal標誌。 有兩種大小的4種基本樣式。 選項： `No Logo` / `We prefer PayPal (150 x 60)` / `We prefer PayPal (150 x 40)` / `Now accepting PayPal (150 x 60)` / `Now accepting PayPal (150 x 40)` / `Payments by PayPal (150 x 60)` / `Payments by PayPal (150 x 40)` / `Shop now using (150 x 60)` / `Shop now using (150 x 40)` |
| **[!UICONTROL PayPal Merchant Pages Style]** |  |  |
| [!UICONTROL Page Style] | 存放區檢視 | 決定您的PayPal商家頁面外觀。 允許的值： <br/>**`paypal`**— 使用PayPal頁面樣式。<br/>**`primary`**  — 使用您在帳戶設定檔中識別為「主要」樣式的頁面樣式。 <br/>**`your_custom_value`**— 使用帳戶設定檔中指定的自訂付款頁面樣式。 |
| [!UICONTROL Header Image URL] | 存放區檢視 | 顯示在結帳頁面左上角的影像URL。 大小上限為750 x 90畫素。 <br/><br/>**_注意：_**PayPal建議將影像儲存在安全(https)伺服器上。 否則，客戶的瀏覽器可能會警告「頁面包含安全及不安全的專案」。 |
| [!UICONTROL Header Image Background Color] | 存放區檢視 | 六個字元 [十六進位色彩](https://en.wikipedia.org/wiki/Web_colors) 結帳頁面上頁首的背景顏色代碼。 您可以用大寫和小寫字元輸入代碼。 |
| [!UICONTROL Header Image Border Color] | 存放區檢視 | 標頭周圍兩畫素邊框的六字元十六進位色彩代碼。 |
| [!UICONTROL Page Background Color] | 存放區檢視 | 結帳頁面背景顏色的六字元十六進位顏色代碼，會顯示在頁首與付款表單後面。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Basic Settings - PayPal Express Checkout]

![PayPal Express簽出基本設定](./assets/payment-methods-paypal-advanced-express-checkout-basic-settings.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Title] | 存放區檢視 | 在結帳時識別PayPal Express結帳付款方法的名稱。 |
| [!UICONTROL Sort Order] | 存放區檢視 | 一個數字，當在結帳期間與其他付款方式一起列出時，會決定PayPal Express結帳的順序。 輸入 `0` ，位於清單頂端。 |
| [!UICONTROL Payment Action] | 網站 | 決定PayPal收到訂單時所採取的動作。 選項： <br/>**`Authorization`**— 核准購買，但保留資金。 此金額必須等到商家「擷取」後才會提取。<br/>**`Sale`**  — 採購金額已獲授權，並立即從客戶帳戶中提取。 <br/>**`Order`**— 代表與PayPal的合約，可讓商家在定義的時段內，從客戶的買方帳戶擷取一或多項金額，最多可達到訂購總額。 最多可達29天。 必須從Commerce管理員產生一或多張商業發票，才能擷取資金。 |
| [!UICONTROL URL Display on Product Details Page] | 存放區檢視 | 決定「使用PayPal結帳」按鈕是否出現在產品頁面上。 選項： `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL PayPal Express Checkout - Advanced Settings]

![PayPal Express簽出進階設定](./assets/payment-methods-paypal-payments-advanced-express-checkout-advanced.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Display on Shopping Cart] | 存放區檢視 | 決定PayPal Express結帳是否顯示為購物車中的付款選項。 選項： `Yes` （建議） / `No` |
| [!UICONTROL Payment Action Applicable From] | 網站 | 決定適用的國家/地區選取範圍。 選項： `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Countries Payment Applicable From] | 網站 | 識別接受付款的每個國家/地區。 只有帳單地址在選定國家/地區的客戶才能使用此付款方式進行購買。 |
| [!UICONTROL Debug Mode] | 網站 | 將商店與PayPal支付系統之間傳送的訊息記錄到記錄檔中。 選項： `Yes` / `No` <br/><br/>**_注意：_**記錄檔儲存在伺服器上，只有開發人員才能存取。 根據PCI資料安全性標準，記錄檔中不會記錄信用卡資訊。 |
| [!UICONTROL Enable SSL Verification] | 網站 | 啟用主機安全性憑證的驗證。 選項： `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | 網站 | 顯示PayPal網站上客戶購物車的條列專案完整摘要。 選項： `Yes` / `No` |
| [!UICONTROL Skip Order Review Step] | 網站 | 決定客戶是否可以從PayPal網站完成交易，或是必須返回您的商店並在提交訂單前完成「訂單複查」步驟。 選項： `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}
