---
title: 設定適用於Commerce的AEM Assets整合
description: 瞭解如何設定並設定您的Experience Manager Assets環境，以管理您商店的Commerce資產。
feature: CMS, Media, Configuration
exl-id: 699f517e-1545-4c22-aa8d-9c8d60d352af
source-git-commit: 934473c5124002b3b0b1bee2da47afff468406dc
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 0%

---

# 設定適用於Commerce的AEM Assets整合

為Commerce設定Adobe Experience Manager Assets整合需要管理存取權來自訂應用程式和環境設定。

- 對布建AEM Assets as a Cloud Service環境的Cloud Manager程式的管理存取權。

- 對Adobe Commerce環境的管理存取權，以及擷取或產生驗證所需的API金鑰的能力。

## 使用整合的需求

若要運用這項整合，企業必須符合下列需求：

- Adobe Commerce、Adobe Experience Manager Assets和[AEM Dynamic Media](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/dynamic/administering-dynamic-media)的有效授權。

- Adobe Commerce 2.4.5+

   - PHP 8.1、8.2、8.3
   - Composer： 2.x

- Adobe Experience Manager已布建[Adobe Experience Manager Assets as a Cloud Service](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-cloud-service/content/assets/overview)

- 設定整合的Adobe Commerce使用者必須擁有布建AEM Assets專案的[IMS組織](https://experienceleague.adobe.com/en/docs/core-services/interface/administration/organizations#concept_EA8AEE5B02CF46ACBDAD6A8508646255)的存取權。

## 主要優點

- **不需額外付費** — 此整合免費提供給符合授權要求的商家。

- **官方Adobe解決方案** — 由Adobe開發、維護並完全支援，確保穩定性並與未來的平台增強功能保持一致。

- **Adobe Managed Support Model**—Adobe可處理協助和疑難排解，讓您完全安心，並簡化問題解決方案。

## 後續步驟

啟用Commerce與Experience Manager Assets的整合需要三個步驟：

1. [設定您的Adobe Experience Manager資產專案以管理Adobe Commerce資產](aem-assets-configure-aem.md)。

1. [安裝適用於Commerce擴充功能的Adobe Experience Manager Assets整合，並設定Adobe Commerce](aem-assets-configure-aem.md)。

1. [啟用資產同步處理](aem-assets-setup-synchronization.md)。
