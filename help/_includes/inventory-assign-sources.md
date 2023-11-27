---
title: 存貨 — 指定來源與數量
description: 關於建立目錄產品時指定來源與數量的「重複使用」區段。
source-git-commit: f36925217230e558043078fdc274f5e69c096c1e
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---

# 存貨 — 指定來源與數量

針對多來源商家，使用 [[!DNL Inventory Management]](../inventory-management/introduction.md)，向下捲動至 **來源** 並指定來源與數量：

1. 若要新增來源，請按一下 **[!UICONTROL Assign Sources]**.

1. 瀏覽或搜尋來源，並選取您要為產品新增之來源旁的核取方塊。

   ![將來源指派給產品](../catalog/assets/inventory-product-assign-sources.png){width="600" zoomable="yes"}

1. 按一下 **[!UICONTROL Done]** 以新增來源。

1. 若要管理來源的數量和狀態，請按一下 **[!UICONTROL Advanced Inventory]** 並設定 **[!UICONTROL Manage Stock]** 至 `Yes`.

1. 設定 **[!UICONTROL Source Item Status]** 至 `In Stock`.

1. 輸入更新金額 **[!UICONTROL Qty]** 用於庫存量。

1. 若要設定存貨數量的通知，請執行下列其中一項作業：

   - _自訂通知數量_  — 清除 **[!UICONTROL Notify Quantity Use Default]** 核取方塊，並輸入金額 **[!UICONTROL Notify Quantity]**.

   - _預設通知數量_  — 選取 **[!UICONTROL Notify Quantity Use Default]** 核取方塊。 Commerce會檢查並使用中的設定 [!UICONTROL Advanced Inventory] 或全域存放區設定。

   ![更新每個來源的產品數量](../catalog/assets/inventory-product-quantity.png){width="600" zoomable="yes"}
