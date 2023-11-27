---
title: 美國郵政服務(USPS)
description: 瞭解如何將USPS設定為您的商店的運送業者。
exl-id: c9601fb8-f0f9-484a-a2e1-d50ee0f2dbf0
feature: Shipping/Delivery
source-git-commit: 50b44190a9568a8d6ad38ab29177904596569d75
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 0%

---

# 美國郵政服務(USPS)

美國郵政服務是美國政府的獨立郵政服務，提供國內及國際的陸運及空運服務。

## 步驟1：開啟USPS出貨帳戶

開啟 [USPS Web Tools][1] 帳戶。 完成註冊程式後，您將會收到使用者ID和USPS測試伺服器的URL。

您也可以開啟 [USPS Web Tools][1] 帳戶。 完成註冊程式後，您將會收到使用者ID和USPS測試伺服器的URL。 若要深入瞭解USPS網頁工具，請參閱其 [技術檔案][2].

## 步驟2：為商店啟用USPS

{{beta2-updates}}

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Sales]** 並選擇 **[!UICONTROL Delivery Methods]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL USPS]** 區段。

   >[!NOTE]
   >
   >如有必要，請先取消選取 **[!UICONTROL Use system value]** 核取方塊來變更下列設定，如所述。

1. 設定 **[!UICONTROL Enabled for Checkout]** 至 `Yes`.

1. 如有需要，請輸入 **[!UICONTROL Gateway URL]** 以存取USPS運費。

   >[!IMPORTANT]
   >
   >自2021年6月24日起，USPS網頁工具將移除對所有不安全HTTP端點的支援。 進行此變更後，對不安全HTTP端點的所有Web工具API請求都將失敗。 確定您的 **[!UICONTROL Gateway URL]** 使用安全的HTTPS端點。

   預設會預設欄位，通常不需要變更。

1. 輸入 **[!UICONTROL Title]** 此送貨方法會在結帳時顯示。

1. 輸入 **[!UICONTROL User ID]** 和 **[!UICONTROL Password]** （適用於您的USPS帳戶）。

1. 設定 **[!UICONTROL Mode]** 變更為下列其中一項：

   - `Development`  — 在測試環境中執行USPS。 在開發環境中執行USPS後，請務必稍後返回，並將模式設定為 `Live`.
   - `Live`  — 在即時生產環境中執行USPS。

## 步驟3：完成封裝說明

1. 若要確定當訂單以多個封裝形式傳送時如何管理，請設定 **[!UICONTROL Packages Request Type]** 變更為下列其中一項：

   - `Divide to Equal Weight` - （一個請求）如果多個包裹的運送量除以等重，則可以作為一個請求來提交。
   - `Use Origin Weight` - （多重請求）如果使用原始重量作為計算出貨成本的基準，則必須以個別請求提交多個套件。

1. 設定 **[!UICONTROL Container]** 通常用於運送商店所訂購產品的包裝型別。

1. 設定 **[!UICONTROL Size]** 從您的商店寄出的典型套件。

1. 設定 **[!UICONTROL Machinable]** 變更為下列其中一項：

   - `Yes`  — 如果您的典型封裝可以由電腦處理。
   - `No`  — 如果您的典型套件必須手動處理。

1. 輸入 **[!UICONTROL Maximum Package Weight]** 根據電信業者需求。

   ![USPS封裝設定](../configuration-reference/sales/assets/delivery-methods-usps-packaging.png){width="600" zoomable="yes"}

## 步驟4：設定手續費

處理費是選擇性的，並且會顯示為DHL運費增加的額外費用。 如果要包含手續費，請執行下列步驟：

1. 設定 **[!UICONTROL Calculate Handling Fee]** 變更為下列其中一種方法：

   - `Fixed`
   - `Percent`

1. 若要決定如何套用手續費，請設定 **[!UICONTROL Handling Applied]** 變更為下列其中一項：

   - `Per Order`
   - `Per Package`

1. 輸入 **[!UICONTROL Handling Fee]** 將被收費。

   若要輸入百分比，請使用小數格式。 例如，輸入 `0.25` 25%。

   ![USPS處理費](../configuration-reference/sales/assets/delivery-methods-usps-handling-fee.png){width="600" zoomable="yes"}

## 步驟5：指定允許的方法和適用的國家

1. 的 **[!UICONTROL Allowed Methods]**，選擇客戶可用的各種USPS送貨方法。

   結帳時，方法會顯示在USPS下。 若要選取多種方法，請按住Ctrl鍵(PC)或Command鍵(Mac)，然後按一下每個選項。

1. 如果您想提供 [免運費](shipping-free.md) 選項透過USPS，設定免費送貨選項：

   - 設定 **[!UICONTROL Free Method]** 改成您要用於免費送貨的方法。 如果您不想透過USPS提供免運費，請選擇 `None`.

   - 若要要求最低訂單金額以符合USPS免費送貨的訂單資格，請設定 **[!UICONTROL Enable Free Shipping Threshold]** 至 `Enable`. 然後，輸入最小值 **[!UICONTROL Free Shipping Amount Threshold]**.

1. 如有需要，請變更 **[!UICONTROL Displayed Error Message]**.

   此文字方塊已預設預設預設預設訊息，但您可以輸入在USPS無法使用時要顯示的不同訊息。

   ![USPS允許的方法](../configuration-reference/sales/assets/delivery-methods-usps-allowed-methods.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Ship to Applicable Countries]** 變更為下列其中一項：

   - `All Allowed Countries`  — 來自所有客戶的客戶 [國家/地區](../getting-started/store-details.md#country-options) 在存放區設定中指定時，可以使用此傳送方法。
   - `Specific Countries`  — 選擇此選項時， _送貨至特定國家_ 清單隨即顯示。 選取清單中可使用此傳遞方法的每個國家/地區。

   ![USPS適用的國家/地區](../configuration-reference/sales/assets/delivery-methods-usps-countries.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Show Method if Not Applicable]** 變更為下列其中一項：

   - `Yes`  — 列出結帳期間所有可用的USPS送貨方法，包括不適用於送貨的方法。
   - `No`  — 僅列出適用於出貨的USPS出貨方法。

1. 若要建立記錄檔，其中包含從您的商店發出的USPS貨物的詳細資料，請設定 **[!UICONTROL Debug]** 至 `Yes`.

1. 的 **[!UICONTROL Sort Order]**，請輸入數字，以決定結帳期間USPS與其他傳送方法一起列出時的顯示順序。

   `0` =第一個， `1` =秒， `2` =第三個，依此類推。

1. 按一下 **[!UICONTROL Save Config]**.


[1]: https://secure.shippingapis.com/registration/
[2]: https://www.usps.com/business/web-tools-apis/welcome.htm
