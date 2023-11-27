---
title: 動作記錄存檔
description: 瞭解如何設定和檢視管理員動作記錄封存。
exl-id: a839f1c6-b5e2-4881-bfaa-267e47585441
feature: Logs, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# 動作記錄存檔

{{ee-feature}}

管理員 [動作](action-log.md) 封存會列出伺服器上儲存的CSV記錄檔。 在設定中，您可以指定記錄專案的儲存時間以及封存頻率。 依預設，檔案名稱包含ISO格式的目前日期：  `yyyyMMddHH`

>[!NOTE]
>
>記錄檔封存需要 [cron工作](cron.md) 進行設定。

## 設定日誌封存

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Advanced]** 並選擇 **[!UICONTROL System]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Admin Actions Log Archiving]** 並設定下列選項：

   - **[!UICONTROL Log Entry Lifetime, Days]**  — 輸入在移除記錄專案之前，要在資料庫中保留記錄專案的天數。
   - **[!UICONTROL Log Archiving Frequency]**  — 設為 `Daily`， `Weekly`，或 `Monthly`.

   ![進階設定 — 管理動作記錄封存](../configuration-reference/advanced/assets/system-admin-actions-log-archiving.png){width="600" zoomable="yes"}

   如需組態設定的詳細清單，請參閱 [管理動作記錄檔封存](../configuration-reference/advanced/system.md) 在 _設定參考_.

1. 完成後，按一下 **[!UICONTROL Save Config]**.

## 檢視封存

在 _管理員_ 側欄，前往 **[!UICONTROL System]** > _[!UICONTROL Actions Logs]_>**[!UICONTROL Archive]**.

![動作記錄存檔](./assets/action-log-archive.png){width="600" zoomable="yes"}
