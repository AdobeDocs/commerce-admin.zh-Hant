---
title: 美國郵政服務(USPS)
description: 瞭解如何將USPS設定為您的商店的運送業者。
exl-id: c9601fb8-f0f9-484a-a2e1-d50ee0f2dbf0
feature: Shipping/Delivery
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 0%

---

# 美國郵政服務(USPS)

美國郵政服務是美國政府的獨立郵政服務，提供國內及國際的陸運及空運服務。

## 步驟1：開啟USPS出貨帳戶

開啟[USPS Web Tools][1]帳戶。 完成註冊程式後，您將會收到使用者ID和USPS測試伺服器的URL。

您也可以開啟[USPS Web Tools][1]帳戶。 完成註冊程式後，您將會收到使用者ID和USPS測試伺服器的URL。 若要深入瞭解USPS Web工具，請參閱其[技術檔案][2]。

## 步驟2：為商店啟用USPS

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Sales]**&#x200B;並選擇&#x200B;**[!UICONTROL Delivery Methods]**。

1. 展開&#x200B;**[!UICONTROL USPS]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   >[!NOTE]
   >
   >如有必要，請先取消選取&#x200B;**[!UICONTROL Use system value]**&#x200B;核取方塊以變更下列設定，如所述。

1. 將&#x200B;**[!UICONTROL Enabled for Checkout]**&#x200B;設為`Yes`。

1. 如有需要，請輸入&#x200B;**[!UICONTROL Gateway URL]**&#x200B;以存取USPS運費。

   >[!IMPORTANT]
   >
   >自2021年6月24日起，USPS網頁工具將移除對所有不安全HTTP端點的支援。 進行此變更後，對不安全HTTP端點的所有Web工具API請求都將失敗。 確定您的&#x200B;**[!UICONTROL Gateway URL]**&#x200B;使用安全的HTTPS端點。

   預設會預設欄位，通常不需要變更。

1. 輸入此送貨方式的&#x200B;**[!UICONTROL Title]**，此送貨方式會在結帳時顯示。

1. 輸入您USPS帳戶的&#x200B;**[!UICONTROL User ID]**&#x200B;和&#x200B;**[!UICONTROL Password]**。

1. 將&#x200B;**[!UICONTROL Mode]**&#x200B;設定為下列其中一項：

   - `Development` — 在測試環境中執行USPS。 在開發環境中執行USPS之後，請確定稍後再傳回，並將Mode設定為`Live`。
   - `Live` — 在即時生產環境中執行USPS。

## 步驟3：完成封裝說明

1. 若要判斷以多個套件傳送時如何管理訂單，請將&#x200B;**[!UICONTROL Packages Request Type]**&#x200B;設定為下列其中一項：

   - `Divide to Equal Weight` - （一個要求）如果多個包裹的運送量除以相等的權重，則可以作為一個要求來提交。
   - `Use Origin Weight` - （多個請求）如果使用原始重量作為計算運費的基礎，則必須以個別請求提交多個套件。

1. 將&#x200B;**[!UICONTROL Container]**&#x200B;設定為通常用來運送商店所訂購產品的包裝型別。

1. 設定從您的商店寄出的典型套件的&#x200B;**[!UICONTROL Size]**。

1. 將&#x200B;**[!UICONTROL Machinable]**&#x200B;設定為下列其中一項：

   - `Yes` — 如果您的典型封裝可以由電腦處理。
   - `No` — 如果您的典型封裝必須手動處理。

1. 根據電信業者需求輸入&#x200B;**[!UICONTROL Maximum Package Weight]**。

   ![USPS封裝設定](../configuration-reference/sales/assets/delivery-methods-usps-packaging.png){width="600" zoomable="yes"}

## 步驟4：設定手續費

處理費是選擇性的，並且會顯示為DHL運費增加的額外費用。 如果要包含手續費，請執行下列步驟：

1. 將&#x200B;**[!UICONTROL Calculate Handling Fee]**&#x200B;設為下列其中一種方法：

   - `Fixed`
   - `Percent`

1. 若要決定如何套用手續費，請將&#x200B;**[!UICONTROL Handling Applied]**&#x200B;設為下列其中一項：

   - `Per Order`
   - `Per Package`

1. 輸入要收費的&#x200B;**[!UICONTROL Handling Fee]**&#x200B;金額。

   若要輸入百分比，請使用小數格式。 例如，輸入`0.25`表示25%。

   ![USPS處理費](../configuration-reference/sales/assets/delivery-methods-usps-handling-fee.png){width="600" zoomable="yes"}

## 步驟5：指定允許的方法和適用的國家

1. 針對&#x200B;**[!UICONTROL Allowed Methods]**，選擇客戶可用的各種USPS送貨方法。

   結帳時，方法會顯示在USPS下。 若要選取多種方法，請按住Ctrl鍵(PC)或Command鍵(Mac)，然後按一下每個選項。

1. 若要透過USPS提供[免運費](shipping-free.md)選項，請設定免運費選項：

   - 將&#x200B;**[!UICONTROL Free Method]**&#x200B;設為您要用於免費送貨的方法。 如果您不想透過USPS提供免運費，請選擇`None`。

   - 若要要求符合USPS免費送貨訂單的最低訂單金額，請將&#x200B;**[!UICONTROL Enable Free Shipping Threshold]**&#x200B;設為`Enable`。 然後，在&#x200B;**[!UICONTROL Free Shipping Amount Threshold]**&#x200B;中輸入最小值。

1. 如有需要，請變更&#x200B;**[!UICONTROL Displayed Error Message]**。

   此文字方塊已預設預設預設預設訊息，但您可以輸入在USPS無法使用時要顯示的不同訊息。

   ![USPS允許的方法](../configuration-reference/sales/assets/delivery-methods-usps-allowed-methods.png){width="600" zoomable="yes"}

1. 將&#x200B;**[!UICONTROL Ship to Applicable Countries]**&#x200B;設定為下列其中一項：

   - `All Allowed Countries` — 來自您商店組態中指定的所有[國家/地區](../getting-started/store-details.md#country-options)的客戶都可以使用這個傳遞方法。
   - `Specific Countries` — 選擇此選項時，會顯示&#x200B;_送貨至特定國家_&#x200B;清單。 選取清單中可使用此傳遞方法的每個國家/地區。

   ![USPS適用的國家/地區](../configuration-reference/sales/assets/delivery-methods-usps-countries.png){width="600" zoomable="yes"}

1. 將&#x200B;**[!UICONTROL Show Method if Not Applicable]**&#x200B;設定為下列其中一項：

   - `Yes` — 列出結帳期間所有可用的USPS送貨方法，包括不適用於送貨的方法。
   - `No` — 僅列出適用於出貨的USPS出貨方法。

1. 若要建立記錄檔，其中包含從您的商店發出的USPS運送詳細資料，請將&#x200B;**[!UICONTROL Debug]**&#x200B;設為`Yes`。

1. 針對&#x200B;**[!UICONTROL Sort Order]**，輸入數字以決定結帳期間與其他傳遞方法一起列出USPS時的顯示順序。

   `0` =第一，`1` =第二，`2` =第三，依此類推。

1. 按一下&#x200B;**[!UICONTROL Save Config]**。


[1]: https://secure.shippingapis.com/registration/
[2]: https://www.usps.com/business/web-tools-apis/welcome.htm
