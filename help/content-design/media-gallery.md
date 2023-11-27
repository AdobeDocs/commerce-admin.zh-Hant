---
title: 此 [!DNL Media Gallery]
description: 使用「媒體集」來組織和管理伺服器上的媒體檔案。
exl-id: bf730e46-70f3-405c-88cf-62d0a3e8634f
feature: Page Content, Media
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# 此 [!DNL Media Gallery]

透過Adobe Commerce或Magento Open Source 2.4，商家可以使用新的 _增強功能_ [!DNL Media Gallery] 組織並管理伺服器上的媒體檔案。 這個新的 [!DNL Media Gallery] 包含與現有媒體儲存相同的功能，但包含改良的使用者介面，以及與更密切的整合 [Adobe Stock][adobe-stock].

![媒體集格線中顯示的影像](./assets/media-gallery-grid.png){width="700" zoomable="yes"}

>[!NOTE]
>
>產品影像已新增至 [_[!UICONTROL Images and Videos]_產品區段](../catalog/product-image.md#upload-an-image) 不受管理 [!DNL Media Gallery]. 僅限中使用的影像_[!UICONTROL Content]_ 產品區段欄位會在新的中顯示和篩選 [!DNL Media Gallery].

## 啟用新的 [!DNL Media Gallery]

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Advanced]** 並選擇 **[!UICONTROL System]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery]**.

   ![進階設定 —  [!DNL Media Gallery]](./assets/system-media-gallery.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Enable Old Media Gallery]** 至 `No`.

1. 按一下 **[!UICONTROL Save Config]**.

1. 出現提示時，按一下 **[!UICONTROL Cache Management]** 連結，並重新整理無效的快取。

   此 [[!UICONTROL Content] 功能表](/help/content-design/content-menu.md) 現在顯示新的 _[!UICONTROL Media Gallery]_選項。

>[!NOTE]
>
>完整的新功能 [!DNL Media Gallery] 需要 `media.gallery.synchronization` 和 `media.content.synchronization` 將取用者排入佇列，以啟動初始同步處理。 另請參閱 [管理訊息佇列](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) 在 _設定指南_ 以取得更多詳細資料。

## 存取新的 [!DNL Media Gallery]

新的 [!DNL Media Gallery] 可從「內容」功能表存取，或當您 [新增或編輯頁面](/help/content-design/page-add.md). 您也可以在 [建立或編輯類別](/help/catalog/category-create.md)，或當您 [使用內容編輯器插入影像](/help/content-design/editor-insert-image.md).

若要存取新的 [!UICONTROL Media Gallery] 透過 [!UICONTROL Content] 功能表：

- 在 _管理員_ 側欄，前往 **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

若要在新增或編輯頁面時存取新的「媒體集」：

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. 按一下 **[!UICONTROL Add a New Page]**.

   如果您想要編輯現有頁面，可以使用 _[!UICONTROL Action]_要點按的欄&#x200B;**[!UICONTROL Select]**並選擇&#x200B;**[!UICONTROL Edit]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Content]** 並執行下列動作：

   - 如果您有 [已啟用頁面產生器](../page-builder/setup.md)，展開 **[!UICONTROL Media]** 面板並拖曳 **[!UICONTROL Image]** 目標容器的預留位置。 然後按一下 **[!UICONTROL Select from Gallery]**.

     ![將影像拖曳到舞台](./assets/pb-media-image-drag.png){width="600" zoomable="yes"}

   - 如果您擁有 [WYSIWYG編輯器已啟用](/help/content-design/editor.md)，按一下 **[!UICONTROL Show/Hide Editor]** 然後按一下 **[!UICONTROL Insert Image]**.

## [!DNL Media Gallery] 示範

若要進一步瞭解 [!DNL Media Gallery]，請觀看此影片：

>[!VIDEO](https://video.tv.adobe.com/v/343785?quality=12)

[adobe-stock]: https://stock.adobe.com

