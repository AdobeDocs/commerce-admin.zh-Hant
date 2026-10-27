---
title: 付款失敗通知
description: 瞭解如何針對無法完成交易的付款方式設定電子郵件通訊。
exl-id: c64a4463-64d5-4dad-a8ad-13bfb141b65f
feature: Payments, Communications
TQID: 'https://experienceleague.adobe.com/ZnVr9N90qZ58fJARyOw4rAecOhQF6KLmJZSBJflgMKc'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 3dcbfa9e-51f8-569c-a0e4-7f59098f730f
    internal-label: Payments
  - id: bb03f6c4-cab9-560e-9d02-5816e1808d17
    internal-label: Communications
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 9d3fe9829bb5a7f2a75ad3c89edd38010f816a0c
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%
---
# 付款失敗通知

如果在結帳期間選取的付款方式無法完成交易，則會傳送通知給商店聯絡人或指定的管理員使用者。

## 步驟1：更新電子郵件範本

請確定您已更新所需的電子郵件範本以反映您的品牌。 如需完整的範本清單，請參閱[電子郵件範本清單](../systems/email-templates.md#email-template-list)。

## 步驟2：設定付款失敗的電子郵件

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > **[!UICONTROL Configuration]**。

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
