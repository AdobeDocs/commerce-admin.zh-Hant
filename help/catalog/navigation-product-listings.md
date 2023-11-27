---
title: 產品清單
description: 瞭解如何修改產品清單設定（這會決定每個頁面要顯示多少產品），以及使用哪個屬性來排序清單。
exl-id: 3779d9db-4adb-473b-b9c9-ad066f50b549
feature: Catalog Management, Products, Page Content
source-git-commit: 7ae9955b0283cb7bcd757e7b45fdbc4c3b2181ca
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 1%

---

# 產品清單

產品清單可設定為預設顯示為清單或格線。 您也可以決定每頁要顯示多少產品，以及使用哪個屬性來排序清單。 產品清單包含一組控制項，可用於排序產品、變更清單格式、依屬性排序以及從一個頁面前進到下一個頁面。

>[!NOTE]
>
>依產品屬性排序類別時，具有相同屬性值的產品也會依其屬性排序 _[!UICONTROL Product ID]_以遞增順序顯示。

![顯示為格線的產品](./assets/storefront-catalog-page.png){width="700" zoomable="yes"}

## 設定產品清單

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Catalog]** 並選擇 **[!UICONTROL Catalog]** 底下。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Storefront]** 區段。

   ![店面組態選項](../configuration-reference/catalog/assets/catalog-storefront.png){width="600" zoomable="yes"}

   如需這些選項的詳細清單，請參閱 [店面](../configuration-reference/catalog/catalog.md#storefront) 在 _設定參考_.

   >[!NOTE]
   >
   >若要正確顯示產品及其價格，請依 _依價格排序產品_，請確定價格的設定會顯示在 [銷售稅組態](../configuration-reference/sales/tax.md) 有相同的值(`Excluding Tax` **或** `Including Tax`)。 對於 _[!UICONTROL Calculation Settings]_，檢查&#x200B;**[!UICONTROL Catalog Prices]**值。 和_[!UICONTROL Price Display Settings]_，檢查 **[!UICONTROL Display Product Prices in Catalog]** 值。 如果這些值不同，分層導覽中的價格篩選器可能無法正確依價格篩選及排序產品。

1. 設定預設值 **[!UICONTROL List Mode]** 變更為下列其中一項：

   - `Grid Only`
   - `List Only`
   - `Grid (default) / List`
   - `List (default / Grid`

1. 的 **[!UICONTROL Products per Page on Grid Allowed Values]**，輸入以格線格式顯示時每頁顯示的產品數目。

   若要輸入值的選取範圍，請以逗號分隔每個數字。

1. 的 **[!UICONTROL Products per Page on Grid Default Value]**，輸入預設每頁顯示在格線中的產品數量。

1. 的 **[!UICONTROL Products per Page on List Allowed Values]**，輸入您要在每個頁面上以清單格式顯示的產品數量。

   若要輸入值的選取範圍，請以逗號分隔每個數字。

1. 的 **[!UICONTROL Products per page on List Default Value]**，輸入每頁出現在清單中的預設產品數量。

1. 設定 **[!UICONTROL Product Listing Sorted by]** 預設屬性，最初用於排序清單。

1. 若要讓客戶選擇列出所有產品，請設定 **[!UICONTROL Allow All Products on Page]** 至 `Yes`.

1. 如果要在客戶瀏覽目錄清單時保留所有分頁設定，請設定 **[!UICONTROL Remember Category Pagination]** 至 `Yes`.

   啟用此設定可確保當購物者從一個類別瀏覽到另一個類別時，在清單或格線中顯示的產品數量會保留。 依預設，此欄位設為 `No` 因為它使用更多快取儲存空間，而且可能會影響搜尋引擎為頁面編制索引的方式。

1. 若使用 [平面目錄](catalog-flat.md) (**不建議**)，請執行以下操作：

   - 若要顯示產品的平面分類清單，請設定 **[!UICONTROL Use Flat Catalog Category]** 至 `Yes`.

   - 若要顯示平面產品清單，請設定 **[!UICONTROL Use Flat Catalog Product]** 至 `Yes`.

1. 如果您想要允許類別和產品URL中的媒體資產動態參考，請設定 **[!UICONTROL Allow Dynamic Media URLs in Products and Categories]** 至 `Yes`.

1. 完成後，按一下 **[!UICONTROL Save Config]**.

## 頁面控制項

| 控制 | 說明 |
|--- |--- |
| [!UICONTROL View As] | 以格線或清單格式顯示產品。 |
| [!UICONTROL Sort By] | 變更清單的排序順序。 |
| [!UICONTROL Show Per Page] | 決定每頁顯示多少產品。 |
| 分頁連結 | 導覽連結至其他頁面。 |

{style="table-layout:auto"}

## 分頁控制項

分頁設定會顯示在清單的頂端和底部，並控制產品清單分頁連結的格式。 您可以設定顯示在控制項中的連結數目，以及設定下一個和上一個連結。 為了顯示分頁連結，清單中的產品數量必須超過產品清單設定中每頁允許的數量。

![分頁控制項](./assets/storefront-pagination-controls.png){width="700" zoomable="yes"}

### 店面分頁控制項

| 控制 | 說明 |
|--- |--- |
| ![顯示格線](./assets/controls-pagination-list-grid.png) | [!UICONTROL View As]  — 以「格線」或「清單」格式顯示清單。 |
| ![排序依據：](./assets/control-pagination-sort-by.png) | [!UICONTROL Sort By]  — 變更清單的排序順序。 此 _[!UICONTROL Used for Sorting in Product Listing]_storefront屬性決定 [產品屬性](../catalog/product-attributes.md) 可用來排序清單。 |
| ![每頁顯示](./assets/control-pagination-show-per-page.png) | [!UICONTROL Show Per Page]  — 決定每頁要顯示多少產品。 |
| ![分頁連結](./assets/control-pagination.png) | 分頁連結 — 導覽連結至其他頁面。 |

{:style=&quot;table-layout:auto&quot;}

### 設定分頁控制項

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. 尋找您要設定的商店檢視，並前往 **[!UICONTROL Action]** 欄，按一下 **[!UICONTROL Edit]**.

1. 在 **[!UICONTROL Other Settings]**，展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Pagination]** 區段。

   ![分頁](./assets/config-design-pagination.png){width="600" zoomable="yes"}

   如需這些設定的詳細資訊，請參閱 [設計組態](../content-design/configuration.md).

1. 的 **[!UICONTROL Pagination Frame]**，輸入您要顯示在分頁控制項中的連結數。

1. 的 **[!UICONTROL Pagination Frame Skip]**，輸入要在分頁控制項中顯示下一組連結前略過的連結數。

   例如，如果分頁框架有五個連結，而您想要跳至下五個連結，您想跳至多少個連結？ 如果您將值設定為四(`4`)，前一個集合的最後一個連結是下一個集合的第一個連結。

1. 的 **[!UICONTROL Anchor Text for Previous]**，輸入您想在上一個連結中顯示的文字。

   留空將使用預設箭頭。

1. 的 **[!UICONTROL Anchor Text for Next]**，輸入您要在下一個連結中顯示的文字。 留空將使用預設箭頭。

1. 完成後，按一下 **[!UICONTROL Save Configuration]**.
