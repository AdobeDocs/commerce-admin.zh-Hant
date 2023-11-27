---
title: 元素 — 標題
description: 瞭解標題內容型別，用於新增標題層級從H1到H6的文字容器至 [!DNL Page Builder] 階段。
exl-id: dc51e7f6-a235-49dc-a978-1419a63fa33e
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '941'
ht-degree: 0%

---

# 元素 — 標題

標題層級會建立組織內容的階層，並協助搜尋引擎為每個頁面編制索引。 使用 _標題_ 中的內容型別 [[!DNL Page Builder] 階段](workspace.md#stage) 將標題層級從H1到H6的文字容器加入舞台。 標題會根據與目前主題關聯的樣式表來格式化。

此 [內容標題](workspace.md) 中的欄位 _[!UICONTROL Content]_區段可用來將H1標題新增至頁面頂端。 不過，欄位是舊版欄位 [!DNL Commerce] 和版本是為了支援舊版內容而提供。 此欄位未利用 [!DNL Page Builder]的進階功能 建議您將「內容標題」欄位保留空白，並使用 [!DNL Page Builder] 標題內容型別，可新增任何層級的標題至頁面。

下列範例說明當使用Luma主題進行格式化時，內容標題和標題內容型別的顯示方式。

![店面的內容標題和標題層級](./assets/pb-storefront-heading-levels.png){width="700" zoomable="yes"}

您可以從以下位置拖曳標題： _元素_ 的區段 [!DNL Page Builder] 面板至舞台上的列、欄或索引標籤集。 標題層級和對齊方式可透過舞台上的編輯器工具列或透過使用 _設定_ ( ![設定圖示](./assets/pb-icon-settings.png){width="20"} )控制項。

{{$include /help/_includes/page-builder-save-timeout.md}}

## 標題編輯器

![具有工具列的標題編輯器](./assets/pb-elements-heading-toolbar.png){width="500" zoomable="yes"}

## 標題容器工具箱

就像所有內容容器一樣，當您將滑鼠游標停留在容器上時，工具箱會出現。

![標題容器工具箱](./assets/pb-elements-heading-toolbox.png){width="500" zoomable="yes"}

| 工具 | 圖示 | 說明 |
| --------- | ----------------- | ---------------------- |
| 移動 | ![移動圖示](./assets/pb-icon-move.png){width="25"} | 將標題容器移至頁面上的另一個有效位置。 |
| （標籤） | 標題 | 將目前的容器識別為標題。 |
| 設定 | ![設定圖示](./assets/pb-icon-settings.png){width="25"} | 開啟「編輯標題」頁面，您可在此變更容器的屬性。 |
| 隱藏 | ![隱藏圖示](./assets/pb-icon-hide.png){width="25"} | 隱藏標題容器。 |
| 顯示 | ![顯示圖示](./assets/pb-icon-show.png){width="25"} | 顯示隱藏的標題容器。 |
| 複製 | ![「複製」圖示](./assets/pb-icon-duplicate.png){width="25"} | 製作標題容器的副本。 |
| 移除 | ![移除圖示](./assets/pb-icon-remove.png){width="25"} | 從階段中刪除標題容器及其內容。 |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## 新增標題

1. 在 [!DNL Page Builder] 面板，展開 **[!UICONTROL Elements]** 並拖曳 **[!UICONTROL Heading]** 舞台上的列、欄或標籤集的預留位置。

   ![將標題拖曳到舞台](./assets/pb-elements-heading-drag.png){width="600" zoomable="yes"}

1. 在編輯器中，將標題文字輸入到 `Edit Heading Text` 預留位置。

   依照預設，標題文字會指定層級二(H2)標題型別。

   ![標題編輯器中的預留位置](./assets/pb-elements-header-editor-placeholder.png){width="500" zoomable="yes"}

1. 在工具列中，選擇H1和H6之間的適當標題型別。

1. 視需要變更對齊方式。

## 編輯標題設定

1. 將滑鼠懸停在標題容器上以顯示工具箱，然後選擇 _設定_ ( ![設定圖示](./assets/pb-icon-settings.png){width="20"} )圖示。

   ![標題工具箱](./assets/pb-elements-heading-toolbox.png){width="500" zoomable="yes"}

1. 更新標題內容(**[!UICONTROL Heading Type]** 和 **[!UICONTROL Heading Text]**)。

   您也可以在標題編輯器中更新此內容。

1. 更新 _[!UICONTROL Advanced]_設定。

   - 若要控制標題在父容器中的位置，請選擇 **[!UICONTROL Alignment]**：

     | 選項 | 說明 |
     | ------ | ----------- |
     | `Default` | 套用目前佈景主題樣式表中指定的對齊預設設定。 |
     | `Left` | 沿著父容器的左邊框對齊清單，並允許指定的任何邊框間距。 |
     | `Center` | 將清單對齊父項容器的中心，並容許任何指定的內距。 |
     | `Right` | 沿著父容器的右邊框對齊區塊，並允許指定的任何邊框間距。 |

     {style="table-layout:auto"}

   - 設定 **[!UICONTROL Border]** 套用至標題容器所有四個邊的樣式：

     | 選項 | 說明 |
     | ------ | ----------- |
     | `Default` | 套用關聯樣式表所指定的預設邊框樣式。 |
     | `None` | 未提供任何容器框線的可見指示。 |
     | `Dotted` | 容器邊框會以虛線顯示。 |
     | `Dashed` | 容器邊框會以虛線顯示。 |
     | `Solid` | 容器邊框會以實線顯示。 |
     | `Double` | 容器邊框會以雙線顯示。 |
     | `Groove` | 容器框線會顯示為槽線。 |
     | `Ridge` | 容器框線會顯示為脊線。 |
     | `Inset` | 容器框線會顯示為內嵌線。 |
     | `Outset` | 容器邊框會顯示為外線。 |

     {style="table-layout:auto"}

   - 如果您設定的邊框樣式不是 `None`，完成邊框顯示選項：

     | 選項 | 說明 |
     | ------ |------------ |
     | [!UICONTROL Border Color] | 選擇色票、按一下檢色器，或輸入有效的顏色名稱或相等的十六進位值，以指定顏色。 |
     | [!UICONTROL Border Width] | 輸入邊框線條寬度的畫素數。 |
     | [!UICONTROL Border Radius] | 輸入畫素數目，以定義用來將邊框每個角落倒圓角的半徑大小。 |

     {style="table-layout:auto"}

   - （選擇性）指定下列專案的名稱： **[!UICONTROL CSS classes]** 從目前的樣式表套用至容器。

     以空格分隔多個類別名稱。

   - 以畫素為單位，輸入 **[!UICONTROL Margins and Padding]** 以決定標題容器的外邊界和內邊距。

     在圖表中輸入對應的值。

     | 容器區域 | 說明 |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | 套用至容器所有側邊外部邊緣的空白空間量。 選項： `Top` / `Right` / `Bottom` / `Left` |
     | [!UICONTROL Padding] | 套用至容器所有邊內側邊緣的空白空間量。 選項： `Top` / `Right` / `Bottom` / `Left` |

     {style="table-layout:auto"}

1. 完成後，按一下 **[!UICONTROL Save]** 以套用設定並返回 [!DNL Page Builder] 工作區。

## 複製標題

對於具有特定設定的格式化標題，複製標題比使用新的預留位置重新開始更有效率。

1. 將滑鼠懸停在標題容器上以顯示工具箱，然後選擇 _複製_ ( ![「複製」圖示](./assets/pb-icon-duplicate.png){width="20"} )圖示。

   重複專案會出現在原始專案的正下方。

   ![複製標題容器](./assets/pb-elements-heading-duplicate.png){width="500" zoomable="yes"}

1. 將滑鼠懸停在新標題容器上以顯示工具箱，然後選擇 _移動_ ( ![移動圖示](./assets/pb-icon-move.png){width="20"} )圖示。

   ![移動標題](./assets/pb-elements-heading-move.png){width="500" zoomable="yes"}

1. 選取並拖曳標題，直到紅色指引標籤新位置為止。

   移動標題時，每個容器的頂端和底部框線都會顯示為虛線。

   ![將複製的標題移至位置](./assets/pb-elements-heading-move-guideline.png){width="500" zoomable="yes"}

1. 如果要變更標題層級，請按一下標題文字，然後在編輯器工具列中選擇新層級。

   ![選擇新的標題層級](./assets/pb-elements-heading-change-heading-level.png){width="500" zoomable="yes"}
