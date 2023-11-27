---
title: 設定來源優先順序演演算法
description: 瞭解如何設定用於庫存中指派來源順序的來源優先順序，以便提出建議。
exl-id: 7b25212d-0cd0-4280-be23-c67f06db900a
feature: Inventory, Shipping/Delivery
source-git-commit: 023716935a6657b0dc2317876debe608e65bf010
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# 設定來源優先順序演演算法

自訂庫存包括指定的來源清單，以透過您的店面銷售及出貨可用的產品庫存。 此演演算法會使用庫存中的指派來源順序來提出建議。

執行時，演演算法會：

- 從最上方開始，在庫存層級處理已設定的來源順序

- 根據清單中的訂單、可用數量及訂購數量，建議出貨數量及每項產品的來源

- 繼續往下清單，直到訂單出貨已滿

- 如果在清單中找到已停用的來源，則會略過

若要設定，請以優先順序從上到下排列這些來源，以履行訂單。 「來源選取演演算法」(SSA)會在決定出貨與存貨扣除額時，使用此訂單提供演演算法「優先順序」。 另請參閱 [排定庫存來源的優先順序](stocks-prioritize-sources.md).

## 設定來源的優先順序

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**.

1. 在編輯模式中開啟庫存，並導覽至 _[!UICONTROL Sources]_區域。

1. 按一下 **[!UICONTROL Assign Sources]**.

1. 在 _[!UICONTROL Assign Sources]_檢視，選取所需來源的核取方塊，然後按一下&#x200B;**[!UICONTROL Done]**將來源指定給庫存。

>[!NOTE]
>
>使用時 [距離優先順序](distance-priority-algorithm.md) 如果路由和資料未針對選取的傳回，則為出貨演演算法 [計算模式](distance-priority-algorithm.md) （駕駛、騎腳踏車或徒步）對於出貨，SSA預設為使用「來源優先順序」。

![優先順序之後的來源順序](assets/inventory-stock-priority-after.png)

| 圖示 | 說明 |
|----------------------------------------------|----------------------------------------------------------------|
| ![拖放圖示以設定優先順序](assets/icon-drag-and-drop-action.png) | 用於根據優先順序拖放來源。 |
| ![按一下圖示以取消指派來源](assets/icon-delete-action.png) | 取消指定庫存的來源。 |
