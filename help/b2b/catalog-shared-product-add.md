---
title: 將產品新增至共用目錄
description: 瞭解如何個別或依類別以群組方式將產品新增至共用目錄。
exl-id: c88b46b4-cea8-4f65-b7e4-6681bab64d41
feature: B2B, Companies, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 0%

---

# 將產品新增至共用目錄

產品可以個別地或依類別以多個產品的群組新增到共用目錄中。

複雜產品（例如套件、群組或可設定）必須符合下列要求，才能從共用目錄中的店面顯示：

- 全部 [關聯產品](../catalog/product-configurations.md) 和選項必須指派給相同的共用目錄，並在主要目錄中啟用。
- 的 [可設定](../catalog/product-create-configurable.md) 和 [已分組](../catalog/product-create-grouped.md) 產品，則只會顯示啟用的關聯產品。
- 針對 [組合](../catalog/product-create-bundle.md) 產品，所有選項都必須包含在共用目錄中。

  ![選取目錄產品](./assets/shared-catalog-select-products-step-1.png){width="600" zoomable="yes"}

## 方法1：新增單一產品

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 對於格線中您要新增的產品，請移至 _[!UICONTROL Action]_欄並按一下&#x200B;**[!UICONTROL Edit]**.

1. 向下捲動，展開 ![展開選擇器](../assets/icon-display-expand.png) 此 _[!UICONTROL Product in Shared Catalogs]_的部分，並執行下列動作：

   - 選取產品應顯示之每個共用目錄的核取方塊。 若要選擇所有目錄，請按一下 **[!UICONTROL Select all]**.

     ![共用目錄中的產品](./assets/shared-catalog-assign-from-product.png){width="600" zoomable="yes"}

     每個所選目錄的名稱都會顯示在 _[!UICONTROL Shared Catalogs]_欄位。

     ![已指派的共用目錄](./assets/shared-catalog-assigned.png){width="600" zoomable="yes"}

   - 按一下 **[!UICONTROL Done]** 以儲存設定。

1. 完成後，按一下 **[!UICONTROL Save]**.

## 方法2：新增多個產品

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. 對於格線中的共用目錄，請移至 _[!UICONTROL Action]_欄並選取&#x200B;**[!UICONTROL Set Pricing and Structure]**.

1. 在類別樹狀結構中，執行下列任一項作業：

   - 若要包含所有產品，請按一下 **[!UICONTROL Select all]** 或選取父類別的核取方塊。
   - 若要包含特定類別的產品，請選取您要包含的每個類別的核取方塊。
   - 若要包含或排除個別產品，請選取或取消選取產品的核取方塊。

   樹狀結構中每個類別下方的標籤法會顯示目前包含在共用目錄中的類別產品數量。 下方記號 [根類別](../catalog/category-root.md) 顯示目前為共用目錄選取之所有類別的產品總數。

1. 若要檢視格線中的類別產品，請按一下樹狀結構中的類別名稱。

   選取類別時，會發生下列情況：

   - 格線第一欄的切換設定為 `On` 每個已選取產品的屬性。
   - 如果產品指派給多個類別，且其中一個類別中省略，則它仍可透過其他類別和以下方式使用： [目錄搜尋](../catalog/search.md).
   - 系統會自動設定 [類別許可權](../catalog/category-permissions.md) 至 `Allow` 所選產品的。
