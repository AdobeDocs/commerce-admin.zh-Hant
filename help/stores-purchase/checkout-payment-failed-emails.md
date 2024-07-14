---
title: 付款失敗通知
description: 瞭解如何針對無法完成交易的付款方式設定電子郵件通訊。
exl-id: c64a4463-64d5-4dad-a8ad-13bfb141b65f
feature: Payments, Communications
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# 付款失敗通知

如果在結帳期間選取的付款方式無法完成交易，則會傳送通知給商店聯絡人或指定的管理員使用者。

## 步驟1：更新電子郵件範本

請確定您已更新所需的電子郵件範本以反映您的品牌。 如需完整的範本清單，請參閱[電子郵件範本清單](../systems/email-templates.md#email-template-list)。

## 步驟2：設定付款失敗的電子郵件

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板上，展開&#x200B;**[!UICONTROL Sales]**&#x200B;並選擇&#x200B;**[!UICONTROL Checkout]**。

1. 展開&#x200B;**[!UICONTROL Payment Failed Emails]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![付款失敗的電子郵件](../configuration-reference/sales/assets/checkout-payment-failed-emails.png){width="600" zoomable="yes"}

1. 設定付款失敗電子郵件的選項：

   - 將&#x200B;**[!UICONTROL Payment Failed Email Sender]**&#x200B;設為顯示為郵件寄件者的商店連絡人。
   - 將&#x200B;**[!UICONTROL Payment Failed Email Receiver]**&#x200B;設定為要接收電子郵件傳輸失敗通知的商店連絡人。
   - 將&#x200B;**[!UICONTROL Payment Failed Template]**&#x200B;設定為當付款方式在結帳期間失敗時傳送之電子郵件所使用的範本。

1. 針對&#x200B;**[!UICONTROL Send Payment Failed Email Copy To]**，輸入任何要接收付款失敗通知副本的人的電子郵件地址。

   如果傳送副本給多位收件者，請以逗號分隔每個地址。

1. 將&#x200B;**[!UICONTROL Payment Failed Copy Method]**&#x200B;設定為下列其中一項：

   - `Bcc` — 在傳送給客戶的同一封電子郵件的標頭中包含收件者，以傳送&#x200B;_不公開的禮貌副本_。 客戶看不到密件副本收件者。
   - `Separate Email` — 以個別電子郵件的形式傳送復本。

1. 按一下&#x200B;**[!UICONTROL Save Config]**。
