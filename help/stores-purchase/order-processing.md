---
title: 訂單工作流程與處理
description: 瞭解訂單工作流程、每個步驟套用的狀態，以及如何透過此處理移轉訂單。
exl-id: 5bc152c8-2adf-4faf-af84-ca65d260c22a
feature: Orders, Customer Service
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1718'
ht-degree: 0%

---

# 訂單工作流程與處理

當客戶下訂單時，銷售訂單會建立為交易的暫時記錄。 在「訂單」網格中，銷售訂單一開始的狀態為「暫緩」，而且可以在處理付款之前隨時取消。 確認付款後，便可對訂單開立商業發票並出貨。

**步驟1：下單**  — 當購物者點按時，結帳程式就會開始 **[!UICONTROL Go to Checkout]** 在購物車頁面或 [重新排序](reorders-allow.md) 直接來自其客戶帳戶。

**步驟2：訂單擱置中**  — 初始銷售訂單狀態為 `Pending`. 在此狀態下，尚未處理付款，仍可編輯或取消訂單。 當付款方式設定為授權模式時，就會發生此狀態。

**步驟3：接收付款**  — 訂單狀態變更為 `Processing` 收到或授權付款時。 根據付款方式，您可能會在交易獲得授權或處理時收到通知。 當付款方式設定為擷取或意圖銷售模式時，此狀態會自動發生。

**步驟4：商業發票訂單**  — 通常會在收到付款後開立訂單。 付款方式會決定訂單所需的開立商業發票選項。 產生並提交商業發票後，系統會將復本傳送給客戶。 如果付款方式設定為 `capture` 或 `intent sale` 付款作業，在核准並擷取付款時，會自動產生商業發票。

>[!NOTE]
>
>使用下訂單時，不會自動建立發票 `Gift Card`， `Store Credit`， `Reward Points`，或其他離線付款方法。

**步驟5：預訂單一出貨**  — 訂單狀態變更為 `Complete` 當出貨明細完成時，出貨即已預訂，且出貨已設定。 列印的包裝單和送貨標籤，或 _通知準備取車_ 已選取（店內傳遞方式）。 客戶收到通知，且封裝已送出。 如果使用追蹤編號，則可從客戶帳戶追蹤出貨。

>[!NOTE]
>
>如需有關訂單狀態與付款方式組態選項的詳細資訊，請參閱 [訂單狀態](order-status.md) 和 [付款](payments.md).

## 檢視訂單

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. 在格線中尋找順序。

1. 在 _[!UICONTROL Action]_欄，按一下&#x200B;**[!UICONTROL View]**.

1. 檢查訂單狀態：

   - A `Pending` 訂單可以修改、保留、取消或開立商業發票與出貨。

   - A `Processing` 無法再大幅編輯或取消訂單，但可以編輯帳單和送貨地址。

   - A `Completed` 訂單可以重新排序。

您可以透過編輯客戶，隨時在訂單工作流程中編輯客戶的電子郵件。 如果訂單是由來賓下達，則無法編輯電子郵件。

未結訂單的左側面板可讓您存取與訂單相關的不同型別資訊。

![檢視訂單](./assets/order-view.png){width="700" zoomable="yes"}

## 處理訂單

當客戶下訂單時，銷售訂單會建立為交易的暫時記錄。 銷售訂單的狀態為 `Pending` 直到收到付款為止。 當在 `Pending` 狀態，直到收到付款並產生商業發票時，才能編輯或取消訂單。 簡單來說，訂單會變成商業發票，而商業發票會變成出貨。 「訂單」格線會列出所有訂單，無論這些訂單在工作流程中的位置為何。 若要瞭解如何協助客戶處理訂單，請參閱 [更新訂單](order-update.md).

![訂購](./assets/orders-grid.png){width="700" zoomable="yes"}

若要開啟 `Pending` 訂購，按一下 **[!UICONTROL Edit]** 位於右上角。

>[!NOTE]
>
>訂單只能在 `Pending` 狀態。 處於不同狀態的訂單或基於「 」的訂單不會顯示「編輯」按鈕 [議價報價](../b2b/quotes.md).

![編輯銷售訂單](./assets/order-pending.png){width="600" zoomable="yes"}

使用欄位說明作為參考，複查銷售訂單中的下列區段。

### 訂單檢視說明

| 標籤 | 說明 |
|--- |--- |
| [!UICONTROL Information] | 顯示訂單與帳戶的詳細資訊，包括帳單與出貨地址、付款與交貨方式、料號訂單、總計及備註。 |
| [!UICONTROL Invoices] | 列出與訂單相關聯的每張商業發票。 |
| [!UICONTROL Credit Memos] | 列出與訂單相關聯的每個銷退折讓單。 |
| [!UICONTROL Shipments] | 列出與訂單相關聯的每筆出貨記錄。 |
| [!UICONTROL Comments History] | 列出與訂單相關的所有附註。 |

{style="table-layout:auto"}

>[!NOTE]
>
>管理員使用者必須具備 **[!UICONTROL Sales / Archive]** [許可權](../systems/permissions-user-roles.md) 以檢視其角色範圍 _發票_， _銷退折讓單_、和 _出貨_ 順序索引標籤。

### 按鈕列

| 按鈕 | 說明 |
|--- |--- |
| **[!UICONTROL Back]** | 返回「訂單」頁面而不儲存變更。 |
| **[!UICONTROL Cancel]** | 取消銷售訂單。 |
| **[!UICONTROL Send Email]** | 傳送有關訂單的電子郵件給客戶。 |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | 將銷售訂單的狀態變更為 `On Hold`. 若要解除銷售訂單的保留，請選擇 **[!UICONTROL Unhold]**. |
| **[!UICONTROL Invoice]** | 將訂單轉換為商業發票，以從銷售訂單建立商業發票。 |
| **[!UICONTROL Ship]** | 建立訂單的出貨記錄。 |
| **[!UICONTROL Notify Order is Ready for Pickup]** | 僅在下訂單作為店內交貨時顯示。 通知客戶訂單已準備好取貨。 |
| **[!UICONTROL Reorder]** | 根據目前訂單建立銷售訂單。 |
| **[!UICONTROL Edit]** | 在編輯模式中開啟擱置訂單。 狀態為「 」的訂單看不到「編輯」按鈕 `Processing`或基於交涉報價的訂單。 |

{style="table-layout:auto"}

### 取消訂單

您可以 [取消](order-update.md) 尚未開立商業發票的訂單。 A [銷退折讓單](credit-memos.md) 如果客戶想要在開立商業發票（擷取付款）後取消訂單，則必須簽發。

如果訂單為 `Pending` 或 `Processing` 而且付款未擷取或未完全擷取，您可以 [讓訂單失效](#void-an-order) ，而不取消它。

若要還原已取消的訂單，請按一下 **[!UICONTROL Reorder]** 按鈕並建立具有狀態的新訂單 `Pending`.

>[!NOTE]
>
>取消訂單也會產生作廢，但作廢訂單不會觸發取消。

### 讓訂單失效

只有未開立商業發票的銷售訂單，其狀態為 `Processing`，和 [付款整合設定 `Authorize`](../configuration-reference/sales/payment-methods.md#payment-actions)，可以是 [已失效](order-update.md#void-a-processing-order). 取消訂單後，即可取消訂單。

### [!UICONTROL Order and Account Information]

![訂單與帳戶資訊](./assets/order-account-information.png){width="600" zoomable="yes"}

#### 訂單資訊

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Order Number] | 訂單編號會顯示在銷售訂單的頂端，後面會附註以指出是否已傳送確認電子郵件。 |
| [!UICONTROL Order Date] | 下訂單的日期和時間。 |
| [!UICONTROL Purchased From] | 表示下訂單的網站、商店和商店檢視。 |
| [!UICONTROL Placed from IP] | 表示下訂單所在電腦的IP位址。 |
| [!UICONTROL Order Placed from Quote] | ![Adobe Commerce B2B](../assets/b2b.svg) (可與Adobe Commerce B2B搭配使用)指出 [引用](../b2b/quotes.md) 產生訂單的來源（如適用）。 報價名稱會連結至報價。 |

{style="table-layout:auto"}

#### 帳戶資訊

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Customer Name] | 下訂單的客戶或採購員名稱。 客戶名稱會連結至客戶設定檔。 |
| [!UICONTROL Email] | 客戶或購買者的電子郵件地址。 電子郵件地址已連結，以開啟新的電子郵件訊息。 |
| [!UICONTROL Customer Group] | 將客戶指派給之客戶群組或共用目錄的名稱。 |
| [!UICONTROL Company Name] | ![Adobe Commerce B2B](../assets/b2b.svg) (可與Adobe Commerce B2B搭配使用)與購買者相關聯並代表其下訂單的公司名稱。 公司名稱已連結至 [公司設定檔](../b2b/account-companies.md). |

{style="table-layout:auto"}

### [!UICONTROL Address Information]

![地址資訊](./assets/order-address-information.png){width="600" zoomable="yes"}

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Billing Address] | 下訂單的客戶或購買者名稱，隨後加上帳單地址、電話號碼及 [VAT](vat.md)，如適用。 電話號碼已連結到行動裝置上的自動撥號。 |
| [!UICONTROL Shipping Address] | 訂單應送貨之人員的名稱，然後是送貨地址與電話號碼。 電話號碼已連結到行動裝置上的自動撥號。 |

{style="table-layout:auto"}

### [!UICONTROL Payment & Shipping Method]

![付款與送貨方法](./assets/order-payment-and-shipping-method-braintree.png){width="600" zoomable="yes"}

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Payment Information] | 用於訂單的付款方式，以及採購單編號（如果適用的話），後面接著用於下訂單的幣別。 如果訂單是借記到公司信用額度，使用 [分期付款](../b2b/enable-basic-features.md#configure-payment-on-account)，則會指出記入帳戶的金額。 |
| [!UICONTROL Shipping & Handling Information] | 要使用的送貨方式，以及適用的任何手續費。 |

{style="table-layout:auto"}

### 檢閱訂購的專案

![已訂購專案](./assets/order-items-ordered-tee.png){width="600" zoomable="yes"}

在 **[!UICONTROL Order Total]** 區段，請執行下列動作：

1. 輸入 **[!UICONTROL Comment]** 以包含在訂單中。

1. 如果您想要以電子郵件將註解傳送給客戶，請選取 **[!UICONTROL Notify Customer by Email]** 核取方塊。

1. 如果您希望註解顯示在客戶帳戶中，請選取 **[!UICONTROL Visible on Storefront]** 核取方塊。

   ![訂單總計](./assets/order-total.png){width="600" zoomable="yes"}

1. 如果您已準備好開立訂單發票，請按一下 **[!UICONTROL Invoice]** 並依照指示進行 [建立發票](invoices.md#create-an-invoice).

#### [!UICONTROL Items Ordered]

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Product] | 產品名稱、SKU和選項（如適用）。 |
| [!UICONTROL Item Status] | 表示專案的狀態。 值： `Ordered` |
| [!UICONTROL Original Price] | 折扣前料號的原始型錄價格。 |
| [!UICONTROL Price] | 專案的購買價格。 此值會反映從共用目錄套用至專案的任何折扣（若適用）。 |
| [!UICONTROL Qty] | 訂購數量。 |
| [!UICONTROL Subtotal] | 小計是採購價格乘以數量。 |
| [!UICONTROL Tax Amount] | 以小數值形式套用至專案的稅金金額。 |
| [!UICONTROL Tax Percent] | 以百分比形式套用至此專案的稅捐百分比。 |
| [!UICONTROL Discount Amount] | 適用於此專案的折扣。 如果訂單是以報價為基礎，則折扣值為零。 |
| [!UICONTROL Row Total] | 明細專案總計，包括產品層次到期的適用稅捐，減去折扣。 |

{style="table-layout:auto"}

#### [!UICONTROL Notes for this Order]

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Status] | 顯示銷售訂單的狀態。 |
| [!UICONTROL Comment] | 一個文字方塊，用來輸入訂單隨附之客戶的註解。 <br/>**[!UICONTROL Notify Customer by Email]**— 如果您要將註解以個別電子郵件的形式傳送給客戶，請選取核取方塊。<br/>**[!UICONTROL Visible on Storefront]**  — 如果您希望註解可從客戶帳戶中顯示，請選取核取方塊。 <br/>**[!UICONTROL Submit Comment]**— 提交註解並透過電子郵件傳送（如果適用）。 |

{style="table-layout:auto"}

#### [!UICONTROL Order Totals]

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Shipping & Handling] | 運費和手續費的金額。 |
| [!UICONTROL Tax] | 適用於訂單的稅捐金額（若適用）。 |
| [!UICONTROL Grand Total] | 訂單總計。 |
| [!UICONTROL Total Paid] | 支付給訂單的總金額（若適用）。 |
| [!UICONTROL Total Refunded] | 從訂單退款的金額總計（若適用）。 |
| [!UICONTROL Total Due] | 到期的總金額。 |
| [!UICONTROL Store Credit] | ![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)套用至訂單的可用商店點數金額（如適用）。 |
| [!UICONTROL Catalog Total Price] | ![Adobe Commerce B2B](../assets/b2b.svg) (可與Adobe Commerce B2B搭配使用)報價單中的料號總價（不含稅捐），根據作為報價單基礎的共用型錄或標準型錄中的定價而定。 如果店面顯示貨幣與基本貨幣不同，值會以兩種貨幣顯示，而店面會以方括弧顯示。 |
| [!UICONTROL Negotiated Discount] | ![Adobe Commerce B2B](../assets/b2b.svg) (適用於Adobe Commerce B2B)買方與賣方議價得出的折扣。 如果店面顯示貨幣與基本貨幣不同，值會以兩種貨幣顯示，而店面會以方括弧顯示。 |
| [!UICONTROL Subtotal] | ![Adobe Commerce B2B](../assets/b2b.svg) (可與Adobe Commerce B2B搭配使用)目錄總價減去議價折扣。 |

{style="table-layout:auto"}

## 訂單處理示範

觀看此影片，並深入瞭解訂單處理與狀態：

>[!VIDEO](https://video.tv.adobe.com/v/343935/?quality=12)
