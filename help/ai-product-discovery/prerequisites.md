---
title: AI產品探索必要條件
description: 檢閱目錄擴充和PDP擴充的需求，並在雲端基礎結構或內部部署上的Adobe Commerce上安裝共用擴充功能。
role: Admin, Developer
source-git-commit: 591fca4f18862d289fb233997e8848cb4692d1e7
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%
---
# 先決條件

在使用目錄擴充或PDP擴充之前，請確認適用於每個部署的需求，然後完成您的Commerce平台的設定。

## 所有部署的需求 {#all-deployments}

| 需求 | 套用至 | 詳細資料 |
| --- | --- | --- |
| 在Edge最佳化 | PDP擴充 | 必填。 Edge最佳化可將擴充的產品資料傳遞給AI代理程式。 請參閱[在Edge最佳化指南](https://experienceleague.adobe.com/en/docs/brand-visibility/using/resources/optimize-at-edge/fastly-byocdn)。 |
| 記錄轉送 | 兩個工作流程 | 選填。 根據代理流量啟用擴充建議。 如果沒有它，您仍然可以手動選取產品或產品頁面。 請參閱[記錄轉送指南](https://experienceleague.adobe.com/en/docs/brand-visibility/using/log-forwarding/log-forwarding-overview)。 |
| 可編目店面 | 目錄擴充 | 對於抓取型建議是必要的。 LLM導向和代理程式機器人必須能夠存取您的產品頁面。 |
| [!DNL Adobe Admin Console]存取權 | 兩個工作流程 | 必填。 在設定期間，[!DNL Adobe Commerce]會檢查您組織的GenAI騎士狀態。 除非您的組織選擇退出GenAI附加服務，否則您具有存取權。 |

<!--
TBD (SME): The Optimize at Edge guide is a Brand Visibility reference, not a Commerce setup guide. Add Commerce-specific Optimize at Edge setup instructions (this might be automated by GA).
-->

## 設定您的Commerce平台 {#set-up}

>[!BEGINTABS]

>[!TAB 雲端基礎結構或內部部署上的 Commerce]

針對雲端基礎結構或內部部署上的[!DNL Adobe Commerce]，您安裝共用擴充擴充功能，這會啟用目錄擴充和PDP擴充。

**開始之前：**

- PHP 8.3或更新版本上的[!DNL Adobe Commerce] 2.4.7或更新版本。 請參閱[發行說明](release-notes.md)。
- [!DNL Adobe IMS]組織。 如果您的組織沒有這類應用程式，請參閱[Adobe IMS整合總覽](https://experienceleague.adobe.com/en/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview)。 目錄擴充使用已登入之管理員使用者的IMS存取權杖。 僅使用Commerce使用者名稱和密碼登入不會提供此權杖。
- 對Commerce應用程式伺服器的命令列存取權，以及從`repo.magento.com`下載套件的許可權。

**安裝及驗證：**

1. 如果[!DNL Live Search]或[!DNL Product Recommendations]皆未啟用，請從您的Commerce專案目錄中新增[!DNL Catalog Service]：

   ```bash
   composer require magento/catalog-service --no-update
   composer update magento/catalog-service
   ```

   [!DNL Catalog Service]已與[!DNL Live Search]和[!DNL Product Recommendations]一起自動安裝，因此如果任一服務已啟用，請略過此步驟。

1. 如果尚未為其他Commerce服務設定，請使用API金鑰和SaaS資料空間來設定[Commerce服務聯結器](https://experienceleague.adobe.com/en/docs/commerce/user-guides/integration-services/saas)。

1. 新增共用擴充功能：

   ```bash
   composer require magento/module-catalog-enrichment --no-update
   composer update magento/module-catalog-enrichment
   ```

1. 部署變更：

   - **雲端基礎結構：**&#x200B;認可並將變更推送至`composer.json`和`composer.lock`。
   - **內部部署：**&#x200B;升級應用程式並清除快取：

     ```bash
     bin/magento setup:upgrade
     bin/magento cache:clean
     ```

1. 在Admin中，前往「**[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Data Feed Sync Status]**」，並確認Commerce已匯出目錄資料。

   成功傳送的產品記錄數應與來源記錄相符，無失敗或等待提交。 對於失敗的記錄，請檢閱錯誤詳細資料、解決問題，並排程受影響記錄的重新同步。

1. 移至&#x200B;**[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Data Management Dashboard]**，並確認預期的目錄資料可在[!DNL Catalog Service]中使用。

如需狀態詳細資料和疑難排解，請參閱[監視資料摘要狀態](/help/systems/data-feed-sync-status.md#monitor-data-feed-status)。

>[!TAB Adobe Commerce as a Cloud Service]

針對[!DNL Adobe Commerce as a Cloud Service]，在帳戶布建期間會為您處理[!DNL Catalog Service]的安裝、目錄擴充和PDP擴充。

完成所有部署[&#128279;](#all-deployments)的需求，這些需求適用於您計畫使用的工作流程。

<!-- TBD (SME): Confirm whether merchants on Adobe Commerce as a Cloud Service should verify catalog data on the Data Management Dashboard, and whether the IMS and Admin Console requirements apply. -->

>[!ENDTABS]

## 下一步 {#next-step}

[設定擴充設定](settings.md)以將您的Commerce執行個體連結至AI產品探索。
