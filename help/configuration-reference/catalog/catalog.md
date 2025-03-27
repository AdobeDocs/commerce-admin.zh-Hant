---
title: '[!UICONTROL Catalog] &amp；gt； [!UICONTROL Catalog]'
description: 檢閱Commerce管理員的[!UICONTROL Catalog] &amp；gt； [!UICONTROL Catalog]頁面上的組態設定。
exl-id: fc25ae80-aaa7-42c4-bba2-f03d3caa7970
feature: Configuration, Catalog Management
source-git-commit: 20f97d6ab391b7f5675d6790ab2ec5d24e9dda21
workflow-type: tm+mt
source-wordcount: '3261'
ht-degree: 0%

---

# [!UICONTROL Catalog] > [!UICONTROL Catalog]

{{config}}

## [!UICONTROL Product Fields Auto-Generation]

![產品欄位自動產生](./assets/catalog-product-fields-auto-generation.png)<!-- zoom -->

<!-- [Product Fields Auto-Generation](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/products/product-workspace#default-field-values) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Mask for SKU] | 全域 | 根據其他欄位的預留位置值和輸入的任何其他文字來決定SKU欄位的預設值。 預設預留位置： <br/>產品名稱 — `{{name}}` |
| [!UICONTROL Mask for Meta Title] | 全域 | 根據其他欄位的預留位置值和輸入的任何其他文字來決定「中繼標題」欄位的預設值。 預設預留位置： <br/>產品名稱 — `{{name}}` |
| [!UICONTROL Mask for Meta Keywords] | 全域 | 根據其他欄位的預留位置值和輸入的任何其他文字，決定&#x200B;_中繼關鍵字_&#x200B;欄位的預設值。 預設預留位置： <br/>產品名稱 — `{{name}}` |
| [!UICONTROL Mask for Meta Description] | 全域 | 根據其他欄位的預留位置值和輸入的任何其他文字來決定「中繼說明」欄位的預設值。 預設預留位置： <br/>產品名稱 — `{{name}}` <br/>說明 — `{{description}}` |

{style="table-layout:auto"}

## [!UICONTROL Product Reviews]

![產品評論](./assets/catalog-product-reviews.png)<!-- zoom -->

<!-- [Product Reviews](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/merchandising/product-reviews/product-reviews) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 存放區檢視 | 啟用產品評論。 選項： `Yes` / `No` |
| [!UICONTROL Allow Guests to Write Reviews] | 網站 | 決定客戶是否必須在您的商店開立帳戶才能撰寫產品評論。 |

{style="table-layout:auto"}

## [!UICONTROL Storefront]

![店面](./assets/catalog-storefront.png)<!-- zoom -->

<!-- [Storefront](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/catalog/navigation/navigation-product-listings) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL List Mode] | 存放區檢視 | 決定搜尋結果清單的格式。 選項： <br/>**`Grid Only`**— 將清單格式化為列與欄的網格。 每個產品都會顯示在網格的單一儲存格中。<br/>**`List Only`** — 將清單格式化，每個產品放在個別的列上。 <br/>**`Grid (default / List)`**— 依預設，產品會出現在格線檢視中，而且可以切換到[清單]檢視。<br/>**`List (default / Grid)`** — 依預設，產品會出現在清單檢視中，而且可以切換至格線檢視。 |
| [!UICONTROL Products per Page on Grid Allowed Values] | 存放區檢視 | 決定格線檢視中顯示的產品數目。 若要提供選項選擇，請輸入多個值，並以逗號分隔。 |
| [!UICONTROL Products per Page on Grid Default Value] | 存放區檢視 | 決定網格檢視中預設每頁顯示的產品數目。 |
| [!UICONTROL Products per Page on List Allowed Values] | 存放區檢視 | 決定清單檢視中顯示的產品數目。 若要提供選項選擇，請輸入多個值，並以逗號分隔。 |
| [!UICONTROL Products per Page on List Default Value] | 存放區檢視 | 決定清單檢視中預設每頁顯示的產品數目。 |
| 產品清單排序依據 | 存放區檢視 | 決定搜尋結果清單的排序順序。 選項的選取是由類別的顯示設定和設定為`Used for Sorting in Product Listing`的可用屬性所決定。 預設值設為`Use All Available Attributes`，通常包含最佳值、名稱、價格。 此設定不適用於[!DNL Live Search] [產品清單頁面Widget](https://experienceleague.adobe.com/en/docs/commerce/live-search/live-search-storefront/plp-styling)。 |
| [!UICONTROL Allow All Products per Page] | 存放區檢視 | 如果設為`Yes`，則在「每頁顯示」控制項中包含`ALL`選項。 |
| [!UICONTROL Remember Category Pagination] | 全域 | 如果設為`Yes`，目前的類別分頁值會儲存為客戶在[產品清單](../../catalog/navigation-product-listings.md)中從一個類別瀏覽到另一個類別。 儲存此值會使用更多快取儲存空間，並可能影響搜尋引擎為頁面編制索引的方式。 選項： `Yes` / `No` （預設） |
| [!UICONTROL Use Flat Catalog Category] | 全域 | 啟用[一般類別結構](../../catalog/catalog-flat.md) （不建議使用）。 選項： `Yes` / `No` |
| [!UICONTROL Use Flat Catalog Product] | 全域 | 啟用平坦產品結構。 （不建議）選項： `Yes` / `No` |
| [!UICONTROL Swatches per Product] | 存放區檢視 | 決定每個產品可用的色票數。 預設： `16` |
| [!UICONTROL Show Swatches in Product List] | 存放區檢視 | 決定色票是否出現在「產品清單」中。 選項： `Yes` / `No` |
| [!UICONTROL Show Swatch Tooltip] | 存放區檢視 | 決定是否顯示色票工具提示。 選項： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Product Alerts]

![產品警示](./assets/catalog-product-alerts.png)<!-- zoom -->

<!-- [Product Alerts](https://experienceleague.adobe.com/en/docs/commerce-admin/inventory/configuration/product-alerts/alert-setup) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Allow Alerts When Product Price Changes] | 存放區檢視 | 判斷是否針對產品價格變更提供電子郵件警示。 選項： `Yes` / `No` |
| [!UICONTROL Price Alert Email Template] | 存放區檢視 | 識別用於產品價格變更電子郵件警示的範本。 預設範本： `Product price alert` |
| [!UICONTROL Allow Alert When Product Comes Back in Stock] | 網站 | 決定客戶是否可選擇在產品補貨時收到警報。 選項： `Yes` / `No` |
| [!UICONTROL Stock Alert Email Template] | 存放區檢視 | 識別用於庫存警示電子郵件通知的範本。 預設範本： `Product stock alert` |
| [!UICONTROL Alert Email Sender] | 存放區檢視 | 決定商店聯絡人，顯示為產品警示電子郵件訊息的寄件者。 選項： `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email` |

{style="table-layout:auto"}

## [!UICONTROL Product Alerts Run Settings]

![產品警示執行設定](./assets/catalog-product-alerts-run-settings.png)<!-- zoom -->

<!-- [Product Alerts Run Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/inventory/configuration/product-alerts/alert-setup) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Frequency] | 全域 | 選擇產品警報的傳送頻率。 選項： `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Start Time] | 全域 | 選擇產品警示程式在一天中的開始時間。 此時間應在執行任何價格或存貨更新之後。 |
| [!UICONTROL Error Email Recipient] | 全域 | 識別當產品警示程式發生錯誤時，應接收電子郵件通知之人員（通常是商店管理員）的電子郵件地址。 |
| [!UICONTROL Error Email Sender] | 全域 | 選取電子郵件為`from`的角色。 |
| [!UICONTROL Error Email Template] | 全域 | 選取用於產品警示錯誤通知的電子郵件範本。 |

{style="table-layout:auto"}

## [!UICONTROL Product Image Placeholders]

![產品影像預留位置](./assets/catalog-product-image-placeholders.png)<!-- zoom -->

<!-- [Product Image Placeholders](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/products/digital-assets/product-image-config#image-placeholders) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Base Image] | 存放區檢視 | 識別為基本影像選擇的預留位置檔案。 |
| [!UICONTROL Small Image] | 存放區檢視 | 識別為小影像選擇的預留位置檔案。 |
| [!UICONTROL Swatch] | 存放區檢視 | 識別為色票選擇的預留位置檔案。 |
| [!UICONTROL Thumbnail] | 存放區檢視 | 識別為縮圖選擇的預留位置檔案。 |
| [!UICONTROL Choose File] |  | 導覽至檔案，並將其上傳為型別的預留位置影像。 |

{style="table-layout:auto"}

## [!UICONTROL Recently Viewed/Compared Products]

![最近檢視/比較的產品](./assets/catalog-recently-viewed-and-compared-products.png)<!-- zoom -->

<!-- Recently Viewed/Compared Products](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/shopper-tools/products-viewed-compared) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Synchronize widget products with backend storage] | 全域 | 決定產品Widget資訊（例如產品ID）與資料庫的同步處理。 如此可重複使用其他裝置上的資訊。 |
| [!UICONTROL Show for Current] | 網站 | 限制目前網站顯示的產品。 選項： `Website` / `Store` / `Store View` |
| [!UICONTROL Default Recently Viewed Products Count] | 存放區檢視 | 決定清單中最近檢視的產品最大數量。 |
| [!UICONTROL Default Recently Compared Products Count] | 存放區檢視 | 決定清單中最近比較的產品數目上限。 |
| [!UICONTROL Lifetime of products in Recently Viewed Widget] | 全域 | 決定已檢視產品在最近檢視的清單中顯示的時間長度（以秒為單位）。 |
| [!UICONTROL Lifetime of products in Recently Compared Widget] | 全域 | 決定最近比較的產品清單中顯示比較產品的時間（秒）。 |

{style="table-layout:auto"}

## [!UICONTROL Product Video]

![產品影片](./assets/catalog-product-video.png)<!-- zoom -->

<!-- [Product Videos](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/products/digital-assets/product-video) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL YouTube API key] | 存放區檢視 | 指定連線到YouTube伺服器所需的API金鑰。 |
| [!UICONTROL Autostart base video] | 存放區檢視 | 若要在頁面載入後自動啟動視訊，請設為`Yes`。 |
| [!UICONTROL Show related video] | 存放區檢視 | 若要顯示相關視訊，請設定為`Yes`。 |
| [!UICONTROL Auto restart video] | 存放區檢視 | 若要啟用自動重播視訊，請將設為`Yes`。 |

{style="table-layout:auto"}

## [!UICONTROL Price]

![價格](./assets/catalog-price.png)<!-- zoom -->

<!--Price](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/products/pricing/catalog-price-scope) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Catalog Price Scope] | 全域 | 決定基本貨幣的範圍。 選項： `Global` / `Website` |
| [!UICONTROL Default Product Price] | 全域 | ![Adobe Commerce](../../assets/adobe-logo.svg) (僅限Adobe Commerce)定義預設產品價格（若適用）。 |

{style="table-layout:auto"}

## [!UICONTROL Layered Navigation]

>[!NOTE]
>
>本節中說明的標準搜尋組態與[即時搜尋](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html)不同。

<!-- [Layered Navigation - Automatic (equalize price ranges)](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/catalog/navigation/navigation-layered#configure-layered-navigation) -->

![分層導覽 — 自動（均衡價格範圍）](./assets/layered-navigation-equalize-price-range.png)<!-- zoom -->

![分層導覽 — 自動（均衡產品計數）](./assets/layered-navigation-equalize-product-counts.png)<!-- zoom -->

![分層導覽 — 手動](./assets/layered-navigation-manual.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Display Product Count] | 存放區檢視 | 決定產品計數是否出現在每個屬性、價格範圍及分類之後。 選項： `Yes` / `No` |
| [!UICONTROL Price Navigation Step Calculation] | 存放區檢視 | 決定用來決定[價格導覽步驟](../../catalog/navigation-layered.md#configure-price-navigation)的方法。 選項： <br/>`Automatic (equalize price ranges)` — 以群組中產品的價格範圍為基礎進行計算。 <br/>`Automatic (equalize product counts)` — 根據群組中的產品數目進行計算。 建立群組中最小產品數量的臨界值，以防止將這些產品分成較小的群組。 <br/>`Manual` — 使用您為價格間隔輸入的除數限制。 |
| [!UICONTROL Default Price Navigation Step] | 存放區檢視 | 決定每個步驟中包含的產品數量。 |
| [!UICONTROL Maximum Number of Price Intervals] | 存放區檢視 | 建立出現在分層導覽的價格間隔數限制。 |

{style="table-layout:auto"}

## [!UICONTROL Category Permissions]

{{ee-feature}}

![類別許可權](./assets/catalog-category-permissions.png)<!-- zoom -->

<!-- [Category Permissions](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/categories/category-permissions) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable] | 全域 | 啟用類別限制。 依預設，使用此功能會限制所有類別。 選項： `Yes` / `No` |
| [!UICONTROL Allow Browsing Category] | 網站 | 決定允許誰瀏覽類別。 選項： <br/>`Yes, for Everyone` — 允許所有訪客和客戶瀏覽類別。 <br/>`Yes, for Specified Customer Groups` — 僅允許所選客戶群組的成員瀏覽類別。 <br/>`No, Redirect to Landing Page` — 拒絕類別存取權，並重新導向至選取的頁面。 |
| [!UICONTROL Display Product Prices] | 網站 | 控制類別產品價格的顯示。 選項： <br/>`Yes, for Everyone` — 允許所有人檢視類別中的產品價格。 <br/>`Yes, for Specified Customer Groups` — 僅允許所選客戶群組的成員檢視類別中的產品價格。 <br/>`No` — 關閉類別的產品價格顯示。 |
| [!UICONTROL Allow Adding to Cart] | 網站 | 決定誰可以從類別購買產品。 選項： <br/>`Yes, for Everyone` — 允許所有人將類別中的產品放入購物車。 <br/>`Yes, for Specified Customer Groups` — 僅允許所選客戶群組的成員將產品從類別放入其購物車。 <br/>`No` — 不允許任何人將類別中的產品放入購物車。 |
| [!UICONTROL Disallow Catalog Search by] | 網站 | 識別不允許在類別中搜尋產品的客戶群組。 |

{style="table-layout:auto"}

## [!UICONTROL Search Engine Optimization]

![搜尋引擎最佳化](./assets/catalog-search-engine-optimization.png)<!-- zoom -->

<!-- [Search Engine Optimization](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/products/settings/product-search-engine-optimization) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Popular Search Terms] | 存放區檢視 | 決定是否在存放區中實作&#x200B;_常用搜尋詞_。 此設定不適用於使用[即時搜尋](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html)的存放區。 選項： `Enable` / `Disable` |
| [!UICONTROL Product URL Suffix] | 存放區檢視 | 決定是否將尾碼（例如html或htm）套用至產品URL。 若使用，請勿在尾碼前加上句號，因為它會自動套用。 |
| [!UICONTROL Category URL Suffix] | 存放區檢視 | 決定是否將尾碼（例如html或htm）套用至類別URL。 若使用，請勿在尾碼前加上句號，因為它會自動套用。 |
| [!UICONTROL Use Categories Path for Product URLs] | 存放區檢視 | 判斷類別路徑是否包含在店面的產品URL中。 這麼做可能會讓多個URL指向相同頁面，因而影響搜尋排名。 若要深入瞭解，請參閱[Canonical meta標籤](../../merchandising-promotions/meta-data.md#canonical-meta-tag)。 |
| [!UICONTROL Create Permanent Redirect for URLs if URL Key Changed] | 存放區檢視 | 決定每當URL索引鍵變更時是否自動建立永久重新導向。 實作時，預設會選取產品URL金鑰欄位下方的「建立舊URL的自訂重新導向」核取方塊。 選項： `Yes` / `No` |
| [!UICONTROL Generate "category/product" URL Rewrites] | 全域 | 決定當使用者儲存包含許多指派產品的類別時，Adobe Commerce是否會產生資料並將其儲存到重寫表格中。  <br/><br/>變更此選項不會影響在Adobe Commerce中解析產品URL的方式，因為不論此設定為何，系統都會自動解析產品URL。 <br/><br/>選項： `Yes` / `No` <br/><br/>**_重要：_**將此產生的資料儲存至URL重寫資料表，可能會降低效能。 如需詳細資訊，請參閱[自動產品重新導向](../../merchandising-promotions/url-redirect-product-automatic.md)。 |
| [!UICONTROL Apply transliteration for product URL] | 存放區檢視 | 決定建立或更新產品URL時是否套用音譯。 選項： `Yes` / `No`。 預設值設為`Yes`。 <br/><br/>對於某些使用案例，您應該停用音譯。 例如，如果您以中文經營線上商店，SEO最佳實務建議產品URL符合產品名稱。 將選項設為`No`可讓產品URL中使用中文字元，而非ASCII等同專案。 |
| [!UICONTROL Page Title Separator] | 存放區檢視 | 識別在瀏覽器標題列中分隔類別名稱和子類別的字元。 |
| [!UICONTROL Use Canonical Link Meta Tag for Categories] | 存放區檢視 | 如果有多個URL指向相同的類別頁面，此選項會使用標準中繼標籤來識別搜尋引擎應編制索引的類別URL。 URL包含使用meta標籤的類別的完整名稱。 如此可減少重複內容並改善SEO。 選項： `Yes` / `No` |
| [!UICONTROL Use Canonical Link Meta Tag for Products] | 存放區檢視 | 如果有多個URL指向相同的產品頁面，此選項會使用標準中繼標籤來識別搜尋引擎應編制索引的產品URL。 URL包含使用meta標籤的產品全名。 如此可減少重複內容並改善SEO。 選項： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Category Top Navigation]

![類別頂端導覽](./assets/catalog-category-top-navigation.png)<!-- zoom -->

<!-- Category Top Navigation](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/catalog/navigation/navigation-top) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Maximal Depth] | 全域 | 決定頂端導覽列中的子類別層級數目。 預設值`0`對層級數目沒有限制。 |

{style="table-layout:auto"}

## [!UICONTROL Catalog Search]

您可以使用[[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html)或Adobe Commerce支援的協力廠商搜尋引擎服務來設定目錄搜尋。 請依照安裝說明操作。

### 具有[!DNL Live Search]的Adobe Commerce

安裝「即時搜尋」時，「目錄搜尋」會包含下列組態設定：

即時搜尋的![目錄搜尋](./assets/catalog-search-live-search.png)<!-- zoom -->

<!-- [Catalog Search for Live Search](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/catalog/search/search-configuration) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Minimal Query Length] | 存放區檢視 | 目錄搜尋中允許的最小字元數。 針對此選項設定的值必須與Elasticsearch搜尋引擎設定中設定的對應範圍相容。 例如，如果您在Adobe Commerce中將此值設為`2`，請更新搜尋引擎中的值。 |
| [!UICONTROL Maximum Query Length] | 存放區檢視 | 目錄搜尋中允許的最大字元數。 針對此選項設定的值必須與Elasticsearch搜尋引擎設定中設定的對應範圍相容。 例如，如果您在Adobe Commerce中將此值設為300，請更新搜尋引擎中的值。 |
| [!UICONTROL Number of top search results to cache] | 存放區檢視 | 快取以加快回應的熱門搜尋字詞和結果數目。 輸入值`0`會在第二次輸入時快取所有搜尋字詞和結果。 預設值： `100` |
| [!UICONTROL Autocomplete Limit] | 存放區檢視 | 決定[店面彈出視窗]頁面中可用的行數上限。 預設值可以在安裝「即時搜尋」時變更，並在稍後透過變更此組態設定進行更新。 預設值： `8` |

{style="table-layout:auto"}

### 協力廠商搜尋引擎

Adobe Commerce支援OpenSearch和Elasticsearch。 Adobe Commerce版本2.3.7-p3、2.4.3-p2以及2.4.4和更新版本支援OpenSearch服務。 雲端基礎結構專案的Adobe Commerce不支援Elasticsearch 7.11和更新版本。 內部部署安裝仍支援Elasticsearch。

>[!IMPORTANT]
>
>- 鑑於Elasticsearch 7於2023年8月宣佈終止支援，Adobe建議所有Adobe Commerce客戶移轉至OpenSearch 2.x搜尋引擎。 如需在升級期間移轉搜尋引擎的相關資訊，請參閱&#x200B;_升級指南_&#x200B;中的[移轉至OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html)。
>- 在2.4.4和2.4.3-p2版中，所有標示為Elasticsearch的欄位也適用於OpenSearch。 當版本2.4.6中引入Elasticsearch 8.x支援時，已建立新標籤以區分Elasticsearch和OpenSearch設定。 不過，兩者的設定選項是相同的。

![目錄搜尋組態選項](./assets/catalog-search-opensearch.png){zoomable="yes"}

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Minimal Query Length] | 存放區檢視 | 目錄搜尋中允許的最小字元數。 針對此選項設定的值必須與OpenSearch或Elasticsearch組態中設定的對應範圍相容。 例如，如果您在Adobe Commerce中將此值設為`2`，您也必須更新搜尋引擎設定中的值。 預設值： `3` |
| [!UICONTROL Maximum Query Length] | 存放區檢視 | 目錄搜尋中允許的最大字元數。 針對此選項設定的值必須與OpenSearch或Elasticsearch設定中設定的對應範圍相容。 例如，如果您在Adobe Commerce中將此值設為`300`，則必須更新搜尋引擎設定中的值。 預設值： `128` |
| [!UICONTROL Number of top search results to cache] | 存放區檢視 | 快取以加快回應的熱門搜尋字詞和結果數目。 輸入值`0`會在第二次輸入時快取所有搜尋字詞和結果。 預設值： `100` |
| [!UICONTROL Enable EAV Indexer] | 全域 | 決定是否啟用或停用「產品EAV」索引器。 此功能可提升索引速度，並限制第三方擴充功能不得使用索引器。 預設選項： `Yes`已啟用 |
| [!UICONTROL Autocomplete Limit] | 存放區檢視 | 搜尋自動完成的搜尋欄位下方可顯示的最大搜尋查詢數。 限制此數量會提高搜尋效能，並降低顯示的清單大小。 預設值： `8` |
| 搜尋引擎 | 全域 | 識別處理目錄資料請求所需的搜尋引擎。 OpenSearch和Elasticsearch的搜尋引擎設定選項相同。 選項： `OpenSearch`或`Elasticsearch` |
| [!UICONTROL OpenSearch Server Hostname] | 全域 | 指定OpenSearch或Elasticsearch主機伺服器的名稱。 |
| [!UICONTROL OpenSearch Server Port] | 全域 | 指定OpenSearch或Elasticsearch使用的伺服器連線埠數目。 預設值： `9200` |
| [!UICONTROL OpenSearch Index Prefix] | 全域 | 指派前置詞以識別OpenSearch或Elasticsearch索引。 預設值： `magento2` |
| [!UICONTROL Enable OpenSearch HTTP Auth] | 全域 | 如果啟用，在存取OpenSearch或Elasticsearch伺服器之前，會使用HTTP驗證來提示使用者名稱和密碼。 選項： `Yes` / `No` |
| [!UICONTROL OpenSearch HTTP Username] | 全域 | 當&#x200B;_啟用Elasticsearch HTTP驗證_&#x200B;設為`Yes`時，指定OpenSearch或Elasticsearch HTTP驗證的使用者名稱。 |
| [!UICONTROL OpenSearch HTTP Password] | 全域 | 當&#x200B;_啟用Elasticsearch HTTP驗證_&#x200B;設定為`Yes`時，指定OpenSearch或Elasticsearch HTTP驗證的密碼。 |
| [!UICONTROL OpenSearch Server Timeout] | 全域 | 決定OpenSearch或Elasticsearch伺服器要求逾時前的秒數。 預設值： `15` |
| [!UICONTROL Test Connection] |  | 驗證OpenSearch或Elasticsearch連線。 |
| [!UICONTROL Enable Search Recommendations] | 存放區檢視 | 決定搜尋未傳回任何結果且出現在搜尋結果頁面的`Related search terms`區段下時，是否提供搜尋建議。 選項： `Yes` / `No` <br/>設定為[是]時，會顯示&#x200B;_[!UICONTROL Search Recommendations Count]_與_[!UICONTROL Shows Results Count for Each Recommendation]_&#x200B;的其他選項。 |
| [!UICONTROL Search Recommendations Count] | 存放區檢視 | 指定建議所提供的搜尋字詞數目。 依預設，不會顯示超過五個。 |
| [!UICONTROL Show Results Count for Each Recommendation] | 存放區檢視 | 設定為`Yes`時，為建議的搜尋建議找到的產品數量會顯示在方括弧中。 選項： `Yes` / `No` |
| [!UICONTROL Enable Search Suggestions] | 存放區檢視 | 決定是否顯示搜尋建議是否有常見的拼字錯誤。 啟用後，系統會針對未傳回任何結果且出現在&#x200B;**搜尋結果**&#x200B;頁面的`Did you mean`區段下的任何要求提供搜尋建議。 搜尋建議可能會影響搜尋效能。 設定為`Yes`時，會針對「啟用搜尋建議」和相關欄位顯示其他選項。 選項： `Yes` / `No` |
| [!UICONTROL Search Suggestions Count] | 存放區檢視 | 決定提供的搜尋建議數目。 例如： `2` |
| [!UICONTROL Show Results Count for Each Suggestion] | 存放區檢視 | 決定是否顯示每個建議的搜尋結果數目。 根據主題，數字通常出現在建議後的方括弧中。 選項： `Yes` / `No` |
| [!UICONTROL Minimum Terms to Match] | 存放區檢視 | 指定一個值，該值對應於查詢中搜尋結果應相符才能傳回的字詞數。 這可確保為購物者帶來最佳結果相關性。 百分比值與數字相關，如有需要，會向下舍入，並做為查詢中相符字詞的最小數量。 該值可以是負整數或正整數、負或正百分比、兩者的組合或多個組合。 若要深入瞭解，請參閱OpenSearch檔案中的[minimum_should_match引數](https://opensearch.org/docs/latest/query-dsl/minimum-should-match/)。 |

## [!UICONTROL Downloadable Product Options]

![可下載的產品選項](./assets/catalog-downloadable-product-options.png)<!-- zoom -->

<!-- [Downloadable Product Options](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/products/types/product-create-downloadable#configure-the-download-options) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Order Item Status to Enable Downloads] | 網站 | 決定訂單在可供下載之前必須具備的狀態。 選項： `Pending` / `Invoiced` |
| [!UICONTROL Default Maximum Number of Downloads] | 網站 | 決定客戶可用的預設下載次數。 |
| [!UICONTROL Shareable] | 網站 | 決定客戶是否必須登入其帳戶才能存取下載連結。 選項： <br/>**是** — 允許透過電子郵件傳送連結，然後可以與其他人共用。 <br/>**否** — 要求客戶登入其帳戶才能存取下載連結。 |
| [!UICONTROL Default Sample Title] | 存放區檢視 | 所有範例檔案的預設標題。 |
| [!UICONTROL Default Link Title] | 存放區檢視 | 所有可下載標題的預設連結。 |
| [!UICONTROL Opens Links in New Window] | 網站 | 決定下載連結是否會在新的瀏覽器視窗中開啟。 選項： `Yes` / `No` |
| [!UICONTROL Use Content Disposition] | 存放區檢視 | 決定如何將可下載內容的連結傳遞為電子郵件附件或瀏覽器視窗中的內嵌連結。 選項： <br/>**`Attachment`**— 下載連結會以電子郵件附件的形式傳遞。<br/>**`Inline`** — 下載連結會在網頁上以內嵌連結的形式傳遞。 |
| [!UICONTROL Disable Guest Checkout if Cart Contains Downloadable Items] | 網站 | 決定購買可下載產品的來賓是否必須註冊帳戶並登入以完成結帳程式。 選項： <br/>**`Yes`**— 如果購物車包含可下載的產品，訪客必須註冊帳戶或登入現有帳戶才能完成購買。<br/>**`No`** — 下載連結會以電子郵件內文中的內嵌連結形式傳遞。 <br/> _**注意：**_&#x200B;只有當「可共用」設定為`Yes`時，才能針對下載產品使用訪客簽出。 |

{style="table-layout:auto"}

## [!UICONTROL Date & Time Custom Options]

![日期與時間自訂選項](./assets/catalog-date-time-custom-options.png)<!-- zoom -->

<!-- Date & Time Custom Options](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/product-attributes/attributes-input-types#date-and-time-options) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Use JavaScript Calendar] | 存放區檢視 | 決定是否要使用JavaScript行事曆作為日期欄位的輸入控制項。 選項： `Yes` / `No` <br/>若設為`No`，日期欄位的每個部分都會出現個別的下拉式清單。 |
| [!UICONTROL Date Fields Order] | 存放區檢視 | 建立三個日期欄位的順序。 選項： `Day` / `Month` / `Year` |
| [!UICONTROL Time Format] | 存放區檢視 | 將時間格式設定為12或24小時時鐘。 選項： `12h AM/PM` / `24h` |
| [!UICONTROL Year Range] | 存放區檢視 | 定義出現在&#x200B;_Year_&#x200B;欄位中的開始和結束年度範圍。 必須以YYYY格式輸入值。 |

{style="table-layout:auto"}

## [!UICONTROL Catalog Events]

{{ee-feature}}

![目錄事件](./assets/catalog-events.png)<!-- zoom -->

<!-- [Catalog Events](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/events/events-private-sales) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable Catalog Events Functionality] | 網站 | 決定是否啟用事件模組。 |
| [!UICONTROL Enable Catalog Event Widget on Frontend] | 存放區檢視 | 決定店面中是否提供事件Widget。 這是靜態區塊，包含您網站中事件的相關資訊。 |
| [!UICONTROL Number of Events to be Displayed in the Event Slider Widget] | 存放區檢視 | 決定類別頁面上事件滑桿Widget中出現的事件數。 若要覆寫，請使用`limit="x"`變數。 |
| [!UICONTROL Events to Scroll per Click in Event Slider Widget] | 存放區檢視 | 決定在CMS頁面（例如首頁）上的事件滑桿Widget中顯示的事件數。 若要覆寫，請使用`scroll="x"`變數。 |

{style="table-layout:auto"}

## [!UICONTROL Rule-Based Product Relations]

{{ee-feature}}

![規則型產品關係](./assets/catalog-rule-based-product-relations.png)<!-- zoom -->

<!-- [Rule-Based Product Relations](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Maximum Number of Products in Related Products List] | 全域 | 決定可在&#x200B;_相關產品_&#x200B;清單中出現的產品數目上限。 |
| [!UICONTROL Show Related Products] | 全域 | 決定商店中顯示的相關產品清單。 它可以是在「產品資訊」中手動選取的清單、為回應產品關係規則而產生的清單，或兩者的組合。 選項： `Both Selected and Rule-Based` / `Selected Only` / `Rule-Based Only` |
| [!UICONTROL Rotation Mode for Products in Related Products List] | 全域 | 決定&#x200B;_相關產品_&#x200B;清單中產品的顯示順序。 選項： `Do not rotate` / `Shuffle` |
| [!UICONTROL Maximum Number of Products in Cross-Sell Product List] | 全域 | 決定交叉銷售清單中可以出現的產品數量上限。 |
| [!UICONTROL Show Cross-Sell Products] | 全域 | 決定商店中顯示的交叉銷售產品清單。 它可以是在「產品資訊」中手動選取的清單、為回應產品關係規則而產生的清單，或兩者的組合。 選項： `Both Selected and Rule-Based` / `Selected Only` / `Rule-Based Only` |
| [!UICONTROL Rotation Mode for Products in Cross-Sell Products List] | 全域 | 決定交叉銷售產品清單中產品的顯示順序。 選項：不旋轉/隨機播放 |
| [!UICONTROL Maximum Number of Products in Upsell Product List] | 全域 | 決定可以在&#x200B;_向上銷售產品_&#x200B;清單中顯示的產品數目上限。 |
| [!UICONTROL Show Upsell Products] | 全域 | 決定商店中顯示的追加銷售產品清單。 它可以是在「產品資訊」中手動選取的清單、為回應產品關係規則而產生的清單，或兩者的組合。 選項： `Both Selected and Rule-Based` / `Selected Only` / `Rule-Based Only` |
| [!UICONTROL Rotation Mode for Products in Upsell Product List] | 全域 | 決定追加銷售產品清單中產品的顯示順序。 選項： `Do not rotate` / `Shuffle` |

{style="table-layout:auto"}
