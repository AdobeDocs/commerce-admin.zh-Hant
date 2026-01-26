---
title: 元素 — HTML程式碼
description: 瞭解HTML程式碼內容型別，用於在 [!DNL Page Builder] 階段中新增HTML、CSS和JavaScript程式碼片段。
exl-id: b6e2dff5-ceac-4c7e-a87f-f95a542ada28
feature: Page Builder, Page Content
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '980'
ht-degree: 0%

---

# 元素 — HTML程式碼

使用&#x200B;_HTML程式碼_&#x200B;內容型別，在[[!DNL Page Builder] 階段](workspace.md#stage)中新增HTML、CSS和JavaScript程式碼的片段。 例如，您可能會想要新增自訂HTML、宣告可套用至頁面上元素的CSS類別。 或者，您可能想要為您從第三方提供者收到的標誌、按鈕或橫幅新增程式碼片段。

## HTML程式碼工具箱

![HTML程式碼工具箱](./assets/pb-elements-html-code-toolbox.png){width="500" zoomable="yes"}

| 工具 | 圖示 | 說明 |
| --------- | ---------- | ----------------- |
| 移動 | ![移動圖示](./assets/pb-icon-move.png){width="25"} | 將HTML程式碼容器移至頁面上的另一個有效位置。 |
| 設定 | ![設定圖示](./assets/pb-icon-settings.png){width="25"} | 開啟「編輯HTML程式碼」頁面，您可在此變更容器屬性。 |
| 隱藏 | ![隱藏圖示](./assets/pb-icon-hide.png){width="25"} | 隱藏HTML程式碼容器。 |
| 顯示 | ![顯示圖示](./assets/pb-icon-show.png){width="25"} | 顯示隱藏的HTML程式碼容器。 |
| 複製 | ![圖示重複](./assets/pb-icon-duplicate.png){width="25"} | 製作HTML程式碼容器的副本。 |
| 移除 | ![移除圖示](./assets/pb-icon-remove.png){width="25"} | 從階段中刪除HTML程式碼容器及其內容。 |

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## 新增HTML程式碼

下列範例示範如何內嵌[Google Font](https://fonts.google.com/)程式碼並宣告覆寫目前樣式表的自訂標題類別。

### 步驟1：選擇Google字型

1. 造訪[Google Fonts](https://fonts.google.com/)網站，並選擇要使用的字型系列。

1. 複製要內嵌在頁面`<head>`區段中的產生程式碼，並將其暫時貼到文字編輯器中。

   - 內嵌字型代碼
   - CSS規則

1. 將字型系列規則新增至每個標題類別，並將標題類別括在`<style>`標籤中。

   此程式碼已貼到[!DNL Page Builder]中。

   ```html
   <style>
      h1 {color: teal; font-family: 'Khand', sans-serif; }
      h2 {color: teal; font-family: 'Khand', sans-serif; }
      h3 {color: teal; font-family: 'Khand', sans-serif; }
   </style>
   ```

### 步驟2：將程式碼新增至頁面

1. 在您商店的&#x200B;_管理員_&#x200B;側邊欄中，前往&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**。

1. 尋找字型可用的頁面，並以編輯模式開啟。

1. 向下捲動並展開&#x200B;**[!UICONTROL Content]**&#x200B;區段。

1. 在[!DNL Page Builder]面板中，展開&#x200B;**[!UICONTROL Elements]**&#x200B;並將&#x200B;**[!UICONTROL HTML Code]**&#x200B;預留位置拖曳至舞台上的列、欄或索引標籤集。

   使用紅色指引將分隔線放置在列、欄或索引標籤集中另一個內容容器之前或之後。

   ![將HTML程式碼預留位置拖曳到舞台](./assets/pb-elements-html-code-drag.png){width="600" zoomable="yes"}

1. 將游標暫留在HTML容器上以顯示工具箱，然後選擇&#x200B;_設定_ （ ![設定圖示](./assets/pb-icon-settings.png){width="20"} ）圖示。

1. 在文字方塊中，貼上您準備的內嵌Google字型程式碼和樣式宣告。

   為了更方便閱讀，您可以輸入一些空格來縮排程式碼。

   ![HTML程式碼和樣式](./assets/pb-elements-html-code-example.png){width="500" zoomable="yes"}

1. 視需要更新其餘的設定(如需詳細資訊，請參閱[變更HTML程式碼設定](#html-settings))。

1. 在右上角，按一下&#x200B;**[!UICONTROL Save]**&#x200B;以套用設定並返回[!DNL Page Builder]工作區。

   透過瀏覽器檢視頁面時，新字型會呈現。

### 步驟3：預覽頁面

1. 在&#x200B;_[!UICONTROL Currently Active]_&#x200B;區段中，將&#x200B;**[!UICONTROL Enable Page]**&#x200B;設為`Yes`。

   ![正在啟用頁面](./assets/pb-elements-html-code-enable-page.png){width="600" zoomable="yes"}

1. 在右上角，按一下&#x200B;**[!UICONTROL Save]**&#x200B;箭頭並選擇&#x200B;**[!UICONTROL Save & Close]**。

1. 在格線中尋找頁面，並在&#x200B;**[!UICONTROL View]**&#x200B;欄中選取&#x200B;_[!UICONTROL Actions]_。

   ![使用新字型系列預覽頁面標題](./assets/pb-elements-html-code-preview.png){width="700" zoomable="yes"}

## 變更HTML程式碼設定 {#html-settings}

1. 將游標暫留在HTML容器上以顯示工具箱，然後選擇&#x200B;_設定_ （ ![設定圖示](./assets/pb-icon-settings.png){width="20"} ）圖示。

1. 在文字方塊中，視需要編輯程式碼。

   支援HTML、CSS和JavaScript程式碼。 您可以在此處輸入屬於頁面`<head>`區段的程式碼片段。

   編輯器也提供在程式碼中插入特殊元素的按鈕：

   | 按鈕 | 說明 |
   | ------ | ----------- |
   | 插入Widget... | 按一下，在HTML文字方塊中的游標位置處插入Widget。 |
   | 插入影像…… | 按一下「 」，在HTML文字方塊中的游標位置處插入來自相簿的上傳影像或影像。 |
   | 插入變數…… | 按一下，在HTML文字方塊中的游標位置處插入變數。 |

1. 視需要更新&#x200B;_[!UICONTROL Advanced]_&#x200B;設定。

   - 若要控制程式碼在父容器中的位置，請選擇&#x200B;**[!UICONTROL Alignment]**：

     | 選項 | 說明 |
     | ------ | ----------- |
     | `Default` | 套用目前佈景主題樣式表中指定的對齊預設設定。 |
     | `Left` | 沿著父容器的左邊框對齊清單，並允許指定的任何邊框間距。 |
     | `Center` | 將清單對齊父項容器的中心，並容許任何指定的內距。 |
     | `Right` | 沿著父容器的右邊框對齊區塊，並允許指定的任何邊框間距。 |

     在下列範例中，選項設定為使用演算後程式碼區塊的置中對齊。

     ![具有中央對齊的分隔線](./assets/pb-elements-divider-settings-advanced-alignment-center.png){width="600" zoomable="yes"}

   - 設定套用至程式碼容器所有四個側面的&#x200B;**[!UICONTROL Border]**&#x200B;樣式：

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

   - 如果您設定了`None`以外的框線樣式，請完成框線顯示選項：

     | 選項 | 說明 |
     | ------ |------------ |
     | [!UICONTROL Border Color] | 選擇色票、按一下檢色器，或輸入有效的顏色名稱或相等的十六進位值，以指定顏色。 |
     | [!UICONTROL Border Width] | 輸入邊框線條寬度的畫素數。 |
     | [!UICONTROL Border Radius] | 輸入畫素數目，以定義用來將邊框每個角落倒圓角的半徑大小。 |

     {style="table-layout:auto"}

   - （選擇性）從目前的樣式表中指定要套用至容器的&#x200B;**[!UICONTROL CSS classes]**&#x200B;名稱。

     以空格分隔多個類別名稱。

   - 輸入&#x200B;**[!UICONTROL Margins and Padding]**&#x200B;的值（以畫素為單位），以決定程式碼容器的外部邊界和內邊距。

     在圖表中輸入對應的值。

     | 容器區域 | 說明 |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | 套用至容器所有側邊外部邊緣的空白空間量。 選項： `Top` / `Right` / `Bottom` / `Left` |
     | [!UICONTROL Padding] | 套用至容器所有邊內側邊緣的空白空間量。 選項： `Top` / `Right` / `Bottom` / `Left` |


<!-- Last updated from includes: 2023-09-11 14:30:19 -->
