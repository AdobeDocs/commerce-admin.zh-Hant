---
title: ' [!DNL New Relic] 報告'
description: ' [!DNL New Relic] 瞭解 Adobe Systems Commerce on 雲端基礎結構 帳戶可用的報告，其中包括 新 Relic APM 服務的軟體。'
exl-id: 65d08bda-da01-4dcf-9d92-189d4d303c76
role: Admin, Leader
feature: System
source-git-commit: e9a7645aed0e3b48bf565b04cdb6a31ce5d39ca0
workflow-type: tm+mt
source-wordcount: '1361'
ht-degree: 0%

---

# [!DNL New Relic] 報告

[New Relic][1] 是軟體分析服務，可協助您分析和改善應用程式互動。 在雲端基礎結構上使用Adobe Commerce的帳戶，包括用於下列專案的軟體： [!DNL New Relic APM] 服務。 如需詳細資訊，請參閱 [New Relic服務][4] 在 _雲端基礎結構上的Commerce指南_.

## 步驟1：註冊 [!DNL New Relic] 帳戶

1. 訪問 [[!DNL New Relic]][1] 網站並註冊帳戶。

   您還可以註冊免費試用帳戶。

1. 按照網站上的說明進行操作。 出現提示時，選擇要首先安裝的產品。

1. 當您在帳戶中時，請找到完成商務配置所需的以下憑據：

   | 選項 | 說明 |
   | ------ | ----------- |
   | 帳戶 ID | 從您的 [!DNL New Relic] account dashboard中，Account ID是URL中位於以下位置的號碼： `/accounts` |
   | 應用程式ID | 從您的 [!DNL New Relic] 帳戶儀表板，按一下 **[!UICONTROL New Relic APM]**. 在功能表中，選擇 **[!UICONTROL Applications]**. 然後，選擇您的應用程式。 應用程式ID是URL中位於下列位置後的數字： `/applications/` |
   | New Relic API金鑰 | 從您的 [!DNL New Relic] 帳戶儀表板，按一下 **[!UICONTROL Account Settings]**. 在左側功能表的「整合」下方，選擇 **[!UICONTROL Data Sharing]**. 您可以在此頁面建立、重新產生或刪除您的API金鑰。 |
   | Insights API金鑰 | 從您的 [!DNL New Relic] 帳戶儀表板，按一下 **[!UICONTROL Insights]**. 在左側「管理」下的功能表中，選擇 **[!UICONTROL API Keys]**. 您的前瞻分析API金鑰會出現在本頁上。 如有必要，請按一下加號(**+**)來產生金鑰。 |

   {style="table-layout:auto"}

## 步驟2：安裝 [!DNL New Relic] 伺服器上的代理程式

使用 [!DNL New Relic APM Pro] 若要收集和傳輸資料，必須在伺服器上安裝PHP代理程式。

1. 提示選擇網路代理程式時，請按一下 **PHP**.

1. 若要在伺服器上設定PHP代理程式，請依照指示操作。

   如果您需要協助，請參閱 [適用於PHP的New Relic][3].

1. 請確定cron正在您的伺服器上執行。

   若要深入瞭解，請參閱 [設定並執行cron][5] 在開發人員檔案中。

## 步驟3：設定您的存放區

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側導覽面板中， **[!UICONTROL General]** 展開，請選擇 **[!UICONTROL New Relic Reporting]** 並執行下列動作：

   ![New Relic報告設定](./assets/new-relic-reporting-general.png){width="600"}

   * 設定 **[!UICONTROL Enable New Relic Integration]** 至 `Yes`.

   * 在 **[!UICONTROL Insights API URL]**，取代百分比(`%`New Relic )符號。

   * 輸入您的 **[!UICONTROL New Relic Account ID]**.

   * 輸入您的 **[!UICONTROL New Relic Application ID]**.

   * 輸入您的 **[!UICONTROL New Relic API Key]**.

   * 輸入您 **[!UICONTROL Insights API Key]**.

1. 的 **[!UICONTROL New Relic Application Name]**，輸入名稱以識別供內部參考的組態。

1. （選用） For **[!UICONTROL Send Adminhtml and Frontend as Separate Apps]**，選取 `Yes` 將店面和管理員收集到的資料以個別應用程式的形式傳送至New Relic。

   此選項要求為 . **[!UICONTROL New Relic Application Name]**

   >[!NOTE]
   >
   >啟用此功能可減少誤判次數 [!DNL New Relic] 警報，允許嚴格針對前端效能進行設定的監控和警報。 New Relic會接收獨立的應用程式資料檔案，且會在檔案後面附加應用程式名稱 `Adminhtml` 和前端。 例如： `MyStore_Adminhtml`

1. 完成後，按一下 **[!UICONTROL Save Config]**.

## 步驟4：啟用Cron [!DNL New Relic] 報告

1. 展開 ![ 該部分選擇器 ](../assets/icon-display-expand.png) **[!UICONTROL Cron]** 展開。

   ![New Relic Cron設定](./assets/new-relic-reporting-cron.png){width="600"}

1. 設定 **[!UICONTROL Enable Cron]** 至 `Yes`.

1. 完成後，按一下 **[!UICONTROL Save Config]**.

## [!DNL New Relic] 查詢

[!DNL New Relic Insights] 資料是根據寫入的陳述式 [!DNL New Relic Query Language] (NRQL)以及您可能包含的任何自訂引數。 資料可從臨機查詢傳回，或透過儲存至儀表板的查詢傳回。 若要進一步瞭解，請參閱 [NRQL參考][6] 在 [!DNL New Relic] 檔案。

### 管理事件

#### 作用中的管理員使用者

傳回作用中管理員使用者的數目。

    SELECT uniqueCount(AdminId)
    FROM交易
    其中appName=&#39;&lt;your_app_name>&#39;從15分鐘前

#### 當前有效的管理員使用者

返回活動管理員使用者的名稱。

    SELECT uniques（AdminName） 
     FROM 交易 
     其中 appName=&#39;&lt;your_app_name>&#39; SINCE 15 分鐘前 
 &lt;/your_app_name>
#### 最近的管理活動

傳回最近的管理員動作數。

    SELECT計數(AdminId)
    FROM交易
    其中appName =&#39;&lt;your_app_name>&#39; FACET AdminName自1天前開始

#### 最新的管理員活動

返回有關最近管理員操作的詳細資訊，包括管理員使用者名、持續時間和應用程式名稱。

    選擇管理員名稱、持續時間、名稱 
     來自事務 
     ，其中 appName=&#39;&#39; 且 AdminName&lt;your_app_name>非空 
     值和 AdminName ！&lt;/your_app_name>= &#39;N/A&#39; 限制 50

### Cron 事件

#### 類別計數

傳回指定時段內依類別分類的應用程式事件數目。

    SELECT average(CatalogCategoryCount)
    從Cron
    其中CatalogCategoryCount不是NULL
    AND appName = &#39;&lt;your_app_name>&#39;時程2分鐘

#### 目前目錄計數

傳回指定時段內依類別分類之目錄中的應用程式事件平均數目。

    SELECT average(CatalogCategoryCount)
    從Cron
    其中CatalogCategoryCount不是NULL
    AND CatalogCategoryCount > 0
    AND appName = &#39;&lt;your_app_name>&#39;由於2分鐘前限制1

#### 使用中的產品

傳回指定時段內依產品分類的應用程式事件數。

    SELECT average(CatalogProductActiveCount)
    從Cron
    其中CatalogProductActiveCount不是NULL
    AND appName = &#39;&lt;your_app_name>&#39;時程2分鐘

#### 使用中的產品計數

傳回指定時段內依產品區分之使用中應用程式事件的平均數目。

    SELECT average(CatalogProductActiveCount)
    從Cron
    其中CatalogProductActiveCount不是NULL
    AND CatalogProductActiveCount > 0
    AND appName = &#39;&lt;your_app_name>&#39;由於2分鐘前限制1

#### 可設定的產品

傳回指定時段內可設定產品之應用程式事件的平均數目。

    SELECT average(CatalogProductConfigurableCount)
    從Cron
    其中CatalogProductConfigurableCount不是NULL
    AND appName = &#39;&lt;your_app_name>&#39;時程2分鐘

#### 可設定的產品計數

傳回指定時段內可設定產品所執行之應用程式事件的平均數目。

    SELECT average(CatalogProductConfigurableCount)
    從Cron
    其中CatalogProductConfigurableCount不是NULL
    AND CatalogProductConfigurableCount > 0
    AND appName = &#39;&lt;your_app_name>&#39;由於2分鐘前限制1

#### 產品計數（全部）

傳回所有產品的應用程式事件總數。

    SELECT average(CatalogProductCount)
    從Cron
    其中CatalogProductCount不是NULL
    AND appName = &#39;&lt;your_app_name>&#39;時程2分鐘

#### 目前產品計數（全部）

傳回指定時段內所有產品的平均應用程式事件數。

    SELECT average(CatalogProductCount)
    從Cron
    其中CatalogProductCount不是NULL
    AND CatalogProductCount > 0
    AND appName = &#39;&lt;your_app_name>&#39;由於2分鐘前限制1

#### 客戶計數

傳回依客戶分類的應用程式事件平均數量。

    SELECT average(CustomerCount)
    從Cron
    其中CustomerCount不是NULL
    而CustomerCount > 0&lt;
    AND appName = &#39;&lt;your_app_name>&#39;時程2分鐘

#### 目前客戶計數

傳回指定時段內的平均客戶數。

    SELECT average(CustomerCount)
    從Cron
    其中CustomerCount不是NULL
    而CustomerCount > 0
    AND appName = &#39;&lt;your_app_name>&#39;由於2分鐘前限制1

#### 模組狀態

傳回指定時段內啟用、停用或安裝應用程式模組的平均次數。

    SELECT average(ModulesDisabled)， average(ModulesEnabled)， average
    （已安裝模組）
    從Cron&lt;
    其中appName = &#39;&lt;your_app_name>&#39;時程2分鐘

#### 目前模組狀態

傳回指定時段內啟用、停用或安裝模組的平均次數。

    SELECT average(ModulesDisabled)， average(ModulesEnabled)， average
    （已安裝模組）
    從Cron
    其中appName = &#39;&lt;your_app_name>&#39;由於2分鐘前限制1

#### 網站和商店計數

傳回指定時段內依網站和商店分類的應用程式事件平均數量。

    SELECT average(StoreViewCount)， average(WebsiteCount)
    從Cron
    WHERE appName = &#39;&amp;lt；your_app_name&amp;gt；&#39; TIMESERIES 2分鐘

#### 目前的網站和商店計數

傳回指定時段內目前應用程式事件的平均數目。

    SELECT average(StoreViewCount)， average(WebsiteCount)
    從Cron
    其中appName = &#39;&lt;your_app_name>&#39;由於2分鐘前限制1

#### Cron — 來自事件的所有資料

傳回所有應用程式事件資料。

    選取*
    從Cron
    其中appName = &#39;&lt;your_app_name>『

### 客戶

#### 作用中客戶計數

傳回指定時段內的作用中客戶數目。

    SELECT uniqueCount(CustomerId)
    FROM交易
    其中appName = &#39;&lt;your_app_name>&#39;從15分鐘前

#### 活躍客戶

返回指定時段期間的活動客戶名稱。

    選擇獨特值 （CustomerName） 
     FROM 交易 
     位置 appName=&#39;&lt;your_app_name>&#39; SINCE 15 分鐘前 
 &lt;/your_app_name>
#### 主要客戶

傳回指定時段內排名最前的客戶。

    SELECT count(CustomerId)
    FROM交易
    其中appName = &#39;&lt;your_app_name>&#39; FACET CustomerName自1天前開始

#### 最近的管理活動

返回定義數量的最近活動記錄，其中包括客戶名稱和造訪持續時間。

    選擇「客戶名稱」、「持續時間」、「 
     來自交易 
     的名稱」，其中 appName=&#39;&lt;your_app_name>&#39; 
     AND 客戶名稱非空 
     值，而「客戶名稱！&lt;/your_app_name>= &#39;N/A&#39; 限制 50

### 訂單

#### 訂購次數

返回在指定時段期間的訂購次數。

    SELECT count(Order)
    從1天前開始的FROM交易

#### 訂單值總計

傳回指定時段內訂購的行專案總數。

    SELECT sum(orderValue)
    從1天前開始的FROM交易

#### 訂購的行專案總數

傳回指定時段內訂購的行專案總數。

    SELECT sum(lineItemCount)
    從1天前開始的FROM交易


[1]: https://newrelic.com/
[3]: https://docs.newrelic.com/docs/agents/php-agent/getting-started/new-relic-php
[4]: https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html
[5]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html
[6]: https://docs.newrelic.com/docs/insights/new-relic-insights/using-new-relic-query-language/nrql-reference
