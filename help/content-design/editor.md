---
title: WYSIWYG編輯器
description: 瞭解如何使用編輯器，並以「您所見即所得_ (WYSIWYG)」檢視處理內容(_H)。
exl-id: 209ca9d6-973c-4ad9-b7cd-4fba58dbfbb8
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# WYSIWYG編輯器

編輯器可讓您在內容的&#x200B;_您所見即所得_ (WYSIWYG)檢視中進行輸入並格式化。 如果您偏好直接使用基礎HTML程式碼，則可輕鬆變更模式。 編輯器可用來建立[頁面](pages.md)、[區塊](blocks.md)和[產品說明](../catalog/product-content.md)的內容。 處理產品詳細資料時，按一下&#x200B;**[!UICONTROL Show / Hide Editor]**&#x200B;以存取編輯器。

>[!NOTE]
>
>TinyMCE 5是預設的WYSIWYG編輯器。 在Adobe Commerce和Magento Open Source 2.4.5中更新TinyMCE 5.10程式庫，解決了在使用某些型別URL更新影像或連結時允許任意JavaScript執行的弱點。 TinyMCE 3在2.4.0版本中已過時，在2.4.3版本中已移除。 TinyMCE 4已在2.4.4版本中移除。

![編輯器工具列](./assets/editor-toolbar.png){width="700" zoomable="yes"}

下列主題提供有關使用編輯器的詳細資訊：

- [插入連結](editor-insert-link.md)
- [插入影像](editor-insert-image.md)
- [插入Widget](editor-widget.md)
- [插入變數](editor-insert-variable.md)

## 設定編輯器

WYSIWYG編輯器預設為啟用，可用於編輯CMS頁面和區塊以及產品和類別中的內容。 從設定中，您可以啟用或停用編輯器，並選擇在產品和類別說明中使用媒體內容的靜態URL，而非[動態](../catalog/catalog-urls.md#dynamic-url)。

![WYSIWYG選項](./assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

如需所有WYSIWYG選項的詳細說明，請參閱&#x200B;_組態參考_&#x200B;中的[內容管理](../configuration-reference/general/content-management.md)。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板的&#x200B;_[!UICONTROL General]_下，選擇&#x200B;**[!UICONTROL Content Management]**。

1. 展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL WYSIWYG Options]**。

1. 將&#x200B;**[!UICONTROL Enable WYSIWYG Editor]**&#x200B;設定為您的偏好設定。

   編輯器預設為啟用。

1. 針對使用WYSIWYG編輯器輸入的所有[媒體內容](../catalog/catalog-urls.md#static-url)，將&#x200B;**[!UICONTROL Static URLs for Media Content in WYSIWYG]**&#x200B;設定為您的偏好設定。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。
