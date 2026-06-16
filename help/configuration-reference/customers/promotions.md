---
title: '[!UICONTROL Customers] > [!UICONTROL Promotions]'
description: 檢閱Commerce管理員的[!UICONTROL Customers] &gt； [!UICONTROL Promotions]頁面上的組態設定。
exl-id: 93035d46-2e9e-466d-a5e3-d69ce6b662b8
feature: Configuration, Promotions/Events
TQID: https://experienceleague.adobe.com/Sc1-Wacd9emNUOl9GabUK-J3OLH-eNX2hvk6m8oyjYc
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 330
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Promotions]

{{config}}

## [!UICONTROL Automated Email Reminder Rules]

{{ee-feature}}

![自動電子郵件提醒規則](./assets/promotions-automated-email-reminder-rules.png)<!-- zoom -->

<!-- [Automated Email Reminder Rules](https://experienceleague.adobe.com/zh-hant/docs/commerce-admin/marketing/communications/email-reminders/email-reminder-rules#configure-email-reminders) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable Reminder Emails] | 全域 | 啟用自動電子郵件提醒。 如果設定為「否」，則會忽略其餘的設定。 選項： `Yes` / `No` |
| [!UICONTROL Frequency] | 全域 | 指出Commerce應檢查符合自動電子郵件提醒資格的新客戶的頻率。 選項： <br/>**`Minute Intervals`**— 根據選取的間隔傳送電子郵件。 （5分鐘、10分鐘、15分鐘、20分鐘或30分鐘）<br/>**`Hourly`** — 每小時傳送電子郵件，在指定小時之後的分鐘傳送。 輸入介於0到59之間的值。<br/>**`Daily`**— 從[開始時間]開始每天傳送電子郵件。 |
| [!UICONTROL Interval] | 全域 | 間隔應等於或大於您的cron.php啟動週期。 選項： `5 minutes` / `10 minutes` / `15 minutes` / `20 minutes` / `30 minutes` |
| [!UICONTROL Start Time] | 全域 | 設定傳送電子郵件的日期、分鐘和秒數。 根據您伺服器上的系統時間，以24小時格式指定。 |
| [!UICONTROL Maximum Emails per One Run] | 全域 | 限制排程區塊中傳送的電子郵件數量。 |
| [!UICONTROL Email Send Failure Threshold] | 全域 | 提醒嘗試將通知傳送至特定電子郵件地址並失敗的次數。 當值設為0時，沒有臨界值，並且儘管發生任何失敗，仍會繼續傳送通知。 |
| [!UICONTROL Reminder Email Sender] | 存放區檢視 | 顯示為電子郵件寄件者的商店身分。 |

{style="table-layout:auto"}

## [!UICONTROL Auto Generated Specific Coupon Codes]

![自動產生特定優惠券代碼](./assets/promotions-auto-generated-specific-coupon-codes.png)<!-- zoom -->

<!-- [Auto Generated Specific Coupon Codes](https://experienceleague.adobe.com/zh-hant/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart-coupon#configure-coupon-codes)  -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Code Length] | 全域 | 定義抵用券代碼的長度，不包括首碼、尾碼和分隔符號。 |
| [!UICONTROL Code Format] | 全域 | 定義優惠券的程式碼格式。 選項包括： <br/>**`Alphanumeric`**— 任何字母和數字的組合。<br/>**`Alphabetical`** — 僅限字母。<br/>**`Numeric`**— 僅限數字。 |
| [!UICONTROL Code Prefix] | 全域 | 附加至所有抵用券代碼開頭的值。 如果您不想使用首碼，請將此欄位留空。 |
| [!UICONTROL Code Suffix] | 全域 | 附加至所有程式碼結尾的值。 如果您不想使用尾碼，請將此欄位留空。 |
| [!UICONTROL Dash Every X Characters] | 全域 | 在所有優惠券代碼中插入破折號(-)的間隔。 如果您不想使用破折號，請將此欄位留空。 <br/>_&#x200B;**注意：**&#x200B;_&#x200B;只有破折號不同的優惠券代碼會被視為不同的代碼。 |

{style="table-layout:auto"}
