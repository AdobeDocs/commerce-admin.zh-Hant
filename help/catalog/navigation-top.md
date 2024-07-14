---
title: 頂端導覽
description: 瞭解如何定義存放區的主要功能表，其功能類似於不同部門的目錄。
exl-id: 8b71fe73-2716-4820-9e57-4cb1e6888132
feature: Catalog Management, Categories, Site Navigation
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 0%

---

# 頂端導覽

商店的主功能表就像商店中不同部門的目錄。 每個選項代表不同的產品類別。 上層導覽的位置和呈現方式可能依主題而異，但其運作方式基本上相同。

![上層導覽](./assets/storefront-top-navigation.png){width="700" zoomable="yes"}

目錄的類別結構會影響搜尋引擎為您的網站編制索引的效果。 類別巢狀結構越深，就越不可能完全編列索引。 一般而言，使用一到三個可見層級是最有效率。 [根類別](category-root.md)雖然未出現在功能表中，但會計為第一級。 頂端導覽中可用的層級數目上限取決於設定。 此外，您的商店主題支援的功能表層級數目可能有所限制。 例如，範例Luma主題支援最多五個層級，包括根。

## 計算功能表層級

| 專案 | 說明 |
|--- |--- |
| 第1級 | 第一個層級是根類別，在範例資料中將其命名為「預設類別」。 根是功能表的容器，其名稱在功能表中不會顯示為選項。 |
| 第2級 | 在案頭顯示器上，頂端導覽是出現在頁面頂端的主要功能表。 在行動裝置上，主功能表通常會以彈出選單的形式顯示。 Luma商店中的第二層級選項為&#x200B;_新增功能_、_女性_、_男性_、_齒輪_、_訓練_&#x200B;以及&#x200B;_銷售_。 |
| 第3級 | 第三層級會顯示在每個主功能表選項的下方。 例如，在&#x200B;_女性_&#x200B;底下，第三層級選項為&#x200B;_頂端_&#x200B;和&#x200B;_底部_。 |
| 第4級 | 第四層級選項是從第三層級選項飛出的子類別。 例如，在&#x200B;_上衣_&#x200B;下，第四層功能表選項為&#x200B;_夾克_、_連帽衫和運動衫_、_T恤_&#x200B;和&#x200B;_胸罩和背心_。 |

{style="table-layout:auto"}

## 設定頂端導覽

若要讓類別出現在商店的頂端導覽列中，請完成下列步驟：

### 步驟1：建立類別

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Categories]**。

1. 設定&#x200B;**[!UICONTROL Store View]**&#x200B;以決定新類別在何處可用。

1. 在類別樹狀結構中，選取新類別的父類別。

   如果您從頭開始，沒有任何資料，清單中可能只有兩個類別： _預設類別_ （根目錄）和&#x200B;_範例類別_。

1. 按一下&#x200B;**[!UICONTROL Add Subcategory]**。

1. 使用下列設定完成基本資訊：

   - **[!UICONTROL Enable Category]**&#x200B;已設定為`Yes`
   - **[!UICONTROL Include in Menu]**&#x200B;已設定為`Yes`

1. 在顯示設定中，將&#x200B;**[!UICONTROL Anchor]**&#x200B;設定為`Yes`。

1. 完成任何其他必要的[類別設定](category-create.md)。

1. 完成時，按一下&#x200B;**[!UICONTROL Save]**。

對於多儲存安裝，可將不同的主功能表指派為每個[儲存區](../stores-purchase/stores.md#add-stores)的[根類別](category-root.md)。

### 步驟2：設定頂端導覽的深度

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Catalog]**&#x200B;並在下方選擇&#x200B;**[!UICONTROL Catalog]**。

1. 展開&#x200B;**[!UICONTROL Category Top Navigation]**&#x200B;區段。

   ![類別頂端導覽](../configuration-reference/catalog/assets/catalog-category-top-navigation.png){width="600" zoomable="yes"}

   由於上層導覽的深度具有全域[設定範圍](../getting-started/websites-stores-views.md#scope-settings)，因此此設定會套用至Commerce安裝中的所有網站、商店和商店檢視。 _[!UICONTROL Category Top Navigation]_設定區段只有在左上角的_[!UICONTROL Store View]_&#x200B;設定為`Default Config`時才能使用。

   如需這些選項的詳細清單，請參閱&#x200B;_組態參考_&#x200B;中的[類別頂端導覽](../configuration-reference/catalog/catalog.md#layered-navigation)。

1. 若要限制顯示在頂端導覽列中的子類別數目，請輸入&#x200B;**[!UICONTROL Maximal Depth]**&#x200B;的數字。

   預設值為`0`，不會限制子類別層級的數量。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。
