---
title: WYSIWYG編輯器
description: 瞭解如何使用編輯器，並以「您所見即所得_ (WYSIWYG)」檢視處理內容(_H)。
exl-id: 209ca9d6-973c-4ad9-b7cd-4fba58dbfbb8
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 0%

---

# WYSIWYG編輯器

該編輯器可讓您在使用時輸入和格式化 _所見即所得_ （所見即所得）內容檢視。 如果您偏好直接使用基礎HTML程式碼，則可輕鬆變更模式。 編輯器可用於建立內容 [頁面](pages.md)， [個區塊](blocks.md)、和 [產品說明](../catalog/product-content.md). 處理產品詳細資料時，按一下以存取編輯器 **[!UICONTROL Show / Hide Editor]**.

>[!NOTE]
>
>TinyMCE 5是預設的WYSIWYG編輯器。 在Adobe Commerce和Magento Open Source2.4.5中更新TinyMCE 5.10程式庫，解決了在使用某些型別URL更新影像或連結時允許任意JavaScript執行的弱點。 TinyMCE 3在2.4.0版本中已過時，在2.4.3版本中已移除。 TinyMCE 4已在2.4.4版本中移除。

![編輯器工具列](./assets/editor-toolbar.png){width="700" zoomable="yes"}

下列主題提供有關使用編輯器的詳細資訊：

- [插入連結](editor-insert-link.md)
- [插入影像](editor-insert-image.md)
- [插入Widget](editor-widget.md)
- [插入變數](editor-insert-variable.md)

## 設定編輯器

WYSIWYG編輯器預設為啟用，可用於編輯CMS頁面和區塊以及產品和類別中的內容。 從設定中，您可以啟用或停用編輯器，並選取使用靜態，而不是 [動態](../catalog/catalog-urls.md#dynamic-url)、產品和類別說明中媒體內容的URL。

![WYSIWYG選項](./assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

如需所有WYSIWYG選項的詳細說明，請參閱 [內容管理](../configuration-reference/general/content-management.md) 在 _設定參考_.

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中的 _[!UICONTROL General]_，選擇&#x200B;**[!UICONTROL Content Management]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) **[!UICONTROL WYSIWYG Options]**.

1. 設定 **[!UICONTROL Enable WYSIWYG Editor]** 依您的偏好設定。

   編輯器預設為啟用。

1. 設定 **[!UICONTROL Static URLs for Media Content in WYSIWYG]** 至您對全部的偏好設定 [媒體內容](../catalog/catalog-urls.md#static-url) 使用WYSIWYG編輯器輸入。

1. 完成後，按一下 **[!UICONTROL Save Config]**.
