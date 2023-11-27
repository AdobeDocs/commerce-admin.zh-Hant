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

**_若要設定銀行轉帳付款，請執行下列步驟：_**

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Sales]** 並選擇 **[!UICONTROL Payment Methods]**.

1. 在 _其他付款方法_，展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Bank Transfer Payment]** 區段。

   ![銀行轉帳付款](../configuration-reference/sales/assets/payment-methods-bank-transfer-payment.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >如有必要，請先清除 **[!UICONTROL Use system value]** 核取方塊以變更這些設定。

1. 若要啟用銀行轉帳，請設定 **[!UICONTROL Enabled]** 至 `Yes`.

1. 的 **[!UICONTROL Title]**，輸入在結帳時識別銀行轉帳付款方式的標題。

1. 設定 **[!UICONTROL New Order Status]** 至 `Pending` 直到付款獲得授權為止。

1. 設定 **[!UICONTROL Payment from Applicable Countries]** 變更為下列其中一項：

   - `All Allowed Countries`  — 來自所有客戶的客戶 [國家/地區](../getting-started/store-details.md#country-options) 在商店設定中指定的可使用此付款方式。

   - `Specific Countries`  — 選擇此選項後， _[!UICONTROL Payment from Specific Countries]_清單隨即顯示。 若要選取多個國家/地區，請按住Ctrl鍵(PC)或Command鍵(Mac)，然後按一下每個選項。

1. 輸入 **[!UICONTROL Instructions]** 您的客戶必須依循這些步驟才能設定銀行轉帳。

   根據銀行所在的國家/地區及銀行需求，您可納入下列資訊：

   - 銀行帳戶名稱
   - 銀行帳號
   - 銀行路由代碼
   - 銀行名稱
   - 銀行地址

1. 設定 **[!UICONTROL Minimum Order Total]** 和 **[!UICONTROL Maximum Order Total]** 至符合使用此付款方式資格的所需金額。

   >[!NOTE]
   >
   >如果總計介於最小或最大總計值之間，或完全符合，訂單即符合條件。

1. 的 **[!UICONTROL Sort Order]**，請輸入數字，以決定此專案在結帳時顯示的付款方式清單中的位置。

   此數字與其他付款方式相關。 (`0` =第一個， `1` =秒， `2` =第三個，依此類推。)

1. 完成後，按一下 **[!UICONTROL Save Config]**.
