---
title: 購物車持續性
description: 瞭解持續性購物車如何追蹤未購買的購物車專案並儲存資訊，以供客戶下一次造訪。
exl-id: 95c336b3-77ac-4cf6-8fb5-23f4ac4b67d6
feature: Shopping Cart, Configuration
source-git-commit: 26d4bb35c6e1878a8ea8c5f05a982559e5d6dc35
workflow-type: tm+mt
source-wordcount: '1475'
ht-degree: 0%

---

# 購物車持續性

永久性的購物車會追蹤購物車中留下的未購買專案，並儲存客戶下次造訪時的資訊。 _被記住_&#x200B;的客戶下次造訪您的商店時，可以恢復其購物車的內容。

使用永續性購物車有助於減少放棄的購物車數量並提高銷售量。 請務必瞭解，永久性購物車不會隨時揭露敏感的帳戶資訊。 永久購物車在使用中，註冊客戶和訪客購物者都需要登入現有帳戶，或在進行結帳前建立帳戶。 對於訪客購物者而言，永久購物車是擷取先前工作階段資訊的唯一方法。

若要管理您網站或特定商店檢視中的購物車持續使用情形，您可以[設定持續性購物車](#configure-a-persistent-cart)設定。 如需這些設定如何影響店面購物者體驗的詳細資訊，請參閱[持續購物車工作流程](#persistent-cart-workflow)。

>[!NOTE]
>
>使用永續性購物車時，建議您將伺服器工作階段和工作階段Cookie的存留期設定為較長的一段時間。 如需詳細資訊，請參閱[工作階段期限](../customers/customer-online-options.md)。

若要使用持續性購物車，客戶的瀏覽器必須設定為允許Cookie。 用於購物車作業的Cookie有兩種型別：

- **工作階段Cookie** — 短期工作階段Cookie存在於單次造訪您的網站期間，並在客戶離開時或設定的時段後過期。

- **永久性Cookie** — 工作階段結束後會持續存在長期永久性Cookie，並儲存客戶的購物車內容記錄以供日後參考。

## 持續性購物車工作流程

當持續性購物車為[已啟用](#configure-a-persistent-cart)時，工作流程取決於：

- _啟用記住我_&#x200B;的值&#x200B;_在登出時清除持續性_&#x200B;設定
- 客戶決定選取或清除&#x200B;_記住我_&#x200B;核取方塊
- 清除永久性Cookie時

套用永久性Cookie時，頁面標頭中會顯示`Not Jane Smith?`連結。 此提示可讓客戶終止持續工作階段並開始以訪客身分工作，或以其他客戶身分登入。 系統會保留購物車內容的記錄，即使客戶稍後使用不同的裝置在您的商店中購物亦然。 例如，客戶可以從筆記型電腦新增專案至購物車、從行動裝置新增更多專案，以及從平板電腦完成結帳程式。

每個瀏覽器都有獨立的永久性Cookie。 如果客戶在單一持續工作階段中造訪您的商店時使用多個瀏覽器，則頁面重新整理時，在單一瀏覽器中進行的變更會反映在任何其他瀏覽器中。 啟用永久購物車後，您的商店會針對客戶用來登入或建立帳戶的每個瀏覽器，建立和維護個別的永久性Cookie。

### 範例：共用電腦上的開啟工作階段

Jane將以持續的工作階段結束她的節日購物。 她在購物車中為John增加一件禮物，並為她的母親增加一件禮物。 然後她去廚房吃點心。

John在Jane在廚房時，坐在電腦前快速購物。 他未注意到頁面頂端的`Not Jane Smith?`連結，就找到一份適合Jane的禮物，並將其新增到購物車中。 當他去結帳並以個人身份登入時，Jane購物車中的兩個專案都會新增到他的購物車中。 John如此匆忙，以至於他在&#x200B;_訂單稽核_&#x200B;期間沒有注意到其他專案，於是提交了訂單。 Jane的購物車現在空了，而且John買了所有的禮物。

### 記住我

客戶可以選取登入頁面上的&#x200B;_記住我_&#x200B;核取方塊，以儲存購物車的內容。

| 記得我嗎？ | 結果 |
| ------------ |  ------ |
| 已選取 | 建立永久性Cookie並儲存購物車的內容，以供客戶下次登入工作階段使用。 |
| 未選取 | 不會建立永久性Cookie，也不會儲存客戶下次登入工作階段的購物車資訊。 |

{style="table-layout:auto"}

### 在登出時繼續保留 — 否

| 動作 | 結果 |
| ------ | ------ |
| 客戶登入 | 除了工作階段Cookie （已在使用中）之外，還會叫用永久性Cookie。 |
| 客戶登出 | 刪除工作階段Cookie，但永久性Cookie維持有效。 客戶下次登入時，會還原購物車專案或將它們新增至購物車中的任何新專案。 |
| 客戶未登出，且工作階段Cookie過期 | 永久性Cookie會維持有效。 |

{style="table-layout:auto"}

### 清除登出的持續性

| 動作 | 結果 |
| ------ | ------ |
| 客戶登入 | 除了工作階段Cookie （已在使用中）之外，還會叫用永久性Cookie。 |
| 客戶登出 | 刪除兩個Cookie。 |
| 客戶未登出，但工作階段Cookie過期 | 永久性Cookie會維持有效。 |

{style="table-layout:auto"}

## 持續性購物車設定和效果

| 設定 | 效果 |
|----------|--------|
| **[!UICONTROL Enable Remember Me]**&#x200B;已設定為`No`。<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**具有任何值。<br/><br/>登入和註冊頁面上無法使用**&#x200B;記住我&#x200B;**核取方塊。 | 不會使用永久性Cookie。 |
| **[!UICONTROL Enable Remember Me]**&#x200B;已設定為`Yes`。<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**具有任何值。未選取<br/><br/>**&#x200B;記住我&#x200B;**。 | 工作階段Cookie會照常套用，而不會使用永久性Cookie。 |
| **[!UICONTROL Enable Remember Me]**&#x200B;已設定為`Yes`。<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**已設定為`Yes`。<br/><br/>**&#x200B;記住我&#x200B;**設定為`Yes`。 | 客戶登入時，兩個Cookie都會套用。 客戶登出時，兩個Cookie都會刪除。 如果客戶未登入，但工作階段Cookie過期，系統仍會使用永久性Cookie。 除了登出之外，當永久性Cookie的期限耗盡或客戶按一下`Not Jane Smith`連結時，永久性Cookie也會被刪除。 |
| **[!UICONTROL Enable Remember Me]**&#x200B;已設定為`Yes`。<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**已設定為`No`。<br/><br/>**&#x200B;記住我&#x200B;**設定為`Yes` | 客戶登入時，兩個Cookie都會套用。 當客戶登出時，工作階段Cookie會遭到刪除，而持續性工作階段會繼續進行。 永久性Cookie在其期限過後或客戶按一下`Not Jane Smith`連結時被刪除。 |

{style="table-layout:auto"}

## 設定持續性購物車

在設定永久性購物車期間，您可以指定Cookie的生命週期，以及您想要為各種客戶活動提供的選項。

如需有關這些設定如何決定客戶工作流程的詳細資訊，請參閱[持續性購物車工作流程](#persistent-cart-workflow)。

>[!NOTE]
>
>如果工作階段Cookie在客戶登入時過期，則永久性Cookie會維持作用中。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Customers]**&#x200B;並選擇&#x200B;**[!UICONTROL Persistent Shopping Cart]**。

1. 若要啟用持續性購物車並顯示其他選項，請將&#x200B;**[!UICONTROL Enable Persistence]**&#x200B;設為`Yes`。

   ![啟用並設定購物車持續性](../configuration-reference/customers/assets/persistent-shopping-cart-general.png){width="600" zoomable="yes"}

   如需這些組態設定的詳細資訊，請參閱&#x200B;[_組態參考_](../configuration-reference/customers/persistent-shopping-cart.md)

   >[!NOTE]
   >
   >如有需要，請清除&#x200B;**[!UICONTROL Use system value]**&#x200B;核取方塊以修改這些設定。

1. 針對&#x200B;**[!UICONTROL Persistence Lifetime (seconds)]**，輸入您想要永久性Cookie持續的時間長度（以秒為單位）。

   31,536,000秒的預設值等於一年。 允許的時間上限為100年。

1. 將&#x200B;**[!UICONTROL Enable "Remember Me"]**&#x200B;設定為下列其中一項：

   - `Yes` — 在您商店的登入頁面上顯示&#x200B;_記住我_&#x200B;核取方塊，讓客戶可以選擇儲存購物車資訊。

   - `No` — 仍可啟用持續性，但客戶無權選擇是否要儲存其資訊。

1. 若要預先選取客戶的&#x200B;_記住我_&#x200B;核取方塊，請將&#x200B;**[!UICONTROL Remember Me Default Value]**&#x200B;設為`Yes`。

   客戶可以選擇清除此選項。

1. 將&#x200B;**[!UICONTROL Clear Persistence on Log Out]**&#x200B;設定為下列其中一項：

   - `Yes` — 當註冊客戶登出時，會清除購物車。

   - `No` — 當註冊客戶登出時，會儲存購物車。

   >[!NOTE]
   >
   >如果工作階段Cookie在客戶仍然登入時過期，則永久性Cookie會維持使用中。

1. 將&#x200B;**[!UICONTROL Persist Shopping Cart]**&#x200B;設定為下列其中一項：

   - `Yes` — 如果工作階段Cookie過期，永久性Cookie會保留。 如果訪客購物者稍後登入或建立帳戶，購物車就會還原。

   - `No` — 在工作階段Cookie過期後，不會為來賓保留購物車。

1. ![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)設定&#x200B;**[!UICONTROL Persist Wish List]**&#x200B;以判斷工作階段結束時是否保留客戶希望清單的狀態：

   - `Yes` — 工作階段結束時會儲存希望清單內容。

   - `No` — 工作階段結束時未儲存希望清單。

1. ![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)設定&#x200B;**[!UICONTROL Persist Recently Ordered Items]**&#x200B;以判斷工作階段結束時是否保留最近排序專案的狀態：

   - `Yes` — 工作階段結束時會儲存最近訂購專案的狀態。

   - `No` — 工作階段結束時未儲存最近訂購專案的狀態。

1. 將&#x200B;**[!UICONTROL Persist Currently Compared Products]**&#x200B;設為`Yes`或`No`。

1. 將&#x200B;**[!UICONTROL Persist Comparison History]**&#x200B;設為`Yes`或`No`。

1. 將&#x200B;**[!UICONTROL Persist Recently Viewed Products]**&#x200B;設為`Yes`或`No`。

1. ![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)設定&#x200B;**[!UICONTROL Persist Customer Group Membership and Segmentation]**&#x200B;以判斷工作階段結束時是否保留客戶的群組成員資格和細分條件：

   - `Yes` — 在工作階段結束時，會儲存客戶的群組成員資格和細分資料的狀態。

   - `No` — 在工作階段結束時，不會儲存客戶的群組成員資格和細分資料的狀態。

1. 按一下&#x200B;**[!UICONTROL Save Config]**。
