---
title: AI產品探索發行說明
description: 如需目錄和PDP擴充功能、修正、升級指引、支援的Commerce版本和已知問題，請檢閱AI產品探索發行說明。
feature: Release Notes
source-git-commit: ed404fb8515374a33116ccc811c96548fb14dd35
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 0%
---
# AI產品探索發行說明

這些發行說明涵蓋目錄擴充和PDP擴充的更新，包括新功能、修正、升級要求和已知問題。 每個版本專案都會識別受影響的擴充功能或工作流程。

![新](../assets/new.svg)新功能
![已修正問題](../assets/fix.svg)修正和改良
![已知問題](../assets/bug.svg)已知問題

## 發行版本2.1.3 {#release-2-1-3}

*2026年11月30日*

在PHP 8.3到8.5上[!BADGE 支援]{type=Informative tooltip="支援"} [!DNL Adobe Commerce] 2.4.9、2.4.8和2.4.7。[!DNL Adobe Commerce as a Cloud Service]

2.1.3版將產品詳細資料頁面擴充與目錄擴充結合為名為&#x200B;**AI產品探索**&#x200B;的新管理功能表專案。 此外，支援延伸至[!DNL Adobe Commerce as a Cloud Service]。

## 發行版本2.1.2 {#release-2-1-2}

*2026年10月22日*

在PHP 8.3到8.5上[!BADGE 支援]{type=Informative tooltip="支援"} [!DNL Adobe Commerce] 2.4.9、2.4.8和2.4.7。

2.1.2版將目錄擴充設為獨立擴充功能。 它現在包含先前由個別[!DNL Adobe Brand Visibility]擴充功能(`magento/llm-optimizer`)提供的所有內容：將已核准的建議套用至目錄、復原建議，以及保護您自己的編輯不會被覆寫。

### 從舊版升級 {#upgrade-from-earlier-versions}

>[!IMPORTANT]
>
>版本2.1.2無法與[!DNL Adobe Brand Visibility]擴充功能一起安裝。 如果已安裝，請在升級時將其移除。

1. 移除[!DNL Adobe Brand Visibility]擴充功能（如果已安裝）：

   ```bash
   composer remove magento/llm-optimizer
   ```

   如果擴充功能是以複製或連結`Magento/LlmoCatalog`到`app/code`的方式安裝，請刪除該目錄。 不僅要停用模組：停用的模組若仍在磁碟中，可能會導致`setup:upgrade`卸除儲存擴充產品原始值的表格。

1. 更新目錄擴充並套用變更：

   ```bash
   composer require magento/module-catalog-enrichment:^2.1
   bin/magento setup:upgrade
   bin/magento cache:flush
   ```

   升級後排清快取。 升級會將現有的存取許可權移到新許可權資源，而且這些許可權要等到快取清除後才會生效。

### 需求

![New](../assets/new.svg) **PHP 8.3和[!DNL Adobe Commerce] 2.4.7或更新版本**—PHP 8.1生命週期結束，PHP 8.2於2026年12月31日到期，因此兩者皆不受支援。不支援[!DNL Adobe Commerce] 2.4.6和較舊版本。

### 新功能

![新增](../assets/new.svg) **[!UICONTROL AI Product Discovery]功能表** — 目錄擴充頁面在管理員側邊欄中現在有自己的區段。 前往&#x200B;**[!UICONTROL AI Product Discovery]** > **[!UICONTROL Catalog Enrichment]**。 之前，頁面位於&#x200B;**[!UICONTROL Catalog]**&#x200B;下方。

![新](../assets/new.svg) [!BADGE Beta]{type=Informative tooltip="尚未正式提供"} **[!UICONTROL Product Details Page Enrichment (Beta)]** — 在&#x200B;**[!UICONTROL AI Product Discovery]**&#x200B;下有一個新頁面，可檢閱產品詳細資料頁面的擴充建議。 產品詳細資料頁面擴充功能處於測試版，尚未正式發佈。

![新增](../assets/new.svg) **套用並復原核准的建議** — 此擴充功能會將核准的名稱和描述更新寫入目錄。 Commerce會記錄每個擴充屬性在首次變更時的原始值，因此復原一律會還原擴充前的值，即使相同屬性套用數個建議後亦然。

![新增](../assets/new.svg) **已接受您的編輯** — 當您在「管理員產品」表單中變更擴充名稱或說明時、**[!UICONTROL Update Attributes]**&#x200B;或透過匯入，您的值會保留，相關建議會標籤為&#x200B;*已過時*。 在預設範圍中所做的變更只會影響繼承值的存放區檢視。

![新的](../assets/new.svg) **建議的唯讀目錄存取權**—[!DNL Commerce Catalog Agent]可以讀取產品、類別、屬性集和產品型別資料，以選取要分析的產品。 讀取只會傳回標籤為&#x200B;**[!UICONTROL Used in Product Listing]**&#x200B;的屬性，加上可擴充的屬性。 它無法變更目錄資料。

### 修正和改良

![已修正問題](../assets/fix.svg) **重試套用報告成功** — 如果套用要求在完成之後重試，重試現在會將變更報告為已套用，而不是報告無變更。 沒有內容會寫兩次。

![已修正問題](../assets/fix.svg) **只有已核准的服務才能變更目錄** — 套用和復原僅接受來自[!DNL Commerce Catalog Agent]的請求。 之前，使用者接受任何有效的Adobe IMS權杖。 同樣的檢查現在也適用於SOAP要求。

![已修正問題](../assets/fix.svg) **更清楚的錯誤**—Adobe IMS中斷現在會傳回`401`而非`500`，因此不會針對目錄重試請求，而且會拒絕無法辨識的Adobe IMS環境，而非將其視為中繼環境。

![已修正問題](../assets/fix.svg) **Adobe IMS環境** — 目錄擴充現在預設會登入生產Adobe IMS環境，包括連線到非生產[!DNL Commerce Services]資料空間的執行個體。 以前，這些執行個體會傳送至測試環境。

![已修正問題](../assets/fix.svg) **在[!DNL Adobe Brand Visibility]網域變更後登入** — 目錄擴充頁面現在會從`abv.adobe.com`載入，這會修正先前網域開始重新導向後的登入回圈。

### 已知問題

![已知問題](../assets/bug.svg) **具有完整[!UICONTROL Catalog]存取權的角色** — 在此版本之前儲存且已授與所有&#x200B;**[!UICONTROL Catalog]**&#x200B;的使用者角色，可保持對&#x200B;**[!UICONTROL Catalog Enrichment Service API]**&#x200B;資源的存取權。 在&#x200B;**[!UICONTROL System]** > **[!UICONTROL Permissions]** > **[!UICONTROL User Roles]**&#x200B;中檢閱這類角色，並清除不需要它的資源。

## 發行版本1.0.2 {#release-1-0-2}

目錄擴充管理頁面的初始版本。 需要[!DNL Adobe Brand Visibility]副檔名才能將建議套用至目錄。
