---
title: 網站地圖
description: 瞭解如何設定網站地圖，以索引Commerce網站的所有頁面和影像。
exl-id: 48c975ae-b088-4e52-80cf-cb19c2b9b00f
feature: Merchandising, Storefront, Search
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"
source-git-commit: 321a9fb0f3c6d86aad520b76ff717c0b07ac37f0
workflow-type: tm+mt
source-wordcount: '1209'
ht-degree: 0%

---

# 網站地圖

>[!TIP]
>
>如需Adobe Commerce as a Cloud Service的相關資訊，請參閱Commerce Storefront檔案中的[SEO指引](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/indexing/)

網站地圖可改善搜尋引擎為商店編制索引的方式，且設計旨在尋找可能被網頁爬蟲忽略的頁面。 網站地圖可設定為索引所有頁面和影像。

啟用後，Commerce會建立名為`sitemap.xml`的檔案，並將該檔案儲存在您指定的位置中的安裝中。 此設定可讓您設定更新的頻率，以及每種內容型別的優先順序。 您的網站地圖應隨著網站內容變更而經常更新，可能是每日、每週或每月更新。

當您的網站處於開發狀態時，您可能會在`robots.txt`檔案中為網頁爬蟲包含指示，以避免為網站編制索引。 在啟動之前，您可以變更指示，允許網站編制索引。

如需技術資訊，請參閱雲端基礎結構指南上的[Commerce](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/robots-sitemap.html)中的&#x200B;_新增Sitemap和robots.txt_。

![網站地圖格線](./assets/marketing-sitemap-grid-generated.png){width="700" zoomable="yes"}

## 步驟1. 設定網站地圖

完成[XML Sitemap設定](#site-map-configuration)，以判斷包含的內容以及網站地圖更新的頻率。

## 步驟2. 產生網站地圖

1. 在&#x200B;_管理員_&#x200B;功能表中，前往&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Site Map]**。

1. 按一下&#x200B;**[!UICONTROL Add Site Map]**。

   ![網站地圖格線](./assets/marketing-sitemap.png){width="700" zoomable="yes"}

1. 輸入網站地圖&#x200B;**[!UICONTROL Filename]**。 例如： `sitemap.xml`

1. 輸入&#x200B;**[!UICONTROL Path]**&#x200B;以決定網站地圖檔案在伺服器上的位置。 請確定路徑是可寫入的。

   - `/sitemap/` — 將網站地圖檔案放置在名為&#x200B;_網站地圖_&#x200B;的目錄中。

   - `/` — 將網站地圖檔案放置在基礎路徑或Commerce安裝的根目錄下。

   ![新網站地圖](./assets/marketing-sitemap-new.png){width="600" zoomable="yes"}

1. 完成時，按一下&#x200B;**[!UICONTROL Save & Generate]**。

   網站地圖可能需要幾分鐘才會顯示在格線中。

## 步驟3. 設定和啟用robots.txt （選擇性）

完成[搜尋引擎Robots](seo-overview.md#search-engine-robots)設定，並指示搜尋引擎抓取您要編制索引的網站部分。

## 步驟4. 將您的網站地圖提交至搜尋引擎

您可以在您的Commerce安裝中提供指向`sitemap.xml`檔案的連結，藉此將您的網站地圖提交至不同的搜尋引擎。 若要複製連結，請執行下列動作：

1. 在&#x200B;_網站地圖_&#x200B;清單中，用滑鼠右鍵按一下&#x200B;**[!UICONTROL Link for Google]**&#x200B;欄中的URL。

1. 在功能表上，選擇&#x200B;**[!UICONTROL Copy Link Address]**。

如需詳細資訊，請參閱特定搜尋引擎的說明。 以下是兩個主要搜尋引擎的指示連結：

- [Google](https://support.google.com/webmasters/answer/183669?hl=en)
- [Microsoft® Bing](https://www.bing.com/webmasters/help/Sitemaps-3b5cf6ed)

## 步驟5：還原先前的自動機制指示（選擇性）

您現在可以還原原始（預設）限制。

## 管理多個網站的Sitemap和robots.txt

如果您有多個網站，可以簡化建立和提交網站應用程式的程式。 只需[建立](#site-map-configuration)一或多個Sitemap （包含所有已驗證存放區的URL），並將這些Sitemap儲存至單一位置。 必須在[Google搜尋主控台](https://support.google.com/webmasters/answer/7451001)中驗證所有網站。

若要為多存放區執行處理建立網站地圖，請執行下列動作：

1. 在網站的根目錄建立名為`sitemaps`的資料夾，然後為每個網域建立子資料夾：

       /sitemaps/domain_1/
       /sitemaps/domain_2/
   
1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Site Map]**。

1. 建立或編輯每個商店的Sitemap清單，並將&#x200B;**[!UICONTROL Path]**&#x200B;設定為您為商店建立的清單：

   `/sitemaps/domain_1/`
   `/sitemaps/domain_2/`

1. 如有需要，請更新您的robots.txt檔案。

   若要確保搜尋引擎編目程式已正確導向至新的Sitemap，您可以更新或建立robots.txt檔案。 在頂端新增下列行。

       網站網站地圖
       網站地圖： https://www.domain_1.com/sitemaps/domain_1/sitemap.xml
       網站地圖： https://www.domain_2.com/sitemaps/domain_2/sitemap.xml
   
>[!NOTE]
>
>如果您的網站使用[Apache](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/web-server/apache.html)網頁伺服器引擎，您應該更新網站根目錄中的[`.htaccess`](https://httpd.apache.org/docs/current/howto/htaccess.html)檔案，將任何其他Sitemap要求導向適當的位置。

## 欄說明

| 欄 | 說明 |
|------|-----------|
| [!UICONTROL ID] | 目前網站地圖的連續記錄編號。 |
| [!UICONTROL Filename] | 網站地圖的檔案名稱。 |
| [!UICONTROL Path] | 網站地圖在伺服器上的位置。 例如： <br/>`/sitemap/` — 將網站地圖檔案放置在名為&#x200B;_網站地圖_&#x200B;的目錄中，此目錄位於Commerce安裝根目錄下的一個層級。 <br/>`/` — 將網站地圖檔案放置在基礎路徑或Commerce安裝的根目錄中。 |
| [!UICONTROL Link for Google] | 要提交至Google和其他搜尋引擎的網站地圖URL。 |
| [!UICONTROL Last Generated] | 表示上次產生網站地圖的日期和時間。 |
| [!UICONTROL Store View] | 網站地圖套用的商店檢視。 |
| [!UICONTROL Generate] | 重新產生網站地圖。 |

{style="table-layout:auto"}

## 網站地圖設定

您的網站地圖應隨著網站內容變更而經常更新，可能是每日、每週或每月更新。 此設定可讓您設定每種內容型別的頻率和優先順序。

### 步驟1. 設定內容更新的頻率和優先順序

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Catalog]**&#x200B;並選擇&#x200B;**[!UICONTROL XML Sitemap]**。

1. 展開![展開選取器](../assets/icon-display-expand.png) **[!UICONTROL Categories Options]**&#x200B;區段，然後執行下列動作：

   >[!NOTE]
   >
   >如有需要，請清除&#x200B;**[!UICONTROL Use system value]**&#x200B;核取方塊以變更這些設定。

   - 將&#x200B;**[!UICONTROL Frequency]**&#x200B;設定為下列其中一項：

      - `Always`
      - `Hourly`
      - `Daily`
      - `Weekly`
      - `Monthly`
      - `Yearly`
      - `Never`

   - 針對&#x200B;**[!UICONTROL Priority]**，請輸入介於`0.0`到`1.0`之間的值。 零的優先順序最低。

   ![XML Sitemap — 類別選項](../configuration-reference/catalog/assets/xml-sitemap-categories-options.png){width="600" zoomable="yes"}

   如需這些選項的詳細清單，請參閱[組態參考](../configuration-reference/catalog/xml-sitemap.md#categories-options)中的&#x200B;_類別選項_。

1. 展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Products Options]**&#x200B;區段，並視需要完成&#x200B;**[!UICONTROL Frequency]**&#x200B;和&#x200B;**[!UICONTROL Priority]**&#x200B;設定。

   如需這些選項的詳細清單，請參閱[組態參考](../configuration-reference/catalog/xml-sitemap.md#products-options)中的&#x200B;_產品選項_。

1. 若要判斷網站地圖中包含影像的範圍，請將&#x200B;**[!UICONTROL Add Images into Sitemap]**&#x200B;設定為下列其中一項：

   - `None`
   - `Base Only`
   - `All`

   ![目錄組態 — XML Sitemap產品](../configuration-reference/catalog/assets/xml-sitemap-products-options.png){width="600" zoomable="yes"}

1. 展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL CMS Pages Options]**&#x200B;區段，並視需要完成&#x200B;**[!UICONTROL Frequency]**&#x200B;和&#x200B;**[!UICONTROL Priority]**&#x200B;設定。

   ![目錄設定 — XML Sitemap CMS頁面](../configuration-reference/catalog/assets/xml-sitemap-cms-pages-options.png){width="600" zoomable="yes"}

   如需這些選項的詳細清單，請參閱[設定參考](../configuration-reference/catalog/xml-sitemap.md#cms-pages-options)中的&#x200B;_CMS頁面選項_。

1. 展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Store Url Options]**&#x200B;區段，並視需要完成&#x200B;**[!UICONTROL Frequency]**&#x200B;和&#x200B;**[!UICONTROL Priority]**&#x200B;設定。

   ![目錄組態 — XML Sitemap存放區URL](./assets/xml-sitemap.png){width="600" zoomable="yes"}

   如需這些選項的詳細清單，請參閱[組態參考](../configuration-reference/catalog/xml-sitemap.md#store-url-options)中的&#x200B;_儲存URL選項_。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

### 步驟2. 完成產生設定

1. 展開![區段的](../assets/icon-display-expand.png)擴充選擇器&#x200B;**[!UICONTROL Generation Settings]**。

   如有需要，請清除&#x200B;**使用系統值**&#x200B;核取方塊以變更這些設定。

   ![目錄組態 — XML Sitemap產生設定](../configuration-reference/catalog/assets/xml-sitemap-generation-settings.png){width="600" zoomable="yes"}

   如需這些選項的詳細清單，請參閱[組態參考](../configuration-reference/catalog/xml-sitemap.md#generation-settings)中的&#x200B;_產生設定_。

1. 若要產生Sitemap，請將&#x200B;**[!UICONTROL Enabled]**&#x200B;設為`Yes`並執行下列動作：

   - 將&#x200B;**[!UICONTROL Start Time]**&#x200B;設定為您要更新Sitemap的時、分、秒。

   - 將&#x200B;**[!UICONTROL Frequency]**&#x200B;設定為下列其中一項：

      - `Daily`
      - `Weekly`
      - `Monthly`

   - 針對&#x200B;**[!UICONTROL Error Email Recipient]**，輸入在Sitemap更新期間發生錯誤時接收通知之人員的電子郵件地址。

   - 將&#x200B;**[!UICONTROL Error Email Sender]**&#x200B;設定為顯示為錯誤通知寄件者的商店連絡人。

   - 將&#x200B;**[!UICONTROL Error Email Template]**&#x200B;設為錯誤通知所使用的範本。

### 步驟3. 設定網站地圖檔案限制

1. 展開![區段的](../assets/icon-display-expand.png)擴充選擇器&#x200B;**[!UICONTROL Sitemap File Limits]**。

   ![目錄組態 — XML Sitemap檔案限制](../configuration-reference/catalog/assets/xml-sitemap-sitemap-file-limits.png){width="600" zoomable="yes"}

   如需這些選項的詳細清單，請參閱[組態參考](../configuration-reference/catalog/xml-sitemap.md#sitemap-file-limits)中的&#x200B;_網站地圖檔案限制_。

1. 針對&#x200B;**[!UICONTROL Maximum No of URLs per File]**，輸入網站地圖中可包含的URL數目上限。

   預設的限製為50,000。

1. 針對&#x200B;**[!UICONTROL Maximum File Size]**，輸入為Sitemap配置的最大位元組大小。

   預設大小為10,485,760位元組。

### 步驟4. 設定搜尋引擎提交設定

1. 展開![區段的](../assets/icon-display-expand.png)擴充選擇器&#x200B;**[!UICONTROL Search Engine Submission Settings]**。

   ![目錄組態 — XML Sitemap搜尋引擎提交設定](../configuration-reference/catalog/assets/xml-sitemap-search-engine-submission-settings.png){width="600" zoomable="yes"}

1. 如果使用`robots.txt`檔案向抓取您網站的搜尋引擎提供指示，請將&#x200B;**[!UICONTROL Enable Submission to Robots.txt]**&#x200B;設為`Yes`。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。
