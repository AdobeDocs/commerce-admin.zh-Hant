---
title: 封存訂單
description: 瞭解如何設定訂單封存以提升效能並簡化組織的Commerce。
exl-id: 12025591-bfe2-4f44-9358-a38ea4493b5c
feature: Orders, Configuration
source-git-commit: 47f170f1a1dd1c236b99c2e7139bb119368abf47
workflow-type: tm+mt
source-wordcount: '745'
ht-degree: 0%

---

# 封存訂單

{{ee-feature}}

封存訂單可定期改善效能，讓您的工作區遠離不必要的資訊，讓您專心處理目前的業務。 商業發票、出貨及銷退折讓單可自動或手動存檔，並可隨時檢視。

>[!NOTE]
>
>此 _[!UICONTROL Archive]_選項會顯示在 [[!UICONTROL Sales] 功能表](sales-menu.md) 僅當封存為 [已啟用](../configuration-reference/sales/sales.md).

## 設定訂單封存

您可以設定商店，在設定的天數後，將訂單、商業發票、出貨及銷退折讓單存檔。 您可以將工單及其相關檔案移轉至存檔，或將它們還原成先前的狀態。 封存的訂單不會被刪除，管理員仍可繼續使用。 封存的資料可匯出至CSV檔案，並在試算表中開啟。 啟用時， _封存_ 動作會顯示在工作區頂端。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Sales]** 區段並選擇 **[!UICONTROL Sales]** 底下。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Orders, Invoices, Shipments, Credit Memos Archiving]** 區段。

   ![訂單、商業發票、出貨、銷退折讓單存檔組態設定](../configuration-reference/sales/assets/sales-orders-invoices-shipments-credit-memos-archiving.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Enable Archiving]** 至 `Yes`.

   >[!NOTE]
   >
   >如果您稍後決定關閉封存，所有封存的訂單都會恢復至先前的狀態。

1. 設定 **[!UICONTROL Archive Orders Purchased]** 至完成訂單存檔前等待的天數。

   依預設，會在購買30天後封存訂單。

1. 在 **[!UICONTROL Order Statuses to be Archived]** 清單中，選取用於識別要封存之訂單的每個訂單狀態。

   若要選取多個專案，請按住Ctrl鍵(Windows)或Command鍵(Mac)，同時按一下每個專案。

1. 按一下 **[!UICONTROL Save Config]**.

1. 出現提示時，請重新整理任何無效的快取。

## 檢視封存的檔案

1. 在 _[!UICONTROL Sales]_下的選單_[!UICONTROL Archive]_，選擇下列任一項：

   - **[!UICONTROL Orders]**
   - **[!UICONTROL Invoices]**
   - **[!UICONTROL Shipments]**
   - **[!UICONTROL Credit Memos]**

1. 若要檢視詳細資訊，請按一下清單中的任何封存檔案。

## 將動作套用至已封存的檔案

選取要作為動作目標的每個檔案，並選擇下列其中一項 **[!UICONTROL Actions]**：

- `Cancel`
- `Hold`
- `Unhold`
- `Print`
- `Move to Orders Management`

## 手動封存檔案

1. 從下列專案選取要封存的檔案型別：

   - **[!UICONTROL Orders]**
   - **[!UICONTROL Invoices]**
   - **[!UICONTROL Shipments]**
   - **[!UICONTROL Credit Memos]**

1. 選取每個要封存專案的核取方塊。

1. 在右上角，設定 **[!UICONTROL Actions]** 至 `Move to Archive`.

1. 按一下 **[!UICONTROL Submit]** 以封存所選檔案。

## 還原已封存的檔案

1. 選擇要還原的檔案型別。

1. 使用下列其中一個選項來選取檔案：

   - 若要選取所有可見的檔案，請按一下左上角的 **[!UICONTROL Select Visible]**.

   - 手動選取要還原之每個檔案的核取方塊。

1. 在右上角，設定 **[!UICONTROL Action]** 至 `Move to Orders Management`.

1. 按一下 **[!UICONTROL Submit]** 以還原檔案。

## 匯出已封存的檔案

1. 選擇您要匯出的檔案型別。

1. 在右上角功能表中，設定 **[!UICONTROL Export to:]** 變更為下列其中一個值：

   - `CSV`
   - `Excel`

1. 按一下 **[!UICONTROL Export]**.

您可以設定商店，在設定的天數後，將訂單、商業發票、出貨及銷退折讓單存檔。 您可以將工單及其相關檔案移轉至存檔，或將它們還原成先前的狀態。 封存的訂單不會被刪除，管理員仍可繼續使用。 封存的資料可匯出至CSV檔案，並在試算表中開啟。 啟用時， _[!UICONTROL Archive]_指令會顯示在工作區頂端。

## 手動封存訂單

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. 若要選取網格上的順序，請選取第一欄中的核取方塊。

1. 設定 **[!UICONTROL Actions]** 控制項至 `Move to Archive` 並尋找已封存訂單的訊息。

   ![將選取的訂單移至封存 ](./assets/order-move-to-archive.png){width="700" zoomable="yes"}

>[!TIP]
>
>若要指定可封存的訂單狀態清單，請參閱 [設定訂單封存](#configure-the-order-archive).

## 檢視已封存的訂單

1. 使用下列其中一種方法開啟封存檢視：

   - 在上方的按鈕列中 _[!UICONTROL Orders]_格點，按一下&#x200B;**[!UICONTROL Go to Archive]**.

   - 在 _管理員_ 側欄，前往 **[!UICONTROL Sales]** > _[!UICONTROL Archive]_>**[!UICONTROL Orders]**.

   >[!NOTE]
   >
   >與「訂單」頁面一樣，已封存訂單頁面的標題為 _[!UICONTROL Orders]_. 唯一顯著的差異是按鈕列中的選項_[!UICONTROL Return to Orders Management]_. 頁面的URL也表示您處於順序封存中。

1. 在 _動作_ 欄，按一下 **[!UICONTROL View]**.

   ![檢視已封存的訂單](./assets/order-archived-view.png){width="600" zoomable="yes"}

## 還原已封存的訂單

>[!NOTE]
>
>系統會根據中設定的天數，再次封存從已封存訂單還原的訂單。 [!UICONTROL Archive Orders Purchased] 設定(請參閱 [設定訂單封存](#configure-the-order-archive))。 天數是根據以下公式計算： [!UICONTROL Updated At] 訂單的日期，當從封存中移轉訂單時，此日期會變更。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. 在按鈕列中，按一下 **[!UICONTROL Go to Archive]**.

1. 找到要還原的記錄，然後按一下核取方塊以選取它。

   ![選取要還原的順序](./assets/order-archived-select-to-restore.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Actions]** 控制值至 `Move to Order Management`.

尋找已封存訂單已從封存中移除的訊息。

## 匯出已封存的訂單

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. 在動作功能表中，按一下 **[!UICONTROL Export]** 並選取所需的格式。
