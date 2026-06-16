---
title: Admin System指南
description: 了解最佳安全實務以保護您的 Commerce 商店及管理各項權限，並了解如何匯入和匯出資料、管理整合和擴充功能以及進行日常維護。
exl-id: 9d22571e-9e09-4d1a-ba55-a889f094158d
TQID: https://experienceleague.adobe.com/TMdBCvfpmoU6cWCqaC8W4JJpIiyt4tXY7Lun7-p-rHA
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c32adafa-ed01-4b31-997e-2413013911b0
  - id: cc250cf1-34eb-4863-80d0-d170d45ea067
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 430
ht-degree: 6%

---

# Adobe Commerce管理系統指南

本指南適用於使用Adobe Commerce和Magento Open Source Admin的系統管理員和整合人員。 它提供有關管理員安全性、維護操作的詳細資訊，以及支援您的電子商務企業之多個組織功能活動的系統範圍資源。 它假定您對核心Commerce設定和功能有基本的瞭解。

本指南涵蓋：

| 主旨 | 說明 |
| ------- | ----------- |
| [簡介](introduction.md) | Commerce例項中的系統和整合功能概觀。 |
| [系統功能表](system-menu.md) | 使用[!UICONTROL System]功能表存取資料匯入與匯出、系統快取與索引管理、使用者帳戶與許可權管理、備份、系統通知與自訂變數的工具。 |
| [管理員帳戶和許可權](permissions.md) | 管理用來授與存放區功能存取權的管理員使用者帳戶和角色。 |
| [變數](variables-predefined.md) | 變數可讓您輕鬆個人化電子郵件和新聞稿範本，以及其他型別的內容，以支援您的網站和客戶體驗。 |
| [電子郵件範本](email-templates.md) | 電子郵件範本定義從您的商店傳送之自動化訊息的配置、內容和格式。 這些電子郵件稱為交易式電子郵件，因為每個電子郵件都與特定型別的交易或事件相關聯。 |
| [資料傳輸](data-transfer.md) | <ul><li>匯入和匯出工具可讓您在單一操作中管理多個記錄。 您不僅可以匯入新專案，還可以更新、取代和刪除現有的產品集。</li><li>檢視從[[!UICONTROL Data Management Dashboard]](data-dashboard.md)傳輸到已連線Commerce服務之實體的資料同步處理狀態。</li><li>監視從[[!UICONTROL Data Export Feed Sync Status]](data-feed-sync-status.md)頁面將資料摘要匯出到Commerce SaaS服務的同步處理狀態。</li></ul> |
| [動作記錄檔](action-log.md) | 對於Adobe Commerce，動作記錄會擷取在您商店中工作的管理員使用者所進行的每項變更。 這可讓您追蹤對存放區進行的所有變更。 |
| 工具 | 僅[!BADGE PaaS]{type=Informative url="https://experienceleague.adobe.com/zh-hant/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案（Adobe管理的PaaS基礎結構）和內部部署專案的Adobe Commerce 。"}系統管理員擁有可用的工具集合： [支援工具](support.md)是用來識別您系統中的已知問題。 系統工具提供作業支援，以執行常式[索引](index-management.md)和[快取](cache-management.md)管理、[備份系統](backups.md)、管理[排程的作業](data-scheduled-import-export.md)，以及使用[開發人員工具](developer-tools.md)的組合。 |
| [整合](integrations.md) | 建立OAuth憑證的位置，並提供第三方整合的重新導向URL。 |
| [安全性](security.md) | 瞭解可用於保護您的存放區和資料的工具，以及在您偵測到危害時安全性行動計畫的准則。 |

{style="table-layout:auto"}

## 可用檔案

{{docs-links}}
