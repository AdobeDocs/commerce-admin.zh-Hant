---
title: 『[!UICONTROL Sales] &gt； [!UICONTROL Payment Methods] &gt；  [!UICONTROL PayPal Payflow Pro]『
description: 檢閱中的組態設定 [!UICONTROL PayPal Payflow Pro] 區段於 [!UICONTROL Sales] &gt； [!UICONTROL Payment Methods] 商務管理員頁面。
exl-id: 2aae038b-15c0-452a-98bc-4d97efbb60f6
feature: Configuration, Payments
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '650'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] >  [!UICONTROL PayPal Payflow Pro]

>[!IMPORTANT]
>
>**PSD2需求：** <br/>
>自2019年9月14日起，歐洲銀行可能會拒絕不符合規定的付款 [PSD2](../../getting-started/compliance-payment-services-directive.md) 需求。 為了遵循PSD2， [!DNL PayPal Payflow Pro] 必須與 [!DNL Cardinal Commerce]. 若要深入瞭解，請參閱 [Payflow的3-D安全](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-overview/).

{{config}}

## [!UICONTROL Required Settings]

![必要設定](./assets/paypal-payflow-pro-settings.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Email Associated with PayPal Merchant Account] | 網站 | （選用）與您的PayPal商家帳戶相關聯的任何電子郵件地址。 電子郵件地址區分大小寫，且必須與您帳戶中的地址完全相符。 |
| [!UICONTROL Partner] | 網站 | 您的PayPal合作夥伴ID （如適用）。 |
| [!UICONTROL Vendor] | 網站 | 您的PayPal使用者登入名稱 |
| 使用者 | 網站 | 您PayPal帳戶上其他使用者的ID。 |
| [!UICONTROL Password] | 網站 | 與您的PayPal商家帳戶關聯的密碼。 |
| [!UICONTROL Test Mode] | 網站 | 啟用後，會在測試環境中執行PayPal Payflow Pro。 當您準備好要在生產模式下「上線」時，請關閉測試模式。 選項： `Yes` / `No` |
| [!UICONTROL Use Proxy] | 網站 | 當伺服器防火牆阻止直接存取PayPal伺服器時，可以使用Proxy來重新導向流量。 如果適用，會識別用來與PayPal伺服器建立連線的Proxy伺服器。 選項： `Yes` / `No` <br/><br/>如果已啟用，請設定Proxy選項： <br/>**`Proxy Host`**— 代理主機的IP位址。<br/>**`Proxy Port`**  — 代理主機連線埠的號碼。 |
| [!UICONTROL Enable this Solution] | 網站 | 決定PayPal Payflow Pro是否可作為付款方式提供給您的客戶。 |
| [!UICONTROL Enable PayPal Credit] | 網站 | 決定您的客戶是否可將PayPal信用作為付款選項。 |

{style="table-layout:auto"}

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

{style="table-layout:auto"}

## [!UICONTROL Basic Settings - PayPal Payflow Pro]

![基本設定](./assets/payment-methods-paypal-payflow-pro-basic-settings.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Title] | 存放區檢視 | 在結帳時將PayPal Payflow Pro識別為付款方法的名稱。 |
| [!UICONTROL Sort Order] | 存放區檢視 | 一個數字，用來決定結帳期間與其他付款方式一起列出時，PayPal Payflow Pro出現的順序。 |
| [!UICONTROL Payment Action] | 網站 | 決定PayPal在提交訂單時所採取的動作。 選項： <br/>**`Authorization`**— 核准購買，但保留資金。 此金額必須等到商家「擷取」後才會提取。<br/>**`Sale`**  — 採購金額已獲授權，並立即從客戶帳戶中提取。 |
| **[!UICONTROL Credit Card Settings]** |  |  |
| [!UICONTROL Allowed Credit Cart Types] | 網站 | 決定客戶在結帳時可使用的信用卡。 選取每個支援的卡片。 選項： `American Express` （需要額外的合約） / `Visa` / `MasterCard` / `Discover` / `JCB` |

{style="table-layout:auto"}

## [!UICONTROL Advanced Settings]

![進階設定](./assets/payment-methods-paypal-payflow-pro-advanced-settings.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| 在購物車上顯示 | 存放區檢視 | 決定PayPal Express結帳是否顯示為購物車中的付款選項。 選項：是（建議） /否 |
| [!UICONTROL Payment Action Applicable From] | 網站 | 決定適用的國家/地區選取範圍。 選項：所有允許的國家/地區/特定國家 |
| [!UICONTROL Countries Payment Applicable From] | 網站 | 識別接受付款的每個國家/地區。 只有帳單地址在選定國家/地區的客戶才能使用此付款方式進行購買。 |
| [!UICONTROL Debug Mode] | 網站 | 將商店與PayPal支付系統之間傳送的訊息記錄到記錄檔中。 選項： `Yes` / `No` <br/><br/>**_注意：_**記錄檔儲存在伺服器上，只有開發人員才能存取。 根據PCI資料安全性標準，記錄檔中不會記錄信用卡資訊。 |
| [!UICONTROL Enable SSL Verification] | 網站 | 啟用主機安全性憑證的驗證。 選項： `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | 網站 | 顯示PayPal網站上客戶購物車的條列專案完整摘要。 選項： `Yes` / `No` |
| [!UICONTROL Skip Order Review Step] | 網站 | 決定客戶是否可以從PayPal網站完成交易，或是必須返回您的商店並在提交訂單前完成「訂單複查」步驟。 選項： `Yes` / `No` |

{style="table-layout:auto"}
