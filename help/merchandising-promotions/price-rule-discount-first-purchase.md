---
title: 購物車價格規則範例 — 首次購買折扣
description: 檢閱使用購物車價格規則為首次客戶提供折扣的範例。
exl-id: 46add769-6fa9-40e0-9f4f-af2215f36283
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: dbe31fa6e7b83ac852e6e4988ac61627e30d9089
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 0%

---

# 購物車價格規則範例 — 首次購買折扣

{{ee-feature}}

購物車價格規則可用於在客戶首次購買時自動提供折扣，而不需要優惠券。

若要提供針對首次客戶的折扣，您可以：

- 建立客戶區段，定義為 _沒有訂單的購買者_，然後
- 建立鎖定新客戶區段的購物車價格規則。

>[!NOTE]
>
>確認已啟用客戶區段功能。 請參閱 [建立客戶區段](../customers/customer-segment-create.md).

## 步驟1. 建立客戶區段

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Customers]** > **[!UICONTROL Segments]**.

1. 在右上角，按一下 **[!UICONTROL Add Segment]**.

1. 定義 **[!UICONTROL General Properties]**.

   - 輸入 **[!UICONTROL Segment Name]** 以識別客戶區段(範例： _首次客戶_)。

   - 的 **[!UICONTROL Assigned to Website]**，選取可以使用客戶區段的網站。

   - 的 **[!UICONTROL Status]**，選取 `Active`.

   - 的 **[!UICONTROL Apply to]**，選取 `Visitors and Registered Customers`.

   - 完成後，按一下 **[!UICONTROL Save and Continue Edit]**.

     左側面板中會顯示其他選項。

   ![客戶區段屬性](./assets/customer-segment-first-time.png){width="600" zoomable="yes"}

1. 定義 **[!UICONTROL Conditions]**.

   在此範例中，條件會鎖定目標客戶 _訂單總數小於1_ 為True。

   - 在左側的面板中，選擇 **[!UICONTROL Conditions]**.

     預設條件會開始：「如果所有這些條件均為TRUE：」

   - 按一下 _新增_ (![「新增」圖示](../assets/icon-add-green-circle.png))並選取 `Number of Orders`.

   - 按一下 **[!UICONTROL is]** 並選取 `less than`.

   - 按一下 **...** 並輸入 `1` 在欄位中。

   - 按一下綠色核取記號( ![綠色核取標籤](../assets/icon-checkmark-green-circle.png) )以儲存條件設定。

   ![客戶區段條件](./assets/customer-segment-first-time-condition.png){width="600" zoomable="yes"}

1. 按一下 **[!UICONTROL Save]**.

客戶區段會建立並顯示在 _[!UICONTROL Customer Segments]_格線。

>[!TIP]
>
>記下區段ID。 您可以使用此ID號碼建立購物車價格規則。

## 步驟2. 建立購物車價格規則

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rule]**.

1. 在右上角，按一下 **[!UICONTROL Add New Rule]**.

   此 **[!UICONTROL Rule Information]** 依預設會顯示截面，其可展開的截面用於 **[!UICONTROL Conditions]** 和 **[!UICONTROL Conditions]**.

1. 定義 **[!UICONTROL Rule Information]**.

   - 完成 **[!UICONTROL Rule Name]** 和 **[!UICONTROL Description]** 欄位。 這些欄位僅供內部參考。

   - 的 **[!UICONTROL Websites]**，選取可使用規則的網站。

   - 的 **[!UICONTROL Customer Groups]**，選取要套用此規則的客戶群組。

     若要選取多個群組，請按住Ctrl鍵(PC)或Command鍵(Mac)，然後按一下每個選項。

     >[!NOTE]
     >
     >此清單中的選項取決於在中建立和管理的客戶群組 **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

   - 的 **[!UICONTROL Coupon]**，選取 `No Coupon`.

   - 的 **[!UICONTROL Uses per Customer]**，輸入 `1`.

   - 的 **[!UICONTROL Priority]**，請輸入數字，以建立此規則相對於其他規則的優先順序。

     >[!NOTE]
     >
     >當相同的目錄產品符合為多個價格規則設定的條件時，「優先順序」設定很重要。 具有最高優先順序設定的規則會針對客戶啟用。 最高優先順序為1。 在此範例中，輸入 `1` 表示此規則會先於任何其他價格規則套用。 此值由 **[!UICONTROL Discard Subsequent Rules]** 在中設定 **[!UICONTROL Action]** 區段。

   - 完成後，按一下 **[!UICONTROL Save and Continue Edit]**.

     左側面板中會顯示其他選項。

   ![購物車價格規則資訊](./assets/rule-information-first-time.png){width="600" zoomable="yes"}

1. 定義 **[!UICONTROL Conditions]**.

   - 向下捲動並展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Conditions]** 區段。

     預設規則會以「如果所有這些條件皆為TRUE：」開始。

   - 按一下 _新增_ (![「新增」圖示](../assets/icon-add-green-circle.png))並選取 `Customer Segment`.

     限定詞欄位預設為 `matches`.

   - 按一下 **...** 並輸入您要鎖定的客戶區段的區段識別碼。

     在此範例中，在步驟1建立的新區段的區段ID為 `2`.

     >[!NOTE]
     >
     >如果您不知道區段ID，請按一下選擇器圖示( ![清單圖示](../assets/icon-list-chooser.png) )以顯示「客戶區段」清單。 您可以在欄位中手動輸入ID，或選取所需區段的核取方塊以自動填入欄位。

   - 按一下綠色核取記號( ![綠色核取標籤](../assets/icon-checkmark-green-circle.png) )以儲存條件設定。

   - 完成後，按一下 **[!UICONTROL Save and Continue Edit]**.

     此規則行適用於符合客戶區段ID 2的所有客戶。

   ![客戶區段條件](./assets/customer-segment-matches.png){width="400"}

1. 向下捲動並展開 ![展開選擇器](../assets/icon-display-expand.png)此 **[!UICONTROL Conditions]** 區段並定義規則的動作。

   在本節中，您定義您要針對首次客戶套用的折扣型別和折扣值/金額。 此範例為所有符合已定義條件的客戶定義10%的折扣。 如需其他可用選項的詳細資訊，請參閱 [建立購物車價格規則](price-rules-cart-create.md).

   - 的 **[!UICONTROL Apply]**，選取產品價格折扣的百分比。

   - 的 **[!UICONTROL Discount Amount]**，輸入 `10`.

   - 若要將此價格規則僅套用至產品金額，請設定 **[!UICONTROL Apply to Shipping Amount]** 至 `No`.

   - 若要防止系統套用多個價格規則至相同的產品，請設定 **[!UICONTROL Discard Subsequent Rules]** 至 `Yes`.

   - 完成後，按一下 **[!UICONTROL Save]**.

   ![購物車價格規則動作](./assets/actions-first-time.png){width="600" zoomable="yes"}

新規則通常在一小時內即可使用。 測試規則，確保它能如您定義般運作。

## 步驟3：儲存並測試規則

{{new-price-rule}}

1. 規則完成後，按一下 **[!UICONTROL Save Rule]**.

1. 測試規則以確保其正常運作。
