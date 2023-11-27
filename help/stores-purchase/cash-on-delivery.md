---
title: 貨到付款(COD)
description: 瞭解如何將貨到付款設定為商店的離線付款方式。
exl-id: dcf94734-a66e-4d32-b389-b47c979ceaa9
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# 貨到付款(COD)

Adobe Commerce和Magento Open Source允許您接受 _貨到付款_ (COD)購買付款。 您只能接受特定國家/地區的貨到付款要求，而且您可以微調具有最小和最大訂單總限額的設定。

出貨承運商在交貨時收到客戶的付款，然後將其轉給您。 您可以調整承運商服務收取的任何運費和手續費。

**_若要設定貨到付款付款，請執行下列步驟：_**

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Sales]** 並選擇 **[!UICONTROL Payment Methods]**.

1. 在 _其他付款方法_，展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Cash On Delivery Payment]** 區段。

   ![貨到付款](../configuration-reference/sales/assets/payment-methods-cash-on-delivery-payment.png){width="600" zoomable="yes"}

   如需這些組態設定的詳細說明，請參閱 [貨到付款](../configuration-reference/sales/payment-methods.md#cash-on-delivery-payment) 在 _設定參考指南_.

   >[!NOTE]
   >
   >如有必要，請先清除 **[!UICONTROL Use system value]** 核取方塊以變更這些設定。

1. 若要啟用貨到付款付款，請設定 **[!UICONTROL Enabled]** 至 `Yes`.

1. 的 **[!UICONTROL Title]**，輸入在結帳時識別COD付款方式的標題。

1. 設定 **[!UICONTROL New Order Status]** 至 `Pending` 直到確認收到付款為止。

   您也可以使用 `Processing` 或 `Suspected Fraud` 使用此付款方式的新訂單狀態。

1. 設定 **[!UICONTROL Payment from Applicable Countries]** 變更為下列其中一項：

   - `All Allowed Countries`  — 來自所有客戶的客戶 [國家/地區](../getting-started/store-details.md#country-options) 在商店設定中指定的可使用此付款方式。
   - `Specific Countries`  — 選擇此選項後， _[!UICONTROL Payment from Specific Countries]_清單隨即顯示。 若要選取多個國家/地區，請按住Ctrl鍵(PC)或Command鍵(Mac)，然後按一下每個選項。

1. 輸入 **[!UICONTROL Instructions]** 接受貨到付款訂單的傳遞。

1. 設定 **[!UICONTROL Minimum Order Total]** 和 **[!UICONTROL Maximum Order Total]** 與符合貨到付款資格的訂單金額相符。

   >[!NOTE]
   >
   >訂單符合總計在最小或最大訂單總計之間，或是符合訂單總計的最大值。

1. 的 **[!UICONTROL Sort Order]**，請輸入數字，以決定此專案在結帳時顯示的付款方式清單中的位置。

   此數字與其他付款方式相關。 (`0` =第一個， `1` =秒， `2` =第三個，依此類推。)

1. 完成後，按一下 **[!UICONTROL Save Config]**.
