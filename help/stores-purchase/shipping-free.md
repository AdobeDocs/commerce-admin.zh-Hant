---
title: 免運費
description: 瞭解如何為商店設定免費送貨選項。
exl-id: 3ce69583-0f7f-4c23-b3e3-7d2502bc1bca
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# 免運費

_免運費_ 是您可以提供的最有效促銷活動之一。 可以最低購買量為基礎，或設定為 [購物車價格規則](../merchandising-promotions/price-rules-cart.md) 會在符合一組條件時套用的規則。 如果兩者套用至相同的順序，組態設定會優先於購物車規則。

>[!NOTE]
>
>檢查您的運送公司組態，瞭解免費運送所需的任何額外設定。

## 步驟1：設定免運費

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Sales]** 並選擇 **[!UICONTROL Delivery Methods]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Free Shipping]** 區段。

   >[!NOTE]
   >
   >如有必要，請先取消選取 **[!UICONTROL Use system value]** 核取方塊來變更下列設定，如所述。

1. 設定 **[!UICONTROL Enabled]** 至 `Yes`.

1. 的 **[!UICONTROL Title]**，輸入結帳時可識別「免運費」方法的標題，以及 **[!UICONTROL Method Name]** 加以說明。

1. 的 **[!UICONTROL Minimum Order Amount]**，輸入符合免運費條件的最小總計值。

   >[!TIP]
   >
   >若要搭配免費送貨使用 [表格費率](shipping-table-rate.md)，變成 _[!UICONTROL Minimum Order Amount]_太高，以至於永遠不滿足。 使用此高值可防止免運費生效，除非由價格規則觸發。

1. 設定 **[!UICONTROL Include Tax to Amount]**：

   - `Yes`  — 計算最小訂單金額時包含稅捐（小計+稅捐 — 折扣）。
   - `No`  — 計算「最小訂單金額」（小計 — 折扣）時不含稅。

   ![免運費](../configuration-reference/sales/assets/delivery-methods-free-shipping.png){width="600" zoomable="yes"}

1. 的 **[!UICONTROL Displayed Error Message]**，輸入在無法使用免費送貨時顯示的訊息。

1. 設定 **[!UICONTROL Ship to Applicable Countries]**：

   - `All Allowed Countries`  — 來自所有客戶的客戶 [國家/地區](../getting-started/store-details.md#country-options) 在商店設定中指定的商品可以使用免運費。

   - `Specific Countries`  — 選取此值後， _[!UICONTROL Ship to Specific Countries]_清單隨即顯示。 選取清單中可使用免費送貨的每個國家/地區。

1. 設定 **[!UICONTROL Show Method if Not Applicable]**：

   - `Yes`  — 一律顯示「免運費」方法，即使不適用亦然。
   - `No`  — 僅在適用時顯示「免運費」方法。

1. 的 **[!UICONTROL Sort Order]**，請輸入數字，以決定結帳時免費送貨在交貨方式清單中的位置。

   `0` =第一個， `1` =秒， `2` =第三個，依此類推。

1. 按一下 **[!UICONTROL Save Config]**.

## 步驟2：在承運商設定中啟用免運費

請務必完成您計畫用於免費送貨的每個承運商所需的任何設定。 例如，如果您的 [UPS設定](ups.md) 若未完成，請更新下列設定以啟用及設定免運費。

1. 在 _[!UICONTROL Delivery Methods]_設定，展開 ![展開選擇器](../assets/icon-display-expand.png) 此&#x200B;**[!UICONTROL UPS]**區段。

1. 設定 **[!UICONTROL Free Method]** 至 `UPS Ground` 或您要指定免費送貨的其他型別。

1. 若要要求免費送貨的最低訂單，請設定 **[!UICONTROL Enable Free Shipping Threshold]** 至 `Enable`.

   如果您選擇使用最小訂單，請輸入 **[!UICONTROL Free Shipping Amount Threshold]**.

1. 按一下 **[!UICONTROL Save Config]**.
