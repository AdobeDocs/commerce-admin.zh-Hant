---
title: 設定適用於Commerce的AEM Assets整合
description: 瞭解如何設定並設定您的Experience Manager Assets環境，以管理您商店的Commerce資產。
feature: CMS, Media, Configuration
exl-id: 699f517e-1545-4c22-aa8d-9c8d60d352af
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hant/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案（Adobe管理的PaaS基礎結構）和內部部署專案的Adobe Commerce 。"
TQID: https://experienceleague.adobe.com/loyCmoFINQvC-13BGzAUKmcF7gY6T2e6mV-lK-SnVxo
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 42029ed6d13cd4203c4a5d8300297315aac1abf5
workflow-type: tm+mt
source-wordcount: 298
ht-degree: 3%

---

# 設定適用於Commerce的AEM Assets整合

為Commerce設定Adobe Experience Manager Assets整合需要管理存取權來自訂應用程式和環境設定。

- 對布建AEM Assets as a Cloud Service環境的Cloud Manager程式的管理存取權。

- 對Adobe Commerce環境的管理存取權，以及擷取或產生驗證所需的API金鑰的能力。

## 使用整合的需求

若要運用這項整合，企業必須符合下列需求：

- Adobe Commerce、Adobe Experience Manager Assets和[AEM Dynamic Media](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-65/content/assets/dynamic/administering-dynamic-media)的有效授權。

- Adobe Commerce 2.4.5+

- Adobe Experience Manager已布建[Adobe Experience Manager Assets as a Cloud Service](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-cloud-service/content/assets/overview)

- 設定整合的Adobe Commerce使用者必須擁有布建AEM Assets專案的[IMS組織](https://experienceleague.adobe.com/zh-hant/docs/core-services/interface/administration/organizations#concept_EA8AEE5B02CF46ACBDAD6A8508646255)的存取權。

## 主要優點

- **不需額外付費** — 此整合免費提供給符合授權要求的商家。

- **官方Adobe解決方案** — 由Adobe開發、維護並完全支援，確保穩定性並與未來的平台增強功能保持一致。

- **Adobe Managed Support Model**—Adobe可處理協助和疑難排解，讓您完全安心，並簡化問題解決方案。

## 後續步驟

啟用Commerce與Experience Manager Assets的整合需要三個步驟：

1. [安裝AEM Assets套件](aem-assets-configure-aem.md)。
1. [安裝Adobe Commerce套件](aem-assets-configure-aem.md)。
1. [設定整合資產](aem-assets-setup-synchronization.md)。
