---
title: 類別 — 內容設定
description: 瞭解如何使用[!UICONTROL Content]設定來定義出現在類別頁面上的任何其他內容。
exl-id: 988083e1-0993-4e08-b5e6-8b0855e56467
feature: Catalog Management, Categories, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 0%

---

# 類別 — 內容設定

_[!UICONTROL Content]_&#x200B;設定會決定類別頁面上是否出現任何其他內容。 除了類別產品清單之外，頁面還可以包含影像、說明和CMS區塊。 您可以使用[[!DNL Page Builder]](../page-builder/introduction.md)內容工具來定義類別說明。

## 在[!DNL Page Builder]中新增類別說明

1. 在編輯模式中開啟類別。

1. 向下捲動並展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Content]**&#x200B;區段。

   ![類別內容](./assets/category-content.png){width="600" zoomable="yes"}

1. 在&#x200B;**[!UICONTROL Description]**&#x200B;區域的右上方，按一下&#x200B;**[!UICONTROL Edit with Page Builder]**。

1. 使用[[!DNL Page Builder]](../page-builder/introduction.md)內容工具[編輯任何現有文字](../page-builder/text.md)並新增其他內容（如有需要）。

## [!DNL Page Builder]預覽

當您展開現有類別的&#x200B;_Content_&#x200B;區段（其中已使用[!DNL Page Builder]建立內容）時，會顯示&#x200B;**[!UICONTROL Description]**&#x200B;內容的預覽（如同顯示在類別頁面中的方式）。 按一下內容區域會開啟[!DNL Page Builder]工作區，您可以在其中進行任何需要的更新。

![描述預覽](../page-builder/assets/pb-product-category-content-preview.png){width="500" zoomable="yes"}

此產品和類別表單的內容預覽預設為啟用。 如果效能因載入預覽而受到影響，您可以在[內容管理組態](../configuration-reference/general/content-management.md#advanced-content-tools)設定中停用預覽。

## 在編輯器中新增類別說明

在文字方塊中只輸入純ASCII字元。 如果從文書處理器貼上文字，請先將它儲存為純.TXT檔案，以移除任何隱藏的控制字元。

如需詳細資訊，請參閱[所見即所得編輯器](../content-design/editor.md)。

1. 在編輯模式中開啟類別。

1. 向下捲動並展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Content]**&#x200B;區段。

   ![類別內容](./assets/category-content-ce.png){width="500" zoomable="yes"}

1. 輸入類別&#x200B;**[!UICONTROL Description]**&#x200B;並使用[編輯器工具列](../content-design/editor.md)來視需要格式化。

   您可以拖曳右下角來變更文字方塊的高度。

## 新增CMS區塊至類別頁面

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Categories]**。

1. 在類別樹狀結構中，選取您要編輯的類別。

1. 展開&#x200B;**[!UICONTROL Content]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

1. 針對&#x200B;**[!UICONTROL Add the CMS block]**，選取您要新增的區塊。

1. 展開&#x200B;**[!UICONTROL Display Settings]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

1. 將&#x200B;**[!UICONTROL Display Mode]**&#x200B;設定為下列其中一項：

   - `Static block only`
   - `Static block and products`

1. 完成後，按一下&#x200B;**[!UICONTROL Save]**&#x200B;並檢閱店面上的區塊顯示（需要快取重新整理）。

## 內容設定參考

| 設定 | [領域](../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Category Image] | 存放區檢視 | 指定類別頁面頂端的影像。 方法： <br/><br/>**[!UICONTROL Upload]**— 將影像檔案從本機電腦上傳到相簿，並將其作為類別影像。<br/><br/>**[!UICONTROL Select from Gallery]** — 提示您從影像庫選擇現有影像。 <br/><br/>![Page Builder相機圖示](../assets/icon-camera.png) — 請將影像檔案拖曳到相機圖磚，或瀏覽至影像並從本機檔案系統中選取影像。 |
| [!UICONTROL Description] | 存放區檢視 | 指定類別頁面上顯示的說明。 <br/><br/>**[!UICONTROL Edit with Page Builder]**— 開啟[[!DNL Page Builder] 工作區](../page-builder/workspace.md)，您可以在其中編輯說明。<br/><br/>**[!UICONTROL Show / Hide Editor]** — 在WYSIWYG編輯器和HTML模式之間切換顯示。 |
| [!UICONTROL Add CMS Block] | 存放區檢視 | 將現有的[CMS區塊](../content-design/blocks.md)新增至類別頁面。 |

{style="table-layout:auto"}
