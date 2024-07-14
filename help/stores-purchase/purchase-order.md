---
title: 採購單
description: 瞭解如何將訂購單設定為商店的離線付款方式。
exl-id: 493c1b59-2155-449f-a08a-eb1aa2af9b3e
feature: Purchase Orders
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# 採購單

_採購單_ （採購單）可讓商業客戶參考採購單編號來支付授權採購的費用。 採購單已由進行採購的公司預先授權並簽發。 結帳時，客戶選擇「採購單」作為付款方式。 收到您的商業發票後，公司即會在應付帳款系統中處理付款，並支付採購費用。

接受採購單付款前，請一律建立商業客戶的信用等級。

**_若要依採購單設定付款：_**

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Sales]**&#x200B;並選擇&#x200B;**[!UICONTROL Payment Methods]**。

1. 在&#x200B;_[!UICONTROL Other Payment Methods]_底下，展開&#x200B;**[!UICONTROL Purchase Order]**區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![採購單](../configuration-reference/sales/assets/payment-methods-purchase-order.png){width="600" zoomable="yes"}

   如需這些組態設定的詳細說明，請參閱&#x200B;_組態參考指南_&#x200B;中的[採購單](../configuration-reference/sales/payment-methods.md#purchase-order)。

   >[!NOTE]
   >
   >如有必要，請先清除&#x200B;**[!UICONTROL Use system value]**&#x200B;核取方塊以變更這些設定。

1. 若要啟用此付款方法，請將&#x200B;**[!UICONTROL Enabled]**&#x200B;設為`Yes`。

1. 針對&#x200B;**[!UICONTROL Title]**，輸入在結帳時識別此付款方式的標題。

1. 將&#x200B;**[!UICONTROL New Order Status]**&#x200B;設定為`Pending`，直到付款獲得授權為止。

1. 將&#x200B;**[!UICONTROL Payment from Applicable Countries]**&#x200B;設定為下列其中一項：

   - `All Allowed Countries` — 來自您商店組態中指定的所有[國家/地區](../getting-started/store-details.md#country-options)的客戶都可以使用此付款方式。
   - `Specific Countries` — 選取此選項後，_[!UICONTROL Payment from Specific Countries]_清單就會顯示。 若要選取多個國家/地區，請按住Ctrl鍵(PC)或Command鍵(Mac)，然後按一下每個選項。

1. 將&#x200B;**[!UICONTROL Minimum Order Total]**&#x200B;與&#x200B;**[!UICONTROL Maximum Order Total]**&#x200B;設為符合此付款方式所需的金額。

   >[!NOTE]
   >
   >如果總計介於最小或最大總計值之間，或完全符合，訂單即符合條件。

1. 針對&#x200B;**[!UICONTROL Sort Order]**，輸入數字，以決定此專案在結帳時顯示的付款方式清單中的位置。

   此數字與其他付款方式相關。 （`0` =第一個，`1` =第二個，`2` =第三個，依此類推。）

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。
