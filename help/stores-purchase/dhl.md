---
title: DHL
description: 瞭解如何將DHL設定為您的商店的運送業者。
exl-id: 765e5f90-3e93-43cf-a5bc-6132e00b506c
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%

---

# DHL

DHL提供整合式國際服務，以及客製化的、以客戶為中心的解決方案，用於管理及運送信件、貨物及資訊。

## 步驟1：啟用DHL

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Sales]**&#x200B;並選擇&#x200B;**[!UICONTROL Delivery Methods]**。

1. 展開&#x200B;**[!UICONTROL DHL]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   >[!NOTE]
   >
   >如有必要，請先清除&#x200B;**[!UICONTROL Use system value]**&#x200B;核取方塊以變更下列設定，如所述。

1. 將&#x200B;**[!UICONTROL Enabled for Checkout]**&#x200B;設為`Yes`。

1. 通常您可以接受預設值&#x200B;**[!UICONTROL Gateway URL]**。

   如果DHL已為您指定替代URL，請在此欄位中輸入該值。

1. 使用DHL提供的憑證完成下列欄位：

   - **[!UICONTROL Access ID]**
   - **[!UICONTROL Password]**
   - **[!UICONTROL Account Number]**

![DHL帳戶設定](../configuration-reference/sales/assets/delivery-methods-dhl-account-settings.png){width="600" zoomable="yes"}

## 步驟2；輸入套件說明和處理費

1. 在&#x200B;**[!UICONTROL Content Type]**&#x200B;清單中，選取最能描述您出貨之封裝型別的選項：

   - `Documents`
   - `Non documents`

1. 根據您的要求設定手續費選項。

   處理費是選擇性的，並且會顯示為DHL運費增加的額外費用。 如果要包含手續費，請執行下列步驟：

   - 針對&#x200B;**[!UICONTROL Calculate Handling Fee]**，選取您要用來計算手續費的方法：

      - `Fixed`
      - `Percentage`

   - 針對&#x200B;**[!UICONTROL Handling Applied]**，選取您要如何套用處理費用：

      - `Per Order`
      - `Per Package`

   - 針對&#x200B;**[!UICONTROL Handling Fee]**，根據您選擇用來計算金額的方法，輸入要收取的金額。

     例如，如果費用是以固定費用為基礎，則以小數點輸入金額，例如`4.90`。 不過，如果處理費是以訂單的百分比為基準，請以百分比輸入金額。 例如，如果您要收取訂單的6%費用，請輸入值為`.06`。

   - 若要允許分解訂單總重量以確保準確計算運費，請將&#x200B;**[!UICONTROL Divide Order Weight]**&#x200B;設定為`Yes`。

   - 將封裝的&#x200B;**[!UICONTROL Weight Unit]**&#x200B;設定為下列其中一項：

      - `Pounds`
      - `Kilograms`

   - 將一般套件的&#x200B;**[!UICONTROL Size]**&#x200B;設定為下列其中一項：

      - `Regular`
      - `Specific`

     如果您選擇`Specific`，請輸入封裝的&#x200B;**[!UICONTROL Height]**、**[!UICONTROL Depth]**&#x200B;和&#x200B;**[!UICONTROL Width]** （公分）。

   ![DHL封裝設定](../configuration-reference/sales/assets/delivery-methods-dhl-package-settings.png){width="600" zoomable="yes"}

## 步驟3：指定允許的傳送方法

1. 針對&#x200B;**[!UICONTROL Allowed Methods]**，選擇您要提供給客戶的每個方法。

   若要選取多種方法，請按住Ctrl鍵(PC)或Command鍵(Mac)，然後按一下每個選項。

   若要顯示正確的傳遞方式清單，您必須先指定[原產國](../configuration-reference/sales/shipping-settings.md)。

1. 針對&#x200B;**[!UICONTROL Ready Time]**，輸入送出已準備出貨之訂單後的小時數。

1. 視需要編輯&#x200B;**[!UICONTROL Displayed Error Message]**。

   選取的方法無法使用時，此訊息便會出現。

1. 若要透過DHL提供[免費送貨](shipping-free.md)選項，請設定免費送貨選項。

   - 針對&#x200B;**[!UICONTROL Free Method]**，請選擇您偏好免費送貨的方法。

   - 設定&#x200B;**[!UICONTROL Free Shipping Amount Threshold]**：

     `Enable` — 如果提供最低訂單的免運費，請輸入&#x200B;**[!UICONTROL Minimum Order Amount for Free Shipping]**。

     `Disable` — 不將免費DHL送貨套用至任何訂單。

     此設定類似於標準&#x200B;_Free Shipping_&#x200B;方法的設定，但會顯示在DHL區段中，讓客戶知道其訂單使用哪種方法。

   - 針對&#x200B;**[!UICONTROL Free Shipping Amount Threshold]**，輸入訂單可免費送貨的最低金額。

     ![DHL允許的方法](../configuration-reference/sales/assets/delivery-methods-dhl-allowed-methods.png){width="600" zoomable="yes"}

## 步驟4：指定適用的國家

1. 將&#x200B;**[!UICONTROL Ship to Applicable Countries]**&#x200B;設定為下列其中一項：

   - `All Allowed Countries`
   - `Specific Countries`

   如果運送到特定國家，請從&#x200B;**[!UICONTROL Ship to Specific Countries]**&#x200B;清單中選取每個國家。

1. 設定&#x200B;**[!UICONTROL Show Method if Not Applicable]**：

   `Yes` — 在結帳期間將DHL顯示為送貨方法，即使不適用於該訂單亦然。

   `No` — 僅在適用的情況下，在結帳期間顯示DHL為送貨方法。

1. 若要建立記錄檔，其中包含從您的商店發出的DHL運送詳細資料，請將&#x200B;**[!UICONTROL Debug]**&#x200B;設為`Yes`。

1. 針對&#x200B;**[!UICONTROL Sort Order]**，請輸入數字以決定結帳期間與其他傳遞方法一起列出DHL時出現的順序。

   `0` =第一，`1` =第二，`2` =第三，依此類推。

1. 按一下&#x200B;**[!UICONTROL Save Config]**。

   ![DHL適用的國家/地區](../configuration-reference/sales/assets/delivery-methods-dhl-applicable-countries.png){width="600" zoomable="yes"}
