---
title: '[!DNL Inventory Management] 指南'
description: 適用於Adobe Commerce和Magento Open Source中 [!DNL Inventory Management] 庫存、來源、數量、組態、訂單及出貨的管理與CLI指南。
seo-title: Adobe Commerce Inventory Management Guide
seo-description: Describes how to use the [!DNL Inventory Management] module in Adobe Commerce or Magento Open Source.
exl-id: 8013bc13-b057-4ad7-bbed-ee00c2f6e4eb
TQID: https://experienceleague.adobe.com/AFaKjUXrfZOMSYWjcW-dyD9OBMlQj6PkILIQiuT8YJU
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c1579802-ddd4-4214-8a91-97b2066abe11id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 94e419120b8e16848cc1d449650f023f361a2af7
workflow-type: tm+mt
source-wordcount: 329
ht-degree: 1%

---

# [!DNL Inventory Management] 概覽

本指南適用於在Adobe Commerce和Magento Open Source中管理多個位置庫存的管理員。 它提供[!DNL Inventory Management]模組的設定和管理程式，並假設對核心[!DNL Commerce]功能有基本的瞭解。

使用&#x200B;**管理員**&#x200B;進行設定、報告和日常清查工作。 使用&#x200B;**命令列介面**&#x200B;進行安裝、升級和後端設定。

本指南涵蓋：

| 主旨 | 說明 |
| ------- | ----------- |
| [簡介](introduction.md) | 功能、術語，以及[!DNL Inventory Management]如何適合您的商店。 |
| [發行說明](release-notes.md) | 模組發行版本記錄和已知問題。 |
| [詳細目錄基本資訊](sources-stocks.md) | [庫存與來源](sources-stocks.md)、[來源選擇與預訂](selection-reservations.md)、[訂單與預訂狀態](order-status.md)與[產品型別](product-types.md)的概念。 |
| 開始使用 | [Commerce升級](migrate.md)、[安裝和更新](install-update.md)、[商家來源型別](merchant-sourcing.md)和[庫存重組](expand-restructure.md)。 |
| [組態](configuration.md) | 店面展示和運送的全域、產品和演演算法設定。 |
| [管理來源](sources-manage.md) | 建立及維護履行地點。 |
| [管理庫存](stocks-manage.md) | 將來源對應至銷售管道。 |
| [管理數量](quantities-manage.md) | 指定並更新每個來源的產品數量。 |
| [管理訂單與出貨](shipments.md) | 履行訂單並管理存貨的出貨。 |
| [CLI參考](cli.md) | 命令列清查和設定工作。 |

{style="table-layout:auto"}

## 開發人員資訊

存取API、自訂和模組架構的進階資源。 如需API與演演算法自訂的技術詳細資訊，請參閱REST API開發人員檔案中的[[!DNL Inventory Management]](https://developer.adobe.com/commerce/webapi/rest/inventory/)。

## Commerce檔案

尋找商家、雲端和開發人員指南，以協助Adobe Commerce的每個部分。 使用這些資源滿足任何設定或管理需求。

{{docs-links}}

## 疑難排解與支援

使用支援文章和票證系統快速解決詳細目錄問題。 取得庫存狀態或產品管理的額外說明。

如果您需要本指南未涵蓋的資訊或問題，請使用下列資源：

- [安裝詳細目錄後庫存狀態不正確](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/stock-status-incorrect-after-magento-inventory-install.html)
- [支援票證](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket) — 提交票證以接收其他說明。
