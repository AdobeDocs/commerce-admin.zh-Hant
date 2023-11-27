---
title: 媒體 — 影片
description: 瞭解影片內容型別，用來將託管於YouTube或Vimeo的影片新增至 [!DNL Page Builder] 階段。
exl-id: 9cd075e7-c10d-4c34-8932-c1ccb32bf198
feature: Page Builder, Page Content
source-git-commit: 79dc16dcba239af12793813ae19636bbd7ec49c5
workflow-type: tm+mt
source-wordcount: '935'
ht-degree: 0%

---

# 媒體 — 影片

使用 _視訊_ 內容型別，用於新增託管於的視訊 [YouTube][1] 或 [Vimeo][2] 至 [[!DNL Page Builder] 階段](workspace.md#stage). 將視訊嵌入頁面或區塊，或產品與類別說明中相當容易。

![店面首頁上的影片](./assets/pb-storefront-video.png){width="700" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## 視訊工具箱

![視訊工具箱](./assets/pb-media-video-toolbox.png){width="600" zoomable="yes"}

| 工具 | 圖示 | 說明 |
|--- |--- |--- |
| 移動 | ![移動圖示](./assets/pb-icon-move.png){width="25"} | 將視訊移至舞台上的另一個位置。 |
| （標籤） | [!UICONTROL Video] | 將目前的內容容器識別為視訊。 將滑鼠停留在影像容器上可檢視工具箱。 |
| 設定 | ![設定圖示](./assets/pb-icon-settings.png){width="25"} | 開啟 _[!UICONTROL Edit Video]_頁面，您可在此變更視訊和容器的屬性。 |
| 隱藏 | ![隱藏圖示](./assets/pb-icon-hide.png){width="25"} | 隱藏目前的視訊。 |
| 顯示 | ![顯示圖示](./assets/pb-icon-show.png){width="25"} | 顯示隱藏的視訊。 |
| 複製 | ![「複製」圖示](./assets/pb-icon-duplicate.png){width="25"} | 製作視訊副本。 |
| 移除 | ![移除圖示](./assets/pb-icon-remove.png){width="25"} | 從舞台刪除視訊。 |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## 新增視訊

1. 開始之前，請導覽至 [YouTube][1] 或 [Vimeo][2] 內嵌的視訊並複製連結。

   另外，您也可以複製有效視訊檔案的直接連結。 另請參閱 [基本視訊設定](#basic-video-settings) 的有效連結。

1. 在 [!DNL Commerce] 管理員，返回 [!DNL Page Builder] 您想要新增視訊的工作區。

1. 在 [!DNL Page Builder] 面板，展開 **[!UICONTROL Media]** 並拖曳 **[!UICONTROL Video]** 舞台的預留位置。

   ![將視訊預留位置拖曳到舞台](./assets/pb-media-video-drag.png){width="600" zoomable="yes"}

1. 將滑鼠停留在視訊容器上以顯示工具箱，然後選擇 _設定_ ( ![設定圖示](./assets/pb-icon-settings.png){width="20"} )圖示。

1. 的 **[!UICONTROL Video URL]**，貼上您複製之視訊的URL。

   的URL [!DNL Page Builder] 此範例中使用的視訊為： `https://www.youtube.com/watch?v=Y0KNS7C5dZA`.

1. 若要限制 **[!UICONTROL Maximum Width]** 在視訊中，輸入最大寬度（畫素）。

   如果留白，視訊寬度將和容器一樣寬，可允許邊界和邊框間距。

1. 在右上角，按一下 **[!UICONTROL Save]** 以套用設定並返回 [!DNL Page Builder] 工作區。

## 變更視訊設定

1. 將滑鼠停留在視訊容器上以顯示工具箱，然後選擇 _設定_ ( ![設定圖示](./assets/pb-icon-settings.png){width="20"} )圖示。

1. 請依照下列章節修改設定：

   - [基本](#basic-video-settings)
   - [進階](#advanced)

1. 在右上角，按一下 **[!UICONTROL Save]** 以套用設定並返回 [!DNL Page Builder] 工作區。

### 基本視訊設定

1. 若要變更目前的視訊，請更新 **[!UICONTROL Video URL]**.

   請輸入有效的視訊URL。 有效的視訊URL可以連結至：

   - YouTube影片： `https://youtu.be/CoDhMRUUjeI`
   - Vimeo影片： `https://vimeo.com/190156113`
   - 有效的視訊檔案(`.mp4` 建議使用)： `https://myvideos.com/spiral.mp4`

1. 若要變更店面中視訊允許的寬度，請輸入新的 **[!UICONTROL Maximum Width]** 以畫素為單位。

   如果留白，視訊會延伸容器的完整寬度，減去邊界和邊框間距的裕量。

1. 若要在頁面載入後自動啟動視訊，請設定 **[!UICONTROL Autoplay]** 至 `Yes`.

   如果自動播放設為 `Yes`，視訊會根據原則在播放時設為靜音。 不過，即使使用此設定，行動裝置也無法自動播放您的視訊。 如需這些原則的詳細資訊，請參閱下列開發人員資源：

   - [Vimeo的自動播放原則](https://vimeo.zendesk.com/hc/en-us/articles/115004485728-Autoplaying-and-looping-embedded-videos)
   - [Google (Chrome/YouTube)的自動播放原則](https://developer.chrome.com/blog/autoplay/)
   - [本機視訊的自動播放原則](https://developer.mozilla.org/en-US/docs/Web/Media/Autoplay_guide)

   如果自動播放設為 `No`，影片只會根據使用者需求播放。

### [!UICONTROL Advanced]

1. 若要控制視訊在容器中的水平位置，請選擇 **[!UICONTROL Alignment]**：

   | 選項 | 說明 |
   | ------ | ----------- |
   | `Default` | 套用目前佈景主題樣式表中指定的對齊預設設定。 |
   | `Left` | 沿著視訊容器的左邊框對齊內容，並允許指定的任何邊框間距。 |
   | `Center` | 對齊視訊容器中央的內容，並容許指定的任何邊框間距。 |
   | `Right` | 沿著視訊容器的右邊框對齊內容，並容許任何指定的邊框間距。 |

   {style="table-layout:auto"}

- 設定 **[!UICONTROL Border]** 套用至視訊容器所有四個邊的樣式：

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

  ![邊框顏色](./assets/pb-settings-border-color.png){width="600" zoomable="yes"}

  | 選項 | 說明 |
  | ------ |------------ |
  | [!UICONTROL Border Color] | 選擇色票、按一下檢色器，或輸入有效的顏色名稱或相等的十六進位值，以指定顏色。 |
  | [!UICONTROL Border Width] | 輸入邊框線條寬度的畫素數。 |
  | [!UICONTROL Border Radius] | 輸入畫素數目，以定義用來將邊框每個角落倒圓角的半徑大小。 |

  {style="table-layout:auto"}

- （選擇性）指定下列專案的名稱： **[!UICONTROL CSS classes]** 目前的樣式表以套用至視訊容器。

  以空格分隔多個類別名稱。

- 以畫素為單位，輸入 **[!UICONTROL Margins and Padding]** 指定視訊容器的外邊界和內邊距。

  在視訊容器圖表中輸入每個對應的值。

  | 容器區域 | 說明 |
  | -------------- | ----------- |
  | [!UICONTROL Margins] | 套用至容器所有側邊外部邊緣的空白空間量。 |
  | [!UICONTROL Padding] | 套用至容器所有邊內側邊緣的空白空間量。 |

  {style="table-layout:auto"}

## 移動視訊

1. 將滑鼠停留在視訊容器上以顯示工具箱，然後選擇 _移動_ ( ![移動圖示](./assets/pb-icon-move.png){width="20"} )圖示。

   ![移動視訊](./assets/pb-media-video-toolbox-move-col1.png){width="500" zoomable="yes"}

1. 選取視訊並將其拖曳到新的位置，正好在紅色指引的下方。

   ![使用紅色指引放置影片](./assets/pb-media-video-toolbox-move-col2.png){width="500" zoomable="yes"}

## 從舞台移除影片

1. 將滑鼠停留在視訊容器上以顯示工具箱，然後選擇 _移除_ (![移除圖示](./assets/pb-icon-remove.png))圖示。

1. 提示確認時，按一下 **[!UICONTROL OK]**.

[1]: https://www.youtube.com/
[2]: https://vimeo.com/
