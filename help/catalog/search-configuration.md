---
title: 設定目錄搜尋
description: 瞭解如何設定商店的目錄搜尋。
exl-id: b4f22bce-39e2-4269-99a4-eb2d647df939
feature: Catalog Management, Search
source-git-commit: 279f54d41264a081166cfda7d2216172ac22cd26
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 0%

---

# 設定目錄搜尋

目錄搜尋設定有兩種變體。 第一個方法說明安裝[即時搜尋](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html)時可用的設定。 第二個方法說明具有[OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/search-engine/overview.html){：target=&quot;_blank&quot;}的原生Adobe Commerce的組態設定。

>[!NOTE]
>
>對於雲端基礎結構專案，請參閱&#x200B;[_雲端基礎結構上的Commerce指南_](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/configure/service/opensearch)中的其他指示。

## 方法1：具有[!DNL Live Search]的Adobe Commerce

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Catalog]**&#x200B;並在下方選擇&#x200B;**[!UICONTROL Catalog]**。

1. 展開&#x200B;**[!UICONTROL Catalog Search]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   即時搜尋的![目錄搜尋](../configuration-reference/catalog/assets/catalog-search-live-search.png){width="600" zoomable="yes"}

   如需這些選項的詳細清單，請參閱&#x200B;_設定參考_&#x200B;中的[Adobe Commerce與即時搜尋](../configuration-reference/catalog/catalog.md#adobe-commerce-with-live-search)。

1. 若要限制搜尋查詢文字的長度和字數，請設定&#x200B;**[!UICONTROL Minimal Query Length]**&#x200B;和&#x200B;**[!UICONTROL Maximum Query Length]**&#x200B;的值。

1. 若要限制快取熱門搜尋結果的數量以加快回應，請設定&#x200B;**[!UICONTROL Number of top search results to cache]**&#x200B;的數量。

   預設值為`100`。 輸入值`0`會在第二次輸入時快取所有搜尋字詞和結果。

1. 若要變更[店面快顯視窗](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-storefront/quick-tour.html)中可傳回結果的行數上限，請輸入其他&#x200B;**[!UICONTROL Autocomplete Limit]**&#x200B;值。

   限制行數可以改善搜尋的效能，並減少傳回清單的大小。 預設值為`8`行。

## 方法2：使用OpenSearch的Commerce

>[!IMPORTANT]
>
>- 由於2023年8月有[!DNL Elasticsearch 7]個支援終止公告，建議所有Adobe Commerce客戶移轉至OpenSearch 2.x搜尋引擎。 如需在產品升級期間移轉搜尋引擎的相關資訊，請參閱&#x200B;_升級指南_&#x200B;中的[移轉至OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html)。
>- 在2.4.4和2.4.3-p2版中，所有標示為Elasticsearch的欄位也適用於OpenSearch。 2.4.6版開始支援Elasticsearch8.x時，建立了新標籤以區分Elasticsearch和OpenSearch設定。 不過，兩者的設定選項是相同的。

### 步驟1：設定一般搜尋選項

>[!NOTE]
>
>使用OpenSearch和Elasticsearch時，不提供依尾碼搜尋的立即可用支援。 例如，如果關鍵字只包含SKU的結尾部分，依SKU搜尋可能不會傳回預期結果。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Catalog]**&#x200B;並在下方選擇&#x200B;**[!UICONTROL Catalog]**。

1. 展開&#x200B;**[!UICONTROL Catalog Search]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![搜尋引擎設定](../configuration-reference/catalog/assets/catalog-search-opensearch.png){zoomable="yes"}

   如需這些選項的詳細資訊，請參閱&#x200B;_設定參考_&#x200B;中的[具有原生搜尋的Adobe Commerce](../configuration-reference/catalog/catalog.md#adobe-commerce-with-native-search)。

1. 若要限制搜尋查詢文字的長度和字數，請設定&#x200B;**[!UICONTROL Minimal Query Length]**&#x200B;和&#x200B;**[!UICONTROL Maximum Query Length]**&#x200B;的值。

   >[!IMPORTANT]
   >
   >為此最小和最大範圍設定的值必須與搜尋引擎設定中設定的對應範圍相容。 例如，如果您在Commerce中將這些值設為`2`和`300`，請更新搜尋引擎中對應的值。

1. 若要限制快取熱門搜尋結果的數量以加快回應，請設定&#x200B;**[!UICONTROL Number of top search results to cache]**&#x200B;的數量。

   預設值為`100`。 輸入值`0`會在第二次輸入時快取所有搜尋字詞和結果。

1. 若要啟用或停用Product EAV索引子，請設定&#x200B;**[!UICONTROL Enable EAV Indexer]**。

   此功能可提升索引速度，並限制第三方擴充功能不得使用索引器。

1. 若要限制搜尋自動完成所顯示的搜尋結果數目上限，請設定&#x200B;**[!UICONTROL Autocomplete Limit]**&#x200B;的金額。

   限制此數量會提高搜尋效能，並降低顯示的清單大小。 預設值為`8`。

### 步驟2：設定OpenSearch連線

>[!IMPORTANT]
>
>在安裝或升級Commerce時，已設定&#x200B;**[!UICONTROL Search Engine]**、**[!UICONTROL OpenSearch Server Hostname]**、**[!UICONTROL OpenSearch Server Port]**、**[!UICONTROL OpenSearch Index Prefix]**、**[!UICONTROL Enable OpenSearch HTTP Auth]**&#x200B;和&#x200B;**[!UICONTROL OpenSearch Server Timeout]**&#x200B;欄位。 只有在升級或修改OpenSearch時，才應該變更這些值。

1. 針對&#x200B;**[!UICONTROL Search Engine]**，選取`OpenSearch`。

1. 對於&#x200B;**[!UICONTROL OpenSearch Server Hostname]**，請接受安裝Commerce時設定的預設值。

1. 對於&#x200B;**[!UICONTROL OpenSearch Server Port]**，請接受安裝Commerce時設定的預設值。

   在此範例中，預設值為`9200`。

1. 針對&#x200B;**[!UICONTROL OpenSearch Index Prefix]**，輸入前置詞以識別Elasticsearch索引。

   預設值為`magento2`。

1. 若要使用HTTP驗證來提示使用者名稱和密碼以存取OpenSearch伺服器，請將&#x200B;**[!UICONTROL Enable OpenSearch HTTP Auth]**&#x200B;設為`Yes`。

1. 針對&#x200B;**[!UICONTROL OpenSearch Server Timeout]**，輸入系統逾時前的秒數。

   預設值為`15`。

1. 若要驗證設定，請按一下&#x200B;**[!UICONTROL Test Connection]**。

### 步驟3：設定建議與建議

>[!NOTE]
>
>搜尋建議和建議可能會影響伺服器效能。

1. 若要提供建議，請將&#x200B;**[!UICONTROL Enable Search Recommendations]**&#x200B;設為`Yes`並執行下列動作：

   - 針對&#x200B;**[!UICONTROL Search Recommendation Count]**，輸入要提供的建議數目。

   - 若要顯示每個建議的發現結果數目，請將&#x200B;**[!UICONTROL Show Results Count for Each Recommendation]**&#x200B;設為`Yes`。

1. 將&#x200B;**[!UICONTROL Enable Search Suggestions]**&#x200B;設為`Yes`並執行下列動作：

   - 針對&#x200B;**[!UICONTROL Search Suggestions Count]**，輸入要提供的搜尋建議數目。

   - 若要顯示每個建議的結果數目，請將&#x200B;**[!UICONTROL Show Results for Each Suggestion]**&#x200B;設為`Yes`。

### 步驟4：設定相符的最少條款

若要控制查詢中搜尋結果應符合的傳回字詞數目下限，請指定&#x200B;**[!UICONTROL Minimum Terms to Match]**&#x200B;的值。 指定此值可確保購物者的最佳結果相關性。 如需接受的值清單，請參閱OpenSearch檔案中的[minimum_should_match引數](https://opensearch.org/docs/latest/query-dsl/minimum-should-match/)。

完成時，按一下&#x200B;**[!UICONTROL Save Config]**。
