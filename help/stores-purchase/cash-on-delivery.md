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

Adobe Commerce和Magento Open Source可讓您接受購買的&#x200B;_貨到付款_ (COD)。 您只能接受特定國家/地區的貨到付款要求，而且您可以微調具有最小和最大訂單總限額的設定。

出貨承運商在交貨時收到客戶的付款，然後將其轉給您。 您可以調整承運商服務收取的任何運費和手續費。

**_若要設定貨到付款付款：_**

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Sales]**&#x200B;並選擇&#x200B;**[!UICONTROL Payment Methods]**。

1. 在&#x200B;_其他付款方式_&#x200B;下，展開![擴充選取器](../assets/icon-display-expand.png) **[!UICONTROL Cash On Delivery Payment]**&#x200B;區段。

   ![貨到付款](../configuration-reference/sales/assets/payment-methods-cash-on-delivery-payment.png){width="600" zoomable="yes"}

   如需這些組態設定的詳細說明，請參閱&#x200B;_組態參考指南_&#x200B;中的[貨到付款付款](../configuration-reference/sales/payment-methods.md#cash-on-delivery-payment)。

   >[!NOTE]
   >
   >如有必要，請先清除&#x200B;**[!UICONTROL Use system value]**&#x200B;核取方塊以變更這些設定。

1. 若要啟用貨到付款付款，請將&#x200B;**[!UICONTROL Enabled]**&#x200B;設為`Yes`。

1. 針對&#x200B;**[!UICONTROL Title]**，輸入在結帳時識別COD付款方式的標題。

1. 設定&#x200B;**[!UICONTROL New Order Status]**&#x200B;為`Pending`，直到確認收到付款為止。

   如果您偏好的話，可以使用此付款方式的新訂單使用`Processing`或`Suspected Fraud`狀態。

1. 將&#x200B;**[!UICONTROL Payment from Applicable Countries]**&#x200B;設定為下列其中一項：

   - `All Allowed Countries` — 來自您商店組態中指定的所有[國家/地區](../getting-started/store-details.md#country-options)的客戶都可以使用此付款方式。
   - `Specific Countries` — 選取此選項後，_[!UICONTROL Payment from Specific Countries]_&#x200B;清單就會顯示。 若要選取多個國家/地區，請按住Ctrl鍵(PC)或Command鍵(Mac)，然後按一下每個選項。

1. 輸入&#x200B;**[!UICONTROL Instructions]**&#x200B;以接受貨到付款訂單的傳遞。

1. 將&#x200B;**[!UICONTROL Minimum Order Total]**&#x200B;與&#x200B;**[!UICONTROL Maximum Order Total]**&#x200B;設為符合貨到付款資格的訂單金額。

   >[!NOTE]
   >
   >訂單符合總計在最小或最大訂單總計之間，或是符合訂單總計的最大值。

1. 針對&#x200B;**[!UICONTROL Sort Order]**，輸入數字，以決定此專案在結帳時顯示的付款方式清單中的位置。

   此數字與其他付款方式相關。 （`0` =第一個，`1` =第二個，`2` =第三個，依此類推。）

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。
