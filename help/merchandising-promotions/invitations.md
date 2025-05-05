---
title: 活動邀請
description: 瞭解客戶如何從客戶帳戶的儀表板傳送和檢視活動邀請和私人銷售。
exl-id: 6a9123a0-bdb4-4cd6-99cd-658f728aa90c
feature: Promotions/Events, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 0%

---

# 活動邀請

{{ee-feature}}

啟用邀請後，客戶可以從其客戶帳戶的儀表板傳送和檢視邀請。 邀請電子郵件會包含您商店客戶登入頁面的連結。

## 我的邀請

客戶帳戶的&#x200B;_[!UICONTROL My Invitations]_&#x200B;區段會列出客戶傳送的所有邀請。 客戶可以傳送邀請給朋友和家人參加商店活動、禮品註冊處、願望清單等。

![我的邀請](./assets/account-dashboard-my-invitations.png){width="700" zoomable="yes"}

### 邀請工作流程

1. **客戶準備邀請**：客戶從帳戶儀表板準備收件者清單並完成邀請。 視設定而定，可包含自訂訊息。
1. **客戶傳送邀請**：準備就緒時，客戶按一下&#x200B;_[!UICONTROL Send Invitations]_&#x200B;按鈕。
1. **系統管理傳輸**：系統會根據組態中設定的數目，以批次傳送邀請。
1. **客戶監視回應**：客戶監視來自帳戶儀表板的每個邀請的狀態，如`Sent`、`Accepted`或`Canceled`。

### 傳送邀請

1. 在店面的帳戶側邊欄中，客戶選擇&#x200B;**[!UICONTROL My Invitations]**。

1. 在&#x200B;_我的邀請_&#x200B;頁面上按一下&#x200B;**[!UICONTROL Send Invitation]**。

1. 定義新的邀請專案：

   - 完成電子郵件資訊。

   - （選擇性）按一下&#x200B;**+**&#x200B;並新增另一個電子郵件地址，以建立多重位址邀請。

     單一邀請的電子郵件地址限製為5個。

   - （選擇性）輸入隨附的訊息。

1. 完成後，按一下&#x200B;**[!UICONTROL Send Invitation]**。

邀請通知會傳送至受邀使用者的電子郵件地址，其中包含設定帳戶的指示連結。

>[!NOTE]
>
>使用者只能向特定電子郵件地址傳送一個邀請。 嘗試將邀請重新傳送至相同的電子郵件地址時，會顯示錯誤訊息，且不會傳送邀請。

## 啟用您商店的邀請

邀請設定會啟用商店的邀請，並決定其傳送方式。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Customers]**&#x200B;並選擇&#x200B;**[!UICONTROL Invitations]**。

1. 展開&#x200B;**[!UICONTROL General]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![客戶組態 — 邀請一般選項](../configuration-reference/customers/assets/invitations-general.png){width="600" zoomable="yes"}

1. 將&#x200B;**[!UICONTROL Enable Invitations Functionality]**&#x200B;設為`Yes`。

1. 若要允許客戶管理店面的邀請，請將&#x200B;**啟用店面的邀請**&#x200B;設定為`Yes`。

1. 將&#x200B;**[!UICONTROL Referred Customer Group]**&#x200B;設定為下列其中一項：

   - `Same as Inviter`
   - `Default Customer Group from Configuration`

1. 將&#x200B;**[!UICONTROL New Accounts Registration]**&#x200B;設定為下列其中一項：

   - `By Invitation Only`
   - `Available to All`

1. 至&#x200B;**[!UICONTROL Allow Customers to Add Custom Message to Invitation Email]**，選取`Yes`。

1. 若要限制一次可傳送的邀請數目，請在&#x200B;**[!UICONTROL Max Invitations Allowed to be Sent at One Time]**&#x200B;欄位中輸入數字。

1. 展開![展開選取器](../assets/icon-display-expand.png) **[!UICONTROL Email]**&#x200B;區段，然後執行下列動作：

   ![客戶組態 — 邀請電子郵件選項](../configuration-reference/customers/assets/invitations-email.png){width="600" zoomable="yes"}

   - 選取要用作&#x200B;**[!UICONTROL Customer Invitation Email Sender]**&#x200B;的存放區識別。

   - 選取用於已傳送邀請的&#x200B;**[!UICONTROL Customer Invitation Email Template]**。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

## 以管理員身分傳送及管理邀請

在[私人銷售報告](../getting-started/private-sales-reports.md)區段中，您可以看到在指定期間內傳送的邀請數目，或您已傳送邀請的客戶。

### 在管理員中建立邀請

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**。

1. 按一下右上角的&#x200B;**[!UICONTROL Add Invitations]**。

1. 在下一個畫面中，輸入電子郵件地址以邀請新客戶、新增自訂訊息、選擇寄件者，以及選取受邀者群組。

   如果您有多個存放區檢視，請使用&#x200B;**[!UICONTROL Send From]**&#x200B;選項來指定傳送邀請的存放區檢視。

   ![邀請資訊](./assets/create-invitation-page.png){width="700" zoomable="yes"}

1. 完成時，按一下&#x200B;**[!UICONTROL Save]**。

### 捨棄單一實體的邀請

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**。

1. 使用篩選器尋找所需的邀請，並以編輯模式開啟。

1. 按一下右上角的&#x200B;**[!UICONTROL Discard Invitation]**。

1. 若要確認動作，請按一下&#x200B;**[!UICONTROL OK]**。

### 捨棄多個實體的邀請

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**。

1. 尋找並選取要捨棄的邀請。

1. 在左上方，使用&#x200B;**[!UICONTROL Actions]**&#x200B;功能表選擇&#x200B;**[!UICONTROL Discard Selected]**&#x200B;並按一下&#x200B;**[!UICONTROL Submit]**。

1. 若要確認動作，請按一下&#x200B;**[!UICONTROL OK]**。

### 欄位說明

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Select] | 選取核取方塊以選取要接受動作的邀請，或使用欄標題中的選取控制項。 選項： `Select All` /` Deselect All` / `Select Visible` / `Unselect Visible` |
| [!UICONTROL ID] | 邀請的內部識別碼 |
| [!UICONTROL Email] | 對應的客戶電子郵件地址 |
| [!UICONTROL Invitee] | 受邀使用者電子郵件 |
| [!UICONTROL Sent] | 傳送邀請的時間和日期 |
| [!UICONTROL Registered] | 客戶註冊的時間和資料 |
| [!UICONTROL Status] | 邀請狀態。 選項： `Sent` / `Not Sent` / `Accepted` / `Discarded` |
| [!UICONTROL Valid Website] | 對應的網站 |
| [!UICONTROL Invitee Group] | 受邀者的客戶群組 |

{style="table-layout:auto"}
