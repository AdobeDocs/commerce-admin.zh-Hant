---
title: 支票與匯票
description: 瞭解如何將支票和匯票設定為商店的離線付款方式。
exl-id: e004f0c3-f659-4b08-a41a-88bfc05acaab
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# 支票與匯票

Adobe Commerce和Magento Open Source可讓您接受支票或匯票付款。 此 _支票/匯票_ 預設為商店啟用付款方法。 您只能接受來自特定國家的支票和匯票，而且您可以微調具有最小和最大訂單總限制的設定。

**_若要以支票或匯票來設定付款，請執行下列步驟：_**

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Sales]** 並選擇 **[!UICONTROL Payment Methods]**.

1. 在 _[!UICONTROL Other Payment Methods]_，展開 ![展開選擇器](../assets/icon-display-expand.png) 此&#x200B;**[!UICONTROL Check / Money Order]**區段。

   ![支票/匯票](../configuration-reference/sales/assets/payment-methods-check-money-order.png){width="600" zoomable="yes"}

   如需這些組態設定的詳細說明，請參閱 [支票/匯票](../configuration-reference/sales/payment-methods.md#check--money-order) 在 _設定參考指南_.

   >[!NOTE]
   >
   >如有必要，請先清除 **[!UICONTROL Use system value]** 核取方塊以變更這些設定。

1. 若要接受支票或匯票付款，請設定 **[!UICONTROL Enabled]** 至 `Yes`.

1. 的 **[!UICONTROL Title]**，輸入在結帳時識別支票/匯票付款方式的標題。

1. 如果訂單通常會等待核准，請接受預設值 **[!UICONTROL New Order Status]** 作為 `Pending"` 直到獲得核准為止。

   您也可以使用 `Processing` 或 `Suspected Fraud` 使用此付款方式的新訂單狀態。

1. 設定 **[!UICONTROL Payment from Applicable Countries]** 變更為下列其中一項：

   - `All Allowed Countries`  — 來自所有客戶的客戶 [國家/地區](../getting-started/store-details.md#country-options) 在商店設定中指定的可使用此付款方式。
   - `Specific Countries`  — 選擇此選項後， _[!UICONTROL Payment from Specific Countries]_清單隨即顯示。 若要選取多個國家/地區，請按住Ctrl鍵(PC)或Command鍵(Mac)，然後按一下每個選項。

1. 的 **[!UICONTROL Make Check Payable To]**，輸入支票必須支付對象的名稱。

1. 的 **[!UICONTROL Send Check To]**，輸入郵寄支票的街道地址或郵政信箱。

1. 設定 **[!UICONTROL Minimum Order Total]** 和 **[!UICONTROL Maximum Order Total]** 至符合此付款方式資格的訂單金額。

   >[!NOTE]
   >
   >如果總計介於最小或最大總計值之間，或完全符合，訂單即符合條件。

1. 的 **[!UICONTROL Sort Order]**，請輸入數字，以決定此專案在結帳時顯示的付款方式清單中的位置。

   此數字與其他付款方式相關。 (`0` =第一個， `1` =秒， `2` =第三個，依此類推。)

1. 完成後，按一下 **[!UICONTROL Save Config]**.
