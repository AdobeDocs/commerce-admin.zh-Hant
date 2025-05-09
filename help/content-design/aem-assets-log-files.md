---
title: 設定記錄輪換
description: 為Commerce的AEM Assets整合設定記錄輪換。
feature: CMS, Media, Integration
exl-id: f735d086-048c-4555-bc58-ac6736c281b0
source-git-commit: c71fd243d809e2b86c5c8e781d527892965838ae
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# 設定Experience Manager Assets

適用於Commerce的AEM Assets整合在您的Commerce執行個體中提供下列記錄檔：

- `/var/log/aem-assets-integration.log`
- `/var/log/aem-assets-integration-errors.log`

請要求您的系統管理員檢查這些記錄的記錄檔輪換排程，以防止它們變得太大。 在某些環境中，記錄檔會自動輪換，但在其他環境中，您必須手動設定記錄輪換。 如需詳細資訊，請參閱下列主題：

- 若為Adobe Commerce內部部署安裝，請要求系統管理員設定[記錄輪換](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/configuration.html?lang=zh-Hant#server-settings)。
- 如需雲端基礎結構專案上的Adobe Commerce，請參閱[檢視及管理記錄檔](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/test/log-locations.html?lang=zh-Hant)。
