---
title: Visual Merchandiser概述
description: 瞭解Visual Merchandiser工具，其可讓您定位產品並決定哪些產品會出現在類別清單中。
exl-id: 00fe8b7f-0c33-4f06-a3cd-1f0bd18079f1
feature: Categories, Merchandising, Products
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# Visual Merchandiser

{{ee-feature}}

_Visual Merchandiser_&#x200B;是一組進階工具，可讓您定位產品並套用條件，以決定哪些產品會出現在類別清單中。 結果可能是動態選取可根據目錄變更調整的產品。 您可以在&#x200B;_視覺模式_&#x200B;中工作，這會在格線上將每個產品顯示為圖磚，或是從類別中的產品清單中工作。 每個模式中都有相同的工具，您可以使用右上角的按鈕，在各種顯示型別之間切換。

![圖磚檢視中的類別產品](./assets/category-products-visual-with-stock.png){width="600" zoomable="yes"}

## 存取Visual Merchandiser

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Categories]**。

1. 在類別樹狀結構中向下展開，然後按一下您要編輯的類別。

1. 向下捲動並展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Products in Category]**&#x200B;區段。

1. 按一下「_以圖磚檢視_」（「![以圖磚檢視](../assets/icon-view-tiles.png)」）按鈕，將產品顯示為格線。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Category]**。

## 變更產品的位置

1. 使用[排序順序](../catalog/navigation-product-listings.md)檢視您要移動的產品。

   - **方法1：拖放**

     抓取產品圖磚右上角的&#x200B;_拖曳_ （![拖曳圖示](../assets/icon-move.png)）控制項，並將產品放置到適當位置。 每項產品的數量會調整以反映新位置。

   - **方法2：設定位置值**

     在產品圖磚上的&#x200B;_位置_&#x200B;控制器（![位置欄位](../assets/control-position.png)）中，輸入您要產品出現的號碼。 輸入`0`將產品放在清單頂端。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Category]**。

>[!NOTE]
>
>在全新安裝中，Adobe Commerce會為預設存放區的根目錄保留類別識別碼`2`。 Visual Merchandiser只能使用識別碼編號為`3`或以上的類別。

## Workspace控制項

| 控制 | 說明 |
|--- |--- |
| ![檢視清單圖示](../assets/icon-view-list.png) | 以清單檢視 |
| ![以圖磚圖示檢視](../assets/icon-view-tiles.png) | 以圖磚檢視 |
| ![依規則比對 — 否](../assets/toggle-no.png) | 依規則比對 — 否 |
| ![依規則比對 — 是](../assets/toggle-yes.png) | 依規則比對 — 是 |
| ![移動圖示](../assets/icon-move.png) | 拖曳 |
| ![位置控制器](../assets/control-position.png) | 位置 |
| ![從類別圖示移除](../assets/icon-delete-x.png) | 從類別中移除 |
| 每個頁面控制項的![個專案](../assets/control-items-per-page.png) | 每頁檢視次數 |
| ![變更頁面顯示](../assets/control-page-display.png) | 移至下一個/上一個 |

{style="table-layout:auto"}
