---
title: 固定運費
description: 瞭解如何為商店設定統一運費選項。
exl-id: a6874509-a79b-42ab-aa93-d70d18fc33f6
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 0%

---

# 固定運費

_平準率_ 是固定、預先定義的費用，可依料號或出貨套用。 統一費率是簡單的送貨解決方案，尤其是與某些電信業者提供的統一費率包裝搭配使用時。 啟用時， _平準率_ 在出庫時顯示為選項。 因為未指定特定電信業者，所以您可以使用您選擇的電信業者。

## 設定固定運費

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Sales]** 並選擇 **[!UICONTROL Delivery Methods]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **平準率** 區段。

   ![平準率](../configuration-reference/sales/assets/delivery-methods-flat-rate.png){width="600" zoomable="yes"}

   如需這些組態設定的詳細說明，請參閱 [平準率](../configuration-reference/sales/delivery-methods.md#flat-rate) 在 _設定參考指南_.

1. 設定 **[!UICONTROL Enabled]** 至 `Yes`.

   統一稅率會在購物車的「預估出貨與稅捐」區段中，以及在結帳期間的「出貨」區段中顯示為選項。

1. 輸入描述性 **[!UICONTROL Title]** 用於「均一速率」方法。

1. 輸入 **方法名稱** 顯示在購物車的計算費率旁邊。

   預設方法名稱為 `Fixed`. 若您收取手續費，您可將此文字變更為 `Plus Handling`，或其他適合的專案。

1. 若要說明如何使用統一運費，請設定 **型別** 變更為下列其中一項：

   - `None`  — 停用付款型別。 「統一運費」選項會列在購物車中，但運費為零，與免運費相同。
   - `Per Order`  — 對整個訂單收取單一統一費率。
   - `Per Item`  — 針對每個料號收取單一統一費率。 無論是否有相同或不同料號的多重數量，此比率都會乘以購物車中的料號數量。

1. 輸入 **價格** 您想要以統一費率運費收取的費用。

1. 根據您的要求設定手續費選項。

   處理費是選擇性的，且顯示為額外費用，會加到運費中。 如果要包含手續費，請執行下列步驟：

   - 的 **計算手續費**，選取您要用來計算手續費的方法：

      - `Fixed`
      - `Percent`

   - 的 **手續費**，根據您選擇用來計算金額的方法，輸入要收取的金額。

     例如，如果費用是以固定費用為基礎，則以小數點輸入金額，例如 `4.90`. 不過，如果處理費是以出貨成本的百分比為基準，請以百分比輸入金額。 例如，如果您收取運費的6%，則輸入值為 `6`.

1. 如有需要，請變更 **顯示的錯誤訊息**.

   此文字方塊已預設預設預設預設訊息，但您可以輸入其他訊息，以在「統一運費」無法使用時顯示。

1. 設定 **送貨至適用國家/地區**：

   - `All Allowed Countries`  — 來自所有客戶的客戶 [國家/地區](../getting-started/store-details.md#country-options) 在存放區設定中指定時，可以使用此傳送方法。
   - `Specific Countries`  — 選擇此選項時， _送貨至特定國家_ 清單隨即顯示。 選取清單中可使用此傳遞方法的每個國家/地區。

1. 設定 **顯示方法（若不適用）**：

   - `Yes`  — 一律顯示「平均匯率」方法，即使不適用。
   - `No`  — 僅在適用時顯示「平均匯率」方法。

1. 的 **[!UICONTROL Sort Order]**，請輸入數字，以決定結帳期間與其他交貨方式一起列出「統一運費」時，系統顯示的順序。

   `0` =第一個， `1` =秒， `2` =第三個，依此類推。

1. 按一下 **[!UICONTROL Save Config]**.
