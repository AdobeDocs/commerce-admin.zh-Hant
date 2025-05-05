---
title: '[!UICONTROL General] &amp；gt； [!UICONTROL New Relic Reporting]'
description: 檢閱Commerce管理員的[!UICONTROL General] &amp；gt； [!UICONTROL New Relic Reporting]頁面上的組態設定。
exl-id: d6bf4810-81a3-420d-abc9-9b87c1e92551
feature: Configuration, System, Reporting
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL New Relic Reporting]

{{config}}

>[!NOTE]
>這些設定選項不適用於雲端基礎結構上的Adobe Commerce。
>
>如果您在Pro計畫上，New Relic已[預先設定並依預設啟用](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html?lang=zh-Hant)。 如果您在入門計畫中，您必須完成設定程式中的[New Relic設定步驟](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/account-management.html?lang=zh-Hant#configure-new-relic-for-starter-environment)。

## [!UICONTROL General]

![一般](./assets/new-relic-reporting-general.png)<!-- zoom -->

<!-- [General](https://experienceleague.adobe.com/zh-hant/docs/commerce-admin/start/reporting/new-relic-reporting) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable New Relic Integration] | 存放區檢視 | 決定您的存放區是否可搭配[!DNL New Relic]報告使用。 選項： `Yes` / `No` |
| [!UICONTROL New Relic API URL] | 存放區檢視 | 部署New Relic API的URL。 例如： `https://api.newrelic.com/deployments.xml` |
| 前瞻分析API URL | 存放區檢視 | Insights API部署所在的URL。 使用百分比符號(%)代表您的帳戶ID。 例如： `https://insights-collector.newrelic.com/v1/accounts/%s/events` |
| [!UICONTROL New Relic Account ID] | 存放區檢視 | 指派給您[!DNL New Relic]帳戶的帳戶ID。 |
| [!UICONTROL New Relic Application ID] | 存放區檢視 | 指派給您[!DNL New Relic]帳戶以用於Commerce整合的應用程式ID。 |
| [!UICONTROL New Relic API Key] | 存放區檢視 | 指派給您的金鑰可取得[!DNL New Relic] API的存取權。 |
| [!UICONTROL Insights API Key] | 存放區檢視 | 指派給您的金鑰，用於取得Insights的存取權。 |
| [!UICONTROL New Relic Application Name] | 存放區檢視 | 您指派給您的[!DNL New Relic]整合的名稱。 |
| [!UICONTROL Send Adminhtml and Frontend as Separate Apps] | 存放區檢視 | 可選擇將店面和管理人員所收集的報表資料以個別應用程式的形式傳送至New Relic。 此選項需要為[!UICONTROL New Relic Application Name]輸入名稱。 此功能會在收集的應用程式資料中附加底線中的應用程式名稱。 例如： `MyStore_Adminhtml`， `MyStore_frontend` |

{style="table-layout:auto"}

## [!UICONTROL Cron]

![Cron](./assets/new-relic-reporting-cron.png)<!-- zoom -->

<!-- Cron](https://experienceleague.adobe.com/zh-hant/docs/commerce-admin/systems/tools/cron) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable Cron] | 存放區檢視 | 決定是否可以使用[Cron](../../systems/cron.md)依排程執行[!DNL New Relic]報告。 選項： `Yes` / `No` |

{style="table-layout:auto"}
