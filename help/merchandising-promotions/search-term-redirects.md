---
title: 搜尋字詞重新導向和店面路由
description: 瞭解如何透過部署為Adobe Commerce和Edge Delivery Services選擇搜尋字詞重新導向、URL重新寫入、即時搜尋規則或店面路由。
feature: Merchandising, Search
role: Admin, User
level: Intermediate
topic: Commerce, Administration
autotag-review: '2026-09-10T17:42:01.349Z'
TQID: 'https://experienceleague.adobe.com/Vxw3B0zOzLZfAm3qn8gJKHGSNtVhkN2Bfmcauhj0sdM'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 67a00b294f1946da5795cd8fb7ea9fac1c80edcd
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 0%
---
# 搜尋字詞重新導向和店面路由

搜尋字詞重新導向、URL重新導向和搜尋銷售可以解決不同的問題。 使用本指南來選擇由[!DNL Edge Delivery Services]支援的標準[!DNL Adobe Commerce]搜尋、[!DNL Live Search]和[!DNL Commerce Storefront]的正確功能。

## 瞭解重新導向型別

這些功能的不同之處在於觸發行為的方式以及購物者看到的內容：

* **搜尋字詞重新導向**&#x200B;會將進入特定搜尋字詞的購物者傳送至指定頁面。

* **URL重新導向**&#x200B;會傳送對舊URL的要求到新URL，通常有HTTP 301或302回應。 瀏覽器位址列會變更為新URL。

* **搜尋銷售**&#x200B;會變更搜尋結果中出現的產品或其順序，而不會變更要求的URL。

* **URL重寫**&#x200B;會將一個URL對應到伺服器上的另一個URL。 [!DNL Adobe Commerce] URL重寫工具會為舊的URL建立永久重新導向(301)。 如需詳細資訊，請參閱[URL重寫](url-rewrite.md)。

## 選擇路由功能

請依照下列指引，識別符合您需求的功能：

| 需求 | 建議的功能 |
| --- | --- |
| 從標準[!DNL Adobe Commerce]搜尋傳送特定查詢至頁面 | 在[管理搜尋字詞](../catalog/search-terms.md)中設定搜尋字詞（如果支援）。 |
| 變更搜尋結果中的產品排名或可見度 | 使用[!DNL Live Search] [同義字](https://experienceleague.adobe.com/zh-hant/docs/commerce/live-search/live-search-admin/synonyms/synonyms)或[銷售規則](https://experienceleague.adobe.com/zh-hant/docs/commerce/live-search/live-search-admin/rules/rules-add)。 |
| 重新導向舊產品、類別或CMS URL | 使用Commerce [URL Rewrite](url-rewrite.md)工具套用至您的部署。 |
| 重新導向[!DNL Edge Delivery Services]路徑 | 使用店面或CDN路由。 |
| 店面移轉後保留舊版URL | 建立並測試舊版到新的URL重新導向對應。 |

## 標準Commerce搜尋

透過標準目錄搜尋，您可以設定搜尋字詞，以開啟部署支援此功能的內容頁面、類別頁面、產品頁面或外部頁面。 當購物者輸入的查詢（例如`gift cards`或`returns`）必須開啟行銷活動或資訊頁面時，請使用此選項。

若要建立或更新此型別的重新導向，請參閱[管理搜尋詞](../catalog/search-terms.md)。 搜尋字詞設定與URL重寫工具不同，因為觸發因素是購物者的查詢，而不是現有的URL。

>[!NOTE]
>
>確認店面使用標準目錄搜尋並支援原生搜尋字詞重新導向。 [!DNL Live Search]、[!DNL Adobe Commerce as a Cloud Service]或Headless店面的行為與可用設定可能不同。

## URL重新導向和重新寫入

當來源是現有URL而不是購物者輸入的搜尋字詞時，請使用URL重寫。 常見的範例包括重新導向：

* 新產品URL的舊產品URL。

* 取代類別URL的已淘汰類別URL。

* 過時的CMS頁面URL與新內容頁面URL。

對於支援URL重寫工具的部署，請前往「**[!UICONTROL Marketing]** > **[!UICONTROL SEO & Search]** > **[!UICONTROL URL Rewrites]**」以建立重新導向。 如需逐步指引，請參閱[URL重寫](url-rewrite.md)。

>[!NOTE]
>
>[URL重寫](url-rewrite.md)主題僅適用於PaaS。 對於[!DNL Adobe Commerce as a Cloud Service]或[!DNL Edge Delivery Services]店面，請改用該店面的路由指南。

## 即時搜尋

[!DNL Live Search]會取代預設的店面搜尋體驗，並提供同義字、多面向和銷售規則等功能。

當您需要變更搜尋關聯性、產品排名或產品可見性時，請使用[!DNL Live Search]。 當不同的字詞應該傳回類似的產品時，請使用同義詞。 當產品必須以不同方式提升、掩埋或排名時，請使用銷售規則。

不應將[!DNL Live Search]搜尋行為視為每個原生Commerce搜尋字詞設定的卸除式取代。 當查詢必須導覽到內容或行銷活動頁面時，在接收請求的店面或邊緣路由層中實作重新導向。 如需詳細資訊，請參閱[[!DNL Live Search] 檔案](https://experienceleague.adobe.com/zh-hant/docs/commerce/live-search/overview)。

## Edge Delivery Services

對於由[!DNL Edge Delivery Services]提供支援的店面，請在店面或邊緣路由層管理重新導向。 請勿假設[!DNL Adobe Commerce]管理員URL重寫控制每個要求。

當您使用檔案編寫時，請在網站的重新導向組態中維護重新導向對應。 對於在請求到達來源之前必須執行的重新導向，請使用適當的CDN或邊緣設定。 如需相關的SEO指引，請參閱[Commerce店面的SEO指引](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/indexing/?lang=zh-Hant)。

## 從Luma移轉

將重新導向移轉視為店面移轉的一部分。 保留客戶歷程和SEO意圖，然後重新實作目標店面的路由。

將流量切換至新店面之前：

1. 匯出並清查現有的Luma URL和搜尋詞登陸頁面。

1. 將每個專案分類為搜尋字詞重新導向、URL重新導向或銷售規則。

1. 將每個舊版URL對應至其新店面路徑。

1. 在接收請求的圖層實作每個重新導向。

1. 測試狀態代碼、查詢引數、規範URL、地區設定路徑和重新導向回圈。

1. 在啟動後監視記錄檔和分析未解決的舊版URL。

## 疑難排解重新導向

當重新導向在[!DNL Adobe Commerce]搜尋、店面路由和存放區檢視中的行為與預期不符時，請使用下列檢查。

| 問題 | 檢查內容 |
| --- | --- |
| 搜尋字詞不會重新導向 | 確認店面使用標準目錄搜尋、搜尋查詢符合設定的字詞，且搜尋字詞已指派給正確的店面檢視。 如果[!DNL Live Search]已啟用，請確認已在店面或邊緣圖層實作重新導向。 |
| 重新導向可在Luma上使用，但無法在Edge Delivery Services上使用 | 確認已在[!DNL Edge Delivery Services]店面或CDN路由層中設定重新導向。[!DNL Adobe Commerce] 管理員URL重寫可能不會收到要求。 |
| 即時搜尋會傳回結果，而非重新導向 | 使用[!DNL Live Search]規則進行產品排名和可見度。 若要導覽至內容或行銷活動頁面，請在店面或邊緣圖層設定重新導向。 |
| 重新導向適用於一個商店檢視，但不適用於另一個商店檢視 | 檢查指派給搜尋字詞或URL規則的存放區檢視。 在每個受影響的存放區檢視中測試完整的地區設定路徑和查詢。 |

## 有關此主題的更多說明

* [SEO概述和最佳作法](seo-overview.md)

* [什麼是店面？](../getting-started/storefront.md)

* [管理搜尋詞](../catalog/search-terms.md)

* [URL重新寫入](url-rewrite.md)
