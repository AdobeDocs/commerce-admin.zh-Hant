---
title: 購物車價格規則範例 — 最低購買折扣
description: 檢閱使用購物車價格規則提供最低購買折扣的範例。
exl-id: dc06cd12-d23b-4836-9ad2-93ca60dac927
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---

# 購物車價格規則範例 — 最低購買折扣

購物車價格規則可用於根據最低購買提供百分比折扣。 在下列範例中，25%的折扣適用於特定類別中超過$200.00的所有購買。 折扣格式如下：

所有Y （類別）有X%折扣超過$Z美元

## 步驟1. 建立購物車規則

遵循基本的 [指示](price-rules-cart.md) 建立購物車規則。

## 步驟2. 定義條件

1. 向下捲動並展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Conditions]** 區段。

1. 按一下 _新增_ (![「新增」圖示](../assets/icon-add-green-circle.png))並選擇 **[!UICONTROL Product Attribute Combination]**.

   ![購物車價格規則條件 — 產品屬性組合](./assets/condition1.png){width="500" zoomable="yes"}

1. 按一下 _新增_ (![「新增」圖示](../assets/icon-add-green-circle.png))在下一行的開頭並在下的清單中 **[!UICONTROL Product Attribute]**，選擇 **[!UICONTROL Category]**.

   - 按一下(**...**) _更多_ 連結以顯示其他選項。

     ![購物車價格規則條件 — 類別選項](./assets/condition3.png){width="600" zoomable="yes"}

   - 按一下 _選擇器_ (![清單圖示](../assets/icon-list-chooser.png))圖示以檢視可用的類別。 在類別樹狀結構中，選取每個要包含的類別的核取方塊。 按一下核取圖示以接受類別選擇。

     ![購物車價格規則條件 — 類別](./assets/condition4.png){width="600" zoomable="yes"}

1. 按一下 _新增_ (![「新增」圖示](../assets/icon-add-green-circle.png))，並執行下列動作：

   - 在「 」下的清單中 **[!UICONTROL Cart Item Attribute]**，選擇 **[!UICONTROL Price in cart]**.

     ![購物車價格規則條件 — 購物車專案屬性](./assets/condition5.png){width="500"}

   - 按一下 **是** 並選擇 `equals or greater than`.

   - 按一下 **...** 並輸入購物車中的價格必須符合此條件的金額。 例如，輸入 `30`.

     ![購物車價格規則條件 — 購物車中的價格](./assets/condition6.png){width="500"}

1. 按一下 **[!UICONTROL Save and Continue Edit]**.

## 步驟3. 定義動作

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Actions]** 並執行下列動作：

   ![購物車價格規則動作](./assets/minimum-discount-actions.png){width="600" zoomable="yes"}

   - 設定 **[!UICONTROL Apply]** 至 `Percent of product price discount`.

   - 輸入 **[!UICONTROL Discount Amount]**. 例如，輸入 `10` 10%的折扣。

   - 若要避免將其他促銷活動套用至購買，請設定 **[!UICONTROL Discard subsequent rules]** 至 `Yes`.

1. 按一下 **[!UICONTROL Save and Continue Edit]** 並視需要完成規則。

## 步驟4. 完成標籤

完成 [步驟4](price-rules-cart.md) ，以輸入結帳期間出現的任何標籤。

## 步驟5：儲存並測試規則

{{new-price-rule}}

1. 規則完成後，按一下 **[!UICONTROL Save Rule]**.

1. 測試規則以確保其正常運作。
