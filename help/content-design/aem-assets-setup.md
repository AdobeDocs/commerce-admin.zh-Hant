---
title: 設定AEM Assets整合
description: 瞭解設定Adobe Commerce與AEM Assetsas a Cloud Service之間整合的需求和步驟。
feature: CMS, Media, Configuration, Integration
source-git-commit: df21ea9a797a4f11d0104cf34134ced3bbabbdf4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# 設定AEM Assets整合

設定AEM Assets環境，並針對Commerce安裝和設定AEM Assets整合，以啟用進階資產管理功能。

當整合作用中時，管理員可以使用Experience Manager Assets as a Cloud Service作為資產建立與管理的單一信任來源，並作為集中數位資產管理工具(DAM)，為Commerce專案建立、管理、組織和分配資產。

## 需求

- Adobe Commerce 2.4.5+
   - PHP 8.1、8.2、8.3
   - Composer： 2.x
- Adobe Experience Manager已布建[Adobe Experience Manager Assetsas a Cloud Service](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-cloud-service/content/assets/overview)
- 設定整合的Adobe Commerce使用者必須擁有布建AEM Assets專案的[IMS組織](https://experienceleague.adobe.com/en/docs/core-services/interface/administration/organizations#concept_EA8AEE5B02CF46ACBDAD6A8508646255)的存取權。

## 設定整合

>[!BEGINSHADEBOX]

**必要條件**

設定AEM Assets整合需要管理存取權來自訂應用程式和環境設定。

- 對布建AEM Assetsas a Cloud Service環境的Cloud Manager程式的管理存取權。
- 對Adobe Commerce環境的管理存取權，以及擷取或產生驗證所需的API金鑰的能力。

>[!ENDSHADEBOX]

啟用Commerce與Experience Manager Assets的整合需要三個步驟：

1. [設定您的Experience Manager Assets專案以管理Commerce資產](aem-assets-configure-aem.md)。

1. [安裝Experience Manager Assets Integration擴充功能並設定Adobe Commerce](aem-assets-configure-aem.md)。

1. [啟用資產同步處理](aem-assets-setup-synchronization.md)。
