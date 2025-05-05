---
title: 免運費
description: 瞭解如何為商店設定免費送貨選項。
exl-id: 3ce69583-0f7f-4c23-b3e3-7d2502bc1bca
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---

# 免運費

_免運費_&#x200B;是您可以提供的最有效促銷活動之一。 可依據最低購買量或設定為當符合一組條件時所套用的[購物車價格規則](../merchandising-promotions/price-rules-cart.md)。 如果兩者套用至相同的順序，組態設定會優先於購物車規則。

>[!NOTE]
>
>檢查您的運送公司組態，瞭解免費運送所需的任何額外設定。

## 步驟1：設定免運費

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Sales]**&#x200B;並選擇&#x200B;**[!UICONTROL Delivery Methods]**。

1. 展開&#x200B;**[!UICONTROL Free Shipping]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   >[!NOTE]
   >
   >如有必要，請先取消選取&#x200B;**[!UICONTROL Use system value]**&#x200B;核取方塊以變更下列設定，如所述。

1. 將&#x200B;**[!UICONTROL Enabled]**&#x200B;設為`Yes`。

1. 針對&#x200B;**[!UICONTROL Title]**，輸入在結帳時識別免費送貨方法的標題，以及描述它的&#x200B;**[!UICONTROL Method Name]**。

1. 針對&#x200B;**[!UICONTROL Minimum Order Amount]**，請輸入符合免費送貨資格的最小總計值。

   >[!TIP]
   >
   >若要搭配[表格費率](shipping-table-rate.md)使用免運費，請將&#x200B;_[!UICONTROL Minimum Order Amount]_&#x200B;設得過高，使其永遠都不符合。 使用此高值可防止免運費生效，除非由價格規則觸發。

1. 設定&#x200B;**[!UICONTROL Include Tax to Amount]**：

   - `Yes` — 計算最小訂單金額時包含稅捐（小計+稅捐 — 折扣）。
   - `No` — 計算最小訂單金額時不含稅（小計 — 折扣）。

   ![免運費](../configuration-reference/sales/assets/delivery-methods-free-shipping.png){width="600" zoomable="yes"}

1. 針對&#x200B;**[!UICONTROL Displayed Error Message]**，輸入在無法使用免費送貨時顯示的訊息。

1. 設定&#x200B;**[!UICONTROL Ship to Applicable Countries]**：

   - `All Allowed Countries` — 來自您商店組態中指定的所有[國家/地區](../getting-started/store-details.md#country-options)的客戶都可以使用免運費。

   - `Specific Countries` — 選擇這個值之後，_[!UICONTROL Ship to Specific Countries]_&#x200B;清單就會顯示。 選取清單中可使用免費送貨的每個國家/地區。

1. 設定&#x200B;**[!UICONTROL Show Method if Not Applicable]**：

   - `Yes` — 一律顯示免費送貨方法，即使不適用也一樣。
   - `No` — 僅在適用時顯示免費送貨方法。

1. 針對&#x200B;**[!UICONTROL Sort Order]**，輸入數字，以決定結帳期間交貨方式清單中免費送貨的位置。

   `0` =第一，`1` =第二，`2` =第三，依此類推。

1. 按一下&#x200B;**[!UICONTROL Save Config]**。

## 步驟2：在承運商設定中啟用免運費

請務必完成您計畫用於免費送貨的每個承運商所需的任何設定。 例如，如果您的[UPS組態](ups.md)已經完成，請更新下列設定以啟用並設定免費送貨。

1. 在&#x200B;_[!UICONTROL Delivery Methods]_&#x200B;設定中，展開&#x200B;**[!UICONTROL UPS]**&#x200B;區段中的![擴充選擇器](../assets/icon-display-expand.png)。

1. 將&#x200B;**[!UICONTROL Free Method]**&#x200B;設定為`UPS Ground`或您要指定免費送貨的其他型別。

1. 若要要求最少免運費訂單，請將&#x200B;**[!UICONTROL Enable Free Shipping Threshold]**&#x200B;設為`Enable`。

   如果您選擇使用最小訂單，請輸入&#x200B;**[!UICONTROL Free Shipping Amount Threshold]**&#x200B;的所需金額。

1. 按一下&#x200B;**[!UICONTROL Save Config]**。
