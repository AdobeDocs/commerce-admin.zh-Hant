---
title: 簡單產品
description: 瞭解如何建立可個別銷售或作為已分組、可設定或套裝產品一部分的簡單產品。
exl-id: 3ac9b28d-3929-4fd6-97ca-145ea6d6897c
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 0%

---

# 簡單產品

運用產品型別力量的關鍵之一，是瞭解何時使用簡單、獨立的產品。 簡單產品可以單獨銷售，也可以作為已分組、可設定或搭售產品的一部分銷售。 具有自訂選項的簡單產品有時稱為&#x200B;_複合產品_。

下列指示示範使用[產品範本](attribute-sets.md)、必要欄位及基本設定來建立簡單產品的程式。 每個必要欄位都標有紅色星號(`*`)。 當您完成基本功能後，您可以視需要完成其他產品設定。

![簡單產品](./assets/product-simple.png){width="700" zoomable="yes"}

## 步驟1：選擇產品型別

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Products]**。

1. 在右上角的&#x200B;_[!UICONTROL Add Product]_（![功能表箭頭](../assets/icon-menu-down-arrow-red.png){width="25"} ）功能表上，選擇&#x200B;**[!UICONTROL Simple Product]**。

   ![新增簡單產品](./assets/product-add-simple.png){width="700" zoomable="yes"}

## 步驟2：選擇屬性集

若要選擇用作產品範本的[屬性集](attribute-sets.md)：

- 按一下&#x200B;**[!UICONTROL Attribute Set]**&#x200B;欄位，然後輸入屬性集的全部或部分名稱。

- 在顯示的清單中，選擇要使用的屬性集。

表單會更新以反映變更。

![選擇屬性集](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## 步驟3：完成必要的設定

1. 輸入&#x200B;**[!UICONTROL Product Name]**。

1. 接受以產品名稱為基礎的預設&#x200B;**[!UICONTROL SKU]**，或輸入其他名稱。

1. 輸入產品&#x200B;**[!UICONTROL Price]**。

1. 因為產品尚未準備好發佈，請將&#x200B;**[!UICONTROL Enable Product]**&#x200B;選項設定為`No`。

1. 按一下&#x200B;**[!UICONTROL Save]**&#x200B;並繼續。

   儲存產品時，[商店檢視](introduction.md#product-scope)選擇器會出現在左上角。

1. 選擇要提供產品的&#x200B;**[!UICONTROL Store View]**。

   ![選擇商店檢視](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## 步驟4：完成基本設定

1. 將&#x200B;**[!UICONTROL Tax Class]**&#x200B;設定為下列其中一項：

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

1. 輸入有庫存的產品的&#x200B;**[!UICONTROL Quantity]**。

   根據預設，**[!UICONTROL Stock Status]**&#x200B;已設為`In Stock`。

   >[!NOTE]
   >
   >如果您啟用[Inventory management](../inventory-management/introduction.md)，Single Source商家會在此區段中設定數量。 多Source商家在「來源」區段中新增來源和數量。 請參閱下列&#x200B;_指派來源與數量(Inventory management)_&#x200B;區段。

1. 輸入產品的&#x200B;**[!UICONTROL Weight]**。

1. 接受`Catalog, Search`的預設&#x200B;**[!UICONTROL Visibility]**&#x200B;設定。

1. 若要將&#x200B;_[!UICONTROL Categories]_指派給產品，請按一下&#x200B;**[!UICONTROL Select…]**方塊並執行下列任一動作：

   **選擇現有類別**：

   - 開始在方塊中輸入內容，直到找到相符專案為止。

   - 選取要指派的每個類別的核取方塊。

   **建立類別**：

   - 按一下&#x200B;**[!UICONTROL New Category]**。

   - 輸入&#x200B;**[!UICONTROL Category Name]**&#x200B;並選擇&#x200B;**[!UICONTROL Parent Category]**，這會決定其在功能表結構中的位置。

   - 按一下&#x200B;**[!UICONTROL Create Category]**。

1. 若要在[新產品](../content-design/widget-new-products-list.md)的清單中新增產品，請選取&#x200B;**[!UICONTROL Set Product as New]**&#x200B;核取方塊。

1. 選擇&#x200B;**[!UICONTROL Country of Manufacture]**。

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

## 步驟6：Publish產品

1. 如果您已準備好發佈目錄中的產品，請將&#x200B;**[!UICONTROL Enable Product]**&#x200B;切換為`Yes`。

1. 執行下列任一項作業：

   - **方法1：**&#x200B;儲存並預覽

      - 按一下右上角的&#x200B;**[!UICONTROL Save]**。

      - 若要檢視您商店中的產品，請在&#x200B;_管理員_ （![功能表箭頭](../assets/icon-menu-down-arrow-black.png)）功能表上選擇&#x200B;**[!UICONTROL Customer View]**。

     該存放區會在新的瀏覽器標籤中開啟。

     ![客戶檢視](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **方法2：**&#x200B;儲存並關閉

     在&#x200B;_[!UICONTROL Save]_（![功能表箭頭](../assets/icon-menu-down-arrow-red.png){width="25"} ）功能表上，選擇&#x200B;**[!UICONTROL Save & Close]**。

## 注意事項

- 可配置、搭售和分組產品型別中可包含簡單產品。

- 簡單產品設定會覆寫特定產品可設定的產品設定。

- 簡單的產品可以有包含各種輸入型別的自訂選項，因此可以從單一SKU銷售許多產品變體。
