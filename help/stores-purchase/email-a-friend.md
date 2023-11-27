---
title: 傳送電子郵件給朋友
description: 瞭解如何提供電子郵件連結，讓您的客戶可以輕鬆與朋友分享產品連結。
exl-id: 46cf9994-6490-4cb4-85b7-9a7cab7783e0
feature: Storefront, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# 傳送電子郵件給朋友

電子郵件連結可讓您的客戶輕鬆與朋友分享產品連結。 在示範Luma商店中，電子郵件連結會顯示為信封圖示。 您可以根據語音和品牌自訂訊息範本。 若要防止傳送垃圾郵件，您可以限制每封電子郵件的收件者人數，以及在一小時期間內可共用的產品數量。

![店面範例 — 傳送電子郵件給朋友](./assets/storefront-email-a-friend.png){width="700" zoomable="yes"}

## 設定朋友電子郵件

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Catalog]** 並選擇 **[!UICONTROL Email to a Friend]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Email Templates]** 並設定選項：

   ![目錄設定 — 電子郵件範本](../configuration-reference/catalog/assets/email-to-a-friend-email-templates.png){width="600" zoomable="yes"}

   如需這些組態設定的詳細說明，請參閱 [電子郵件範本](../configuration-reference/catalog/email-to-a-friend.md) 在 _設定參考指南_.

   若要變更任何欄位的預設設定，請清除 **[!UICONTROL Use system value]** 核取方塊，讓欄位可編輯。

   - 設定 **[!UICONTROL Enabled]** 至 `Yes`.

   - 設定 **[!UICONTROL Select Email Template]** 至要作為訊息基礎的範本。

   - 如果您想要要求只有註冊客戶才能傳送電子郵件給朋友，請設定 **[!UICONTROL Allow for Guests]** 至 `No`.

   - 的 **[!UICONTROL Max Recipients]**，輸入單一訊息的通訊群組清單可包含的朋友數目上限。

   - 的 **[!UICONTROL Max Products Sent in 1 Hour]**，輸入單一使用者可在一小時內，與好友分享的產品數量上限。

   - 設定 **[!UICONTROL Limit Sending By]** 透過下列其中一種方法識別電子郵件的寄件者：

     `IP Address`  - （建議）依用來傳送電子郵件之電腦的IP位址識別寄件者。

     `Cookie (unsafe)`  — 透過瀏覽器Cookie識別寄件者。 此方法效果較差，因為傳送者可以刪除Cookie以略過限制。

1. 完成後，按一下 **[!UICONTROL Save Config]**.

## 傳送電子郵件給店面的朋友

設定此功能後，商店客戶將依照這些步驟與朋友分享產品資訊。

1. 在目錄頁面上，客戶按一下 **[!UICONTROL Email]** 連結。

1. 如果功能僅針對註冊使用者設定，則執行下列任一項作業：

   - 登入您的客戶帳戶。
   - 註冊新帳戶。

1. 完成 **[!UICONTROL Message]** 並輸入收件者 **[!UICONTROL Name]** 和 **[!UICONTROL Email Address]**.

   如有需要，客戶可以新增更多收件者：

   - 點擊數 **[!UICONTROL Add Invitee]**.

   - 輸入 **[!UICONTROL Name]** 和 **[!UICONTROL Email Address]** 其他人員的。

     他們可以傳送訊息給設定允許的其他人，數量不限。 他們可以按一下 **[!DNL Remove]** 連結。

1. 準備好傳送訊息時，請按一下 **[!UICONTROL Send Email]**.

   ![店面範例 — 傳送電子郵件給朋友](./assets/storefront-email-a-friend-form.png){width="700" zoomable="yes"}
