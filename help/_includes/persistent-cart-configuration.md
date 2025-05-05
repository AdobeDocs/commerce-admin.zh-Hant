---
title: 持續性購物車的設定參考
description: 持續性購物車的設定參考的可重複使用內容。
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---


# [!UICONTROL General Options]

![一般選項](/help/configuration-reference/customers/assets/persistent-shopping-cart-general.png)<!-- zoom -->

<!-- [General Options](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-persistent#configure-a-persistent-cart) -->

| 欄位 | [領域](/help/getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |------------------------------------------------------------------------|--- |
| [!UICONTROL Enable Persistence] | 網站 | 決定是否啟用持續性功能。 |
| [!UICONTROL Persistence Lifetime (seconds)] | 網站 | 定義永久性Cookie的生命週期（以秒為單位）。 允許的最大值為34560000秒（400天）。 這是建議Cookie存留期上限的限制。 |
| [!UICONTROL Enable "Remember Me"] | 網站 | 定義是否要在商店的登入與註冊頁面上顯示&#x200B;_記住我_&#x200B;核取方塊。 選項： <br/>**`Yes`**— 顯示&#x200B;_記住我_核取方塊。<br/>**`No`** — 不顯示&#x200B;_記住我_&#x200B;核取方塊，永久性Cookie僅供已有該永久性Cookie的客戶使用。 |
| [!UICONTROL "Remember Me" Default Value] | 網站 | 定義&#x200B;_記住我_&#x200B;核取方塊的預設狀態。 |
| [!UICONTROL Clear Persistence on Log Out] | 網站 | 定義當商店客戶登出時是否刪除永久性Cookie。 無論此選項的設定方式為何，如果客戶未登出，但工作階段Cookie過期，仍會使用永久性Cookie。 |
| [!UICONTROL Persist Shopping Cart] | 網站 | 定義使用永久性Cookie是否會提供對應帳戶之購物車資料的存取權。 選項： <br/>**`Yes`**&#x200B;或&#x200B;**`No`**。 |
| [!UICONTROL Persist Wish List] | 網站 | ![Adobe Commerce](/help/assets/adobe-logo.svg) (僅限Adobe Commerce)決定工作階段結束時是否保留客戶願望清單的狀態。 選項： <br/>**`Yes`**— 在工作階段結束時儲存希望清單內容。<br/>**`No`** — 工作階段結束時未儲存希望清單。 |
| [!UICONTROL Persist Recently Ordered Items] | 網站 | ![Adobe Commerce](/help/assets/adobe-logo.svg) (僅限Adobe Commerce)決定是否在工作階段結束時儲存最近排序專案的狀態。 選項： <br/>**`Yes`**&#x200B;或&#x200B;**`No`**。 |
| [!UICONTROL Persist Currently Compared Products] | 網站 | ![Adobe Commerce](/help/assets/adobe-logo.svg) (僅限Adobe Commerce)判斷工作階段結束時，目前比較的產品狀態是否保留。 選項： <br/>**`Yes`**&#x200B;或&#x200B;**`No`**。 |
| [!UICONTROL Persist Comparison History] | 網站 | ![Adobe Commerce](/help/assets/adobe-logo.svg) (僅限Adobe Commerce)判斷工作階段結束時是否保留比較歷程記錄的狀態。 選項： <br/>**`Yes`**&#x200B;或&#x200B;**`No`**。 |
| [!UICONTROL Persist Recently Viewed Products] | 網站 | ![Adobe Commerce](/help/assets/adobe-logo.svg) (僅限Adobe Commerce)判斷工作階段結束時，是否保留最近檢視產品的狀態。 選項： <br/>**`Yes`**&#x200B;或&#x200B;**`No`**。 |
| [!UICONTROL Persist Customer Group Membership and Segmentation] | 網站 | ![Adobe Commerce](/help/assets/adobe-logo.svg) (僅限Adobe Commerce)決定工作階段結束時，是否保留客戶群組成員資格和細分條件的狀態。 選項： <br/>**`Yes`**— 在工作階段結束時，會儲存客戶的群組成員資格和細分資料的狀態。<br/>**`No`** — 在工作階段結束時，不會儲存客戶的群組成員資格和細分資料的狀態。 |

{style="table-layout:auto"}
