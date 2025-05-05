---
title: 產品清單
description: 瞭解Admin中的_[!UICONTROL Products]_頁面，您可在此建立產品並編輯現有產品。
exl-id: 47e14f72-017f-456a-8904-6d32ef47e6f1
feature: Catalog Management, Products, Admin Workspace
source-git-commit: 8bb91b80f8ba957676c654e984deb5704b777612
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 0%

---

# 產品清單

目錄中的所有產品都可從「管理員」的&#x200B;_[!UICONTROL Products]_&#x200B;頁面存取，您可在此建立產品並編輯現有產品。 針對多網站安裝，每個網站都可從相同目錄提供不同產品選項，以供銷售。

_[!UICONTROL Products]_&#x200B;清單包含目錄中的所有產品、指出可供使用的網站，以及是否目前啟用銷售這些產品。 在啟用[共用目錄](../b2b/catalog-shared.md)的Adobe Commerce B2B安裝中，網格包含一欄，指出哪些產品在共用目錄中具有替代折扣定價。

您可以逐頁瀏覽清單頁面，或搜尋特定產品。 使用標準[控制項](../getting-started/admin-grid-controls.md)來排序及篩選清單，並將[動作](../getting-started/admin-actions-control.md)套用至選取的產品。

![產品格線](./assets/products-grid.png){width="700" zoomable="yes"}

## 限制產品顯示

若要改善大型型錄的效能，建議您限制格線中顯示的產品數目。 您可以限制下列專案顯示的產品格線：

- 產品頁面
- 新增相關/向上銷售/交叉銷售產品
- 將產品新增至套件組合產品
- 新增產品至群組產品
- 建立訂單（管理員）

預設會停用此產品顯示限制的組態設定。 一旦啟用，您就可以將格線中的產品數量限製為特定值。 如果已啟用，且網格顯示的相符產品數量大於記錄限制，則會傳回有限的記錄集合。 當達到限制時，找到的記錄總數、選取的記錄數以及分頁元素不會出現在網格標頭中。

>[!NOTE]
>
>如果您不希望產品格線受到限制，請更精確地使用篩選器，以產生專案數少於&#x200B;_[!UICONTROL Records Limit]_&#x200B;欄位中所指定數目的集合。

**_若要設定產品顯示限制：_**

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 展開&#x200B;**[!UICONTROL Advanced]**&#x200B;並選擇&#x200B;**[!UICONTROL Admin]**。

1. 展開![展開選取器](../assets/icon-display-expand.png) **[!UICONTROL Admin Grids]**&#x200B;區段，然後執行下列動作：

   - 將&#x200B;**[!UICONTROL Limit Number of Products in Grid]**&#x200B;設為`Yes`。

   - （選擇性）在&#x200B;**[!UICONTROL Records Limit]**&#x200B;欄位中輸入值，將格線中的產品數目限製為特定值。 預設最小值為`20000`。

   ![管理網格組態設定](../configuration-reference/advanced/assets/admin-admin-grids.png){width="600" zoomable="yes"}

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

## 頁面控制項

| 控制 | 說明 |
|--- |--- |
| [!UICONTROL Add Product] | 啟動程式以建立新的簡單產品。 若要選擇特定產品型別，請按一下向下箭頭。 選項： [[!UICONTROL Simple Product]](product-create-simple.md) / [[!UICONTROL Configurable Product]](product-create-configurable.md) / [[!UICONTROL Grouped Product]](product-create-grouped.md) / [[!UICONTROL Virtual Product]](product-create-virtual.md) / [[!UICONTROL Bundle Product]](product-create-bundle.md) / [[!UICONTROL Downloadable Product]](product-create-downloadable.md) / [[!UICONTROL Gift Card]](product-gift-card-create.md) |
| [!UICONTROL Actions] | 列出所有可套用至清單中所選產品的動作。 若要將動作套用至產品或產品群組，請選取每個產品第一欄中的核取方塊。 選項： `Delete` / `Change Status` / `Update Attributes` / `Assign Inventory Source` / `Unassign Inventory Source` / `Transfer Inventory To Source` |
| [!UICONTROL Filters] | 根據目前的篩選器起始目錄搜尋。 |
| [!UICONTROL Default View] | 表示目前的格線欄配置。 如果有已儲存的格點欄檢視，您可以選擇其他檢視。 |
| [!UICONTROL Columns] | 列出所有可套用至清單中所選產品的動作。 若要將動作套用至產品或產品群組，請選取每個產品第一欄中的核取方塊。 |
| [!UICONTROL Search by keyword] | 左上角的搜尋方塊是用來依關鍵字尋找產品。 |
| [!UICONTROL Edit] | 以編輯模式開啟產品。 您可以按一下列上的任何位置，完成相同工作。 |

{style="table-layout:auto"}

## 預設欄

| 欄 | 說明 |
|--- |--- |
| （核取方塊） | 選取要接受動作的多個記錄。 每個選定記錄的第一欄中的核取方塊都會標示。 選項： <br/>**[!UICONTROL Select All]**— 選取找到的所有符合目前篩選設定的記錄。<br/>**[!UICONTROL Select All on This Page]** — 僅選取在目前頁面上找到的符合篩選器設定的記錄。 |
| [!UICONTROL ID] | 首次儲存新產品時指派的唯一循序編號。 |
| [!UICONTROL Thumbnail] | 顯示主要產品影像的縮圖。 |
| [!UICONTROL Name] | 產品名稱。 |
| [!UICONTROL Type] | 產品型別。 |
| [!UICONTROL Attribute Set] | 用作產品範本的屬性集名稱。 |
| [!UICONTROL SKU] | 指定給產品的唯一庫存單位。 |
| [!UICONTROL Price] | 產品的單價。 |
| [!UICONTROL Quantity] | 有庫存的數量。 |
| [!UICONTROL Salable Quantity] | 此產品所有可用單位的總和。 |
| [!UICONTROL Visibility] | 表示產品在目錄中的可見位置。 選項： `Not Visible Individually` / `Catalog` / `Search` / `Catalog, Search` |
| [!UICONTROL Status] | 表示產品的狀態。 選項： `Enabled`和`Disabled` |
| [!UICONTROL Websites] | 表示產品可用的網站。 |
| [!UICONTROL Action] | 以編輯模式開啟產品。 |
| [!UICONTROL Shared Catalog] | ![Adobe Commerce B2B](../assets/b2b.svg) (僅適用於[Adobe Commerce B2B](./b2b/../introduction.md))表示包含產品自訂定價的共用目錄。 |

{style="table-layout:auto"}

## 其他欄

| 欄 | 說明 |
|--- |--- |
| [!UICONTROL Short Description] | 產品的簡短說明。 |
| [!UICONTROL Special Price From Date] | 特殊價格促銷的第一個日期。 |
| [!UICONTROL Special Price To Date] | 特殊價格促銷的最後日期。 |
| [!UICONTROL Cost] | 料號的實際成本。 |
| [!UICONTROL Manufacturer] | 產品的製造商。 |
| [!UICONTROL Meta Keywords] | 產品的中繼關鍵字。 |
| [!UICONTROL Color] | 產品顏色。 |
| [!UICONTROL Set Product as New from Date] | 將產品設為新促銷活動的第一個日期。 |
| [!UICONTROL Set Product as New to Date] | 將產品設定為新促銷活動的最後日期。 |
| [!UICONTROL Active From / To] | 產品的開始和結束日期。 |
| [!UICONTROL Layout] | 產品版面。 |
| [!UICONTROL Minimum Advertised Price] | 產品的最低廣告價格。 |
| [!UICONTROL Allow Gift Message] | 給購買禮品卡之客戶的禮品訊息。 |
| [!UICONTROL Special Price] | 產品的特殊價格。 |
| [!UICONTROL Weight] | 產品重量。 |
| [!UICONTROL Meta Title] | 產品的中繼標題。 |
| [!UICONTROL Meta Description] | 產品中繼資料說明。 |
| [!UICONTROL Country of Manufacture] | 製造國家。 |
| [!UICONTROL New Theme] | 已將自訂主題套用至產品。 |
| [!UICONTROL URL Key] | 產品的URL索引鍵。 |
| [!UICONTROL Tax Class] | 產品稅捐類別。 |
| [!UICONTROL Allow Gift Message] | 顯示產品之贈品訊息選項的可用性。 |

{style="table-layout:auto"}
