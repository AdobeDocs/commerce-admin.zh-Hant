---
title: 聯合包裹服務(UPS)
description: 瞭解如何將UPS設定為您的商店的運送業者。
exl-id: a7965b2f-2473-4b63-a247-3b2230cde5d8
feature: Shipping/Delivery
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 0%

---

# 聯合包裹服務(UPS)

United Parcel Service (UPS)提供國內及國際的陸運及空運服務，服務對象超過220個國家。

{{ups-api}}

>[!NOTE]
>
>UPS可以使用[維度重量](carriers.md#dimensional-weight)來決定某些運費。 不過，Adobe Commerce僅支援重量型出貨成本計算。

## 步驟1：開啟UPS出貨帳戶

若要提供此送貨方式給您的客戶，您必須先使用UPS開立帳戶。

## 步驟2：為商店啟用UPS

1. 在&#x200B;_管理員側欄_&#x200B;上，前往&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側的面板中，在&#x200B;**[!UICONTROL Sales]**&#x200B;下選擇&#x200B;**[!UICONTROL Delivery Methods]**。

1. 展開&#x200B;**[!UICONTROL UPS]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

1. 將&#x200B;**[!UICONTROL Enabled for Checkout]**&#x200B;設為`Yes`。

1. 對於UPS REST帳戶（預設），請執行下列動作：

   - 輸入您的UPS認證： UPS使用者端ID為&#x200B;**[!UICONTROL User ID]**，UPS使用者端密碼為&#x200B;**[!UICONTROL Password]**

   - 將&#x200B;**[!UICONTROL Mode]**&#x200B;設為`Live`以透過安全連線傳送資料至UPS運送系統。 （開發模式不會透過安全連線傳送資料。）

   - 驗證傳送要求所需的&#x200B;**[!UICONTROL Gateway URL]**。 將沙箱URL用於測試模式，將生產URL用於即時請求。

   - 驗證取得追蹤資訊所需的&#x200B;**[!UICONTROL Tracking URL]**。 將沙箱URL用於測試模式，將生產URL用於即時請求。

   - 將&#x200B;**[!UICONTROL Origin of the Shipment]**&#x200B;設定為出貨來源區域。

   - 如果您的UPS費率特殊，請將&#x200B;**[!UICONTROL Enable Negotiated Rates]**&#x200B;設為`Yes`，並輸入UPS指派給您的六位數&#x200B;**[!UICONTROL Shipper Number]**。

   - 將&#x200B;**[!UICONTROL Live Account]**&#x200B;設定為下列其中一項：

      - `Yes` — 以生產模式執行UPS，並提供UPS作為送貨方式給您的客戶。
      - `No` — 在測試模式下執行UPS。

   >[!NOTE]
   >
   >標準United Parcel Service型別已排定淘汰。 對於新組態，請使用預設`United Parcel Service REST`型別。 REST型別也需要產生[送貨標籤](shipping-labels.md).<br/>
   >在2.4.7版本中，**[!UICONTROL UPS Type]**&#x200B;已移除，因為`UPS`和`UPS XML`型別已排定棄用，而`UPS REST`為預設值。 原生Adobe Commerce整合所使用的United Parcel Service (UPS) API暫時被取代，因為它目前不支援OAuth 2.0安全性模型。

   >[!IMPORTANT]
   >
   >UPS將停止支援HTTP，目前預設值（系統值）會使用它。 清除&#x200B;**[!UICONTROL Use system value]**&#x200B;核取方塊並修改URL以使用HTTPS。 範例： `https://www.ups.com/using/services/rave/qcostcgi.cgi`

1. 針對&#x200B;**[!UICONTROL Title]**，輸入此送貨選項的名稱，以使其在結帳時顯示。

   依預設，此欄位設為`United Parcel Service`。

   ![啟用UPS](../configuration-reference/sales/assets/delivery-methods-ups1.png){width="600" zoomable="yes"}

## 步驟3：完成容器說明

1. 將&#x200B;**[!UICONTROL Packages Request Type]**&#x200B;設定為下列其中一項：

   - `Use origin weight (few requests)`
   - `Divide to equal weight (one request)`

1. 針對&#x200B;**[!UICONTROL Container]**，指定用於出貨的典型封裝型別：

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

1. 將&#x200B;**[!UICONTROL Weight Unit]**&#x200B;設定為您用來測量產品重量的系統。

   UPS支援的重量系統因國家而異。 如有疑問，請詢問UPS您應該使用哪個重量系統。 選項包括：

   - `LBS`
   - `KGS`

1. 將&#x200B;**[!UICONTROL Destination Type]**&#x200B;設定為下列其中一項：

   - `Residential` — 您的大部分出貨都是企業對消費者(B2C)。
   - `Commercial` — 您的大部分出貨都是企業對企業(B2B)。

1. 輸入電信業者允許的&#x200B;**[!UICONTROL Maximum Package Weight]**。

1. 將&#x200B;**[!UICONTROL Pickup Method]**&#x200B;設定為下列其中一項：

   - `Regular Daily Pickup`
   - `On Call Air`
   - `One Time Pickup`
   - `Letter Center`
   - `Customer Counter`

1. 輸入電信業者允許的&#x200B;**[!UICONTROL Minimum Package Weight]**。

   ![容器說明](./assets/ups2.png){width="600" zoomable="yes"}

## 步驟4：設定手續費

處理費是選擇性的，而且會顯示為UPS送貨成本的額外費用。 如果要包含手續費，請執行下列步驟：

1. 將&#x200B;**[!UICONTROL Calculate Handling Fee]**&#x200B;設為下列其中一種方法：

   - `Fixed`
   - `Percent`

1. 若要決定如何套用手續費，請將&#x200B;**[!UICONTROL Handling Applied]**&#x200B;設為下列其中一項：

   - `Per Order`
   - `Per Package`

1. 輸入要收費的&#x200B;**[!UICONTROL Handling Fee]**&#x200B;金額。

   若要輸入百分比，請使用小數格式。 例如，輸入`0.25`表示25%。

   ![手續費](./assets/ups3.png){width="600" zoomable="yes"}

## 步驟5：指定允許的方法和適用的國家

1. 針對&#x200B;**[!UICONTROL Allowed Methods]**，選擇客戶可用的各種UPS送貨方法。

   簽出時，方法會顯示在UPS底下。 若要選取多種方法，請按住Ctrl鍵(PC)或Command鍵(Mac)，然後按一下每個選項。

1. 如果您要透過UPS提供[免運費](shipping-free.md)選項，請設定免運費選項：

   - 將&#x200B;**[!UICONTROL Free Method]**&#x200B;設為您要用於免費送貨的方法。 如果您不想透過UPS提供免運費，請選擇`None`。

   - 若要要求符合UPS免費送貨訂單的最低訂單金額，請將&#x200B;**[!UICONTROL Enable Free Shipping Threshold]**&#x200B;設為`Enable`。 然後，在&#x200B;**[!UICONTROL Free Shipping Amount Threshold]**&#x200B;中輸入最小值。

1. 如有需要，請變更&#x200B;**[!UICONTROL Displayed Error Message]**。

   此文字方塊預設為預設訊息，但您可以輸入在UPS無法使用時要顯示的不同訊息。

   ![允許的方法](./assets/ups4.png){width="600" zoomable="yes"}

1. 將&#x200B;**[!UICONTROL Ship to Applicable Countries]**&#x200B;設定為下列其中一項：

   - `All Allowed Countries` — 來自您商店組態中指定的所有[國家/地區](../getting-started/store-details.md#country-options)的客戶都可以使用這個傳遞方法。
   - `Specific Countries` — 選擇此選項時，會顯示&#x200B;_送貨至特定國家_&#x200B;清單。 選取清單中可使用此傳遞方法的每個國家/地區。

1. 將&#x200B;**[!UICONTROL Show Method if Not Applicable]**&#x200B;設定為下列其中一項：

   - `Yes` — 列出結帳期間所有可用的UPS送貨方法，包括不適用於送貨的方法。
   - `No` — 僅列出適用於運送的UPS運送方式。

   ![適用的國家/地區](./assets/ups5.png){width="600" zoomable="yes"}

1. 若要建立記錄檔，其中包含從您的商店發出的UPS運送詳細資料，請將&#x200B;**[!UICONTROL Debug]**&#x200B;設為`Yes`。

1. 針對&#x200B;**[!UICONTROL Sort Order]**，請輸入數字，以決定結帳期間與其他傳遞方法一起列出UPS時的顯示順序。

   `0` =第一，`1` =第二，`2` =第三，依此類推。

1. 按一下&#x200B;**[!UICONTROL Save Config]**。

## 步驟6：設定出貨來源地址

1. 確定您的[存放區資訊](../getting-started/store-details.md#store-information)已完成。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Sales]**&#x200B;並選取&#x200B;**[!UICONTROL Shipping Settings]**。

1. 展開頁面上的![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Origin]**&#x200B;並設定出貨來源地址。

   ![銷售組態 — 出貨來源地址選項](./assets/shipping-origin.png){width="600" zoomable="yes"}

1. 按一下&#x200B;**[!UICONTROL Save Config]**。

>[!NOTE]
>
>計算運費時，Commerce不會向UPS宣告完整的訂單價格。 此行為無法變更。
