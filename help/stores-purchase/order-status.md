---
title: 訂單狀態
description: 瞭解預先定義的訂單狀態，以及如何定義自訂訂單狀態以符合您的營運需求。
exl-id: d1153558-a721-4643-a70c-7fc20072983c
feature: Orders
source-git-commit: c2d5e9b41a76ba58d1343a8b3ee5122104d5bfe0
workflow-type: tm+mt
source-wordcount: '1223'
ht-degree: 0%

---

# 訂單狀態

所有訂單的訂單狀態都與訂單處理[工作流程](order-processing.md)中的階段相關聯。\
順序狀態與順序狀態之間的差異在於&#x200B;**[!UICONTROL order states]**&#x200B;是以程式設計方式使用。 他們不是
對客戶或管理員使用者可見。 它們決定訂單的流程，以及訂單可能執行的作業。
以特定狀態訂購。\
**[!UICONTROL Order statuses]**&#x200B;可用來將訂單狀態傳達給客戶和管理員。
您可以建立其他訂單狀態，以符合您的營運需求。 方便顯示訂單狀態
Adobe Commerce外部的進度，例如訂單撿料與交貨進度。 它們對訂單沒有影響
處理工作流程。\
每個訂單狀態都與一個訂單狀態相關聯。 您的商店有一組預先定義的訂單狀態和
順序狀態設定。

![訂單狀態和狀態](./assets/order-states-and-statuses.png){width="700" zoomable="yes"}

每個訂單的狀態會顯示在&#x200B;_訂單_&#x200B;格線的&#x200B;_狀態_&#x200B;資料行中。

![訂單狀態](./assets/stores-order-status-column.png){width="700" zoomable="yes"}

>[!TIP]
>
>部份退款的訂單在&#x200B;**_所有_**&#x200B;訂購料號（包括退款的料號）出貨前仍為`Processing`狀態。 在訂單中的每個專案都已出貨之前，訂單狀態不會變更為`Complete`。

## 訂單狀態工作流程

![訂單狀態工作流程](./assets/order-state-workflow.png)

## 預先定義的狀態

| 訂單狀態 | 狀態代碼 |                                                                                                                                                                                                                                                                                        |
|--------------------------|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 已接收 | `received` | 此狀態是啟用非同步下單時所下訂單的初始狀態。 |
| 疑似詐騙 | `fraud` | 有時透過PayPal或其他付款閘道支付的訂單會標示為&#x200B;_疑似詐騙_。 此狀態表示訂單沒有開立商業發票，也不會傳送確認電子郵件。 |
| 處理中 | `processing` | 當新訂單的狀態設為「處理」時，_自動開立所有料號發票_&#x200B;選項即可在組態中使用。 對於使用禮品卡、商店信用、獎勵點數或其他離線付款方式所下的訂單，不會自動建立發票。 |
| 未決付款 | `pending_payment` | 如果訂單已建立且使用PayPal或類似的付款方式，則會使用此狀態。 這表示客戶已導向付款閘道網站，但尚未收到退貨資訊。 當客戶付款時，此狀態會變更。 |
| 付款複查 | `payment_review` | 開啟PayPal付款稽核時，此狀態就會顯示。 |
| 擱置中 | `pending` | 此狀態表示尚未提交商業發票與出貨。 |
| 保留 | `holded` | 此狀態只能手動指派。 您可以保留任何訂單。 |
| 完成 | `complete` | 此狀態表示訂單已建立、已付款且已出貨給客戶。 |
| 已關閉 | `closed` | 此狀態表示訂單已指定銷退折讓單，且客戶已收到退款。 |
| 已取消 | `canceled` | 此狀態會在「管理員」中手動指派，或針對某些付款閘道，在客戶未在指定時間內付款時指派。 |
| 已拒絕 | `rejected` | 此狀態表示訂單在非同步訂單處理期間遭到拒絕。 非同步下單期間發生en錯誤時，就會發生此狀況。 |
| PayPal已取消迴轉 | `paypay_canceled_reversal` | 此狀態表示PayPal已取消迴轉。 |
| 擱置中的PayPal | `pending_paypal` | 此狀態表示PayPal已收到訂單，但尚未處理付款。 |
| PayPal已回覆 | `paypal_reversed` | 此狀態表示PayPal已迴轉交易。 |

{style="table-layout:auto"}

## 自訂訂單狀態

除了預設的訂單狀態設定外，您也可以建立自己的自訂訂單狀態設定、將其指派給訂單狀態，以及設定訂單狀態的預設訂單狀態。 訂單狀態會指出訂單在訂單處理工作流程中的位置，而訂單狀態會將有意義的可翻譯標籤指定給訂單的位置。 例如，您可能需要自訂訂單狀態，例如`packaging"`、`backordered`，或特定於您需求的狀態。 您可以為自訂狀態建立描述性名稱，並將其指派給工作流程中的關聯訂單狀態。

>[!NOTE]
>
>訂單工作流程中只會使用預設的自訂訂單狀態值。 未設定為預設的自訂狀態值只能用於訂單的註解區段。

![訂單狀態設定](./assets/order-status.png){width="700" zoomable="yes"}

### 建立自訂訂單狀態

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Order Status]**。

1. 按一下右上角的&#x200B;**[!UICONTROL Create New Status]**。

   ![建立新訂單狀態](./assets/order-status-new.png){width="600" zoomable="yes"}

1. 更新&#x200B;_[!UICONTROL Order Status Information]_&#x200B;區段：

   - 輸入&#x200B;**[!UICONTROL Status Code]**&#x200B;以供內部參考。 第一個字元必須是字母(a-z)，其餘字元可以是字母和數字(0-9)的任意組合。 請使用底線字元，而非空格。

   - 針對&#x200B;**[!UICONTROL Status Label]**，在管理員和店面中輸入可識別狀態設定的標籤。

1. 在&#x200B;_[!UICONTROL Store View Specific Labels]_&#x200B;區段中，輸入不同存放區檢視所需的任何標籤。

1. 按一下&#x200B;**[!UICONTROL Save Status]**。

### 將訂單狀態指派給狀態

1. 在&#x200B;_訂單狀態_&#x200B;頁面上，按一下&#x200B;**[!UICONTROL Assign Status to State]**。

   ![指派狀態](./assets/store-status-assign-status.png){width="600" zoomable="yes"}

1. 更新&#x200B;**[!UICONTROL Assignment Information]**&#x200B;區段，請執行下列動作：

   - 選擇要指派的&#x200B;**[!UICONTROL Order Status]**。 它們會依狀態標籤列出。

   - 將&#x200B;**[!UICONTROL Order State]**&#x200B;設定為工作流程中訂單狀態所屬的位置。

     >[!NOTE]
     >
     >**_[!UICONTROL Order State]_**&#x200B;清單包含預設的指派順序狀態。 例如，會顯示`Pending`預設訂單狀態，而非`New`訂單狀態值。

   - 若要將此狀態設為訂單狀態的預設值，請選取&#x200B;**[!UICONTROL Use Order Status as Default]**&#x200B;核取方塊。

     >[!NOTE]
     >
     >訂單工作流程中只會使用預設訂單狀態。 非預設狀態只能在Admin的&#x200B;**[!UICONTROL Order Comments]**&#x200B;區段中設定。

   - 若要從店面顯示此狀態，請選取「**[!UICONTROL Visible On Storefront]**」核取方塊。

   ![將狀態指派給狀態](./assets/order-status-assign-state.png){width="600" zoomable="yes"}

1. 按一下&#x200B;**[!UICONTROL Save Status Assignment]**。

### 編輯現有訂單狀態

1. 在&#x200B;_[!UICONTROL Order Status]_&#x200B;格線中，以編輯模式開啟狀態記錄。

1. 視需要更新狀態設定。

1. 按一下&#x200B;**[!UICONTROL Save Status]**。

### 從已指派狀態中移除訂單狀態

>[!NOTE]
>
>如果狀態正在使用中，則無法從狀態中取消指派狀態設定。

1. 在&#x200B;_[!UICONTROL Order Status]_&#x200B;網格中，尋找要取消指派的訂單狀態記錄。

1. 在列最右邊的&#x200B;_[!UICONTROL Action]_&#x200B;欄中，按一下&#x200B;**[!UICONTROL Unassign]**&#x200B;連結。

   工作區的頂端會顯示訊息，指出訂單狀態已取消指派。 雖然訂單狀態標籤仍會顯示在清單中，但已不再指派給狀態。 無法刪除訂單狀態設定。

>[!NOTE]
>
>如果預設訂單狀態是從訂單狀態取消指派，_&#x200B;**另一個**&#x200B;_&#x200B;訂單狀態是&#x200B;_&#x200B;**自動設定**&#x200B;_&#x200B;為此訂單狀態的預設值。

## 通知

如果組態中啟用了訂單RSS摘要，則客戶可透過[RSS摘要](../merchandising-promotions/social-rss.md)追蹤其訂單的狀態。 啟用時，每張訂單上都會顯示RSS摘要的連結。

### 啟用訂單狀態通知

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Catalog]**&#x200B;並在下方選擇&#x200B;**[!UICONTROL RSS Feeds]**。

1. 展開&#x200B;**[!UICONTROL Order]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

1. 將&#x200B;**[!UICONTROL Customer Order Status Notification]**&#x200B;設為`Enable`。

   ![客戶訂單狀態通知](../configuration-reference/catalog/assets/rss-feeds-order.png){width="600" zoomable="yes"}

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

### 設定新訂單電子郵件通知

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Sales]**&#x200B;並在下方選擇&#x200B;**[!UICONTROL Sales Emails]**。

1. 展開&#x200B;**[!UICONTROL Order]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![組態 — 訂單選項](../configuration-reference/sales/assets/sales-emails-order.png){width="600" zoomable="yes"}

1. 將&#x200B;**[!UICONTROL New Order Confirmation Email Sender]**&#x200B;設定為下列其中一項：

   - `General Contact`
   - `Sales Representative`
   - `Customer Support`
   - `Custom Email 1`
   - `Custom Email 2`

1. 選擇您要用於每種客戶型態的範本：

   - **[!UICONTROL New Order Confirmation Template]** — 選擇範本以用於擁有已註冊商店帳戶的客戶。
   - **[!UICONTROL New Order Confirmation Template for Guest]** — 選擇範本以用於沒有註冊商店帳戶的訪客客戶。

1. 若要通知其他人員（例如業務經理）新訂單，請輸入電子郵件地址&#x200B;**[!UICONTROL Send Order Email Copy To]**。

   如果需要一個以上的收件者，您可以新增多個電子郵件地址。

1. 將&#x200B;**[!UICONTROL Send Order Email Copy Method]**&#x200B;設定為下列其中一項：

   - `Bcc` — 只傳送一封有關新訂單的電子郵件給客戶和其他收件者，但客戶沒有看到他們收到的電子郵件也傳送給其他收件者。
   - `Separate Email` — 傳送兩封個別的電子郵件 — 一封給收件者，一封給客戶。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。
