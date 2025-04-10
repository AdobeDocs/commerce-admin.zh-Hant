---
title: 安裝適用於Commerce的AEM Assets套件
description: 新增啟用Commerce的AEM Assets整合所需的資產中繼資料，以在Adobe Commerce和Experience Manager Assets專案之間同步資產。
feature: CMS, Media, Integration
exl-id: deb7c12c-5951-4491-a2bc-542e993f1f84
source-git-commit: d0599505bf99954c425ad3f2c7107744491f3446
workflow-type: tm+mt
source-wordcount: '643'
ht-degree: 0%

---

# 安裝AEM Assets套件

Adobe提供專案範本`commerce-assets`，以將Commerce名稱空間和中繼資料結構描述資源新增至Experience Manager Assets as a Cloud Service環境設定。 將此範本部署為Maven套件至您的環境。 然後，在AEM Assets製作環境中設定Commerce中繼資料，以完成設定。

範本將下列資源新增至AEM Assets製作環境。

- [自訂名稱空間](https://github.com/ankumalh/assets-commerce/blob/main/ui.config/jcr_root/apps/commerce/config/org.apache.sling.jcr.repoinit.RepositoryInitializer~commerce-namespaces.cfg.json)，`Commerce`可識別Commerce相關屬性。

- 具有標籤`Eligible for Commerce`的自訂中繼資料型別`commerce:isCommerce`可標籤與Adobe Commerce專案相關聯的Commerce資產。

- 自訂中繼資料型別`commerce:productmetadata`與對應的UI元件以新增&#x200B;*[!UICONTROL Product Data]*&#x200B;屬性。 產品資料包含中繼資料屬性，以將Commerce資產與產品SKU建立關聯，並指定資產的影像`role`和`position`屬性。

  ![自訂產品資料UI控制項](./assets/aem-commerce-sku-metadata-fields-from-template.png){width="600" zoomable="yes"}

- 中繼資料結構表單具有Commerce索引標籤，其中包含用於標籤Commerce資產的`Does it exist in Adobe Commerce?`和`Product Data`欄位。 此表單也提供在AEM Assets UI中顯示或隱藏`roles`和`order` （位置）欄位的選項。

  AEM Assets中繼資料結構表單的![Commerce索引標籤](./assets/assets-configure-metadata-schema-form-editor.png){width="600" zoomable="yes"}

- [範例已標籤並核准Commerce資產](https://github.com/ankumalh/assets-commerce/blob/main/ui.content/src/main/content/jcr_root/content/dam/wknd/en/activities/hiking/equipment_6.jpg/.content.xml) `equipment_6.jpg`，以支援初始資產同步化。 只有已核准的Commerce資產才能從AEM Assets同步到Adobe Commerce。

>[!NOTE]
>如需`commerce-assets` AEM專案範本的其他資訊，請參閱[讀我檔案](https://github.com/ankumalh/assets-commerce)。

您需要下列資源和許可權才能使用此AEM專案更新環境設定：

- [存取具有計畫和部署管理員角色的AEM Assets Cloud Manager計畫和環境](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/onboarding/journey/cloud-manager#access-sysadmin-bo)。

- [本機AEM開發環境](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/overview)，而且熟悉AEM本機開發程式。

- 瞭解[AEM專案結構](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure)以及如何使用Cloud Manager部署自訂內容套件。

## 安裝`commerce-assets`封裝

1. 如有需要，可從Cloud Manager建立AEM Assets專案的生產和中繼環境。

1. 視需要設定部署管道。

1. 從GitHub下載[Commerce-Assets AEM專案](https://github.com/ankumalh/assets-commerce)的範本程式碼。

1. 從您的[本機AEM開發環境](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/overview)，將自訂程式碼作為Maven套件安裝在您的AEM Assets環境設定中，或手動將程式碼複製到現有的專案設定中。

1. 提交變更，並將本機開發分支推送到Cloud Manager Git存放庫。

1. 從Cloud Manager [部署您的程式碼以更新AEM環境](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/using-cloud-manager/deploy-code#deploying-code-with-cloud-manager)。

## 設定中繼資料設定檔

在AEM Assets製作環境中，透過建立中繼資料設定檔，設定Commerce資產中繼資料的預設值。 然後，將新設定檔套用至AEM資產資料夾，以自動使用這些預設值。 此設定可減少手動步驟，以簡化資產處理。

1. 登入Adobe Experience Manager作者環境。

1. 在Adobe Experience Manager工作區中，按一下Adobe Experience Manager圖示以前往AEM Assets的作者內容管理工作區。

   ![AEM Assets製作](./assets/aem-assets-authoring.png){width="600" zoomable="yes"}

1. 選取槌子圖示，開啟「管理員」工具。

   ![AEM作者管理員管理中繼資料設定檔](./assets/aem-manage-metadata-profiles.png){width="600" zoomable="yes"}

1. 按一下&#x200B;**[!UICONTROL Metadata Profiles]**&#x200B;開啟設定檔設定頁面。

1. **[!UICONTROL Create]** Commerce整合的中繼資料設定檔。

   ![AEM作者管理員新增中繼資料設定檔](./assets/aem-create-metadata-profile.png){width="600" zoomable="yes"}

1. 新增Commerce中繼資料的索引標籤。

   1. 按一下左側的&#x200B;**[!UICONTROL Settings]**。

   1. 按一下索引標籤區段中的&#x200B;**[!UICONTROL +]**，然後指定&#x200B;**[!UICONTROL Tab Name]**、`Commerce`。

1. 將`Does it exist in Commerce?`欄位新增至表單，並將預設值設為`yes`。

   ![AEM作者管理員將中繼資料欄位新增至設定檔](./assets/aem-edit-metadata-profile-fields.png){width="600" zoomable="yes"}

1. 儲存更新。

1. 將`Commerce integration`中繼資料設定檔套用至儲存Commerce資產的資料夾。

   1. 從[!UICONTROL  Metadata Profiles]頁面，選取Commerce整合設定檔。

   1. 從動作功能表中選取&#x200B;**[!UICONTROL Apply Metadata Profiles to Folders]**。

   1. 選取包含Commerce資產的資料夾。

      建立Commerce資料夾（如果沒有）。

   1. 按一下&#x200B;**[!UICONTROL Apply]**。

>[!TIP]
>
>您可以更新中繼資料設定檔，將&#x200B;_[!UICONTROL Review Status]_欄位的預設值設為`Approved`，藉此在上傳至Commerce環境時自動同步AEM Assets資產。 `Review Status`欄位的屬性型別是`./jcr:content/metadata/dam:status`。

## 下一步

[安裝Adobe Commerce套件](aem-assets-configure-commerce.md)
