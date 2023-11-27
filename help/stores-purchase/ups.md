---
title: 聯合包裹服務(UPS)
description: 瞭解如何將UPS設定為您的商店的運送業者。
exl-id: a7965b2f-2473-4b63-a247-3b2230cde5d8
feature: Shipping/Delivery
source-git-commit: 50b44190a9568a8d6ad38ab29177904596569d75
workflow-type: tm+mt
source-wordcount: '827'
ht-degree: 0%

---

# 聯合包裹服務(UPS)

United Parcel Service (UPS)提供國內及國際的陸運及空運服務，服務對象超過220個國家。

{{ups-api}}

>[!NOTE]
>
>UPS可以使用 [維度權數](carriers.md#dimensional-weight) 以決定某些運費。 不過，Adobe Commerce僅支援重量型出貨成本計算。

## 步驟1：開啟UPS出貨帳戶

若要提供此送貨方式給您的客戶，您必須先使用UPS開立帳戶。

## 步驟2：為商店啟用UPS

{{beta2-updates}}

1. 在 _管理員側邊欄_，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側的面板中，在 **[!UICONTROL Sales]**，選擇 **[!UICONTROL Delivery Methods]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL UPS]** 區段。

1. 設定 **[!UICONTROL Enabled for Checkout]** 至 `Yes`.

1. 針對UPS XML帳戶（預設），設定 **[!UICONTROL UPS Type]** 至 `United Parcel Service XML` 並執行下列動作：

   - 輸入您的UPS認證： **[!UICONTROL User ID]**， **[!UICONTROL Access License Number]** (16位數的UPS帳戶 `Access Key`)，以及 **[!UICONTROL Password]**

   - 設定 **[!UICONTROL Mode]** 至 `Live` 透過安全連線將資料傳送至UPS運送系統。 （開發模式不會透過安全連線傳送資料。）

   - 驗證 **[!UICONTROL Gateway XML URL]** 以XML檔案傳送要求時所需的專案。

   - 設定 **[!UICONTROL Origin of the Shipment]** 至出貨來源區域。

   - 如果您的UPS費率特殊，請設定 **[!UICONTROL Enable Negotiated Rates]** 至 `Yes` 並輸入6位數 **[!UICONTROL Shipper Number]** 由UPS指派給您。

1. 對於標準UPS帳戶，請設定 **[!UICONTROL UPS Type]** 至 `United Parcel Service` 並執行下列動作：

   >[!NOTE]
   >
   >標準United Parcel Service型別已排定淘汰。 若為新設定，您應使用預設值  `United Parcel Service XML` 型別。 還需要有XML型別才能產生 [送貨標籤](shipping-labels.md).

   - 設定 **[!UICONTROL Live Account]** 變更為下列其中一項：

      - `Yes`  — 以生產模式執行UPS，並提供UPS作為配送方式給您的客戶。
      - `No`  — 以測試模式執行UPS。

   - 在 **[!UICONTROL Gateway URL]** 欄位，輸入用於計算UPS運費的URL。

     >[!IMPORTANT]
     >
     >UPS將停止支援HTTP，目前預設值（系統值）會使用它。 清除 **[!UICONTROL Use system value]** 核取方塊，並修改URL以使用HTTPS。 範例： `https://www.ups.com/using/services/rave/qcostcgi.cgi`

1. 的 **[!UICONTROL Title]**，輸入此送貨選項的名稱，以方便您在結帳時顯示。

   依預設，此欄位設為 `United Parcel Service`.

   ![啟用UPS](../configuration-reference/sales/assets/delivery-methods-ups1.png){width="600" zoomable="yes"}

## 步驟3：完成容器說明

1. 設定 **[!UICONTROL Packages Request Type]** 變更為下列其中一項：

   - `Use origin weight (few requests)`
   - `Divide to equal weight (one request)`

1. 的 **[!UICONTROL Container]**，指定用於出貨的典型封裝型別：

   - `Customer Packaging`
   - `UPS Letter Envelope`
   - `Customer Supplied Package`
   - `UPS Tube`
   - `PAK`
   - `UPS Express Box`
   - `UPS Worldwide 25 kilo`
   - `UPS Worldwide 10 kilo`
   - `Pallet`
   - `Small Express Box`
   - `Medium Express Box`
   - `Large Express Box`

1. 設定 **[!UICONTROL Weight Unit]** 至您用來測量產品重量的系統。

   UPS支援的重量系統因國家而異。 如有疑問，請詢問UPS您應該使用哪個重量系統。 選項包括：

   - `LBS`
   - `KGS`

1. 設定 **[!UICONTROL Destination Type]** 變更為下列其中一項：

   - `Residential`  — 您的大部分出貨都是企業對消費者(B2C)。
   - `Commercial`  — 您的大部分出貨都是企業對企業(B2B)。

1. 輸入 **[!UICONTROL Maximum Package Weight]** 由電信業者允許。

1. 設定 **[!UICONTROL Pickup Method]** 變更為下列其中一項：

   - `Regular Daily Pickup`
   - `On Call Air`
   - `One Time Pickup`
   - `Letter Center`
   - `Customer Counter`

1. 輸入 **[!UICONTROL Minimum Package Weight]** 由電信業者允許。

   ![容器說明](./assets/ups2.png){width="600" zoomable="yes"}

## 步驟4：設定手續費

處理費是選擇性的，而且會顯示為UPS送貨成本的額外費用。 如果要包含手續費，請執行下列步驟：

1. 設定 **[!UICONTROL Calculate Handling Fee]** 變更為下列其中一種方法：

   - `Fixed`
   - `Percent`

1. 若要決定如何套用手續費，請設定 **[!UICONTROL Handling Applied]** 變更為下列其中一項：

   - `Per Order`
   - `Per Package`

1. 輸入 **[!UICONTROL Handling Fee]** 將被收費。

   若要輸入百分比，請使用小數格式。 例如，輸入 `0.25` 25%。

   ![手續費](./assets/ups3.png){width="600" zoomable="yes"}

## 步驟5：指定允許的方法和適用的國家

1. 的 **[!UICONTROL Allowed Methods]**，選擇可供客戶使用的各種UPS送貨方法。

   簽出時，方法會顯示在UPS底下。 若要選取多種方法，請按住Ctrl鍵(PC)或Command鍵(Mac)，然後按一下每個選項。

1. 如果您想提供 [免運費](shipping-free.md) 選項透過UPS，設定免費送貨選項：

   - 設定 **[!UICONTROL Free Method]** 改成您要用於免費送貨的方法。 如果您不想透過UPS提供免運費，請選擇 `None`.

   - 若要要求最低訂單金額以符合UPS免費送貨的訂單資格，請設定 **[!UICONTROL Enable Free Shipping Threshold]** 至 `Enable`. 然後，輸入最小值 **[!UICONTROL Free Shipping Amount Threshold]**.

1. 如有需要，請變更 **[!UICONTROL Displayed Error Message]**.

   此文字方塊預設為預設訊息，但您可以輸入在UPS無法使用時要顯示的不同訊息。

   ![允許的方法](./assets/ups4.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Ship to Applicable Countries]** 變更為下列其中一項：

   - `All Allowed Countries`  — 來自所有客戶的客戶 [國家/地區](../getting-started/store-details.md#country-options) 在存放區設定中指定時，可以使用此傳送方法。
   - `Specific Countries`  — 選擇此選項時， _送貨至特定國家_ 清單隨即顯示。 選取清單中可使用此傳遞方法的每個國家/地區。

1. 設定 **[!UICONTROL Show Method if Not Applicable]** 變更為下列其中一項：

   - `Yes`  — 列出結帳期間所有可用的UPS送貨方法，包括不適用於送貨的方法。
   - `No`  — 僅列出適用於出貨的UPS出貨方式。

   ![適用的國家/地區](./assets/ups5.png){width="600" zoomable="yes"}

1. 若要建立記錄檔，其中包含從您的商店發出的UPS運送詳細資料，請設定 **[!UICONTROL Debug]** 至 `Yes`.

1. 的 **[!UICONTROL Sort Order]**，請輸入數字，以決定結帳期間UPS與其他傳送方法一起列出時的顯示順序。

   `0` =第一個， `1` =秒， `2` =第三個，依此類推。

1. 按一下 **[!UICONTROL Save Config]**.

## 步驟6：設定出貨來源地址

1. 確定您的 [存放區資訊](../getting-started/store-details.md#store-information) 完成。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Sales]** 並選取 **[!UICONTROL Shipping Settings]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) **[!UICONTROL Origin]** 並設定送貨來源地址。

   ![銷售組態 — 出貨來源地址選項](./assets/shipping-origin.png){width="600" zoomable="yes"}

1. 按一下 **[!UICONTROL Save Config]**.

>[!NOTE]
>
>計算運費時，Commerce不會向UPS宣告完整的訂單價格。 此行為無法變更。
