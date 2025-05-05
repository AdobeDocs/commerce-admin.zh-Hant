---
title: '[!UICONTROL Sales Channels] &amp；gt； [!UICONTROL Global Settings]'
description: 檢閱Commerce管理員的[!UICONTROL Sales Channels] &amp；gt； [!UICONTROL Global Settings]頁面上的組態設定。
exl-id: 28a5ef4b-265e-457a-9480-96763785b5fd
feature: Configuration, Sales Channels
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---

# [!UICONTROL Sales Channels] > [!UICONTROL Global Settings]

{{config}}

安裝[[!DNL Amazon Sales Channel]](https://experienceleague.adobe.com/docs/commerce-channels/amazon/getting-started/install.html?lang=zh-Hant)時，可以使用這些設定。

![Sales Channel設定](./assets/config-sales-channel-global-settings.png)<!-- zoom -->

| 欄位 | [領域](../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|-----|---------|------|
| [!UICONTROL Clear Log History] | 全域 | 選項：<br/><br/>**`Once Daily`**：選取此選項可每天清除一次您商店的活動歷史記錄。<br/><br/>**`Once Weekly`**：選取此選項可每週清除一次您商店的活動歷史記錄。<br/><br/>**`Once Monthly`**： （預設）選取此選項可每月清除一次您商店的活動歷史記錄。 |
| [!UICONTROL Background Tasks (CRON) Source] | 全域 | 選取「`Magento CRON`」以指定[!DNL Amazon Sales Channel]使用您的Commerce cron設定來決定與Amazon Seller Central的通訊和資料同步間隔。 |
| [!UICONTROL Enable Debug Logging] | 全域 | 選取`Enabled`以在需要疑難排解時收集其他同步處理資料。<br/><br/>此選項預設為停用，應該只在疑難排解需要時才啟用，因為持續記錄對效能有負面影響。 若啟用以進行疑難排解，則應在完成時停用此功能。 |
| [!UICONTROL Read-Only Mode] | 全域 | 選取`Enabled`以封鎖所有外寄狀態變更API要求。 在停用唯讀模式之前，可能會儲存變更，但不會傳送。 若要再次開始資料傳輸，請選取`Disabled`。<br/><br/>當資料庫移轉至執行個體的新復本時（在組態中儲存區的URL變更時偵測），會自動啟用唯讀模式。<br/><br/>這是設計用於生產執行個體的復本，例如&#x200B;_Staging_&#x200B;或&#x200B;_QA_，不應該用於生產執行個體。<br/><br/>**_注意&#x200B;_**：必須清除設定快取，才能啟用[!UICONTROL Read-Only Mode]。 |

{style="table-layout:auto"}
