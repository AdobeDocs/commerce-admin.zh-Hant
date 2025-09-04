---
title: 新增內容 — 區塊
description: 瞭解Block內容型別，用於新增可重複使用的區塊至 [!DNL Page Builder] 階段。
exl-id: fcedb125-e0c8-4b59-bd26-7f3912e0db2a
feature: Page Builder, Page Content
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# 新增內容 — 區塊

使用&#x200B;_區塊_&#x200B;內容型別將現有的作用中[區塊](../content-design/blocks.md)新增到[[!DNL Page Builder] 階段](workspace.md#stage)。 在下列範例中，第一欄包含具有頁面側功能表的區塊。 第二欄包含影像。

![使用側邊功能表封鎖](./assets/pb-add-content-block-example.png){width="600" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## 區塊工具箱

| 工具 | 圖示 | 說明 |
| --------- | -------- | ------------- |
| 移動 | ![移動圖示](./assets/pb-icon-move.png) | 將區塊容器及其內容移至舞台上的另一個位置。 |
| 設定 | ![設定圖示](./assets/pb-icon-settings.png) | 開啟「編輯區塊」頁面，您可在其中選擇區塊並變更容器的屬性。 |
| 隱藏 | ![隱藏圖示](./assets/pb-icon-hide.png) | 隱藏目前的區塊容器及其內容。 |
| 顯示 | ![顯示圖示](./assets/pb-icon-show.png) | 顯示隱藏的區塊容器及其內容。 |
| 複製 | ![圖示重複](./assets/pb-icon-duplicate.png) | 製作區塊容器及其內容的副本。 |
| 移除 | ![移除圖示](./assets/pb-icon-remove.png) | 從階段中刪除區塊容器及其內容。 |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## 新增現有區塊

1. 導覽至目標頁面、區塊、動態區塊、產品或類別上的[!DNL Page Builder]工作區。

1. 在[!DNL Page Builder]面板中，展開&#x200B;**[!UICONTROL Add Content]**&#x200B;並將&#x200B;**[!UICONTROL Block]**&#x200B;預留位置拖曳到舞台。

   ![將區塊拖曳到舞台上](./assets/pb-add-content-block-drag.png){width="600" zoomable="yes"}

1. 將滑鼠懸停在空白的區塊容器上以顯示工具箱，然後選擇&#x200B;_設定_ （ ![設定圖示](./assets/pb-icon-settings.png){width="25"} ）圖示。

1. 按一下&#x200B;**[!UICONTROL Select Block]**。

   ![選取區塊](./assets/pb-add-content-block-select.png){width="200"}

1. 在您要新增的區塊列中，按一下最後一欄中的&#x200B;**[!UICONTROL Select]**。

   ![選取的區塊](./assets/pb-add-content-block-selected.png){width="600" zoomable="yes"}

   所選區塊的名稱會顯示在頁面上。

   ![區塊名稱](./assets/pb-add-content-block-name.png){width="200"}

1. 視需要完成其餘的設定，並參考此頁面結尾的欄位說明。

1. 完成後，按一下&#x200B;**[!UICONTROL Save]**&#x200B;套用設定並返回[!DNL Page Builder]工作區。

### 進階設定

1. 若要控制區塊在父容器中的位置，請選擇&#x200B;**[!UICONTROL Alignment]**：

   | 選項 | 說明 |
   | ------ | ----------- |
   | `Default` | 套用目前佈景主題樣式表中指定的對齊預設設定。 |
   | `Left` | 沿著父容器的左邊框對齊清單，並允許指定的任何邊框間距。 |
   | `Center` | 將清單對齊父項容器的中心，並容許任何指定的內距。 |
   | `Right` | 沿著父容器的右邊框對齊區塊，並允許指定的任何邊框間距。 |

   {style="table-layout:auto"}

1. 設定套用至區塊容器所有四個側面的&#x200B;**[!UICONTROL Border]**&#x200B;樣式：

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

1. 如果您設定了`None`以外的框線樣式，請完成框線顯示選項：

   | 選項 | 說明 |
   | ------ |------------ |
   | [!UICONTROL Border Color] | 選擇色票、按一下檢色器，或輸入有效的顏色名稱或相等的十六進位值，以指定顏色。 |
   | [!UICONTROL Border Width] | 輸入邊框線條寬度的畫素數。 |
   | [!UICONTROL Border Radius] | 輸入畫素數目，以定義用來將邊框每個角落倒圓角的半徑大小。 |

   {style="table-layout:auto"}

1. （選擇性）從目前的樣式表中指定要套用至容器的&#x200B;**[!UICONTROL CSS classes]**&#x200B;名稱。

   以空格分隔多個類別名稱。

1. 輸入&#x200B;**[!UICONTROL Margins and Padding]**&#x200B;的值（以畫素為單位），以決定區塊容器的外部邊界和內邊距。

   在圖表中輸入對應的值。

   | 容器區域 | 說明 |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | 套用至容器所有側邊外部邊緣的空白空間量。 選項： `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | 套用至容器所有邊內側邊緣的空白空間量。 選項： `Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}

## 編輯區塊設定

1. 將滑鼠停留在區塊容器上，然後在工具箱中選擇&#x200B;_設定_ （ ![設定圖示](./assets/pb-icon-settings.png){width="25"} ）圖示。

   ![區塊工具箱](./assets/pb-add-content-block-toolbox.png){width="600" zoomable="yes"}

1. 若要選擇其他區塊，請按一下&#x200B;**[!UICONTROL Select Block]**。

   - 在使用中區塊清單中，按一下&#x200B;**[!UICONTROL Select]**&#x200B;您要新增的區塊。
   - 按一下&#x200B;**[!UICONTROL Add Selected]**。

1. 視需要更新其餘的設定，可使用此頁面結尾的欄位說明作為參考。

1. 完成後，按一下&#x200B;**[!UICONTROL Save]**&#x200B;套用設定並返回[!DNL Page Builder]工作區。

## 複製區塊

1. 將滑鼠懸停在區塊容器上以顯示工具箱，並選擇&#x200B;_複製_ （![復製圖示](./assets/pb-icon-duplicate.png)）圖示。

   重複專案會出現在原始專案的正下方。

1. 若要將新區塊移動至新位置，請將滑鼠指標暫留在容器上，然後按一下工具箱中的[移動] _（_[移動]圖示![）。](./assets/pb-icon-move.png)

1. 選取並拖曳區塊，直到紅色指引出現在新位置為止。

   移動區塊時，每個容器的頂端和底部邊界都會顯示為虛線。

## 從舞台移除區塊

1. 將滑鼠懸停在區塊容器上以顯示工具箱，然後選擇&#x200B;_移除_ （![移除圖示](./assets/pb-icon-remove.png)）圖示。

1. 提示確認時，按一下&#x200B;**[!UICONTROL OK]**。

<!-- Last updated from includes: 2023-09-11 14:30:19 -->
