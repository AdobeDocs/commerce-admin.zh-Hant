---
title: 目錄和產品URL
description: 瞭解目錄產品的URL格式型別，以及如何進行設定。
exl-id: 47405dc6-9b5e-4ca8-87eb-5a222de40793
feature: Catalog Management, Products, Search, Categories
source-git-commit: 11d78b7d7b548c373cfe0ec398814994c3e99e7a
workflow-type: tm+mt
source-wordcount: '882'
ht-degree: 0%

---

# 目錄和產品URL

您指派給產品和類別的URL在決定搜尋引擎為您的網站編制索引的效果方面扮演了主要角色。 開始建立目錄之前，請先考慮可用的選項。 若要檢視目前的URL格式，請前往店面並導覽至目錄中的任何產品。 URL的格式取決於您用來尋找頁面的目前組態設定和方法。

## URL格式

### 動態URL

動態URL是&#x200B;_即時建立_，可能包含查詢字串，內含產品ID、排序順序及提出要求的頁面的變數。 當客戶在您的商店中搜尋產品時，產生的URL看起來可能會像這樣：

- `http://mystore.com/catalogsearch/result/?q=racer+back`
- `http://mystore.com/women/tops-women.html?style_general=135`

### 靜態URL

靜態URL是特定頁面的固定位址。 靜態URL可以適用於搜尋引擎的格式顯示，或是依ID參照產品和類別。 這些URL包含人們可能用來尋找產品的字詞，並需要啟用網頁伺服器重寫。 具有靜態URL的檔案通常用於產品和類別頁面、內容頁面，以及[主題資產](../content-design/theme-assets.md)。

- `http://mystore.com/antonia-racer-tank.html`

## URL元件

### URL索引鍵

URL索引鍵是說明產品或類別的靜態URL的一部分。 當您建立產品或類別時，系統會根據名稱自動產生初始URL金鑰。 若要變更URL索引鍵，請參閱產品資訊的[搜尋引擎最佳化](product-search-engine-optimization.md)區段。

>[!NOTE]
>
>根據預設，帶重音的特殊字元會在URL鍵中自動取代為其一般不帶重音的版本。 例如，`ñ`會自動取代為`n`。 可透過將&#x200B;_[!UICONTROL Search Engine Optimization: Apply transliteration for product URL]_組態選項設定為`No`來停用此行為。 請參閱[設定目錄URL](#configure-catalog-urls)。

URL索引鍵應由小寫字元組成，並在這些字元之間加上非尾隨連字型大小以分隔字詞。 URL索引鍵的開頭或結尾不允許使用連字型大小。 設計良好的「方便搜尋引擎」URL索引鍵可能包含產品名稱和關鍵字，以改進搜尋引擎編制索引的方式。 URL金鑰可設定為在URL金鑰變更時建立自動重新導向。

>[!NOTE]
>
>若要延伸URL自訂，例如當地語系化的URL，請參閱[URL重寫](../merchandising-promotions/url-rewrite.md)以取得詳細資訊。

### HTML尾碼

您的目錄可設定為將尾碼納入或排除為類別和產品URL的一部分。 人們可能選擇使用或忽略尾碼的原因有很多。 一些人認為尾碼不再有任何效用，而且搜尋引擎會更有效率地索引沒有尾碼的頁面。 不過，貴公司可能會針對需要尾碼的URL採用標準化格式。

由於尾碼是由系統設定所控制，因此您絕對不應該在類別或產品的URL索引鍵中直接輸入尾碼。 （這麼做會導致URL結尾出現雙尾碼。） 無論您是否決定使用尾碼，請保持一致，並對所有產品和類別頁面使用相同的設定。 以下是尾碼有或無尾碼的URL範例。

#### 具有HTML尾碼的URL

- `http://mystore.com/helena-hooded-fleece.html`
- `http://mystore.com/helena-hooded-fleece.htm`

#### 不含HTML尾碼的URL

- `http://mystore.com/helena-hooded-fleece`

### 類別路徑

您可以將URL設定為包含或排除類別路徑。 依預設，類別路徑會包含在所有類別和產品頁面中。 以下範例顯示有和不有類別路徑的相同產品URL。

#### 具有類別路徑的URL

- `http://mystore.com/women/tops-women/hoodies-and-sweatshirts-women/helena-hooded-fleece.html`

#### 沒有類別路徑的URL

- `http://mystore.com/helena-hooded-fleece.html`

為避免搜尋引擎索引指向相同內容的多個URL，您可以從URL中排除類別路徑。 另一種方法是使用標準中繼標籤，讓搜尋引擎知道要索引的URL以及要忽略的URL。 依預設，Commerce不會在產品URL中加入類別路徑。

## 設定目錄URL

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Catalog]**&#x200B;並在下方選擇&#x200B;**[!UICONTROL Catalog]**。

1. 展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Search Engine Optimizations]**&#x200B;區段並設定選項：

   - 將&#x200B;**[!UICONTROL Product URL Suffix]**&#x200B;設為`html`或`htm`。 輸入不含句號的尾碼，因為會自動套用。

   - 將&#x200B;**[!UICONTROL Category URL Suffix]**&#x200B;設為`html`或`htm`。 輸入不含句號的尾碼，因為會自動套用。

   - 將&#x200B;**[!UICONTROL Use Categories Path for Product URLs]**&#x200B;設定為您的偏好設定。

   ![搜尋引擎最佳化](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

   如需這些選項的詳細清單，請參閱&#x200B;_組態參考_&#x200B;中的[搜尋引擎最佳化](../configuration-reference/catalog/catalog.md#search-engine-optimization)。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

1. 出現提示時，請按一下系統訊息中的&#x200B;**[!UICONTROL Cache Management]**&#x200B;連結，然後重新整理無效的快取。

   ![重新整理快取](./assets/msg-cache-management.png){width="450" zoomable="yes"}

   如需這些選項的詳細資訊，請參閱[重新整理快取](../systems/cache-management.md#refresh-specific-caches)。

## 設定目錄媒體URL格式

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL General]**&#x200B;並選擇&#x200B;**[!UICONTROL Web]**。

1. 展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Url Options]**&#x200B;區段並設定選項：

![網頁>一般選項](../configuration-reference/general/assets/web-url-options.png){width="600" zoomable="yes"}

| 欄位 | [領域](../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Add Store Code to URLs] | 全域 | 如果啟用了網頁伺服器重寫，則啟用此設定會在URL中插入目前檢視的存放區代碼。 選項： `Yes` / `No` |
| [!UICONTROL Auto-redirect to Base URL] | 全域 | （針對單一商店設定）如果您的網站上有中斷的連結，這會將流量重新導向至基本URL，而非具有「404找不到頁面」訊息的頁面。 選項： `No` / `Yes (302 Found)` / `Yes (301 Moved Permanently)` <br /><br />**_重要！_**請勿針對多存放區設定使用自動重新導向至基底URL。 |
| [!UICONTROL Catalog media URL format] | 全域 | 定義指派給產品和類別的URL格式。 選項： <br />**[!UICONTROL Unique hash per image variant (Legacy mode)]**— 將轉換的檔案名稱定義為唯一的雜湊值。<br />**[!UICONTROL Image optimization based on query parameters]** — 根據查詢引數定義[影像最佳化](../content-design/media-gallery-image-optimization.md)程式。 |

{style="table-layout:auto"}
