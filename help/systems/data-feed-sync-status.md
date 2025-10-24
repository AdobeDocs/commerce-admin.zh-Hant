---
title: 資料摘要狀態監視
description: 監視資料匯出同步處理，並識別 [!DNL Catalog Service]、 [!DNL Live Search]和 [!DNL Product Recommendations]摘要處理的任何問題或延遲。
feature: Products, Customers, Data Import/Export
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hant/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"
source-git-commit: 433d3fd4dc10a81b685262c1e3c06a0da5778841
workflow-type: tm+mt
source-wordcount: '1455'
ht-degree: 0%

---


# 資料摘要狀態監視

Adobe Commerce管理員可以使用Commerce管理員中的資料摘要同步狀態頁面，監控從Adobe Commerce匯出至連線Commerce服務的資料同步狀態。

![資料摘要同步狀態詳細資訊頁面，內含摘要專案狀態報告](assets/data-feed-sync-status.png)

此頁面提供資料匯出摘要的健全狀況與效能的即時深入分析，這些摘要會將產品與類別資料從Commerce傳輸至外部服務，例如[!DNL Product Recommendations]、[!DNL Live Search]與[!DNL Catalog Service]。

同步狀態頁面僅顯示匯出狀態。 成功狀態表示資料已成功匯出至SaaS資料庫以供發佈。 使用[資料管理儀表板](data-dashboard.md)追蹤從Commerce資料庫傳輸到連線服務的資料。

監控摘要狀態有助於確保資料一致性，並可迅速解決匯出程式中發生的任何問題。 管理員可以：

* **檢視所有資料摘要的同步處理狀態**
* **識別並疑難排解摘要處理中的錯誤**
* **存取個別摘要專案的詳細狀態資訊**

系統會追蹤下列摘要的狀態：

* 產品資訊源
* 產品屬性摘要
* 類別摘要
* 產品覆寫摘要
* 產品價格摘要
* 產品系列資訊源

>[!TIP]
>
>若要深入瞭解資料同步化程式，請參閱[SaaS Data Export指南](https://experienceleague.adobe.com/zh-hant/docs/commerce/saas-data-export/data-synchronization)*中的&#x200B;*Synchronize data with SaaS data export*。

## 安裝擴充功能

擁有下列Commerce服務有效授權的所有Commerce商戶都可使用「資料摘要狀態」頁面：

* [[!DNL Product Recommendations v6.0.0+]](https://experienceleague.adobe.com/zh-hant/docs/commerce/product-recommendations/guide-overview)
* [[!DNL Live Search v4.1.0+]](https://experienceleague.adobe.com/zh-hant/docs/commerce/live-search/guide-overview)
* [[!DNL Catalog Service v1.17+]](https://experienceleague.adobe.com/zh-hant/docs/commerce/catalog-service/guide-overview)具有使用中的授權。

**需求**

* PHP 8.1、8.2、8.3或8.4
* Adobe Commerce 2.4.4+
* [Adobe Commerce資料匯出擴充功能](https://experienceleague.adobe.com/zh-hant/docs/commerce/saas-data-export/manage-extension)，103.4.15版或更新版本
* 存取[repo.magento.com](https://repo.magento.com)

  若要產生金鑰並取得必要的許可權，請參閱[取得您的驗證金鑰](https://experienceleague.adobe.com/zh-hant/docs/commerce-operations/installation-guide/prerequisites/authentication-keys)。 如需雲端安裝，請參閱[雲端基礎結構上的Commerce指南](https://experienceleague.adobe.com/zh-hant/docs/commerce-on-cloud/user-guide/develop/authentication-keys)。

* 存取Adobe Commerce應用程式伺服器的命令列。

### 安裝步驟

使用撰寫器新增`adobe-commerce/module-data-exporter-status`模組：

```shell
composer require magento/module-data-exporter-status
```

如需詳細的安裝步驟，請參閱下列指南：

* 在雲端基礎結構上的Adobe Commerce上[安裝擴充功能](https://experienceleague.adobe.com/zh-hant/docs/commerce-on-cloud/user-guide/configure-store/extensions)

* [安裝擴充功能Adobe Commerce內部部署](https://experienceleague.adobe.com/zh-hant/docs/commerce-operations/installation-guide/tutorials/extensions)

## 存取資料摘要狀態頁面

從Commerce管理員，存取Commerce管理員的資料摘要狀態頁面： **[!DNL System]** >資料傳輸> **[!DNL Data Feed SyncStatus]**。

![資料摘要同步狀態頁面摘要資料摘要匯出活動](assets/data-feed-sync-status.png)

資料摘要狀態監視提供兩個介面：

* [資料摘要同步狀態摘要頁面](#data-feed-sync-status-summary)列出可用的摘要和目前狀態
* [資料摘要同步狀態 — 詳細資訊頁面](#data-feed-sync-status-details)會顯示所選摘要的詳細資訊。

## 資料摘要同步狀態摘要

摘要同步狀態摘要頁面提供資料摘要匯出活動的相關資訊，包括下列資訊：

| 欄位 | 說明 |
|-------|-------------|
| **摘要名稱** | 負責同步處理特定實體或其零件的摘要索引子名稱，例如產品或產品價格。 |
| **Source記錄** | 可從Commerce資料庫匯出的記錄數。 由於每個摘要專案都屬於特定範圍（例如商店檢視代碼），此數字可能會大於「Commerce管理員」中顯示的記錄數。 |
| **已成功傳送記錄** | 成功傳輸至Commerce SaaS以供進一步處理的記錄數。 如果在傳輸期間發生錯誤，則表示已成功傳輸至外部服務的記錄數。 |
| **個失敗的記錄** | 匯出失敗且需要注意的記錄數。 |
| **動作** | 選取&#x200B;**[!UICONTROL Details]**&#x200B;以檢視摘要的同步活動。 |

## 資料摘要同步狀態詳細資料

在資料摘要狀態摘要頁面中，按一下摘要名稱或使用[!DNL View Details]動作來存取摘要中個別記錄的詳細資訊。

具有摘要專案狀態報告的![[!UICONTROL Data Feed Sync Status - Details]頁面](assets/data-feed-sync-status-details.png)

詳細資料檢視會提供每個摘要專案的下列資訊：

| 欄位 | 說明 |
|-------|-------------|
| **摘要專案識別碼** | 摘要記錄的內部識別碼 |
| **實體識別碼** | 來源實體ID （產品ID、類別ID等） |
| **匯出狀態** | 摘要專案的[同步處理狀態](#export-status-types)。 使用顏色編碼指示器之匯出嘗試的目前狀態 |
| **上次同步日期** | 記錄上次傳送至Commerce服務的時間戳記 |
| **實體是否已刪除？** | 指示實體或其零件（例如產品或產品價格）是否已在Adobe Commerce中刪除。 只有在同步處理期間發生錯誤時，才會顯示專案。 |
| **要求ID** | 同步化要求的唯一識別碼。 提供此ID以支援疑難排解特定實體更新時使用。 |
| **錯誤** | 如果摘要專案同步化失敗，則提供詳細的錯誤資訊。 |

您可以使用下列控制項來管理檢視：

* [!DNL Mass Action]為選取的摘要專案排程重新同步
* [!DNL Filters]
* [!DNL Default View]以建立和儲存篩選的檢視，並在檢視之間切換
* [!DNL Columns]顯示和隱藏資料表中的資料行。

### 摘要健康狀態指標

在每個摘要詳細資訊頁面頂端，重要健康狀態指標提供每個摘要的系統狀態：

#### 索引器狀態

* **有效**：資料已同步化；不需要重新索引。
* **無效**：原始資料已變更；應該更新索引。
* **正在處理**：正在編制索引。

>[!TIP]
>
>若要深入瞭解索引處理，請參閱[索引管理](https://experienceleague.adobe.com/zh-hant/docs/commerce-admin/systems/tools/index-management)主題。

#### 變更記錄檔待處理專案

* **所有已同步**：沒有擱置的變更要處理
* 待處理專案中的&#x200B;**專案**：等待處理的擱置變更數目

### 匯出狀態型別

系統提供狀態指示器，幫助您快速識別問題：

#### 狀態類別

| **狀態** | **描述** | **需要動作** |
|--------|-----------|-------------|
| **已提交至服務** | 摘要專案已成功匯出至Commerce服務。 | 無 |
| **失敗，將重試** | 暫時失敗。 系統將自動重試。 | 監視解析度 |
| **失敗，需要注意** | 由於應用程式或資料錯誤而失敗。 | 調查並解決[!DNL Error]欄中的問題 |
| **正在等待提交** | 已排入匯出佇列，但尚未處理。 | 一般處理狀態 |

## 監視資料摘要狀態

當您更新Commerce資料庫中與產品和類別相關的實體時，資料會根據您的摘要設定傳輸至Commerce服務。 您可以從資料摘要同步狀態摘要頁面即時監視此程式。

>[!IMPORTANT]
>
>完成資料同步化的時間會依目錄大小、更新資料的量以及外部服務效能而有所不同。

當成功傳送的記錄數與來源記錄數相符時，表示同步處理已完成，且所有資料都已成功傳輸。

>[!NOTE]
>
>Adobe也提供開發人員和系統整合經銷商可用來管理和追蹤同步作業的命令列介面工具和系統記錄檔。 如需詳細資訊，請參閱[SaaS資料匯出指南](https://experienceleague.adobe.com/zh-hant/docs/commerce-merchant-services/saas-data-export/overview)。

### 管理失敗的匯出

若要檢視匯出失敗的詳細資料，並採取修正動作：

1. 在「摘要同步狀態」頁面中，尋找含有失敗記錄的摘要。
1. 按一下&#x200B;**[!DNL Details]**。

1. 檢閱特定失敗原因的錯誤訊息。

1. 使用整批動作來排定失敗專案的重新同步作業。

### 重新同步失敗的資料

您可以使用[!DNL Actions]頁面上的[!DNL Data Feed Sync Status - Details]功能表，手動重新同步失敗或有問題的資料摘要。

當系統自動重試某些型別的失敗時，在下列情況下可能需要手動介入：

* 您注意到驗證或許可權錯誤（401、403狀態代碼）。
* 解決導致裝載錯誤的資料格式問題後。
* 以下為外部服務設定或端點的更新。
* 您正在部署會影響資料匯出程式的自訂。

透過主動監控摘要狀態並及時解決故障，您可以維持整個Commerce生態系統的資料一致性和可靠性。

#### 手動重新同步摘要專案

如果您需要重新同步特定摘要專案：

1. **選取記錄**：使用核取方塊來選取需要注意的失敗記錄。
2. **選擇動作**：從大量動作下拉式清單中選取&#x200B;**[!DNL Schedule Resync]**。
3. **確認**：按一下&#x200B;**[!DNL Submit]**&#x200B;並確認重新同步作業。
4. **監視結果**：檢查成功訊息並監視狀態變更。

## 最佳實務

### 定期監視

1. **每日檢查**：每日檢閱概觀頁面，找出任何顯示高失敗率的摘要
1. **每週深入探討**：檢查重要摘要（產品、價格）的詳細狀態
1. **每月分析**：追蹤匯出成功率和效能的趨勢

### 疑難排解工作流程

1. **識別問題**：尋找錯誤和高失敗計數
1. **檢查索引器健康狀況**：確定索引器有效且可管理待處理專案
1. **檢閱錯誤詳細資料**：按一下失敗記錄即可檢視特定錯誤訊息
1. **排程重新同步**：使用大量動作重試失敗的匯出
1. **監視器解析度**：確認重新同步的專案顯示成功狀態

### 修正常見問題

#### 高失敗率

**症狀**：大量記錄顯示「失敗，需要注意」狀態

**可能的原因**：

* 外部服務設定變更
* 資料格式不相容
* 驗證或許可權問題

**解決步驟**：

1. 檢查外部服務狀態和設定
1. 檢閱錯誤訊息以瞭解模式
1. 驗證驗證認證
1. 如有需要，請聯絡外部服務支援

#### 匯出效能緩慢

**症狀**：變更記錄檔待處理專案太多，狀態更新緩慢

**可能的原因**：

* 索引器效能問題
* 高資料量
* 外部服務速率限制

**解決步驟**：

1. 檢查索引器狀態，如果無效則重新執行
2. 監視外部服務回應時間
3. 考慮在非尖峰時段排程匯出
4. 檢閱系統資源與效能

#### 驗證失敗

**症狀**： 401或403狀態碼

**解決步驟**：

1. 驗證API憑證和權杖
1. 檢查外部服務帳戶許可權
1. 更新過期的驗證權杖
1. 如需存取問題，請連絡您的服務提供者

>[!MORELIKETHIS]
>
>* [資料管理儀表板](https://experienceleague.adobe.com/zh-hant/docs/commerce-admin/systems/data-transfer/data-dashboard)
>* [SaaS資料匯出指南](https://experienceleague.adobe.com/zh-hant/docs/commerce-merchant-services/saas-data-export/overview)
