---
title: 適用於Commerce管理員的Adobe Experience Cloud整合
description: 瞭解Admin Unified Experience擴充功能，其將Commerce與Experience Cloud整合，以便客戶可從Experience Cloud首頁存取Commerce專案。
feature: Integration
exl-id: e3fb6337-c7d5-4b6f-8f4a-583697a1f2d2
source-git-commit: a07c91bc2f01cd110f3e0ccd6d27fe5d37eb2fc9
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# 適用於商務的Adobe Experience Cloud整合

{{ee-feature}}

啟用Admin Unified Experience擴充功能，將Adobe Commerce專案與Experience Cloud整合。 當整合作用中時，管理員可以從Adobe Experience Cloud存取Commerce專案。

![從Experience Cloud首頁存取Commerce](./assets/admin-uex-home-page.png){width="700" zoomable="yes"}

## 檢視可用的商務專案

管理員可以檢視他們有權存取的Commerce專案，方法是選取 **[!UICONTROL Commerce]** 從Experience Cloud首頁。

![Experience Cloud上的Commerce專案工作區](./assets/admin-uex-commerce-projects-home.png){width="700" zoomable="yes"}

管理員可以從以下位置為每個專案開啟管理員和店面： [!DNL Commerce Projects] 工作區並檢視其他資訊。

- **Commerce店面首頁快照** — 店面首頁的快照。 如果專案有多個網站，快照會顯示預設網站的首頁。

- **[專案名稱](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html)** — 識別例項的雲端專案環境。 專案名稱預設為 [Git分支名稱](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/console-branches.html) 在雲端專案中。 變更或更新中的專案名稱 [統一的Experience Store組態設定](admin-unified-experience-integration-manage.md#manage-the-integration-from-the-admin).

- **[店面URL](../stores-purchase/store-urls.md)** — 顯示預設網站的基底URL。

- **[環境型別](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html)** — 使用識別部署至開發或測試環境的商務執行個體 [!UICONTROL Development] 或 [!UICONTROL Staging] 標籤。 沒有標籤的執行個體會部署至生產環境。

- **Commerce管理員存取權** — 按一下「 」以開啟「管理員」 **[!UICONTROL Open]**.

- **店面存取** — 透過選取來開啟店面 **[!UICONTROL Open storefront]** 從「選項」功能表。

- **快速存取選取的專案** — 選擇 **[!UICONTROL Add to Favorites]** 從選項功能表將專案新增到 [!UICONTROL Favorites] 標籤。

## 驗證流程

啟用Experience Cloud整合時，管理員會使用以下工作流程來驗證和存取Commerce專案。

1. 透過Experience Cloud登入頁面登入。

   ![Experience Cloud登入頁面](./assets/admin-uex-experience-cloud-login.png){width="600" zoomable="yes"}

   管理員必須登入才能使用與商務執行個體相關聯之組織的Adobe企業設定檔Experience Cloud。 另請參閱 [管理Adobe設定檔](https://helpx.adobe.com/enterprise/using/manage-adobe-profiles.html).

1. 在Experience Cloud首頁上，開啟 [!UICONTROL Commerce Projects workspace] 藉由選取 **[!UICONTROL Open]**.

1. 存取專案的管理員，方法是選取 **[!UICONTROL Open]**.

1. 在Adobe Commerce登入頁面上，選取 **[!UICONTROL Sign in with Adobe ID]** 以完成驗證並開啟Admin。

   ![Adobe Commerce登入頁面](./assets/admin-adobeid-login.png){width="600" zoomable="yes"}

>[!NOTE]
>
>另請參閱 [管理Experience Cloud整合](admin-unified-experience-integration-manage.md) 以取得當啟用或停用Experience Cloud整合時如何影響驗證工作流程的詳細資訊。

## 需求

- Adobe Commerce 2.4.5或更新版本
- 雲端基礎結構上的Adobe Commerce
- Adobe Commerce擴充功能

   - Commerce Admin Unified Experience擴充功能(`magento/module-unified-experience`)

     如果Commerce執行個體上沒有此模組，則可使用Composer進行安裝。

   - [Adobe I/O事件服務](https://developer.adobe.com/commerce/extensibility/events/) — 需要傳送事件資料，以管理管理員對Experience Cloud中Commerce專案的存取。

     Adobe I/O Commerce事件擴充功能(`magento/commerce-eventing`)，此版本隨Adobe Commerce 2.4.4及更新版本提供。

## 啟用整合

依照以下指示啟用整合： [使用Commerce管理員設定Experience Cloud整合](admin-unified-experience-integration-configure.md).

>[!TIP]
>
>如果Commerce例項上已啟用Experience Cloud整合，請參閱 [管理Experience Cloud整合](admin-unified-experience-integration-manage.md) 以取得變更或更新組態、管理管理員存取權及疑難排解的詳細資訊。
