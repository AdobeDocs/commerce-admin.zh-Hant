---
title: 簡單產品
description: 瞭解如何建立可個別銷售或作為已分組、可設定或套裝產品一部分的簡單產品。
exl-id: 3ac9b28d-3929-4fd6-97ca-145ea6d6897c
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '594'
ht-degree: 0%

---

# 簡單產品

運用產品型別力量的關鍵之一，是瞭解何時使用簡單、獨立的產品。 簡單產品可以單獨銷售，也可以作為已分組、可設定或搭售產品的一部分銷售。 具有自訂選項的簡單產品有時稱為 _複合產品_.

下列指示示範使用建立簡單產品的程式 [產品範本](attribute-sets.md)、必填欄位和基本設定。 每個必填欄位都標有紅色星號(`*`)。 當您完成基本功能後，您可以視需要完成其他產品設定。

![簡單產品](./assets/product-simple.png){width="700" zoomable="yes"}

## 步驟1：選擇產品型別

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 在 _[!UICONTROL Add Product]_( ![選單箭頭](../assets/icon-menu-down-arrow-red.png){width="25"} )功能表，選擇&#x200B;**[!UICONTROL Simple Product]**.

   ![新增簡單產品](./assets/product-add-simple.png){width="700" zoomable="yes"}

## 步驟2：選擇屬性集

若要選擇 [屬性集](attribute-sets.md) 做為產品的範本：

- 按一下 **[!UICONTROL Attribute Set]** 欄位並輸入屬性集的全部或部分名稱。

- 在顯示的清單中，選擇要使用的屬性集。

表單會更新以反映變更。

![選擇屬性集](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## 步驟3：完成必要的設定

1. 輸入 **[!UICONTROL Product Name]**.

1. 接受預設值 **[!UICONTROL SKU]** 根據產品名稱或輸入其他名稱。

1. 輸入產品 **[!UICONTROL Price]**.

1. 由於產品尚未準備好發佈，請設定 **[!UICONTROL Enable Product]** 選項至 `No`.

1. 按一下 **[!UICONTROL Save]** 並繼續。

   儲存產品時， [存放區檢視](introduction.md#product-scope) 選擇器會出現在左上角。

1. 選擇 **[!UICONTROL Store View]** 產品可用的位置。

   ![選擇商店檢視](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## 步驟4：完成基本設定

1. 設定 **[!UICONTROL Tax Class]** 變更為下列其中一項：

   - `None`
   - `Taxable Goods`
   - `Refund Adjustments`
   - `Gift Options`
   - `Order Gift Wrapping`
   - `Item Gift Wrapping`
   - `Printed Gift Card`
   - `Reward Points`
   - `VAT Reduced`
   - `VAT Standard`

1. 輸入 **[!UICONTROL Quantity]** 有庫存的產品的ID。

   根據預設， **[!UICONTROL Stock Status]** 設為 `In Stock`.

   >[!NOTE]
   >
   >如果您啟用 [Inventory management](../inventory-management/introduction.md)，單一來源商家會設定本節中的數量。 多來源商家在「來源」區段中新增來源與數量。 請參閱下列內容 _指定來源與數量(Inventory management)_ 區段。

1. 輸入 **[!UICONTROL Weight]** 產品的。

1. 接受預設值 **[!UICONTROL Visibility]** 設定 `Catalog, Search`.

1. 要指派 _[!UICONTROL Categories]_若要存取產品，請按一下&#x200B;**[!UICONTROL Select…]**方塊並執行下列任一項作業：

   **選擇現有類別**：

   - 開始在方塊中輸入內容，直到找到相符專案為止。

   - 選取要指派的每個類別的核取方塊。

   **建立類別**：

   - 按一下 **[!UICONTROL New Category]**.

   - 輸入 **[!UICONTROL Category Name]** 並選擇 **[!UICONTROL Parent Category]**，這會決定其在功能表結構中的位置。

   - 按一下 **[!UICONTROL Create Category]**.

1. 若要在產品清單中推出產品 [新產品](../content-design/widget-new-products-list.md)，選取 **[!UICONTROL Set Product as New]** 核取方塊。

1. 選擇 **[!UICONTROL Country of Manufacture]**.

可能有其他個別屬性可說明產品。 選取範圍會因屬性集而異，您稍後可以完成它們。

### 指定來源與數量([!DNL Inventory Management])

{{$include /help/_includes/inventory-assign-sources.md}}

## 步驟5：完成產品資訊

視需要向下捲動並填入下列章節中的資訊：

- [內容](product-content.md)
- [影像和影片](product-images-and-video.md)
- [相關產品、向上銷售和交叉銷售](related-products-up-sells-cross-sells.md)
- [搜尋引擎最佳化](product-search-engine-optimization.md)
- [可自訂的選項](settings-advanced-custom-options.md)
- [網站中的產品](settings-basic-websites.md)
- [設計](settings-advanced-design.md)
- [贈品選項](product-gift-options.md)

## 步驟6：發佈產品

1. 如果您已準備好在目錄中發佈產品，請設定 **[!UICONTROL Enable Product]** 切換至 `Yes`.

1. 執行下列任一項作業：

   - **方法1：** 儲存並預覽

      - 在右上角，按一下 **[!UICONTROL Save]**.

      - 若要檢視您商店中的產品，請選擇 **[!UICONTROL Customer View]** 於 _管理員_ (![選單箭頭](../assets/icon-menu-down-arrow-black.png))功能表。

     該存放區會在新的瀏覽器標籤中開啟。

     ![客戶檢視](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **方法2：** 儲存並關閉

     在 _[!UICONTROL Save]_ ( ![選單箭頭](../assets/icon-menu-down-arrow-red.png){width="25"} )功能表，選擇&#x200B;**[!UICONTROL Save & Close]**.

## 注意事項

- 可配置、搭售和分組產品型別中可包含簡單產品。

- 簡單產品設定會覆寫特定產品可設定的產品設定。

- 簡單的產品可以有包含各種輸入型別的自訂選項，因此可以從單一SKU銷售許多產品變體。
