---
title: 客戶現已上線
description: '[!UICONTROL Customers &#x200B;]功能表上的_Now Online_選項會列出您商店中目前線上上的所有客戶和訪客。'
exl-id: 69af669d-f9aa-471b-9d62-5657f3fb2103
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 0%

---

# 客戶現已上線

[!DNL Customers]功能表上的&#x200B;**[!UICONTROL Now Online]**&#x200B;選項列出您商店中目前線上上的所有客戶和訪客。 客戶顯示為目前線上上的時間間隔是在設定中設定，並決定管理員看到[!DNL Customer's]活動的時間。 依預設，間隔為15分鐘。 如果此時未使用鍵盤，工作階段就會結束，客戶必須再次登入帳戶才能繼續購物。 請務必注意，購物車的內容會儲存以供稍後存取。

![線上客戶](assets/customers-now-online.png){width="700" zoomable="yes"}

只有在客戶登入、註冊或任何其他狀態變更事件時，才會更新客戶的線上狀態。 其中包含與購物車相關的事件，例如新增、移除和修改產品。

>[!NOTE]
>
>僅頁面瀏覽不會更新客戶的線上狀態。 若要收集這類資訊，建議[設定Google Analytics](../merchandising-promotions/google-analytics.md) (單獨或搭配[Google Tag Manager](../merchandising-promotions/google-tag-manager.md))，或使用其他分析軟體搭配Adobe Commerce。

## 檢視目前所有線上客戶

在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL Online Now]**。

>[!TIP]
>
>如需協助線上客戶完成購買的詳細資訊，請參閱[購物協助](../stores-purchase/introduction.md#shopping-assistance)。

## 設定時間間隔

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Customers]**&#x200B;並選擇&#x200B;**[!UICONTROL Customer Configuration]**。

1. 展開&#x200B;**[!UICONTROL Online Customers Options]**&#x200B;區段並執行下列動作：

   ![線上客戶選項](../configuration-reference/customers/assets/customer-configuration-online-customers-options.png){width="600" zoomable="yes"}

   - 針對&#x200B;**[!UICONTROL Online Minutes Interval]**，輸入管理員可看見客戶工作階段的分鐘數。 將欄位保留空白以接受15分鐘的預設間隔。

   - 對於&#x200B;**[!UICONTROL Customer Data Lifetime]**，請輸入客戶輸入的任何未儲存資料到期前的分鐘數。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

## 欄說明

| 欄 | 說明 |
| --- | --- |
| **[!UICONTROL ID]** | 註冊客戶的客戶ID。 |
| **[!UICONTROL First Name]** | 註冊客戶的名字。 |
| **[!UICONTROL Last Name]** | 註冊客戶的姓氏。 |
| **[!UICONTROL Email]** | 註冊客戶的電子郵件地址。 |
| **[!UICONTROL Last Activity]** | 客戶上次在您商店中活動的日期和時間。 |
| **[!UICONTROL Type]** | 選項： `Customer` / `Visitor` |
| **[!UICONTROL Last URL]** | 客戶造訪的最後一個URL。 |
| **[!UICONTROL Company]** | 使用者所屬公司的名稱。 |

{style="table-layout:auto"}
