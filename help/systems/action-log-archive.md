---
title: 動作記錄存檔
description: 瞭解如何設定和檢視管理員動作記錄封存。
exl-id: a839f1c6-b5e2-4881-bfaa-267e47585441
feature: Logs, Configuration
TQID: https://experienceleague.adobe.com/xgyeoO5XJFZPopM9bsIn2oOtrxl4fyuEY2du5ryXeTY
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 160
ht-degree: 0%

---

# 動作記錄存檔

{{ee-feature}}

管理員[動作](action-log.md)封存會列出伺服器上儲存的CSV記錄檔。 在設定中，您可以指定記錄專案的儲存時間以及封存頻率。 依預設，檔案名稱包含ISO格式的目前日期： `yyyyMMddHH`

>[!NOTE]
>
>記錄檔封存需要設定[cron工作](cron.md)。

## 設定日誌封存

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Advanced]**&#x200B;並選擇&#x200B;**[!UICONTROL System]**。

1. 展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Admin Actions Log Archiving]**&#x200B;區段並設定下列選項：

   - **[!UICONTROL Log Entry Lifetime, Days]** — 輸入在移除記錄專案之前，要在資料庫中保留記錄專案的天數。
   - **[!UICONTROL Log Archiving Frequency]** — 設定為`Daily`、`Weekly`或`Monthly`。

   ![進階設定 — 管理動作記錄檔封存](../configuration-reference/advanced/assets/system-admin-actions-log-archiving.png){width="600" zoomable="yes"}

   如需組態設定的詳細清單，請參閱&#x200B;_組態參考_&#x200B;中的[管理動作記錄檔封存](../configuration-reference/advanced/system.md)。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

## 檢視封存

在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL System]** > _[!UICONTROL Actions Logs]_>**[!UICONTROL Archive]**。

![動作記錄檔封存](./assets/action-log-archive.png){width="600" zoomable="yes"}
