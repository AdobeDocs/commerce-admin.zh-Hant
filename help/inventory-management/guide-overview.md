---
title: Inventory management指南 [!DNL Inventory Management] 指南
description: 適用於Adobe Commerce和Magento Open Source管理員的 [!DNL Inventory Management] 相關完整資訊，包括移轉和設定。
seo-title: Adobe Commerce Inventory Management Guide
seo-description: Describes how to use the [!DNL Inventory Management] module in Adobe Commerce or Magento Open Source.
exl-id: 8013bc13-b057-4ad7-bbed-ee00c2f6e4eb
TQID: https://experienceleague.adobe.com/AFaKjUXrfZOMSYWjcW-dyD9OBMlQj6PkILIQiuT8YJU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 394
ht-degree: 0%

---

# [!DNL Inventory Management]指南總覽

本指南適用於Adobe Commerce和Magento Open Source Admin的管理員。 其中提供啟用此模組的詳細資訊，包括其功能的設定和管理。 它假定您對核心[!DNL Commerce]組態和功能有基本的瞭解。

[!DNL Inventory Management]有兩個管理員區域：

- 管理員：使用此區域來存取設定UI和報表。
- 命令列介面：使用此工具來執行安裝和後端組態工作。

本指南涵蓋：

| 主旨 | 說明 |
| ------- | ----------- |
| [簡介](introduction.md) | 您可用來管理多個位置庫存的[!DNL Inventory Management]功能總覽，好讓您的Commerce存放區能正確反映實際盤點。 |
| [發行說明](release-notes.md) | 檢閱發行說明以取得所有[!DNL Inventory Management]發行版本的相關資訊。 |
| 詳細目錄基本需知 | 瞭解管理存貨的基本知識： [庫存和來源](sources-stocks.md)、[來源選擇和預訂](selection-reservations.md)、[訂單和預訂狀態](order-status.md)以及[產品型別](product-types.md) |
| 開始使用 | 瞭解[!DNL Inventory Management]模組以及它如何適合您的Commerce執行個體和商店作業： [Commerce升級](migrate.md)、[模組安裝和更新](install-update.md)、[商家來源型別](merchant-sourcing.md)以及[來源結構變更](expand-restructure.md) |
| [組態](configuration.md) | 瞭解[!DNL Inventory Management]選項的組態，這些選項決定來源可用性、店面產品和訂單出貨。 |
| [管理來源](sources-manage.md) | 瞭解來源，以及來源如何定義管理及出貨產品存貨以進行訂單履行或提供服務的實際位置。 |
| [管理庫存](stocks-manage.md) | 瞭解如何使用存貨來代表您銷售管道來源的虛擬彙總產品詳細目錄。 |
| [管理數量](quantities-manage.md) | 瞭解如何為新產品指派來源和數量或變更現有產品。 |
| [管理訂單與出貨](shipments.md) | 瞭解其他[!DNL Inventory Management]功能和選項，用於透過出貨流程管理存貨數量。 |
| [CLI參考](cli.md) | 瞭解[!DNL Inventory Management]模組提供的命令，以管理清查資料和組態設定。 |

{style="table-layout:auto"}

## 開發人員資訊

如需模組架構、API和演演算法自訂的詳細資訊，請參閱開發人員檔案中的[[!DNL Inventory Management]](https://developer.adobe.com/commerce/webapi/rest/inventory/)。

## Commerce檔案

{{docs-links}}

## 疑難排解與支援

如果您需要本指南未涵蓋的資訊或問題，請使用下列資源：

- [安裝詳細目錄後庫存狀態不正確](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/stock-status-incorrect-after-magento-inventory-install.html)
- [支援票證](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket) — 提交票證以接收其他說明。
