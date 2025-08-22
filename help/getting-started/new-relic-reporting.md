---
title: '[!DNL New Relic]報告'
description: 瞭解雲端基礎結構上Adobe Commerce帳戶可用的 [!DNL New Relic] 報告，其中包括New Relic APM服務的軟體。
exl-id: 65d08bda-da01-4dcf-9d92-189d4d303c76
role: Admin, Leader
feature: System
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"
source-git-commit: c406add80981387305755221f21624dad475e63f
workflow-type: tm+mt
source-wordcount: '1399'
ht-degree: 0%

---

# [!DNL New Relic]報告

[New Relic][1]是軟體分析服務，可協助您分析和改善應用程式互動。 雲端基礎結構上的Adobe Commerce帳戶包含[!DNL New Relic APM]服務的軟體。 如需詳細資訊，請參閱[雲端基礎結構上的New Relic指南][4]中的&#x200B;_Commerce服務_。

## 步驟1：註冊[!DNL New Relic]帳戶

1. 移至[[!DNL New Relic]][1]網站並註冊帳戶。

   您也可以註冊免費試用帳戶。

1. 按照網站上的指示進行。 出現提示時，請選擇您要先安裝的產品。

1. 當您在帳戶中時，請找到完成Commerce設定所需的下列憑證：

   | 選項 | 說明 |
   | ------ | ----------- |
   | 帳戶 ID | 從您的[!DNL New Relic]帳戶儀表板，帳戶ID是URL中位於下列之後的數字： `/accounts` |
   | 應用程式ID | 從您的[!DNL New Relic]帳戶儀表板，按一下&#x200B;**[!UICONTROL New Relic APM]**。 在功能表中，選擇&#x200B;**[!UICONTROL Applications]**。 然後，選擇您的應用程式。 應用程式ID是URL中的數字，在`/applications/`之後 |
   | New Relic API金鑰 | 從您的[!DNL New Relic]帳戶儀表板，按一下&#x200B;**[!UICONTROL Account Settings]**。 在左側功能表的[整合]下方，選擇&#x200B;**[!UICONTROL Data Sharing]**。 您可以在此頁面建立、重新產生或刪除您的API金鑰。 |
   | Insights API金鑰 | 從您的[!DNL New Relic]帳戶儀表板，按一下&#x200B;**[!UICONTROL Insights]**。 在左側[管理]下方的功能表中，選擇&#x200B;**[!UICONTROL API Keys]**。 您的前瞻分析API金鑰會出現在本頁上。 如有必要，請按一下[插入金鑰]旁的加號(**+**)以產生金鑰。 |

   {style="table-layout:auto"}

## 步驟2：在您的伺服器上安裝[!DNL New Relic]代理程式

若要使用[!DNL New Relic APM Pro]來收集和傳輸資料，必須在伺服器上安裝PHP代理程式。

1. 當提示選擇網路代理程式時，請按一下&#x200B;**PHP**。

1. 若要在伺服器上設定PHP代理程式，請依照指示操作。

   如果您需要協助，請參閱適用於PHP[的][3]New Relic。

1. 請確定cron正在您的伺服器上執行。

   若要深入瞭解，請參閱開發人員檔案中的[設定並執行cron][5]。

## 步驟3：設定您的存放區

>[!NOTE]
>這些設定選項不適用於雲端基礎結構上的Adobe Commerce。
>
>如果您在Pro計畫上，New Relic已[預先設定並依預設啟用](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html)。 如果您在入門計畫中，您必須完成設定程式中的[New Relic設定步驟](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/account-management.html#configure-new-relic-for-starter-environment)。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在展開&#x200B;**[!UICONTROL General]**&#x200B;的左側導覽面板中，選擇&#x200B;**[!UICONTROL New Relic Reporting]**&#x200B;並執行下列動作：

   ![New Relic報告設定](./assets/new-relic-reporting-general.png){width="600"}

   * 將&#x200B;**[!UICONTROL Enable New Relic Integration]**&#x200B;設為`Yes`。

   * 在&#x200B;**[!UICONTROL Insights API URL]**&#x200B;中，將百分比(`%`)符號取代為您的New Relic帳戶ID。

   * 輸入您的&#x200B;**[!UICONTROL New Relic Account ID]**。

   * 輸入您的&#x200B;**[!UICONTROL New Relic Application ID]**。

   * 輸入您的&#x200B;**[!UICONTROL New Relic API Key]**。

   * 輸入您&#x200B;**[!UICONTROL Insights API Key]**。

1. 針對&#x200B;**[!UICONTROL New Relic Application Name]**，輸入名稱以識別供內部參考的組態。

1. （選擇性）針對&#x200B;**[!UICONTROL Send Adminhtml and Frontend as Separate Apps]**，選取`Yes`以將店面和Admin收集的資料以個別應用程式的形式傳送至New Relic。

   此選項需要為&#x200B;**[!UICONTROL New Relic Application Name]**&#x200B;輸入名稱。

   >[!NOTE]
   >
   >啟用此功能可減少誤判[!DNL New Relic]警示的數量，並允許嚴格設定監控與警示以獲得前端效能。 New Relic會接收分別的應用程式資料檔案，其應用程式名稱會附加至`Adminhtml`和前端字元。 例如： `MyStore_Adminhtml`

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

## 步驟4：為[!DNL New Relic]報告啟用Cron

1. 展開![區段的](../assets/icon-display-expand.png)擴充選擇器&#x200B;**[!UICONTROL Cron]**。

   ![New Relic Cron設定](./assets/new-relic-reporting-cron.png){width="600"}

1. 將&#x200B;**[!UICONTROL Enable Cron]**&#x200B;設為`Yes`。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

## [!DNL New Relic]個查詢

[!DNL New Relic Insights]資料是以以[!DNL New Relic Query Language] (NRQL)撰寫的陳述式為基礎，以及您可能包含的任何自訂引數。 資料可從臨機查詢傳回，或透過儲存至儀表板的查詢傳回。 若要深入瞭解，請參閱[檔案中的][6]NRQL參考[!DNL New Relic]。

### 管理事件

#### 作用中的管理員使用者

傳回作用中管理員使用者的數目。

    SELECT uniqueCount(AdminId)
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39; SINCE 15分鐘前

#### 目前有效的管理員使用者

傳回作用中管理員使用者的名稱。

    SELECT uniques(AdminName)
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39; SINCE 15分鐘前

#### 最近的管理活動

傳回最近的管理員動作數。

    從交易選取count(AdminId)
    WHERE appName =&#39;&lt;your_app_name>&#39; FACET AdminName自1天前
    

#### 最新的管理員活動

傳回有關最近管理員動作的詳細資訊，包括管理員使用者名稱、持續時間和應用程式名稱。

    從交易選取AdminName、持續時間、名稱
    其中appName=&#39;&lt;your_app_name>&#39;和AdminName不是NULL
    和AdminName！
    = &#39;N/A&#39;限制50

### Cron事件

#### 類別計數

傳回指定時段內依類別分類的應用程式事件數目。

    從Cron
    選取AVERAGE(CatalogCategoryCount)
    其中CatalogCategoryCount不是NULL
    且appName = &#39;&lt;your_app_name>&#39;時序2分鐘

#### 目前目錄計數

傳回指定時段內依類別分類之目錄中的應用程式事件平均數目。

    從Cron
    選取AVERAGE(CatalogCategoryCount)
    其中CatalogCategoryCount不是NULL
    且CatalogCategoryCount > 0
    且appName = &#39;&lt;your_app_name>&#39;自2分鐘前限制1

#### 使用中的產品

傳回指定時段內依產品分類的應用程式事件數。

    從Cron
    選取AVERAGE(CatalogProductActiveCount)
    其中CatalogProductActiveCount不是NULL
    且appName = &#39;&lt;your_app_name>&#39;時序2分鐘

#### 使用中的產品計數

傳回指定時段內依產品區分之使用中應用程式事件的平均數目。

    從Cron
    選取AVERAGE(CatalogProductActiveCount)
    其中CatalogProductActiveCount不是NULL
    且CatalogProductActiveCount > 0
    AND appName = &#39;&lt;your_app_name>&#39;自2分鐘前限制1

#### 可設定的產品

傳回指定時段內可設定產品之應用程式事件的平均數目。

    從Cron
    選取AVERAGE(CatalogProductConfigurableCount)
    其中CatalogProductConfigurableCount不是NULL
    且appName = &#39;&lt;your_app_name>&#39;時序2分鐘

#### 可設定的產品計數

傳回指定時段內可設定產品所執行之應用程式事件的平均數目。

    從Cron
    選取AVERAGE(CatalogProductConfigurableCount)
    其中CatalogProductConfigurableCount不是NULL
    且CatalogProductConfigurableCount > 0
    AND appName = &#39;&lt;your_app_name>&#39;自2分鐘前限制1

#### 產品計數（全部）

傳回所有產品的應用程式事件總數。

從Cron    選取
    AVERAGE(CatalogProductCount)
    其中CatalogProductCount不是NULL
    且appName = &#39;&lt;your_app_name>&#39;時序2分鐘

#### 目前產品計數（全部）

傳回指定時段內所有產品的平均應用程式事件數。

    從Cron
    選取AVERAGE(CatalogProductCount)
    其中CatalogProductCount不是NULL
    且CatalogProductCount > 0
    且appName = &#39;&lt;your_app_name>&#39;自2分鐘前限制1

#### 客戶計數

傳回依客戶分類的應用程式事件平均數量。

從Cron    選取
    AVERAGE(CustomerCount)
    其中CustomerCount不是NULL
    且CustomerCount > 0&lt;
    且appName = &#39;&lt;your_app_name>&#39;時序2分鐘

#### 目前客戶計數

傳回指定時段內的平均客戶數。

從Cron    選取
    AVERAGE(CustomerCount)
    其中CustomerCount不是NULL
    且CustomerCount > 0
    且appName = &#39;&lt;your_app_name>&#39;自2分鐘前限制1

#### 模組狀態

傳回指定時段內啟用、停用或安裝應用程式模組的平均次數。

    SELECT average(ModulesDisabled)， average(ModulesEnabled)， average
    (ModulesInstalled)
    FROM Cron&lt;
    WHERE appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2分鐘

#### 目前模組狀態

傳回指定時段內啟用、停用或安裝模組的平均次數。

    SELECT average(ModulesDisabled)， average(ModulesEnabled)， average
    (ModulesInstalled)
    FROM Cron
    WHERE appName = &#39;&lt;your_app_name>&#39; SINCE 2分鐘前LIMIT 1

#### 網站和商店計數

傳回指定時段內依網站和商店分類的應用程式事件平均數量。

    SELECT average(StoreViewCount)， average(WebsiteCount)
    FROM Cron
    WHERE appName = &#39;&amp;amp；lt；your_app_name&amp;amp；gt；&#39; TIMESERIES 2分鐘

#### 目前的網站和商店計數

傳回指定時段內目前應用程式事件的平均數目。

    SELECT average(StoreViewCount)， average(WebsiteCount)
    FROM Cron
    WHERE appName = &#39;&lt;your_app_name>&#39; SINCE 2分鐘前LIMIT 1

#### Cron — 來自事件的所有資料

傳回所有應用程式事件資料。

    從Cron
    選取*
    其中appName = &#39;&lt;your_app_name>&#39;

### 客戶

#### 作用中客戶計數

傳回指定時段內的作用中客戶數目。

    SELECT uniqueCount(CustomerId)
    FROM Transaction
    WHERE appName = &#39;&lt;your_app_name>&#39; SINCE 15分鐘前

#### 活躍客戶

傳回指定時段內活躍客戶的名稱。

    SELECT uniques(CustomerName)
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39; SINCE 15分鐘前

#### 主要客戶

傳回指定時段內排名最前的客戶。

    SELECT count(CustomerId)
    FROM Transaction
    WHERE appName = &#39;&lt;your_app_name>&#39; FACET CustomerName自1天前

#### 最近的管理活動

傳回最近活動的已定義記錄數，包括客戶名稱和造訪持續時間。

    從交易選取CustomerName、持續時間、名稱
    其中appName=&#39;&lt;your_app_name>&#39;
    且CustomerName不是NULL
    且CustomerName！
    = &#39;N/A&#39;限制50

### 訂購

#### 訂購次數

傳回指定時段內的訂單數。

從1天前開始的    SELECT count(Order)
    FROM交易

#### 訂單值總計

傳回指定時段內訂購的行專案總數。

    SELECT sum(orderValue)
    FROM交易自1天前

#### 訂購的行專案總數

傳回指定時段內訂購的行專案總數。

    SELECT sum(lineItemCount)
    FROM交易自1天前


[1]: https://newrelic.com/
[3]: https://docs.newrelic.com/docs/agents/php-agent/getting-started/new-relic-php
[4]: https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html
[5]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html
[6]: https://docs.newrelic.com/docs/insights/new-relic-insights/using-new-relic-query-language/nrql-reference
