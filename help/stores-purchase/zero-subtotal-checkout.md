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

_零小計簽出_ 可用於小計為零且套用折扣後徵稅的訂單。 例如，下列情況可能會使用零小計簽出：

- 折扣涵蓋整個購買價格，不需額外付運費。

- 客戶新增 [可下載](../catalog/product-create-downloadable.md) 或 [虛擬](../catalog/product-create-virtual.md) 產品到購物車，價格等於零。

- 的價格 [簡單](../catalog/product-create-simple.md) product為0，而 [免費送貨](shipping-free.md) 方法可供使用。

- A [抵用券代碼](../merchandising-promotions/price-rules-cart-coupon.md) 涵蓋產品及運費的全價。

若要節省時間，可將零小計訂單設定為自動開立商業發票。

**_若要設定零小計簽出：_**

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Sales]** 並選擇 **[!UICONTROL Payment Methods]**.

1. 在 _[!UICONTROL Other Payment Methods]_，展開 ![展開選擇器](../assets/icon-display-expand.png) 此&#x200B;**[!UICONTROL Zero Subtotal Checkout]**區段。

   ![零小計簽出](../configuration-reference/sales/assets/payment-methods-zero-subtotal-checkout.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >如有必要，請先清除 **[!UICONTROL Use system value]** 核取方塊以變更這些設定。

1. 若要啟用零小計簽出，請設定 **[!UICONTROL Enabled]** 至 `Yes`.

1. 的 **[!UICONTROL Title]**，輸入在結帳期間識別Zero Subtotal方法的標題。

1. 如果訂單通常會等待核准，請接受預設值 **[!UICONTROL New Order Status]** 作為 `Pending"` 直到訂單核准為止。

   您也可以使用 `Processing` 或 `Suspected Fraud` 使用此付款方式的新訂單狀態。

1. 設定 **[!UICONTROL Automatically Invoice All Items]** 至 `Yes` 如果您要自動為餘額為零的所有料號開立商業發票。

   此選項僅在 **[!UICONTROL New Order Status]** 選項已設為 `Processing`.

   >[!NOTE]
   >
   >如果 _[!UICONTROL New Order Status]_設為 `Processing` 和_[!UICONTROL Automatically Invoice All Items]_ 設為 `No`，您也必須指派 **[!UICONTROL Order Status]** = `Processing` 針對 **[!UICONTROL Order State]** = `Pending` 和 **[!UICONTROL Default Status]** = `No` 對應 [訂單狀態](order-status.md#custom-order-status) 頁面。

1. 設定 **[!UICONTROL Payment from Applicable Countries]** 變更為下列其中一項：

   - `All Allowed Countries`  — 來自所有客戶的客戶 [國家/地區](../getting-started/store-details.md#country-options) 在商店設定中指定的可使用此付款方式。
   - `Specific Countries`  — 選擇此選項後， _[!UICONTROL Payment from Specific Countries]_清單隨即顯示。 若要選取多個國家/地區，請按住Ctrl鍵(PC)或Command鍵(Mac)，然後按一下每個選項。

1. 的 **[!UICONTROL Sort Order]**，請輸入數字，以決定此專案在結帳時顯示的付款方式清單中的位置。

   此數字與其他付款方式相關。 (`0` =第一個， `1` =秒， `2` =第三個，依此類推。)

1. 完成後，按一下 **[!UICONTROL Save Config]**.
