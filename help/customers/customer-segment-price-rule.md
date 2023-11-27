---
title: 價格規則中的客戶區段
description: 瞭解如何將客戶區段與購物車價格規則建立關聯，以便您能夠為商店定義目標促銷活動。
exl-id: eaa04e7a-c0f9-4f09-8e65-75965ccbdc69
feature: Customers, Configuration, Price Rules
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---

# 價格規則中的客戶區段

{{ee-feature}}

客戶區段可與建立關聯，以用於目標促銷活動。 [購物車價格規則](../merchandising-promotions/price-rules-cart.md).

![購物車價格規則 — 目標客戶區段](assets/price-rule-cart-condition-segments.png){width="700" zoomable="yes"}

_**若要將區段與購物車價格規則產生關聯，請執行下列步驟：**_

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Marketing]** > _促銷活動_ > **[!UICONTROL Cart Price Rules]**.

1. 開啟新的或現有的規則：

   * 若要使用新規則，請按一下 **[!UICONTROL Add New Rule]** 位於右上角。
   * 若要使用現有規則，請按一下清單中的規則，以編輯模式開啟該規則。

1. 向下捲動並展開 **[!UICONTROL Conditions]** 區段。

1. 新增條件。

   * 按一下 _新增_ (![清單圖示](../assets/icon-add-green-circle.png))圖示，其中顯示條件清單。 然後，選擇 **[!UICONTROL Customer Segment]**.

   ![購物車價格規則 — 新增客戶區段條件](assets/condition-customer-segment.png){width="600" zoomable="yes"}

   依預設，條件設定為尋找符合條件。 如有需要，請按一下 **[!UICONTROL matches]** 連結運運算元，並將其變更為下列其中一項：

   * `does not match`
   * `is one of`
   * `is not one of`

   ![條件運運算元](assets/price-rule-condition-customer-segment-operator.png){width="600" zoomable="yes"}

1. 若要鎖定特定區段，請按一下 **...** 連結以顯示其他選項。 然後，按一下 _選擇器_ (![清單圖示](../assets/icon-list-chooser.png))圖示來顯示客戶區段清單。

1. 在清單中，選取您要以條件定位之每個區段的核取方塊。

   ![購物車價格規則 — 條件選擇器清單](assets/condition-segment-chooser-list.png){width="600" zoomable="yes"}

1. 按一下 **[!UICONTROL Select]** 將所選客戶區段放置到條件中。

1. 視需要完成其餘的價格規則。

1. 完成後，按一下 **[!UICONTROL Save]**.
