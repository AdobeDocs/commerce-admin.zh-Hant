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

Adobe Commerce和Magento Open Source可讓您接受支票或匯票付款。 根據預設，已為您的商店啟用&#x200B;_支票/匯票_&#x200B;付款方式。 您只能接受來自特定國家的支票和匯票，而且您可以微調具有最小和最大訂單總限制的設定。

**_若要以支票或匯票設定付款：_**

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Sales]**&#x200B;並選擇&#x200B;**[!UICONTROL Payment Methods]**。

1. 在&#x200B;_[!UICONTROL Other Payment Methods]_底下，展開&#x200B;**[!UICONTROL Check / Money Order]**區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![支票/匯票](../configuration-reference/sales/assets/payment-methods-check-money-order.png){width="600" zoomable="yes"}

   如需這些組態設定的詳細說明，請參閱&#x200B;_組態參考指南_&#x200B;中的[支票/匯票](../configuration-reference/sales/payment-methods.md#check--money-order)。

   >[!NOTE]
   >
   >如有必要，請先清除&#x200B;**[!UICONTROL Use system value]**&#x200B;核取方塊以變更這些設定。

1. 若要接受支票或匯票付款，請將&#x200B;**[!UICONTROL Enabled]**&#x200B;設為`Yes`。

1. 針對&#x200B;**[!UICONTROL Title]**，輸入在結帳時識別支票/匯票付款方式的標題。

1. 如果訂單通常等待核准，請接受預設的&#x200B;**[!UICONTROL New Order Status]**&#x200B;作為`Pending"`，直到它獲得核准為止。

   如果您偏好的話，可以使用此付款方式的新訂單使用`Processing`或`Suspected Fraud`狀態。

1. 將&#x200B;**[!UICONTROL Payment from Applicable Countries]**&#x200B;設定為下列其中一項：

   - `All Allowed Countries` — 來自您商店組態中指定的所有[國家/地區](../getting-started/store-details.md#country-options)的客戶都可以使用此付款方式。
   - `Specific Countries` — 選取此選項後，_[!UICONTROL Payment from Specific Countries]_清單就會顯示。 若要選取多個國家/地區，請按住Ctrl鍵(PC)或Command鍵(Mac)，然後按一下每個選項。

1. 針對&#x200B;**[!UICONTROL Make Check Payable To]**，輸入支票必須支付給哪一方的名稱。

1. 針對&#x200B;**[!UICONTROL Send Check To]**，輸入郵寄支票的街道地址或郵政信箱。

1. 將&#x200B;**[!UICONTROL Minimum Order Total]**&#x200B;與&#x200B;**[!UICONTROL Maximum Order Total]**&#x200B;設為符合此付款方式資格的訂單金額。

   >[!NOTE]
   >
   >如果總計介於最小或最大總計值之間，或完全符合，訂單即符合條件。

1. 針對&#x200B;**[!UICONTROL Sort Order]**，輸入數字，以決定此專案在結帳時顯示的付款方式清單中的位置。

   此數字與其他付款方式相關。 （`0` =第一個，`1` =第二個，`2` =第三個，依此類推。）

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。
