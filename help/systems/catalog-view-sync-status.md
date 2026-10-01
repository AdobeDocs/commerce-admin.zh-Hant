---
title: 目錄檢視同步狀態監視
description: 監視Adobe Commerce Optimizer Connector的B2B共用目錄投影健康情況，並協調目錄檢視、原則、價格手冊和存取金鑰。
feature: Products, Customers, Data Import/Export
role: Admin
level: Intermediate
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: b974b164-8a4e-43b8-a9e2-8e67ec131677
    internal-label: Commerce on Prem
  - id: cdf0c6dd-1717-4e20-9530-a24eee57088b
    internal-label: Commerce on Cloud
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
    internal-label: Reporting
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
    internal-label: Data management
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 9ec73be87dd329dc04e7b133885fcc156f4ffcb6
workflow-type: tm+mt
source-wordcount: '1332'
ht-degree: 0%
---

# 目錄檢視同步狀態監視

您可以使用「目錄檢視：同步狀態」頁面來監視同步作業，以及疑難排解預計要投影到Adobe Commerce Optimizer的目錄檢視。 對於每個自訂共用目錄，[!DNL Adobe Commerce Optimizer Connector for B2B]會為共用目錄網站範圍內的每個商店檢視建立一個目錄檢視。 每個目錄檢視都設定了分類原則、其連結的價格手冊以及用於驗證限制存取權杖的公開金鑰。 Adobe Commerce會保留對應的目錄檢視中繼資料，包括私密金鑰和預設價格簿ID。

>[!NOTE]
>
>若要追蹤目錄資料摘要的同步處理狀態，請使用[[!UICONTROL Data Feed Sync Status]](data-feed-sync-status.md)頁面。

## 對象與可用性 {#audience}

僅[!BADGE 個PaaS]{type=Informative url="https://experienceleague.adobe.com/zh-hant/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端基礎結構上的Adobe Commerce和內部部署專案。"}

使用B2B共用目錄與[!DNL Adobe Commerce Optimizer Connector for B2B]整合的Adobe Commerce on Cloud Infrastructure和內部部署商家可以使用[!UICONTROL Catalog View Sync Status]頁面。 頁面會在聯結器擴充功能安裝後自動安裝及啟用。

## 存取「目錄檢視同步處理狀態」頁面 {#access-catalog-view-sync-status-page}

從管理區域，瀏覽至&#x200B;**[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Catalog View Sync Status]**。

![目錄檢視同步狀態頁面列出目錄檢視及其同步狀況](assets/catalog-view-sync-status.png){width="600" zoomable="yes"}

此頁面有三個索引標籤：

- **[!UICONTROL Catalog Views]** — 聯結器建立的目錄檢視，每個檢視都有同步處理狀況。 檢視[目錄檢視同步處理狀態摘要](#catalog-view-sync-status-summary)。
- **[!UICONTROL Orphaned in ACO]** — 存在於[!DNL Adobe Commerce Optimizer]中沒有對應[!DNL Adobe Commerce]來源的實體。 請參閱[在ACO索引標籤](#orphaned-in-aco-tab)中孤立。
- **[!UICONTROL Deleted]** — 目錄檢視投影的記錄已移除，因為其共用目錄已刪除。 請參閱[已刪除的索引標籤](#deleted-tab)。

## 目錄檢視同步狀態摘要 {#catalog-view-sync-status-summary}

頁面頂端的摘要卡片會顯示每個健全狀態中的目錄檢視次數，加上將在30天內到期的受限制存取金鑰計數：

| 卡片 | 說明 |
| --- | --- |
| **狀況良好** | 沒有偵測到漂移的目錄檢視。 |
| **已降級** | 具有可修復漂移的目錄檢視。 |
| **失敗** | 從未建立或直接在[!DNL Adobe Commerce Optimizer]中刪除的目錄檢視。 |
| **金鑰≤30D** | 限制存取金鑰30天內過期。 |

網格會為每個目錄檢視列出一列：

| 欄位 | 說明 |
| --- | --- |
| **目錄檢視** | 投影到[!DNL Adobe Commerce Optimizer]中的目錄檢視的識別碼。 |
| **Source** | 投影目錄檢視的共用目錄。 選取連結，在「管理員」中開啟共用目錄。 |
| **存放區檢視** | 目錄檢視代表的存放區檢視。 |
| **公司** | 目前連結至此目錄檢視的公司數。 |
| **狀態** | 目錄檢視的整體同步處理狀況。 檢視[同步處理狀態值](#sync-status-values)。 |
| **原則** | 指派給此目錄檢視的分類原則是否符合您的[!DNL Adobe Commerce]設定。 |
| **價格簿** | 指派給此目錄檢視的價格簿是否與您的[!DNL Adobe Commerce]組態相符。 |
| **存取金鑰** | 受限制的存取金鑰是否已連結至此目錄檢視。 |
| **金鑰過期** | 目錄檢視的受限制存取金鑰的到期日，以及剩餘天數。 |
| **漂移** | 偵測到的漂移型別（如果有的話）。 |
| **上次調解時間** | 調解程式上次檢查此目錄檢視的時間。 |
| **動作** | **[!UICONTROL View details]**&#x200B;會開啟[目錄檢視同步處理狀態詳細資訊]頁面，以檢視目前狀態、漂移、存取金鑰以及最近的事件。 **[!UICONTROL Open in ACO admin]**&#x200B;在[!DNL Adobe Commerce Optimizer] Studio中開啟目錄檢視詳細資訊頁面。 **[!UICONTROL Copy ID]**&#x200B;複製目錄檢視識別碼以供參考。 請參閱[調解與修復漂移](#reconcile-and-repair-drift)。 |

## 同步狀態值 {#sync-status-values}

| 狀態 | 含義 |
| --- | --- |
| **狀況良好** | 未偵測到任何漂移。 目錄檢視、原則、價格手冊和金鑰符合您的[!DNL Adobe Commerce]設定。 |
| **已降級** | 偵測到漂移，且可修復，例如，原則或價格簿在[!DNL Adobe Commerce Optimizer]中直接變更。 |
| **失敗** | 從未建立目錄檢視，或直接在[!DNL Adobe Commerce Optimizer]中刪除。 |
| **擱置中** | 目錄檢視尚未調解，或正在等待其第一個投影。 |
| **正在退休** | 共用目錄已在[!DNL Adobe Commerce]中刪除，且目錄檢視位於其刪除寬限期內。 |
| **已刪除** | 目錄檢視投影已在其寬限期後移除。 在[!UICONTROL Deleted]標籤上將其記錄保留90天。 |
| **孤立** | 目錄檢視或索引鍵存在於[!DNL Adobe Commerce Optimizer]中，但沒有對應的[!DNL Adobe Commerce]來源。 請參閱[在ACO索引標籤](#orphaned-in-aco-tab)中孤立。 |

### 設定刪除寬限期 {#configure-the-deletion-grace-period}

刪除寬限期會指定刪除關聯的共用目錄後，目錄檢視和相關聯資料的資料保留時段。 此值預設為7天。
視窗過期後，所有資料都會被移除。

#### 變更資料保留設定

1. 開啟[!DNL Adobe Commerce]管理員。

1. 從&#x200B;**[!UICONTROL Stores]**&#x200B;功能表選取&#x200B;**[!UICONTROL Configuration]** > **[!UICONTROL Services]** > **[!UICONTROL ACO Catalog View Sync]** > **[!UICONTROL Deletion]** > **[!UICONTROL Deletion Grace Period (days)]**。

1. 視需要更新&#x200B;**[!UICONTROL Deletion Grace Period (days)]**&#x200B;值。

   若要在刪除共用目錄之後立即移除目錄檢視ACO投影，請將此值設定為`0`。

1. 選取&#x200B;**[!UICONTROL Save Config]**。

如需詳細資訊，請參閱[服務> ACO目錄檢視同步](../configuration-reference/services/aco-catalog-view-sync.md)，瞭解所有可用的同步和漂移調解器設定。

## 調解及修復組態差異 {#reconcile-and-repair-drift}

[!DNL Adobe Commerce]是B2B共用目錄投影的授權來源。 調解會比較您的[!DNL Adobe Commerce]設定與[!DNL Adobe Commerce Optimizer]，並報告或修復任何差異。

>[!IMPORTANT]
>
>在[!DNL Adobe Commerce Optimizer]中直接對聯結器管理的目錄檢視、原則、價格簿或金鑰所做的變更，並非主要真實來源。 調解會將這些差異報告為組態差異，當您修復時，會將它們回覆成符合[!DNL Adobe Commerce]。 在[!DNL Adobe Commerce]中進行設定變更，而不是在[!DNL Adobe Commerce Optimizer]中進行變更。 「修復」不會移除您手動新增且隨聯結器管理原則一併加入的原則。

使用頁面層次按鈕來調解：

- **[!UICONTROL Reconcile]** — 檢查組態差異並更新同步處理狀態，而不需在[!DNL Adobe Commerce Optimizer]中進行任何變更。

- **[!UICONTROL Reconcile & Repair]** — 檢查組態差異，並自動還原任何可修復差異的預期組態。

  選取&#x200B;**[!UICONTROL Reconcile & Repair]**&#x200B;會傳送非同步調解要求，並在修復執行前傳回。 確認訊息會立即顯示狀態重新整理，但頁面不會自動重新載入。 等候處理完成，然後重新整理網格以檢查結果。

使用資料列上的&#x200B;**[!UICONTROL Action]**&#x200B;功能表可以：

- **[!UICONTROL View details]** — 開啟[目錄檢視] [同步狀態]詳細資訊頁面，檢視目前狀態、漂移、存取金鑰和最近事件。
- **[!UICONTROL Open in ACO admin]** — 在[!DNL Adobe Commerce Optimizer] Studio中開啟目錄檢視詳細資訊頁面。
- **[!UICONTROL Copy ID]** — 複製目錄檢視ID以供參考。

## 在ACO標籤中孤立 {#orphaned-in-aco-tab}

**[!UICONTROL Orphaned in ACO]**&#x200B;索引標籤列出存在於[!DNL Adobe Commerce Optimizer]中但沒有對應[!DNL Adobe Commerce]來源的目錄檢視和受限制的存取金鑰，例如，在[!DNL Adobe Commerce Optimizer] Studio中手動建立的實體，而不是由聯結器建立的實體。 這些實體無法出現在主格線中，因為沒有可比對它們的[!DNL Adobe Commerce]記錄。

![在ACO索引標籤中孤立，列出沒有Adobe Commerce來源的實體](assets/catalog-view-sync-orphan.png){width="600" zoomable="yes"}

| 欄位 | 說明 |
| --- | --- |
| **型別** | 孤立實體的類別： [!UICONTROL Catalog View]或[!UICONTROL Access Key]。 |
| **ACO ID** | [!DNL Adobe Commerce Optimizer]中實體的識別碼。 |
| **詳細資料** | 有關實體的其他內容，例如其原則。 |
| **第一次出現** | 調解首次偵測到此實體時。 |
| **動作** | 選取&#x200B;**[!UICONTROL Copy ID]**&#x200B;以複製實體識別碼。 使用複製的ID尋找並移除[!DNL Adobe Commerce Optimizer] Studio目錄檢視中的實體。 |

>[!NOTE]
>
>此標籤僅供報表使用。 調解不會刪除孤立的實體。 如果不再需要它們，請直接在[!DNL Adobe Commerce Optimizer] Studio中移除。

## 已刪除索引標籤 {#deleted-tab}

**[!UICONTROL Deleted]**&#x200B;索引標籤列出因共用目錄已在[!DNL Adobe Commerce]中刪除而被移除的目錄檢視預測。 由於共用目錄及其目錄檢視已不存在，因此這些列不會在任何地方連結。 這些檔案只會記錄已移除的內容。

![已刪除索引標籤，列出刪除共用目錄後移除的目錄檢視預測](assets/catalog-view-sync-deleted.png){width="600" zoomable="yes"}

| 欄位 | 說明 |
| --- | --- |
| **目錄檢視** | 已移除目錄檢視的識別碼。 |
| **Source** | 已刪除的共用目錄。 |
| **存放區檢視** | 存放區檢視所代表的目錄檢視。 |
| **刪除於** | 移除投影時。 |

90天後會自動清除此標籤上的列。

## 已知限制

- [!DNL Adobe Commerce Optimizer] Studio中沒有視覺指示器，可用來區分聯結器管理的目錄檢視與手動建立的目錄檢視。 使用此頁面（而非[!DNL Adobe Commerce Optimizer] Studio UI）來決定聯結器要管理的專案。
- **[!UICONTROL Orphaned in ACO]**&#x200B;索引標籤的&#x200B;**[!UICONTROL ACO ID]**&#x200B;欄識別目錄檢視、原則或存取金鑰，而非唯一識別碼。 欄的命名可能會有所變更。

>[!MORELIKETHIS]
>
> - [管理目錄檢視設定](/help/b2b/catalog-views-manage.md) — 從共用目錄或公司帳戶檢閱目錄檢視
> - [資料摘要同步處理狀態](data-feed-sync-status.md)
> - [服務> ACO目錄檢視同步處理](../configuration-reference/services/aco-catalog-view-sync.md) — 設定刪除與建立寬限期，以及漂移調解器
> - [受限制的存取金鑰管理](restricted-access-keys.md) — 管理此頁面顯示其到期的金鑰
> - [在&#x200B;*Adobe Commerce Optimizer Connector指南*&#x200B;中監視B2B共用目錄的目錄檢視同步處理](https://experienceleague.adobe.com/en/docs/commerce/aco-optimizer-connector/manage-sync/catalog-view-sync/catalog-view-sync-status)
> - [私人目錄檢視](https://experienceleague.adobe.com/zh-hant/docs/commerce/optimizer/setup/private-catalog-view)
> - [受限制的存取金鑰](https://experienceleague.adobe.com/zh-hant/docs/commerce/optimizer/setup/restricted-access-keys)
