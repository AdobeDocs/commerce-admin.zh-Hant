---
title: '[!DNL Adobe Commerce Marketplace]'
description: 瞭解 [!DNL Commerce Marketplace]，此工具為商家提供精選的解決方案，並為合格的開發人員提供工具、平台和絕佳位置，以建立欣欣向榮的業務。
exl-id: e04e48f2-3b1d-45bf-b0f6-3a1ed43e78c5
feature: Extensions
source-git-commit: 7b5c331625e4c4dab0e41156722c4a8deb4aa4c0
workflow-type: tm+mt
source-wordcount: '1293'
ht-degree: 0%

---

# Adobe Commerce Marketplace

[Adobe Commerce Marketplace][1]是應用程式商店，為商戶提供精選的解決方案，並為合格的開發人員提供工具、平台和最佳位置，以建立欣欣向榮的業務。 [!DNL Commerce Marketplace]提供多種免費的擴充功能以及其他可供銷售的擴充功能。 可以用信用卡或[PayPal][2]支付購買費用。

[!DNL Commerce Marketplace]上可用的所有擴充功能均已通過廣泛檢閱。 [擴充功能品質計畫][3] (EQP)結合了[!DNL Commerce]專業知識、開發指引和驗證工具，以確保Commerce Marketplace上的所有擴充功能都符合編碼標準和最佳實務。 稽核程式包括自動檢查和手動QA稽核。 在此過程中，會檢查並測試每個擴充功能的結構和程式碼，以找出病毒/惡意程式碼感染的證據，以及是否有任何剽竊的跡象。 檢閱包括由[!DNL Commerce]工程師進行的深入技術檢查和健全性檢查，重點是檔案、編碼結構、效能、擴充性、安全性以及與[!DNL Commerce]核心的相容性。

雖然您可以從其他來源購買擴充功能，但只有在[!DNL Commerce Marketplace]上可用的擴充功能，才能透過擴充功能品質方案中的廣泛技術和行銷稽核進行驗證。

## 應用程式資源

開發人員傳統上會使用PHP建立程式內擴充功能，以新增功能、服務和整合至Adobe Commerce。 與擴充功能相比，透過建立具有程式外擴充功能的應用程式，您可以避免相容性問題。

下列資源為新的採用者提供熟悉應用程式的起點：

### Commerce資源

- [設定Adobe Commerce的I/O事件](https://developer.adobe.com/commerce/extensibility/events/)
- [為Adobe Commerce設定事件](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/)
- [設定Admin UI SDK](https://developer.adobe.com/commerce/extensibility/admin-ui-sdk/)
- [將擴充功能轉換為應用程式](https://developer.adobe.com/commerce/extensibility/app-development/#how-do-i-port-an-extension-into-an-app)

### App Builder資源

- [Commerce App Builder概觀](https://developer.adobe.com/commerce/extensibility/app-development/)
- [為Adobe Developer App Builder設定API網格](https://developer.adobe.com/graphql-mesh-gateway/gateway/getting-started/)
- [正在部署App Builder應用程式](https://developer.adobe.com/app-builder/docs/guides/deployment/)
- 適用於App Builder應用程式的[CI/CD](https://developer.adobe.com/app-builder/docs/guides/deployment/ci_cd_for_firefly_apps/)
- App Builder/Developer Console快速入門
   - [開始使用App Builder](https://developer.adobe.com/app-builder/docs/getting_started/)
   - [瞭解專案和工作環境](https://developer.adobe.com/app-builder/docs/resources/videos/exploring/projects-and-workspaces/)

## [!DNL Marketplace]認證

在您可以安裝從[!DNL Commerce Marketplace]購買的擴充功能之前，請登入您的[!DNL Commerce]帳戶並確認您擁有有效的存取金鑰。 您可以從[[!DNL Marketplace]][1]或[Magento.com][6]的標題登入您的[!DNL Commerce]帳戶。

您的存取金鑰是一組公開和私密金鑰，用來將您的[!DNL Commerce]安裝與[!DNL Commerce]帳戶同步並驗證您的認證。 帳戶同步之後，每次從Commerce Marketplace安裝擴充功能或模組或升級[!DNL Commerce]安裝時，都必須輸入私密金鑰。

您可以根據不同目的建立多個存取金鑰，並視需要啟用或停用它們。 不過，您必須使用安裝[!DNL Commerce]軟體所使用的相同存取金鑰。 例如，您無法使用Magento Open Source存取金鑰更新或升級Adobe Commerce，反之亦然。 您也無法使用屬於其他使用者或來自[共用帳戶](commerce-account-share.md)的存取金鑰。

### 建立存取金鑰

1. 登入您的[!DNL Commerce]帳戶。

1. 在&#x200B;_[!UICONTROL My Account]_&#x200B;頁面上，選擇&#x200B;**[!UICONTROL Marketplace]**&#x200B;標籤。

1. 在名稱旁邊的右上角，按一下向下箭頭，然後選擇&#x200B;**[!UICONTROL My Profile]**。

   ![您的[!DNL Marketplace]設定檔](./assets/marketplace-profile.png){width="600"}

1. 在「_[!UICONTROL My Products]_」下的「_[!UICONTROL Marketplace]_」標籤上，按一下「**[!UICONTROL Access Keys]**」，然後執行下列任一動作：

   - 檢視您是否擁有一組用於購買Marketplace的存取金鑰。 您可以針對不同用途建立多組存取金鑰。

   ![存取金鑰](./assets/access-keys.png){width="600"}

   - 按一下&#x200B;**[!UICONTROL Create a New Access Key]**。 輸入新金鑰組的名稱並按一下&#x200B;**[!UICONTROL OK]**。 有效字元包括大小寫字元和連字型大小而非空格。

1. 完成時，按一下&#x200B;**[!UICONTROL OK]**。

   您的新存取金鑰已啟用，並會顯示在清單中。

   請注意每個公開和私密金鑰後面的&#x200B;_複製_&#x200B;連結。 在下一步中，您將複製並貼上這些值，以將您的存放區與Commerce Marketplace同步。

## 安裝程式

>[!IMPORTANT]
>
>從Adobe Commerce和Magento Open Source 2.4.0開始，Web安裝精靈已移除，您必須使用命令列[安裝](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html?lang=zh-Hant)或[升級](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade.html?lang=zh-Hant)您的執行個體。 此需求也包含[模組](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html?lang=zh-Hant)和[擴充功能](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html?lang=zh-Hant)。

Commerce的&#x200B;_內部部署_&#x200B;安裝中，[!DNL Marketplace]次購買的安裝程式與[Adobe雲端架構][4]上託管的安裝不同。

![Commerce Marketplace](./assets/marketplace.png){width="600"}

## 支援

如果您在安裝或使用擴充功能時需要協助，請先參閱擴充功能隨附的檔案。 如果您找不到問題的答案，請使用擴充功能清單中的連絡資訊，直接連絡開發人員。 如果您在Marketplace購買的產品不符合您的需求，您可在購買日期起的25天內[要求退款](#refund-requests)。 Adobe會稽核所有退款請求，並（如果已核准）發出適當的退款。 若為Commerce Marketplace的相關問題：

方法1：前往[Adobe Commerce Marketplace](https://commercemarketplace.adobe.com/)，導覽至頁面底部，然後按一下[!UICONTROL Contact Us]，開啟表單以提交票證。

方法2： [電子郵件支援](mailto:commercemarketplacesupport@adobe.com)。

### 簽出問題

您必須在Marketplace購買系統中完成帳戶設定檔中的位址列位，才能進行驗證。

1. 在您的Marketplace帳戶設定檔中新增位址列位。
1. 儲存更新的設定檔。
1. 繼續您的結帳。

### 登入問題

登入問題通常與帳戶資料庫中MAGEID與電子郵件地址不符有關。 請聯絡Marketplace支援以尋求協助。

>[!INFO]
>
>應用程式和擴充功能購買不可以是[轉送](#purchase-transfers)到新帳戶。

### 開放原始碼問題

市集支援團隊僅解決與[commercemarketplace.adobe.com/](https://commercemarketplace.adobe.com/)和[commercedeveloper.adobe.com/](https://commercedeveloper.adobe.com/)網站相關的問題。 請將Magento Open Source的相關問題直接傳送到[社群論壇](https://community.magento.com/)或[聯絡可以協助Magento Open Source的合作夥伴](https://business.adobe.com/products/magento/partners.html)。

### 退款請求

若要申請Marketplace購買的退款，請登入您的帳戶，然後依照下列步驟進行：

1. 按一下&#x200B;[!UICONTROL **我的設定檔**] > [!UICONTROL **購買記錄**]。
1. 找到購買專案，然後按一下&#x200B;[!UICONTROL **要求退款**]。
1. 完成退款訂單表單。

Marketplace支援將在產生退款請求後索取資訊。 退款選項可在購買日期後25天內使用。 請參閱[市集客戶合約](https://www.adobe.com/legal/terms/enterprise-licensing/magento-legacy-terms.html)。

### 訂單商業發票

您可以從您的Marketplace帳戶中的&#x200B;[!UICONTROL **購買記錄**]&#x200B;下載訂單發票。 商業發票未提供賣家的VAT或地址，因為目前不是Marketplace需求。

若要下載Marketplace購買的訂單發票，請登入您的Marketplace帳戶，然後依照下列步驟進行：

1. 按一下&#x200B;[!UICONTROL **我的設定檔**] > [!UICONTROL **購買記錄**]。
1. 找到購買專案。
1. 按一下訂單右上角的印表機圖示。

### 購買轉移

Marketplace支援團隊無法將購買轉移給其他帳戶。 您必須購買主要Commerce帳戶下的所有應用程式和擴充功能，以避免安裝和部署問題。 Adobe Commerce有權使用單一唯一識別碼。 由於使用Composer進行安裝，因此只能使用與主要帳戶繫結的一組[存取金鑰](#create-an-access-key)。 唯一可用的解決方案是向Marketplace購買帳戶[要求退款](#refund-requests) (如果Adobe Commerce退款政策允許)。

您可以透過主要帳戶[共用](commerce-account-share.md) Commerce執行個體。 共用存取權會將主要帳戶的特殊許可權授予給從屬帳戶。 共用存取點是從主要帳戶產生。 主要帳戶可以是Commerce授權帳戶、主要商家帳戶或組織內共用的帳戶。

這些特殊許可權會授予與主要使用者相同層級的Adobe Commerce存取權，但不會延續至Adobe Commerce Marketplace或開發人員入口網站。 這表示從Marketplace中的附屬帳戶購買擴充功能時，無法與主要帳戶共用。 共用存取權是單向通道（主要帳戶至附屬帳戶）。 當從屬帳戶嘗試共用回主要帳戶時，此功能無法運作。

[1]: https://marketplace.magento.com/
[2]: https://www.paypal.com/us/home
[3]: https://developer.adobe.com/commerce/marketplace/guides/sellers/extension-quality-program/
[4]: https://www.adobe.com/commerce/magento/enterprise.html
[6]: https://business.adobe.com/products/magento/magento-commerce.html
