---
title: Quote template use cases and workflows
description: Create a quote template from an existing quote to streamline quote negotiation for recurring orders.
feature: B2B, Quotes
source-git-commit: 3000d9abab467a86e37c7eca6e7db16b39c763ab
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 0%

---


# Quote templates use case and workflows

The Quote Template capability allows buyers and sellers to streamline the quote process by creating reusable and customizable quote templates.

- **可自訂的報價單** — 採購員可以從預先核准的範本產生連結的報價單，允許在指定的引數（如明細行料號數量與選取專案）中進行自訂。
- ****
- ****
- ****
- ****

## Use Case

公司購買者可以使用報價範本，在一段時間內訂購特定的一組產品。 採購員設定下列報價樣版選項，讓報價程式更有效率、更一致，並與策略性採購協定一致。

- 訂單臨界值，指定適用於議價訂價的最小與最大訂單數。 這可用來套用及追蹤合約協定中指定的訂單配額。

- 數量臨界值（最小/最大數量）樣版會指定數量臨界值，以設定每筆訂單可購買的最小與最大數量，確保賣家能有效管理存貨層次，同時提供買方彈性來視需要調整數量。

## 報價範本工作流程

報價範本可由買方或賣方起始。

**步驟1：報價範本建立（新增）**

- **購買者建立報價範本**

  在複查現有的報價範本時，採購員決定公司必須在下一年度提交多份訂單，並想要根據重複的業務請求額外的折扣。 他們使用報價上的&#x200B;*[!UICONTROL Create quote template]*&#x200B;動作來建立報價範本。 然後，他們透過將新範本傳送給賣方進行稽核來啟動交涉。

  買家也可以直接從店面的&#x200B;*[!UICONTROL My Quote Templates]**頁面建立報價範本。

- ****[!UICONTROL Quote Templates]`draft`In draft state, the quote is visible only to the seller. `Submitted`It cannot be modified by the seller until the buyer sends it back.

  ![賣家從Admin](./assets/quote-template-create-from-grid.png){width="700" zoomable="yes"}的Quotes格線中起始買方報價

**步驟2：報價稽核與交涉（稽核）**

複查或議定報價樣版可包括變更數量、移除料號、新增明細專案備註、套用明細專案或報價折扣（賣方）以及新增出貨地址（採購員）。

- *****[!UICONTROL Quote Templates]*`Pending`[](quote-price-negotiation.md) The buyer and sales representative are notified by email that the seller has responded.

- ****__ The buyer can leave notes to the seller at the line item or quote level, change quantities, and remove items.

The buyer and seller continue the negotiation process until an agreement is reached, or the seller declines the quote template. If the buyer makes changes to the quote—adding or removing products or changing product quantities—the quote must be returned to the seller for review.

- **購買者新增送貨地址** — 如果報價範本沒有送貨地址，購買者必須新增送貨地址。 買方新增地址後，賣方可提供運送和交貨選項。 顯示的送貨方法視店面組態而定。

如果買方新增出貨地址，則必須複查議價協定，而賣方可以繼續議價處理，直到達成協定或賣方拒絕報價樣版為止。

**步驟3：購買者接受報價範本**

採購員接受樣版中的議定條款。 接受報價樣版之後，採購員可以使用樣版來產生預先核准的連結式報價單，這些報價單可用於提交訂單，而不需要進一步的議價。

結帳時鎖定送貨選項。

### 檢視報價範本

1. 在記錄的&#x200B;**[!UICONTROL Actions]**&#x200B;欄中，按一下&#x200B;**[!UICONTROL View]**。

1. 若要回應客戶請求，請遵循指示，開始與議價報價單相同的[價格議價](quote-price-negotiation.md)處理。

### 檢視報價範本活動

[!UICONTROL Comments][!UICONTROL History Log]

1. Open a quote template.

1. **[!UICONTROL Negotiation]****[!UICONTROL Comments]****[!UICONTROL History Log]**

   ![檢視歷程記錄](./assets/quote-view-history.png){width="400"}

1. 歷史記錄也會在明細行專案層次進行追蹤。

   ![檢視條列專案歷史記錄](./assets/quote-view-line-item-history.png){width="400"}


### 拒絕報價範本

只能拒絕狀態為`In Review`的報價範本。

1. 從&#x200B;*[!UICONTROL Quote Templates]*&#x200B;格線中，開啟您要拒絕的報價範本。

1. 在報價範本上，按一下&#x200B;**[!UICONTROL Decline]**。

1. 出現提示時，輸入報價遭拒絕的原因，然後按一下&#x200B;**[!UICONTROL Confirm]**。
