---
title: 獎勵和忠誠計畫
description: 瞭解可用於促進客戶參與及提升客戶忠誠度的獎勵點數系統。
exl-id: 2bccdcce-7936-4449-9634-d463ad29e5cc
feature: Rewards, Promotions/Events, Customers, Configuration
source-git-commit: f8254db7d69e58c8e9a78948ee6e40f5ea88cea0
workflow-type: tm+mt
source-wordcount: '1389'
ht-degree: 0%

---

# 獎勵和忠誠計畫

{{ee-feature}}

Adobe Commerce中的&#x200B;_獎勵點數_&#x200B;系統可讓您實作獨特的方案，以促進客戶參與及提高客戶忠誠度。 積分可以針對廣泛的交易與客戶活動授予，而組態可以設定為控制積分分配、平衡及有效期。 客戶可以根據您建立的獎勵點數與貨幣之間的轉換率，將點數兌換為購買。

## 購物車價格規則

可根據[購物車規則](price-rules-cart.md)獎勵給客戶。 這些優惠可獎勵為價格規則的唯一動作，或隨附折扣。

## 客戶餘額

管理員使用者可為每位客戶管理獎勵點餘額。 如果在店面中啟用，客戶也可以檢視其點數平衡的細節。

## 兌換點

>[!NOTE]
>
>[在結帳期間由客戶和管理員使用者兌換獎勵點數時，需要](reward-exchange-rates.md)獎勵匯率設定。

點數可在結帳期間由管理員使用者和客戶兌換（如果已啟用）。 在「付款方式」區段中，啟用付款方式的上方會顯示「使用我的獎勵點數」核取方塊。 包括可用的點數和貨幣匯率。 如果可用餘額大於訂單的總計，則不需要額外的付款方式。 套用至訂單的獎勵點數會與訂單總計一起顯示（從總計中扣除），類似於商店信用卡或禮品卡。 如果獎勵點數與商店信用卡或禮品卡搭配使用，則獎勵點數會先扣除。 如果訂單總計大於可兌換的獎勵點數，則會扣除商店信用卡或禮品卡。

>[!NOTE]
>
>不建議將獎勵點數用於貨到付款採購，因為必須在開立訂單商業發票之後才能確認付款收款。

## 退回獎勵積分

以獎勵點數下單的訂單可退回到獎勵點數餘額，最多可退回到訂單中的金額。 在&#x200B;[_新銷退折讓單_&#x200B;頁面](../stores-purchase/credit-memo-create.md)上，可以輸入要套用至客戶餘額的點數。 依預設，欄位包含順序中使用的完整點數。

## 啟用商店的獎勵點作業

獎勵點數設定會決定獎勵點數在商店中的呈現方式，並定義基本操作引數。

![客戶組態 — 獎勵點數](../configuration-reference/customers/assets/reward-points-reward-points.png){width="600" zoomable="yes"}

### 步驟1. 設定獎勵點數

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Customers]**&#x200B;並選擇&#x200B;**[!UICONTROL Reward Points]**。

1. 展開![展開選取器](../assets/icon-display-expand.png) **[!UICONTROL Reward Points]**&#x200B;區段，然後執行下列動作：

   - 若要啟用獎勵積分，請將&#x200B;**[!UICONTROL Enable Reward Points Functionality]**&#x200B;設為`Yes`。

   - 若要允許客戶取得自己的獎勵積分，請將&#x200B;**[!UICONTROL Enable Reward Points Functionality on Storefront]**&#x200B;設為`Yes`。

   - 若要允許客戶檢視其獎勵的詳細歷史記錄，請將&#x200B;**[!UICONTROL Customers May See Reward Point History]**&#x200B;設為`Yes`。

1. 針對&#x200B;**[!UICONTROL Reward Points Balance Redemption Threshold]**，輸入兌換前必須累積的點數（空白表示沒有最小值）。

1. 針對&#x200B;**[!UICONTROL Cap Reward Points Balance At]**，輸入客戶可累積的最大點數（空白表示無限制）。

1. 針對&#x200B;**[!UICONTROL Reward Points Expire in (days)]**，輸入獎勵點數到期前的天數（無到期則為空白）。

1. 將&#x200B;**[!UICONTROL Reward Points Expiry Calculation]**&#x200B;設定為下列其中一項：

   - `Static` — 根據設定中所設定的天數，決定獎勵分數的剩餘期限。 如果設定中的到期限制變更，則現有點的到期日不會變更。

   - `Dynamic` — 計算獎勵點餘額增加時的剩餘天數。 如果設定中的到期限制變更，則所有現有點的到期時間都會據此更新。

1. 如果您想要自動退款可用的獎勵積分，請將&#x200B;**[!UICONTROL Refund Reward Points Automatically]**&#x200B;設為`Yes`。

1. 若要在取得積分的訂單已全部或部分退款時，作廢透過採購所取得的獎勵積分，請將&#x200B;**[!UICONTROL Deduct Reward Points from Refund Amount Automatically]**&#x200B;設為`Yes`。

   >[!NOTE]
   >
   >只有使用正在退款的訂單所取得的點數會受到影響。

1. 將&#x200B;**[!UICONTROL Landing Page]**&#x200B;設定為說明您的獎勵積分方案的內容頁面。

   請務必使用您自己的資訊更新預設的獎勵點數頁面。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

### 步驟2. 設定客戶活動獲得的點數

在此步驟中，會指定可為各種客戶活動取得的獎勵點數。 當客戶完成已指定點的動作時，客戶會看到一則訊息，指出已獲得多少點。

1. 展開&#x200B;**[!UICONTROL Actions for Acquiring Reward Points by Customer]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![客戶組態 — 客戶取得獎勵分數的動作](../configuration-reference/customers/assets/reward-points-actions-for-acquiring.png){width="600" zoomable="yes"}

1. 若要允許根據設定的[獎勵匯率](reward-exchange-rates.md)為購買取得獎勵積分，請將&#x200B;**[!UICONTROL Purchase]**&#x200B;設為`Yes`。

   >[!NOTE]
   >
   >若要獲得其&#x200B;_前_&#x200B;筆訂單的獎勵積分，客戶必須在&#x200B;_前_&#x200B;以付款方式擷取交易註冊。 大多數付款方式都可以設定為在下訂單時&#x200B;_自動_&#x200B;擷取交易，但&#x200B;_在_&#x200B;之前，客戶帳戶註冊已完成。

1. 針對&#x200B;**[!UICONTROL Registration]**，輸入開立客戶帳戶所獲得的點數。

1. 針對&#x200B;**[!UICONTROL Newsletter Signup]**，輸入訂閱電子報的註冊客戶獲得的點數。

1. 針對&#x200B;**[!UICONTROL Converting Invitation to Customer]**，輸入傳送邀請的客戶獲得點數，然後收件者開啟客戶帳戶。

   您可以限制傳送邀請的客戶可獲得點數的邀請轉換次數（無限制空白）。 若要這麼做，請在&#x200B;**[!UICONTROL Invitation to Customer Conversions Quantity Limit]**&#x200B;欄位中輸入數字。

1. 針對&#x200B;**[!UICONTROL Converting Invitation to Order]**，輸入傳送邀請給收件者的客戶獲得點數，收件者之後會下訂單，並執行下列動作：

   - 針對&#x200B;**訂單轉換邀請數量限制**，請輸入當收件者下初始訂單時，傳送邀請的客戶獲得點數（空白表示無限制）。

   - 針對&#x200B;**[!UICONTROL Invitation Conversion to Order Reward]**，選取`Each`選項以取得每個收件者訂單的點數，或選取`First`選項以僅取得收件者第一筆訂單的點數。

1. 針對&#x200B;**[!UICONTROL Review Submission]**，輸入客戶提交稽核並核准發佈的點數。

1. 然後，若要限制可用於獲得每位客戶點數的評論數量，請在&#x200B;**[!UICONTROL Rewarded Reviews Submission Quantity Limit]**&#x200B;欄位中輸入數字（空白表示無限制）。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

### 步驟3. 完成電子郵件通知設定

1. 展開&#x200B;**[!UICONTROL Email Notification Settings]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![客戶設定 — 獎勵點數電子郵件通知](../configuration-reference/customers/assets/reward-points-email-notification-settings.png){width="600" zoomable="yes"}

1. 將&#x200B;**[!UICONTROL Email Sender]**&#x200B;設為顯示為餘額更新與到期通知之寄件者的商店連絡人。

1. 如果您想要依預設訂閱客戶，以接收餘額更新及即將到期日期的通知，請將&#x200B;**[!UICONTROL Subscribe Customers by Default]**&#x200B;設為`Yes`。

1. 將&#x200B;**[!UICONTROL Balance Update Email]**&#x200B;設為每當客戶點數餘額更新時傳送給客戶的通知所使用的範本。

1. 設定&#x200B;**[!UICONTROL Reward Points Expiry Warning Email]**&#x200B;為當達到批次點到期限制時傳送給客戶的通知所使用的範本。

1. 針對&#x200B;**[!UICONTROL Expiry Warning Before (days)]**，輸入傳送通知的點數過期前的天數。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

## 更新獎勵點數餘額

報酬點數餘額可以從管理員進行更新。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL All Customers]**。

1. 在格線中尋找客戶，然後按一下&#x200B;_[!UICONTROL Action]_欄中的&#x200B;**[!UICONTROL Edit]**。

1. 在&#x200B;_客戶資訊_&#x200B;底下，選擇&#x200B;**[!UICONTROL Reward Points]**&#x200B;區段。

1. 輸入&#x200B;**[!UICONTROL Update Points]**&#x200B;的數字：

   - 若要更新獎勵點數金額，請輸入數字以增加總點數餘額。
   - 若要減去獎勵點數，請輸入要減少總點數餘額的負數。

1. 視需要輸入與獎勵點數調整相關的&#x200B;**[!UICONTROL Comments]**。

   ![獎勵點數餘額](./assets/reward-points-balance.png){width="700" zoomable="yes"}

1. 可選擇讓客戶訂閱&#x200B;_獎勵點通知_：

   - **[!UICONTROL Subscribe for Balance Updates]**
   - **[!UICONTROL Subscribe for Points Expiration Notifications]**

1. 按一下&#x200B;**[!UICONTROL Save Customer]**。

與獎勵點數相關的所有動作都會顯示在店面其帳戶中客戶的&#x200B;_[!UICONTROL Reward Points History]_區塊中。

## 欄位說明

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Balance] | 目前使用者端獎勵點數的餘額 |
| [!UICONTROL Amount Balance] | 目前現金餘額的金額 |
| [!UICONTROL Points] | 新增或減去的點數 |
| [!UICONTROL Amount] | 增加或減去的金額 |
| [!UICONTROL Rate] | [獎勵匯率](reward-exchange-rates.md) |
| [!UICONTROL Website] | 已指派獎勵點歷史記錄的網站 |
| [!UICONTROL Reason] | 獎勵點數的原因：<br>**[!UICONTROL Making purchases]**— 每次客戶購買時，都能獲得點數。<br>**[!UICONTROL Registering on the site]** — 註冊時累計（一次）。<br>**[!UICONTROL Subscribing to a newsletter]**— 首次訂閱累計（一次）。<br>**[!UICONTROL Sending Invitations]** — 藉由邀請朋友加入網站來取得點數。<br>**[!UICONTROL Converting Invitations to Customer]**— 每發出一次邀請，即主要朋友在網站上註冊時，都能獲得點數。<br>**[!UICONTROL Converting Invitations to Order]** — 每次銷售都會從已傳送的邀請中取得點數。<br>**[!UICONTROL Review Submission]**— 獲得提交產品評論的點數。 |
| [!UICONTROL Created] | 獎勵點數更新的日期和時間 |
| [!UICONTROL Expired] | 過期的獎勵點數 |
| [!UICONTROL Comment] | 新增或減去點時的註解 |

{style="table-layout:auto"}

## 疑難排解資源

如需疑難排解獎勵點問題的說明，請參閱下列Commerce支援知識庫文章：

- [404錯誤 — 移除多重出貨結帳的獎勵點](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/storefront/magento-2.4.0-404-error-removing-rewards-points-on-multi-shipping-checkout.html)
