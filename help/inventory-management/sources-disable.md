---
title: 停用存貨來源
description: 瞭解如何停用來源及修改資訊，包括位置和聯絡點。
exl-id: 3fcbfa3c-8bb7-4e08-a395-9760bbd69f04
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# 停用來源

為確保所有訂單資料都保留在[!DNL Commerce]中，無法刪除來源。 來源、訂單及出貨會直接連結。 您可以停用來源並修改資訊，包括位置和聯絡點。

根據您位置的狀態，您可能想要停用來源。 停用的來源會保留每個存貨與產品的所有指派，但不會存取存貨與訂單。

當來源停用時：

- [!DNL Inventory Management]會忽略且不列出出貨或訂單處理的來源。
- 庫存不會從來源存取彙總存貨總計的存貨數量。
- 訂單出貨無法指定至停用的地點。

您無法停用預設Source。 [!DNL Commerce]會將此來源用於所有新匯入的產品、套件組合產品以及協力廠商系統支援。 您可以隨時啟用或停用自訂來源。

將來源設定為`disabled`有助於下列情況：

- 新增商店或倉儲 — 當您開啟新商店或讓新倉庫與出貨地點上線時，請新增來源專案，以使用匯入設定產品存貨，並連線至潛在存貨。
- 季節性出貨 — 假日是一年中的繁忙時段。 您可能只想限制從特定出貨地點（例如倉庫）出貨，以保持實體地點存貨充足，並專注於當地購物者。 或者，您可以在有限的時間內新增出貨地點，以處理較高的銷售和傳入訂單。
- 關閉地點 — 關閉要移轉至新設施或永久移轉的地點時，請停用以停止該地點的新出貨。

## 停用一或多個自訂來源

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**。

1. 勾選您要停用的每個已啟用自訂來源的核取方塊。

1. 按一下左上角的&#x200B;_動作_&#x200B;功能表，然後選擇&#x200B;**[!UICONTROL Disable]**。

   ![[!DNL Inventory Management]來源 — 動作功能表](assets/inventory-source-disable.png){width="600" zoomable="yes"}

1. 在確認對話方塊中，按一下&#x200B;**[!UICONTROL OK]**。

## 啟用或停用單一自訂來源

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**。

1. 找到自訂來源並按一下&#x200B;**[!UICONTROL Edit]**。

1. 展開![擴充選擇器](../assets/icon-display-expand.png) _一般_&#x200B;區段並變更&#x200B;**[!UICONTROL Is Enabled]**：

   | 選項 | 說明 |
   | ----- | ----- |
   | `Yes` | Source已啟用。 數量新增至「可銷售數量」。 出貨訂單時，來源會以目前數量列出。 Source選擇演演算法會檢查其送貨來源。 |
   | `No` | Source已停用。 數量不會新增至「可銷售數量」。 出貨訂單時，來源不會列出。 送貨選項會略過此來源。 |

1. 按一下&#x200B;**[!UICONTROL Save and Close]**。
