---
title: 新增內容 — 產品推薦
description: 瞭解Product Recommendations內容型別，用於新增建議清單至 [!DNL Page Builder] 階段。
exl-id: ca90c10d-8d7a-42a2-bb13-2602aa9d6eef
feature: Page Builder, Page Content, Recommendations
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '931'
ht-degree: 0%

---

# 新增內容 — 產品推薦

使用&#x200B;_Product Recommendations_&#x200B;內容型別，將現有的作用中[建議單位](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/admin/create)新增至CMS頁面、區塊或動態區塊的[[!DNL Page Builder] 階段](workspace.md#stage)。

>[!NOTE]
>
>[!DNL Page Builder] _產品建議_&#x200B;內容型別在Adobe Commerce 2.4.4和更新版本中受到支援，並可在[產品建議中繼3.0.x或更新版本中使用](https://commercemarketplace.adobe.com/magento-product-recommendations.html)。 若要為產品建議新增[!DNL Page Builder]支援，[請參閱安裝資訊](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/getting-started/install-configure)。 **此內容型別不適用於Magento Open Source。**

{{$include /help/_includes/page-builder-save-timeout.md}}

## 產品建議工具箱

| 工具 | 圖示 | 說明 |
| --- | --| --- |
| 移動 | ![移動圖示](./assets/pb-icon-move.png){width="25"} | 將產品推薦容器及其內容移至舞台上的另一個位置。 |
| 設定 | ![設定圖示](./assets/pb-icon-settings.png){width="25"} | 開啟「編輯產品建議」頁面，您可在其中選擇建議單位並變更容器屬性。 |
| 隱藏 | ![隱藏圖示](./assets/pb-icon-hide.png){width="25"} | 隱藏目前的產品推薦容器及其內容。 |
| 顯示 | ![顯示圖示](./assets/pb-icon-show.png){width="25"} | 顯示隱藏的產品推薦容器及其內容。 |
| 複製 | ![圖示重複](./assets/pb-icon-duplicate.png){width="25"} | 製作產品推薦容器及其內容的重複副本。 |
| 移除 | ![移除圖示](./assets/pb-icon-remove.png){width="25"} | 從階段刪除產品推薦容器及其內容。 |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## 新增現有的建議單位

1. 確定您已[建立](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/admin/create)頁面型別的建議單位[!DNL Page Builder]。

>[!NOTE]
>
>您只能在預設存放區檢視中為[!DNL Page Builder]頁面型別建立建議單位。

1. 在編輯模式中開啟頁面、區塊或動態區塊。

1. 展開&#x200B;_[!UICONTROL Content]_區段，然後按一下&#x200B;**[!UICONTROL Edit with Page Builder]**或內容預覽區域內的「[!DNL Page Builder]」工作區以開啟。

1. 在[!DNL Page Builder]下方的&#x200B;_[!UICONTROL Layout]_面板中，將&#x200B;**[!UICONTROL Row]**預留位置拖曳到舞台。

1. 在[!DNL Page Builder]下方的&#x200B;_[!UICONTROL Add Content]_面板中，將&#x200B;**[!UICONTROL Product Recommendation]**預留位置拖曳至列。

   ![正在新增產品推薦內容型別](./assets/pb-add-prex-drag.png){width="600" zoomable="yes"}

1. 執行下列任一項作業：

   - 按一下&#x200B;**[!UICONTROL Edit Product Recommendation]**。
   - 將滑鼠懸停在空白容器上以顯示工具箱，然後按一下&#x200B;_設定_ （![設定圖示](./assets/pb-icon-settings.png)）圖示。

   ![編輯產品推薦](./assets/pb-prex-toolbox.png){width="600" zoomable="yes"}

1. 在&#x200B;_[!UICONTROL Selection]_區段中，按一下&#x200B;**[!UICONTROL Select]**。

1. 在使用中產品推薦清單中，尋找含有您要新增之推薦單位的列，然後按一下最後一欄中的&#x200B;**[!UICONTROL Select]**。

   ![選取的產品推薦](./assets/pb-prex-select.png){width="600" zoomable="yes"}

1. 按一下右上角的&#x200B;**[!UICONTROL Add Selected]**。

   所選產品推薦的名稱會顯示在&#x200B;_[!UICONTROL Selection]_頁面的_[!UICONTROL Edit Product Recommendation]_&#x200B;區段中。

1. 對[進階設定](#advanced-settings)進行任何必要的變更。

   ![編輯產品推薦](./assets/pb-prex-edit.png){width="600" zoomable="yes"}

1. 完成後，請執行下列動作：

   - 如果使用最大化的瀏覽器視窗，請按一下工作區右上角的&#x200B;_關閉全熒幕_ （![關閉全熒幕圖示](./assets/pb-icon-reduce.png)）圖示。

   - 按一下&#x200B;**[!UICONTROL Save]**&#x200B;以套用設定並返回[!DNL Page Builder]工作區。

   當您回到舞台時，產品預留位置影像會出現在容器中。

## 編輯建議單位設定

1. 將滑鼠停留在建議單位容器上以顯示工具箱，然後按一下&#x200B;_設定_ （![設定圖示](./assets/pb-icon-settings.png)）圖示。

   ![建議工具箱](./assets/pb-placeholder-toolbox.png){width="600" zoomable="yes"}

1. 對[進階設定](#advanced-settings)進行任何必要的變更。

1. 完成後，按一下&#x200B;**[!UICONTROL Save]**&#x200B;套用設定並返回[!DNL Page Builder]工作區。

## 複製建議單位

1. 將游標停留在建議單位容器上以顯示工具箱，然後按一下工具箱中的&#x200B;_複製_ （![復製圖示](./assets/pb-icon-duplicate.png)）圖示。

   重複專案會出現在原始專案的正下方。

1. 若要將重複的建議單位移至新位置，請將滑鼠指標暫留在容器上，然後按一下工具箱中的&#x200B;_移動_ （![移動圖示](./assets/pb-icon-move.png)）圖示。

1. 選取並拖曳建議單位，直到紅色指引出現在新位置為止。

   移動建議單位時，每個容器的頂端和底部邊界都會顯示為虛線。

## 從階段中移除建議單位

1. 將游標停留在建議單位容器上，然後按一下工具箱中的&#x200B;_移除_ （![移除圖示](./assets/pb-icon-remove.png)）圖示。

1. 提示確認時，按一下&#x200B;**[!UICONTROL OK]**。

## 進階設定

1. 若要控制Product Recommendations單位在父容器中的位置，請選擇&#x200B;**[!UICONTROL Alignment]**：

   | 選項 | 說明 |
   | ------ | ----------- |
   | `Default` | 套用目前佈景主題樣式表中指定的對齊預設設定。 |
   | `Left` | 將單位沿父容器的左邊框對齊，並允許指定的任何邊框間距。 |
   | `Center` | 將單位對齊父容器的中心，並容許任何指定的內距。 |
   | `Right` | 將單位沿父容器的右邊框對齊，並容許任何指定的內距。 |

   {style="table-layout:auto"}

1. 設定套用至「產品建議」單位所有四個方面的&#x200B;**[!UICONTROL Border]**&#x200B;樣式：

   | 選項 | 說明 |
   | ------ | ----------- |
   | `Default` | 套用關聯樣式表所指定的預設邊框樣式。 |
   | `None` | 未提供任何單位框線的可見指示。 |
   | `Dotted` | 單位邊框會以虛線顯示。 |
   | `Dashed` | 單位邊框會以虛線顯示。 |
   | `Solid` | 單位邊框顯示為實線。 |
   | `Double` | 單位邊框會以雙線顯示。 |
   | `Groove` | 單位邊界會顯示為凹槽線。 |
   | `Ridge` | 單位邊界會顯示為脊線。 |
   | `Inset` | 單位框線會顯示為內嵌線。 |
   | `Outset` | 單位邊界會顯示為外線。 |

   {style="table-layout:auto"}

1. 如果您設定了`None`以外的框線樣式，請完成框線顯示選項：

   | 選項 | 說明 |
   | ------ |------------ |
   | [!UICONTROL Border Color] | 選擇色票、按一下檢色器，或輸入有效的顏色名稱或相等的十六進位值，以指定顏色。 |
   | [!UICONTROL Border Width] | 輸入邊框線條寬度的畫素數。 |
   | [!UICONTROL Border Radius] | 輸入畫素數目，以定義用來將邊框每個角落倒圓角的半徑大小。 |

   {style="table-layout:auto"}

1. （選擇性）從目前的樣式表中指定要套用至單位的&#x200B;**[!UICONTROL CSS classes]**&#x200B;名稱。

   以空格分隔多個類別名稱。

1. 輸入&#x200B;**[!UICONTROL Margins and Padding]**&#x200B;的畫素值，以決定單位的外邊界和內邊距。

   在圖表中輸入對應的值。

   | 容器區域 | 說明 |
   | ------ | ----------- |
   | [!UICONTROL Margins] | 套用至單位所有側邊外部邊緣的空白空間量。 選項： `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | 套用至單位所有側邊內邊的空白空間量。 選項： `Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}

<!-- Last updated from includes: 2023-09-11 14:30:19 -->
