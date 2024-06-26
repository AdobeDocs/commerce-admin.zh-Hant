---
title: 資料管理控制面板
description: 瞭解如何存取資料串流的深入分析 [!DNL Catalog Service]， [!DNL Live Search]、和 [!DNL Product Recommendation]s.
feature: Products, Customers, Data Import/Export
exl-id: 63c261c1-1a52-46f7-93f8-81055edf1f7b
source-git-commit: 4495a27b57c04c6f9c37b2c5237b5f2233cc8532
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# 資料管理控制面板

資料管理儀表板提供從Commerce資料庫傳輸到Commerce SaaS服務之產品資料的同步狀態概觀。 使用者可以方便地監視產品同步狀態，並從統一的儀表板起始資料重新同步。 此功能可為您的店面提供寶貴的產品資料可用性深入分析，確保可及時向購物者顯示。

## 對象

所有Commerce商家均可使用資料管理控制面板，不需額外付費， [[!DNL Product Recommendations v6.0.0]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview)， [[!DNL Live Search v4.1.0]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/guide-overview)，或 [[!DNL Catalog Service v1.17]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/catalog-service/guide-overview) 具有使用中的授權。

資料管理儀表板位於 *系統* >資料傳輸> *資料管理控制面板*.

![資料管理控制面板](assets/data-management-dashboard.png)

儀表板包含下列欄位：

| 欄位 | 說明 |
|--- |--- |
| 範圍 | 同步資料的特定網站。 |
| [!DNL Product Recommendations] | 顯示同步狀態、同步的產品數目，以及 [可顯示](https://experienceleague.adobe.com/en/docs/commerce-admin/config/catalog/inventory#stock-options) 以下專案的同步產品： [!DNL Product Recommendations]. |
| [!DNL Live Search] | 顯示同步狀態、同步的產品數目，以及 [可顯示](https://experienceleague.adobe.com/en/docs/commerce-admin/config/catalog/inventory#stock-options) 以下專案的同步產品： [!DNL Live Search]. |
| [!DNL Catalog Service] | 顯示同步狀態、已同步的產品數目以及已同步產品的表格。 [!DNL Catalog Service]. |
| 設定 | 開啟對話方塊，您可以 [手動重新同步目錄資料](#resync-catalog-data). |
| 同步狀態 | 顯示過去三小時內已從Commerce資料庫傳輸至任何SaaS服務的產品數量。 如果您不經常更新目錄，此值通常為零。 如果同步正在進行中，請按一下 **[!UICONTROL Refresh]** 以取得更新的計數。 |
| 產品計數 | 反映服務可用的目錄產品總數。 此 [!DNL Product Recommendations] 和 [!DNL Live Search] 儀表板顯示總數 _可顯示_ 產品。 [!DNL Catalog Service] 不會依可顯示內容來篩選產品，因此如果您同時擁有兩者 [!DNL Catalog Service] 和 [!DNL Live Search] 或 [!DNL Product Recommendations] 安裝後，兩個控制面板可能會顯示產品計數的兩個不同值。 |
| 同步的產品 | 提供有關核心Commerce索引中產品的詳細資訊。 根據預設，此表格會依「上次更新」排序。 若要尋找特定產品，請使用 **[!UICONTROL Search by SKU]** 欄位。 若要控制要顯示的欄，請按一下 **[!UICONTROL Customize Table]** 在表格的右側。 |

## 使用資料管理儀表板

當您更新Commerce資料庫中的產品時，產品資料會根據您的系統組態傳輸至SaaS服務。 啟動同步程式時， **產品計數** 表示傳送至SaaS服務的產品數目。

>[!IMPORTANT]
>
>完成同步所需的時間會因目錄大小和更新資料的數量而異。

當處理的產品數目與更新的產品數目相符時，表示同步已完成。

>[!NOTE]
>
>Adobe也提供命令列介面和系統記錄，供開發人員和系統整合經銷商用來管理和追蹤同步作業，以及Commerce SaaS服務的疑難排解錯誤。 如需詳細資訊，請參閱 [SaaS資料匯出指南](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview).

### 同步的產品清單

若要檢視同步產品的詳細資訊，請按一下表格中的產品。

![同步產品詳細資料](assets/sync-product-detail.png)

### 重新同步目錄資料

為確保您的Commerce SaaS服務一律包含最新產品資訊，您應： [實作排程](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/cli/manage-indexers#reindex) 用於同步目錄資料。

雖然您可以 [手動啟動](#manually-resync-catalog) 不建議將目錄資料從Commerce資料庫重新同步至SaaS服務，因為這會增加硬體資源的負載。 但是，在下列情況下可能需要手動重新同步目錄：

- 每當對產品目錄進行重大變更時（例如新增產品、更新產品詳細資料或修改類別）

- 如果您發現商店正面顯示產品資料時發生任何差異或效能問題

- 在對Commerce資料庫和SaaS服務之間的整合進行任何更新或變更後

- 部署影響產品資料管理或同步程式的自訂專案或設定時

遵守這些指引，並視需要主動重新同步目錄資料，就能在Adobe Commerce生態系統中維持資料的一致性、正確性和可靠性。

#### 手動重新同步目錄

如果您需要重新同步目錄資料，請按一下 **[!UICONTROL Settings]** 在頁面右側顯示一個對話方塊，您可以在此啟動重新同步。 重新同步目錄資料會強制服務從Commerce資料庫重新擷取資料至SaaS服務。

![手動同步產品](assets/resync-data.png)
