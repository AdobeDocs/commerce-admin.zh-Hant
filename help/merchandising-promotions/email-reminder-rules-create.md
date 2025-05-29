---
title: 建立電子郵件提醒
description: 瞭解如何設定使用現有購物車價格規則的電子郵件提醒規則。
exl-id: b04dc8a3-5daa-43f2-bf52-d85bfd2554b7
feature: Merchandising, Communications
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"
source-git-commit: 7e28081ef2723d4113b957edede6a8e13612ad2f
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 0%

---

# 建立電子郵件提醒

設定電子郵件提醒規則之前，您必須先[設定購物車價格規則](price-rules-cart-create.md)，以定義所提供的促銷活動。 觸發電子郵件提醒的規則條件可以根據購物車屬性、願望清單屬性或兩者。

>[!NOTE]
>
>電子郵件提醒可能會促銷包含或不包含抵用券的購物車價格規則。 定義自動產生抵用券的購物車價格規則，會為每個客戶產生隨機抵用券代碼。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Reminder Rules]**。

1. 按一下右上角的&#x200B;**[!UICONTROL Add New Rule]**。

1. 完成&#x200B;_[!UICONTROL Rule Information]_，如下所示：

   ![電子郵件提醒規則](./assets/email-reminder-new.png){width="700" zoomable="yes"}

   - 輸入&#x200B;**[!UICONTROL Rule Name]**&#x200B;以在內部識別規則。

   - 輸入規則的簡短&#x200B;**[!UICONTROL Description]**。

   - 若要選擇此提醒要通告的&#x200B;**[!UICONTROL Cart Price Rule]**&#x200B;促銷活動，請按一下&#x200B;**[!UICONTROL Select Rule…]**，然後選取規則。

     ![購物車規則 — 選取](./assets/email-reminder-select-rule.png){width="600" zoomable="yes"}

   - 若要讓規則立即生效，請將&#x200B;**[!UICONTROL Status]**&#x200B;設為`Active`。

   - 若要設定規則生效的日期範圍，請輸入&#x200B;**[!UICONTROL From]**&#x200B;和&#x200B;**[!UICONTROL To]**&#x200B;日期。

     您也可以從行事曆選擇日期（ ![行事曆圖示](../assets/icon-calendar.png) ）。

   - 若要多次傳送提醒，請在&#x200B;**[!UICONTROL Repeat Schedule]**&#x200B;欄位中輸入下次傳送電子郵件前的天數。

1. 在左側的面板中，選擇&#x200B;**[!UICONTROL Conditions]**。

   必須為規則定義至少一個條件。 此程式類似於建置[目錄價格規則。](price-rules-catalog.md)

   ![電子郵件提醒條件](./assets/email-reminder-conditions.png){width="600" zoomable="yes"}

   按一下&#x200B;_新增_ （![新增圖示](../assets/icon-add-green-circle.png)）以顯示選項清單，然後選擇下列條件之一：

   - 希望清單
   - 購物車

   >[!NOTE]
   >
   >如果客戶有多個相符的放棄購物車、希望清單或兩者的組合，則只會為該客戶觸發一次電子郵件提醒。 若要再次觸發相同的電子郵件提醒，請使用&#x200B;_[!UICONTROL Repeat Schedule]_欄位設定電子郵件之間的天數。<br/>
   >
   >**_新_**&#x200B;放棄的購物車&#x200B;**_之後_** _[!UICONTROL Repeat Schedule]_期間結束後，同一客戶的&#x200B;**_未重新觸發_**相同的電子郵件提醒。

   完成條件以說明觸發電子郵件提醒的情境。

   ![電子郵件提醒條件範例](./assets/email-reminder-condition-example.png){width="600" zoomable="yes"}

1. 在左側的面板中，選擇&#x200B;**[!UICONTROL Emails and Labels]**。

   ![電子郵件提醒規則 — 電子郵件和標籤範本](./assets/email-reminder-rule-emails-labels-email-templates.png){width="600" zoomable="yes"}

1. 在&#x200B;**[!UICONTROL Email Templates]**&#x200B;區段中，選擇要用於您[商店階層](../getting-started/websites-stores-views.md)中每個網站和商店檢視的電子郵件範本。

   如果您不想傳送提醒電子郵件給商店檢視的客戶，請保留值`Not Selected`。

1. 在&#x200B;_預設標題和說明_&#x200B;區段中，執行下列動作：

   - 輸入&#x200B;**[!UICONTROL Rule Title for All Store Views]**。

     >[!NOTE]
     >
     >此值可以使用`promotion_name`變數合併到電子郵件範本中。

   - 輸入&#x200B;**[!UICONTROL Rule Description for All Store Views]**。

     ![電子郵件提醒 — 標題和說明](./assets/email-reminders-emails-and-labels-default-titles-description.png){width="500" zoomable="yes"}

   - 在&#x200B;_[!UICONTROL Titles and Descriptions Per Store View]_區段中，輸入_&#x200B;預設存放區檢視&#x200B;_的&#x200B;**[!UICONTROL Rule Title]**和&#x200B;**[!UICONTROL Description]**。 針對多個商店檢視，輸入每個商店檢視的適當標題和說明。

     >[!NOTE]
     >
     >使用promotion_description變數可將說明併入電子郵件範本。

     ![標題和說明 — 商店檢視](./assets/email-reminder-rules-title-descriptions-per-store-view.png){width="500" zoomable="yes"}

1. 完成時，按一下&#x200B;**[!UICONTROL Save]**。

## 觸發條件

| Source | 觸發 |
|--- |--- |
| [!UICONTROL Wish List] | [!UICONTROL Conditions Combination]<br/>[!UICONTROL Sharing]<br/>[!UICONTROL Number of Items]<br/>[!UICONTROL Items Sub selection] |
| [!UICONTROL Shopping Cart] | [!UICONTROL Conditions Combination]<br/>[!UICONTROL Coupon Code]<br/>[!UICONTROL Cart Line Items]<br/>[!UICONTROL Items Quantity]<br/>[!UICONTROL Virtual Only]<br/>[!UICONTROL Total Amount]<br/>[!UICONTROL Items Subselection] |

{style="table-layout:auto"}

## 欄位說明

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Rule Name] | 自動提醒規則的名稱，可在內部識別規則。 |
| [!UICONTROL Description] | 供內部參考的規則說明。 |
| [!UICONTROL Shopping Cart Price Rule] | 與此電子郵件提醒相關聯的購物車規則。 提醒電子郵件可促銷附有或不附贈券的購物車價格規則。 如果購物車價格規則包含自動產生的優惠券，則提醒規則會為每個客戶產生隨機、唯一的優惠券代碼。 |
| [!UICONTROL Assigned to Website] | 根據此規則接收自動提醒電子郵件的網站。 |
| [!UICONTROL Status] | 啟動規則。 如果狀態為非使用中，則會忽略所有其他設定，且不會觸發規則。 選項： `Active` / `Inactive` |
| [!UICONTROL From Date] | 此自動提醒規則的開始日期。 若未指定日期，規則會立即生效。 |
| [!UICONTROL To Date] | 此自動提醒規則的結束日期。 如果未指定日期，規則會無限期地啟用。 |
| [!UICONTROL Repeat Schedule] | 觸發規則前的天數，並在符合條件時再次傳送提醒電子郵件。 若要觸發規則多次，請輸入下次傳送電子郵件前的天數（以逗號分隔）。 例如，輸入`7`讓規則在七天後再次觸發；輸入`7,14`讓規則在七天後再次觸發，並在14天後再次觸發。 |
| [!UICONTROL Email Templates] | 決定用於每個商店檢視的電子郵件範本。 |
| [!UICONTROL Rule Title for All Store Views] | 決定每個存放區檢視的規則標題。 |
| [!UICONTROL Rule Description for All Store Views] | 決定每個存放區檢視的規則說明。 |

{style="table-layout:auto"}
