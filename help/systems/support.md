---
title: 支援工具
description: 瞭解您可用於識別系統中問題的支援工具。
exl-id: f67616e6-7879-4fd3-947a-16856f8447ba
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hant/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"
source-git-commit: addde8c3e41b641712f5b08107c1d68b40cd4159
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 0%

---

# 支援工具

{{ee-feature}}

支援工具旨在識別您系統中的已知問題。 它們可在開發和最佳化過程中作為資源，並作為診斷工具，協助我們的支援團隊識別和解決問題。

## 系統報表

系統報告工具可讓您定期取得系統的完整或部分快照，並儲存以供日後參考。 您可以比較程式碼開發週期之前和之後的效能設定，或伺服器設定的變更。 系統報告工具可大幅減少準備和提交「支援」開始調查所需資訊的時間。

從「系統報表」格線中，您可以檢視及下載現有報表、刪除報表及建立報表。

### 存取系統報告

在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**。

![管理員 — 系統報告](./assets/reports.png){width="600" zoomable="yes"}

### 產生報表

1. 按一下&#x200B;**[!UICONTROL New Report]**。

1. 在&#x200B;**[!UICONTROL Groups]**&#x200B;清單中，選取要納入報告中的每一組資訊。 預設會選取所有群組。

   ![系統報告 — 選取群組](./assets/report-create.png){width="600" zoomable="yes"}

1. 按一下右上角的&#x200B;**[!UICONTROL Create]**。

   視選取的報表型別數目而定，報表可能需要幾分鐘的時間才能產生。 報表準備就緒後，會顯示於網格頂端，並產生日期和時間。

### 檢視模組資訊

您可以找到有關已安裝模組的實用資訊。

**_若要檢視每個已安裝模組的報表資訊：_**

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**。
1. 按一下&#x200B;**[!UICONTROL New Report]**。
1. 從&#x200B;**[!UICONTROL Groups]**&#x200B;清單中選取`Modules`。
1. 按一下&#x200B;**[!UICONTROL Create]**。
1. 報表產生後，按一下&#x200B;**[!UICONTROL Select]**，然後按&#x200B;**[!UICONTROL View]**&#x200B;檢視所有模組版本。
1. 按一下&#x200B;**[!UICONTROL Download]**&#x200B;下載報表。

### 管理系統報表

在網格的&#x200B;**[!UICONTROL Action]**&#x200B;欄中，選取下列其中一項：

- `View` — 使用此函式來檢視報告的詳細資料。
- `Delete` — 使用此函式從清單中刪除產生的報告。
- `Download` — 使用此函式將報表儲存為HTML檔案。

### 檢視系統報告詳細資訊

1. 對於您需要的報表，請在&#x200B;_[!UICONTROL Actions]_&#x200B;欄中選取&#x200B;**[!UICONTROL View]**。

1. 在左側面板中，展開報表的每個區段![展開選取器](../assets/icon-display-expand.png)以檢視詳細資料。

   ![一般系統報告資訊](./assets/report-information.png){width="600" zoomable="yes"}

### 可用的系統報告

| 報表群組 | 包含的資訊 |
| ------------ | -------------------- |
| [!UICONTROL General] | Adobe Commerce版本<br>資料計數<br>快取狀態<br>索引狀態 |
| [!UICONTROL Environment] | 環境資訊<br>MySQL狀態 |
| [!UICONTROL Data] | 依URL索引鍵重複類別<br>依URL索引鍵重複產品<br>依SKU重複產品<br>依遞增識別碼重複訂單<br>依電子郵件重複使用者<br>損毀的類別資料 |
| [!UICONTROL Modules] | 自訂模組清單<br>已停用的模組清單<br>所有模組清單 |
| [!UICONTROL Configuration] | 設定<br>來自`app/etc/env.php`<br>送貨方法<br>付款方法<br>付款功能對照表的資料 |
| [!UICONTROL Logs] | 記錄檔<br>常用系統訊息<br>今天常用系統訊息<br>常用偵錯訊息<br>今天常用偵錯訊息<br>常用例外訊息<br>今天常用例外訊息 |
| [!UICONTROL Attributes] | 使用者定義的EAV屬性<br>新的EAV屬性<br>實體型別<br>所有EAV屬性<br>類別EAV屬性<br>產品EAV屬性<br>客戶EAV屬性<br>客戶地址EAV屬性<br>RMA專案EAV屬性 |
| [!UICONTROL Events] | 自訂全域事件<br>自訂管理員事件<br>自訂前端事件<br>自訂檔案事件<br>自訂Crontab事件<br>自訂REST事件<br>自訂SOAP事件<br>核心全域事件<br>核心管理員事件<br>核心前端事件<br>核心檔案事件<br>核心Crontab事件<br>核心REST事件<br>核心SOAP事件<br>所有全域事件<br>所有管理員事件<br>所有前端事件<br>所有Doc事件<br>所有REST事件<br>所有SOAP事件<br>所有Crontab事件 |
| [!UICONTROL Cron] | 依狀態碼的Cron排程<br>依工作碼的Cron排程<br>Cron排程佇列中的錯誤<br>Cron排程清單<br>自訂全域Cron工作<br>可自訂設定的Cron工作<br>核心全域Cron工作<br>可設定的核心Cron工作<br>所有全域Cron工作<br>所有可設定的Cron工作 |
| [!UICONTROL Design] | Adminhtml主題清單<br>前端主題清單 |
| [!UICONTROL Stores] | 網站樹狀結構<br>網站清單<br>存放區清單<br>存放區檢視清單 |
| OMS聯結器&#x200B;<br>_（與OMS整合一起顯示）_ | 聯結器版本<br>聯結器監視<br>訊息處理結果 |

{style="table-layout:auto"}
