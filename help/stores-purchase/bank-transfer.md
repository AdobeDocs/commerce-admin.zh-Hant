---
title: 銀行轉帳
description: 瞭解如何將銀行轉帳設定為商店的離線付款方式。
exl-id: 34b2163c-2edd-4741-b002-3d8fb561fc78
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---

# 銀行轉帳

Adobe Commerce和Magento Open Source可讓您接受從客戶銀行帳戶轉入，並存入您的商家銀行帳戶的付款。

**_若要設定銀行轉帳付款：_**

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Sales]**&#x200B;並選擇&#x200B;**[!UICONTROL Payment Methods]**。

1. 在&#x200B;_其他付款方式_&#x200B;下，展開![擴充選取器](../assets/icon-display-expand.png) **[!UICONTROL Bank Transfer Payment]**&#x200B;區段。

   ![銀行轉帳付款](../configuration-reference/sales/assets/payment-methods-bank-transfer-payment.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >如有必要，請先清除&#x200B;**[!UICONTROL Use system value]**&#x200B;核取方塊以變更這些設定。

1. 若要啟用銀行轉帳，請將&#x200B;**[!UICONTROL Enabled]**&#x200B;設為`Yes`。

1. 針對&#x200B;**[!UICONTROL Title]**，輸入在結帳時識別銀行轉帳付款方式的標題。

1. 將&#x200B;**[!UICONTROL New Order Status]**&#x200B;設定為`Pending`，直到付款獲得授權為止。

1. 將&#x200B;**[!UICONTROL Payment from Applicable Countries]**&#x200B;設定為下列其中一項：

   - `All Allowed Countries` — 來自您商店組態中指定的所有[國家/地區](../getting-started/store-details.md#country-options)的客戶都可以使用此付款方式。

   - `Specific Countries` — 選取此選項後，_[!UICONTROL Payment from Specific Countries]_&#x200B;清單就會顯示。 若要選取多個國家/地區，請按住Ctrl鍵(PC)或Command鍵(Mac)，然後按一下每個選項。

1. 輸入您的客戶必須遵循的&#x200B;**[!UICONTROL Instructions]**&#x200B;以設定銀行轉帳。

   根據銀行所在的國家/地區及銀行需求，您可納入下列資訊：

   - 銀行帳戶名稱
   - 銀行帳號
   - 銀行路由代碼
   - 銀行名稱
   - 銀行地址

1. 將&#x200B;**[!UICONTROL Minimum Order Total]**&#x200B;與&#x200B;**[!UICONTROL Maximum Order Total]**&#x200B;設為符合使用此付款方式資格的所需金額。

   >[!NOTE]
   >
   >如果總計介於最小或最大總計值之間，或完全符合，訂單即符合條件。

1. 針對&#x200B;**[!UICONTROL Sort Order]**，輸入數字，以決定此專案在結帳時顯示的付款方式清單中的位置。

   此數字與其他付款方式相關。 （`0` =第一個，`1` =第二個，`2` =第三個，依此類推。）

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。
