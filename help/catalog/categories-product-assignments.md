---
title: 類別產品指派
description: 瞭解如何使用[!UICONTROL Products in Category]設定來控制目前指派給類別的產品。
exl-id: e7ab11c0-2d55-4824-a397-a1c858344d4f
feature: Catalog Management, Categories, Products
source-git-commit: 5aea3aa13ab0eb74866fc0cbcbfe08b5099abe95
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 0%

---

# 類別產品指派

若為類別，請使用&#x200B;_[!UICONTROL Products in Category]_區段來檢閱目前指派給類別的產品。 每欄頂端的搜尋篩選器是用來新增和移除類別中的產品。 您也可以使用[類別規則](../merchandising-promotions/category-product-rules.md) (僅限![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce)在滿足一組條件時動態變更產品選擇。 若要深入瞭解，請參閱[Visual Merchandiser](../merchandising-promotions/visual-merchandiser.md)。

>[!TIP]
>
>在類別規則設定期間，儲存此類別時，產品為&#x200B;_已排序_、_相符_、_已指派_&#x200B;及&#x200B;_已取消指派_ （僅根據規則&#x200B;**__**）。 為了確保將新產品新增至目錄時，能根據規則指派產品，您&#x200B;**必須重新儲存每個設定為依規則比對產品的類別**。 此外，如果任何產品庫存狀態變更為`In Stock`或`Out of Stock`，且類別中的產品已根據&#x200B;_自動排序_&#x200B;規則&#x200B;**排序**，您必須按一下&#x200B;**[!UICONTROL Save Category]**。

![類別產品](./assets/category-products-in-category.png){width="600" zoomable="yes"}

>[!NOTE]
>
>_Stock_&#x200B;欄僅顯示&#x200B;_**選取的類別範圍**_&#x200B;的可用產品數量。 當針對產品管理多個庫存時，您應在對應的範圍之間切換，以在&#x200B;_類別產品_&#x200B;格線中顯示其他&#x200B;_庫存_&#x200B;欄值。

## 套用類別規則

{{ee-feature}}

1. 將&#x200B;**[!UICONTROL Match products by rule]**&#x200B;設為`Yes`。

   自動排序和條件選項隨即顯示。

   ![依規則比對產品](./assets/category-match-products-by-rule.png){width="600" zoomable="yes"}

1. 設定&#x200B;**[!UICONTROL Automatic Sorting]**&#x200B;順序。

   此自動排序是根據目前狀況。

   - `Stock level` — 移至頂端或底部。
   - `Special price` — 移至頂端或底部。
   - `New Products` — 先列出最新的產品。
   - `Color` — 依色彩的字母順序排序。
   - `Name` — 依名稱以遞增或遞減順序排序。
   - `SKU` — 依SKU以遞增或遞減順序排序
   - `Price` — 依價格以遞增或遞減順序排序。

1. 按一下&#x200B;**[!UICONTROL Add Condition]**&#x200B;並執行下列動作：

   - 選擇條件基礎的&#x200B;**[!UICONTROL Attribute]**。
   - 選擇組成運算式所需的&#x200B;**[!UICONTROL Operator]**。
   - 輸入要比對的&#x200B;**[!UICONTROL Value]**。

   ![新增條件至類別規則](./assets/category-rule-create.png){width="600" zoomable="yes"}

   對每個要用來描述要滿足的條件的屬性重複此程式。 例如，若要比對在7到30天前建立的產品，請執行下列動作：

   - 將&#x200B;**[!UICONTROL Date Created]**&#x200B;設為`Less than 30`。
   - 將&#x200B;**[!UICONTROL Logic]**&#x200B;設為`AND`。
   - 將&#x200B;**[!UICONTROL Date Modified]**&#x200B;設為`Greater than 7`。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Category]**。

### 頁面選項

| 選項 | 說明 |
|--- |--- |
| [!UICONTROL Match products by rule] | 決定類別中的產品清單是否由類別規則動態產生。 選項： `Yes` / `No` |
| [!UICONTROL Automatic Sorting] | 自動將排序順序套用至類別產品清單。 選項： <br/>`None`<br/>`Move low stock to top`<br/>`Move low stock to bottom`<br/>`Special price to top`<br/>`Special price to bottom`<br/>`Newest products first`<br/>`Sort by color`<br/>`Name: A - Z`<br/>`Name: Z - A`<br/>`SKU: Ascending`<br/>`SKU: Descending`<br/>`Price: High to Low`<br/>`Price: Low to High` |
| [!UICONTROL Add Condition] | 將另一個條件新增至規則。 |

{style="table-layout:auto"}

### 頁面條件

| 選項 | 說明 |
|--- |--- |
| [!UICONTROL Attribute] | 決定作為條件基礎的屬性。 選項： <br/>**[!UICONTROL Clone Category ID(s)]**— 根據類別ID動態地複製多個類別中的產品，而不需要排序和順序。<br/>**[!UICONTROL Color]** — 包含以顏色為準的產品。 <br/>**[!UICONTROL Date Created (days ago)]**— 包含以產品加入目錄後的天數為基礎的產品。<br/>**[!UICONTROL Date Modified (days ago)]** — 包含以上次修改產品後的天數為基礎的產品。 <br/>**[!UICONTROL Name]**— 包含以產品名稱為依據的產品。<br/>**[!UICONTROL Price]** — 包含以價格為準的產品。 <br/>**[!UICONTROL Quantity]**— 包含以庫存數量為基準的產品。<br/>** SKU **— 包含以SKU為基礎的產品。 |
| [!UICONTROL Operator] | 指定套用至屬性值以符合條件的運運算元。 除非指定運運算元，否則會使用`Equal`作為預設值。 選項： `Equal` / `Not equal` / `Greater than` / `Greater than or equal to` / `Less than` / `Less than or equal to` / `Contains` |
| [!UICONTROL Value] | 指定屬性必須符合條件的值。 |
| [!UICONTROL Logic] | 用於定義多個條件，且僅在新增其他條件時顯示。 選項： `OR` / `AND` |

{style="table-layout:auto"}

>[!NOTE]
>
>可設定產品及其子項選項的數量是透過結合所有子項產品數量來計算。 請考量可設定產品&#x200B;_耐力健身背心_&#x200B;的範例，其顏色選項為紫色、紅色和黃色，且每種選項數量不同。 在此案例中，上階產品數量是紫色、紅色和黃色下階產品的合併數量。

## 控制項


## 頁面控制項

{{ee-feature}}

| 控制 | 說明 |
|----------|--------------|
| ![以清單檢視](../assets/icon-view-list.png) | 以清單檢視 |
| ![以圖磚檢視](../assets/icon-view-tiles.png) | 以圖磚檢視 |
| ![切換否](../assets/toggle-no.png) | 依規則比對 — 否 |
| ![切換是](../assets/toggle-yes.png) | 依規則比對 — 是 |
| ![移動控制器](../assets/icon-move.png) | 拖放控制項可讓您抓取產品，並將其移至格線目前頁面中的另一個位置。 若要深入瞭解，請參閱[視覺化銷售工具](../merchandising-promotions/visual-merchandiser.md)。 |
| ![位置控制器](../assets/control-position.png) | 決定產品在清單中的位置。 |

{style="table-layout:auto"}

## 頁面控制項

{{ce-feature}}

| 控制 | 說明 |
|----------|--------------|
| ![已選取核取方塊](../assets/checkbox-selected.png) | 使用第一欄標題中的核取方塊，以選取所有產品或清除所有選取專案。 第一列中的控制項決定搜尋型別，並可設定為包含任何記錄，或僅包含已指定或未指定給類別的記錄。 每一列第一欄中的核取方塊可識別要新增至類別的產品。 選項： `Yes` / `No` / `Any` |
| [!UICONTROL Search Filters] | 每欄頂端的篩選控制項可用於輸入您想要在清單中包含或省略的特定值，視「選取全部」設定而定。 |
| [!UICONTROL Reset Filter] | 清除所有搜尋篩選器。 |
| [!UICONTROL Search] | 根據篩選條件搜尋目錄並顯示結果。 |

{style="table-layout:auto"}
