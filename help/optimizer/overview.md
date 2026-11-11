---
title: Merchandising Services概述
description: 瞭解為布建CCDM的Adobe Commerce as a Cloud Service執行個體提供的目錄設定、銷售、報告和監視工具。
recommendations: noCatalog
badgeSaas: label="僅限SaaS" type="Positive" url="https://experienceleague.adobe.com/zh-hant/docs/commerce/user-guides/product-solutions" tooltip="僅適用於以CCDM布建的Adobe Commerce as a Cloud Service執行個體（Adobe管理的SaaS基礎結構）。"
exl-id: f9516d4c-fbae-4db2-a1a9-cda3684a8122
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: a6a5a899ba60097bd6baf2a5de14063a0af2f313
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 0%
---
# 搭配CCDM的銷售服務概覽

以Composable Catalog Data Model (CCDM)布建的Adobe Commerce as a Cloud Service執行個體在Adobe Unified Experience的[Commerce Admin中提供目錄設定、銷售、報告和監視工具。](../getting-started/admin-unified-experience.md) CCDM與支援Adobe Commerce Optimizer的目錄基礎相同。

使用銷售服務，您可以：

- 使用您Adobe Commerce as a Cloud Service例項的目錄資料來支援店面體驗。
- 設定目錄檢視和原則，以定義店面產品分類。
- 跨所有目錄檢視套用銷售規則，或針對特定檢視量身打造。
- 設定產品建議、搜尋Facet和同義字。
- 透過成功量度和搜尋績效報告來檢閱店面績效。
- 監視目錄同步和擷取的店面事件。

Commerce Foundation依然是產品和價格的真實來源，並繼續管理購物車、結帳和其他異動操作。

## 快速導覽

>[!BEGINTABS]

>[!TAB 目錄組態]

設定店面可用的目錄內容。

- **目錄檢視** — 結合目錄來源、原則和價格簿以定義店面可擷取的產品和定價。 檢視[目錄檢視](./setup/catalog-view.md)。
- **目錄層** — 覆寫選取的產品屬性，而不變更來源資料。 針對產品影像使用AEM Assets時，會透過產品視覺效果套用AEM-Assets圖層。 請參閱[目錄圖層](./setup/catalog-layer.md)。
- **私人目錄檢視** — 啟用目錄保護在擷取目錄檢視的資料時，需要有效的已簽署權杖。 檢視[私人目錄檢視](./setup/private-catalog-view.md)。

>[!TAB 原則]

原則會根據產品屬性，篩選透過目錄檢視可用的產品。 例如，原則可將分類限製為特定品牌或產品類別。

原則會決定可用的產品分類。 它們不會取代目錄保護，後者控制對私人目錄檢視的存取權。

>[!TAB 銷售]

設定購物者如何發現產品以及在可用分類中如何促銷產品。

- **商機** — 檢閱產品績效、購物者行為和搜尋趨勢，以找出銷售改善的領域。
- **建議** — 在Commerce管理中建立和管理建議單位。 Recommendations會使用目錄資料和彙總的購物者行為來建議相關產品，例如「也檢視過此產品的客戶」。
- **銷售規則** — 控制產品如何促銷和排名。 規則可套用至所有目錄檢視或針對特定檢視量身打造。 請參閱[建立銷售規則](https://experienceleague.adobe.com/zh-hant/docs/commerce/optimizer/merchandising/rules/add#create-a-rule)。
- **Facet** — 設定購物者用來依品牌、大小或價格等屬性縮小產品結果的篩選器。
- **同義字** — 關聯對等搜尋字詞，以協助購物者找到使用相同概念之不同字詞的產品。
- **設定** — 設定搜尋和銷售選項，包括價格層面、語言和進階搜尋。

原則會決定可透過目錄檢視使用的產品。 銷售規則可控制該分類中產品的促銷和排名方式。

如需搜尋結果如何比對和排名的詳細資訊，請參閱[搜尋比對和排名](./manage-results/search-relevance-matching.md)。

>[!TAB 報告]

使用報告檢閱店面活動並通知銷售決策。

- **成功量度** — 根據店面活動檢閱收入、轉換、參與、贏取和跳出率。
- **搜尋績效** — 檢閱購物者使用的搜尋字詞及其績效，以識別精簡產品探索的區域。

報表取決於實作所收集的店面活動資料。

>[!TAB 系統組態]

監控目錄同步和店面事件收集，以調查資料可用性和實施問題。

- **目錄同步** — 檢閱從Commerce Foundation傳輸之目錄資料的同步處理狀態。
- **事件** — 檢閱產品探索、建議和報告所使用的已擷取店面事件。 使用「事件」頁面來協助驗證行為資料收集，以及調查遺失或未預期的事件。

>[!ENDTABS]
<!--
Watch the following video for a high-level overview of [!DNL Adobe Commerce Optimizer]:

>[!VIDEO](https://video.tv.adobe.com/v/3450226)
-->

## 確認執行個體使用CCDM

1. 透過Unified Shell登入Commerce Admin，並選取預定的Adobe Commerce as a Cloud Service執行個體。
1. 確認可在執行個體的導覽中使用CCDM銷售頁面，例如「目錄檢視」和「原則」 。
1. 如果這些頁面無法使用，請確認您選取了正確的執行個體並且正在使用Unified Shell。

   請聯絡Adobe支援或Commerce布建團隊，確認執行個體的CCDM布建狀態。

執行個體的「就緒」狀態會確認其已布建，但本身不會確認其使用CCDM。

