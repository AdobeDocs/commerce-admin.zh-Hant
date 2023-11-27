---
title: 系統備份
description: 瞭解如何建立和排程系統備份，包括檔案系統、資料庫和媒體檔案。
exl-id: 3a9655c1-c124-42be-a487-b31404dada90
feature: System, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# 系統備份

Adobe Commerce和Magento Open Source可讓您備份系統的不同部分（例如檔案系統、資料庫和媒體檔案），並自動回覆。 每個備份的記錄會顯示在上的網格中 _備份_ 頁面。 從清單中刪除記錄也會刪除已封存的檔案。 資料庫備份檔案會使用GZ格式壓縮。 對於系統備份、資料庫和媒體備份，會使用TGZ格式。 您應先限制對備份工具的存取權，並在安裝擴充功能和更新之前進行備份，此為最佳作法。

- **限制存取備份工具。** 可以透過設定來限制對備份和復原管理工具的存取 [使用者角色](permissions-user-roles.md) 用於備份與回覆資源。 若要限制存取，請取消選取對應的核取方塊。 若要授與回覆資源的存取權，您也必須授與備份資源的存取權。

- **安裝擴充功能和更新之前請先備份。** 安裝擴充功能或更新前，請務必執行備份。

{{$include /help/_includes/backups-note.md}}

## 啟用及排程備份

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Advanced]** 並選擇 **[!UICONTROL System]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Backup Settings]**.

1. 設定 **[!UICONTROL Enabled Schedule Backup]** 至 `Yes`.

1. 若要排程自動召喚，請設定排程選項：

   - 設定 **[!UICONTROL Enabled Schedule Backup]** 至 `Yes`.
   - 設定 **[!UICONTROL Scheduled Backup Type]** 以排定的間隔執行的備份型別。
   - 設定 **[!UICONTROL Start Time]** 執行備份作業的時間。
   - 設定 **[!UICONTROL Frequency]** 至 `Daily`， `Weekly`，或 `Monthly`.
   - 設定 **[!UICONTROL Maintenance Mode]** 至 `Yes`.

   ![進階設定 — 備份](../configuration-reference/advanced/assets/system-scheduled-backup-settings.png){width="600" zoomable="yes"}

1. 完成後，按一下 **[!UICONTROL Save Config]**.

## 建立備份

1. 在 _管理員_ 側欄，前往 **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Backups]**.

1. 在右上角，按一下您要建立的備份型別：

   - **[!UICONTROL System Backup]**  — 建立資料庫和檔案系統的完整備份。 在此過程中，您可以選擇將媒體資料夾包含在備份中。

   - **[!UICONTROL Database and Media Backup]**  — 建立資料庫和媒體資料夾的備份。

   - **[!UICONTROL Database Backup]**  — 建立資料庫的備份。

   ![系統工具 — 備份](./assets/tools-backups.png){width="600" zoomable="yes"}

1. 若要在備份期間將存放區置於維護模式，請選取核取方塊。

   備份完成後，維護模式會自動關閉。

1. 對於系統備份，請選取 **[!UICONTROL Include Media folder to System Backup]** 核取方塊以包含媒體資料夾。

1. 出現提示時，請確認動作。


