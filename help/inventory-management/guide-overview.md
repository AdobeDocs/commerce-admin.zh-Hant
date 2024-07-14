---
title: 'Inventory management指南 [!DNL Inventory Management] 指南'
description: 有關Adobe Commerce和Magento Open Source管理員 [!DNL Inventory Management] 的完整資訊，包括移轉和設定。
seo-title: Adobe Commerce Inventory Management Guide
seo-description: Describes how to use the [!DNL Inventory Management] module in Adobe Commerce or Magento Open Source.
exl-id: 8013bc13-b057-4ad7-bbed-ee00c2f6e4eb
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---

# [!DNL Inventory Management]指南總覽

本指南適用於Adobe Commerce和Magento Open Source的管理員。 其中提供啟用此模組的詳細資訊，包括其功能的設定和管理。 它假定您對核心[!DNL Commerce]組態和功能有基本的瞭解。

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

- [大量預訂不一致](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-8/mdva-30112-magento-patch-large-number-reservation-inconsistencies.html)
- [庫存不一致性問題](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-14/mdva-33281-magento-patch-inventory-inconsistency-issues.html)
- [未刪除的色票清查達到「0」](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-17/mdva-34850-swatches-not-strike-through-inventory-reaches-0.html)
- 安裝詳細目錄後[庫存狀態不正確](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/stock-status-incorrect-after-magento-inventory-install.html)
- [支援票證](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket) — 提交票證以接收其他說明。
