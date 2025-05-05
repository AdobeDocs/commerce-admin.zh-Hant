---
title: 設定Commerce管理員的Experience Cloud整合
description: 瞭解如何設定Commerce專案，以透過Experience Cloud啟用管理員存取權。
hide: false
hidefromtoc: false
feature: Integration
role: Admin, Leader
exl-id: b2522d25-8255-4219-98b5-4b764430dea2
source-git-commit: 8278d725a7377b865c118b86a57702cd2be43238
workflow-type: tm+mt
source-wordcount: '1011'
ht-degree: 0%

---

# 透過Commerce管理員設定Experience Cloud整合

透過設定Commerce應用程式以使用Commerce Admin Unified Experience和Commerce Events擴充功能，開始與Commerce Admin整合Experience Cloud。


## 必要條件

- Adobe Commerce必須設定為使用[Adobe IMS驗證](../getting-started/adobe-ims-config.md)
- 帳戶布建與許可權 — 管理員必須擁有[Adobe企業設定檔](https://helpx.adobe.com/enterprise/kb/introducing-adobe-profiles.html#:~:text=Adobe%20profiles%20help%20you%20manage,under%20the%20same%20email%20address)，且有權存取下列資源，才能設定Experience Cloud整合：
   - [Adobe Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html) — 新增並管理組織的Adobe使用者和開發人員帳戶
   - [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/getting-started/) — 開發人員或系統管理員存取權可建立App Builder專案，並產生連線認證和專案設定以使用Adobe I/O事件服務
   - [雲端基礎結構專案上的Commerce](https://experienceleague.adobe.com/docs/commerce-cloud-service/start/onboarding.html#get-started-with-the-project-web-interface) — 安裝必要的模組並使用Adobe Commerce CLI設定Commerce應用程式伺服器
   - [Commerce管理員](https://experienceleague.adobe.com/docs/commerce-admin/start/guide-overview.html) — 更新存放區設定並管理Commerce使用者帳戶

## 設定概述

完成下列工作以啟用整合：

1. [檢查Commerce環境和應用程式設定](#check-the-commerce-environment-and-application-configuration)。

1. [啟用Commerce Admin Unified Experience擴充功能](#enable-the-commerce-admin-unified-experience-extension)。

1. [設定Commerce的Adobe I/O事件](#set-up-adobe-io-events)。

1. [測試整合](#test-the-integration)。

## 檢查Commerce環境和應用程式設定

在設定Experience Cloud整合之前，請確認您的專案和Commerce應用程式符合需求。

1. 在本機工作站上，變更至Commerce專案的專案目錄。

1. 檢視執行個體的環境分支，以與Experience Cloud整合。

1. 確認Adobe IMS已啟用。

   - 使用環境的[SSH存取URL](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html)連線至Commerce應用程式伺服器。

   - 從命令列，使用Adobe Commerce CLI來檢查IMS模組狀態。

     ```bash
     bin/magento admin:adobe-ims:status
     ```

   如果未啟用此模組，請[使用IMS整合專案的組織和認證來啟用它](../getting-started/adobe-ims-config.md#step-3-enable-the-adminadobeims-module)。

1. 確認管理員使用者可以使用其Adobe ID登入Commerce管理員。

   - 前往Commerce管理員URL。

   - 如果您已登入，請登出。

   - 確保系統重新導向管理員使用者，以使用其Adobe ID登入。

     ![Adobe Commerce使用Adobe ID登入](./assets/admin-adobeid-login.png){width="600" zoomable="yes"}

1. 從本機工作站上的雲端專案目錄中，確認已安裝Commerce Admin Unified Experience擴充功能。

   ```bash
   composer show *unified-experience*
   ```

   如果已安裝擴充功能，Composer會傳回擴充功能名稱和說明。

   ```
   magento/module-unified-experience <version> Commerce module responsible for integration with Adobe Experience Cloud
   ```

   如果未安裝擴充功能，請使用Composer進行安裝。 然後，提交變更並重新部署雲端環境。

   ```
   composer require magento/module-unified-experience
   composer update
   ```

## 啟用Commerce Admin統一體驗

啟用Commerce Admin Unified Experience擴充功能，然後透過Experience Cloud登入。

>[!NOTE]
>
>這些指示顯示Commerce Cloud專案管理員如何使用Adobe Commerce CLI啟用擴充功能。 Commerce管理員使用者也可以更新[Commerce存放區組態設定](admin-unified-experience-integration-manage.md#from-the-commerce-admin)，以啟用擴充功能。

1. 從本機工作站上雲端專案環境的根目錄中，使用[magento-cloud CLI工具](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/dev-tools/cloud-cli/cloud-cli-overview.html)登入Commerce應用程式伺服器。

   ```bash
   magento-cloud ssh
   ```

1. 使用Adobe Commerce CLI啟用`magento/module-unified-experience`擴充功能：

   ```bash
   bin/magento config:set admin/unified_experience/enabled 1
   Admin Unified Experience integration is enabled
   ```

1. 清除快取。

   ```bash
   bin/magento cache:clean
   ```

## 設定Commerce的Adobe I/O事件

啟用Experience Cloud整合後，Adobe I/O事件服務會傳送Commerce事件資料給Experience Cloud，以管理管理員對Commerce專案的存取權。 服務設定需要啟用Commerce擴充功能(`magento/commerce-eventing`)的Adobe I/O事件，並在Admin中設定Adobe I/O事件服務。

### 啟用Commerce事件

啟用Commerce Events擴充功能(`magento/commerce-eventing`)，將自訂事件資料從Commerce應用程式傳送至Adobe I/O事件服務。

>[!NOTE]
>
>若是Commerce 2.4.6和更新版本，預設會安裝Commerce Events擴充功能。 針對使用Commerce 2.4.5的Commerce專案，請先使用Composer [安裝擴充功能](https://developer.adobe.com/commerce/extensibility/events/installation/#install-adobe-io-modules-on-commerce)，然後啟用它。

1. 從您的本機Commerce專案開發環境，新增下列設定至`.magento.env.yaml`檔案。

   ```yaml
   stage:
     global:
       ENABLE_EVENTING: true
     deploy:
       CRON_CONSUMERS_RUNNER:
         cron_run: true
         max_messages: 0
         consumers: []
   ```

1. 新增、認可更新的`.magento.env.yaml file`並將其部署至雲端環境。

>[!TIP]
>
>如需使用`.magento.env.yaml`檔案設定和管理環境變數的詳細資訊，請參閱[設定部署的環境變數](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/env/configure-env-yaml.html)。

### 設定Commerce事件整合

完成下列工作以設定Commerce事件整合。 如需詳細指示，請參閱[Commerce的Adobe I/O事件](https://developer.adobe.com/commerce/extensibility/events/project-setup/)開發人員檔案。

1. [建立App Builder專案](https://developer.adobe.com/commerce/extensibility/events/project-setup/)以從Commerce執行個體接收事件資料。

   您需要App Builder專案的認證和設定資料，才能在Commerce管理員中設定整合。

1. 設定Adobe Commerce以使用Adobe I/O事件。

   - [更新Adobe I/O事件服務的存放區組態設定](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#begin-configuring-events-on-commerce)。

   - [設定事件提供者以傳送Commerce事件](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#create-an-event-provider-and-complete-the-commerce-configuration)。

1. [更新App Builder專案以從Commerce執行個體接收事件資料](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#subscribe-and-register-events)。

   請勿註冊或訂閱來自Commerce例項的事件。 當您設定App Builder應用程式的事件提供者時，系統會將事件註冊推送至Commerce專案。

   將事件提供者連線至App Builder專案後，訂閱`observer.uex_commerce_instance_update`事件並儲存變更。

1. 若要建立連線，請透過事件提供者將事件傳送給取用者。

   - 從本機雲端專案目錄的命令列，[使用SSH連線至Commerce應用程式伺服器](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html#connect-to-a-remote-environment)。

     ```bash
     magento-cloud ssh
     ```

   - 使用Adobe Commerce CLI檢查Admin Unified Experience擴充功能的狀態，以傳送事件資料。

     ```bash
     bin/magento bin/magento admin:uex:status
     ```

### 測試整合

確認Commerce管理員可以登入Experience Cloud以檢視可用的Commerce專案，並存取每個專案的管理員和店面。

1. [使用與Commerce執行個體相關聯的Adobe ID和組織登入Experience Cloud](https://experiencecloud.adobe.com/library)。

   ![從Experience Cloud首頁存取Commerce專案](./assets/admin-uex-home-page.png){width="600" zoomable="yes"}

1. 選取&#x200B;**[!UICONTROL Commerce]**&#x200B;以檢視可用的Commerce專案。

   適用於Experience Cloud![&#128279;](./assets/admin-uex-commerce-projects-home.png){width="600" zoomable="yes"}的Commerce專案工作區

1. 選取&#x200B;**[!UICONTROL Open]**，開啟執行個體的管理員。

   ![已啟用Experience Cloud整合的Commerce管理員檢視](./assets/admin-dashboard.png){width="600" zoomable="yes"}

1. 確認您可以如預期執行管理員工作。

   Commerce管理員中的工作流程應遵循相同程式。 如果您在啟用Experience Cloud整合後遇到工作流程變更或錯誤，請連絡您的Commerce系統管理員或[提交Adobe支援票證](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket)。

設定Experience Cloud整合後，請確認已正確布建管理員帳戶，以透過Experience Cloud存取Commerce專案。 請參閱[管理管理員使用者](/help/getting-started/admin-unified-experience-integration-manage.md#manage-admin-user-accounts)。
