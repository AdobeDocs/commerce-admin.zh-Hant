---
title: 支援工具
description: 瞭解您可用於識別系統中問題的支援工具。
exl-id: f67616e6-7879-4fd3-947a-16856f8447ba
source-git-commit: 97eeb733836f0336401664c5cfb3df2b9f2f2ccf
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 0%

---

# 支援工具

{{ee-feature}}

支援工具旨在識別您系統中的已知問題。 它們可在開發和最佳化過程中作為資源，並作為診斷工具，協助我們的支援團隊識別和解決問題。

## 資料收集器

資料收集器會收集系統相關資訊，供我們的支援團隊針對Adobe Commerce安裝問題進行疑難排解。 建立的備份需要幾分鐘才能完成，而且包含程式碼和資料庫傾印。 資料可匯出為CSV或Excel XML檔案。

![系統 — 資料收集器](./assets/data-collector.png){width="600" zoomable="yes"}

### 執行資料收集器

1. 在 _管理員_ 側欄，前往 **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL Data Collector]**.

1. 在右上角，按一下 **[!UICONTROL New Backup]**.

   產生備份需要幾分鐘的時間。 您可以按一下「 」，監控處理結果 **[!UICONTROL Refresh Status]**. 完成後，備份會顯示在 _[!UICONTROL Data Collector]_格線。

1. 若要檢視含有備份詳細資訊的記錄檔，請執行下列動作：

   - 在 _[!UICONTROL Action]_欄，選取&#x200B;**[!UICONTROL Show Log]**.

   - 按一下 **[!UICONTROL Back]** 以返回格線。

   ![資料收集器記錄](./assets/data-collector-log.png){width="600" zoomable="yes"}

### 匯出備份資料

1. 在第一欄中，選取要匯出之備份的核取方塊。

1. 使用 **[!UICONTROL Export]** 功能表以選擇匯出資料的格式。

   ![匯出格式](./assets/data-collector-export.png){width="600" zoomable="yes"}

1. 從網頁瀏覽器下載位置存取檔案，並 **[!UICONTROL Save]** it.

### 下載備份資料

產生備份後，您可以下載程式碼和資料庫資料的復本。

1. 在格線中尋找所需的備份實體。

1. 確定它有 `Complete` 狀態。

1. 按一下中的實體名稱 _[!UICONTROL Code Dump]_或_[!UICONTROL DB Dump]_ 欄。

下載程式應該會自動啟動。

## 刪除備份資料

1. 在 _管理員_ 側欄，前往 **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL Data Collector]**.

1. 尋找並選取要刪除的備份資料。

1. 在 _[!UICONTROL Action]_欄，按一下&#x200B;**[!UICONTROL Delete]**.

1. 若要確認動作，請按一下 **[!UICONTROL OK]**.

## 系統報表

系統報告工具可讓您定期取得系統的完整或部分快照，並儲存以供日後參考。 您可以比較程式碼開發週期之前和之後的效能設定，或伺服器設定的變更。 系統報告工具可大幅減少準備和提交「支援」開始調查所需資訊的時間。

從「系統報表」格線中，您可以檢視及下載現有報表、刪除報表及建立報表。

### 存取系統報告

在 _管理員_ 側欄，前往 **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.

![管理員 — 系統報表](./assets/reports.png){width="600" zoomable="yes"}

### 產生報表

1. 按一下 **[!UICONTROL New Report]**.

1. 在 **[!UICONTROL Groups]** 清單中，選取要納入報告中的每一組資訊。 預設會選取所有群組。

   ![系統報告 — 選取群組](./assets/report-create.png){width="600" zoomable="yes"}

1. 在右上角，按一下 **[!UICONTROL Create]**.

   視選取的報表型別數目而定，報表可能需要幾分鐘的時間才能產生。 報表準備就緒後，會顯示於網格頂端，並產生日期和時間。

### 檢視模組資訊

您可以找到有關已安裝模組的實用資訊。

**_若要檢視每個已安裝模組的報表資訊：_**

1. 在 _管理員_ 側欄，前往 **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.
1. 按一下 **[!UICONTROL New Report]**.
1. 選取 `Modules` 從 **[!UICONTROL Groups]** 清單。
1. 按一下 **[!UICONTROL Create]**.
1. 報表產生後，按一下 **[!UICONTROL Select]** 然後 **[!UICONTROL View]** 以檢視所有模組版本。
1. 按一下 **[!UICONTROL Download]** 以下載報表。

### 管理系統報表

在 **[!UICONTROL Action]** 欄中，選取下列其中一項：

- `View`  — 使用此函式來檢視報告的詳細資料。
- `Delete`  — 使用此函式從清單中刪除產生的報告。
- `Download`  — 使用此函式將報表儲存為HTML檔案。

### 檢視系統報告詳細資訊

1. 對於您需要的報告，請選取 **[!UICONTROL View]** 在 _[!UICONTROL Actions]_欄。

1. 在左側面板中，展開 ![展開選擇器](../assets/icon-display-expand.png) 報表的每個區段來檢視詳細資訊。

   ![一般系統報告資訊](./assets/report-information.png){width="600" zoomable="yes"}

### 可用的系統報告

| 報表群組 | 包含的資訊 |
| ------------ | -------------------- |
| [!UICONTROL General] | Adobe Commerce版本<br>資料計數<br>快取狀態<br>索引狀態 |
| [!UICONTROL Environment] | 環境資訊<br>MySQL狀態 |
| [!UICONTROL Data] | 依URL索引鍵複製類別<br>依URL索引鍵複製產品<br>依SKU複製產品<br>依遞增Id復制訂單<br>依電子郵件複製使用者<br>損毀的類別資料 |
| [!UICONTROL Modules] | 自訂模組清單<br>已停用的模組清單<br>所有模組清單 |
| [!UICONTROL Configuration] | 設定<br>資料來源 `app/etc/env.php`<br>送貨方法<br>付款方法<br>付款功能矩陣 |
| [!UICONTROL Logs] | 記錄檔<br>主要系統訊息<br>今日最受歡迎的系統訊息<br>熱門偵錯訊息<br>今天熱門的除錯訊息<br>最常見的例外訊息<br>今日最常見的例外訊息 |
| [!UICONTROL Attributes] | 使用者定義的EAV屬性<br>新EAV屬性<br>實體型別<br>所有EAV屬性<br>類別EAV屬性<br>產品EAV屬性<br>客戶EAV屬性<br>客戶地址EAV屬性<br>RMA料號EAV屬性 |
| [!UICONTROL Events] | 自訂全域事件<br>自訂管理事件<br>自訂前端事件<br>自訂檔案事件<br>自訂Crontab事件<br>自訂REST事件<br>自訂SOAP事件<br>核心全球活動<br>核心管理事件<br>核心前端事件<br>核心檔案事件<br>核心Crontab事件<br>核心REST事件<br>核心SOAP事件<br>所有全域事件<br>所有管理員事件<br>所有前端事件<br>所有檔案事件<br>所有REST事件<br>所有SOAP事件<br>所有Crontab事件 |
| [!UICONTROL Cron] | 依狀態代碼的Cron排程<br>依工作代碼的Cron排程<br>Cron排程佇列中的錯誤<br>Cron排程清單<br>自訂全域Cron工作<br>自訂可設定的Cron作業<br>核心全域Cron工作<br>核心可設定的Cron工作<br>所有全域Cron工作<br>所有可設定的Cron工作 |
| [!UICONTROL Design] | 管理HTML主題清單<br>前端主題清單 |
| [!UICONTROL Stores] | 網站樹狀結構<br>網站清單<br>存放區清單<br>存放區檢視清單 |
| OMS聯結器&#x200B;<br>_（透過OMS整合顯示）_ | 聯結器版本<br>聯結器監視<br>訊息處理結果 |

{style="table-layout:auto"}
