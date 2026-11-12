---
title: 依角色的目錄銷售任務
description: 尋找使用以CCDM布建的Adobe Commerce as a Cloud Service執行個體的管理員、開發人員和銷售人員的任務指南。
role: Admin, Developer
recommendations: noCatalog
badgeSaas: label="僅限SaaS" type="Positive" url="https://experienceleague.adobe.com/zh-hant/docs/commerce/user-guides/product-solutions" tooltip="僅適用於以CCDM布建的Adobe Commerce as a Cloud Service執行個體（Adobe管理的SaaS基礎結構）。"
TQID: 'https://experienceleague.adobe.com/0PmobUkdEWspxuRSaIPL8vS1ojDDZ3gw-L-3SfPmJAg'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
feature_v2:
  - id: cc04bd17-78d5-5120-8c3d-1b8a57e49280
    internal-label: Integration
  - id: dec06508-d41f-555a-87e8-29e8bcdfa95a
    internal-label: Recommendations
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
    internal-label: Architecture
  - id: f37757d8-3174-5335-b977-1161792f965d
    internal-label: Personalization
subfeature_v2:
  - id: f8ddfd3b-6194-46e8-a176-0e918039be56
    internal-label: Cloud architecture
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: dba482e5-29a8-4127-afa2-c4b913512ef8
    internal-label: Data and analytics
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
    internal-label: Data integration
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 742236e7fdb26c56a80f66a44b0a4960210f4dac
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 0%
---

# 依角色將銷售任務分類

使用本工作參考來尋找在Adobe Commerce as a Cloud Service例項中設定目錄資料、整合店面、管理銷售以及檢閱效能的指引，這些例項是以可撰寫目錄資料模型(CCDM)布建。

責任因實施而異。 下列段落會依照通常執行工作的角色來分組工作。

- 管理員可在Commerce Foundation中管理產品、價格和B2B設定。
- 開發人員設定店面整合，並驗證目錄請求和行為資料收集。
- 銷售人員設定產品探索和推薦，並使用報告來通知銷售決策。

透過原生Adobe Commerce as a Cloud Service整合，將產品和價格資料同步至CCDM。 不需要另外安裝聯結器或App Builder應用程式。

## 準備目錄和店面

完成適用於實作的工作。 B2C目錄檢視可以手動建立。 B2B目錄檢視、原則和價格手冊是從Commerce Foundation中的B2B設定產生的。

| 任務 | 說明 | 資源 |
| --- | --- | --- |
| **設定產品和價格** | 在Commerce Foundation中管理產品和價格。 價格資料會同步至CCDM做為價格手冊；請勿獨立撰寫CCDM中的價格。 | [產品清單](../catalog/products-list.md)、[建立產品](../catalog/product-create.md)、[價格範圍](../catalog/catalog-price-scope.md)和[進階價格](../catalog/pricing-advanced.md) |
| **設定存放區檢視** | 在Commerce Foundation中設定店面所需的商店檢視和當地語系化的產品資料。 | [存放區檢視](../stores-purchase/store-views.md) |
| **設定B2B共用目錄和公司** | 針對B2B實作，請先在Commerce Foundation中設定共用目錄和公司關係，然後再檢閱產生的目錄設定。 | [共用目錄](../b2b/catalog-shared.md)與[公司](../b2b/account-companies.md) |
| **設定B2C目錄檢視與原則** | 建立目錄檢視並選取定義可用產品分類的原則。 將適用的已同步價格簿與每個檢視表建立關聯。 | [目錄檢視](./setup/catalog-view.md) |
| **檢閱B2B目錄檢視** | 確認原生同步處理已產生預期的目錄檢視、原則和價格簿。 在Commerce Foundation中管理基礎B2B設定，而非手動建立重複結構。 | [B2B目錄檢視](./setup/catalog-view.md#b2b-catalog-views) |
| **設定店面** | 設定店面以請求預期的目錄內容。 對於自訂或其他店面整合，檢閱適用的目錄請求標頭。 | [店面組態](https://experienceleague.adobe.com/en/tools/commerce-storefront/setup/configuration/commerce-configuration/) |

設定銷售之前，請確認店面會傳回預期的產品和價格。 測試加入購物車、購物車和結帳，驗證交易定價符合預期的Commerce Foundation設定。

## 設定銷售與檢閱績效

| 任務 | 說明 | 資源 |
| --- | --- | --- |
| **設定產品探索** | 設定銷售規則、多面向和同義字。 規則可套用至所有目錄檢視或針對特定檢視量身打造。 | [銷售概述](./merchandising/overview.md) |
| **檢閱搜尋設定** | 檢閱實作的搜尋設定和可用的語意搜尋選項。 | [銷售設定](./settings.md)和[語意搜尋](./setup/semantic-search.md) |
| **設定建議** | 建立建議單位，並確認店面會收集實施所需的行為資料。 | [建議總覽](./merchandising/recommendations/overview.md) |
| **檢閱績效** | 使用成功量度和搜尋績效報告來評估店面活動並告知銷售決策。 | [成功量度](./manage-results/success-metrics.md)和[搜尋效能](./manage-results/search-performance.md) |

## 後續步驟

設定銷售與檢閱效能後，繼續視需要監控和調整您的規則、Facet和建議，以最佳化店面體驗。
