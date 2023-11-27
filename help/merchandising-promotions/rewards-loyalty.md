---
title: 獎勵和忠誠計畫
description: 瞭解可用於促進客戶參與及提升客戶忠誠度的獎勵點數系統。
exl-id: 2bccdcce-7936-4449-9634-d463ad29e5cc
feature: Rewards, Promotions/Events, Customers, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '1391'
ht-degree: 0%

---

# 獎勵和忠誠計畫

{{ee-feature}}

此 _獎勵點數_ Adobe Commerce中的系統可讓您實作獨特的計畫，以促進客戶參與及提高客戶忠誠度。 積分可以針對廣泛的交易與客戶活動授予，而組態可以設定為控制積分分配、平衡及有效期。 客戶可以根據您建立的獎勵點數與貨幣之間的轉換率，將點數兌換為購買。

## 購物車價格規則

可獲得點數獎勵給客戶，基礎是 [購物車規則](price-rules-cart.md). 這些優惠可獎勵為價格規則的唯一動作，或隨附折扣。

## 客戶餘額

管理員使用者可為每位客戶管理獎勵點餘額。 如果在店面中啟用，客戶也可以檢視其點數平衡的細節。

## 兌換點

>[!NOTE]
>
>[獎勵匯率](reward-exchange-rates.md) 若要在結帳期間由客戶和管理員使用者兌換獎勵積分，則必須進行設定。

點數可在結帳期間由管理員使用者和客戶兌換（如果已啟用）。 在「付款方式」區段中，啟用付款方式的上方會顯示「使用我的獎勵點數」核取方塊。 包括可用的點數和貨幣匯率。 如果可用餘額大於訂單的總計，則不需要額外的付款方式。 套用至訂單的獎勵點數會與訂單總計一起顯示（從總計中扣除），類似於商店信用卡或禮品卡。 如果獎勵點數與商店信用卡或禮品卡搭配使用，則獎勵點數會先扣除。 如果訂單總計大於可兌換的獎勵點數，則會扣除商店信用卡或禮品卡。

>[!NOTE]
>
>不建議將獎勵點數用於貨到付款採購，因為必須在開立訂單商業發票之後才能確認付款收款。

## 退回獎勵積分

以獎勵點數下單的訂單可退回到獎勵點數餘額，最多可退回到訂單中的金額。 在 [_新增銷退折讓單_ 頁面](../stores-purchase/credit-memo-create.md)，即可輸入套用至客戶餘額的點數。 依預設，欄位包含順序中使用的完整點數。

## 啟用商店的獎勵點作業

獎勵點數設定會決定獎勵點數在商店中的呈現方式，並定義基本操作引數。

![客戶設定 — 獎勵點數](../configuration-reference/customers/assets/reward-points-reward-points.png){width="600" zoomable="yes"}

### 步驟1. 設定獎勵點數

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Customers]** 並選擇 **[!UICONTROL Reward Points]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Reward Points]** 並執行下列動作：

   - 若要啟用獎勵積分，請設定 **[!UICONTROL Enable Reward Points Functionality]** 至 `Yes`.

   - 若要允許客戶取得自己的獎勵積分，請設定 **[!UICONTROL Enable Reward Points Functionality on Storefront]** 至 `Yes`.

   - 若要讓客戶檢視其獎勵的詳細歷史記錄，請設定 **[!UICONTROL Customers May See Reward Point History]** 至 `Yes`.

1. 的 **[!UICONTROL Reward Points Balance Redemption Threshold]**，輸入兌換前必須累積的點數（空白表示沒有最小值）。

1. 的 **[!UICONTROL Cap Reward Points Balance At]**，輸入客戶可累積的最大點數（空白表示無限制）。

1. 的 **[!UICONTROL Reward Points Expire in (days)]**，輸入獎勵點數過期前的天數（無過期天數的空白值）。

1. 設定 **[!UICONTROL Reward Points Expiry Calculation]** 變更為下列其中一項：

   - `Static`  — 根據設定中所設定的天數決定獎勵分數的剩餘期限。 如果設定中的到期限制變更，則現有點的到期日不會變更。

   - `Dynamic`  — 計算獎勵點餘額增加時的剩餘天數。 如果設定中的到期限制變更，則所有現有點的到期時間都會據此更新。

1. 如果您想要自動退款可用的獎勵積分，請設定 **[!UICONTROL Refund Reward Points Automatically]** 至 `Yes`.

1. 如果要自動扣除獎勵積分，請設定 **[!UICONTROL Deduct Reward Points from Refund Amount Automatically]** 至 `Yes`.

1. 設定 **[!UICONTROL Landing Page]** 前往說明您的獎勵積分計畫的內容頁面。

   請務必使用您自己的資訊更新預設的獎勵點數頁面。

1. 完成後，按一下 **[!UICONTROL Save Config]**.

### 步驟2. 設定客戶活動獲得的點數

在此步驟中，會指定可為各種客戶活動取得的獎勵點數。 當客戶完成已指定點的動作時，客戶會看到一則訊息，指出已獲得多少點。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Actions for Acquiring Reward Points by Customer]** 區段。

   ![客戶設定 — 客戶取得獎勵分數的動作](../configuration-reference/customers/assets/reward-points-actions-for-acquiring.png){width="600" zoomable="yes"}

1. 若要在購物車中顯示訊息，其中包含購買所獲得的獎勵點數和客戶目前的獎勵點餘額，請設定 **[!UICONTROL Purchase]** 至 `Yes`.

   >[!NOTE]
   >
   >若要為員工取得獎勵積分， _第一_ 訂購，客戶必須註冊 _早於_ 交易由付款方式擷取。 大部分的付款方法都可以設定為擷取交易 _自動_ 下單時間，但 _早於_ 客戶帳戶註冊已完成。

1. 的 **[!UICONTROL Registration]**，輸入開立客戶帳戶所獲得的點數。

1. 的 **[!UICONTROL Newsletter Signup]**，輸入訂閱電子報的註冊客戶獲得的點數。

1. 的 **[!UICONTROL Converting Invitation to Customer]**，輸入傳送邀請的客戶所獲點數，然後收件者會開啟客戶帳戶。

   您可以限制傳送邀請的客戶可獲得點數的邀請轉換次數（無限制空白）。 若要這麼做，請在 **[!UICONTROL Invitation to Customer Conversions Quantity Limit]** 欄位。

1. 的 **[!UICONTROL Converting Invitation to Order]**，輸入將邀請傳送至收件者（隨後下訂單）的客戶所獲得的點數，並執行下列動作：

   - 的 **訂單轉換邀請數量限制**，輸入當收件者下初始訂單時，傳送邀請的客戶所獲得的點數（空白表示無限制）。

   - 的 **[!UICONTROL Invitation Conversion to Order Reward]**，選取 `Each` 用於取得每個收件者訂單所下的點數的選項，或選取 `First` 僅針對收件者所下第一筆訂單獲得點數的選項。

1. 的 **[!UICONTROL Review Submission]**，輸入客戶提交核准發佈的評論所取得的點數。

1. 然後，要限制可用於獲得每位客戶點數的評論數量，請在 **[!UICONTROL Rewarded Reviews Submission Quantity Limit]** 欄位（空白表示無限制）。

1. 完成後，按一下 **[!UICONTROL Save Config]**.

### 步驟3. 完成電子郵件通知設定

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Email Notification Settings]** 區段。

   ![客戶設定 — 獎勵點電子郵件通知](../configuration-reference/customers/assets/reward-points-email-notification-settings.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Email Sender]** 至顯示為餘額更新和到期通知寄件者的商店聯絡人。

1. 如果您想要依預設訂閱客戶，以接收餘額更新和即將到期日期的通知，請設定 **[!UICONTROL Subscribe Customers by Default]** 至 `Yes`.

1. 設定 **[!UICONTROL Balance Update Email]** 用於每當客戶點數餘額更新時傳送給客戶的通知的範本。

1. 設定 **[!UICONTROL Reward Points Expiry Warning Email]** 批次達到點到期限制時傳送給客戶的通知所使用的範本。

1. 的 **[!UICONTROL Expiry Warning Before (days)]**，輸入該通知的傳送時間在點到期前的天數。

1. 完成後，按一下 **[!UICONTROL Save Config]**.

## 更新獎勵點數餘額

報酬點數餘額可以從管理員進行更新。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. 在格線中尋找客戶，然後按一下 **[!UICONTROL Edit]** 在 _[!UICONTROL Action]_欄。

1. 在 _客戶資訊_，選擇 **[!UICONTROL Reward Points]** 區段。

1. 輸入數字 **[!UICONTROL Update Points]**：

   - 若要更新獎勵點數金額，請輸入數字以增加總點數餘額。
   - 若要減去獎勵點數，請輸入要減少總點數餘額的負數。

1. 輸入 **[!UICONTROL Comments]** 與獎勵積分調整相關（如有需要）。

   ![獎勵點數餘額](./assets/reward-points-balance.png){width="700" zoomable="yes"}

1. 可選擇讓客戶訂閱 _獎勵點數通知_：

   - **[!UICONTROL Subscribe for Balance Updates]**
   - **[!UICONTROL Subscribe for Points Expiration Notifications]**

1. 按一下 **[!UICONTROL Save Customer]**.

所有與獎勵積分相關的動作都會顯示在客戶的 _[!UICONTROL Reward Points History]_封鎖他們在店面的帳戶。

## 欄位說明

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Balance] | 目前使用者端獎勵點數的餘額 |
| [!UICONTROL Amount Balance] | 目前現金餘額的金額 |
| [!UICONTROL Points] | 新增或減去的點數 |
| [!UICONTROL Amount] | 增加或減去的金額 |
| [!UICONTROL Rate] | 此 [獎勵匯率](reward-exchange-rates.md) |
| [!UICONTROL Website] | 已指派獎勵點歷史記錄的網站 |
| [!UICONTROL Reason] | 獎勵點數的理由：<br>**[!UICONTROL Making purchases]**— 客戶每次購買都能獲得點數。<br>**[!UICONTROL Registering on the site]**  — 註冊時累計（一次）。<br>**[!UICONTROL Subscribing to a newsletter]**— 首次訂閱時累積（一次）。<br>**[!UICONTROL Sending Invitations]**  — 邀請朋友加入網站以取得點數。<br>**[!UICONTROL Converting Invitations to Customer]**— 每發出一次邀請，就會獲得點數，主要的朋友會在網站上註冊。<br>**[!UICONTROL Converting Invitations to Order]**  — 每次收到已傳送的邀請即可獲得銷售點數。<br>**[!UICONTROL Review Submission]**— 獲得提交產品評論的點數。 |
| [!UICONTROL Created] | 獎勵點數更新的日期和時間 |
| [!UICONTROL Expired] | 過期的獎勵點數 |
| [!UICONTROL Comment] | 新增或減去點時的註解 |

{style="table-layout:auto"}

## 疑難排解資源

如需疑難排解獎勵點問題的說明，請參閱下列Commerce支援知識庫文章：

- [部分訂單的熟客點數](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-8/mdva-31295-magento-patch-loyalty-points-on-partial-orders.html)
- [404錯誤 — 移除多重運送結帳的獎勵點](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/storefront/magento-2.4.0-404-error-removing-rewards-points-on-multi-shipping-checkout.html)
