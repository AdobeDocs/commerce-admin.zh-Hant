---
title: 傳回
description: 瞭解退貨工作流程及核發退貨授權。
exl-id: 9dde0360-aa99-4fc4-92ff-976d9874ffec
feature: Returns
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 0%

---

# 傳回

A _退貨商品授權_ (RMA)可授與要求退回料號以進行更換或退款的客戶。 通常客戶會聯絡商家要求退款。 如果核准，則會指派唯一的RMA編號，以識別傳回的產品。 在設定中，您可以為所有產品啟用RMA，或僅允許特定產品使用RMA。 此 _[!UICONTROL Returns]_grid會列出目前退回的商品請求(RMA)，並用來輸入新的退回請求。

![傳回格線](./assets/return.png){width="600" zoomable="yes"}

RMA可針對簡單、分組、可設定和套裝產品型別發行。 不過，RMA不適用於虛擬產品、可下載產品和禮品卡。

## 欄說明

| 欄 | 說明 |
|--- |--- |
| [!UICONTROL Select] | 選取要接受動作之傳回的核取方塊，或使用欄標題中的選取控制項。 選項： `Select All` / `Deselect All` / `Select Visible` / `Unselect Visible` |
| [!UICONTROL RMA] | 指派給每個傳回的唯一數值識別碼 |
| [!UICONTROL Requested] | 退貨的日期和時間 |
| [!UICONTROL Order] | 原始訂單的唯一編號 |
| [!UICONTROL Ordered] | 下訂單的日期和時間 |
| [!UICONTROL Customer] | 下訂單的客戶或採購員名稱 |
| [!UICONTROL Status] | 傳回狀態。 選項： `Pending` / `Authorized` / `Partially Authorized` / `Approved` / `Rejected` / `Processed and Closed` / `Closed` |
| [!UICONTROL Action] | **[!UICONTROL View]** 在編輯模式中開啟傳回。 |

{style="table-layout:auto"}

## RMA與退貨工作流程

1. **接收要求**  — 如果 [已啟用](rma-configure.md#enable-rmas-for-your-store) 對於店面，註冊客戶和來賓都可以要求RMA。 您也可以 [在管理員中提交RMA請求](#create-a-return-request-in-the-admin).

2. **RMA已核發**  — 考慮請求後，您可以部分、完整地授權它，或取消請求。 如果您授權退貨，並同意支付退貨出貨，則可以使用支援的承運商，從「管理員」建立出貨單。

3. **收到的商品及處理的產品退貨**  — 下列流程圖說明完成退貨處理的作業順序：

   ![產品退貨工作流程](./assets/workflow-customer-returns.png){width="500"}

## RMA狀態

在其生命週期中，退回商品授權(RMA)可以有許多指派的狀態（例如「擱置中」或「已授權」）。 RMA狀態會指出使用者或商家提出RMA要求的進度。

| 狀態 | 說明 |
|--- |--- |
| [!UICONTROL Pending] | 指定給RMA請求的初始狀態（當使用者在店面或商家在管理員中提出時）。 |
| [!UICONTROL Authorized] | 當所有要求的專案都由退貨管理員中的商家授權時，此狀態會指派給RMA。 |
| [!UICONTROL Partially Authorized] | 若有任何要求的專案遭拒，且其他產品已獲得授權，則會將此狀態指派給RMA。 |
| [!UICONTROL Denied] | 如果退貨的管理員中的商家拒絕所有要求的料號，則會將此狀態指派給RMA。 |
| [!UICONTROL Return Received] | 從使用者收到要求的專案時，商家會將此狀態指派給RMA。 |
| [!UICONTROL Return Partially Received] | 當要求的料號已部份退回，且部份料號被拒絕處理時，商家會將此狀態指派給RMA。 |
| [!UICONTROL Approved] | 當請求的料號被核准以進一步處理時，此狀態會由商家指定給RMA。 |
| [!UICONTROL Rejected] | 當要求的料號被拒絕以進一步處理時，此狀態會由商家指定給RMA。 |
| [!UICONTROL Processed and Closed] | 當所有請求料號都核准進行進一步處理時，此狀態會由商家指定給RMA。 |
| [!UICONTROL Closed] | 當要求的料號被拒絕以處理退貨時，此狀態會由商家指派給RMA。 |

{style="table-layout:auto"}

## 在Admin中建立傳回要求

商家可以從管理員代客戶建立退貨請求。 客戶可以 [建立退貨要求](rma-customer-experience.md) Adobe Commerce商店的店面。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Sales]** > **[!UICONTROL Returns]**.

1. 按一下 **[!UICONTROL New Return Request]**.

1. 若要建立退貨請求，請按一下訂單，並附上 `Complete` 狀態。

1. 在 _[!UICONTROL Return Information]_區段，選取&#x200B;**[!UICONTROL Return Items]**標籤。

1. 若要新增要傳回的專案，請按一下 **[!UICONTROL Add Items]**.

1. 選取所需產品的核取方塊，然後按一下 **[!UICONTROL Add Selected Product to returns]**.

1. 的 **[!UICONTROL Requested]**，輸入要傳回的專案數。

1. 設定 **[!UICONTROL Return Reason]** 變更為下列其中一項：

   - `Wrong Color`
   - `Wrong Size`
   - `Out of Service`
   - `Other`

   如果退貨的原因與列出的選擇不同，您可以輸入您自己的選擇 `Other` 選項。

1. 設定 **[!UICONTROL Item Condition]** 變更為下列其中一項：

   - `Unopened`
   - `Opened`
   - `Damaged`

1. 設定 **[!UICONTROL Resolution]** 變更為下列其中一項：

   - `Exchange`
   - `Refund`
   - `Store Credit`

1. 若要建立退貨，請按一下 **[!UICONTROL Submit Returns]**.

   ![已要求RMA專案](./assets/return-item-request.png){width="600" zoomable="yes"}

   新提交的RMA請求會顯示在 **[!UICONTROL Returns]** 頁面具有 `Pending` 狀態。
