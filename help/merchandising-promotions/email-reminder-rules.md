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

電子郵件提醒的目的是鼓勵造訪過您商店的人利用促銷活動進行購買。 當符合一組特定條件時，可以自動傳送電子郵件提醒給客戶。 例如，您可以傳送提醒給已將某專案新增至購物車或願望清單，但尚未購買的客戶。 您可以使用電子郵件提醒來鼓勵客戶返回您的商店，並附上[優惠券代碼](price-rules-cart-coupon.md)作為獎勵。 系統會自動為每批電子郵件提醒產生抵用券代碼，讓您能夠控制每批相關聯的優惠方案。

自購物車放棄後的特定天數過後，或針對您要定義的任何其他條件，可以觸發電子郵件提醒。 常見條件包括購物車總值、數量、購物車中的專案等。

>[!NOTE]
>
>如果客戶有多個相符的放棄購物車、希望清單或兩者的組合，則只會為該客戶觸發一次電子郵件提醒。 若要再次觸發相同的電子郵件提醒，請使用&#x200B;_[!UICONTROL Repeat Schedule]_欄位設定電子郵件之間的天數。

![電子郵件提醒](./assets/email-reminders.png){width="700" zoomable="yes"}

## 設定電子郵件提醒

電子郵件提醒規則可依分鐘、小時或天定期傳送。 此設定會決定批次中會傳送多少電子郵件，以及顯示為訊息寄件者的存放區身分。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Customers]**&#x200B;並選擇&#x200B;**[!UICONTROL Promotions]**。

1. 展開![展開選取器](../assets/icon-display-expand.png) **[!UICONTROL Automated Email Reminder Rules]**&#x200B;區段，然後執行下列動作：

   ![客戶設定 — 自動電子郵件提醒規則](../configuration-reference/customers/assets/promotions-automated-email-reminder-rules.png){width="600" zoomable="yes"}

   - 將&#x200B;**[!UICONTROL Enable Reminder Emails]**&#x200B;設為`Yes`。

   - 若要設定檢查符合自動電子郵件提醒資格的新客戶的頻率，請將&#x200B;**[!UICONTROL Frequency]**&#x200B;設定為下列其中一項：

      - `Minute Intervals`
      - `Hourly`
      - `Daily`

   - 根據&#x200B;_[!UICONTROL Frequency]_設定設定適當的&#x200B;**[!UICONTROL Interval]**。

   - 將&#x200B;**[!UICONTROL Start Time]**&#x200B;設定為根據24小時時鐘傳送電子郵件的時、分、秒。

   - 若要限制批次可傳送的電子郵件數量，請在&#x200B;**[!UICONTROL Maximum Emails per One Run]**&#x200B;欄位中輸入數字。

   - 若要避免重複嘗試傳送失敗的電子郵件，請在&#x200B;**[!UICONTROL Email Send Failure Threshold]**&#x200B;欄位中輸入最大嘗試次數。

   - 將&#x200B;**[!UICONTROL Reminder Email Sender]**&#x200B;設為顯示為提醒電子郵件寄件者的[商店連絡人](../getting-started/store-details.md#store-email-addresses)。

   如需這些選項的詳細清單，請參閱&#x200B;_設定參考_&#x200B;中的[自動電子郵件提醒規則](../configuration-reference/customers/promotions.md#automated-email-reminder-rules)。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

## 電子郵件提醒範本

您可以自訂預設的電子郵件提醒範本，以及為不同促銷活動建立的其他範本。 電子郵件提醒具有可以併入訊息中的特定變數選擇。 這些變數中的資訊由您設定的電子郵件提醒規則，以及與優惠券關聯的購物車價格規則決定。 插入變數按鈕可用來將標籤標籤與變數一起插入範本中。 若要深入瞭解，請參閱[電子郵件](../systems/email-templates.md)。

![電子郵件提醒預覽](./assets/email-reminder-preview-promotion-template.png){width="600" zoomable="yes"}

### 自訂電子郵件提醒範本

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**。

1. 按一下&#x200B;**[!UICONTROL Add New Template]**。

1. 在`Magento_Reminder`下的&#x200B;**[!UICONTROL Template]**&#x200B;清單中，選擇&#x200B;**[!UICONTROL Promotion Notification/Reminder]**&#x200B;範本。

1. 按一下&#x200B;**[!UICONTROL Load Template]**。

依照標準[指示](../systems/email-template-custom.md)自訂範本。

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
