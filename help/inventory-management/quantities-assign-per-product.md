---
title: 指定每個產品的存貨數量
description: 瞭解如何更新產品的存貨數量，以及追蹤庫存量、可用存貨量。
exl-id: 935385bb-6657-4d49-980e-96a3d0d3a187
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# 指定每個產品的數量

新增之後 [來源](sources-assign-per-product.md)，更新產品的存貨數量。 這些值會追蹤庫存量、可用庫存量。

若要在不移除來源的情況下隱藏出貨來源的存貨，請設定 _[!UICONTROL Source Item Status]_至 `Out of Stock`. SSA和出貨選項只會存取下列來源 `In Stock` 具有可用存貨數量。

所有更新的數量和來源都會顯示在產品格線中。

## 更新數量

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 在編輯模式中尋找並開啟產品。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Sources]** 區段。

1. 設定 **[!UICONTROL Source Item Status]** 至 `In Stock`.

1. 若要更新庫存量數量，請輸入 **[!UICONTROL Qty]**.

1. 若要設定存貨數量的通知，請執行下列其中一項作業：

   - 自訂通知數量 — 取消選取 **[!UICONTROL Use Default]** 核取方塊，並輸入金額 **[!UICONTROL Notify Qty]**.
   - 預設通知數量 — 選取 **[!UICONTROL Use Default]** 核取方塊。 [!DNL Commerce] 檢查並使用中的設定 _[!UICONTROL Advanced Inventory]_或全域存放區設定。

   ![更新每個來源的產品數量](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. 執行下列任一項作業以儲存：

   - 按一下 **[!UICONTROL Save]**.

   - 在 **[!UICONTROL Save]** (![選單箭頭](../assets/icon-menu-down-arrow-red.png))功能表，選擇 **[!UICONTROL Save & Close]**.


「產品格線」會以所有來源和相關數量的清單更新。 對於超過五個指派來源的產品，將游標暫留在 _[!UICONTROL Quantity per Source]_欄，以檢視完整清單。

![每個來源的產品數量](assets/inventory-product-quantity.png){width="600" zoomable="yes"}
