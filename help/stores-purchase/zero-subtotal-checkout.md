---
title: 零小計簽出
description: 瞭解如何設定零小計作為商店的離線付款方式。
exl-id: c14ce289-8292-41d9-a448-f493c784f35c
feature: Checkout, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# 零小計簽出

_零小計結帳_&#x200B;可用於在套用折扣後徵稅的零小計訂單。 例如，下列情況可能會使用零小計簽出：

- 折扣涵蓋整個購買價格，不需額外付運費。

- 客戶將[可下載](../catalog/product-create-downloadable.md)或[虛擬](../catalog/product-create-virtual.md)產品加入購物車，且價格等於零。

- [簡單](../catalog/product-create-simple.md)產品的價格為零，且可使用[免費送貨](shipping-free.md)方法。

- [優惠券代碼](../merchandising-promotions/price-rules-cart-coupon.md)涵蓋產品及運費的全價。

若要節省時間，可將零小計訂單設定為自動開立商業發票。

**_若要設定零小計簽出：_**

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Sales]**&#x200B;並選擇&#x200B;**[!UICONTROL Payment Methods]**。

1. 在&#x200B;_[!UICONTROL Other Payment Methods]_底下，展開&#x200B;**[!UICONTROL Zero Subtotal Checkout]**區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![零小計簽出](../configuration-reference/sales/assets/payment-methods-zero-subtotal-checkout.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >如有必要，請先清除&#x200B;**[!UICONTROL Use system value]**&#x200B;核取方塊以變更這些設定。

1. 若要啟用零小計簽出，請將&#x200B;**[!UICONTROL Enabled]**&#x200B;設為`Yes`。

1. 針對&#x200B;**[!UICONTROL Title]**，輸入在結帳期間識別Zero Subtotal方法的標題。

1. 如果訂單通常等待核准，請接受預設的&#x200B;**[!UICONTROL New Order Status]**&#x200B;作為`Pending"`，直到訂單核准為止。

   如果您偏好的話，可以使用此付款方式的新訂單使用`Processing`或`Suspected Fraud`狀態。

1. 如果要自動為餘額為零的所有專案開立發票，請將&#x200B;**[!UICONTROL Automatically Invoice All Items]**&#x200B;設為`Yes`。

   此選項僅在&#x200B;**[!UICONTROL New Order Status]**&#x200B;選項設定為`Processing`時可用。

   >[!NOTE]
   >
   >如果&#x200B;_[!UICONTROL New Order Status]_設定為`Processing`且_[!UICONTROL Automatically Invoice All Items]_&#x200B;設定為`No`，您也必須為[訂單狀態](order-status.md#custom-order-status)頁面上的&#x200B;**[!UICONTROL Order State]** = `Pending`且&#x200B;**[!UICONTROL Default Status]** = `No`對應指派&#x200B;**[!UICONTROL Order Status]** = `Processing`。

1. 將&#x200B;**[!UICONTROL Payment from Applicable Countries]**&#x200B;設定為下列其中一項：

   - `All Allowed Countries` — 來自您商店組態中指定的所有[國家/地區](../getting-started/store-details.md#country-options)的客戶都可以使用此付款方式。
   - `Specific Countries` — 選取此選項後，_[!UICONTROL Payment from Specific Countries]_清單就會顯示。 若要選取多個國家/地區，請按住Ctrl鍵(PC)或Command鍵(Mac)，然後按一下每個選項。

1. 針對&#x200B;**[!UICONTROL Sort Order]**，輸入數字，以決定此專案在結帳時顯示的付款方式清單中的位置。

   此數字與其他付款方式相關。 （`0` =第一個，`1` =第二個，`2` =第三個，依此類推。）

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。
