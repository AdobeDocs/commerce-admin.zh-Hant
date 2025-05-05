---
title: 使用內容傳遞網路
description: 瞭解如何使用內容傳遞網路(CDN)來儲存媒體檔案。
exl-id: cb612b79-f3e3-4f1b-8cf9-d47886486686
feature: Page Content, Media, Configuration
level: Experienced
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%

---

# 使用內容傳遞網路

內容傳遞網路(CDN)可用來儲存媒體檔案。 雲端基礎結構上的Adobe Commerce包含Fastly CDN (請參閱&#x200B;_雲端基礎結構上的Commerce指南_&#x200B;中的[Fastly](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/cdn/fastly.html))。 _內部部署_&#x200B;安裝的Commerce執行個體不包含與任何特定CDN的整合，您可以使用您選擇的CDN。

設定CDN後，您必須從管理員完成設定。 您可以在全域或網站層級進行變更。 當CDN用於媒體儲存時，Commerce存放區頁面上的所有媒體路徑都會變更為設定中指定的CDN路徑。

## CDN工作流程

1. **瀏覽器要求媒體** — 商店的頁面會在客戶的瀏覽器中開啟，且瀏覽器會要求HTML中指定的媒體。
1. **傳送至CDN的要求；找到並提供影像** — 要求會先傳送至CDN。 如果CDN的儲存空間中有影像，則會將媒體檔案提供給客戶的瀏覽器。
1. **找不到媒體，要求傳送至[!DNL Commerce]網頁伺服器** — 如果CDN沒有媒體檔案，要求會傳送至[!DNL Commerce]網頁伺服器。 如果在檔案系統中找到媒體檔案，網頁伺服器會將其傳送給客戶的瀏覽器。

>[!IMPORTANT]
>
>為安全起見，當CDN用作媒體儲存時，如果CDN位於您的子網域之外，JavaScript可能無法正常運作。

## 設定內容傳遞網路

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板的&#x200B;_[!UICONTROL General]_&#x200B;下，選擇&#x200B;**[!UICONTROL Web]**。

1. 在左上角，視需要設定&#x200B;**[!UICONTROL Store View]**。

1. 展開![展開選取器](../assets/icon-display-expand.png) **[!UICONTROL Base URLs]**&#x200B;區段，然後執行下列動作：

   ![一般設定 — 網頁基底URL](./assets/web-base-urls.png){width="600" zoomable="yes"}

   - 以儲存靜態檢視檔案之CDN上位置的URL更新&#x200B;**[!UICONTROL Base URL for Static View Files]**。

   - 以CDN上JavaScript檔案的URL更新&#x200B;**[!UICONTROL Base URL for User Media Files]**。

     這兩個欄位都可以保留空白，或以預留位置開頭： `{% raw %}{{unsecure_base_url}}{% endraw %}`

1. 展開![展開選取器](../assets/icon-display-expand.png) **[!UICONTROL Base URLs (Secure)]**&#x200B;區段，然後執行下列動作：

   ![一般設定 — Web基底URL （安全）](./assets/web-base-urls-secure.png){width="600" zoomable="yes"}

   - 以儲存靜態檢視檔案之CDN上位置的URL更新&#x200B;**[!UICONTROL Secure Base URL for Static View Files]**。

   - 以CDN上JavaScript檔案的URL更新&#x200B;**[!UICONTROL Secure Base URL for User Media Files]**。

     這兩個欄位都可以保留空白，或以預留位置開頭： `{% raw %}{{unsecure_base_url}}{% endraw %}`

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。
