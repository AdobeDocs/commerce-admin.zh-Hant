---
title: 使用內容傳遞網路
description: 瞭解如何使用內容傳遞網路(CDN)來儲存媒體檔案。
exl-id: cb612b79-f3e3-4f1b-8cf9-d47886486686
feature: Page Content, Media, Configuration
level: Experienced
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# 使用內容傳遞網路

內容傳遞網路(CDN)可用來儲存媒體檔案。 雲端基礎結構上的Adobe Commerce包括Fastly CDN (請參閱 [Fastly](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/cdn/fastly.html) 在 _雲端基礎結構上的Commerce指南_)。 已安裝的Commerce例項 _內部部署_ 不包含與任何特定CDN的整合，您可以使用您選擇的CDN。

設定CDN後，您必須從管理員完成設定。 您可以在全域或網站層級進行變更。 當CDN用於媒體儲存時，Commerce商店頁面上的所有媒體路徑都會變更為設定中指定的CDN路徑。

## CDN工作流程

1. **瀏覽器要求媒體**  — 商店中的頁面會在客戶的瀏覽器中開啟，瀏覽器會要求HTML中指定的媒體。
1. **要求傳送至CDN；找到並處理影像**  — 要求會先傳送至CDN。 如果CDN的儲存空間中有影像，則會將媒體檔案提供給客戶的瀏覽器。
1. **找不到媒體，請求已傳送至 [!DNL Commerce] 網頁伺服器**  — 如果CDN沒有媒體檔案，系統會將要求傳送至 [!DNL Commerce] 網頁伺服器。 如果在檔案系統中找到媒體檔案，網頁伺服器會將其傳送給客戶的瀏覽器。

>[!IMPORTANT]
>
>為安全起見，當使用CDN作為媒體儲存空間時，如果CDN位於子網域之外，JavaScript可能無法正常運作。

## 設定內容傳遞網路

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中的 _[!UICONTROL General]_，選擇&#x200B;**[!UICONTROL Web]**.

1. 在左上角，設定 **[!UICONTROL Store View]** 視需要。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Base URLs]** 並執行下列動作：

   ![一般設定 — 網頁基底URL](./assets/web-base-urls.png){width="600" zoomable="yes"}

   - 更新 **[!UICONTROL Base URL for Static View Files]** 與CDN上儲存靜態檢視檔案的位置的URL。

   - 更新 **[!UICONTROL Base URL for User Media Files]** 與CDN上JavaScript檔案的URL搭配使用。

     這兩個欄位都可以保留空白，或以預留位置開頭： `{% raw %}{{unsecure_base_url}}{% endraw %}`

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Base URLs (Secure)]** 並執行下列動作：

   ![一般設定 — 網頁基底URL （安全）](./assets/web-base-urls-secure.png){width="600" zoomable="yes"}

   - 更新 **[!UICONTROL Secure Base URL for Static View Files]** 與CDN上儲存靜態檢視檔案的位置的URL。

   - 更新 **[!UICONTROL Secure Base URL for User Media Files]** 與CDN上JavaScript檔案的URL搭配使用。

     這兩個欄位都可以保留空白，或以預留位置開頭： `{% raw %}{{unsecure_base_url}}{% endraw %}`

1. 完成後，按一下 **[!UICONTROL Save Config]**.
