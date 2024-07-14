---
title: 大量存貨來源指定與取消指定
description: 瞭解如何使用指派來源工具來管理產品的來源指派。
exl-id: 1f1e81a5-fb06-46b7-84ca-7feea4942093
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 0%

---

# 大量來源指派和取消指派

使用&#x200B;_指派來源_&#x200B;工具新增一或多個來源至您的產品。 此工具有助於建立自訂來源並指派給您的預設庫存或自訂庫存，以及準備新的位置和庫存。

新增自訂來源後，您可以透過管理員或使用[匯入功能](inventory-import-export.md)，為每個產品](quantities-assign-per-product.md)或多個產品新增[存貨數量。

![新增所選產品的詳細目錄來源](assets/inventory-bulk-assign-sources.gif)

## 指定來源與數量

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Products]**。

1. 選取您要修改其來源的產品。

   瀏覽或搜尋以尋找產品並選取這些核取方塊。

1. 按一下頂端的&#x200B;**[!UICONTROL Actions]**&#x200B;功能表，然後選擇&#x200B;**[!UICONTROL Assign Inventory Source]**。

1. 在確認對話方塊中按一下&#x200B;**[!UICONTROL OK]**。

1. 針對您要新增至產品的所有來源，選取核取方塊。

1. 按一下&#x200B;**[!UICONTROL Assign Sources]**。

   ![選取要新增來源的產品](assets/inventory-bulk-assign-sources-summary.png){width="600" zoomable="yes"}

會將來源新增至存貨數量為0的產品。 您可以為每個來源新增[存貨數量](quantities-assign-per-product.md)。

## 取消指定來源與數量

從產品取消指派來源時，您會指出該產品不再儲存在該位置。 此程式會完全清除目前指派給產品之來源的所有詳細目錄資料。 如果您想要將現有存貨移轉到新位置，請考慮使用&#x200B;_移轉存貨_&#x200B;選項。

{{$include /help/_includes/unassign-source.md}}

強烈建議您在移除來源之前，完成這些產品的所有訂單與出貨。

![取消指派所選產品的來源](assets/inventory-bulk-unassign-sources.gif)

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Products]**。

1. 選取您要修改來源的產品。

   瀏覽或搜尋以尋找產品並選取這些核取方塊。

1. 按一下頂端的&#x200B;**[!UICONTROL Actions]**&#x200B;功能表，然後選擇&#x200B;**[!UICONTROL Unassign Inventory Source]**。

1. 在確認對話方塊中按一下&#x200B;**[!UICONTROL OK]**。

1. 選取您要從產品中移除的來源。

   頁面會顯示取消指派會從產品中移除所有特定來源和數量資料的警報。

1. 按一下&#x200B;**[!UICONTROL Unassign Sources]**。

   ![從選取的產品移除來源](assets/inventory-bulk-unassign-sources-summary.png){width="600" zoomable="yes"}
