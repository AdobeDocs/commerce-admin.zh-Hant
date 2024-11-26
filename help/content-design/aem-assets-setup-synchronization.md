---
title: 啟用資產同步
description: 瞭解如何連結Adobe Commerce和Experience Manager Assets專案，以啟用這兩個系統之間的資產同步。
feature: CMS, Media
exl-id: cc3ae56b-f1c8-4c96-a284-bcd726ce2bab
source-git-commit: e069f0a99ed9289b22cafe06fe2f787912cbba23
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---

# 啟用資產同步

在啟用流程中，您會使用您AEM編寫環境的計畫和環境ID來註冊專案的租使用者ID。 這些ID可識別您連線的AEM Assets專案，並提供用於啟用Commerce與AEM Assets環境之間通訊的認證。

識別AEM資產專案後，選取相符規則以在Adobe Commerce和AEM Assets之間同步資產。

- **[!UICONTROL Match by product SKU]** — 符合資產中繼資料中的SKU與[Commerce產品SKU](https://experienceleague.adobe.com/en/docs/commerce-operations/operational-playbook/glossary#sku)的預設規則，以確保資產與正確的產品相關聯。

- **[!UICONTROL Custom match]** — 符合規則，適用於需要自訂比對邏輯的較複雜案例或特定業務需求。 實作自訂比對需要在Adobe Developer App Builder中開發自訂程式碼，以定義資產與產品的比對方式。 即將推出更多詳細資料……

對於初始入門，使用預設的&#x200B;*依產品SKU比對*&#x200B;規則。

## 先決條件

- [設定AEM Experience Manager Assets以管理Commerce資產](#aem-assets-configure-aem)
- [安裝並設定Commerce的AEM Assets整合](#aem-assets-configure-commerce.md)以新增擴充功能，並產生使用擴充功能所需的認證和連線。

## 設定連線

1. 取得[AEM Assets製作環境](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start)專案和環境識別碼。

   1. 開啟AEM Sites主控台並選取&#x200B;**[!UICONTROL Assets]**。

   1. 從URL複製並儲存專案和環境ID：<br>`https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/`|

1. 從「Commerce管理員」開啟AEM Assets整合設定。

   1. 移至「**[!UICONTROL Store]** >設定> **[!UICONTROL ADOBE SERVICES]** > **[!UICONTROL AEM Assets Integration]**」。

      ![AEM Assets整合啟用整合](assets/aem-assets-integration-enable-config.png){width="600" zoomable="yes"}

1. 進入AEM Assets環境&#x200B;**[!UICONTROL Program ID]**&#x200B;和&#x200B;**[!UICONTROL Environment ID]**。

1. 輸入**[!UICONTROL Asset Selector IMS Client ID]。

   [IMS ID](../getting-started/adobe-ims-config.md)可讓您將AEM Assets與頁面產生器整合。

1. 選取[[!UICONTROL Commerce integration]](aem-assets-configure-commerce.md#add-the-integration-to-the-commerce-environment)**以驗證Commerce與資產比對服務之間的要求。

1. 將&#x200B;**[!UICONTROL Integration enabled]**&#x200B;設定為`Yes`，允許Commerce接受來自AEM Assets的傳入更新。

   啟用整合後，請設定資產比對規則。

   ![AEM Assets整合選取資產比對規則](assets/aem-assets-config-matching-rule.png){width="600" zoomable="yes"}

1. 定義資產同步的比對規則。

   1. 選取&#x200B;**[!UICONTROL Match by product SKU]**。

   1. 新增在&#x200B;**[!UICONTROL Match by product SKU attribute name]**&#x200B;欄位（例如`commerce:skus`）中為AEM Assets產品SKU定義的[Commerce中繼資料欄位名稱](aem-assets-configure-aem.md#configure-metadata)。

   ![AEM Assets整合選取資產比對規則](assets/aem-assets-config-matching-rule.png){width="600" zoomable="yes"}

1. 選取&#x200B;**[!UICONTROL Save Config]**&#x200B;以套用更新並啟動資產同步處理
