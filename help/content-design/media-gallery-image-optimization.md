---
title: 媒體集影像最佳化
description: 瞭解如何針對您的使用影像最佳化 [!DNL Commerce] 媒體資產。
exl-id: ba75e90a-406b-4b14-b049-0b78c4a27188
feature: Page Content, Media
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---

# 媒體集影像最佳化

新的 [媒體集](media-gallery.md) 提供 _影像最佳化_ 功能，可改善效能並降低店面媒體檔案大小。 此最佳化預設為啟用，並可在存放區組態設定中修改。

## 設定影像最佳化

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Advanced]** 並選擇 **[!UICONTROL System]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery Image Optimization]** 並執行下列動作：

   - 設定 **[!UICONTROL Enable Image Optimization]** 至 `Yes`.
   - 輸入 **[!UICONTROL Maximum Width]** 和 **[!UICONTROL Maximum Height]** 值（畫素）。

## 行為

啟用「媒體集」影像最佳化功能時，最佳化的影像復本會自動插入的內容，從 [媒體集](media-gallery.md) 而不是原始檔案。

當 _最大寬度_ 和 _最大高度_ 值在設定中變更，會更新先前插入的所有現有最佳化影像。

媒體集影像最佳化需要 `media.gallery.renditions.update` 當組態變更時，佇列取用者正在執行以重新產生最佳化的影像。 另請參閱 [管理訊息佇列](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) 在 _設定指南_ 以取得更多詳細資料。
