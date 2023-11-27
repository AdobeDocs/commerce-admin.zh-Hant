---
title: 索引管理
description: 瞭解索引管理，包括觸發重新索引和最佳實務的動作。
exl-id: cbb249a2-b957-44fe-bf81-df795a8fd5d1
feature: System, Configuration
source-git-commit: 55b0672984ce8cdb853daf024299919beaf7ce0b
workflow-type: tm+mt
source-wordcount: '1308'
ht-degree: 0%

---

# 索引管理

當一或多個專案變更時，Adobe Commerce和Magento Open Source會自動重新索引。 觸發重新索引的動作包括價格變更、建立目錄或購物車價格規則、新增類別等。 為了最佳化效能，Commerce使用索引器將資料累積到特殊表格中。 當資料變更時，必須更新索引資料表，或重新編制索引。 Commerce會重新索引作為背景程式，而您的存放區在程式期間仍可存取。

重新索引資料可加快處理速度，並減少客戶必須等候的時間。 例如，如果您將某個專案的價格從$4.99變更為$3.99，Commerce會對資料重新編制索引，以顯示商店中的價格變更。 如果沒有索引，Commerce必須即時計算每個產品的價格；處理購物車價格規則、搭售定價、折扣、層級定價等。 載入產品價格所需的時間，可能會超過客戶願意等候的時間。

索引子可以設定為在儲存時或依排程更新。 除了只支援儲存的Customer Grid外，所有索引都可以使用任一選項。 在儲存時建立索引時，Commerce會在儲存動作時開始重新索引。 「索引管理」頁面會完成更新並排清快取，而重新索引訊息會在一兩分鐘內顯示。 依排程重新索引時，重新索引會根據排程執行，作為cron作業。 系統訊息會顯示於 [cron工作](cron.md) 無法更新任何變成無效的索引子。 重新索引程式進行期間，您的存放區仍可存取。

>[!NOTE]
> 使用「即時搜尋」、「目錄服務」或「產品Recommendations」的Adobe Commerce商家可選擇使用 [SaaS價格索引器](https://experienceleague.adobe.com/docs/commerce-merchant-services/price-indexer/index.html).

當需要重新索引時，通知會顯示在頁面頂端。 索引和訊息會根據您採取的重新索引模式和潛在動作清除。 如需關於索引的詳細資訊，請參閱 [應用程式如何實作索引](https://developer.adobe.com/commerce/php/development/components/indexing/#how-the-application-implements-indexing) 在 _PHP開發人員指南_.

![索引管理 — 動作](./assets/index-management.png){width="700" zoomable="yes"}

- 對於一般產品目錄，「索引管理」的呈現方式稍有不同。
- 為避免在多位管理員使用者更新觸發自動重新索引的物件時發生問題，建議您將所有索引器設定為依排程執行 [cron工作](cron.md). 否則，每次儲存物件時，任何具有相依性的物件都可能導致死結。 死結的症狀包括高CPU使用率和MySQL錯誤。 根據最佳實務，建議您使用排程索引。
- ![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)依預設，系統會將管理員動作（例如重新索引）記錄下來，且可在以下位置檢視： [動作記錄檔報告](action-log-report.md). 動作記錄可在以下位置設定： [管理員動作記錄](action-log.md) 進階管理員設定中。

## 重新索引的最佳實務

在Commerce中，重新索引和快取具有不同的目的。 索引會追蹤資料庫資訊，以提升搜尋效能、加快儲存區域的資料擷取速度等等。 [快取](cache-management.md) 儲存已載入的資料、影像、格式等，以提高載入和存取店面的效能。

- 通常，在Commerce中更新資料時想要重新索引。
- 如果您有大型商店或多個商店，可能會因為重新索引回圈的可能性，而想要將索引器（例如類別和產品）設定為已排程的cron工作。 您可能會想要在非尖峰時段依排程設定重新索引。
- 重新索引時，您不需要同時執行排清快取。
- 對於全新的Commerce安裝，您必須清除快取並重新索引。
- 排清快取和重新索引不會排清電腦的網頁瀏覽器快取。 完成更新您的店面後，清除瀏覽器快取。

## 變更索引模式

>[!IMPORTANT]
>
>針對使用的商店 [適用於Adobe Commerce的B2B](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html) 並將Elasticsearch設為全文(`catalogsearch_fulltext`)索引器：在大量許可權變更或&#39;permissions&#39;索引器處於&#39;Scheduled&#39;模式時，必須重新執行全文檢索索引。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Index Management]**.

1. 選取您要變更之每個索引器的核取方塊。

1. 設定 **[!UICONTROL Actions]** 變更為下列其中一項：

   - `Update on Save`
   - `Update by Schedule`
   - `Invalidate index`

   >[!IMPORTANT]
   >
   >客戶格線只能使用下列專案重新索引： `Update on Save`. 此索引可以 **_非_** 支援 `Update by Schedule`.

1. 按一下 **[!UICONTROL Submit]** 將變更套用到每個選取的索引器。

   **「索引管理」資料欄**

   | 欄 | 說明 |
   | ------ | ----------- |
   | [!UICONTROL Indexer] | 索引器的名稱。 |
   | [!UICONTROL Description] | 索引器的說明。 |
   | [!UICONTROL Mode] | 表示每個索引器的目前更新模式。 選項： <br/>**[!UICONTROL Update on Save]**— 索引會設定為在儲存實體變更時更新。 這些實體包括產品、類別和客戶。 儲存動作完成後，一系列步驟會開始擷取變更並更新索引。 「索引管理」頁面會在一兩分鐘內更新並排清重新索引訊息。<br/>**[!UICONTROL Update on Schedule]**  — 索引已設定為根據 [cron工作](cron.md). cron作業包括重新索引的排程間隔，在執行時將更新寫入索引。 |
   | [!UICONTROL Schedule Status] | 顯示排程狀態更新。 |
   | [!UICONTROL Status] | 顯示下列其中一項： <br/>**[!UICONTROL Ready]**— 索引是最新的。<br/>**[!UICONTROL Scheduled]**  — 已排程進行重新索引。 <br/>**[!UICONTROL Running]**— 正在重新索引。<br/>**[!UICONTROL Reindex Required]**  — 已進行需要重新索引的變更，但索引子無法自動更新。 檢查以檢視 [cron](cron.md) 可用且已正確設定。 |
   | [!UICONTROL Updated] | 表示上次更新索引的日期和時間。 |

   {style="table-layout:auto"}

## 使用命令列重新索引

Commerce使用命令列提供其他重新索引選項。 如需完整的詳細資訊和命令選項，請參閱 [重新索引](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/manage-indexers.html#reindex){：target=&quot;blank&quot;}於 _設定指南_.

## 索引觸發事件

## 重新索引觸發程式

| 索引型別 | 重新索引事件 |
| ---------- | ---------------- |
| [!UICONTROL Product Prices] | 新增客戶群組<br/>變更組態設定 |
| [!UICONTROL Flat catalog product data] | 新增存放區<br/>新增商店群組<br/>新增、編輯或刪除屬性（用於搜尋和篩選） |
| [!UICONTROL Flat catalog category data] | 新增存放區<br/>新增商店群組<br/>新增、編輯或刪除屬性（用於搜尋和篩選） |
| [!UICONTROL Catalog category/product index] | 新增、編輯或刪除產品（單一、大量及匯入）<br/>變更產品與類別的關係<br/>新增、編輯或刪除類別<br/>新增或刪除存放區<br/>刪除商店群組<br/>刪除網站 |
| [!UICONTROL Catalog search index] | 新增、編輯或刪除產品（單一、大量及匯入）<br/>新增或刪除存放區<br/>刪除商店群組<br/>刪除網站 |
| [!UICONTROL Stock status index] | 變更詳細目錄組態設定。 |
| [!UICONTROL Category permissions index] | 新增存放區<br/>新增商店群組<br/>新增、刪除或更新屬性（用於搜尋和篩選） |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>不再建議使用平面型錄作為最佳實務。 據悉，繼續使用此功能會導致效能降低和其他索引問題。 另請參閱 [使用平面型錄產品](../catalog/catalog-flat.md) 以取得詳細資訊。

## 索引動作和控制項

| 動作 | 結果 | 控制項 |
| ------ | ------ | -------- |
| 建立商店、新客戶群組或中列出的任何動作 `Actions that Cause a Full Reindex` | 完整重新索引 | 按照您的Adobe Commerce或Magento Open Sourcecron工作決定的排程執行完整的重新索引。 |
| 大量載入專案（Commerce匯入/匯出、直接SQL查詢，以及直接新增、變更或刪除資料的任何其他方法） | 部分重新索引（只有變更的專案才會重新索引） | 頻率由您的Commerce cron工作決定。 |
| 變更範圍（例如，從全域變更為網站） | 部分重新索引（只有變更的專案才會重新索引） | 頻率由您的Commerce cron工作決定。 |

{style="table-layout:auto"}

## 觸發完整重新索引的事件

| 索引子 | Event |
| ------- | ----- |
| [!UICONTROL Catalog Category Flat Indexer] | 建立網站商店<br/>建立網站商店檢視<br/>建立或刪除屬於下列任一專案的屬性：<br/> — 可在進階搜尋中搜尋或顯示<br/> — 可篩選<br/> — 可在搜尋中篩選<br/> — 用於排序<br/>將現有屬性變更為任何先前屬性。<br/>啟用一般類別店面選項 |
| [!UICONTROL Catalog Product Flat Indexer] | 建立網站商店<br>建立網站商店檢視<br/>建立或刪除屬於下列任一專案的屬性：<br/> — 可在進階搜尋中搜尋或顯示<br> — 可篩選<br> — 可在搜尋中篩選<br/> — 用於排序 <br/>將現有屬性變更為任何先前屬性。<br/>啟用一般類別店面選項 |
| [!UICONTROL Stock status indexer] | 當發生下列情況 _目錄詳細目錄選項_ 變更系統組態：<br/>`Stock Options`  — 顯示無庫存產品<br/>`Product Stock Options`  — 管理庫存 |
| [!UICONTROL Price Indexer] | 新增客戶群組。<br/>當下列任何目錄清查選項在系統組態中變更時：<br/>`Stock Options`  — 顯示無庫存產品<br/>`Product Stock Options`  — 管理庫存<br/>`Price`  — 目錄價格範圍 |
| [!UICONTROL Category or Product Indexer] | 建立或刪除商店檢視<br/>刪除商店<br/>刪除網站 |

{style="table-layout:auto"}
