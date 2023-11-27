---
title: DHL
description: 瞭解如何將DHL設定為您的商店的運送業者。
exl-id: 765e5f90-3e93-43cf-a5bc-6132e00b506c
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 0%

---

# DHL

DHL提供整合式國際服務，以及客製化的、以客戶為中心的解決方案，用於管理及運送信件、貨物及資訊。

## 步驟1：啟用DHL

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Sales]** 並選擇 **[!UICONTROL Delivery Methods]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL DHL]** 區段。

   >[!NOTE]
   >
   >如有必要，請先清除 **[!UICONTROL Use system value]** 核取方塊來變更下列設定，如所述。

1. 設定 **[!UICONTROL Enabled for Checkout]** 至 `Yes`.

1. 通常，您可以接受預設值 **[!UICONTROL Gateway URL]**.

   如果DHL已為您指定替代URL，請在此欄位中輸入該值。

1. 使用DHL提供的憑證完成下列欄位：

   - **[!UICONTROL Access ID]**
   - **[!UICONTROL Password]**
   - **[!UICONTROL Account Number]**

![DHL帳戶設定](../configuration-reference/sales/assets/delivery-methods-dhl-account-settings.png){width="600" zoomable="yes"}

## 步驟2；輸入套件說明和處理費

1. 在 **[!UICONTROL Content Type]** 清單中，選取最能描述您出貨之封裝型別的選項：

   - `Documents`
   - `Non documents`

1. 根據您的要求設定手續費選項。

   處理費是選擇性的，並且會顯示為DHL運費增加的額外費用。 如果要包含手續費，請執行下列步驟：

   - 的 **[!UICONTROL Calculate Handling Fee]**，選取您要用來計算手續費的方法：

      - `Fixed`
      - `Percentage`

   - 的 **[!UICONTROL Handling Applied]**，選取您要如何套用手續費：

      - `Per Order`
      - `Per Package`

   - 的 **[!UICONTROL Handling Fee]**，根據您選擇用來計算金額的方法，輸入要收取的金額。

     例如，如果費用是以固定費用為基礎，則以小數點輸入金額，例如 `4.90`. 不過，如果處理費是以訂單的百分比為基準，請以百分比輸入金額。 例如，如果您對訂單的6%計費，則輸入值為 `.06`.

   - 若要允許分解訂單總重量以確保準確計算出貨費用，請設定 **[!UICONTROL Divide Order Weight]** 至 `Yes`.

   - 設定 **[!UICONTROL Weight Unit]** 封裝的下列其中一個專案：

      - `Pounds`
      - `Kilograms`

   - 設定 **[!UICONTROL Size]** 將典型封裝型別變更為下列其中一項：

      - `Regular`
      - `Specific`

     如果您選擇 `Specific`，輸入 **[!UICONTROL Height]**， **[!UICONTROL Depth]**、和 **[!UICONTROL Width]** 公分（以公分為單位）。

   ![DHL封裝設定](../configuration-reference/sales/assets/delivery-methods-dhl-package-settings.png){width="600" zoomable="yes"}

## 步驟3：指定允許的傳送方法

1. 的 **[!UICONTROL Allowed Methods]**，選擇您想要讓客戶使用的每個方法。

   若要選取多種方法，請按住Ctrl鍵(PC)或Command鍵(Mac)，然後按一下每個選項。

   若要顯示正確的傳遞方式清單，您必須先指定 [原產國/地區](../configuration-reference/sales/shipping-settings.md).

1. 的 **[!UICONTROL Ready Time]**，輸入在提交訂單後，封裝準備出貨的小時數。

1. 編輯 **[!UICONTROL Displayed Error Message]** 視需要。

   選取的方法無法使用時，此訊息便會出現。

1. 如果您想提供 [免運費](shipping-free.md) 選項透過DHL，設定免費送貨選項。

   - 的 **[!UICONTROL Free Method]**，選擇您偏好用於免運費的方法。

   - 設定 **[!UICONTROL Free Shipping Amount Threshold]**：

     `Enable`  — 如果提供最少訂單的免運費，請輸入 **[!UICONTROL Minimum Order Amount for Free Shipping]**.

     `Disable`  — 不將免費DHL運送套用至任何訂單。

     此設定類似於標準設定 _免運費_ 方法，但會出現在DHL區段中，讓客戶知道用於其訂單的方法。

   - 的 **[!UICONTROL Free Shipping Amount Threshold]**，輸入訂單可免費送貨的最低金額。

     ![DHL允許的方法](../configuration-reference/sales/assets/delivery-methods-dhl-allowed-methods.png){width="600" zoomable="yes"}

## 步驟4：指定適用的國家

1. 設定 **[!UICONTROL Ship to Applicable Countries]** 變更為下列其中一項：

   - `All Allowed Countries`
   - `Specific Countries`

   如果運送到特定國家/地區，請從 **[!UICONTROL Ship to Specific Countries]** 清單。

1. 設定 **[!UICONTROL Show Method if Not Applicable]**：

   `Yes`  — 在結帳期間顯示DHL為送貨方法，即使不適用於該訂單亦然。

   `No`  — 僅在適用的情況下，在結帳期間顯示DHL作為送貨方法。

1. 若要建立記錄檔，其中包含從您的商店發出的DHL運送詳細資料，請設定 **[!UICONTROL Debug]** 至 `Yes`.

1. 的 **[!UICONTROL Sort Order]**，請輸入數字，以決定結帳期間DHL與其他傳送方法一起列出時的顯示順序。

   `0` =第一個， `1` =秒， `2` =第三個，依此類推。

1. 按一下 **[!UICONTROL Save Config]**.

   ![DHL適用國家/地區](../configuration-reference/sales/assets/delivery-methods-dhl-applicable-countries.png){width="600" zoomable="yes"}
