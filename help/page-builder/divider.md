---
title: 元素 — 分隔線
description: 瞭解分隔線內容型別，用於新增規則作為 [!DNL Page Builder] 階段中內容區段之間的視覺分隔符號。
exl-id: e1052170-6d2f-4893-a78b-a845a8b6c0d9
feature: Page Builder, Page Content
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 0%

---

# 元素 — 分隔線

使用&#x200B;_分隔線_&#x200B;內容型別新增規則，作為[[!DNL Page Builder] 階段](workspace.md#stage)中內容區段之間的視覺分隔符號。 您可以指定分隔線的線條顏色、厚度和寬度。 您也可以控制對齊方式、設定邊界與邊框間距，以及容器邊框的格式。 依預設，分隔線是可延伸容器完整寬度的細線規則，且允許邊框間距。

![沒有框線的容器中的預設分隔線](./assets/pb-elements-divider-default.png){width="500" zoomable="yes"}

雖然大部分的分隔線容器都是不可見的，但下列範例會以紅色虛線框線顯示容器，讓您檢視分隔線、邊框間距與容器之間的關係。 您可以調整分隔線頂端和底部的內距，以控制元素之間的間距。

![在包含虛線框線的容器中具有填補的分隔器](./assets/pb-elements-divider-default-border-dashed.png){width="500" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## 分隔線工具箱

| 工具 | 圖示 | 說明 |
| ---- | --------------------| ------------|
| 移動 | ![移動圖示](./assets/pb-icon-move.png){width="25"} | 將分隔線容器移至頁面上的另一個有效位置。 |
| （標籤） | 分隔線 | 將目前的容器識別為分隔線元素。 |
| 設定 | ![設定圖示](./assets/pb-icon-settings.png){width="25"} | 開啟「編輯分隔線」頁面，您可以在此變更分隔線及其容器的屬性。 |
| 隱藏 | ![隱藏圖示](./assets/pb-icon-hide.png){width="25"} | 隱藏分隔線容器。 |
| 顯示 | ![顯示圖示](./assets/pb-icon-show.png){width="25"} | 顯示隱藏的分隔器容器。 |
| 複製 | ![圖示重複](./assets/pb-icon-duplicate.png){width="25"} | 製作分隔線容器的副本。 |
| 移除 | ![移除圖示](./assets/pb-icon-remove.png){width="25"} | 從舞台刪除分隔線容器及其內容。 |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## 新增分隔線

1. 在[!DNL Page Builder]面板中，展開&#x200B;**[!UICONTROL Elements]**&#x200B;並將&#x200B;**[!UICONTROL Divider]**&#x200B;預留位置拖曳至舞台上的列、欄或索引標籤集。

   當您在舞台上另一個內容容器之前或之後放置分隔線時，請使用紅色指引作為參考。

   ![將分隔線拖曳到舞台](./assets/pb-elements-divider-drag.png){width="600" zoomable="yes"}

   在下列範例中，分隔線會標籤文字新區段的開頭。

   ![分隔文字區段的分隔線](./assets/pb-elements-dividers-multiple-text-row.png){width="500" zoomable="yes"}

1. 若要指定新分隔線的設定，請遵循下列程式。

## 變更分隔線設定

1. 將滑鼠懸停在分隔線容器上以顯示工具箱，然後選擇&#x200B;_設定_ （ ![設定圖示](./assets/pb-icon-settings.png){width="20"} ）圖示。

   ![分隔線工具箱](./assets/pb-elements-divider-toolbox.png){width="500" zoomable="yes"}

1. 使用下列其中一種方法變更分隔線&#x200B;**[!UICONTROL Line Color]**：

   - 請輸入有效的[HTML色彩名稱][1]。 例如，`Teal`。
   - 輸入十六進位色彩值。 例如，`#008080`。

   完成時，按一下&#x200B;**[!UICONTROL Apply]**。

   ![設定線條色彩](./assets/pb-elements-divider-settings-line-color.png){width="600" zoomable="yes"}

1. 輸入&#x200B;**[!UICONTROL Line Thickness]**&#x200B;畫素。

1. 若要指示測量單位，請輸入&#x200B;**[!UICONTROL Line Width]**，然後輸入`px`或`%`。

   ![設定線條色彩、粗細和寬度](./assets/pb-elements-divider-settings-line-color-thickness-width.png){width="600" zoomable="yes"}

1. 視需要更新&#x200B;_[!UICONTROL Advanced]_設定。

   - 若要控制分隔線在父容器中的位置，請選擇&#x200B;**[!UICONTROL Alignment]**：

     | 選項 | 說明 |
     | ------ | ----------- |
     | `Default` | 套用目前佈景主題樣式表中指定的對齊預設設定。 |
     | `Left` | 沿著父容器的左邊框對齊清單，並允許指定的任何邊框間距。 |
     | `Center` | 將清單對齊父項容器的中心，並容許任何指定的內距。 |
     | `Right` | 沿著父容器的右邊框對齊區塊，並允許指定的任何邊框間距。 |

     {style="table-layout:auto"}

     在下列範例中，選項設定為使用分隔線的中心對齊。

     ![具有中央對齊的分隔線](./assets/pb-elements-divider-settings-advanced-alignment-center.png){width="600" zoomable="yes"}

   - 設定套用至分隔線容器所有四個邊的&#x200B;**[!UICONTROL Border]**&#x200B;樣式：

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

   - 如果您設定了`None`以外的框線樣式，請完成框線顯示選項：

     | 選項 | 說明 |
     | ------ |------------ |
     | [!UICONTROL Border Color] | 選擇色票、按一下檢色器，或輸入有效的顏色名稱或相等的十六進位值，以指定顏色。 |
     | [!UICONTROL Border Width] | 輸入邊框線條寬度的畫素數。 |
     | [!UICONTROL Border Radius] | 輸入畫素數目，以定義用來將邊框每個角落倒圓角的半徑大小。 |

     {style="table-layout:auto"}

   - （選擇性）從目前的樣式表中指定要套用至容器的&#x200B;**[!UICONTROL CSS classes]**&#x200B;名稱。

     以空格分隔多個類別名稱。

   - 輸入&#x200B;**[!UICONTROL Margins and Padding]**&#x200B;的值（以畫素為單位），以決定分隔線容器的外部邊界和內邊距。

     在圖表中輸入對應的值。

     | 容器區域 | 說明 |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | 套用至容器所有側邊外部邊緣的空白空間量。 選項： `Top` / `Right` / `Bottom` / `Left` |
     | [!UICONTROL Padding] | 套用至容器所有邊內側邊緣的空白空間量。 選項： `Top` / `Right` / `Bottom` / `Left` |

     {style="table-layout:auto"}

1. 完成後，按一下&#x200B;**[!UICONTROL Save]**&#x200B;套用設定並返回[!DNL Page Builder]工作區。

   ![分隔線以資料列居中](./assets/pb-elements-divider-settings-2px-centered.png){width="500" zoomable="yes"}

## 複製分隔線

對於具有特定設定的格式化分隔線，製作重複比使用新的預留位置重新開始更有效率。

1. 將滑鼠懸停在分隔線容器上以顯示工具箱，然後選擇&#x200B;_複製_ （ ![復製圖示](./assets/pb-icon-duplicate.png){width="20"} ）圖示。

   重複分隔線容器會出現在原始分隔線的正下方。

   ![重複的分隔線](./assets/pb-elements-divider-duplicate.png){width="500" zoomable="yes"}

1. 將滑鼠停留在新的分隔線容器上以顯示工具箱，並選擇&#x200B;_移動_ （![移動圖示](./assets/pb-icon-move.png){width="20"} ）圖示。

   ![移動分隔線](./assets/pb-elements-divider-move.png){width="500" zoomable="yes"}

1. 選取並拖曳分隔線，直到紅色指引標籤新位置為止。

   分隔線移動時，每個容器的頂端和底部邊界會顯示為虛線。

   ![將重複的分隔線移至位置](./assets/pb-elements-divider-move-guideline.png){width="500" zoomable="yes"}

[1]: https://en.wikipedia.org/wiki/Web_colors

<!-- Last updated from includes: 2023-09-11 14:30:19 -->
