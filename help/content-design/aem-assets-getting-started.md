---
title: 設定適用於Commerce的AEM Assets整合
description: 瞭解如何使用您的 [!DNL Commerce] 執行個體加入Experience Manager Assets，以存取無數用於商店的媒體資產。
feature: CMS, Media, Configuration
source-git-commit: c109edc9d9277baafd61da1df0f1917f07089353
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---

# 設定適用於Commerce的AEM Assets整合

設定AEM Assets整合需要管理存取權來自訂應用程式和環境設定。

- 對布建AEM Assets as a Cloud Service環境的Cloud Manager程式的管理存取權。

- 對Adobe Commerce環境的管理存取權，以及擷取或產生驗證所需的API金鑰的能力。

## 使用整合的需求

若要運用這項整合，企業必須符合下列需求：

- Adobe Commerce、AEM Assets和[AEM Dynamic Media](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/dynamic/administering-dynamic-media)的有效授權。

- Adobe Commerce 2.4.5+

   - PHP 8.1、8.2、8.3
   - Composer： 2.x

- Adobe Experience Manager已布建[Adobe Experience Manager Assets as a Cloud Service](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-cloud-service/content/assets/overview)

- 設定整合的Adobe Commerce使用者必須擁有布建AEM Assets專案的[IMS組織](https://experienceleague.adobe.com/en/docs/core-services/interface/administration/organizations#concept_EA8AEE5B02CF46ACBDAD6A8508646255)的存取權。

## 主要優點

- **不需額外付費** — 此整合免費提供給符合授權要求的商家。

- **官方Adobe解決方案** — 由Adobe開發、維護並完全支援，確保穩定性並與未來的平台增強功能保持一致。

- **Adobe Managed Support Model** — 協助和疑難排解由Adobe直接處理，讓您完全安心，並簡化問題解決方案。

## 後續步驟

啟用Commerce與Experience Manager Assets的整合需要三個步驟：

1. [設定您的AEM資產專案以管理Adobe Commerce資產](aem-assets-configure-aem.md)。

1. [安裝AEM資產整合擴充功能並設定Adobe Commerce](aem-assets-configure-aem.md)。

1. [啟用資產同步處理](aem-assets-setup-synchronization.md)。
