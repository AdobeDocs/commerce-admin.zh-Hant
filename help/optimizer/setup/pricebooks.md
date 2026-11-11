---
title: 價格手冊
description: 瞭解如何從[!DNL Adobe Commerce]中的目錄和定價資料對應價格簿。
role: Admin, Developer
recommendations: noCatalog
badgeSaas: label="僅限SaaS" type="Positive" url="https://experienceleague.adobe.com/zh-hant/docs/commerce/user-guides/product-solutions" tooltip="僅適用於以CCDM布建的Adobe Commerce as a Cloud Service執行個體（Adobe管理的SaaS基礎結構）。"
TQID: 'https://experienceleague.adobe.com/8gpl-l6oQebTnrt-00-n1FEdKnzqhTQi3hRz4lrGQoE'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
feature_v2:
  - id: 3033d2ab-c1d2-5b52-b865-72d9e5ad2c37
    internal-label: Currency
  - id: 58c984c2-e237-5c50-9718-500e40d1e82c
    internal-label: Merchandising
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
source-git-commit: 1041abe0e7d7c1212a717d5fd03180ce7fd32958
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 0%
---
# 價格簿

價格簿定義跨客戶層級和市場的目錄來源產品價格。 它們支援上下階價格簿的階層。

![價格簿階層](../assets/price-book-hier.png)

## 重要概念

| 詞語 | 說明 |
| ------ | ------------- |
| **價格簿** | 邏輯群組，定義型錄來源的價格；例如，特定區域或客戶階層，用來管理產品價格。 |
| **遞補價格手冊** | 階層中最上層的價格簿。 它沒有父代，而且是&#x200B;*僅*&#x200B;價格簿，定義其本身及其所有子系價格簿的貨幣。<br/><br/>如果在建立價格簿期間（透過API）未定義上階，則會建立新的備援價格簿。 |
| **父價格簿** | 較高層級的價格簿，若未明確設定子項價格，則子項價格簿可從中繼承價格。 |
| **階層深度** | 最多3個層級（備援 — >子項 — >子項）<br/><br/>在內嵌時未強制執行。 |
| **貨幣** | 僅針對遞補價格簿定義。 由所有下階價格簿繼承。<br/><br/>如果在建立遞補價格簿期間未指定貨幣（透過API），該貨幣會預設為USD。 |
| **產品價格** | 指定給特定價格簿中之產品(SKU)的特定價格。 |
| **折扣** | 折扣以產品價格定義。 未繼承。 |

## 價格簿實作

搭配可撰寫的目錄資料模型(CCDM)使用Adobe Commerce as a Cloud Service時，價格手冊會從目錄和定價資料進行對應。 它們不會手動建立。

從高層面來看，對應為：

- **存放區檢視→目錄來源** — 存放區檢視產品資料（包括當地語系化的屬性）對應到目錄來源。
- **網站→價格手冊或價格手冊** — 網站定價對應至適用的價格手冊。
- **客戶 — 群組訂價→價格簿專案** — 客戶 — 群組訂價對應到相關的價格專案。

維護Adobe Commerce組態中的來源型錄、網站及訂價組態，然後設定可用的價格簿，在相關型錄檢視中指定對應的價格簿。 如果未指定價格簿，則型錄檢視會使用預設價格簿。

目錄檢視會使用可用的價格簿設定及其目錄資料和原則來決定銷售體驗，包括產品傳回的價格。

>[!NOTE]
>
>對於Commerce B2B，系統會根據共用型錄組態，為每個型錄檢視建立並指派單一價格簿。 您不需要針對這些檢視設定價格簿可用性。

## 結帳定價

價格手冊支援銷售和店面目錄體驗。 Commerce Core會繼續處理購物車和結帳。 僅適用於CCDM的價格不會自動成為結帳所使用的價格。

讓價格與Commerce核心設定一致，並測試顯示的價格、加入購物車、促銷和結帳，作為實作驗證的一部分。

## 檢視價格簿

目錄資料同步完成後，請在&#x200B;**[!UICONTROL Catalog views]**&#x200B;工作區中檢視可用的價格簿及其ID。

1. 移至&#x200B;_存放區設定_，然後按一下&#x200B;**[!UICONTROL Catalog views]**。

1. 按一下&#x200B;**[!UICONTROL Create catalog view]**。

1. 檢閱目錄檢視組態之&#x200B;**[!UICONTROL Price Books]**&#x200B;區段中的可用價格簿。

   ![價格簿名稱與ID](../assets/price-book-name-ids.png)

## 設定價格簿可用性

在Commerce管理員的「目錄檢視」工作區中設定可用的價格簿，將對應的價格簿與目錄檢視建立關聯。

>[!NOTE]
>
>私人目錄檢視（已啟用[!UICONTROL Catalog Protection]的檢視）只能參考一個價格簿。

1. 從&#x200B;**[!UICONTROL Catalog views]**&#x200B;工作區中，選取您要設定的目錄檢視。

1. 在&#x200B;**[!UICONTROL Price Books]**&#x200B;區段中，選取目錄檢視所支援之存放區可用的價格簿。
