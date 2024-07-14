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

_統一費率_&#x200B;是固定、預先定義的費用，可依每個專案或每次出貨套用。 統一費率是簡單的送貨解決方案，尤其是與某些電信業者提供的統一費率包裝搭配使用時。 啟用時，在結帳期間會顯示&#x200B;_平均匯率_&#x200B;作為選項。 因為未指定特定電信業者，所以您可以使用您選擇的電信業者。

## 設定固定運費

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Sales]**&#x200B;並選擇&#x200B;**[!UICONTROL Delivery Methods]**。

1. 展開![展開選擇器](../assets/icon-display-expand.png) **平均速率**&#x200B;區段。

   ![平準速率](../configuration-reference/sales/assets/delivery-methods-flat-rate.png){width="600" zoomable="yes"}

   如需這些組態設定的詳細說明，請參閱&#x200B;_組態參考指南_&#x200B;中的[統一速率](../configuration-reference/sales/delivery-methods.md#flat-rate)。

1. 將&#x200B;**[!UICONTROL Enabled]**&#x200B;設為`Yes`。

   統一稅率會在購物車的「預估出貨與稅捐」區段中，以及在結帳期間的「出貨」區段中顯示為選項。

1. 輸入平均匯率方法的描述性&#x200B;**[!UICONTROL Title]**。

1. 輸入&#x200B;**方法名稱**，顯示在購物車的計算費率旁邊。

   預設方法名稱為`Fixed`。 若您收取處理費，您可以將此文字變更為`Plus Handling`或其他適當的文字。

1. 若要說明如何使用固定運費，請將&#x200B;**Type**&#x200B;設定為下列其中一項：

   - `None` — 停用付款型別。 「統一運費」選項會列在購物車中，但運費為零，與免運費相同。
   - `Per Order` — 對整個訂單收取單一固定費用。
   - `Per Item` — 對每個專案收取單一固定費用。 無論是否有相同或不同料號的多重數量，此比率都會乘以購物車中的料號數量。

1. 輸入您要以統一費率運送的&#x200B;**價格**。

1. 根據您的要求設定手續費選項。

   處理費是選擇性的，且顯示為額外費用，會加到運費中。 如果要包含手續費，請執行下列步驟：

   - 針對&#x200B;**計算手續費**，請選取您要用來計算手續費的方法：

      - `Fixed`
      - `Percent`

   - 針對&#x200B;**手續費**，根據您選擇用來計算金額的方法，輸入要收取的金額。

     例如，如果費用是以固定費用為基礎，則以小數點輸入金額，例如`4.90`。 不過，如果處理費是以出貨成本的百分比為基準，請以百分比輸入金額。 例如，如果您收取運費的6%，請輸入值為`6`。

1. 如有需要，請變更&#x200B;**顯示的錯誤訊息**。

   此文字方塊已預設預設預設預設訊息，但您可以輸入其他訊息，以在「統一運費」無法使用時顯示。

1. 設定&#x200B;**送貨至適用的國家**：

   - `All Allowed Countries` — 來自您商店組態中指定的所有[國家/地區](../getting-started/store-details.md#country-options)的客戶都可以使用這個傳遞方法。
   - `Specific Countries` — 選擇此選項時，會顯示&#x200B;_送貨至特定國家_&#x200B;清單。 選取清單中可使用此傳遞方法的每個國家/地區。

1. 設定&#x200B;**Show方法（若不適用）**：

   - `Yes` — 一律顯示Flat Rate方法，即使不適用。
   - `No` — 只在適用時才顯示平均匯率方法。

1. 針對&#x200B;**[!UICONTROL Sort Order]**，請輸入數字，以決定結帳期間與其他傳遞方式一起列出時，統一運費送貨的順序。

   `0` =第一，`1` =第二，`2` =第三，依此類推。

1. 按一下&#x200B;**[!UICONTROL Save Config]**。
