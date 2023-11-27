---
title: 『[!UICONTROL Sales] 功能表
description: 商務管理員包含 [!UICONTROL Sales] 功能表，可讓您根據訂單在工作流程中的位置來存取用於處理訂單的工具。
exl-id: 105106a4-85f7-4143-8411-69ff67ff9331
source-git-commit: a7c6203cf738e3fb9be887d637010ca9c155937a
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---

# [!UICONTROL Sales] 功能表

「銷售」功能表會根據異動在訂單工作流程中的位置來列出異動。 您可能會將每個選項視為訂單期限中的不同階段。

![銷售功能表](./assets/admin-menu-sales.png){width="450" zoomable="yes"}

## 顯示 [!UICONTROL Sales] 功能表

在 _管理員_ 側欄，按一下 **[!UICONTROL Sales]**.

## 功能表選項

### [!UICONTROL Quotes]

![適用於Adobe Commerce的B2B](../assets/b2b.svg) (適用於Adobe Commerce的B2B提供)

授權購買者可以 [議價](../b2b/quotes.md) 傳送訊息給賣家 [請求](../b2b/quote-request.md) 從購物車中。

### [!UICONTROL Orders]

當 [訂購](orders.md) 已下單，則會建立銷售訂單作為交易的暫時記錄。 尚未處理付款，訂單仍可取消。

### [!UICONTROL Invoices]

一個 [invoice](invoices.md) 是訂單付款的收款記錄。 單一訂單可建立多張發票，每張發票可包含您所指定之採購產品的數量或數量。 視付款作業而定，系統會在產生商業發票時自動擷取付款。

### [!UICONTROL Shipments]

A [出貨](shipments.md) 是已出貨訂單中產品的記錄。 與商業發票一樣，在訂單中的所有產品都已出貨之前，多個出貨可以與單一訂單相關聯。

### [!UICONTROL Credit Memos]

A [銷退折讓單](credit-memos.md) 是一份檔案，顯示客戶全額或部分退款的應付金額。 金額可用於購買或退款給客戶。

### [!UICONTROL Returns]

![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)

A [退貨商品授權](returns.md) (RMA)可授與要求退回料號以進行更換或退款的客戶。 RMA可針對簡單、分組、可設定和套裝產品型別發行。 不過，RMA不適用於虛擬及可下載的產品，或禮品卡。

### [!UICONTROL Billing Agreements]

A [帳單協定](paypal-billing-agreements.md) 與採購單類似，但不限於單次購買。 結帳時，客戶選擇「帳單協定」作為付款方式。 帳單協定可簡化結帳程式，因為客戶不需要為每次購買輸入付款資訊。

### [!UICONTROL Transactions]

此 [交易](transactions.md) 頁面會列出您的商店與所有付款系統之間發生的所有付款活動，並提供更詳細資訊的存取權。

### [!UICONTROL Braintree Virtual Terminal]

在「Braintree虛擬終端機」頁面上，管理員使用者可接受所選金額的付款。 若要讓終端機功能可用，商家應該設定基本 [Braintree設定](braintree.md). Braintree提供完全可自訂的結帳體驗，包含詐騙偵測和PayPal整合。

### [!UICONTROL Archive]

![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)

（必須啟用封存選項） [封存訂單](order-archive.md) 和其他銷售檔案會定期改善效能，讓您的工作區沒有不必要的資訊。
