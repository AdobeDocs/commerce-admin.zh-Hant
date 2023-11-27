---
title: 出貨
description: 瞭解如何建立商業發票的出貨記錄，以及如何取消出貨。
exl-id: 6df83549-ba38-43f7-aab1-dbf3f6b89d74
feature: Shipping/Delivery, Invoices
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '943'
ht-degree: 1%

---

# 出貨

此 _[!UICONTROL Shipments]_grid會列出已準備出貨的所有商業發票的出貨記錄。 當訂單為下列情況時，可以產生出貨記錄 [已開發票](invoices.md) 或更新版本。

Adobe Commerce和Magento Open Source支援部分及完整訂單出貨，並提供其他選項，請參閱 [Inventory management](../inventory-management/introduction.md) 和協力廠商擴充功能整合。

![出貨格線](./assets/shipments.png){width="600" zoomable="yes"}

## 欄說明

| 欄或控制項 | 說明 |
|--- |--- |
| [!UICONTROL Select] | 選取每個要接受動作之報價的核取方塊，或使用欄標題中的選取控制項。 選項： `Select All` / `Deselect All` |
| [!UICONTROL Shipment] | 第一次儲存新出貨時指派的唯一連續編號 |
| [!UICONTROL Ship Date] | 送貨日期 |
| [!UICONTROL Order] | 訂單的唯一編號 |
| [!UICONTROL Order Date] | 下訂單的日期和時間 |
| [!UICONTROL Ship-to Name] | 訂單的收貨人名稱 |
| [!UICONTROL Total Quantity] | 要出貨的料號總數量 |
| [!UICONTROL Action] | 檢視以編輯模式開啟出貨 |

{style="table-layout:auto"}

其他欄：

| 欄 | 說明 |
|--- |--- |
| [!UICONTROL Order Status] | 指示訂單狀態 |
| [!UICONTROL Purchased From] | 表示下訂單的網站、商店和商店檢視 |
| [!UICONTROL Customer Name] | 下訂單的客戶或採購員名稱 |
| [!UICONTROL Email] | 註冊客戶的電子郵件地址 |
| [!UICONTROL Customer Group] | 將客戶指派給之客戶群組或共用目錄的名稱 |
| [!UICONTROL Billing Address] | 下訂單的客戶或採購員名稱 |
| [!UICONTROL Shipping Address] | 訂單的收貨人名稱 |
| [!UICONTROL Payment Method] | 用於訂單的付款方式 |
| [!UICONTROL Shipping Information] | 要用來出貨訂單的方法 |

{style="table-layout:auto"}

## 建立出貨

下列指示會逐步引導您進行在Adobe Commerce或Magento Open Source中建立出貨的程式。 如果您已啟用Inventory management，則可能需要檢閱 [建立多來源出貨](../inventory-management/shipments-create.md) 並選取來源（或地點）以及每個明細行料號要傳送的數量。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. 在格線中尋找順序並開啟。

1. 如果訂單已付款、已開立商業發票且準備出貨，請按一下 **[!UICONTROL Ship]**.

   出貨頂端的區段包含銷售訂單的名稱、地址及付款資訊。

1. 使用下列各節中的指示，完成出貨表單的每個區段。

### [!UICONTROL Items to Ship]

針對訂單中的每個明細專案，修改 **[!UICONTROL Qty to Ship]** 視需要。

### [!UICONTROL Shipping Information]

**方法1：** 使用訂單頁面

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. 在 **[!UICONTROL Action]** 欄，按一下 **[!UICONTROL View]**.

1. 按一下 **[!UICONTROL Ship]**.

1. 向下捲動至 _[!UICONTROL Payment & Shipping Method]_封鎖並按一下&#x200B;**[!UICONTROL Add Tracking Number]**.

1. 設定 **[!UICONTROL Carrier]**：

   - `Custom Value`
   - `DHL`
   - `Federal Express`
   - `United Parcel Service`
   - `United States Postal Service`

1. 若要追蹤出貨，請輸入 **[!UICONTROL Title]** 和 **[!UICONTROL Number]** .

**方法2：** 使用出貨頁面

只有在訂單出貨已從訂單頁面建立時，才允許使用此方法。
您可以使用直接出貨頁面，視需要修改出貨與追蹤資訊：

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. 在編輯模式中尋找並開啟出貨。

1. 向下捲動至 _[!UICONTROL Payment & Shipping Method]_區塊。

1. 選取 **[!UICONTROL Carrier]**.

1. 輸入 **[!UICONTROL Title]** 適用於此套件。

1. 輸入追蹤 **[!UICONTROL Number]**.

1. 按一下 **[!UICONTROL Add]**.

1. 若要傳送包含追蹤資訊的電子郵件給客戶，請按一下 **[!UICONTROL Send Tracking Information]**，並確認動作。

   若要追蹤任何出貨地點，請在編輯模式中開啟所需的出貨，然後按一下 **[!UICONTROL Track this shipment]**.

   ![送貨與追蹤資訊](./assets/tracking-information.png){width="600" zoomable="yes"}

### 按鈕

| 按鈕 | 說明 |
|--- |--- |
| **[!UICONTROL Back]** | 關閉「新增出貨」表單，並退回訂單 |
| **[!UICONTROL Submit Shipment]** | 新增訂單的出貨。 |
| **[!UICONTROL Reset]** | 將所有欄位恢復為原始值。 |

{style="table-layout:auto"}

### 送貨註解

1. 輸入 **註解** 運送（如有需要）。

1. 當出貨準備就緒時，按一下 **提交出貨**.

## 設定出貨的註解

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在 _[!UICONTROL Sales]_，選取&#x200B;**[!UICONTROL Sales Email]**.

1. 展開 **出貨註解** 並視需要修改設定：

   ![出貨註解設定](../configuration-reference/sales/assets/sales-emails-shipment-comments.png){width="600" zoomable="yes"}

   - 此 **[!UICONTROL Enabled]** 選項已設為 `Yes` 根據預設，這表示在輸入送貨註解時，會將電子郵件傳送給客戶。

   - 的 **[!UICONTROL Shipment Comment Email Sender]**，選取寄出附註電子郵件的寄件者。 預設提供五個電子郵件地址。

   - 的 **[!UICONTROL Shipment Comment Email Template]**，根據您的需求選取範本或選取預設選項。

   - 的 **[!UICONTROL Shipment Comment Email Template for Guests]**，選擇您的商店中沒有帳戶的客戶所使用的範本。

   - 的 **[!UICONTROL Shipment Comment Email Copy To]**，輸入電子郵件地址，以傳送出貨評論電子郵件副本。 請使用逗號分隔多個電子郵件地址。

   - 的 **[!UICONTROL Shipment Comment Email Copy Method]**，選取 `bcc` （密件副本）或 `separate email copy` 根據您偏好的方法。

1. 按一下 **[!UICONTROL Save Config]**.

## 取消出貨

在出貨分派給承運商之前，只要承運商支援取消，就可以開啟訂單並瀏覽至出貨來取消出貨。 有些電信業者在預訂後會限制或限製取消。 例如，UPS允許取消，但需要在出貨預訂後24小時等候。 如果取消出貨，則無法迴轉取消。 唯一的補救辦法是重新建立訂單。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. 在格線中尋找順序。

1. 在 _動作_ 欄，選擇 **[!UICONTROL View]**.

1. 在左側面板中，選擇 **[!UICONTROL Shipments]**.

   如果可以取消出貨， _[!UICONTROL Cancel Shipment]_會在頂端按鈕列顯示為選項。

1. 按一下 **[!UICONTROL Cancel Shipment]**.

1. 提示確認時，按一下 **[!UICONTROL OK]**.

出貨的狀態變更為 `Canceled`. 若承運商不支援取消，則會出現錯誤訊息，說明無法取消出貨的原因。

## 出貨欄位說明

### [!UICONTROL Shipping Information]

| 欄位 | 說明 |
|-----|-----------|
| [!UICONTROL Carrier] | 所選電信業者的名稱 |
| [!UICONTROL Title] | 電信業者指派給封裝的描述性名稱。 |
| [!UICONTROL Number] | 指派給封裝的連結追蹤編號。 |
| [!UICONTROL Action] | ![垃圾桶圖示](../assets/icon-delete-trashcan-solid.png)  — 從出貨記錄刪除包裹資訊。 |
| [!UICONTROL Add] | 新增另一個套件至出貨。 |

{style="table-layout:auto"}

### [!UICONTROL Route Information]

| 欄位 | 說明 |
|-----|-----------|
| [!UICONTROL Origin Location] | 顯示可用位置的清單。 |
| [!UICONTROL International] | 如果勾選，會將出貨識別為國際出貨。 |

{style="table-layout:auto"}

### [!UICONTROL Items Ordered]

| 欄位 | 說明 |
|-----|-----------|
| [!UICONTROL Description] | 專案的說明。 |
| [!UICONTROL SKU] | 料號的庫存單位。 |
| [!UICONTROL Weight] | 專案的重量。 |
| [!UICONTROL Qty Ordered] | 訂購的料號數量。 |
| [!UICONTROL Qty Shipped] | 已出貨的料號數量。 |
| [!UICONTROL Qty Packed] | 此封裝中包含的專案數。 |

{style="table-layout:auto"}

### [!UICONTROL Shipment Comments]

| 欄位 | 說明 |
|-----|-----------|
| [!UICONTROL Comments] | 有關出貨的註解供內部使用。 |

{style="table-layout:auto"}

### [!UICONTROL Documentation]

| 欄位 | 說明 |
|-----|-----------|
| [!UICONTROL Package Label] | **PNG**  — 下載出貨包裝標籤。 尺寸：A6 （105 x 148毫米；4.1 x 5.6英吋） |

{style="table-layout:auto"}
