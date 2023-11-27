---
title: 管理系統簡介
description: 瞭解存放區管理員可用來有效管理網站、資料、整合和管理員使用者的系統工具和功能。
exl-id: 52792a89-8f6f-4230-9a04-e193b3943410
source-git-commit: 46564240e7f76cf2a691c209b36d530763ba4f01
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# 管理系統簡介

商店管理員是安全的後台，商戶可在其中設定產品和促銷活動、管理訂單及執行其他管理任務。 所有基本設定任務和存放區管理操作都是從管理員執行。 還有一些功能可跨多個存放區功能提供支援，以供管理員為其組織管理。

## 變數和客戶通訊

變數是可一次建立並用於多個位置的資訊片段。 您的存放區包含許多預先定義的變數，可輕鬆用於個人化 [電子郵件](email-templates.md) 和 [電子報](../merchandising-promotions/newsletter-template.md) 範本和其他型別 [內容](../content-design/introduction.md#content). 您也可以建立自訂變數，以納入您需求的特定資訊。

- [預先定義的變數](variables-predefined.md)
- [自訂變數](variables-custom.md)

在啟動商店之前要完成的一項任務是，檢閱商店傳送的所有通訊所使用的電子郵件範本，以確保這些範本反映您的品牌。 這包括自訂電子郵件和 [電子報範本](../merchandising-promotions/newsletter-template.md)，並PDF發票和包裝單。 此外，也包含使用變數及個人化內容 [標籤標籤](markup-tags.md).

## 營運管理

管理員也支援系統管理員的各種工作，以便管理其組織內的管理員使用者並操作存放區。 這些工具包括：

- **管理員使用者帳戶和許可權**  — 管理管理員 [使用者帳戶](permissions-users-all.md)，以及相關的 [角色與許可權](permissions-user-roles.md) 這些許可權可控制訪客對管理員中網站和功能區域的存取權。
- **管理員工作階段和網站限制**  — 檢閱 [安全性](security.md) 最佳實務，並瞭解如何管理管理員工作階段和認證、實作驗證碼及管理網站限制。
- **系統工具**  — 執行常式 [索引](index-management.md) 和 [快取](cache-management.md) 管理作業， [備份](backups.md) 系統，管理 [排定的作業](data-scheduled-import-export.md)，並使用分類 [開發人員工具](developer-tools.md).
- **資料傳輸**  — 使用 [資料傳輸](data-transfer.md) 匯入及匯出資料以及管理產品、定價、客戶及稅率資料的工具。
- **整合**  — 建立OAuth憑證的位置和重新導向URL [協力廠商整合](integrations.md)，並識別可用的API資源。
- **動作記錄** - ![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)存取記錄([動作記錄檔](action-log.md))中，對使用您商店的管理員使用者所進行的變更進行變更。
- **支援工具** - ![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)支援工具([資料收集器](support.md#data-collector) 和 [系統報表](support.md#access-system-reports))專門用於識別您系統中的已知問題。 它們可在開發和最佳化過程中作為資源，並作為診斷工具，協助我們的支援團隊識別和解決問題。
