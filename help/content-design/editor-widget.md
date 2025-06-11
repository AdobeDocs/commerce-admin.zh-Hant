---
title: 在編輯器中插入Widget
description: 使用WYSIWYG編輯器中的Widget工具，將各種內容元素新增至頁面。
exl-id: bbc5e059-06d8-4dda-89a7-6c9826b73fd3
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hant/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%

---

# 在編輯器中插入Widget

[Widget](widget-create.md)工具可用來將各種內容元素新增至頁面，包括任何Commerce內容頁面或節點、產品或類別的連結。 連結可以區塊格式放置在頁面上，或直接併入內容中。 您可以使用Widget工具建立下列內容型別的連結：

- [內容頁面](pages.md)
- [目錄類別](../catalog/categories.md)
- [目錄產品](../catalog/product-create.md)

依照預設，連結會從佈景主題的樣式表中繼承其樣式。

{{$include /help/_includes/directives-caution.md}}

1. 在編輯模式中開啟頁面、區塊或動態區塊。

1. 移至&#x200B;_[!UICONTROL Content]_&#x200B;區段，然後按一下任何支援編輯器的元素。

1. 將游標置於您要顯示介面工具集的位置，然後按一下&#x200B;_插入Widget_&#x200B;圖示。

   ![編輯器工具列 — 插入Widget](./assets/editor-toolbar-widget-button.png){width="700" zoomable="yes"}

   如果您未啟用頁面產生器，且偏好使用程式碼，請按一下&#x200B;**[!UICONTROL Show / Hide Editor]**。 將插入點放置在文字中要顯示Widget的位置。 然後，按一下&#x200B;**[!UICONTROL Insert Widget]**。

1. 選擇&#x200B;**[!UICONTROL Widget Type]**。

   如需這些選項的詳細資訊，請參閱[Widget型別](widgets.md#widget-types)。 下列步驟使用將連結插入產品的範例。

1. 若要使用產品名稱，請將&#x200B;**[!UICONTROL Anchor Custom Text]**&#x200B;欄位留空。

1. 輸入&#x200B;**[!UICONTROL Anchor Custom Title]**&#x200B;以取得最佳SEO實務。

   此標題在頁面上不可見。

1. 將&#x200B;**[!UICONTROL Template]**&#x200B;設定為下列其中一項：

   - 若要將連結併入文字中，請選取`Product Link Inline Template`。

   - 若要將連結放在單獨的一行，請選取`Product Link Block Template`。

1. 按一下&#x200B;**[!UICONTROL Select Product]**&#x200B;並執行下列動作：

   - 在樹狀結構中，導覽至您想要的類別。

   - 在清單中，選擇連結的產品。

1. 按一下&#x200B;**[!UICONTROL Insert Widget]**&#x200B;將連結放到頁面上。

   如果您使用HTML程式碼，連結的[標籤標籤](../systems/markup-tags.md)會顯示在頁面頂端，並以雙大括弧括住。 如有需要，請使用&#x200B;_剪下並貼上_，將標籤標籤放置在您要顯示連結的程式碼中。

1. 當您的內容編輯完成時，按一下&#x200B;**[!UICONTROL Save]**。
