---
title: 已分組的產品
description: 瞭解如何建立包含簡單獨立產品（以群組呈現）的群組產品。
exl-id: af42b7fc-27f2-4c5a-b504-a70a324fae76
feature: Catalog Management, Products
source-git-commit: 140930df515d1e0604b18a4ebf689254b9487b53
workflow-type: tm+mt
source-wordcount: '1055'
ht-degree: 0%

---

# 已分組的產品

群組產品由簡單獨立產品組成，並以群組呈現。 您可以提供單一產品的變數，或依季節或主題分組。 展示分組產品可鼓勵客戶購買其他專案。 分組產品可讓您輕鬆提供產品的變化，並在相同頁面上列出所有變化。

例如，您可能會銷售開放式庫存的平面軟體，並列出在正式位置設定中使用的各種器具。 有人可能會訂購多份沙拉叉、魚叉、晚餐叉、晚餐刀、魚刀、黃油刀、湯匙和甜點勺子。 其他客戶可能會訂購簡單的叉子、刀和勺子。 客戶可依需求訂購任何數量的專案。

雖然是以群組方式顯示，但群組中的每項產品都是以個別專案的形式購買。 在購物車中，每個專案和購買的數量都會顯示為個別的條列專案。

下列指示示範使用[產品範本](attribute-sets.md)、必要欄位及基本設定來建立群組產品的程式。 每個必要欄位都標有紅色星號(`*`)。 當您完成基本功能後，您可以視需要完成其他產品設定。

![已分組的產品](./assets/product-grouped.png){width="700" zoomable="yes"}

## 步驟1：選擇產品型別

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Products]**。

1. 在右上角的&#x200B;_[!UICONTROL Add Product]_（![功能表箭頭](../assets/icon-menu-down-arrow-red.png){width="25"} ）功能表上，選擇&#x200B;**[!UICONTROL Grouped Product]**。

   ![新增分組的產品](./assets/product-add-grouped.png){width="700" zoomable="yes"}

## 步驟2：選擇屬性集

若要選擇做為產品範本的[屬性集](attribute-sets.md)，請執行下列其中一項作業：

- 若要搜尋，請輸入&#x200B;**[!UICONTROL Attribute Set]**&#x200B;的名稱。
- 在清單中，選擇要使用的屬性集。

表單會更新以反映變更。

![選擇範本](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

如果需要的屬性不存在，您可以在建立產品時新增屬性：

- 按一下右上角的&#x200B;**[!UICONTROL Add Attribute]**。
- 定義新屬性（請參閱[將屬性新增至產品](product-attributes-add.md)）。

  ![新屬性](./assets/product-attribute-add-select.png){width="600" zoomable="yes"}

若要將現有屬性加入產品中，請使用[篩選控制項](../getting-started/admin-grid-controls.md)在格線中尋找屬性，並執行下列動作：

- 在要新增的每個屬性的第一欄中選取核取方塊。
- 按一下&#x200B;**[!UICONTROL Add Selected]**。

## 步驟3：完成必要的設定

1. 輸入&#x200B;**[!UICONTROL Product Name]**。

1. 接受以產品名稱為基礎的預設&#x200B;**[!UICONTROL SKU]**，或輸入其他名稱。

   請注意，**[!UICONTROL Quantity]**&#x200B;欄位無法使用，因為值衍生自組成群組的個別產品。

   群組的產品在目錄中沒有自己的價格。 群組產品價格衍生自群組中所包含個別產品的價格。

1. 因為產品尚未準備好發佈，請將&#x200B;**[!UICONTROL Enable Product]**&#x200B;設定為`No` （ ![切換否](../assets/toggle-no.png) ）。

1. 按一下&#x200B;**[!UICONTROL Save]**&#x200B;並繼續。

   儲存產品時，產品名稱會出現在頁面頂端，[商店檢視](introduction.md#product-scope)選擇器會出現在左上角。

1. 選擇要提供產品的&#x200B;**[!UICONTROL Store View]**。

   ![選擇存放區檢視](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## 步驟4：完成基本設定

1. 接受`In Stock`的&#x200B;**[!UICONTROL Stock Status]**&#x200B;設定。

1. 若要將&#x200B;**[!UICONTROL Categories]**&#x200B;指派給產品，請按一下&#x200B;**[!UICONTROL Select…]**&#x200B;方塊並執行下列任一動作：

   **選擇現有類別：**

   - 開始在方塊中輸入內容，直到找到相符專案為止。

   - 選取要指派的類別的核取方塊。

   **建立類別：**

   - 按一下&#x200B;**[!UICONTROL New Category]**。

   - 輸入&#x200B;**[!UICONTROL Category Name]**&#x200B;並選擇&#x200B;**[!UICONTROL Parent Category]**，這會決定其在功能表結構中的位置。

   - 按一下&#x200B;**[!UICONTROL Create Category]**。

1. 接受`Catalog, Search`的&#x200B;**[!UICONTROL Visibility]**&#x200B;設定。

1. 若要在新產品[清單](../content-design/widget-new-products-list.md)中設定該產品，請選擇行事曆上的&#x200B;**[!UICONTROL Set Product as New]** **[!UICONTROL from]**&#x200B;和&#x200B;**[!UICONTROL to]**&#x200B;日期。

1. 選擇&#x200B;**[!UICONTROL Country of Manufacture]**。

   可能有其他個別屬性可說明產品。 選取範圍會改變屬性集，您稍後可以完成它們。

## 步驟5：將產品新增至群組

1. 向下捲動至&#x200B;**[!UICONTROL Grouped Products]**&#x200B;區段並按一下&#x200B;**[!UICONTROL Add Products to Group]**。

   ![已分組的產品](./assets/product-grouped-products.png){width="600" zoomable="yes"}

1. 如有必要，請使用[篩選器](../getting-started/admin-grid-controls.md)來尋找您要加入群組的產品。

1. 在清單中，選取要包含在群組中的每個專案的核取方塊。

   >[!NOTE]
   >
   >只有簡單、可下載且沒有可設定選項的虛擬產品才能分組為子產品。 其他產品型別不會出現在選取專案清單中。

   ![新增選取的產品](./assets/product-grouped-add-products.png){width="600" zoomable="yes"}

1. 若要將其新增至產品群組，請按一下&#x200B;**[!UICONTROL Add Selected Products]**。

   選取的產品會出現在&#x200B;_[!UICONTROL Grouped Products]_區段中。

   對於具有[Inventory management](../inventory-management/sources-stocks.md)的多Source商家，網格包含&#x200B;**[!UICONTROL Quantity per Source]**&#x200B;欄，每個欄各有指定的來源和存貨量。

   群組](./assets/product-grouped-grouped-products-section.png){width="600" zoomable="yes"}中的![產品

1. 輸入任何專案的&#x200B;**[!UICONTROL Default Quantity]**。

1. 若要變更產品的順序，請抓取第一欄中的&#x200B;_變更順序_&#x200B;圖示（ ![位置控制器](../assets/icon-sort-order.png) ），並將產品拖曳到清單中的新位置。

1. 若要從群組移除產品，請按一下&#x200B;**[!UICONTROL Remove]**。

## 步驟5：完成產品資訊

視需要填寫下列章節中的資訊：

- [內容](product-content.md)
- [影像和影片](product-images-and-video.md)
- [搜尋引擎最佳化](product-search-engine-optimization.md)
- [相關產品、向上銷售和交叉銷售](related-products-up-sells-cross-sells.md)
- [可自訂的選項](settings-advanced-custom-options.md)
- [網站中的產品](settings-basic-websites.md)
- [設計](settings-advanced-design.md)
- [贈品選項](product-gift-options.md)

## 步驟6：Publish產品

1. 如果您已準備好發佈目錄中的產品，請將&#x200B;**[!UICONTROL Enable Product]**&#x200B;設為`Yes`。

1. 執行下列任一項作業：

   **方法1：**&#x200B;儲存並預覽

   - 按一下右上角的&#x200B;**[!UICONTROL Save]**。

   - 若要檢視您商店中的產品，請在&#x200B;_管理員_ （ ![功能表箭頭](../assets/icon-menu-down-arrow-black.png) ）功能表上選擇&#x200B;**[!UICONTROL Customer View]**。

     該存放區會在新的瀏覽器標籤中開啟。

     ![客戶檢視](./assets/product-admin-customer-view.png){width="700" zoomable="yes"}

   **方法2：**&#x200B;儲存並關閉

   - 在&#x200B;_[!UICONTROL Save]_（![功能表箭頭](../assets/icon-menu-down-arrow-red.png){width="25"} ）功能表上，選擇&#x200B;**[!UICONTROL Save & Close]**。

## 步驟7：設定購物車縮圖（選用）

如果您對群組中的每個產品都有不同的影像，您可以設定為使用購物車縮圖的正確影像。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Sales]**&#x200B;並選擇&#x200B;**[!UICONTROL Checkout]**。

1. 展開&#x200B;**[!UICONTROL Shopping Cart]**&#x200B;的![擴充選擇器](../assets/icon-display-expand.png)。

   如需這些組態選項的詳細清單，請參閱&#x200B;_組態參考_&#x200B;中的[購物車](../configuration-reference/sales/checkout.md#shopping-cart)。

1. 將&#x200B;**[!UICONTROL Grouped Product Image]**&#x200B;設為`Product Thumbnail Itself`。

   ![購物車](./assets/config-sales-cart-grouped-product.png){width="600" zoomable="yes"}

   必要時，取消選取&#x200B;**[!UICONTROL Use system value]**&#x200B;核取方塊以設定此選項。

1. 按一下&#x200B;**[!UICONTROL Save Config]**。

## 注意事項

- 群組產品基本上是簡單關聯產品的集合。

- 分組的子產品可以是簡單、可下載或虛擬產品&#x200B;**[!UICONTROL without custom options]**。

- 每個購買的專案都會個別出現在購物車中，而不是群組的一部分。

- 群組的產品在目錄中沒有自己的價格。 群組產品價格衍生自群組中所包含個別產品的價格。

- 購物車中的縮圖影像可設定為顯示來自分組的父項產品或相關產品的影像。
