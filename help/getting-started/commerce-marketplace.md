---
title: '[!DNL Adobe Commerce Marketplace]'
description: 瞭解 [!DNL Commerce Marketplace]，為商戶提供精選的解決方案，並為合格的開發人員提供工具、平台和絕佳位置，以建立欣欣向榮的業務。
exl-id: e04e48f2-3b1d-45bf-b0f6-3a1ed43e78c5
feature: Extensions
source-git-commit: 1a5a00493e9994343c7decc763f2decdd11192c7
workflow-type: tm+mt
source-wordcount: '892'
ht-degree: 0%

---

# Adobe Commerce Marketplace

[Adobe Commerce Marketplace][1] 是應用程式商店，為商家提供精選的解決方案，並為合格開發人員提供工具、平台和絕佳位置，以建立欣欣向榮的業務。 [!DNL Commerce Marketplace] 提供一系列免費的擴充功能以及其他可供出售的擴充功能。 可以用信用卡或帳戶支付購買專案 [PayPal][2].

所有擴充功能均可在 [!DNL Commerce Marketplace] 已通過廣泛審查。 此 [擴充功能品質計畫][3] (EQP)組合 [!DNL Commerce] 專業知識、開發指引和驗證工具，以確保Commerce Marketplace上的所有擴充功能都符合編碼標準和最佳實務。 稽核程式包括自動檢查和手動QA稽核。 在此過程中，會檢查並測試每個擴充功能的結構和程式碼，以找出病毒/惡意程式碼感染的證據，以及是否有任何剽竊的跡象。 檢閱包括由執行機構進行的深入技術檢查和健全性檢查 [!DNL Commerce] 工程師，專注於檔案、編碼結構、效能、擴充性、安全性，以及與 [!DNL Commerce] 核心。

雖然您可以從其他來源購買擴充功能，但僅限上可用的擴充功能 [!DNL Commerce Marketplace] 可透過擴充功能品質計畫中的廣泛技術和行銷審查，來進行驗證。

## 應用程式資源

開發人員傳統上會使用PHP建立程式內擴充功能，以新增功能、服務和整合至Adobe Commerce。 與擴充功能相比，透過建立具有程式外擴充功能的應用程式，您可以避免相容性問題。

下列資源為新的採用者提供熟悉應用程式的起點：

### Commerce資源：

- [設定Adobe Commerce的I/O事件](https://developer.adobe.com/commerce/extensibility/events/)
- [為Adobe Commerce設定事件](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/)
- [設定管理員UI SDK](https://developer.adobe.com/commerce/extensibility/admin-ui-sdk/)
- [將擴充功能轉換為應用程式](https://developer.adobe.com/commerce/extensibility/app-development/#how-do-i-port-an-extension-into-an-app)

### App Builder資源：

- [Commerce App Builder概觀](https://developer.adobe.com/commerce/extensibility/app-development/)
- [為Adobe Developer App Builder設定API網格](https://developer.adobe.com/graphql-mesh-gateway/gateway/getting-started/)
- [部署App Builder應用程式](https://developer.adobe.com/app-builder/docs/guides/deployment/)
- [App Builder應用程式的CI/CD](https://developer.adobe.com/app-builder/docs/guides/deployment/ci_cd_for_firefly_apps/)
- App Builder/開發人員控制檯快速入門
   - [App Builder快速入門](https://developer.adobe.com/app-builder/docs/getting_started/)
   - [瞭解專案和工作環境](https://developer.adobe.com/app-builder/docs/resources/videos/exploring/projects-and-workspaces/)

## [!DNL Marketplace] 認證

安裝您購買的擴充功能之前， [!DNL Commerce Marketplace]，登入您的 [!DNL Commerce] 帳戶，並確認您擁有作用中的存取金鑰。 您可以登入 [!DNL Commerce] 來自標題的帳戶 [[!DNL Marketplace]][1] 或 [Magento.com][6].

您的存取金鑰是一組公開和私密金鑰，用來同步您的 [!DNL Commerce] 使用進行安裝 [!DNL Commerce] 帳戶並驗證您的認證。 帳戶同步後，每次從Commerce Marketplace安裝擴充功能或模組或升級時，都必須輸入私密金鑰 [!DNL Commerce] 安裝。

您可以根據不同目的建立多個存取金鑰，並視需要啟用或停用它們。 不過，您必須使用與安裝 [!DNL Commerce] 軟體。 例如，您無法使用Magento Open Source存取金鑰來更新或升級Adobe Commerce，反之亦然。 您也無法使用屬於其他使用者或來自的存取金鑰。 [共用帳戶](commerce-account-share.md).

### 建立存取金鑰

1. 登入您的 [!DNL Commerce] 帳戶。

1. 在 _[!UICONTROL My Account]_頁面，選擇&#x200B;**[!UICONTROL Marketplace]**標籤。

1. 在名稱的右上角，按一下向下箭頭，然後選擇 **[!UICONTROL My Profile]**.

   ![您的 [!DNL Marketplace] 設定檔](./assets/marketplace-profile.png){width="600"}

1. 在 _[!UICONTROL Marketplace]_標籤下的_[!UICONTROL My Products]_，按一下 **[!UICONTROL Access Keys]**，然後執行下列任一項作業：

   - 檢視您是否擁有一組用於購買Marketplace的存取金鑰。 您可以針對不同用途建立多組存取金鑰。

   ![存取金鑰](./assets/access-keys.png){width="600"}

   - 按一下 **[!UICONTROL Create a New Access Key]**. 輸入新金鑰組的名稱，然後按一下 **[!UICONTROL OK]**. 有效字元包括大小寫字元和連字型大小而非空格。

1. 完成後，按一下 **[!UICONTROL OK]**.

   您的新存取金鑰已啟用，並會顯示在清單中。

   請注意 _複製_ 每個公開和私密金鑰之後的連結。 在下一步中，您將複製並貼上這些值，以將您的存放區與Commerce Marketplace同步。

## 安裝程式

>[!IMPORTANT]
>
>從Adobe Commerce和Magento Open Source2.4.0開始，Web設定精靈會移除，您必須使用命令列 [安裝](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) 或 [升級](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade.html) 您的執行個體。 此需求也包括 [模組](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) 和 [擴充功能](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html).

的安裝程式 [!DNL Marketplace] 購買與不同 _內部部署_ Commerce的安裝比託管的安裝還多 [Adobe雲端架構][4].

![Commerce Marketplace](./assets/marketplace.png){width="600"}

## 支援

如果您在安裝或使用擴充功能時需要協助，請先參閱擴充功能隨附的檔案。 如果您找不到問題的答案，請使用擴充功能清單中的連絡資訊，直接連絡開發人員。

如果您在Commerce Marketplace上購買的產品不符合您的需求，您可以在購買日起25天內要求退款。 Adobe會複查所有退款請求，並在核准後核發適當的退款。

如需Commerce Marketplace的相關支援問題，請參閱 [[!DNL Marketplace] 說明中心][5].

[1]: https://marketplace.magento.com/
[2]: https://www.paypal.com/us/home
[3]: https://developer.adobe.com/commerce/marketplace/guides/sellers/extension-quality-program/
[4]: https://www.adobe.com/commerce/magento/enterprise.html
[5]: https://marketplacesupport.magento.com/hc/en-us
[6]: https://business.adobe.com/products/magento/magento-commerce.html
