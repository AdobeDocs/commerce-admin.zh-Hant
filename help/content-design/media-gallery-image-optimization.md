---
title: 媒體集影像最佳化
description: 瞭解如何針對您的 [!DNL Commerce] 媒體資產使用影像最佳化。
exl-id: ba75e90a-406b-4b14-b049-0b78c4a27188
feature: Page Content, Media
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hant/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案（Adobe管理的PaaS基礎結構）和內部部署專案的Adobe Commerce 。"
TQID: https://experienceleague.adobe.com/BTjXX6X70q2Mwm0xPNx-t429R5m93VprCHBDcYgQNpY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 211
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

Media Gallery Image Optimization需要執行`media.gallery.renditions.update`佇列取用者，以便在設定變更時重新產生最佳化影像。 如需詳細資訊，請參閱&#x200B;_設定指南_&#x200B;中的[管理訊息佇列](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html?lang=zh-Hant)。

{{$include /help/_includes/image-optimization-animated-gif-note.md}}

<!-- Last updated from includes: 2024-01-30 15:43:39 -->
