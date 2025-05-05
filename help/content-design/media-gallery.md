---
title: ' [!DNL Media Gallery]'
description: 使用「媒體集」來組織和管理伺服器上的媒體檔案。
exl-id: bf730e46-70f3-405c-88cf-62d0a3e8634f
feature: Page Content, Media
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---

# [!DNL Media Gallery]

透過Adobe Commerce或Magento Open Source 2.4，商家可以使用新的&#x200B;_增強型_ [!DNL Media Gallery]來整理和管理伺服器上的媒體檔案。 此新[!DNL Media Gallery]包含與現有媒體儲存相同的功能，但包含改良的使用者介面以及與[Adobe Stock][adobe-stock]更緊密的整合。

![顯示在媒體集格線中的影像](./assets/media-gallery-grid.png){width="700" zoomable="yes"}

>[!NOTE]
>
>新增至&#x200B;[_[!UICONTROL Images and Videos]_&#x200B;產品區段](../catalog/product-image.md#upload-an-image)的產品影像不是由[!DNL Media Gallery]管理。 只有在&#x200B;_[!UICONTROL Content]_&#x200B;產品區段欄位中使用的影像，才會顯示在新的[!DNL Media Gallery]中並經過篩選。

## 啟用新[!DNL Media Gallery]

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Advanced]**&#x200B;並選擇&#x200B;**[!UICONTROL System]**。

1. 展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery]**。

   ![進階設定 — [!DNL Media Gallery]](./assets/system-media-gallery.png){width="600" zoomable="yes"}

1. 將&#x200B;**[!UICONTROL Enable Old Media Gallery]**&#x200B;設為`No`。

1. 按一下&#x200B;**[!UICONTROL Save Config]**。

1. 出現提示時，請按一下系統訊息中的&#x200B;**[!UICONTROL Cache Management]**&#x200B;連結，然後重新整理無效的快取。

   [[!UICONTROL Content]功能表](/help/content-design/content-menu.md)現在會顯示新的&#x200B;_[!UICONTROL Media Gallery]_&#x200B;選項。

>[!NOTE]
>
>新[!DNL Media Gallery]的完整功能需要啟動`media.gallery.synchronization`和`media.content.synchronization`佇列使用者以進行初始同步。 如需詳細資訊，請參閱&#x200B;_設定指南_&#x200B;中的[管理訊息佇列](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html?lang=zh-Hant)。

## 存取新的[!DNL Media Gallery]

可從「內容」功能表或當您[新增或編輯頁面](/help/content-design/page-add.md)時，存取新的[!DNL Media Gallery]。 您[建立或編輯類別](/help/catalog/category-create.md)時，或使用「內容編輯器」[插入影像時](/help/content-design/editor-insert-image.md)，也可以存取它。

若要透過[!UICONTROL Content]功能表存取新[!UICONTROL Media Gallery]：

- 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**。

若要在新增或編輯頁面時存取新的「媒體集」：

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**。

1. 按一下&#x200B;**[!UICONTROL Add a New Page]**。

   若要編輯現有頁面，您可以使用&#x200B;_[!UICONTROL Action]_&#x200B;欄按一下&#x200B;**[!UICONTROL Select]**&#x200B;並選擇&#x200B;**[!UICONTROL Edit]**。

1. 展開![展開選取器](../assets/icon-display-expand.png) **[!UICONTROL Content]**&#x200B;區段，然後執行下列動作：

   - 如果您已啟用[頁面產生器](../page-builder/setup.md)，請展開&#x200B;**[!UICONTROL Media]**&#x200B;面板，並將&#x200B;**[!UICONTROL Image]**&#x200B;預留位置拖曳至目標容器。 然後按一下&#x200B;**[!UICONTROL Select from Gallery]**。

     ![將影像拖曳到舞台](./assets/pb-media-image-drag.png){width="600" zoomable="yes"}

   - 如果您已啟用[WYSIWYG編輯器](/help/content-design/editor.md)，請按一下&#x200B;**[!UICONTROL Show/Hide Editor]**，然後按一下&#x200B;**[!UICONTROL Insert Image]**。

## [!DNL Media Gallery]展示

若要進一步瞭解[!DNL Media Gallery]，請觀看此影片：

>[!VIDEO](https://video.tv.adobe.com/v/343785?quality=12&learn=on)

[adobe-stock]: https://stock.adobe.com

