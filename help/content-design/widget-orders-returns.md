---
title: 訂單與退貨Widget
description: 瞭解如何使用訂單與退貨Widget，讓客戶能夠檢查其訂單狀態、列印商業發票及追蹤出貨。
exl-id: 1c3948e6-a0de-4ee4-8abf-10ab845a94a7
feature: Page Content, Orders, Returns
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 0%

---

# 訂單與退貨Widget

此 _訂購與退貨_ Widget可讓來賓檢查訂單狀態、列印發票及追蹤出貨。 將Widget新增至店面時，唯有未登入其帳戶的來賓和客戶才能看到它。 來賓可以透過提供訂單ID、帳單姓氏以及電子郵件地址或郵遞區號來尋找訂單。

![店面側邊欄中的訂單與退貨Widget](./assets/storefront-widget-orders-returns-sidebar.png){width="600" zoomable="yes"}

## 店面上的訂單與退貨Widget

1. 客戶可以使用 **[!UICONTROL Find Order By]** 選項以選擇下列其中一個引數來尋找訂單：

   - 電子郵件地址
   - 郵遞區號

1. 客戶輸入 **[!UICONTROL Order ID]** 和 **[!UICONTROL Billing Last Name]**.

1. 輸入任一帳單 **[!UICONTROL Email Address]** 或 **[!UICONTROL ZIP Code]** 與訂單相關聯的訂單編號。

1. 點按次數 **[!UICONTROL Search]** 以擷取訂單。

   ![店面中顯示的訂單資訊](./assets/storefront-widget-orders-returns-view.png){width="700" zoomable="yes"}

## 設定訂單與退貨Widget

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. 在右上角，按一下 **[!UICONTROL Add Widget]**.

1. 在 _[!UICONTROL Settings]_區段，請執行下列動作：

   - 設定 **[!UICONTROL Type]** 至 `Orders and Returns`.

   - 選擇 **[!UICONTROL Design Theme]** 由商店使用。

1. 按一下 **[!UICONTROL Continue]**.

1. 在 _[!UICONTROL Storefront Properties]_區段，請執行下列動作：

   - 的 **[!UICONTROL Widget Title]**，輸入Widget的描述性標題。

     此標題只會從管理員看到。

   - 的 **[!UICONTROL Assign to Store Views]**，選取顯示Widget的商店檢視。

     您可以選取特定的商店檢視，或 `All Store Views`. 若要選取多個檢視，請按住Ctrl鍵(PC)或Command鍵(Mac)並按一下每個選項。

   - （選用） For **[!UICONTROL Sort Order]**，請輸入數字以決定此專案在頁面相同部分與其他專案一起出現的順序。 (`0` =第一個， `1` =秒， `3` =第三個，依此類推。)

1. 在 _[!UICONTROL Layout Updates]_區段，按一下&#x200B;**[!UICONTROL Add Layout Update]**並執行下列動作：

   - 設定 **[!UICONTROL Display On]** 至您要顯示Widget的頁面型別。

   - 若要確定Widget在頁面上顯示的位置，請完成其餘的版面更新資訊。

1. 完成後，按一下 **[!UICONTROL Save]**.

1. 當提示重新整理快取時，請按一下頁面頂端訊息中的連結，然後依照指示進行。
