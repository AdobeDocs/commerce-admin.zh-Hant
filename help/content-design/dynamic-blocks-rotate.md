---
title: 新增旋轉動態區塊
description: 將多個動態區塊新增至旋轉器，在店面展示互動式內容的投影片。
exl-id: 3d338014-cf26-4171-b48b-d37b3d7b0e81
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '624'
ht-degree: 0%

---

# 新增旋轉動態區塊

{{ee-feature}}

若要呈現互動式內容的投影片放映，您可以將多個[動態區塊](dynamic-blocks.md)新增至旋轉器。 [Widget](widgets.md)工具可用來將旋轉器放置在單一頁面上的特定位置，或是整個商店的多個頁面上的特定位置。

![動態區塊旋轉器](./assets/widget-dynamic-block-rotator.png){width="700" zoomable="yes"}

## 步驟1：建立個別的動態區塊

若要[建立您想要放置在旋轉器中的動態區塊](dynamic-blocks.md)，請遵循下列指示：

## 步驟2：新增動態區塊旋轉器Widget

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**。

1. 按一下右上角的&#x200B;**[!UICONTROL Add Widget]**。

1. 在&#x200B;_設定_&#x200B;下，將&#x200B;**[!UICONTROL Type]**&#x200B;設定為`Dynamic Blocks Rotator`。

1. 選擇目前存放區的&#x200B;**[!UICONTROL Design Theme]**。

   此設定可識別目前封裝或決定商店頁面版面的[佈景主題](themes.md)。

1. 按一下&#x200B;**[!UICONTROL Continue]**。

   ![動態區塊旋轉器設定](./assets/widget-dynamic-block-rotator-settings.png){width="600" zoomable="yes"}

## 步驟3：完成選項

1. 在&#x200B;_店面屬性_&#x200B;下，設定選項：

   - 輸入旋轉器的&#x200B;**[!UICONTROL Title]**。

   - 在&#x200B;**[!UICONTROL Assign to Store Views]**&#x200B;清單中，選取旋轉器可用的[存放區檢視](../getting-started/websites-stores-views.md)。

   - （選擇性）輸入&#x200B;**[!UICONTROL Sort Order]**&#x200B;數字，以決定目標容器中旋轉器的位置。 此元件是相對於其他可指派給相同容器的Widget而定。

   ![旋轉器店面屬性](./assets/widget-dynamic-block-rotator-storefront-properties.png){width="600" zoomable="yes"}

1. 在&#x200B;_配置選項_&#x200B;下，按一下&#x200B;**[!UICONTROL Add Layout Update]**&#x200B;並執行下列動作：

   - 將&#x200B;**[!UICONTROL Display on]**&#x200B;設定為要顯示旋轉器的頁面或頁面型別。

      - `Categories` — 在[錨點](../catalog/navigation-layered.md)或非錨點類別頁面上顯示旋轉器。 選項：錨點類別/非錨點類別
      - `Products` — 在特定型別的產品頁面上或所有產品頁面上顯示旋轉器。 選項：所有產品型別/ [簡單產品](../catalog/product-create-simple.md) / [虛擬產品](../catalog/product-create-virtual.md) / [套裝產品](../catalog/product-create-bundle.md) / [可下載的產品](../catalog/product-create-downloadable.md) / [禮品卡](../catalog/product-gift-card-create.md) / [可設定產品](../catalog/product-create-configurable.md) / [群組產品](../catalog/product-create-grouped.md)
      - `Generic Pages` — 在所有頁面、特定頁面或只有特定版面的頁面上顯示旋轉器。 選項： `All Pages` / `Specified Page` / `Page Layouts`

     在此範例中，旋轉器將放置在`Specified Page`上。

   - 選取要顯示旋轉器的特定&#x200B;**[!UICONTROL Page]**。

   - 將&#x200B;**[!UICONTROL Container]**&#x200B;設定為旋轉器將要顯示的[頁面配置](page-layout.md#standard-page-layouts)部分。

     如果將其他Widget指派給相同的容器，它們會根據排序順序依序出現。

   - 接受`Dynamic Block Template`作為預設&#x200B;**[!UICONTROL Template]**。

     此設定會根據旋轉器是獨立或置於現有文字中來決定用來格式化旋轉器的範本。

     ![旋轉器配置更新](./assets/widget-dynamic-block-rotator-layout-updates.png){width="600" zoomable="yes"}

   - 按一下&#x200B;**[!UICONTROL Save and Continue Edit]**。

1. 在左側面板中選擇&#x200B;**[!UICONTROL Widget Options]**。

1. 對於&#x200B;**[!UICONTROL Dynamic Blocks to Display]**，接受`Specified Dynamic Blocks`。

   此設定決定旋轉器中包含的動態區塊型別。

   - `Specified Dynamic Blocks` — 僅包含特定動態區塊。
   - `Cart Price Rule Related` — 僅包含與購物車價格規則關聯的動態區塊。
   - `Catalog Price Rule Related` — 僅包含與目錄價格規則相關聯的動態區塊。

1. 選取可以與Widget搭配使用的&#x200B;**[!UICONTROL Restrict the Dynamic Block Types]**。`Content Area`

   此設定會將橫幅限制在頁面配置的特定部分。

   - `Content Area` — 將動態區塊放置在頁面的主要內容區域中。
   - `Footer` — 將動態區塊放置在頁尾中。
   - `Header` — 將動態區塊放置在頁首中。
   - `Left Column` — 將動態區塊放置在頁面配置的左欄（如果有的話）。
   - `Right Column` — 將動態區塊放置在頁面配置的右欄（如果有的話）。

1. 將&#x200B;**[!UICONTROL Rotation Mode]**&#x200B;設定為下列其中一項：

   - `Display all instead of rotating` — 顯示全部可見的動態區塊棧疊。
   - `One at a time, Random` — 以隨機順序顯示指定的動態區塊。 重新整理頁面時，會出現另一個（和隨機）動態區塊。
   - `One at the time, Series` — 顯示新增序列中指定的動態區塊。 重新整理頁面時，序列中的下一個動態區塊就會出現。
   - `One at the time, Shuffle` — 以隨機順序一次顯示一個動態區塊。 此選項與`One at a time, Random`選項類似，不同之處在於相同的動態區塊不會重複。

     ![旋轉器Widget選項](./assets/widget-dynamic-block-rotator-widget-options.png){width="600" zoomable="yes"}

1. 在&#x200B;**[!UICONTROL Specify Dynamic Blocks]**&#x200B;格線中，選取每個要包含在旋轉器中的動態區塊的核取方塊。

1. 完成時，按一下&#x200B;**[!UICONTROL Save]**。
