---
title: PayPal Payflow連結
description: 瞭解如何將PayPal Payflow Link設定為商店上的線上付款解決方案。
exl-id: dba4057e-1fea-4a23-8594-cc85f619d664
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '2172'
ht-degree: 0%

---

# PayPal Payflow連結

PayPal Payflow Link僅適用於美國和加拿大的商家。 客戶不需擁有個人PayPal帳戶，並可在PayPal託管的表單中輸入其信用卡資訊。 這些資訊絕不會儲存在您的Adobe Commerce或Magento Open Source伺服器上。 「付款流程連結」無法用於從「管理員」建立的訂單。

線上及離線退款均支援銷退折讓單。 但是，不支援多個線上退款。

>[!IMPORTANT]
>
>**PSD2需求：** <br/>
>自2019年9月14日起，歐洲銀行可能會拒絕不符合規定的付款 [PSD2](../getting-started/compliance-payment-services-directive.md) 需求。 為了遵循PSD2，PayPal Payflow Link必須與Cardinal Commerce整合。 若要深入瞭解，請參閱 [Payflow的3-D安全](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-overview/).

## 需求

- [PayPal企業帳戶][1] PayPal Payflow Pro閘道將PayPal的商家帳戶與商家網站連結，同時充當閘道與商家帳戶。

- 如果您管理多個Commerce網站，每個網站都必須有個別的PayPal商家帳戶。

## 客戶工作流程

1. **客戶前往結帳**  — 結帳時，客戶選擇使用PayPal Payflow連結付款，並輸入信用卡資訊。 客戶不需要擁有個人PayPal帳戶。
1. **客戶選擇「立即付款」**  — 客戶點選「立即付款」按鈕以提交訂單。
1. **客戶輸入信用卡資訊**  — 客戶在PayPal託管的表單上輸入信用卡資訊。 如果客戶按一下 _取消付款_ 連結，客戶會回到結帳的「付款資訊」階段，而訂單狀態會變更為 _已取消_.
1. **客戶提交訂單**  — 信用卡資訊會直接提交給PayPal，不會保留在商務網站的任何位置。

## 訂單工作流程

1. **PayPal接收要求** - PayPal會收到客戶要求立即付款的請求。
1. **PayPal會驗證付款資訊** - PayPal會驗證信用卡資訊，並指派適當的狀態：
   - **付款已驗證：** 若已驗證， _未決付款_ 狀態最初會指定給訂單，直到交易結算為止。
   - **處理中**  — 交易成功。
   - **未決付款**  — 系統未收到PayPal的回應。
   - **已取消**  — 交易由於某些原因未成功。
   - **疑似詐騙**  — 交易未傳遞某些 [PayPal詐騙篩選器](paypal.md#paypal-fraud-management-filters). 系統會收到PayPal的回應，告知交易正由Fraud Service稽核。
   - **取消付款：** 如果客戶按一下 _取消付款_ 連結，客戶會回到結帳的「付款資訊」階段，而訂單狀態會變更為 _已取消_.
1. **客戶已重新導向至確認頁面**   — 如果交易成功完成，系統會將客戶重新導向至您商店的訂單確認頁面。 如果交易因任何原因而失敗，則結帳頁面上會顯示一則錯誤訊息，並指示客戶重複結帳程式。 這些情況由PayPal管理。
1. **商家履行訂單**  — 商戶如常開立商業發票並送出訂單。

## 設定您的PayPal帳戶

1. 登入您的 [PayPal企業帳戶][2].

1. 設定 [託管的簽出頁面][4] 搭配使用PayPal Manager及下列設定：

   - 在 **[!UICONTROL Security Options]**，完成下列設定：

     **[!UICONTROL AVS]**: `No`

     **[!UICONTROL CSC]**: `No`

     **[!UICONTROL Enable Secure Token]**: `Yes`

   - 選擇 **[!UICONTROL Customize]**，然後選擇 **[!UICONTROL Layout C]**.

     版面C只會顯示信用卡和借記卡欄位，而且可以在您的網站上設定框架，或作為獨立的快顯視窗使用。 大小固定為490 x 565畫素，並額外留出空間以儲存錯誤訊息。 在某些系統上，此設定可更正透明重新導向的問題。

1. 組態設定完成後，按一下 **[!UICONTROL Save and Publish]**.

1. 設定額外的使用者（PayPal建議）：

   - 在主功能表的第二列，按一下 **[!UICONTROL Manage Users]**.

   - 若要將其他使用者新增至帳戶，請按一下 **[!UICONTROL Add User]**.

   - 填妥以下章節的必要欄位 _新增使用者_ 表單：

      - [!UICONTROL Admin Confirmation]
      - [!UICONTROL User Information]
      - [!UICONTROL User Login Information]
      - [!UICONTROL Assign Privilege to User]

   - 按一下 **[!UICONTROL Update]**.

## 設定PayPal Payflow連結

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

1. 展開 **[!UICONTROL PayPal Payment Gateways]** （如有需要），然後按一下 **[!UICONTROL Configure]** 的 **[!UICONTROL Payflow Link]**.

   ![Payflow連結 — 設定](./assets/payflow-link.png){width="600" zoomable="yes"}

### 步驟2：完成必要的PayPal設定

![必要的PayPal設定 — PayPal Payflow連結](./assets/payflow-required-link.png){width="600" zoomable="yes"}

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

1. 如果您的系統使用Proxy伺服器來建立與PayPal系統的連線，請設定 **[!UICONTROL Test Mode]** 至 `Yes` 並執行下列動作：

   - 輸入IP位址 **[!UICONTROL Proxy Host]**.

   - 輸入連線埠號碼 **[!UICONTROL Proxy Port]**.

     當伺服器防火牆阻止直接存取PayPal伺服器時，就會使用Proxy。 在這種情況下，會使用協力廠商伺服器來轉送流量。

1. 設定 **[!UICONTROL Enable Payflow Link]** 至 `Yes`.

1. 如果您要啟用 [PayPal Express簽出](paypal-express-checkout.md) 客戶選項，設定 **[!UICONTROL Enable Express Checkout]** 至 `Yes`.

1. 如果您想要提供 [PayPal點數](paypal.md#paypal-credit-and-pay-later) 對您的客戶，設定 **[!UICONTROL Enable PayPal Credit]** 至 `Yes`.

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

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 其餘段落並重複前面的步驟來設定首頁：

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

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Basic Settings - PayPal Payflow Link]** 區段。

   ![基本設定 — PayPal Payflow連結](../configuration-reference/sales/assets/payment-methods-paypal-payflow-link-basic-settings.png){width="600" zoomable="yes"}

1. 的 **[!UICONTROL Title]**，輸入在結帳時識別PayPal Payflow Link的標題。

   建議您使用標題 _借記卡或信用卡_.

1. 如果您提供多種付款方式，請輸入數字 **[!UICONTROL Sort Order]** 決定與其他付款方式一起列出時，「付款流程連結」出現的順序。

   此數字與其他付款方式相關。 (`0` =第一個， `1` =秒， `2` =第三個，依此類推。)

1. 設定 **[!UICONTROL Payment Action]** 變更為下列其中一項：

   - `Authorization`  — 核准購買並保留資金。 此金額必須等到商戶擷取後才會提取。
   - `Sale`  — 採購金額已獲授權，並立即從客戶帳戶中提取。

### 步驟5：完成進階設定

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Advanced Settings]** 區段。

   ![進階設定 — PayPal Payflow連結](../configuration-reference/sales/assets/payment-methods-paypal-payflow-link-advanced-settings.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Payment Applicable From]** 變更為下列其中一項：

   - `All Allowed Countries`  — 來自所有客戶的客戶 [國家/地區](../getting-started/store-details.md#country-options) 在商店設定中指定的可使用此付款方式。
   - `Specific Countries`  — 選擇此選項後， _[!UICONTROL Payment from Specific Countries]_清單隨即顯示。 按住Ctrl鍵，並選取清單中客戶可在您商店購買產品的國家/地區。

1. 若要將與付款系統的通訊寫入記錄檔，請設定 **[!UICONTROL Debug Mode]** 至 `Yes`.

   >[!NOTE]
   >
   >根據PCI資料安全性標準，記錄檔中不會記錄信用卡資訊。

1. 若要啟用主機驗證功能，請設定 **[!UICONTROL Enable SSL Verification]** 至 `Yes`.

1. 如果您希望客戶能夠更正信用卡背面輸入的3位數CVV安全性代碼，請設定 **[!UICONTROL CVV Entry is Editable]** 至 `Yes`.

1. 若要要求客戶輸入CVV代碼，請設定 **[!UICONTROL Require CVV Entry]** 至 `Yes`.

1. 若要傳送付款確認給客戶，請設定 **[!UICONTROL Send Email Confirmation]** 至 `Yes`.

1. 若要決定在交易期間與PayPal伺服器交換資訊的方法，請設定 **[!UICONTROL URL method for Cancel URL and Return URL]** 變更為下列其中一項：

   - `GET`  — 擷取處理作業結果的資訊（預設方法）。
   - `POST`  — 為資料處理流程提供資料區塊，例如輸入表單中的資料。

   此 _取消URL_ 和 _傳回URL_ 請參閱客戶在PayPal伺服器上完成或取消結帳程式的付款部分後，所回訪的頁面

1. 視您的商店需求，完成下列章節：

   - [結算報表設定](#settlement-report-settings)
   - [前端體驗設定](#frontend-experience-settings)

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

使用 _[!UICONTROL Frontend Experience Settings]_選擇要在您的網站上顯示的PayPal標誌，以及自訂PayPal商家頁面的外觀。

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

   ![基本設定](../configuration-reference/sales/assets/payment-methods-paypal-payflow-link-express-checkout-basic-settings.png){width="600" zoomable="yes"}

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

   ![進階設定](../configuration-reference/sales/assets/payment-methods-paypal-payflow-link-express-checkout-advanced-settings.png){width="600" zoomable="yes"}

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

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://manager.paypal.com/
[3]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[4]: https://developer.paypal.com/docs/payflow/integration-guide/configure-hosted-checkout/#configuring-hosted-pages-using-paypal-manager
