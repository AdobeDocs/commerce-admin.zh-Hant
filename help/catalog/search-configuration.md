---
title: 設定目錄搜尋
description: 瞭解如何設定商店的目錄搜尋。
exl-id: b4f22bce-39e2-4269-99a4-eb2d647df939
feature: Catalog Management, Search
source-git-commit: 1f84bf9ab20aeccacf56eab396b2778140964d17
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 0%

---

# 設定目錄搜尋

目錄搜尋設定有兩種變體。 第一種方法說明在下列情況下可用的設定： [即時搜尋](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html) 已安裝。 第二種方法說明的原生Adobe Commerce組態設定，其中 [Elasticsearch][1]{：target=&quot;_blank&quot;}。

## 方法1：Adobe Commerce與 [!DNL Live Search]

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Catalog]** 並選擇 **[!UICONTROL Catalog]** 底下。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Catalog Search]** 區段。

   ![即時搜尋的目錄搜尋](../configuration-reference/catalog/assets/catalog-search-live-search.png){width="600" zoomable="yes"}

   如需這些選項的詳細清單，請參閱 [Adobe Commerce搭配Live Search](../configuration-reference/catalog/catalog.md#adobe-commerce-with-live-search) 在 _設定參考_.

1. 若要限制搜尋查詢文字的長度和字數，請設定 **[!UICONTROL Minimal Query Length]** 和 **[!UICONTROL Maximum Query Length]**.

1. 若要限制快取較快回應的熱門搜尋結果數量，請設定 **[!UICONTROL Number of top search results to cache]**.

   預設值為 `100`. 輸入值 `0` 第二次輸入時會快取所有搜尋字詞和結果。

1. 若要變更傳回結果的最大可用行數，請 [店面蹦蹦跳跳](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-storefront/quick-tour.html)，輸入其他值 **[!UICONTROL Autocomplete Limit]** 值。

   限制行數可以改善搜尋的效能，並減少傳回清單的大小。 預設值為 `8` 行。

## 方法2：含Elasticsearch的商務

>[!IMPORTANT]
>
>由於 [!DNL Elasticsearch 7] 2023年8月支援終止公告，建議所有Adobe Commerce客戶移轉至OpenSearch 2.x搜尋引擎。 如需在產品升級期間移轉搜尋引擎的相關資訊，請參閱 [移轉至OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html) 在 _升級指南_.

{{beta2-updates}}

### 步驟1：設定一般搜尋選項

>[!NOTE]
>
>使用Elasticsearch時，不提供依尾碼搜尋的立即可用支援。 例如，如果關鍵字只包含SKU的結尾部分，依SKU搜尋可能不會傳回預期結果。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Catalog]** 並選擇 **[!UICONTROL Catalog]** 底下。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Catalog Search]** 區段。

   ![Elasticsearch設定](../configuration-reference/catalog/assets/catalog-search-elasticsearch.png){width="600" zoomable="yes"}

   如需這些選項的詳細資訊，請參閱 [Adobe Commerce與Elasticsearch](../configuration-reference/catalog/catalog.md#adobe-commerce-with-elasticsearch) 在 _設定參考_.

1. 若要限制搜尋查詢文字的長度和字數，請設定 **[!UICONTROL Minimal Query Length]** 和 **[!UICONTROL Maximum Query Length]**.

   >[!IMPORTANT]
   >
   >為此最小和最大範圍設定的值必須與Elasticsearch搜尋引擎設定中設定的對應範圍相容。 例如，如果您將這些值設為 `2` 和 `300` 在Commerce中，更新搜尋引擎中對應的值。

1. 若要限制快取較快回應的熱門搜尋結果數量，請設定 **[!UICONTROL Number of top search results to cache]**.

   預設值為 `100`. 輸入值 `0` 第二次輸入時會快取所有搜尋字詞和結果。

1. 如果要啟用或停用「產品EAV索引器」，請設定 **[!UICONTROL Enable EAV Indexer]**.

   此功能可提升索引速度，並限制第三方擴充功能不得使用索引器。

1. 若要限制搜尋自動完成所顯示的搜尋結果數目上限，請設定 **[!UICONTROL Autocomplete Limit]**.

   限制此數量會提高搜尋效能，並降低顯示的清單大小。 預設值為 `8`.

### 步驟2：設定Elasticsearch連線

>[!IMPORTANT]
>
>此 **[!UICONTROL Search Engine]**， **[!UICONTROL Elasticsearch Server Hostname]**， **[!UICONTROL Elasticsearch Server Port]**， **[!UICONTROL Elasticsearch Index Prefix]**， **[!UICONTROL Enable Elasticsearch HTTP Auth]**、和 **[!UICONTROL Elasticsearch Server Timeout]** 欄位是在安裝或升級Commerce時設定的。 只有在升級或修改Elasticsearch時，才應變更這些值。

1. 的 **[!UICONTROL Search Engine]**，接受預設值 `Elasticsearch 7`.

   所有Commerce安裝均需要Elasticsearch7.6.x。

1. 的 **[!UICONTROL Elasticsearch Server Hostname]**，接受安裝Commerce時設定的預設值。

   在此範例中，預設值為 `elasticsearch.internal`.

1. 的 **[!UICONTROL Elasticsearch Server Port]**，接受安裝Commerce時設定的預設值。

   在此範例中，預設值為 `9200`.

1. 的 **[!UICONTROL Elasticsearch Index Prefix]**，輸入前置詞以識別Elasticsearch索引。

   預設值為 `magento2`.

1. 若要使用HTTP驗證來提示使用者名稱和密碼以存取Elasticsearch伺服器，請設定 **[!UICONTROL Enable Elasticsearch HTTP Auth]** 至 `Yes`.

1. 的 **[!UICONTROL Elasticsearch Server Timeout]**，輸入系統逾時前的秒數。

   預設值為 `15`.

1. 若要驗證設定，請按一下 **[!UICONTROL Test Connection]**.

### 步驟3：設定建議與建議

>[!NOTE]
>
>搜尋建議和建議可能會影響伺服器效能。

1. 若要提供建議，請設定 **[!UICONTROL Enable Search Recommendations]** 至 `Yes` 並執行下列動作：

   - 的 **[!UICONTROL Search Recommendation Count]**，輸入要提供的建議數量。

   - 若要顯示每個建議的發現結果數，請設定 **[!UICONTROL Show Results Count for Each Recommendation]** 至 `Yes`.

1. 設定 **[!UICONTROL Enable Search Suggestions]** 至 `Yes` 並執行下列動作：

   - 的 **[!UICONTROL Search Suggestions Count]**，輸入要提供的搜尋建議數量。

   - 若要顯示每個建議的結果數目，請設定 **[!UICONTROL Show Results for Each Suggestion]** 至 `Yes`.

### 步驟4：設定相符的最少條款

若要控制查詢中搜尋結果應比對以傳回的最小字詞數，請為 **[!UICONTROL Minimum Terms to Match]**. 指定此值可確保購物者的最佳結果相關性。 如需接受的值清單，請參閱 [minimum_should_match引數](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-minimum-should-match.html) 在Elasticsearch檔案中。

完成後，按一下 **[!UICONTROL Save Config]**.

[1]: https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/search-engine/overview.html
[2]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/search/overview-search.html
