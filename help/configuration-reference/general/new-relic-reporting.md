---
title: 『[!UICONTROL General] &gt； [!UICONTROL New Relic Reporting]『
description: 檢閱上的組態設定 [!UICONTROL General] &gt； [!UICONTROL New Relic Reporting] 商務管理員頁面。
exl-id: d6bf4810-81a3-420d-abc9-9b87c1e92551
feature: Configuration, System, Reporting
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 4%

---

# [!UICONTROL General] > [!UICONTROL New Relic Reporting]

{{config}}

## [!UICONTROL General]

![一般](./assets/new-relic-reporting-general.png)<!-- zoom -->

<!-- [General](https://docs.magento.com/user-guide/reports/new-relic-reporting.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable New Relic Integration] | 存放區檢視 | 決定您的商店是否可搭配 [!DNL New Relic] 報表。 選項： `Yes` / `No` |
| [!UICONTROL New Relic API URL] | 存放區檢視 | 部署New Relic API的URL。 例如： `https://api.newrelic.com/deployments.xml` |
| 前瞻分析API URL | 存放區檢視 | Insights API部署所在的URL。 使用百分比符號(%)代表您的帳戶ID。 例如： `https://insights-collector.newrelic.com/v1/accounts/%s/events` |
| [!UICONTROL New Relic Account ID] | 存放區檢視 | 指派給您的帳戶ID [!DNL New Relic] 帳戶。 |
| [!UICONTROL New Relic Application ID] | 存放區檢視 | 指派給您的 [!DNL New Relic] 帳戶進行商務整合。 |
| [!UICONTROL New Relic API Key] | 存放區檢視 | 指派給您的金鑰，用於存取 [!DNL New Relic] API。 |
| [!UICONTROL Insights API Key] | 存放區檢視 | 指派給您的金鑰，用於取得Insights的存取權。 |
| [!UICONTROL New Relic Application Name] | 存放區檢視 | 您指派給您的名稱 [!DNL New Relic] 整合。 |
| [!UICONTROL Send Adminhtml and Frontend as Separate Apps] | 存放區檢視 | 可選擇將店面和管理人員所收集的報表資料以個別應用程式的形式傳送至New Relic。 此選項需要為輸入名稱 [!UICONTROL New Relic Application Name]. 此功能會在收集的應用程式資料中附加底線中的應用程式名稱。 例如： `MyStore_Adminhtml`， `MyStore_frontend` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Cron]

![Cron](./assets/new-relic-reporting-cron.png)<!-- zoom -->

<!-- Cron](https://docs.magento.com/user-guide/system/cron.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable Cron] | 存放區檢視 | 決定是否 [!DNL New Relic] 報告可以透過以下方式依排程執行 [Cron](../../systems/cron.md). 選項： `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}
