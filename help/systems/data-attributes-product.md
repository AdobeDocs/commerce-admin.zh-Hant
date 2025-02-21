---
title: 產品資料屬性參考
description: 當您處理產品資料匯入和匯出時，請使用此產品資料屬性參考。
exl-id: 9ffa4d1f-cbf8-4a08-bb79-33f21e698a74
feature: Products, Attributes
source-git-commit: c1f797da417bfdf24b537f8c59f954df58dac11a
workflow-type: tm+mt
source-wordcount: '2473'
ht-degree: 0%

---

# 產品資料屬性參考

下表列出典型產品匯出的屬性，其顯示順序為預設順序。 每個屬性在CSV檔案中以欄的形式呈現，而產品記錄則以列呈現。 以底線開頭的欄包含服務資料，例如複雜資料的屬性或選項值。 您可以從您的目錄[匯出](data-export.md)產品，以檢視資料中每個屬性的呈現方式。

用於匯出此資料的安裝已安裝範例資料，並有兩個網站和多個商店檢視。 雖然此清單包含通常匯出的所有欄，但`sku`是唯一必要的值。 若要匯入資料，您只能包含含有變更的欄。 `sku`應該是第一欄，但其餘屬性的順序並不重要。

## 簡單產品CSV檔案結構

| 屬性 | 說明 |
|--- |--- |
| `sku` | （必要）「庫存單位」是用於追蹤存貨的唯一英數字元識別碼。 SKU的長度最多可為64個字元。 例如： `sku123`<br/>**_注意：_**超過64個字元的SKU會導致匯入失敗。 |
| `store_view_code` | 識別可使用產品的特定商店檢視。 如果留空，則可在預設商店檢視中取得產品。 例如： `storeview1`、`english`、`spanish` |
| `attribute_set_code` | 根據產品型別，將產品指派給特定的屬性集或產品範本。 建立產品後，就無法變更屬性集。 例如： `default` |
| `product_type` | 表示產品型別。 值： <br/>`simple` — 有形專案，通常以單一單位或固定數量銷售。<br/>`grouped` — 一組作為一組產品銷售的個別產品。<br/>`configurable` — 包含多個選項的產品，客戶在購買之前必須先選取這些選項。 您可以為每組變數管理詳細目錄，因為它們代表具有不同SKU的獨立產品。 例如，可設定產品的顏色和大小組合與目錄中的特定SKU相關聯。<br/>`virtual` — 不需要出貨且未保留在庫存中的無形產品。 範例包括服務、成員資格和訂閱。<br/>`bundle` — 可自訂的產品集，包含一起銷售的簡單產品。 |
| `categories` | 表示指派給產品的每個類別。 使用正斜線分隔類別和子類別。 若要指示多個類別路徑，請使用垂直號\|分隔每個路徑 符號。 例如： `Default Category/Gear\|Default Category/Gear/Bags` |
| `product_websites` | 每個可取得產品的網站的網站程式碼。 單一產品可指派至多個網站，或限於一個網站。 如果指定多個網站，請以逗號分隔每個網站，但不含空格。 例如： `base`或`base,website2` |
| `name` | 產品名稱會出現在所有產品清單中，而且是客戶用來識別產品的名稱。 |
| `description` | 產品說明提供產品的詳細資訊，並可能包含簡單的HTML標籤。 |
| `short_description` | 簡短產品說明的使用方式取決於主題。 它可能會出現在產品清單中，有時也會用在傳送至購物網站的RSS摘要清單中。 |
| `weight` | 個別產品的重量。 實際產品重量由承運商在出貨時決定。 |
| product_online | 判斷產品是否可在市集內銷售。 值： <br/>`1` — （是）產品已啟用，且可供銷售。<br/>`2` — （否）產品已停用，無法銷售。 |
| `tax_class_name` | 與此產品相關聯的稅捐類別名稱。 |
| `visibility` | 決定產品是否顯示在目錄中，以及是否可供搜尋。 值： <br/>`Not Visible Individually` — 產品不包含在產品清單中，雖然它可能是其他產品的變數。<br/>`Catalog` — 產品會出現在所有目錄清單中。<br/>`Search` — 產品可用於搜尋作業。<br/>`Catalog, Search` — 產品包含在目錄清單中，也可供搜尋。 |
| `price` | 產品在您的商店中出售的價格。 |
| `special_price` | 指定日期範圍內產品的折扣價格。 |
| `special_price_from_date` | 特殊價格生效之時間週期的開始日期。 |
| `special_price_to_date` | 特殊價格生效之時間期間的最後日期。 |
| `url_key` | 識別產品的URL部分。 預設值以產品名稱為基礎。 例如： `product-name` |
| save_rewrites_history | 當提供值`1`與新的`url_key`時，會產生新的301 URL重新寫入，以便將舊的URL重新導向到新的URL。 |
| `meta_title` | 中繼標題會顯示在瀏覽器和搜尋結果清單的標題列和索引標籤中。 中繼標題應為產品專屬的中繼標題、併入高值關鍵字，且長度小於70個字元。 |
| `meta_keywords` | 中繼關鍵字僅對搜尋引擎可見，並被某些搜尋引擎忽略。 選擇以逗號分隔的高值關鍵字。 例如： `keyword1`、`keyword2`、`keyword3` |
| `meta_description` | 中繼說明提供搜尋結果清單產品的簡短概觀。 在理想的情況下，中繼說明的長度應介於150到160個字元之間，不過欄位可接受最多255個字元。 |
| `base_image` | 產品頁面上主要影像的相對路徑。 Commerce以字母資料夾結構在內部儲存檔案。 您可以在匯出的資料中檢視每個影像的確切位置。 例如： `/sample_data/m/b/mb01-blue-0.jpg`<br/>若要上傳新影像或覆寫現有影像，請輸入檔案名稱，前面加上正斜線。 例如： `/image.jpg` |
| `base_image_label` | 與基本影像關聯的標籤。 |
| `small_image` | 用於目錄頁面上的小影像檔案名稱，前面有正斜線。 例如： `/image.jpg` |
| `small_image_label` | 與小影像關聯的標籤。 例如： `Small Image 1`， `Small Image 2` |
| `thumbnail_image` | 任何要在產品頁面的相簿中顯示的縮圖影像的檔案名稱，前面有正斜線。 例如： `/image.jpg` |
| `thumbnail_image_label` | 與任何縮圖影像相關聯的標籤。 例如： `Thumbnail 1`， `Thumbnail 2` |
| `created_at` | 表示產品的建立日期。 日期會在建立產品時自動產生，但可在稍後編輯。 |
| `updated_at` | 表示上次更新產品的日期。 |
| `new_from_date` | 指定新產品清單的「起始」日期，並決定該產品是否作為新產品提供。 |
| `new_to_date` | 指定新產品清單的「截止」日期，並決定該產品是否作為新產品而提供。 |
| `display_product_options_in` | 如果產品有多個選項，可決定這些選項在產品頁面上出現的位置。 值：產品資訊欄/資訊欄後的區塊 |
| `map_price` | 產品的最低廣告價格。 （僅在啟用MAP時顯示。） |
| `msrp_price` | 製造商建議的產品零售價。 （僅在啟用MAP時顯示。） |
| `map_enabled` | 決定組態中是否啟用最低廣告價格。 值： <br/>`1` — （是） MAP已啟用。<br/>`0` （或空白） — （無） MAP未啟用。 |
| `gift_message_available` | 決定產品購買中是否包含贈品訊息。 值：<br/>`1` — （是）向客戶呈現包含贈品訊息的選項。<br/>`0` （或空白） — （否）未向客戶顯示包含贈品訊息的選項。 |
| `custom_design` | 列出可套用至產品頁面的可用主題。 |
| `custom_design_from` | 指定將所選主題套用至產品頁面的開始日期。 |
| `custom_design_to` | 指定將所選主題套用至產品頁面的結束日期。 |
| `custom_layout_update` | 作為配置更新套用至產品頁面的其他XML程式碼。 |
| `page_layout` | 決定產品頁面的頁面配置。 值：<br/>`No layout updates` — 頁面配置未發生任何變更。<br/>`1 column` — 將單欄版面配置套用至產品頁面。<br/>`2 columns with left bar` — 將帶有左側邊欄的雙欄版面配置套用至產品頁面。<br/>`2 columns with right bar` — 將帶有右側欄的雙欄版面配置套用至產品頁面。<br/>`3 columns` — 將三欄版面配置套用至產品頁面。<br/>`empty` — 將空白版面配置套用至產品頁面。 |
| `product_options_container` | 如果產品有多個選項，可決定這些選項在產品頁面上出現的位置。 值：產品資訊欄/資訊欄後的區塊 |
| `msrp_display_actual_price_type` | 決定客戶看到產品實際價格的位置。 值： <br/>`In Cart` — 顯示購物車中的實際產品價格。<br/>`Before Order Confirmation` — 在訂單確認前，於結帳程式結束時顯示實際產品價格。<br/>`On Gesture` — 當客戶按一下&#x200B;_價格點按_&#x200B;或&#x200B;_這是什麼？_&#x200B;連結。 |
| `country_of_manufacture` | 識別製造產品的國家/地區。 |
| `additional_attributes` | 為產品建立的其他屬性。 例如： <br/>`has_options=0,required_options=0color=Black,has_options=0,required_options=0,size_general=XS` |
| `qty` | 目前庫存的產品數量。 |
| `out_of_stock_qty` | 決定產品無庫存的庫存水準。 |
| `use_config_min_qty` | 決定是否使用組態中的預設值，且與「使用組態設定」核取方塊相對應。 值： <br/>`1` — （是）此屬性的值使用預設組態設定。<br/>`0` （或空白） — （否）可覆寫此屬性的值的預設組態。 |
| `is_qty_decimal` | 決定數量屬性是否具有十進位值。 值：<br/>`1` — （是） qty屬性的值是十進位值。<br/>`0` （或空白） — （否） qty屬性的值是整數（整數）。 |
| `allow_backorders` | 決定您的商店是否允許延期交貨，以及如何管理延期交貨。 |
| `use_config_backorders` | 決定是否使用延期交貨的預設組態設定，且對應至「使用組態設定」核取方塊的狀態。 值：<br/>`1` — （是） qty屬性的值是十進位值。<br/>`0` （或空白） — （否） qty屬性的值是整數（整數）。 |
| `min_cart_qty` | 指定單一訂單可購買之料號的最小數量。 |
| `use_config_min_sale_qty` | 決定是否使用最小數量的預設組態設定，且與「使用組態設定」核取方塊的狀態相對應。 值：<br/>`1` — （是）<br/>`0` （或空白） — （否） |
| `max_cart_qty` | 指定單一訂單可購買之產品的最大數量。 |
| `use_config_max_sale_qty` | 決定是否要使用最大數量的預設組態設定，且與「使用組態設定」核取方塊的狀態相對應。 值：<br/>`1` — （是）<br/>`0` （或空白） — （否） |
| `is_in_stock` | 表示產品是否有庫存。 |
| `notify_on_stock_below` | 指定觸發&#x200B;_缺貨_&#x200B;通知的庫存等級。 |
| `use_config_notify_stock_qty` | 決定預設組態設定是否用於觸發庫存層級通知，且對應至「使用組態設定」核取方塊的狀態。 值：<br/>`1` — （是）<br/>`0` （或空白） — （否） |
| `manage_stock` | 決定是否使用存貨控制來管理產品。 值： <br/>`1` — （是）啟用完整存貨控制來管理產品的存貨層次。<br/>`0` （或空白） — （否）系統不會追蹤目前庫存中的專案數。 |
| `use_config_manage_stock` | 決定是否使用管理庫存的預設組態設定，且與「使用組態設定」核取方塊的狀態相對應。 值：<br/>`1` — （是）<br/>`0` （或空白） — （否） |
| `use_config_qty_increments` | 決定是否要使用數量增量的預設組態設定，並與「使用組態設定」核取方塊的狀態相對應。 值：<br/>`1` — （是）<br/>`0` （或空白） — （否） |
| `qty_increments` | 建立構成數量增量的產品數量。 |
| `use_config_enable_qty_inc` | 決定是否使用預設組態設定來啟用數量增量，且與「使用組態設定」核取方塊的狀態相對應。 值：<br/>`1` — （是）<br/>`0` （或空白） — （否） |
| `enable_qty_increments` | 決定是否啟用產品的數量增加。 |
| `is_decimal_divided` | 決定產品的零件是否可以單獨出貨。 選項： `Yes` / `No` |
| `website_id` | 若為具有多個網站的安裝，需識別可使用該產品的特定網站。 如果留空，此產品將可在所有網站取得。 |
| `related_skus` | 列出已識別為相關產品的每個產品的SKU。 例如： `24-WG080,24-UG03,24-UG01,24-UG02` |
| `related_position` | 決定在related_skus欄中列為「相關產品」之SKU的位置（排序順序）。 例如： `1,2,3,4` |
| `crosssell_skus` | 列出每項已識別為交叉銷售產品的SKU。 |
| `crosssell_position` | 決定在`crosssell_skus`欄中列為交叉銷售產品的SKU位置（排序順序）。 |
| `upsell_skus` | 列出已識別為向上銷售之每項產品的SKU。 |
| `upsell_position` | 決定在`upsell_skus`欄中列為追加銷售產品的SKU位置（排序順序）。 |
| `additional_images` | 任何要與產品相關聯之其他影像的檔案名稱，其前面會加上正斜線。 例如： `/image.jpg` |
| `additional_image_labels` | 與任何其他影像相關聯的標籤。 例如： `Label 1`， `Label 2` |
| `custom_options` | 指定指派給每個自訂選項的屬性和值。 例如： <br/>`name=Color, type=drop_down, required=1, price= price_type=fixed, sku=, option_title=Black|name=Color, type=drop_down, required=1, price=, price_type=fixed, sku=, option_title=White` |

{style="table-layout:auto"}

## 產品變數的服務資料

| 屬性 | 說明 | 套用至 |
|--- |--- | --- |
| `_super_products_sku` | 針對可設定產品變數產生的SKU。 例如：WB03-XS-Green | 可設定的產品 |
| `_super_attribute_code` | 可設定產品變數的屬性代碼。 例如：顏色 | 可設定的產品 |
| `_super_attribute_option` | 可設定產品變數的值。 例如：綠色 | 可設定的產品 |
| `_super_attribute_price_corr` | 與可設定產品變化相關聯的價格調整。 | 可設定的產品 |
| `_associated_sku` | 與分組產品相關聯之產品的SKU。 | 群組產品<br/>套件組合產品 |
| `_associated_default_qty` | 決定包含的相關產品的數量。 | 可設定的產品<br/>群組產品<br/>組合產品 |
| `_associated_position` | 與其他相關產品一起列出時，決定相關產品的位置。 | 可設定的產品<br/>群組產品<br/>組合產品 |

{style="table-layout:auto"}

## 複雜的產品資料屬性

複雜資料一詞指的是與多個產品選項相關的資料。 以下產品型別使用來自不同產品的資料來建立產品變數和多個選項。

- [可設定](../catalog/product-create-configurable.md)
- [已分組](../catalog/product-create-grouped.md)
- [組合](../catalog/product-create-bundle.md)

如果您匯出可設定的產品，您會找到組成簡單產品的標準屬性，以及管理複雜資料所需的其他屬性。

![可設定的產品 — 已匯出的資料](./assets/data-exported-configurable-product.png){width="600" zoomable="yes"}

### 可設定的產品

| 屬性 | 說明 |
|--- |--- |
| `configurable_variation_labels` | 可識別產品變異的標籤。 例如： `Choose Color:`或`Choose Size:` |
| `configurable_variations` | 說明與產品變數相關的值。 例如： `sku=sku-red xs,color=red,size=xs,price=10.99,display=1,image=/pub/media/import/image1.png|sku=sku-red-m,color=red,size=m,price=20.88,display=1,image=/pub/media/import/image2.png` |

{style="table-layout:auto"}

### 已分組的產品

| 屬性 | 說明 |
|--- |--- |
| `associated_skus` | 識別組成群組的個別產品的SKU。 |

{style="table-layout:auto"}

### 套裝產品

| 屬性 | 說明 |
|--- |--- |
| `bundle_price_type` | 決定組合專案的價格是固定或動態。 |
| `bundle_sku_type` | 決定每個專案是否被指派變數、動態SKU，或是否使用固定SKU作為搭配。 選項：固定/動態 |
| `bundle_weight_type` | 決定束專案的權重是可變的還是固定的。 |
| `bundle_values` | 說明與套件組合選項相關的教導值。 例如： `name=Bundle Option One,type=dropdown; required=1, sku=sku-option2,price=10, price_type=fixed` |

{style="table-layout:auto"}

## 進階訂價屬性

「進階價格匯入/匯出」可讓您快速更新產品群組與階層價格的定價資訊。 [匯入](data-import.md)與[匯出](data-export.md)進階價格資料的程式與任何其他實體型別相同。 範例CSV檔案包含支援進階定價之每種產品型別的層級與群組價格。 變更進階價格不會影響其餘的產品記錄。

![匯出資料範例 — 進階定價](./assets/data-advanced-pricing-export-sample.png){width="600" zoomable="yes"}

| 屬性 | 說明 |
|--- |--- |
| `sku` | （必要）「庫存單位」是用於追蹤存貨的唯一英數字元識別碼。 SKU的長度最多可為64個字元。 例如： `sku123`<br/>**_注意：_**超過64個字元的SKU會導致匯入失敗。 |
| `tier_price_website` | [網站程式碼](../stores-purchase/stores.md#add-websites)會識別每個可使用層級定價的網站。 例如： `-  website1 -  All Websites [USD]` |
| `tier_price_customer` | 識別有階層定價可用的[客戶群組](../customers/customer-groups.md)。 例如： `-  ALL GROUPS -  NOT LOGGED IN -  General -  Wholesale -  Retailer` |
| `tier_price_customer_group` | 識別可使用層級定價的客戶群組。 例如： `-  ALL GROUPS -  NOT LOGGED IN -  General -  Wholesale -  Retailer` |
| `tier_price_qty` | 必須訂購才能收到層級價格折扣的產品數量。 |
| `tier_price` | 產品的折扣層級價格。 對於[套件組合產品](../catalog/product-create-bundle.md)，層級價格是以百分比計算。 |
| `group_price_website` | 每個提供群組定價的網站的[網站代碼](../stores-purchase/stores.md#add-websites)。 如果指定多個網站，請以逗號分隔每個網站，但不含空格。 例如： `-  website1 -  All Websites [USD]` |
| `group_price_customer_group` | 識別可使用群組定價的客戶群組。 例如： `-  NOT LOGGED IN -  General -  Wholesale -  Retailer` |
| `group_price` | 產品的折扣群組價格。 針對[套件組合產品](../catalog/product-create-bundle.md)，群組價格是以百分比計算。 |

{style="table-layout:auto"}
