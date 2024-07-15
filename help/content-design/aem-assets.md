---
title: 適用於Commerce的Experience Manager Assets整合
description: 瞭解如何將Experience Manager Assets與您的 [!DNL Commerce] 執行個體整合，以存取您商店中使用的無數媒體資產。
feature: CMS, Media, Configuration, Integration
source-git-commit: 8588973f265c6bd3dfdd41e574f27f653cc9da0e
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 0%

---

# 適用於Commerce的Experience Manager Assets整合

{{$include /help/_includes/aem-assets-integration-beta-note.md}}

Commerce與Adobe Experience Manager (AEM) Assets的整合結合了AEM as a Digital Asset Management (DAM)系統與Adobe Commerce的強大功能，以強化電子商務體驗。 此整合採用AEM強大的資產管理功能，提供順暢、可擴充且有效率的方式，跨商業商店管理和交付資產。

**主要功能**

- **集中式資產管理**

   - **AEM Assets as a Single Source of Truth**-AEM Assets是所有數位資產的中央存放庫，確保所有電子商務平台都可存取品牌上核准的資產。

   - **大量資產管理** — 由於AEM強大的資產管理功能，組織可以高效地管理大量資產。 這可讓行銷人員和銷售人員有效率地為新產品線對應大型影像集。

- **個人化Commerce體驗** — 在AEM中使用GenAI服務，組織可以為個人化的電子商務體驗產生數百萬種產品變數。 行銷人員和銷售人員可以使用這些影像為產品推出和季節性行銷活動建立動態店面，從而增強參與度並提升轉換率。

- **自動化資產比對** — 整合包含規則引擎服務，可根據SKU或其他關鍵屬性，自動比對AEM中的資產與Adobe Commerce中的產品。 此服務可確保電子商務商店隨時提供最新產品資產和變數。 這樣還能減少管理資產所需的手動工作，騰出時間用於更具策略性的活動。

- **簡化程式**
   - **從Commerce管理員啟用並設定整合** — 管理員和開發人員可以使用熟悉的工具和程式，從Adobe Commerce安裝和設定整合。
   - **動態更新** — 使用資產管理系統中的最新變更，讓產品影像保持最新狀態。 這些自動更新可確保Commerce店面一律具有最新的產品資訊。
   - **有效的目錄管理** — 透過自動化資產清理和重新整理，簡化產品目錄的維護作業。

## 整合Commerce和Experience Manager Assets

>[!BEGINSHADEBOX]

**必要條件**

- 必須將Adobe Commerce設定為[Commerce管理員與Adobe ID](/help/getting-started/adobe-ims-config.md)的整合，並指派組織ID。
- Experience Manager Assets必須以產品形式指派給相同的組織ID。
- 設定整合的使用者必須在相同組織中擁有一個帳戶，該帳戶具有存取Adobe Commerce和Experience Manager Assets的管理許可權。

>[!ENDSHADEBOX]

透過完成下列工作來啟用Commerce與Experience Manager Assets的整合：

1. [設定您的Experience Manager Assets專案以管理Commerce資產](aem-assets-configure-aem.md)

1. [安裝Experience Manager Assets整合擴充功能並設定Adobe Commerce](aem-assets-configure-commerce.md)

1. [設定同步化服務](aem-assets-setup-synchronization.md)
