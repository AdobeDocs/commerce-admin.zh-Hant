---
title: 目錄管理指南
description: 有關 Adobe Commerce 和 Magento Open Source 管理員和電子商務商品企劃人員適用的產品目錄功能的綜合資訊。
seo-title: Adobe Commerce Catalog Management Guide
seo-description: Describes how to use the product catalog features for Adobe Commerce and Magento Open Source.
exl-id: 894b7cc3-8dc5-43aa-ab9c-ebc6480c7b2f
TQID: https://experienceleague.adobe.com/HJiD3cpDixdbHlBXmMhkHpEd40eyjEfNBu3MzEDhBL0
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
subfeature_v2:
  - id: e91a50b1-0b31-436e-9033-00e4776e94cb
    internal-label: Categories
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: c425649d00a0a57f84ce4042d33f6d0c5eabe99c
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 3%
---
# Adobe Commerce目錄管理指南

本指南適用於使用Adobe Commerce和Magento Open Source Admin的產品銷售商和詳細目錄管理員。 它提供有關產品目錄功能的詳細資訊，包括建立目錄的導覽結構。 它假定您對核心[!DNL Commerce]設定和功能有基本的瞭解。

本指南涵蓋：

| 主旨 | 說明 |
| ------- | ----------- |
| [簡介](introduction.md) | 使用目錄管理功能來反映您希望客戶在您的商店尋找產品的方式的總覽。 |
| [目錄功能表](catalog-menu.md) | 使用[!UICONTROL Catalog]功能表存取多項功能，以管理商店的目錄、類別和產品。 |
| [目錄和產品URL](catalog-urls.md) | 檢閱基本URL型別，以及如何設計URL以最大化搜尋引擎最佳化。 |
| [目錄導覽](navigation.md) | 使用導覽工具來定義您的購物者在整個商店中從一個頁面移動到另一個頁面的方式。 |
| [目錄搜尋](search.md) | 檢閱客戶可用於在店面尋找產品的工具，並根據您的產品目錄設定搜尋體驗。 |
| [類別](categories.md) | 以最佳化店面購物者體驗的方式，建立目錄的基本類別結構。 |
| [產品](products-list.md) | 從簡單到複雜，使用多個選項、色票、可自訂套件組合來建立產品。 建立可下載的產品，以及適用於服務和其他無形專案的虛擬產品。 |
| [共用目錄](../b2b/enable-basic-features.md) | 共用目錄可讓商家為不同的公司提供策劃的產品分類和自訂定價。 需要Adobe Commerce B2B授權和設定，包括公司帳戶和共用目錄功能。 |
| [目錄擴充](catalog-enrichment.md) | 檢閱並將AI建議的改進套用至產品名稱和說明，以便您的目錄在LLM和AI協助的探索中準確呈現。 |
| [產品屬性](product-attributes.md) | 使用產品選項的輸入控制項建立屬性，並在產品頁面上提供其他資訊。 |
| [目錄檢視](../optimizer/setup/catalog-view.md) [!BADGE 僅限SaaS]{type=Positive url="https://experienceleague.adobe.com/zh-hant/docs/commerce/user-guides/product-solutions" tooltip="僅適用於Adobe Commerce as a Cloud Service和Adobe Commerce Optimizer專案（Adobe管理的SaaS基礎結構）。"} | 針對使用銷售服務與可撰寫目錄資料模型(CCDM)的Commerce部署，結合每個品牌、地區、業務單位或頻道的目錄來源、目錄層、原則和價格簿，以定義使用者端可擷取的產品和定價。 選擇性地限制目錄檢視，使其成為私人檢視。 |
| [原則](../optimizer/setup/policies.md)僅[!BADGE SaaS]{type=Positive url="https://experienceleague.adobe.com/zh-hant/docs/commerce/user-guides/product-solutions" tooltip="僅適用於Adobe Commerce as a Cloud Service和Adobe Commerce Optimizer專案（Adobe管理的SaaS基礎結構）。"} | 針對使用CCDM的Commerce部署，定義資料存取篩選器，以控制每個目錄檢視傳送哪些產品，因此正確的內容會傳送至正確的目的地。 |

{style="table-layout:auto"}

>[!TIP]
>
>Adobe Commerce B2B可讓您使用不同公司的自訂價格，維護閘道共用目錄。 除了標準、主要產品目錄之外，它還可以讓客戶存取具有不同定價結構的兩種共用目錄。 如需共用目錄功能的詳細資訊，請參閱[Adobe Commerce B2B使用手冊](../b2b/catalog-shared.md)。

## 可用檔案

{{docs-links}}
