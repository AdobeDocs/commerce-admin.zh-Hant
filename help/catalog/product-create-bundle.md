---
title: 搭售產品
description: 瞭解如何建立套裝產品，讓購物者能夠在您的商店中建立自訂產品。
exl-id: dfa31eb8-2330-44eb-889b-5d10ce56ef13
feature: Catalog Management, Products
source-git-commit: e16fdc9f55cada17f82777fdaaaca44780c91e4b
workflow-type: tm+mt
source-wordcount: '1579'
ht-degree: 0%

---

# 搭售產品

組合是&#x200B;_建置您自己的_、可自訂的產品。 套件組合中的每個專案都可以以下列其中一種產品型別為基礎：

- [簡單產品](product-create-simple.md)
- [虛擬產品](product-create-virtual.md)

![套裝產品](./assets/product-bundle.png){width="700" zoomable="yes"}

當客戶按一下&#x200B;**[!UICONTROL Customize]**&#x200B;或&#x200B;**[!UICONTROL Add to Cart]**&#x200B;時，就會顯示選項。 由於套件中包含的產品不盡相同，因此SKU、價格和重量皆可設定為動態或固定值。

>[!NOTE]
>
>使用動態定價的套件組合產品無法使用最低廣告價格(MAP)。

>[!NOTE]
>
>父套裝產品一律自動顯示為其所有子產品的向上銷售產品。

如果[立即購買](../stores-purchase/checkout-instant-purchase.md)可用，組合中每個專案的&#x200B;_加入購物車_&#x200B;按鈕下方會出現&#x200B;_立即購買_&#x200B;按鈕。

![自訂組合](./assets/product-bundle-customize.png){width="600" zoomable="yes"}

下列指示會引導您使用[產品範本](attribute-sets.md)、必要欄位及基本設定來建立套件組合產品。 每個必要欄位都標有紅色星號(`*`)。 當您完成基本功能後，您可以視需要完成其他產品設定。

## 步驟1：選擇產品型別

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Products]**。

1. 在&#x200B;_[!UICONTROL Add Product]_（ ![功能表箭頭](../assets/icon-menu-down-arrow-red.png){width="25"} ）功能表的右上角，選擇&#x200B;**[!UICONTROL Bundle Product]**。

   ![新增組合產品](./assets/product-add-bundle.png){width="700" zoomable="yes"}

## 步驟2：選擇屬性集

若要選擇做為產品範本的[屬性集](attribute-sets.md)，請執行下列其中一項作業：

- 針對&#x200B;**[!UICONTROL Search]**，輸入屬性集的名稱，
- 在清單中，選擇要使用的屬性集。

表單會更新以反映變更。

![選擇範本](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## 步驟3：完成必要的設定

1. 輸入產品&#x200B;**[!UICONTROL Product Name]**。

1. 接受以產品名稱為基礎的預設&#x200B;**[!UICONTROL SKU]**&#x200B;或輸入不同的值。

   若要決定指定給每個組合專案的SKU型別，請執行下列步驟：

   - 藉由新增尾碼至預設SKU，可自動將&#x200B;**[!UICONTROL Dynamic SKU]**&#x200B;指派給每個組合專案。 預設為`Yes`。

   - 如果您偏好為每個套件組合專案指派唯一的SKU，請將&#x200B;**[!UICONTROL Dynamic SKU]**&#x200B;設為`No`。

   ![動態SKU與價格](./assets/product-bundle-manual-sku.png){width="600" zoomable="yes"}

1. 若要決定套裝的價格，請執行下列任一項作業：

   - 若要讓價格反映客戶選擇的選項，請將&#x200B;**[!UICONTROL Dynamic Price]**&#x200B;設為`Yes`並保留&#x200B;**[!UICONTROL Price]**&#x200B;空白。 在這種情況下，套裝產品在目錄中沒有自己的價格，而產品價格是從套裝中包含的個別產品的價格衍生而來的。

   - 若要對套件組合收取固定價格，請將&#x200B;**[!UICONTROL Dynamic Price]**&#x200B;設為`No`並輸入您要對套件組合收取的&#x200B;**[!UICONTROL Price]**。

   >[!NOTE]
   >
   >[!UICONTROL Special Price]與[!UICONTROL Customer Group Price] （層級價格）一律設為所有套件組合產品型別的折扣百分比。

1. 因為產品尚未準備好發佈，請將&#x200B;**[!UICONTROL Enable Product]**&#x200B;設定為`No`。

1. 按一下&#x200B;**[!UICONTROL Save]**&#x200B;並繼續。

   儲存產品時，[商店檢視](introduction.md#product-scope)選擇器會出現在左上角。

1. 選擇要提供產品的&#x200B;**[!UICONTROL Store View]**。

   ![選擇存放區檢視](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## 步驟4：完成基本設定

1. 如果套件組合有固定定價，請將&#x200B;**[!UICONTROL Tax Class]**&#x200B;設定為下列其中一項：

   - `None`
   - `Taxable Goods`

   如果組合具有「動態定價」，則針對&#x200B;**_每個_**&#x200B;組合專案決定稅捐。 如果組合具有固定定價，則針對&#x200B;**_整個_**&#x200B;組合產品決定稅捐。

1. 請注意下列事項：

   - **[!UICONTROL Quantity]**&#x200B;無法使用，因為每個組合專案的值都已確定。

   - 根據預設，**[!UICONTROL Stock Status]**&#x200B;設定為`In Stock`。

1. 若要決定束的重量，請執行下列任一項作業：

   - 若要讓權重反映客戶選擇的選項，請設定&#x200B;**[!UICONTROL Dynamic Weight]**&#x200B;設定`Yes`並保留&#x200B;**[!UICONTROL Weight]**&#x200B;空白。

   - 若要指派固定權重給組合，請將&#x200B;**[!UICONTROL Dynamic Weight]**&#x200B;設定為`No`並輸入組合的&#x200B;**[!UICONTROL Weight]**。

   ![動態加權](./assets/product-bundle-dynamic-weight.png){width="600" zoomable="yes"}

1. 若要在[新產品](../content-design/widget-new-products-list.md)的清單中新增產品，請選取&#x200B;**[!UICONTROL Set Product as New]**&#x200B;核取方塊。

1. 接受`Catalog, Search`的預設&#x200B;**[!UICONTROL Visibility]**&#x200B;設定。

1. 若要將&#x200B;_[!UICONTROL Categories]_指派給產品，請按一下&#x200B;**[!UICONTROL Select…]**方塊並執行下列任一動作：

   **選擇現有類別：**

   - 開始在方塊中輸入內容，直到找到相符專案為止。

   - 選取要指派的每個類別的核取方塊。

   ![選取套件組合產品的一或多個類別](./assets/product-create-categories.png){width="600" zoomable="yes"}

   **建立類別：**

   - 按一下&#x200B;**[!UICONTROL New Category]**。

   - 輸入&#x200B;**[!UICONTROL Category Name]**&#x200B;並選擇&#x200B;**[!UICONTROL Parent Category]**，這會決定其在功能表結構中的位置。

   - 按一下&#x200B;**[!UICONTROL Create Category]**。

1. 選擇&#x200B;**[!UICONTROL Country of Manufacture]**。

   可能有其他屬性可說明產品。 選取範圍會改變屬性集，您稍後可以完成它們。

## 步驟5：新增束專案

_[!UICONTROL Bundle Items]_區段用於將專案新增至組合產品型別，並編輯目前選擇的專案。

為產品](./assets/product-bundle-items-ball.png){width="600" zoomable="yes"}定義的![套件組合專案

1. 向下捲動至&#x200B;_組合專案_&#x200B;區段，並將&#x200B;**[!UICONTROL Ship Bundle Items]**&#x200B;設定為下列其中一項：

   - `Separately`
   - `Together`

   如果您選取`Together`，所有組合專案都必須指派相同的[來源](../inventory-management/sources-manage.md)。

1. 按一下&#x200B;**[!UICONTROL Add Option]**&#x200B;並執行下列動作：

   - 輸入要做為欄位標籤的&#x200B;**[!UICONTROL Option Title]**。

   - 將&#x200B;**[!UICONTROL Input Type]**&#x200B;設定為下列其中一項：

      - `Drop-down`
      - `Radio buttons`
      - `Checkbox`
      - `Multiple Select`

   - 若要讓欄位成為必要專案，請選取&#x200B;**[!UICONTROL Required]**&#x200B;核取方塊。

   - 按一下「**[!UICONTROL Add Products to Option]**」，然後選取每個要包含在此選項中的產品核取方塊。

     如果有多種產品，請使用清單篩選器和分頁控制來尋找您需要的產品。

   - 按一下&#x200B;**[!UICONTROL Add Selected Products]**。

     ![新增選取的產品](./assets/product-bundle-add-products-to-option.png){width="600" zoomable="yes"}

   - 專案出現在&#x200B;_選項_&#x200B;區段之後，請選擇專案作為&#x200B;**[!UICONTROL Default]**&#x200B;選取專案。

   - 在&#x200B;_預設數量_&#x200B;欄中，輸入當客戶選擇專案時，要新增至組合的每個專案數量。

   - 若要允許客戶變更套件組合專案的數量，請選取&#x200B;**[!UICONTROL User Defined]**。


     >[!NOTE]
     >
     >量值可以是預設值或使用者定義的值。 但是，請勿將&#x200B;_[!UICONTROL User Defined]_屬性指派給核取方塊或多選輸入型別。

     依預設，客戶無法變更包含在套件專案中的「預設數量」。 但是，客戶可以輸入要包含在套件中的料號數量。

     例如，如果Sprite Status Ball的「預設數量」設定為`2`，而客戶訂購該組合選項的`4`，則購買的總球數為`8`。

     ![專案詳細資料](./assets/product-bundle-item-detail.png){width="600" zoomable="yes"}

1. 對要新增至束的每個專案重複這些步驟。

1. 若要變更組合區段中專案的順序，請按一下列開頭的&#x200B;_移動_ （![移動圖示](../assets/icon-move.png) ）圖示，並將專案拖曳至位置。

   ![變更組合專案的順序](./assets/product-bundle-items-move.png){width="600" zoomable="yes"}

   也可以在匯出的組合產品資料中變更專案順序，然後重新匯入到目錄中。 如需詳細資訊，請參閱[匯入套件組合產品](../systems/data-transfer-bundle-products.md)。

   若要更清楚地檢視工作區，請先收合每個區段，然後將它們拖曳到適當位置。

1. 若要從套件組合移除任何專案，請按一下&#x200B;**[!UICONTROL Delete]** （ ![垃圾桶圖示](../assets/icon-delete-trashcan.png) ）圖示。

1. 完成時，按一下&#x200B;**[!UICONTROL Save]**。

## 步驟6：完成產品資訊

視需要向下捲動並填入下列章節中的資訊：

- [內容](product-content.md)
- [影像和影片](product-images-and-video.md)
- [搜尋引擎最佳化](product-search-engine-optimization.md)
- [相關產品、向上銷售和交叉銷售](related-products-up-sells-cross-sells.md)
- [可自訂的選項](settings-advanced-custom-options.md)
- [網站中的產品](settings-basic-websites.md)
- [設計](settings-advanced-design.md)
- [贈品選項](product-gift-options.md)

## 步驟7：Publish產品

1. 如果您已準備好在目錄中發佈產品，請將&#x200B;**[!UICONTROL Enable Product]**&#x200B;設定為`Yes` （ ![切換是](../assets/toggle-yes.png) ）。

1. 執行下列任一項作業：

   **方法1：**&#x200B;儲存並預覽

   - 按一下右上角的&#x200B;**[!UICONTROL Save]**。

   - 若要檢視您商店中的產品，請在&#x200B;_管理員_ （ ![功能表箭頭](../assets/icon-menu-down-arrow-black.png) ）功能表上選擇&#x200B;**[!UICONTROL Customer View]**。

     該存放區會在新的瀏覽器標籤中開啟。

   ![客戶檢視](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   **方法2：**&#x200B;儲存並關閉

   在&#x200B;_[!UICONTROL Save]_（![功能表箭頭](../assets/icon-menu-down-arrow-red.png){width="25"} ）功能表上，選擇&#x200B;**[!UICONTROL Save & Close]**。

## 輸入控制項

| 控制 | 說明 | 範例 |
|--- |--- |--- |
| [!UICONTROL Drop-down] | 顯示包含產品名稱和價格的選項下拉式清單。 只能選取一個專案。 | ![下拉式清單](./assets/product-bundle-input-type-drop-down.png){width="200"} |
| [!UICONTROL Radio Buttons] | 顯示每個選項的單選按鈕，其後加上產品名稱和價格。 只能選取一個專案。 | ![選項按鈕](./assets/product-bundle-input-type-radio-buttons.png){width="200"} |
| [!UICONTROL Checkbox] | 顯示每個選項的核取方塊，然後是產品名稱和價格。 可選取多個專案。 | ![核取方塊](./assets/product-bundle-input-type-checkbox.png){width="200"} |
| [!UICONTROL Multiple Select] | 顯示選項清單以及產品名稱和價格。 若要選取多個專案，請按住Ctrl鍵(PC)或Command鍵(Mac)，然後按一下每個專案。 | ![多重選取](./assets/product-bundle-input-type-multiple-select.png){width="200"} |

{style="table-layout:auto"}

## 欄位說明

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL SKU] | 決定每個專案是否被指派變數或動態SKU，或者是否使用固定SKU作為搭配。 選項： `Fixed` / `Dynamic` |
| [!UICONTROL Weight] | 指定加權是根據所選專案計算，還是整個束的固定加權。 選項： `Fixed` / `Dynamic` |
| [!UICONTROL Price View] | 決定產品價格是否顯示為範圍，從最便宜到最昂貴（價格範圍）或顯示最便宜（最低）。 選項： `Price Range` / `As Low As` |
| 出貨套件組合專案 | 指定個別料號是否可單獨出貨。 |

{style="table-layout:auto"}

## 組合產品庫存狀態

當下列任一情況發生時，套裝產品庫存狀態為&#x200B;**_自動變更為無庫存_**：

- 所有選項都是選擇性的，而且所有關聯的產品都是&#x200B;_缺貨_。

- 需要某些選項，且與任何必要選項相關聯的產品為&#x200B;_無庫存_。

當下列任一情況發生時，組合產品庫存狀態為&#x200B;**_未自動變更為缺貨_**：

- 所有選項都是選擇性的，而且至少有一個相關產品為&#x200B;_庫存中_。

- 需要一些選項，每個必要選項中至少有一個相關產品為&#x200B;_庫存_。

## 注意事項

![核取方塊](../assets/checkbox.png)客戶可以&#x200B;_建置自己的_&#x200B;套件組合產品。

![核取方塊](../assets/checkbox.png)套件組合專案可以是簡單或沒有自訂選項的虛擬產品。

![核取方塊](../assets/checkbox.png)價格檢視可設為`Price Range`或`As Low As`。

![核取方塊](../assets/checkbox.png) SKU和權重可以是`Fixed`或`Dynamic`。

![核取方塊](../assets/checkbox.png)數量可以是預設集或使用者定義的值。 但是，請勿將&#x200B;_[!UICONTROL User Defined]_屬性指派給核取方塊或多選輸入型別。

![核取方塊](../assets/checkbox.png)套件組合專案可以一起或單獨出貨。

![核取方塊](../assets/checkbox.png)父套裝產品一律自動顯示為其所有子產品的追加銷售產品。

![核取方塊](../assets/checkbox.png) [!UICONTROL Special Price]與[!UICONTROL Customer Group Price] （層級價格）一律設為所有套件組合產品型別的折扣百分比。
