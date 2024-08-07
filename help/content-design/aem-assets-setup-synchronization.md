---
title: 啟用資產同步
description: 瞭解如何連結Adobe Commerce和Experience Manager Assets專案，以啟用這兩個系統之間的資產同步。
feature: CMS, Media
exl-id: cc3ae56b-f1c8-4c96-a284-bcd726ce2bab
source-git-commit: 508e9e1d23a4b6e70ada22e2a22c0dcd401393a9
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# 啟用資產同步

>[!BEGINSHADEBOX]

**必要條件**

- [設定AEM Experience Manager Assets以管理Commerce資產](#aem-assets-configure-aem)
- [安裝並設定Commerce的AEM Assets整合](#aem-assets-configure-commerce.md)以新增擴充功能，並產生使用擴充功能所需的認證和連線。

>[!ENDSHADEBOX]

在此啟用流程中，您可為您的AEM編寫環境提供計畫和環境ID，以註冊您的租使用者ID。 這些ID可識別您連線的AEM Assets專案，並提供憑證，以啟用Commerce與AEM Assets之間的通訊和工作流程。

識別AEM資產專案後，選取要用於在Adobe Commerce和AEM Assets之間同步資產的相符規則。

適用於Commerce的AEM Assets整合支援兩種相符規則，可在Adobe Commerce和AEM Assets之間同步資產。

- **依產品SKU比對** — 這是預設的比對規則，會根據產品的庫存單位(SKU)比對資產。 SKU是每個產品的唯一識別碼。 此規則會比對資產中繼資料中的SKU與Commerce產品SKU，以確保資產與正確的產品相關聯。

- **自訂比對** — 此比對規則適用於需要自訂比對邏輯的較複雜案例或特定業務需求。 若要使用此規則，您必須在Adobe Developer App Builder中實作自訂程式碼，以定義資產與產品的比對方式。 即將推出更多詳細資料……

對於初始上線，請使用預設`Match by product sku`規則。 如有需要，您稍後可以變更相符規則。

## 啟用整合

1. 取得您[AEM Assets編寫環境](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start)的專案和環境識別碼。

   1. 開啟AEM Sites主控台，然後選取&#x200B;**[!UICONTROL Assets]**。

   1. 從URL複製並儲存專案和環境ID：<br>`https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/`|

1. 從「Commerce管理員」開啟AEM Assets整合設定。

   1. 選取「**[!UICONTROL Store]**」>「組態」>「**[!UICONTROL CATALOG]**」>「**[!UICONTROL Catalog]**」。

   1. 展開&#x200B;**[!UICONTROL Experience Manager Assets integration]**。

      ![AEM Assets整合啟用整合](assets/aem-assets-integration-enable-config.png){width="600" zoomable="yes"}

1. 輸入&#x200B;**[!UICONTROL Program ID]**&#x200B;和&#x200B;**[!UICONTROL Environment ID]**&#x200B;以識別要連線的Experience Manager Assets專案。

1. 新增OAUTH認證以驗證Adobe Commerce與ARES服務之間的API要求，方法是選取&#x200B;**[[!UICONTROL Commerce integration]](aem-assets-configure-commerce.md#add-the-integration-to-the-commerce-environment)**，例如`Assets integration`。

1. 將&#x200B;**[!UICONTROL Enable integration]**&#x200B;設定為`Yes`，允許Commerce接受來自AEM Assets的傳入更新。

   啟用整合後，您可以設定資產比對規則。

   ![AEM Assets整合選取資產比對規則](assets/aem-assets-config-matching-rule.png){width="600" zoomable="yes"}

1. 定義資產同步的比對規則。

   1. 選取&#x200B;**[!UICONTROL Match by product SKU]**。

   1. 新增在&#x200B;**[!UICONTROL Match by product SKU attribute name]**&#x200B;欄位（例如`commerce:skus`）中為AEM Assets產品SKU定義的[Commerce中繼資料欄位名稱](aem-assets-configure-aem.md#configure-metadata)。

1. 套用組態並透過選取&#x200B;**[!UICONTROL Save Config]**&#x200B;來啟動同步處理作業。
