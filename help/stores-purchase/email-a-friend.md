---
title: 傳送電子郵件給朋友
description: 瞭解如何提供電子郵件連結，讓您的客戶可以輕鬆與朋友分享產品連結。
exl-id: 46cf9994-6490-4cb4-85b7-9a7cab7783e0
feature: Storefront, Configuration
TQID: https://experienceleague.adobe.com/a75E4X5mTDXeCQKysvIecdU3OhsICiWTtwh7k-oK9cw
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 414
ht-degree: 0%

---

# 傳送電子郵件給朋友

電子郵件連結可讓您的客戶輕鬆與朋友分享產品連結。 在示範Luma商店中，電子郵件連結會顯示為信封圖示。 您可以根據語音和品牌自訂訊息範本。 若要防止傳送垃圾郵件，您可以限制每封電子郵件的收件者人數，以及在一小時期間內可共用的產品數量。

![店面範例 — 傳送電子郵件給朋友](./assets/storefront-email-a-friend.png){width="700" zoomable="yes"}

## 設定朋友電子郵件

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Catalog]**&#x200B;並選擇&#x200B;**[!UICONTROL Email to a Friend]**。

1. 展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Email Templates]**&#x200B;區段並設定選項：

   ![目錄設定 — 電子郵件範本](../configuration-reference/catalog/assets/email-to-a-friend-email-templates.png){width="600" zoomable="yes"}

   如需這些組態設定的詳細說明，請參閱&#x200B;_組態參考指南_&#x200B;中的[電子郵件範本](../configuration-reference/catalog/email-to-a-friend.md)。

   若要變更任何欄位的預設設定，請清除「**[!UICONTROL Use system value]**」核取方塊以使欄位可編輯。

   - 將&#x200B;**[!UICONTROL Enabled]**&#x200B;設為`Yes`。

   - 將&#x200B;**[!UICONTROL Select Email Template]**&#x200B;設定為您要做為訊息基礎的範本。

   - 如果您想要要求只有註冊客戶才能傳送電子郵件給朋友，請將&#x200B;**[!UICONTROL Allow for Guests]**&#x200B;設為`No`。

   - 針對&#x200B;**[!UICONTROL Max Recipients]**，輸入單一訊息可加入通訊群組清單的朋友數目上限。

   - 針對&#x200B;**[!UICONTROL Max Products Sent in 1 Hour]**，輸入單一使用者在一小時期間內可與朋友共用的產品數量上限。

   - 將&#x200B;**[!UICONTROL Limit Sending By]**&#x200B;設為下列其中一個方法，以識別電子郵件的寄件者：

     `IP Address` - （建議）依用來傳送電子郵件之電腦的IP位址識別寄件者。

     `Cookie (unsafe)` — 透過瀏覽器Cookie識別寄件者。 此方法效果較差，因為傳送者可以刪除Cookie以略過限制。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

## 傳送電子郵件給店面的朋友

設定此功能後，商店客戶將依照這些步驟與朋友分享產品資訊。

1. 客戶在目錄頁面上按一下&#x200B;**[!UICONTROL Email]**&#x200B;連結。

1. 如果功能僅針對註冊使用者設定，則執行下列任一項作業：

   - 登入您的客戶帳戶。
   - 註冊新帳戶。

1. 完成&#x200B;**[!UICONTROL Message]**&#x200B;並輸入收件者&#x200B;**[!UICONTROL Name]**&#x200B;和&#x200B;**[!UICONTROL Email Address]**。

   如有需要，客戶可以新增更多收件者：

   - 按一下&#x200B;**[!UICONTROL Add Invitee]**。

   - 輸入其他人員的&#x200B;**[!UICONTROL Name]**&#x200B;和&#x200B;**[!UICONTROL Email Address]**。

     他們可以傳送訊息給設定允許的其他人，數量不限。 他們可以按一下&#x200B;**[!DNL Remove]**&#x200B;連結來移除新增的被邀請者。

1. 準備傳送訊息時，請按一下&#x200B;**[!UICONTROL Send Email]**。

   ![店面範例 — 傳送電子郵件給朋友](./assets/storefront-email-a-friend-form.png){width="700" zoomable="yes"}
