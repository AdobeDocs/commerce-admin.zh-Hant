---
title: 銷售電子郵件
description: 瞭解如何設定銷售電子郵件，以支援與客戶就其訂單進行通訊。
exl-id: b205dc61-08cc-4783-810c-686ccf2ba300
feature: Communications, Orders
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---

# 銷售電子郵件

與訂單相關的事件會觸發數個電子郵件訊息，而且設定類似。 請確定您識別顯示為訊息寄件者的商店聯絡人、要使用的電子郵件範本，以及任何要接收訊息復本的人。 銷售電子郵件可在事件觸發時或依預定間隔傳送。

![銷售設定 — 銷售電子郵件](./assets/config-sales-sales-email-full.png){width="600" zoomable="yes"}

## 步驟1. 更新電子郵件範本

請務必更新 [電子郵件標頭](../systems/email-template-custom.md#header-template) 範本，以便其反映您的品牌以及所需的其他電子郵件範本。 如需完整的範本清單，請參閱 [電子郵件範本](../systems/email-templates.md).

## 步驟2. 選擇傳輸型別

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Sales]** 並選擇 **[!UICONTROL Sales Emails]**.

1. 如有必要，請展開 ![展開選擇器](../assets/icon-display-expand.png) 此  **[!UICONTROL General Settings]** 區段。

   ![銷售組態 — 銷售電子郵件一般設定](../configuration-reference/sales/assets/sales-emails-general-settings.png){width="600" zoomable="yes"}

   根據預設，非同步傳送設為 `Disable`. 若要變更系統設定，請清除 **[!UICONTROL Use system value]** 核取方塊並設定 **[!UICONTROL Asynchronous sending]** 變更為下列其中一項：

   - `Disable`  — 由事件觸發時傳送銷售電子郵件。
   - `Enable`  — 以預先決定的固定間隔傳送銷售電子郵件。

   Adobe Commerce支援建議啟用非同步傳送，以改善下單效能。 另請參閱 [訂單處理的設定最佳實務](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/maintenance/order-processing-configuration.html) Adobe Commerce支援知識庫中的。

## 步驟3. 完成每封銷售電子郵件訊息的詳細資料

1. 如有必要，請展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Order]** 區段。

   ![銷售設定 — 銷售電子郵件訂單](../configuration-reference/sales/assets/sales-emails-order.png){width="600" zoomable="yes"}

1. 確認 **[!UICONTROL Enabled]** 設為 `Yes` （預設）。

1. 設定 **[!UICONTROL New Order Confirmation Email]** 與顯示為訊息寄件者的商店連絡人。

1. 設定 **[!UICONTROL New Order Confirmation Template]** 至用來傳送給註冊客戶之電子郵件的範本。

1. 設定 **[!UICONTROL New Order Confirmation Template for Guest]** 至用於傳送給沒有您商店帳戶的來賓之電子郵件的範本。

1. 的 **[!UICONTROL Send Order Email Copy To]**，輸入任何收到新訂單電子郵件副本的人的電子郵件地址。

   如果傳送副本給多位收件者，請以逗號分隔每個地址。

1. 設定 **[!UICONTROL Send Order Email Copy Method]** 變更為下列其中一項：

   - `Bcc`  — 傳送 _盲文提供_ 在傳送給客戶的相同電子郵件的標題中包含收件者。 客戶看不到密件副本收件者。
   - `Separate Email`  — 以個別電子郵件的形式傳送副本。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Order Comments]** 區段並重複這些步驟。

   ![銷售組態 — 銷售電子郵件訂單註解](../configuration-reference/sales/assets/sales-emails-order-comments.png){width="600" zoomable="yes"}

1. 完成其餘銷售電子郵件型別的設定：

   - **[!UICONTROL Invoice]** / **[!UICONTROL Invoice Comments]**
   - **[!UICONTROL Shipment]** / **[!UICONTROL Shipment Comments]**
   - **[!UICONTROL Credit Memo]** / **[!UICONTROL Credit Memo Comments]**

1. 完成後，按一下 **[!UICONTROL Save Config]**.

   出現提示時，按一下 [快取管理](../systems/cache-management.md) 工作區頂端訊息中的連結，並清除所有無效快取。
