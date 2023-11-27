---
title: 網站地圖
description: 瞭解如何設定網站地圖，以索引您的Commerce網站的所有頁面和影像。
exl-id: 48c975ae-b088-4e52-80cf-cb19c2b9b00f
feature: Merchandising, Storefront, Search
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '1207'
ht-degree: 0%

---

# 網站地圖

網站地圖可改善搜尋引擎為商店編制索引的方式，且設計旨在尋找可能被網頁編目程式忽略的頁面。 網站地圖可設定為索引所有頁面和影像。

啟用後，Commerce會建立名為的檔案 `sitemap.xml` 會以您指定的位置儲存至您的安裝。 此設定可讓您設定更新的頻率，以及每種內容型別的優先順序。 您的網站地圖應隨著網站內容變更而經常更新，可能是每日、每週或每月更新。

當您的網站處於開發狀態時，您可能會在 `robots.txt` 檔案供Web編目程式使用，以避免為網站編制索引。 在啟動之前，您可以變更指示，允許網站編制索引。

如需技術資訊，請參閱 [新增Sitemap和robots.txt][1] 在 _雲端基礎結構上的Commerce指南_.

![網站地圖格線](./assets/marketing-sitemap-grid-generated.png){width="700" zoomable="yes"}

## 步驟1. 設定網站地圖

完成 [XML Sitemap設定](#site-map-configuration) 以判斷包含的內容，以及網站地圖的更新頻率。

## 步驟2. 產生網站地圖

1. 在 _管理員_ 選單，前往 **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Site Map]**.

1. 按一下 **[!UICONTROL Add Site Map]**.

   ![網站地圖格線](./assets/marketing-sitemap.png){width="700" zoomable="yes"}

1. 輸入網站地圖 **[!UICONTROL Filename]**. 例如： `sitemap.xml`

1. 輸入 **[!UICONTROL Path]** 以判斷網站地圖檔案在伺服器上的存放位置。 請確定路徑是可寫入的。

   - `/sitemap/`  — 將網站地圖檔案放置在名為的目錄中 _Sitemap_.

   - `/`  — 將網站地圖檔案放置在基礎路徑或Commerce安裝的根目錄下。

   ![新增網站地圖](./assets/marketing-sitemap-new.png){width="600" zoomable="yes"}

1. 完成後，按一下 **[!UICONTROL Save & Generate]**.

   網站地圖可能需要幾分鐘才會顯示在格線中。

## 步驟3. 設定和啟用robots.txt （選擇性）

完成 [搜尋引擎機器人](seo-overview.md#search-engine-robots) 使用指示進行設定，指示搜尋引擎對您要建立索引的網站部分進行編目。

## 步驟4. 將您的網站地圖提交至搜尋引擎

您可以向不同的搜尋引擎提交網站地圖，方法是提供網站地圖的 `sitemap.xml` 檔案中指定的URL位置。 若要複製連結，請執行下列動作：

1. 在 _網站地圖_ 清單中，以滑鼠右鍵按一下 **[!UICONTROL Link for Google]** 欄。

1. 在功能表中，選擇 **[!UICONTROL Copy Link Address]**.

如需詳細資訊，請參閱特定搜尋引擎的說明。 以下是兩個主要搜尋引擎的指示連結：

- [Google][2]
- [Microsoft® Bing][3]

## 步驟5：還原先前的自動機制指示（選擇性）

您現在可以還原原始（預設）限制。

## 管理多個網站的Sitemap和robots.txt

如果您有多個網站，可以簡化建立和提交網站應用程式的程式。 簡單 [建立](#site-map-configuration) 一或多個網站地圖包含所有已驗證存放區的URL，並將網站地圖儲存至單一位置。 所有網站都必須在中驗證 [Google Search Console](https://support.google.com/webmasters/answer/7451001).

若要為多存放區執行處理建立網站地圖，請執行下列動作：

1. 建立名為的資料夾 `sitemaps` 然後，在網站的根目錄下為每個網域建立子資料夾：

       /sitemaps/domain_1/
       /sitemaps/domain_2/
   
1. 在 _管理員_ 側欄，前往 **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Site Map]**.

1. 建立或編輯每個商店的網站地圖清單，並設定 **[!UICONTROL Path]** 至您為存放區建立的專案：

   `/sitemaps/domain_1/`
   `/sitemaps/domain_2/`

1. 如有需要，請更新您的robots.txt檔案。

   若要確保搜尋引擎編目程式已正確導向至新的Sitemap，您可以更新或建立robots.txt檔案。 在頂端新增下列行。

       網站網站地圖
       網站地圖： https://www.domain_1.com/sitemaps/domain_1/sitemap.xml
       網站地圖： https://www.domain_2.com/sitemaps/domain_2/sitemap.xml
   
>[!NOTE]
>
>如果您的網站使用 [Apache](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/web-server/apache.html) 網頁伺服器引擎，請更新 [`.htaccess`](https://httpd.apache.org/docs/current/howto/htaccess.html) 將任何其他Sitemap要求導向至適當位置的網站根目錄中的檔案。

## 欄說明

| 欄 | 說明 |
|------|-----------|
| [!UICONTROL ID] | 目前網站地圖的連續記錄編號。 |
| [!UICONTROL Filename] | 網站地圖的檔案名稱。 |
| [!UICONTROL Path] | 網站地圖在伺服器上的位置。 例如： <br/>`/sitemap/`  — 將網站地圖檔案放置在名為的目錄中 _Sitemap_，比Commerce安裝的根目錄低一個層級。 <br/>`/`  — 將網站地圖檔案放在基本路徑或Commerce安裝的根目錄下。 |
| [!UICONTROL Link for Google] | 要提交至Google和其他搜尋引擎的網站地圖URL。 |
| [!UICONTROL Last Generated] | 表示上次產生網站地圖的日期和時間。 |
| [!UICONTROL Store View] | 網站地圖套用的商店檢視。 |
| [!UICONTROL Generate] | 重新產生網站地圖。 |

{style="table-layout:auto"}

## 網站地圖設定

您的網站地圖應隨著網站內容變更而經常更新，可能是每日、每週或每月更新。 此設定可讓您設定每種內容型別的頻率和優先順序。

### 步驟1. 設定內容更新的頻率和優先順序

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Catalog]** 並選擇 **[!UICONTROL XML Sitemap]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Categories Options]** 並執行下列動作：

   >[!NOTE]
   >
   >如有需要，請清除 **[!UICONTROL Use system value]** 核取方塊以變更這些設定。

   - 設定 **[!UICONTROL Frequency]** 變更為下列其中一項：

      - `Always`
      - `Hourly`
      - `Daily`
      - `Weekly`
      - `Monthly`
      - `Yearly`
      - `Never`

   - 的 **[!UICONTROL Priority]**，請輸入介於以下範圍的值： `0.0` 和 `1.0`. 零的優先順序最低。

   ![XML Sitemap — 類別選項](../configuration-reference/catalog/assets/xml-sitemap-categories-options.png){width="600" zoomable="yes"}

   如需這些選項的詳細清單，請參閱 [類別選項](../configuration-reference/catalog/xml-sitemap.md#categories-options) 在 _設定參考_.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Products Options]** 區段並填妥 **[!UICONTROL Frequency]** 和 **[!UICONTROL Priority]** 設定。

   如需這些選項的詳細清單，請參閱 [產品選項](../configuration-reference/catalog/xml-sitemap.md#products-options) 在 _設定參考_.

1. 若要判斷影像包含在網站地圖中的範圍，請設定 **[!UICONTROL Add Images into Sitemap]** 變更為下列其中一項：

   - `None`
   - `Base Only`
   - `All`

   ![目錄設定 — XML Sitemap產品](../configuration-reference/catalog/assets/xml-sitemap-products-options.png){width="600" zoomable="yes"}

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL CMS Pages Options]** 區段並填妥 **[!UICONTROL Frequency]** 和 **[!UICONTROL Priority]** 設定。

   ![目錄組態 — XML Sitemap CMS頁面](../configuration-reference/catalog/assets/xml-sitemap-cms-pages-options.png){width="600" zoomable="yes"}

   如需這些選項的詳細清單，請參閱 [CMS頁面選項](../configuration-reference/catalog/xml-sitemap.md#cms-pages-options) 在 _設定參考_.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Store Url Options]** 區段並填妥 **[!UICONTROL Frequency]** 和 **[!UICONTROL Priority]** 設定。

   ![目錄設定 — XML網站地圖存放區URL](./assets/xml-sitemap.png){width="600" zoomable="yes"}

   如需這些選項的詳細清單，請參閱 [儲存Url選項](../configuration-reference/catalog/xml-sitemap.md#store-url-options) 在 _設定參考_.

1. 完成後，按一下 **[!UICONTROL Save Config]**.

### 步驟2. 完成產生設定

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Generation Settings]** 區段。

   如有需要，請清除 **使用系統值** 核取方塊以變更這些設定。

   ![目錄組態 — XML Sitemap產生設定](../configuration-reference/catalog/assets/xml-sitemap-generation-settings.png){width="600" zoomable="yes"}

   如需這些選項的詳細清單，請參閱 [產生設定](../configuration-reference/catalog/xml-sitemap.md#generation-settings) 在 _設定參考_.

1. 若要產生網站地圖，請設定 **[!UICONTROL Enabled]** 至 `Yes` 並執行下列動作：

   - 設定 **[!UICONTROL Start Time]** 到您希望Sitemap更新的小時、分鐘和秒。

   - 設定 **[!UICONTROL Frequency]** 變更為下列其中一項：

      - `Daily`
      - `Weekly`
      - `Monthly`

   - 的 **[!UICONTROL Error Email Recipient]**，輸入在Sitemap更新期間發生錯誤時收到通知之人員的電子郵件地址。

   - 設定 **[!UICONTROL Error Email Sender]** 給顯示為錯誤通知寄件者的商店連絡人。

   - 設定 **[!UICONTROL Error Email Template]** 至用於錯誤通知的範本。

### 步驟3. 設定網站地圖檔案限制

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Sitemap File Limits]** 區段。

   ![目錄設定 — XML Sitemap檔案限制](../configuration-reference/catalog/assets/xml-sitemap-sitemap-file-limits.png){width="600" zoomable="yes"}

   如需這些選項的詳細清單，請參閱 [Sitemap檔案限制](../configuration-reference/catalog/xml-sitemap.md#sitemap-file-limits) 在 _設定參考_.

1. 的 **[!UICONTROL Maximum No of URLs per File]**，請輸入網站地圖中可包含的最大URL數量。

   預設的限製為50,000。

1. 的 **[!UICONTROL Maximum File Size]**，輸入為Sitemap配置的最大位元組大小。

   預設大小為10,485,760位元組。

### 步驟4. 設定搜尋引擎提交設定

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Search Engine Submission Settings]** 區段。

   ![目錄設定 — XML Sitemap搜尋引擎提交設定](../configuration-reference/catalog/assets/xml-sitemap-search-engine-submission-settings.png){width="600" zoomable="yes"}

1. 若使用 `robots.txt` 檔案以向編目您網站的搜尋引擎提供指示，請設定 **[!UICONTROL Enable Submission to Robots.txt]** 至 `Yes`.

1. 完成後，按一下 **[!UICONTROL Save Config]**.

[1]: https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/robots-sitemap.html
[2]: https://support.google.com/webmasters/answer/183669?hl=en
[3]: https://www.bing.com/webmasters/help/Sitemaps-3b5cf6ed
