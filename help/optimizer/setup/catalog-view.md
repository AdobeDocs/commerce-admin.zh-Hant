---
title: 目錄檢視
description: 瞭解什麼是目錄檢視，以及如何建立檢視，以依業務結構、原則和定價組織您的產品目錄。
role: Admin, Developer
recommendations: noCatalog
badgeSaas: label="僅限SaaS" type="Positive" url="https://experienceleague.adobe.com/zh-hant/docs/commerce/user-guides/product-solutions" tooltip="僅適用於以CCDM布建的Adobe Commerce as a Cloud Service執行個體（Adobe管理的SaaS基礎結構）。"
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 8fbcfcdeb13c452a45e872d939e129703ac5abab
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 0%
---

# 目錄檢視

目錄檢視會定義店面可擷取的產品和定價。 在布建了可撰寫目錄資料模型(CCDM)的Adobe Commerce as a Cloud Service例項中，目錄檢視會使用支援Adobe Commerce Optimizer的相同目錄基礎。

目錄檢視會結合目錄來源、原則和價格簿，以定義店面的目錄內容。 原則會決定可用的產品分類。 銷售規則可控制該分類中產品的促銷和排名方式，並可套用至所有目錄檢視或針對特定檢視量身打造。 請參閱[建立銷售規則](../merchandising/rules/add.md)。

Commerce Foundation依然是產品和價格的真實來源。 產品與價格資料會透過原生Adobe Commerce as a Cloud Service整合，以單一方式同步至CCDM，無需個別安裝聯結器或App Builder應用程式。 網站、商店和商店檢視設定保留在Commerce Foundation中，該基金會也管理購物車、結帳、促銷、客戶、訂單和付款。

>[!NOTE]
>
>針對已布建CCDM的執行個體，請使用Adobe Unified Experience中的[Commerce管理員](../../getting-started/admin-unified-experience.md)來設定目錄檢視與原則，並將同步化的價格手冊與目錄檢視建立關聯。 使用目錄服務搭配「即時搜尋」和「產品建議」的執行個體無法存取這些目錄管理畫面。

## 目錄檢視的運作方式

目錄檢視將店面內容的目錄資料和設定集合在一起。 它可用來代表業務單位、品牌、地區或其他店面體驗。

- **[目錄來源](catalog-sources.md)**&#x200B;提供目錄體驗的產品資料。
- **[原則](policies.md)**&#x200B;會篩選目錄檢視的產品資料。
- **[價格簿](pricebooks.md)**&#x200B;提供與目錄檢視相關聯的定價資料。

目錄檢視不會取代Adobe Commerce as a Cloud Service中的網站、商店和商店檢視結構。 Commerce Foundation會繼續管理該結構和異動作業。

目錄資料會以單向方式從Commerce Foundation同步至CCDM。 CCDM支援店面目錄體驗和產品探索。 Commerce Foundation會繼續處理購物車、結帳、促銷活動、客戶和訂單。

## 開始之前

設定目錄檢視之前：

- [確認Adobe Commerce as a Cloud Service執行個體使用CCDM](../overview.md)。
- 確認已填入店面所需的目錄資料且[已同步](data-sync.md)。
- 識別店面內容所需的[目錄來源](catalog-sources.md)、[原則](policies.md)和[價格手冊](pricebooks.md)。
- 決定是否需要手動建立B2C目錄檢視，或檢閱由原生同步化產生的B2B目錄檢視。

>[!NOTE]
>
>針對B2B實作，原生同步會從Commerce Foundation的B2B設定產生目錄檢視、原則和價格手冊。 請勿手動建立這些自動產生結構的重複專案。

## 建立B2C實作的目錄檢視

當B2C實作需要手動設定目錄檢視時，請使用此工作流程。

1. 登入Unified Experience中的[Commerce管理員](../../getting-started/admin-unified-experience.md)，然後選取以CCDM布建的Adobe Commerce as a Cloud Service執行個體。
1. 在左側導覽中，前往&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Catalog Views]**。
1. 選取&#x200B;**[!UICONTROL Create catalog view]**。
1. 輸入目錄檢視的名稱。
1. 選取店面內容的[目錄來源](catalog-sources.md)。
1. 將相關的[原則](policies.md)與目錄檢視產生關聯。
1. 透過[設定價格簿可用性](pricebooks.md)，將相關價格簿與目錄檢視建立關聯。
1. 建立目錄檢視。

## B2B目錄檢視

針對B2B實作，原生同步會從Commerce Foundation的B2B設定產生目錄檢視、原則和價格手冊。 在Commerce Foundation中管理基礎B2B目錄和公司關係，而非在CCDM中手動建立重複結構。

如需設定指示，請參閱[建立共用目錄](../../b2b/catalog-shared-create.md)和[將公司指派給共用目錄](../../b2b/catalog-shared-assign-companies.md)。

設定B2B關係之後：

1. 確認[同步處理](data-sync.md)已完成。
2. 檢閱在[Unified Experience中的Commerce Admin &#x200B;](../../getting-started/admin-unified-experience.md)中產生的目錄檢視、[原則](policies.md)和[價格手冊](pricebooks.md)。
3. 確認店面會顯示公司的預期產品分類與定價。
4. 測試加入購物車、購物車和結帳，以確認產品可用性和交易定價符合預期的B2B設定。

## 價格手冊與結帳

價格簿會透過目錄檢視提供可用的定價資料。 在Adobe Commerce as a Cloud Service中，Commerce Foundation依然是價格的真實來源，定價資料會透過原生整合約步至CCDM。 設定目錄檢視時，請使用適用的同步化價格簿，而非在CCDM中獨立編寫價格。

購物車和結帳使用Commerce Foundation定價。 確認顯示的店面價格符合適用的購物車和結帳價格。

## 檢閱及驗證目錄檢視

設定目錄檢視後，請驗證完整的店面體驗：

- 確認預期的目錄資料為[已同步處理](data-sync.md)。
- 確認目錄檢視與預期的[原則](policies.md)和[價格手冊](pricebooks.md)相關聯。
- 檢查店面是否傳回預期的產品分類。
- 根據對應的Commerce Foundation定價來驗證顯示的定價。
- 測試加入購物車、購物車和結帳。

對於B2B實作，也請確認同步產生的目錄結構符合預期的公司和目錄設定。

## 疑難排解

### 店面中缺少產品

- [確認執行個體使用CCDM](../overview.md)。
- 確認目錄資料具有[已同步處理](data-sync.md)。
- 檢查店面是否使用預期的目錄內容。
- 檢閱與目錄檢視相關聯的[原則](policies.md)。

### 顯示的價格是意外的

- 確認預期的[價格簿](pricebooks.md)與目錄檢視相關聯。
- 檢查價格資料是否為[已同步](data-sync.md)且與Commerce Foundation一致。

  如需網站和客戶群組定價對應，請參閱[價格手冊](pricebooks.md)。

- 在購物車和結帳中再次驗證價格。

### CCDM目錄畫面在Commerce管理中不可見

[確認選取的執行個體使用CCDM](../overview.md)，以及您正在存取Unified Experience中的[Commerce管理員](../../getting-started/admin-unified-experience.md)。 執行目錄服務v1的執行個體沒有CCDM管理畫面。

## 相關內容

- [Adobe Commerce as a Cloud Service快速入門](https://experienceleague.adobe.com/zh-hant/docs/commerce/cloud-service/getting-started)
- [Adobe Commerce B2B共用目錄概觀](../../b2b/catalog-shared.md)
- [Adobe Commerce as a Cloud Service發行說明](https://experienceleague.adobe.com/zh-hant/docs/commerce/cloud-service/release-notes)
- [目錄同步](data-sync.md)
