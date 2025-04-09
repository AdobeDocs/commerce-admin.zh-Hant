---
title: FedEx
description: 瞭解如何將FedEx設定為您的商店的運送業者。
exl-id: 75bb3ed1-3ae9-418a-be90-888046b28a7b
feature: Shipping/Delivery
source-git-commit: ad5da1d77b63bf6bcc0227a5c467e369b7bb8d89
workflow-type: tm+mt
source-wordcount: '899'
ht-degree: 0%

---

# FedEx

FedEx是世界上最大的航運服務公司之一，提供多種優先順序的空運、貨運及陸運服務。

結帳時有![FedEx運送選項](./assets/storefront-checkout-shipping-fedex.png){width="700" zoomable="yes"}

>[!NOTE]
>
>FedEx可以使用[維度權重](carriers.md#dimensional-weight)來決定某些運費。 不過，Adobe Commerce和Magento Open Source僅支援以重量為基礎的運送成本計算。

## 步驟1：註冊FedEx Web服務生產

需要FedEx商家帳戶和FedEx Web服務生產存取的註冊。 建立FedEx帳戶之後，請閱讀生產帳戶資訊頁，然後按一下頁面底部的&#x200B;_取得生產金鑰_&#x200B;連結，以註冊並取得金鑰。

>[!NOTE]
>
>請務必複製或寫下驗證金鑰。 必須在Commerce送貨設定中設定FedEx。

## 步驟2：為您的存放區啟用FedEx

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Sales]**&#x200B;並選擇&#x200B;**[!UICONTROL Delivery Methods]**。

1. 展開&#x200B;**[!UICONTROL FedEx]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

1. 將&#x200B;**[!UICONTROL Enabled for Checkout]**&#x200B;設為`Yes`。

1. 針對&#x200B;**[!UICONTROL Title]**，輸入在結帳時識別FedEx送貨方法的標題。

1. 從您的FedEx帳戶輸入下列資訊：

   - **[!UICONTROL Account ID]**
   - **[!UICONTROL Api Key]**
   - **[!UICONTROL Secret Key]**

1. 如果您有個別的追蹤API認證，請啟用下列設定：

   - **[!UICONTROL Enable Tracking API credentials]**

1. 從您的FedEx帳戶輸入下列資訊：

   - **[!UICONTROL Tracking API Key]**
   - **[!UICONTROL Tracking API Secret Key]**

1. 如果您已設定FedEx沙箱且想要在測試環境中工作，請將&#x200B;**[!UICONTROL Sandbox Mode]**&#x200B;設為`Yes`。

   >[!NOTE]
   >
   >當您準備好提供FedEx作為送貨方法給您的客戶時，請記得將沙箱模式設定為`No`。

   ![FedEx帳戶設定](../configuration-reference/sales/assets/delivery-methods-fedex-account-settings.png){width="600" zoomable="yes"}

## 步驟3：套件說明和處理費用

1. 將&#x200B;**[!UICONTROL Pickup Type]**&#x200B;設定為用於出貨的取貨方式。

   - `DropOff at Fedex Location` - （預設）表示您在本機FedEx站卸貨。
   - `Contact Fedex to Schedule` — 表示您連絡FedEx要求取車。
   - `Use Scheduled Pickup` — 表示出貨是作為定期排程取貨的一部分而取貨。
   - `On Call` — 表示已透過呼叫FedEx排程取車。
   - `Package Return Program` — 表示出貨是由FedEx Ground Package Returns Program取貨。
   - `Regular Stop` — 表示出貨是以定期取貨排程取貨。
   - `Tag` — 表示出貨取貨是特供Express貨簽或地面電話貨簽取貨請求使用。 這僅適用於回程送貨標籤。

1. 針對&#x200B;**[!UICONTROL Packages Request Type]**，選取將訂單分割為多筆出貨時，最能描述您偏好設定的請求型別：

   - `Divide to equal weight (one request)`
   - `Use origin weight (few requests)`

1. 針對&#x200B;**[!UICONTROL Packaging]**，選取您通常用來從商店出貨的FedEx封裝型別。

1. 將&#x200B;**[!UICONTROL Weight Unit]**&#x200B;設定為您的地區設定所使用的測量單位。

   - `Pounds`
   - `Kilograms`

1. 輸入FedEx出貨允許的&#x200B;**[!UICONTROL Maximum Package Weight]**。

   預設的FedEx最大重量為150磅。 如需詳細資訊，請洽詢您的運送公司。 除非您與FedEx有特殊安排，否則建議使用預設值。 如需詳細資訊，請參閱[維度權數](carriers.md#dimensional-weight)。

   ![FedEx封裝設定](../configuration-reference/sales/assets/delivery-methods-fedex-packaging.png){width="600" zoomable="yes"}

1. 根據您的要求設定手續費選項。

   處理費是選擇性的，在結帳期間不會顯示。 如果要包含手續費，請執行下列步驟：

   - 設定&#x200B;**[!UICONTROL Calculate Handling Fee]**：

      - `Fixed Fee`
      - `Percentage`

   - 針對&#x200B;**[!UICONTROL Handling Applied]**，選擇下列其中一種管理處理費的方法：

      - `Per Order`
      - `Per Package`

   - 根據計算方法，輸入&#x200B;**[!UICONTROL Handling Fee]**&#x200B;為`fixed`金額或`percentage`。

1. 設定&#x200B;**[!UICONTROL Residential Delivery]**&#x200B;為下列其中一項，視您銷售企業對消費者(B2C)或企業對企業(B2B)而定。

   - `Yes` — 適用於B2C住宅傳送。
   - `No` — 適用於B2B住宅傳送。

   ![FedEx處理費設定](../configuration-reference/sales/assets/delivery-methods-fedex-handling-fee.png){width="600" zoomable="yes"}

## 步驟4：允許的方法和適用的國家

1. 將&#x200B;**[!UICONTROL Allowed Methods]**&#x200B;設定為您要提供的每個出貨方式。

   選擇方法時，請考量您的FedEx帳戶、出貨的頻率和大小，以及是否允許國際出貨。 您可以視需要提供多種或多種方法，例如：

   - 歐洲第一優先順序
   - 交貨日選項：1天運費、2天運費、2天上午、2天運費、3天運費
   - 國內選項：Express Saver、Ground、First、Onight、Home Delivery、Standard Onight
   - 國際選項 — 國際經濟、國際經濟貨運、國際優先、國際地理、國際、優先國際
   - 優先順序選項 — 運費、隔夜優先順序
   - 提供Smart Post方法的Smart Post-If （輸入&#x200B;**中心ID**）
   - 運費選項 — 運費，國家運費

1. 若要透過FedEx提供[免運費](shipping-free.md)選項，請設定免運費選項。

   - 將&#x200B;**[!UICONTROL Free Method]**&#x200B;設為您要用於免費送貨的方法。 如果您不想透過FedEx提供免運費，請選擇`None`。

   - 若要要求符合FedEx免費送貨訂單的最低訂單金額，請將&#x200B;**[!UICONTROL Enable Free Shipping Threshold]**&#x200B;設為`Enable`。 然後，在&#x200B;**[!UICONTROL Free Shipping Amount Threshold]**&#x200B;中輸入最小值。

   此設定類似於標準Free Shipping方法的設定，但會在結帳時顯示在FedEx區段中，讓客戶知道用於其訂單的方法。

1. 如有需要，請變更&#x200B;**[!UICONTROL Displayed Error Message]**。

   此文字方塊已預設預設預設預設訊息，但您可以輸入其他訊息，以在FedEx無法使用時顯示。

   ![FedEx允許的傳遞方法](../configuration-reference/sales/assets/delivery-methods-fedex-delivery-methods.png){width="600" zoomable="yes"}

1. 設定&#x200B;**[!UICONTROL Ship to Applicable Countries]**：

   - `All Allowed Countries` — 來自您商店組態中指定的所有[國家/地區](../getting-started/store-details.md#country-options)的客戶都可以使用這個傳遞方法。

   - `Specific Countries` — 選擇此選項時，會顯示&#x200B;_送貨至特定國家_&#x200B;清單。 選取清單中可使用此傳遞方法的每個國家/地區。

1. 如果要保留存放區與FedEx系統之間所有通訊的記錄，請將&#x200B;**[!UICONTROL Debug]**&#x200B;設為`Yes`。

1. 設定&#x200B;**[!UICONTROL Show Method if Not Applicable]**：

   - `Yes` — 向客戶顯示所有FedEx送貨方法，無論其是否可用。
   - `No` — 僅顯示套用至訂單的FedEx送貨方法。

1. 針對&#x200B;**[!UICONTROL Sort Order]**，請輸入數字，以決定結帳期間與其他傳遞方法一起列出時，FedEx出現的順序。

   `0` =第一，`1` =第二，`2` =第三，依此類推。

1. 按一下&#x200B;**[!UICONTROL Save Config]**。

   ![FedEx適用國家/地區](../configuration-reference/sales/assets/delivery-methods-fedex-applicable-countries.png){width="600" zoomable="yes"}

>[!NOTE]
>
>計算運費時，Commerce一律會向FedEx宣告完整的訂單價格。 此行為無法變更。
