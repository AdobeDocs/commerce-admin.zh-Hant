---
title: 媒體集影像最佳化
description: 瞭解如何針對您的 [!DNL Commerce] 媒體資產使用影像最佳化。
exl-id: ba75e90a-406b-4b14-b049-0b78c4a27188
feature: Page Content, Media
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---

# 媒體集影像最佳化

新的[媒體集](media-gallery.md)提供&#x200B;_影像最佳化_&#x200B;功能，可改善效能並降低店面媒體檔案大小。 此最佳化預設為啟用，並可在存放區組態設定中修改。

## 設定影像最佳化

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Advanced]**&#x200B;並選擇&#x200B;**[!UICONTROL System]**。

1. 展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery Image Optimization]**&#x200B;並執行下列動作：

   - 將&#x200B;**[!UICONTROL Enable Image Optimization]**&#x200B;設為`Yes`。
   - 根據您的需求，輸入&#x200B;**[!UICONTROL Maximum Width]**&#x200B;和&#x200B;**[!UICONTROL Maximum Height]**&#x200B;值（畫素）。

## 行為

啟用Media Gallery影像最佳化功能時，影像的最佳化復本會自動插入[Media Gallery](media-gallery.md)的內容，而非原始檔案。

當組態中的&#x200B;_最大寬度_&#x200B;和&#x200B;_最大高度_&#x200B;值變更時，它會更新先前插入的所有現有最佳化影像。

Media Gallery Image Optimization需要執行`media.gallery.renditions.update`佇列取用者，以便在設定變更時重新產生最佳化影像。 如需詳細資訊，請參閱&#x200B;_設定指南_&#x200B;中的[管理訊息佇列](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html)。

{{$include /help/_includes/image-optimization-animated-gif-note.md}}
