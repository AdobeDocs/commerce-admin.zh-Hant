---
title: 封存訂單
description: 瞭解如何設定訂單封存，以提升效能並簡化組織的Commerce。
exl-id: 12025591-bfe2-4f44-9358-a38ea4493b5c
feature: Orders, Configuration
source-git-commit: 47f170f1a1dd1c236b99c2e7139bb119368abf47
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 0%

---

# 封存訂單

{{ee-feature}}

封存訂單可定期改善效能，讓您的工作區遠離不必要的資訊，讓您專心處理目前的業務。 商業發票、出貨及銷退折讓單可自動或手動存檔，並可隨時檢視。

>[!NOTE]
>
>只有在封存已啟用[時](../configuration-reference/sales/sales.md)，_[!UICONTROL Archive]_選項才會出現在[[!UICONTROL Sales]功能表](sales-menu.md)中。

## 設定訂單封存

您可以設定商店，在設定的天數後，將訂單、商業發票、出貨及銷退折讓單存檔。 您可以將工單及其相關檔案移轉至存檔，或將它們還原成先前的狀態。 封存的訂單不會被刪除，管理員仍可繼續使用。 封存的資料可匯出至CSV檔案，並在試算表中開啟。 啟用時，_封存_&#x200B;動作會顯示在工作區的頂端。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Sales]**&#x200B;區段並在下方選擇&#x200B;**[!UICONTROL Sales]**。

1. 展開&#x200B;**[!UICONTROL Orders, Invoices, Shipments, Credit Memos Archiving]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![訂單、商業發票、出貨、銷退折讓單封存組態設定](../configuration-reference/sales/assets/sales-orders-invoices-shipments-credit-memos-archiving.png){width="600" zoomable="yes"}

1. 將&#x200B;**[!UICONTROL Enable Archiving]**&#x200B;設為`Yes`。

   >[!NOTE]
   >
   >如果您稍後決定關閉封存，所有封存的訂單都會恢復至先前的狀態。

1. 將&#x200B;**[!UICONTROL Archive Orders Purchased]**&#x200B;設定為完成訂單封存前的等待天數。

   依預設，會在購買30天後封存訂單。

1. 在&#x200B;**[!UICONTROL Order Statuses to be Archived]**&#x200B;清單中，選取用於識別要封存之訂單的每個訂單狀態。

   若要選取多個專案，請按住Ctrl鍵(Windows)或Command鍵(Mac)，同時按一下每個專案。

1. 按一下&#x200B;**[!UICONTROL Save Config]**。

1. 出現提示時，請重新整理任何無效的快取。

## 檢視封存的檔案

1. 在&#x200B;_[!UICONTROL Archive]_下的_[!UICONTROL Sales]_&#x200B;功能表中，選擇下列任一項：

   - **[!UICONTROL Orders]**
   - **[!UICONTROL Invoices]**
   - **[!UICONTROL Shipments]**
   - **[!UICONTROL Credit Memos]**

1. 若要檢視詳細資訊，請按一下清單中的任何封存檔案。

## 將動作套用至已封存的檔案

選取要作為動作目標的每個檔案，並選擇下列&#x200B;**[!UICONTROL Actions]**&#x200B;之一：

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

1. 在右上角，將&#x200B;**[!UICONTROL Actions]**&#x200B;設為`Move to Archive`。

1. 按一下&#x200B;**[!UICONTROL Submit]**&#x200B;以封存選取的檔案。

## 還原已封存的檔案

1. 選擇要還原的檔案型別。

1. 使用下列其中一個選項來選取檔案：

   - 若要選取所有可見的檔案，請按一下左上角的&#x200B;**[!UICONTROL Select Visible]**。

   - 手動選取要還原之每個檔案的核取方塊。

1. 在右上角，將&#x200B;**[!UICONTROL Action]**&#x200B;設定為`Move to Orders Management`。

1. 按一下&#x200B;**[!UICONTROL Submit]**&#x200B;以還原檔案。

## 匯出已封存的檔案

1. 選擇您要匯出的檔案型別。

1. 在右上角功能表中，將&#x200B;**[!UICONTROL Export to:]**&#x200B;設定為下列其中一個值：

   - `CSV`
   - `Excel`

1. 按一下&#x200B;**[!UICONTROL Export]**。

您可以設定商店，在設定的天數後，將訂單、商業發票、出貨及銷退折讓單存檔。 您可以將工單及其相關檔案移轉至存檔，或將它們還原成先前的狀態。 封存的訂單不會被刪除，管理員仍可繼續使用。 封存的資料可匯出至CSV檔案，並在試算表中開啟。 啟用時，_[!UICONTROL Archive]_命令會顯示在工作區的頂端。

## 手動封存訂單

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**。

1. 若要選取網格上的順序，請選取第一欄中的核取方塊。

1. 將&#x200B;**[!UICONTROL Actions]**&#x200B;控制項設為`Move to Archive`，並尋找已封存訂單的訊息。

   ![正在將選取的訂單移至封存](./assets/order-move-to-archive.png){width="700" zoomable="yes"}

>[!TIP]
>
>若要指定可封存的訂單狀態清單，請參閱[設定訂單封存](#configure-the-order-archive)。

## 檢視已封存的訂單

1. 使用下列其中一種方法開啟封存檢視：

   - 在&#x200B;_[!UICONTROL Orders]_格線上方的按鈕列中，按一下&#x200B;**[!UICONTROL Go to Archive]**。

   - 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Sales]** > _[!UICONTROL Archive]_>**[!UICONTROL Orders]**。

   >[!NOTE]
   >
   >與「訂單」頁面一樣，已封存訂單頁面的標題為&#x200B;_[!UICONTROL Orders]_。 唯一明顯的差異是按鈕列中的_[!UICONTROL Return to Orders Management]_&#x200B;選項。 頁面的URL也表示您處於順序封存中。

1. 在&#x200B;_動作_&#x200B;資料行中，按一下&#x200B;**[!UICONTROL View]**。

   ![檢視已封存的訂單](./assets/order-archived-view.png){width="600" zoomable="yes"}

## 還原已封存的訂單

>[!NOTE]
>
>根據[!UICONTROL Archive Orders Purchased]設定中設定的天數，從封存訂單還原的訂單會再次封存（請參閱[設定訂單封存](#configure-the-order-archive)）。 系統會根據訂單的[!UICONTROL Updated At]日期計算天數，當從封存中移動訂單時，日期會變更。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**。

1. 在按鈕列中按一下&#x200B;**[!UICONTROL Go to Archive]**。

1. 找到要還原的記錄，然後按一下核取方塊以選取它。

   ![選取要還原的順序](./assets/order-archived-select-to-restore.png){width="600" zoomable="yes"}

1. 將&#x200B;**[!UICONTROL Actions]**&#x200B;控制項值設為`Move to Order Management`。

尋找已封存訂單已從封存中移除的訊息。

## 匯出已封存的訂單

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**。

1. 在動作功能表中，按一下&#x200B;**[!UICONTROL Export]**&#x200B;並選取所需的格式。
