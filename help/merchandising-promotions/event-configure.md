---
title: 設定事件
description: 瞭解如何在店面側邊欄中完成基本設定，以啟用事件並設定事件區塊。
exl-id: 620b2d60-ce6f-4f31-93bb-18d3dd9cdce6
feature: Marketing Tools, Promotions/Events
source-git-commit: 084d2c3381f57a8a4c7e8ffde9da1abd4d8af670
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# 設定事件

{{ee-feature}}

您必須先完成基本設定以啟用事件，並在側邊欄中設定事件區塊，才能建立事件。

## 啟用和設定事件

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Catalog]** 並選擇 **[!UICONTROL Catalog]** 底下。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Catalog Events]** 並執行下列動作：

   ![目錄設定 — 目錄事件](../configuration-reference/catalog/assets/catalog-events.png){width="600" zoomable="yes"}

   - 設定 **[!UICONTROL Enable Catalog Events Functionality]** 至 `Yes`.

   - 設定 **[!UICONTROL Enable Catalog Event Widget on Storefront]** 至 `Yes`.

   - 輸入 **[!UICONTROL Number of Events to be Displayed in the Event Slider Sidebar Widget]**. 根據預設，此值會設為 `5`. 如果一次只想在滑桿中顯示一個事件，請輸入 `1`.

   - 輸入數字 **[!UICONTROL Events to Scroll per Click in Event Slider Sidebar Widget]**. 根據預設，此值會設為 `2`. 如果您希望滑桿在按一下時依序顯示下一個事件，請輸入 `1`.

1. 完成後，按一下 **[!UICONTROL Save Config]**.

## 存取限制

私人銷售、活動或網站的存取權可限制給登入的註冊客戶，或延伸給在取得存取權之前必須註冊的未註冊客戶。

![一般設定 — 網站限制](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

### 限制存取

私人銷售、活動或網站的存取權可限制給登入的註冊客戶，或延伸給在取得存取權之前必須註冊的未註冊客戶。

![一般設定 — 網站限制](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL General]** 並選擇 **[!UICONTROL General]** 底下。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Website Restrictions]** 區段。

1. 設定 **[!UICONTROL Access Restriction]** 至 `Yes`.

1. 設定 **[!UICONTROL Restriction Mode]** 變更為下列其中一項：

   - `Website Closed`
   - `Private Sales: Login Only`
   - `Private Sales: Login and Register`

1. 設定 **[!UICONTROL Startup Page]** 變更為下列其中一項：

   - `To login form (302 Found)`  — 在存取網站之前，系統會將使用者重新導向至登入表單。

   - `To landing page (302 Found)`  — 系統會將使用者重新導向至指定的登陸頁面，直到他們登入為止。

     >[!IMPORTANT]
     >
     >請務必加入登陸頁面之登入頁面的連結，讓客戶能登入存取網站。

1. 選擇 **[!UICONTROL Landing Page]** 在客戶登入私人銷售網站之前顯示。

1. 讓搜尋引擎機器人和編目程式知道登陸頁面正確，網站上沒有其他頁面可編列索引，請設定 **[!UICONTROL HTTP Response]** 至 `200 OK`.

   在所有其他情況下，將設為 `503 Service Unavailable`.

   >[!NOTE]
   >
   >僅在限制模式設定為時適用 _網站已關閉_. 登入頁面會呈現為原始HTML。

1. 如果您希望客戶登入和忘記密碼表單中的欄位自動填寫先前輸入項，請設定 **[!UICONTROL Enable Autocomplete on login/forgot password forms]** 至 `Yes`.

1. 完成後，按一下 **[!UICONTROL Save Config]**.

### 限制銷售

依預設，在即將發生或已關閉的事件中出現的產品不可用於一般銷售和 _[!UICONTROL Add to Cart]_按鈕未出現在產品清單或產品頁面上。

若要還原 _[!UICONTROL Add to Cart]_按鈕時，必須刪除該事件(請參閱 [更新事件](event-create.md#update-events))。 不過，如果產品與另一個沒有銷售限制的類別相關聯，則產品頁面上會提供此按鈕。 同樣地，如果產品與沒有銷售限制的其他類別相關聯，則股票代號區塊不會出現在產品頁面上。
