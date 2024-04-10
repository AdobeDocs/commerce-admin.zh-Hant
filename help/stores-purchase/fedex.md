---
title: FedEx
description: 瞭解如何將FedEx設定為您的商店的運送業者。
exl-id: 75bb3ed1-3ae9-418a-be90-888046b28a7b
feature: Shipping/Delivery
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '881'
ht-degree: 0%

---

# FedEx

FedEx是世界上最大的航運服務公司之一，提供多種優先順序的空運、貨運及陸運服務。

![結帳時的FedEx送貨選項](./assets/storefront-checkout-shipping-fedex.png){width="700" zoomable="yes"}

>[!NOTE]
>
>FedEx可以使用 [維度權數](carriers.md#dimensional-weight) 以決定某些運費。 不過，Adobe Commerce和Magento Open Source僅支援以重量為基礎的運送成本計算。

## 步驟1：註冊FedEx Web服務生產

A [FedEx商家帳戶][1] 需要註冊FedEx Web服務生產存取。 建立FedEx帳戶後，請閱讀生產帳戶資訊頁，然後按一下 _取得生產金鑰_ 頁面底部的連結，用以註冊及取得金鑰。

>[!NOTE]
>
>請務必複製或寫下驗證金鑰。 必須在Commerce送貨設定中設定FedEx。

## 步驟2：為您的存放區啟用FedEx

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Sales]** 並選擇 **[!UICONTROL Delivery Methods]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL FedEx]** 區段。

1. 設定 **[!UICONTROL Enabled for Checkout]** 至 `Yes`.

1. 的 **[!UICONTROL Title]**，輸入在結帳時識別FedEx送貨方法的標題。

1. 從您的FedEx帳戶輸入下列資訊：

   - **[!UICONTROL Account ID]**
   - **[!UICONTROL Api Key]**
   - **[!UICONTROL Secret Key]**

1. 如果您已設定FedEx沙箱且想要在測試環境中工作，請設定 **[!UICONTROL Sandbox Mode]** 至 `Yes`.

   >[!NOTE]
   >
   >記得將沙箱模式設定為 `No` 準備好提供FedEx作為送貨方式給客戶時。

   ![FedEx帳戶設定](../configuration-reference/sales/assets/delivery-methods-fedex-account-settings.png){width="600" zoomable="yes"}

## 步驟3：套件說明和處理費用

1. 設定 **[!UICONTROL Pickup Type]** 至用於出貨的取貨方式。

   - `DropOff at Fedex Location` - （預設）表示您在本地FedEx站卸貨。
   - `Contact Fedex to Schedule`  — 表示您聯絡FedEx要求取車。
   - `Use Scheduled Pickup`  — 表示出貨已作為定期排程取貨的一部分進行取貨。
   - `On Call`  — 表示已透過呼叫FedEx排程取車。
   - `Package Return Program`  — 表示出貨是由FedEx Ground Package Returns Program取貨。
   - `Regular Stop`  — 表示出貨是以定期取貨排程取貨。
   - `Tag`  — 表示出貨取貨是特供Express貨簽或Ground電話貨簽取貨請求。 這僅適用於回程送貨標籤。

1. 的 **[!UICONTROL Packages Request Type]**，選取將訂單分割為多筆出貨時，最能描述您偏好設定的請求型態：

   - `Divide to equal weight (one request)`
   - `Use origin weight (few requests)`

1. 的 **[!UICONTROL Packaging]**，選取您通常用來從商店出貨的FedEx包裝型別。

1. 設定 **[!UICONTROL Weight Unit]** 至您的地區設定中所使用的測量單位。

   - `Pounds`
   - `Kilograms`

1. 輸入 **[!UICONTROL Maximum Package Weight]** 允許用於FedEx出貨。

   預設的FedEx最大重量為150磅。 如需詳細資訊，請洽詢您的運送公司。 除非您與FedEx有特殊安排，否則建議使用預設值。 另請參閱 [維度權數](carriers.md#dimensional-weight) 以取得詳細資訊。

   ![FedEx封裝設定](../configuration-reference/sales/assets/delivery-methods-fedex-packaging.png){width="600" zoomable="yes"}

1. 根據您的要求設定手續費選項。

   處理費是選擇性的，在結帳期間不會顯示。 如果要包含手續費，請執行下列步驟：

   - 設定 **[!UICONTROL Calculate Handling Fee]**：

      - `Fixed Fee`
      - `Percentage`

   - 的 **[!UICONTROL Handling Applied]**，選擇下列其中一種管理處理費的方法：

      - `Per Order`
      - `Per Package`

   - 輸入 **[!UICONTROL Handling Fee]** 作為 `fixed` 金額或 `percentage`，視計算方法而定。

1. 設定 **[!UICONTROL Residential Delivery]** 對消費者(B2C)或企業對企業(B2B)的銷售情況。

   - `Yes`  — 適用於B2C住宅傳送。
   - `No`  — 適用於B2B住宅傳送。

   ![FedEx處理費設定](../configuration-reference/sales/assets/delivery-methods-fedex-handling-fee.png){width="600" zoomable="yes"}

## 步驟4：允許的方法和適用的國家

1. 設定 **[!UICONTROL Allowed Methods]** 您想要提供的每一種出貨方式。

   選擇方法時，請考量您的FedEx帳戶、出貨的頻率和大小，以及是否允許國際出貨。 您可以視需要提供多種或多種方法，例如：

   - 歐洲第一優先順序
   - 交貨日選項：1天運費、2天運費、2天上午、2天運費、3天運費
   - 國內選項：Express Saver、Ground、First、Onight、Home Delivery、Standard Onight
   - 國際選項 — 國際經濟、國際經濟貨運、國際優先、國際地理、國際、優先國際
   - 優先順序選項 — 運費、隔夜優先順序
   - 提供智慧型貼文方法的智慧型貼文(輸入 **中心ID**)
   - 運費選項 — 運費，國家運費

1. 如果您想提供 [免運費](shipping-free.md) 選項透過FedEx，設定免運費選項。

   - 設定 **[!UICONTROL Free Method]** 改成您要用於免費送貨的方法。 如果您不想透過FedEx提供免運費，請選擇 `None`.

   - 若要要求最低訂單金額以符合FedEx免費出貨的訂單資格，請設定 **[!UICONTROL Enable Free Shipping Threshold]** 至 `Enable`. 然後，輸入最小值 **[!UICONTROL Free Shipping Amount Threshold]**.

   此設定類似於標準Free Shipping方法的設定，但會在結帳時顯示在FedEx區段中，讓客戶知道用於其訂單的方法。

1. 如有需要，請變更 **[!UICONTROL Displayed Error Message]**.

   此文字方塊已預設預設預設預設訊息，但您可以輸入其他訊息，以在FedEx無法使用時顯示。

   ![FedEx允許的傳遞方法](../configuration-reference/sales/assets/delivery-methods-fedex-delivery-methods.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Ship to Applicable Countries]**：

   - `All Allowed Countries`  — 來自所有客戶的客戶 [國家/地區](../getting-started/store-details.md#country-options) 在存放區設定中指定時，可以使用此傳送方法。

   - `Specific Countries`  — 選擇此選項時， _送貨至特定國家_ 清單隨即顯示。 選取清單中可使用此傳遞方法的每個國家/地區。

1. 如果要保留存放區與FedEx系統之間所有通訊的記錄，請設定 **[!UICONTROL Debug]** 至 `Yes`.

1. 設定 **[!UICONTROL Show Method if Not Applicable]**：

   - `Yes`  — 向客戶顯示所有FedEx送貨方法，無論其是否可用。
   - `No`  — 僅顯示套用至訂單的FedEx送貨方法。

1. 的 **[!UICONTROL Sort Order]**，請輸入數字，以決定結帳期間FedEx與其他傳送方法一起列出時的顯示順序。

   `0` =第一個， `1` =秒， `2` =第三個，依此類推。

1. 按一下 **[!UICONTROL Save Config]**.

   ![FedEx適用國家/地區](../configuration-reference/sales/assets/delivery-methods-fedex-applicable-countries.png){width="600" zoomable="yes"}

>[!NOTE]
>
>計算運費時，Commerce一律會向FedEx宣告完整的訂單價格。 此行為無法變更。

[1]: https://www.fedex.com/login/web/jsp/contactInfo1.jsp
