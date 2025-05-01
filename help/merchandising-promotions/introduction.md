---
title: Commerce銷售與促銷活動簡介
description: 了解 Commerce 工具如何建立針對性促銷活動和客戶參與機會。
exl-id: 8e55ac42-aeef-4f97-b1e8-9b2db354e5e6
source-git-commit: 7774aa82149faff55591303c7ff2fe2c84797a4a
workflow-type: tm+mt
source-wordcount: '1111'
ht-degree: 1%

---

# Commerce銷售與促銷活動簡介

鎖定促銷活動，創造客戶參與的機會，並將購物者變成買家。 透過支援購買後活動並為回頭的客戶提供特別折扣來管理客戶關係。 瞭解最佳實務和技術，以支援您的SEO方案。

## 銷售

_銷售_&#x200B;是零售中使用的術語，用於描述樓層平面圖開發及產品展示的藝術與科學。 您可能會將[類別導覽](../catalog/navigation-top.md)視為商店的平面圖，將產品的動態呈現視為您可以套用至商店中產品清單的條件。 此外，您可以實作可促進更多產品銷售的程式：

- [!BADGE 僅限PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"} [Visual Merchandiser](visual-merchandiser.md) — 一組進階工具，可讓您定位產品，並套用條件來決定哪些產品會出現在類別清單中。

- [禮品登記處](gift-registries.md) — 讓您的客戶能夠建立特殊場合的禮品登記處，並且邀請他們的朋友和家人從禮品登記處購買他們的禮物。

- [獎勵和忠誠度](rewards-loyalty.md) — 使用點數系統來實作獨特的方案，以提升客戶參與度並提升客戶忠誠度。 您可以為各種交易與客戶活動授予積分，並控制積分分配、平衡及有效期。

- [私人銷售與活動](events-private-sales.md) — 使用您現有的客戶群來產生熱點和新的銷售機會，或是透過私人銷售與其他目錄活動來解除安裝剩餘存貨。

>[!TIP]
>
>若要瞭解產品推薦以及如何提供您所需的insight和控制功能，讓您的購買者獲得最佳體驗，請參閱[產品推薦使用手冊](https://experienceleague.adobe.com/docs/commerce/product-recommendations/guide-overview.html)。

## 促銷活動

在Adobe Commerce中，使用促銷功能來設定產品關係，並使用價格規則來根據各種條件觸發折扣。 您可以使用價格規則來提供客戶獎勵，例如：

- 傳送優惠券給最佳客戶，以獲得特定產品的折扣
- 為超過特定金額的購買提供免運費
- 為特定時段排程促銷

規則是條件（一或多個）的集合，當滿足一或多個條件時，會將價格變更套用至產品。 每個規則可以有多個條件，當全部或任何（一或多個，但不是全部）陳述式為true或false時套用。

### 條件

條件為陳述式，可調整產品清單和套用規則的情況。 條件的屬性和選項因可用規則的型別而異。 達到條件時，動作就會完成，例如折扣、單次購買(BOGO)和其他選項。 規則可以簡單或複雜，以符合您的業務需求、季節性折扣和促銷活動以及長達一年的商機。 例如，當購物車的小計很高時，您可能會想要在全年免費送貨時為假期新增一些選項。

>[!NOTE]
>
>若要根據特定產品屬性定義條件，您必須將[店面屬性](../catalog/attribute-product-create.md)中屬性的&#x200B;**[!UICONTROL Use for Promo Rule Conditions]**&#x200B;設為`Yes`。


### 價格規則

針對[目錄價格規則](price-rules-catalog.md)，您會根據目錄、比較函式和選取的屬性中的[屬性集](../catalog/attribute-sets.md)建立條件。 您可以選取一些陳述式來建立條件，例如句子。 例如，您可以建立兩個價格規則，以根據類別來套用童裝和男裝/女裝的折扣。

![圖表 — 目錄價格規則範例](./assets/diagram-catalog-price-rules.png){width="500"}

[購物車價格規則](price-rules-cart.md)條件可以是以商店[root](../catalog/category-root.md)之子類別為基礎。 價格規則會預先設定，當符合必要條件時，便會開始執行。 這些規則會使用屬性，包括產品屬性組合，例如使用產品屬性比對購物車中的SKU。 這些規則也可以使用產品選擇數量條件、複雜規則的條件組合，以及購物車屬性（例如小計）。

![圖表 — 購物車價格規則範例](./assets/diagram-cart-price-rules.png){width="500"}

## 通訊與SEO

掌握[搜尋引擎最佳化(SEO)](seo-overview.md)對於吸引潛在買家至關重要。 瞭解搜尋引擎最佳化並微調網站的內容和呈現方式，以改進搜尋引擎為頁面編制索引的方式。

在啟動商店之前要完成的一項任務是，檢閱商店傳送的所有通訊所使用的電子郵件範本，以確保這些範本反映您的品牌。 但您應該更進一步開發其他通訊功能，向現有客戶推廣您的品牌和產品。 您可以使用變數和標籤標籤來個人化內容。

>[!NOTE]
>
>Adobe Commerce和Magento Open Source版本2.4.0到2.4.3包含由供應商開發並用來與dotdigital Engagement Cloud整合的dotdigital擴充功能。 從2.4.4版開始，此擴充功能不再與核心版本搭配，必須從Commerce Marketplace安裝和更新。 此Marketplace也可讓您存取擴充功能開發人員提供的目前檔案。
><br><br>
>如果您已啟用並設定隨附的擴充功能，則必須在2.4.4升級程式中更新composer.json檔案，並管理後續的擴充功能更新。 如需詳細資訊，請參閱&#x200B;_升級指南_&#x200B;中的[升級模組](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html)。

- [電子報](newsletters.md) — 製作電子報、管理您的訂閱者清單、開發內容，並帶動您商店的流量。

- [RSS摘要](social-rss.md#rss-feeds) — 使用RSS摘要將您的產品資訊發佈到購物彙總網站，甚至將它們包含在您的電子報中。 客戶可以訂閱您的RSS摘要，瞭解新產品和促銷活動。

- [社交網路](social-rss.md#social-networks) — 透過安裝Marketplace擴充功能或新增外掛程式至內容頁面，將您的商店與社交網路整合。

## Google行銷工具

您的商店設定與以下Google工具整合，以協助最佳化您的內容、分析您的流量，以及將您的目錄連結至購物彙總和行銷場所。

>[!NOTE]
>
>自2.4.5版開始，Google服務整合已更新，以支援使用GTag API。 GTag是整合網頁之Google功能的統一機制，可支援透過Google服務追蹤及管理內容的最新功能與機會。 如需詳細資訊，請參閱[Google Analytics開發人員檔案](https://developers.google.com/analytics/devguides/collection/gtagjs)。

- [Google Analytics](google-analytics.md) — 使用Google Universal Analytics定義額外的自訂維度和量度以進行追蹤，並支援離線和行動應用程式互動，以及存取持續更新。

- [Google內容實驗](google-content-experiments.md) — 使用Google Analytics內容設定產品、類別或內容頁面的A/B測試

- [Google標籤管理員](google-tag-manager.md) - ![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)使用Google標籤管理員來管理許多與行銷活動事件相關的標籤。

- [Google AdWords](google-adwords.md) — 建立Google AdWords行銷活動並追蹤您商店的轉換。
