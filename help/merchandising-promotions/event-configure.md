---
title: 設定事件
description: 瞭解如何在店面側邊欄中完成基本設定，以啟用事件並設定事件區塊。
exl-id: 620b2d60-ce6f-4f31-93bb-18d3dd9cdce6
feature: Marketing Tools, Promotions/Events
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"
source-git-commit: 7e28081ef2723d4113b957edede6a8e13612ad2f
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 0%

---

# 設定事件

{{ee-feature}}

您必須先完成基本設定以啟用事件，並在側邊欄中設定事件區塊，才能建立事件。

## 啟用和設定事件

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Catalog]**&#x200B;並在下方選擇&#x200B;**[!UICONTROL Catalog]**。

1. 展開![展開選取器](../assets/icon-display-expand.png) **[!UICONTROL Catalog Events]**&#x200B;區段，然後執行下列動作：

   ![目錄組態 — 目錄事件](../configuration-reference/catalog/assets/catalog-events.png){width="600" zoomable="yes"}

   - 將&#x200B;**[!UICONTROL Enable Catalog Events Functionality]**&#x200B;設為`Yes`。

   - 將&#x200B;**[!UICONTROL Enable Catalog Event Widget on Storefront]**&#x200B;設為`Yes`。

   - 輸入&#x200B;**[!UICONTROL Number of Events to be Displayed in the Event Slider Sidebar Widget]**。 預設情況下，此值設定為`5`。 如果您一次只想在滑桿中顯示一個事件，請輸入`1`。

   - 輸入&#x200B;**[!UICONTROL Events to Scroll per Click in Event Slider Sidebar Widget]**&#x200B;的數字。 預設情況下，此值設定為`2`。 如果您希望滑桿在按一下時依序顯示下一個事件，請輸入`1`。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

## 存取限制

私人銷售、活動或網站的存取權可限制給登入的註冊客戶，或延伸給在取得存取權之前必須註冊的未註冊客戶。

![一般設定 — 網站限制](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

### 限制存取

私人銷售、活動或網站的存取權可限制給登入的註冊客戶，或延伸給在取得存取權之前必須註冊的未註冊客戶。

![一般設定 — 網站限制](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL General]**&#x200B;並在下方選擇&#x200B;**[!UICONTROL General]**。

1. 展開&#x200B;**[!UICONTROL Website Restrictions]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

1. 將&#x200B;**[!UICONTROL Access Restriction]**&#x200B;設為`Yes`。

1. 將&#x200B;**[!UICONTROL Restriction Mode]**&#x200B;設定為下列其中一項：

   - `Website Closed`
   - `Private Sales: Login Only`
   - `Private Sales: Login and Register`

1. 將&#x200B;**[!UICONTROL Startup Page]**&#x200B;設定為下列其中一項：

   - `To login form (302 Found)` — 在取得網站的存取權之前，會將使用者重新導向至登入表單。

   - `To landing page (302 Found)` — 系統會將使用者重新導向至指定的登陸頁面，直到他們登入為止。

     >[!IMPORTANT]
     >
     >請務必加入登陸頁面之登入頁面的連結，讓客戶能登入存取網站。

1. 選擇客戶登入私人銷售網站前顯示的&#x200B;**[!UICONTROL Landing Page]**。

1. 若要讓搜尋引擎機器人和編目程式知道登入頁面正確，且網站上沒有其他頁面可編列索引，請將&#x200B;**[!UICONTROL HTTP Response]**&#x200B;設為`200 OK`。

   在所有其他情況下，設定為`503 Service Unavailable`。

   >[!NOTE]
   >
   >僅當限制模式設定為&#x200B;_網站已關閉_&#x200B;時才適用。 登入頁面會呈現為原始HTML。

1. 如果您希望客戶登入及忘記密碼表單中的欄位自動填寫先前專案的欄位，請將&#x200B;**[!UICONTROL Enable Autocomplete on login/forgot password forms]**&#x200B;設為`Yes`。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

### 限制銷售

依預設，在即將發生或已關閉的事件中出現的產品不可用於一般銷售，且&#x200B;_[!UICONTROL Add to Cart]_按鈕未出現在產品清單或產品頁面上。

若要還原已關閉事件的&#x200B;_[!UICONTROL Add to Cart]_按鈕，必須刪除該事件（請參閱[更新事件](event-create.md#update-events)）。 不過，如果產品與另一個沒有銷售限制的類別相關聯，則產品頁面上會提供此按鈕。 同樣地，如果產品與沒有銷售限制的其他類別相關聯，則股票代號區塊不會出現在產品頁面上。
