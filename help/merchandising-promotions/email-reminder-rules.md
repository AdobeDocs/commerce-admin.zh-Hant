---
title: 電子郵件提醒
description: 瞭解在滿足特定條件時會自動傳送給客戶的電子郵件提醒。
exl-id: 3293caca-9dd3-4d64-a80c-58c92a9208e5
feature: Merchandising, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 0%

---

# 電子郵件提醒

{{ee-feature}}

電子郵件提醒的目的是鼓勵造訪過您商店的人利用促銷活動進行購買。 當符合一組特定條件時，可以自動傳送電子郵件提醒給客戶。 例如，您可以傳送提醒給已將某專案新增至購物車或願望清單，但尚未購買的客戶。 您可以使用電子郵件提醒來鼓勵客戶回訪您的商店，並加入 [抵用券代碼](price-rules-cart-coupon.md) 作為獎勵。 系統會自動為每批電子郵件提醒產生抵用券代碼，讓您能夠控制每批相關聯的優惠方案。

自購物車放棄後的特定天數過後，或針對您要定義的任何其他條件，可以觸發電子郵件提醒。 常見條件包括購物車總值、數量、購物車中的專案等。

>[!NOTE]
>
>如果客戶有多個相符的放棄購物車、希望清單或兩者的組合，則只會為該客戶觸發一次電子郵件提醒。 若要再次觸發相同的電子郵件提醒，請使用 _[!UICONTROL Repeat Schedule]_欄位以設定電子郵件之間的天數。

![電子郵件提醒](./assets/email-reminders.png){width="700" zoomable="yes"}

## 設定電子郵件提醒

電子郵件提醒規則可依分鐘、小時或天定期傳送。 此設定會決定批次中會傳送多少電子郵件，以及顯示為訊息寄件者的存放區身分。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Customers]** 並選擇 **[!UICONTROL Promotions]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Automated Email Reminder Rules]** 並執行下列動作：

   ![客戶設定 — 自動電子郵件提醒規則](../configuration-reference/customers/assets/promotions-automated-email-reminder-rules.png){width="600" zoomable="yes"}

   - 設定 **[!UICONTROL Enable Reminder Emails]** 至 `Yes`.

   - 若要設定對符合自動化電子郵件提醒資格的新客戶執行檢查的頻率，請設定 **[!UICONTROL Frequency]** 變更為下列其中一項：

      - `Minute Intervals`
      - `Hourly`
      - `Daily`

   - 設定適當的 **[!UICONTROL Interval]**，根據 _[!UICONTROL Frequency]_設定。

   - 設定 **[!UICONTROL Start Time]** 根據24小時時鐘，傳送電子郵件的時間（小時、分鐘和秒）。

   - 若要限制批次可傳送的電子郵件數量，請在 **[!UICONTROL Maximum Emails per One Run]** 欄位。

   - 若要避免重複嘗試傳送失敗的電子郵件，請在 **[!UICONTROL Email Send Failure Threshold]** 欄位。

   - 設定 **[!UICONTROL Reminder Email Sender]** 至 [商店聯絡人](../getting-started/store-details.md#store-email-addresses) 顯示為提醒電子郵件的寄件者。

   如需這些選項的詳細清單，請參閱 [自動電子郵件提醒規則](../configuration-reference/customers/promotions.md#automated-email-reminder-rules) 在 _設定參考_.

1. 完成後，按一下 **[!UICONTROL Save Config]**.

## 電子郵件提醒範本

您可以自訂預設的電子郵件提醒範本，以及為不同促銷活動建立的其他範本。 電子郵件提醒具有可以併入訊息中的特定變數選擇。 這些變數中的資訊由您設定的電子郵件提醒規則，以及與優惠券關聯的購物車價格規則決定。 插入變數按鈕可用來將標籤標籤與變數一起插入範本中。 若要深入瞭解，請參閱 [電子郵件](../systems/email-templates.md).

![電子郵件提醒預覽](./assets/email-reminder-preview-promotion-template.png){width="600" zoomable="yes"}

### 自訂電子郵件提醒範本

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. 按一下 **[!UICONTROL Add New Template]**.

1. 在 **[!UICONTROL Template]** 清單在 `Magento_Reminder`，選擇 **[!UICONTROL Promotion Notification/Reminder]** 範本。

1. 按一下 **[!UICONTROL Load Template]**.

遵循標準 [指示](../systems/email-template-custom.md) 以自訂範本。

### 電子郵件提醒變數

#### 抵用券代碼

```
{{var coupon.getCode()|escape}}
```

#### 優惠券使用量限制

```
{{var coupon.usage_limit|escape}}
```

#### 每位客戶的優惠券使用量

```
{{var coupon.usage_per_customer|escape}}
```

#### 客戶帳戶URL

```
{{var this.getUrl($store,'customer/account/',[_nosid:1])}}
```

#### 客戶名稱

```
{{var customer_data.name|escape}}
```

#### 電子郵件頁尾範本

```
{{template config_path="design/email/footer_template"}}
```

#### 電子郵件標頭範本

```
{{template config_path="design/email/header_template"}}
```

#### 電子郵件標誌影像替代方案

```
{{var logo_alt}}
```

#### 電子郵件標誌影像URL

```
{{var logo_url}}
```

#### 促銷活動說明

```
{{var promotion_description|escape|nl2br}}
```

#### 促銷活動名稱

```
{{var promotion_name|escape}}
```

#### 存放區名稱

```
{{var store.frontend_name}}
```

#### 商店URL

```
{{store url=""}}
```
