---
title: 管理公司評價
description: 瞭解公司信用額度、設定引數及處理分期付款的相關資訊。
exl-id: 62ff2a36-053d-4ba0-9969-0f05701afbff
feature: B2B, Companies, Payments
role: Admin
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '802'
ht-degree: 0%

---

# 管理公司評價

如果組態中啟用了[帳戶付款](../getting-started/../b2b/enable-basic-features.md#configure-payment-on-account)，則公司可以在其帳戶上進行購買，但最多可達到授予公司的信用額度。 啟用後，客戶可以從其帳戶儀表板檢查其公司業績的狀態。

![公司點數](./assets/company-create-credit-admin.png){width="700" zoomable="yes"}

您可以為每個公司設定檔設定下列信用相關引數：

- 貸方貨幣
- 信用額度
- 允許超過信用額度
- 變更原因

如果公司有未結餘額，則當從管理員檢視時，通知商店管理員會顯示在銷售訂單的頂端。 若要深入瞭解，請參閱[建立公司帳戶](account-company-create.md)。

## 公司信用活動

公司設定檔的[!UICONTROL Company Credit]區段會顯示客戶信用活動的摘要，以及公司信用記錄的網格。

![公司信用活動](./assets/company-credit-reimbursements-grid.png){width="700" zoomable="yes"}

| 欄 | 說明 |
|--- |--- |
| [!UICONTROL Date] | 交易的日期。 若要顯示日期和時間，請將游標停留在日期上。 |
| [!UICONTROL Operation] | 與交易相關聯的活動型別。 值： <br/>**[!UICONTROL Allocated]**— 指派給公司的評分。<br/>**[!UICONTROL Updated]** — 變更已套用至下列其中一個欄位： [!UICONTROL Credit limit] / [!UICONTROL Credit currency] / [!UICONTROL Allow to exceed credit limit] <br/>**[!UICONTROL Purchased]**— 已下訂單。<br/>**[!UICONTROL Reimbursed]** — 未償還餘額已償還。 <br/>**[!UICONTROL Refunded]**— 銷退折讓單金額已退款。<br/>**[!UICONTROL Reverted]** — 訂單已取消，金額已傳回至貸方餘額。 |
| [!UICONTROL Amount] | 與下列交易型別相關的交易金額： `Purchased` / `Reimbursed` / `Refunded` / `Reverted` <br/>對於購買金額，金額會以商店的顯示貨幣和信用貨幣設定的格式顯示，之後會加上目前的轉換率（如果適用）。 例如：<br/>EUR 20,000.00 ($22,400.00) <br/>USD/EUR 0.8928 |
| [!UICONTROL Outstanding Balance] | 已償還的金額，減去使用「掛帳付款」方式下所有訂單的到期總額。 數量可能會顯示為正數或負數。 <br/>**[!UICONTROL Positive value]**— 預付款以正值表示。<br/>**[!UICONTROL Negative value]** — 應付金額以負值表示。 |
| [!UICONTROL Available Credit] | _[!UICONTROL Credit Limit]_與_[!UICONTROL Outstanding Balance]_&#x200B;的總和。 如果公司已超過信用額度，金額會顯示為負值。 |
| [!UICONTROL Credit Limit] | 給予公司的信用額度。 |
| [!UICONTROL Updated By] | 起始作業人員的姓名。 |
| [!UICONTROL Custom Reference Number] | 與交易相關聯的自訂參考編號。 |
| [!UICONTROL Comment] | 根據作業型別，從`Reason for Change`欄位編譯值。 <br/>**[!UICONTROL Purchased]**— 包含採購的評論，以及訂單編號和訂單連結。<br/>**[!UICONTROL Reimbursed]** — 包含已償還交易的註解。 |
| [!UICONTROL Action] | 僅適用於`Reimbursed`作業。 **[!UICONTROL Edit]** — 允許更新補助金額。 |

{style="table-layout:auto"}

## 更新信用資訊

當客戶將其未結銷退折讓付款給商家時，商店管理員必須在「管理員」中更新客戶銷退折讓資訊。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，前往&#x200B;**客戶>公司**。

1. 在格線中尋找公司，並以&#x200B;_編輯_&#x200B;模式開啟。

1. 展開&#x200B;**公司業績**&#x200B;區段。

1. 針對&#x200B;**信用額度**，請輸入新值。

1. 視需要變更其他值。

1. 更新完成時，按一下&#x200B;**[!UICONTROL Save]**。

## 接收付款

償還餘額是公司對其帳戶餘額進行的離線付款。 店舖管理員使用&#x200B;_償還餘額_&#x200B;按鈕，在公司設定檔中手動輸入金額。 提交金額時，系統會重新計算未結餘額與可用的公司信用額度，並將此作業記錄在公司信用記錄中。 已償還金額是以信用幣別輸入，如組態中所指定。

### 將付款套用至公司帳戶

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL Companies]**。

1. 在清單中尋找公司記錄，並以&#x200B;**[!UICONTROL Edit]**&#x200B;模式開啟。

1. 按一下頁面頂端的&#x200B;**償還餘額**。

1. 在對話方塊中，新增付款資訊：

   ![償還餘額](./assets/company-reimburse-balance.png){width="500"}

   - 輸入付款的&#x200B;**金額**。

     金額可以輸入為正數或負數。

   - 如果適用，請輸入&#x200B;**自訂參考編號**&#x200B;以供參考。

     每個補助只能輸入一個自訂參考編號。 若要將付款套用至多個採購單，請為每個採購單建立個別的補助。

   - 視需要輸入&#x200B;**註解**&#x200B;以說明補助金。

1. 按一下&#x200B;**償還**。

   系統會重新計算公司的未結餘額與可用信用額度，並更新「公司信用記錄」以反映補助。

### 編輯補助

1. 以&#x200B;**[!UICONTROL Edit]**&#x200B;模式開啟公司設定檔。

1. 展開&#x200B;**公司評價**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

1. 在網格中尋找補助交易，然後按一下&#x200B;**[!UICONTROL Edit]**。

1. 對&#x200B;**自訂參考編號**&#x200B;和&#x200B;**註解**&#x200B;進行任何必要的變更。

   補助金額無法變更。

1. 按一下&#x200B;**[!UICONTROL Save]**。

## 店面信用資訊

對於公司管理員，帳戶儀表板會顯示&#x200B;_公司業績_&#x200B;區段。 它提供目前未結餘額、可用信用額，以及配置給其公司帳戶的信用額度，後面接著未結商業發票清單。

如果商家取消已記入公司銷退折讓的訂單，則訂單金額會傳回至公司餘額，且&#x200B;_銷退折讓配置歷史記錄_&#x200B;包含該動作的記錄。

![公司點數](./assets/company-credit.png){width="700" zoomable="yes"}

## 公司信用示範

觀看此示範影片，瞭解如何管理公司點數：

>[!VIDEO](https://video.tv.adobe.com/v/344445?quality=12&learn=on)
