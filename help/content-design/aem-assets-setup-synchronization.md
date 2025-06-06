---
title: 設定整合
description: 瞭解如何連結Adobe Commerce和Experience Manager Assets專案，以啟用這兩個系統之間的資產同步。
feature: CMS, Media
exl-id: cc3ae56b-f1c8-4c96-a284-bcd726ce2bab
source-git-commit: f01ba239d885d96285186e35361a8d40f2f68e4e
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# 設定整合

將Commerce連線至AEM Assets執行個體，並選取資產同步的比對策略，以設定整合。

識別AEM Assets專案後，選取在Adobe Commerce和AEM Assets之間同步資產的相符規則。

- **[!UICONTROL Match by product SKU]** — 符合資產中繼資料中的SKU與[Commerce產品SKU](https://experienceleague.adobe.com/zh-hant/docs/commerce-operations/implementation-playbook/glossary#sku)的預設規則，以確保資產與正確的產品相關聯。

- **[!UICONTROL Custom match]** — 符合規則，適用於需要自訂比對邏輯的較複雜案例或特定業務需求。 實作自訂比對需要在Adobe Developer App Builder中開發自訂程式碼，以定義資產與產品的比對方式。 即將推出更多詳細資料……

對於初始設定，請使用預設的&#x200B;*依產品SKU比對*&#x200B;規則。

## 先決條件

- [安裝AEM Assets套件](aem-assets-configure-aem.md)

- [安裝Adobe Commerce套件](aem-assets-configure-commerce.md)以新增擴充功能，並產生使用擴充功能所需的認證和連線。

- 建立支援票證以請求啟用AEM Assets以進行Commerce整合。 在票證中，加入您要連線至Commerce之AEM Assets編寫環境的&#x200B;**[!UICONTROL Program ID]**、**[!UICONTROL Environment ID]**&#x200B;和&#x200B;**[!UICONTROL IMS Org ID]**。

- 提供&#x200B;**[!UICONTROL Asset Selector IMS Client ID]**。 請參閱&#x200B;*AEM Assets選取器*&#x200B;檔案中的[ImsAuthProps](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-cloud-service/content/assets/manage/asset-selector/asset-selector-integration/integrate-asset-selector-adobe-app)。

## 設定連線

1. 取得[AEM Assets製作環境](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-cloud-service/content/sites/authoring/quick-start)專案和環境識別碼。

   1. 開啟AEM Sites主控台並選取&#x200B;**[!UICONTROL Assets]**。

   1. 從URL複製並儲存專案和環境ID： <br>`https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/`
1. 從「Commerce管理員」開啟AEM Assets整合設定。

   1. 移至「**[!UICONTROL Store]** >設定> **[!UICONTROL ADOBE SERVICES]** > **[!UICONTROL AEM Assets Integration]**」。

      ![AEM Assets整合啟用整合](assets/aem-assets-integration-enable-config.png){width="600" zoomable="yes"}

1. 進入AEM Assets環境&#x200B;**[!UICONTROL Program ID]**&#x200B;和&#x200B;**[!UICONTROL Environment ID]**。

   從&#x200B;*[!UICONTROL Use system value]*&#x200B;中移除選取專案，以編輯設定值。

1. 輸入&#x200B;**[!UICONTROL Asset Selector IMS Client ID]**。

   [!UICONTROL Assets Selector]需要[Asset Selector IMS使用者端ID](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-cloud-service/content/assets/manage/asset-selector/asset-selector-integration/integrate-asset-selector-adobe-app#ims-auth-props)，此AEM Assets功能可讓使用者直接將視覺資產內嵌至Commerce產品頁面。

1. 選取[[!UICONTROL Commerce integration]](aem-assets-configure-commerce.md#add-the-integration-to-the-commerce-environment)以驗證Commerce與資產比對服務之間的要求。

1. 將&#x200B;**[!UICONTROL Integration enabled]**&#x200B;設為`Yes`以允許Commerce接受來自AEM Assets的傳入更新。

   啟用整合後，可使用其他設定選項來指定資產比對條件。

1. 定義資產同步的比對規則。

   1. 選取&#x200B;**[!UICONTROL Match by product SKU]**&#x200B;或&#x200B;**[!UICONTROL Custom match (Requires App Builder)]**。

   1. 新增在&#x200B;**[!UICONTROL Match by product SKU attribute name]**&#x200B;欄位（例如`commerce:skus`）中為AEM Assets產品SKU定義的[Commerce中繼資料欄位名稱](aem-assets-configure-aem.md#configure-metadata)。

1. 選取&#x200B;**[!UICONTROL Save Config]**&#x200B;以套用更新並啟動資產同步處理。

   設定更新會觸發初始同步流程，允許Commerce接受來自AEM Assets的傳入更新。 同步所需的時間取決於資產數量和特定配置。 整合利用自動化程式，將同步所需的時間減至最少。

### 設定自訂網域URL

如果商家在其AEM儀表板中設定[自訂網域名稱](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-cloud-service/content/implementing/using-cloud-manager/custom-domain-names/add-custom-domain-name){target=_blank}，則需要在Commerce中新增此&#x200B;**自訂網域URL**，以便AEM Assets整合能夠使用它。

1. 導覽至「**[!UICONTROL Store]** >設定> **[!UICONTROL ADOBE SERVICES]** > **[!UICONTROL AEM Assets Integration]**」。

   ![AEM Assets整合啟用整合](assets/aem-assets-view.png){width="600" zoomable="yes"}

1. 將&#x200B;**自訂網域URL**&#x200B;新增至&#x200B;**[!UICONTROL Asset Custom Domain]**&#x200B;欄位。

1. 按一下&#x200B;**[!UICONTROL Save Config]**&#x200B;以套用更新並啟動資產同步處理。

## 下一步

[搭配Commerce使用AEM Assets](aem-assets-manage.md)
