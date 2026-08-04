---
title: 在Commerce中監視資料摘要同步狀態
description: 追蹤匯出。 診斷 [!DNL Catalog Service]、 [!DNL Live Search]、 [!DNL Product Recommendations]和 [!DNL Adobe Commerce Optimizer Connector]的同步處理問題。
feature: Products, Customers, Data Import/Export
role: Admin
level: Beginner
exl-id: 4e1b9da0-450c-4488-8693-1938a948e792
TQID: https://experienceleague.adobe.com/Y8vYxKS-8iX-bCLSJpAiJOItWlJk348bSMWfk1Cgpbg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 424b379815ffbf818c2490d0195bf0bf7dd51ab7
workflow-type: tm+mt
source-wordcount: 1664
ht-degree: 0%

---


# 資料摘要同步狀態監視

[!UICONTROL Data Feed Sync Status]頁面可讓Commerce管理員在管理區域中監視產品和類別資料摘要的匯出健康情況。

## 對象與可用性 {#audience}

擁有下列其中一項服務之有效授權的Commerce商家可以免費使用「資料摘要同步狀態」頁面：

- [[!DNL Product Recommendations v6.0.0]](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/guide-overview)
- [[!DNL Live Search v4.1.0]](https://experienceleague.adobe.com/en/docs/commerce/live-search/overview)
- [[!DNL Catalog Service v1.17]](https://experienceleague.adobe.com/en/docs/commerce/catalog-service/guide-overview)
- [[!DNL Adobe Commerce Optimizer Connector]](https://experienceleague.adobe.com/en/docs/commerce/aco-optimizer-connector/overview)

受支援的Commerce服務設定會自動提供資料摘要同步狀態頁面。 在雲端基礎結構或內部部署上的Adobe Commerce上，如果在啟用合格的服務或聯結器後遺失頁面，請遵循下列手動安裝指示。 對於產品管理的SaaS體驗，請勿使用Composer安裝程式。

## 存取同步狀態頁面 {#access-data-feed-sync-status-page}

從管理區域，瀏覽至&#x200B;**[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Data Feed Sync Status]**。

![資料摘要同步狀態頁面摘要資料摘要匯出活動](assets/data-feed-sync-status.png){width="600" zoomable="yes"}

>[!NOTE]
>
> 此頁面僅報告匯出狀態。 成功狀態表示資料已成功匯出，但無法確認資料是否可用於連線的服務。 如需詳細資訊，請參閱[確認連線服務中的資料](#confirm-data-in-connected-services)。

## 可用的匯出摘要

您可以從「資料同步狀態」頁面管理的可用匯出摘要清單，視所連線的Commerce服務而定。

- **已設定Commerce服務的[!DNL Adobe Commerce on Cloud, On Premises, and Commerce as a Cloud Service]：**&#x200B;請參閱&#x200B;_SaaS資料匯出指南_&#x200B;中的[支援的摘要](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/reference/feed-table-reference#supported-feeds)。

- **對於雲端或內部部署上以[!DNL Adobe Commerce Optimizer Connector]：**&#x200B;設定的Adobe Commerce，請參閱&#x200B;_Adobe Commerce Optimizer聯結器指南_&#x200B;中的[支援的摘要](https://experienceleague.adobe.com/en/docs/commerce/aco-optimizer-connector/reference/connector-reference#supported-feeds)。


## 資料摘要同步狀態摘要 {#data-feed-sync-status-summary}

摘要方格會列出每個摘要及其匯出計數。

| 欄位 | 說明 |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **摘要名稱** | 實體或實體一部份（產品、產品價格）的摘要索引子。 |
| **Source記錄** | 需要同步的Commerce記錄數。 可能會超過管理格線計數，因為摘要專案的範圍已設定（例如商店檢視代碼）。 |
| **已成功傳送記錄** | 從Commerce成功提交至已設定服務端點的摘要專案數。 這不會確認下游擷取或目錄可用性。 如果發生同步錯誤，此數字可能小於來源記錄數。 |
| **個失敗的記錄** | 無法傳送至連線Commerce服務的記錄數。 |
| **動作** | 選取&#x200B;**[!UICONTROL Details]**&#x200B;以檢視摘要的同步活動。 |

## 資料摘要同步狀態詳細資料 {#data-feed-sync-status-details}

從摘要頁面中，選取摘要名稱或選取&#x200B;**[!UICONTROL Details]**&#x200B;以檢視每個摘要專案的匯出狀態：

![資料摘要同步狀態詳細資訊頁面，內含摘要專案狀態報告](assets/data-feed-sync-status-details.png){width="600" zoomable="yes"}

| 欄位 | 說明 |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **摘要專案識別碼** | 用於系統用途的自動產生識別碼 |
| **實體識別碼** | 來源實體的唯一識別碼（產品ID、類別ID等） |
| **摘要識別碼** | 摘要專案的唯一識別碼。 例如，產品摘要的SKU和商店檢視代碼。 值會依摘要而異。 |
| **匯出狀態** | 摘要專案的[同步處理狀態](#export-status-types)，具有以顏色編碼的指標 |
| **上次同步日期** | Commerce最近一次匯出嘗試或提交專案的日期和時間。 此時間戳記無法確認下游可用性。 |
| **實體是否已刪除？** | 指出實體是否已在Adobe Commerce中刪除。 只有在同步失敗時才會顯示刪除的專案。 |
| **要求ID** | 同步請求的唯一ID。 在疑難排解實體更新時提供支援服務。 |
| **錯誤** | 同步化失敗的詳細錯誤資訊 |

您可以使用下列控制項來管理檢視：

- [!UICONTROL Mass Action]為選取的摘要專案排程重新同步
- [!UICONTROL Filters]和[!UICONTROL Columns]
- [!UICONTROL Default View]以建立和儲存篩選的檢視，並在檢視之間切換

### 摘要健康狀態指標 {#feed-health-indicators}

| **指標** | **描述** |
| ------------- | --------------- |
| 索引器狀態 | <ul><li>**就緒**：索引子是最新的。 不需要重新索引。</li><li>**需要重新索引**： Source資料已變更。 執行重新索引以擷取最近的變更。</li><li>**正在處理**：正在編制索引。</li></ul> |
| 變更記錄檔待處理專案 | <ul><li>**所有已同步**：沒有擱置的變更要處理。</li><li>待處理專案中的&#x200B;**專案**：等待處理的擱置變更數目。 超過1,000個專案的待處理專案可能表示效能問題。</li></ul> |
| 索引器模式 | <ul><li>**排程模式** （建議）：索引器會依排程執行，以降低資料遺失的風險。</li><li>**儲存時更新** （即時）：在頁面上顯示為警告。 即時模式不是預期的模式，這增加了負載時資料遺失的風險。</li></ul> |

>[!TIP]
>
> 若要深入瞭解索引處理，請參閱[索引管理](index-management.md)主題。

### 匯出狀態型別 {#export-status-types}

| **狀態** | **描述** | **需要動作** |
| ----------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------------ |
| **已提交至服務** | 摘要專案已成功從Commerce提交以供下游處理。 | 無 |
| **失敗，將重試** | 無法傳送，但系統會嘗試重新傳送。 | 監視解析度 |
| **失敗，需要注意** | 由於應用程式或資料錯誤而失敗。 | 調查並解決[!UICONTROL Error]欄中的問題 |
| **正在等待提交** | 在變更記錄檔中偵測到變更，但尚未處理。 | 一般處理狀態 |

## 監視資料摘要狀態

當您更新Commerce資料庫中與產品和類別相關的實體時，資料會根據您的摘要設定傳輸至Commerce服務。 您可以從[!UICONTROL Data Feed Sync Status]摘要頁面監視匯出活動及其目前狀態。

>[!IMPORTANT]
>
> 完成資料同步化的時間會依目錄大小、更新資料的量以及外部服務效能而有所不同。

當成功傳送的計數符合摘要的來源計數，且沒有任何專案等待提交或失敗，則Commerce已完成該摘要的匯出。 使用適當的儀表板來[確認下游可用性](#confirm-data-in-connected-services)。

>[!NOTE]
>
> Adobe也提供開發人員和系統整合經銷商可用來管理和追蹤同步作業的命令列介面工具和系統記錄檔。 如需詳細資訊，請參閱[SaaS資料匯出指南](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/overview)。

### 管理失敗的匯出 {#manage-failed-exports}

若要檢閱失敗的匯出並排程重新同步：

1. 從摘要頁面中，尋找含有失敗記錄的摘要。
1. 選取&#x200B;**[!UICONTROL Details]**。
1. 檢閱[!UICONTROL Error]欄中的錯誤訊息。
1. 使用核取方塊選取要重新同步的記錄。
1. 從[!UICONTROL Mass Action]功能表選取&#x200B;**[!UICONTROL Schedule Resync]**，選取&#x200B;**[!UICONTROL Submit]**，然後確認作業。
1. 在詳細資訊頁面上監視狀態變更。

系統會自動重試某些故障。

#### 何時手動重新同步 {#resync-feed-items}

在以下情況下手動重新同步：

- 驗證或許可權錯誤（401或403狀態代碼）持續存在
- 您已修正導致裝載錯誤的資料格式問題
- 外部服務設定或端點已變更
- 已部署影響資料匯出的自訂

### 確認連線服務中的資料 {#confirm-data-in-connected-services}

若要在匯出完成之後驗證端對端同步化，請使用下列其中一種方法。 如需此頁面的匯出狀態限制，請參閱上面的[備註](#export-status-scope)。

- 具有Commerce服務的&#x200B;**[!DNL Adobe Commerce as a Cloud Service]：**&#x200B;請檢查適用的[資料管理儀表板](data-dashboard.md)以確認下游可用性。
- **雲端或內部部署上具有Adobe Commerce Optimizer Connector的Adobe Commerce**：請先檢查Commerce管理員匯出狀態，然後檢查[!DNL Commerce Optimizer Studio]中的[資料同步頁面](https://experienceleague.adobe.com/en/docs/commerce/optimizer/setup/data-sync)
- **[!DNL Adobe Commerce Optimizer]（獨立）：**&#x200B;資料未從Commerce後端匯出。 使用[!DNL Commerce Optimizer Studio]中的[資料同步頁面](https://experienceleague.adobe.com/en/docs/commerce/optimizer/setup/data-sync)確認資料可用性。

>[!TIP]
>
> 若要深入瞭解資料同步化程式，請參閱&#x200B;*SaaS Data Export指南*&#x200B;中的[&#x200B; Synchronize data with SaaS data export](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/data-synchronization/data-sync-manage#view-and-manage-the-synchronization-process)。

## 最佳實務 {#best-practices}

- 每日檢閱摘要頁面，瞭解高失敗率的摘要。
- 每週檢查重要摘要的詳細資訊，例如產品和價格。
- 每月追蹤匯出成功趨勢，以識別週期性問題。

## 疑難排解常見問題 {#troubleshoot-common-issues}

| 問題 | 症狀 | 該做什麼 |
| ---------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 高失敗率 | 許多記錄顯示&#x200B;*失敗，需要注意*&#x200B;狀態 | <ul><li>檢查外部服務狀態和設定</li><li>檢視[!UICONTROL Error]欄中的錯誤訊息</li><li>解決基本問題後，請參閱[管理和重新同步失敗的匯出](#manage-failed-exports)</li><li>如有需要，請聯絡外部服務支援</li></ul> |
| 匯出效能緩慢 | 變更記錄檔待處理量高或狀態更新緩慢 | <ul><li>檢查[摘要健康狀態指示器](#feed-health-indicators)的索引器和待處理狀態</li><li>如果顯示&#x200B;**需要重新索引**，請重新執行索引</li><li>監視外部服務回應時間</li><li>儘可能在非高峰時間排程匯出</li><li>檢閱系統資源與效能</li></ul> |
| 驗證失敗 | [!UICONTROL Error]欄中有401或403個狀態代碼 | <ul><li>驗證API憑證和權杖</li><li>檢查外部服務帳戶許可權</li><li>續約過期的權杖，或連絡您的服務提供者</li><li>認證還原後，[重新同步受影響的記錄](#manage-failed-exports)</li></ul> |
| 遺失資料摘要同步處理狀態頁面 | 啟用連線的服務後，**[!UICONTROL Data Feed Sync Status]**&#x200B;未列在&#x200B;**[!UICONTROL System]** > **[!UICONTROL Data Transfer]**&#x200B;下 | <ul><li>若為Commerce as a Cloud Service，請確認已啟用符合資格的服務（請參閱[對象與可用性](#audience)）</li><li>僅適用於Commerce雲端或內部部署，[手動安裝擴充功能](#install-the-extension)</li></ul> |

雲端基礎結構或內部部署上的Adobe Commerce：確認已啟用合格的服務或Adobe Commerce Optimizer聯結器；如果仍然缺少頁面，請按照手動安裝指示操作。
ACCS或Adobe Commerce Optimizer：請勿手動安裝模組；請使用產品管理的同步處理體驗，或聯絡適當的服務支援團隊。

## 安裝擴充功能 {#install-the-extension}

只有當您啟用合格服務後，管理區域中缺少[!UICONTROL Data Feed Sync Status]頁面時，雲端或內部部署的Adobe Commerce才需要手動安裝。 檢視[對象與可用性](#audience)。

### 先決條件

- Adobe Commerce 2.4.4+。 如需詳細需求，請參閱[系統需求](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/system-requirements)。
- [Adobe Commerce資料匯出擴充功能](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/reference/manage-extension)，103.4.15版或更新版本
- 具有從Adobe Commerce存放庫下載所需套件許可權的驗證金鑰。 若要建立驗證金鑰並取得必要的封裝存取權，請參閱[取得您的驗證金鑰](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys)。 如需雲端安裝，請參閱[雲端基礎結構上的Commerce指南](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/develop/authentication-keys)。
- 存取Adobe Commerce應用程式伺服器的命令列。

### 安裝步驟

使用撰寫器新增`magento/module-data-exporter-status`模組：

```shell
composer require magento/module-data-exporter-status
```

如需詳細的安裝步驟，請參閱下列指南：

- [在雲端基礎結構上安裝Adobe Commerce的擴充功能](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/configure-store/extensions)
- [在Adobe Commerce內部部署安裝擴充功能](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/tutorials/extensions)

>[!MORELIKETHIS]
>
> - [資料管理儀表板](data-dashboard.md)
> - [SaaS資料匯出指南](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/overview)
