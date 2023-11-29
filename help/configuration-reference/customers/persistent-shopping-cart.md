---
title: 『[!UICONTROL Customers] &gt； [!UICONTROL Persistent Shopping Cart]『
description: 檢閱上的組態設定 [!UICONTROL Customers] &gt； [!UICONTROL Persistent Shopping Cart] 商務管理員頁面。
exl-id: d6c5ae46-32ed-4fcd-bcd6-ee3a07d7db5f
feature: Configuration, Shopping Cart
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Persistent Shopping Cart]

{{config}}

>[!NOTE]
>
>A [永久購物車](../../stores-purchase/cart-persistent.md) 允許保留購物車中留下的未購買專案，並將其儲存一段設定於 _永續性存留期_. 客戶瀏覽器中應允許Cookie使用永續性購物車。

## [!UICONTROL General Options]

![一般選項](./assets/persistent-shopping-cart-general.png)<!-- zoom -->

<!-- [General Options](https://docs.magento.com/user-guide/sales/cart-persistent-configuration.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable Persistence] | 網站 | 決定是否啟用持續性。 |
| [!UICONTROL Persistence Lifetime (seconds)] | 網站 | 定義永久性Cookie的生命週期（以秒為單位）。 允許的最大值為3153600000秒（100年）。 |
| [!UICONTROL Enable "Remember Me"] | 網站 | 定義是否 _記住我_ 核取方塊會出現在商店的登入和註冊頁面上。 選項： <br/>**`Yes`**— 顯示 _記住我_ 核取方塊。<br/>**`No`**  — 不顯示 _記住我_ 核取方塊，而永久性Cookie僅用於已擁有該功能的客戶。 |
| [!UICONTROL "Remember Me" Default Value] | 網站 | 定義預設狀態 _記住我_ 核取方塊。 |
| [!UICONTROL Clear Persistence on Log Out] | 網站 | 定義當商店客戶登出時是否刪除永久性Cookie。 無論此設定為何，如果客戶未登出，但工作階段Cookie過期，仍會使用永久性Cookie。 |
| [!UICONTROL Persist Shopping Cart] | 網站 | 定義使用永久性Cookie是否會提供對往來帳戶之購物車資料的存取權。 選項： <br/>**`Yes`**— 在工作階段結束後儲存購物車內容。<br/>**`No`**  — 工作階段結束後未儲存購物車內容。 |
| [!UICONTROL Persist Wish List] | 網站 | ![Adobe Commerce](../../assets/adobe-logo.svg) (僅限Adobe Commerce)決定是否在工作階段結束時保留客戶願望清單的狀態。 選項： <br/>**`Yes`**— 工作階段結束時會儲存希望清單內容。<br/>**`No`**  — 工作階段結束時未儲存希望清單。 |
| [!UICONTROL Persist Recently Ordered Items] | 網站 | ![Adobe Commerce](../../assets/adobe-logo.svg) (僅限Adobe Commerce)決定是否在工作階段結束時保留最近排序專案的狀態。 選項： <br/>**`Yes`**— 作業階段結束時會儲存「最近訂購的專案」的狀態。<br/>**`No`**  — 作業階段結束時不會儲存最近訂購專案的狀態。 |
| [!UICONTROL Persist Currently Compared Products] | 網站 | ![Adobe Commerce](../../assets/adobe-logo.svg) (僅限Adobe Commerce)決定是否在工作階段結束時保留目前比較產品的狀態。 選項： <br/>**`Yes`**— 工作階段結束時，會儲存目前比較產品的狀態。<br/>**`No`**  — 工作階段結束時，目前比較產品的狀態不會儲存。 |
| [!UICONTROL Persist Comparison History] | 網站 | ![Adobe Commerce](../../assets/adobe-logo.svg) (僅限Adobe Commerce)決定作業階段結束時是否保留比較歷史記錄的狀態。 選項： <br/>**`Yes`**— 作業階段結束時會儲存比較歷程記錄的狀態。<br/>**`No`**  — 作業階段結束時不會儲存比較歷程記錄的狀態。 |
| [!UICONTROL Persist Recently Viewed Products] | 網站 | ![Adobe Commerce](../../assets/adobe-logo.svg) (僅限Adobe Commerce)決定是否會在工作階段結束時保留最近檢視產品的狀態。 選項： <br/>**`Yes`**— 工作階段結束時，會儲存最近檢視過的產品的狀態。<br/>**`No`**  — 工作階段結束時未儲存最近檢視過的產品的狀態。 |
| [!UICONTROL Persist Customer Group Membership and Segmentation] | 網站 | ![Adobe Commerce](../../assets/adobe-logo.svg) (僅限Adobe Commerce)決定在工作階段結束時，是否保留客戶群組成員資格和細分條件的狀態。 選項： <br/>**`Yes`**— 在工作階段結束時，會儲存客戶的群組成員資格和細分資料的狀態。<br/>**`No`**  — 工作階段結束時，不會儲存客戶的群組成員資格狀態和細分資料。 |

{style="table-layout:auto"}
