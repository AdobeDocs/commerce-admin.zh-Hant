---
title: '[!UICONTROL Customers] &amp；gt； [!UICONTROL Reward Points]'
description: 檢閱Commerce管理員的[!UICONTROL Customers] &amp；gt； [!UICONTROL Reward Points]頁面上的組態設定。
exl-id: 0b7f8806-74c5-4467-87da-0faae50f164b
feature: Configuration, Rewards
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '781'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Reward Points]

{{ee-feature}}

{{config}}

>[!NOTE]
>
>在結帳期間由客戶和管理員兌換獎勵點數需要[獎勵匯率](../../merchandising-promotions/reward-exchange-rates.md)設定。

## [!UICONTROL Reward Points]

![獎勵點數](./assets/reward-points-reward-points.png)<!-- zoom -->

<!-- [Reward Points](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/merchandising/reward-points/rewards-loyalty#enable-reward-point-operations-for-your-store) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Reward Points Functionality] | 全域 | 啟用或停用獎勵點數。 選項： `Yes` / `No`。 |
| [!UICONTROL Enable Reward Points Functionality on Storefront] | 網站 | 啟用後，客戶可透過其活動取得點數，並在結帳時兌換點數。 如果停用，只有管理員使用者可以代表客戶指派和兌換點數。 選項： `Yes` / `No`。 |
| [!UICONTROL Customers May See Reward Points History] | 網站 | 啟用後，客戶可以在帳戶儀表板中檢視每個應計、贖回和獎勵點數到期的詳細歷史記錄。 選項： `Yes` / `No` |
| [!UICONTROL Reward Points Balance Redemption Threshold] | 網站 | 要求客戶必須先達到最低點數餘額，才能兌換訂單。 保留空白則沒有最小值。 |
| [!UICONTROL Cap Reward Points Balance At] | 網站 | 防止客戶累積超過此最大點數餘額。 保留空白則沒有上限。 |
| [!UICONTROL Reward Points Expire in (days)] | 網站 | 表示獎勵點數的期限（以天為單位）。 在個別活動中獲得的每一批次點數都有個別的生命週期。 「獎勵點數」記錄中的每一批次會指出點數到期前的剩餘天數。 歷史紀錄可從客戶的帳戶控制面板（若已啟用）以及管理員檢視。 保留空白則不會過期。 |
| [!UICONTROL Reward Points Expiry Calculation] | 網站 | 決定用來決定獎勵點數何時過期的方法。 選項： <br/>**`Static`**— 根據設定中所設定的天數，決定獎勵分數的剩餘期限。 如果設定中的到期限制變更，則現有點的到期日不會變更。<br/>**`Dynamic`** — 計算當獎勵點餘額增加時剩餘的天數。 如果組態中的到期限制變更，則所有現有點的到期計算都會隨之更新。 |
| [!UICONTROL Refund Reward Points Automatically] | 全域 | 決定是否自動退款可用的獎勵積分。 選項： `Yes` / `No` |
| [!UICONTROL Deduct Reward Points from Refund Amount Automatically] | 全域 | 當啟用此功能時，這會決定透過採購取得的獎勵點數是完全或部分作廢訂單退款。 當訂單退款時，只會影響已取得之訂單的獎勵積分。 選項： `Yes` / `No`。 |
| [!UICONTROL Landing Page] | 存放區檢視 | 指定說明您的獎勵積分方案的CMS頁面。 預設「獎勵」頁面的連結會出現在商店中可以取得點數的位置。 |

{style="table-layout:auto"}

## [!UICONTROL Actions for Acquiring Reward Points by Customers]

客戶取得獎勵點數的![動作](./assets/reward-points-actions-for-acquiring.png)<!-- zoom -->

<!-- [Actions for Acquiring Reward Points by Customers](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/merchandising/reward-points/rewards-loyalty#enable-reward-point-operations-for-your-store) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Purchase] | 網站 | 根據設定的[獎勵匯率](../../merchandising-promotions/reward-exchange-rates.md)，判斷購買是否獲得獎勵積分。 選項： `Yes` / `No` |
| [!UICONTROL Registration] | 網站 | 指定開立客戶帳戶所獲得的點數。 |
| [!UICONTROL Newsletter Signup] | 網站 | 指定訂閱電子報的註冊客戶獲得的點數。 （訪客的訂閱無法使用點數。） 如果客戶取消訂閱，然後再次訂閱，則不會獲得第二個訂閱的點數。 |
| [!UICONTROL Converting Invitation to Customer] | 網站 | 指定當收件者接著開啟客戶帳戶時，傳送邀請的客戶獲得點數。 |
| [!UICONTROL Invitation to Customer Conversions Quantity Limit] | 網站 | 限制傳送邀請的客戶可獲得點數的邀請轉換次數。 保留空白則無限制。 |
| [!UICONTROL Converting Invitation to Order] | 網站 | 指定當收件者下初始訂單時，傳送邀請的客戶獲得點數。 |
| [!UICONTROL Invitation to Order Conversions Quantity Limit] | 網站 | 限制訂單轉換次數，此轉換次數可為傳送邀請的人員取得點數。 如果空白，則沒有上限。 |
| [!UICONTROL Invitation Conversion to Order Reward] | 網站 | 表示受邀者購買產品時，客戶獲得獎勵分數的頻率。 選項： <br/>**`Each`**— 客戶會收到受邀者所下每個已開立商業發票訂單的獎勵積分。 系統會根據網站與客戶群組所需組合所設定的匯率，提供獎勵積分。<br/>**`First`** — 客戶只會收到受邀者所下的第一筆已開立商業發票訂單的獎勵積分。 如果有多位受邀者註冊並下訂單，則只有第一筆訂單的金額會轉換為獎勵點數並授予客戶。 |
| [!UICONTROL Review Submission] | 網站 | 決定客戶提交核准發佈的稽核所獲得的點數。 |
| [!UICONTROL Rewarded Reviews Submission Quantity Limit] | 網站 | 限制可用於取得每位客戶點數的評論數量。 保留空白則無限制。 |

{style="table-layout:auto"}

## [!UICONTROL Email Notification Settings]

![電子郵件通知設定](./assets/reward-points-email-notification-settings.png)<!-- zoom -->

<!-- [Email Notification Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/merchandising/reward-points/rewards-loyalty#enable-reward-point-operations-for-your-store) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Email Sender] | 存放區檢視 | 決定顯示為餘額更新和到期通知電子郵件寄件者的商店聯絡人。 |
| [!UICONTROL Subscribe Customers by Default] | 全域 | 決定客戶在餘額更新和到期通知電子郵件中的預設訂閱狀態。 |
| [!UICONTROL Balance Update Email] | 存放區檢視 | 決定當客戶的點數餘額更新時，傳送給客戶的通知所使用的範本。 預設範本： `Reward Points Balance Update` |
| [!UICONTROL Reward Points Expiry Warning Email] | 存放區檢視 | 決定當達到批次點的到期警告限制時，客戶收到的電子郵件範本。 預設範本： `Reward Points Expiry Warning` |
| [!UICONTROL Expiry Warning before (days)] | 全域 | 指定在點到期之前傳送通知的天數。 留空將不傳送到期通知。 如果輸入的天數大於點的剩餘存留期，則不會傳送通知。 |

{style="table-layout:auto"}
