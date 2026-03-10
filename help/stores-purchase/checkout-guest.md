---
title: 訪客簽出
description: 瞭解如何在您的商店啟用訪客結帳功能。
exl-id: ce25eba3-7503-46aa-a5cd-9b7d5662164b
feature: Checkout
source-git-commit: 347321ec5b0722f06240780136cb29816aab559f
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# 訪客簽出

您的商店可設定為要求購物者在購買前先開立帳戶。 預設設定可讓訪客進行購買，並可選擇在完成結帳程式後註冊帳戶。

![Luma存放區顯示簽出為來賓](./assets/storefront-checkout-as-guest.png){width="600" zoomable="yes"}

**_停用來賓簽出:_**

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板上，展開&#x200B;**[!UICONTROL Sales]**&#x200B;並選擇&#x200B;**[!UICONTROL Checkout]**。

1. 展開![區段的](../assets/icon-display-expand.png)擴充選擇器&#x200B;**[!UICONTROL Checkout Options]**。

   ![在設定頁面上展開的簽出選項](./assets/checkout-checkout-options.png){width="700" zoomable="yes"}

如需這些組態設定的詳細說明，請參閱[組態參考指南](../configuration-reference/sales/checkout.md#checkout-options)中的&#x200B;_簽出選項_。

1. 如果設定是針對特定存放區檢視，[請選擇組態套用的存放區檢視](../configuration-reference/scope-change.md#set-the-scope)。

   出現提示時，按一下&#x200B;**[!UICONTROL OK]**&#x200B;以繼續。

1. 將&#x200B;**[!UICONTROL Allow Guest Checkout]**&#x200B;設為`No`。

   如有必要，請清除&#x200B;**[!UICONTROL Use system value]**&#x200B;核取方塊以啟用此設定的變更。

1. 按一下&#x200B;**[!UICONTROL Save Config]**。

## 允許已註冊電子郵件的訪客訂單存取權

僅[!BADGE SaaS]{type=Positive url="https://experienceleague.adobe.com/zh-hant/docs/commerce/user-guides/product-solutions" tooltip="僅適用於Adobe Commerce as a Cloud Service專案(Adobe管理的SaaS基礎結構)。"}

選用的商店層級設定預設為停用，可讓訪客購物者追蹤使用符合註冊客戶帳戶的電子郵件地址所下的訂單。

啟用後，仍可存取透過已註冊電子郵件下單的訪客結帳訂單，同時也會出現在客戶的訂單歷史記錄中。

若要啟用此功能，請瀏覽至&#x200B;**商店** >設定> **組態** >銷售> **銷售** > **訪客簽出**，並將&#x200B;**允許註冊電子郵件的訪客訂單存取**&#x200B;設定設為`Yes`。
