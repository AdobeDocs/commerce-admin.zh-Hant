---
title: 價格規則中的客戶區段
description: 瞭解如何將客戶區段與購物車價格規則建立關聯，以便您能夠為商店定義目標促銷活動。
exl-id: eaa04e7a-c0f9-4f09-8e65-75965ccbdc69
feature: Customers, Configuration, Price Rules
TQID: https://experienceleague.adobe.com/MSMNikJwG2lQuLlQxnK82zjCOeF-u8JEjmabKFJgpZU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 232
ht-degree: 0%

---

# 價格規則中的客戶區段

{{ee-feature}}

將客戶區段與[購物車價格規則](../merchandising-promotions/price-rules-cart.md)建立關聯，便可用於目標促銷活動。

![購物車價格規則 — 目標客戶區段](assets/price-rule-cart-condition-segments.png){width="700" zoomable="yes"}

_&#x200B;**若要將區段與購物車價格規則建立關聯：**&#x200B;_

1. 在&#x200B;_管理員_&#x200B;側邊欄上，前往&#x200B;**[!UICONTROL Marketing]** > _促銷活動_ > **[!UICONTROL Cart Price Rules]**。

1. 開啟新的或現有的規則：

   * 若要使用新規則，請按一下右上角的&#x200B;**[!UICONTROL Add New Rule]**。
   * 若要使用現有規則，請按一下清單中的規則，以編輯模式開啟該規則。

1. 向下捲動並展開&#x200B;**[!UICONTROL Conditions]**&#x200B;區段。

1. 新增條件。

   * 按一下&#x200B;_新增_ （![清單圖示](../assets/icon-add-green-circle.png)）圖示，其中會顯示條件清單。 然後選擇&#x200B;**[!UICONTROL Customer Segment]**。

   ![購物車價格規則 — 新增客戶區段條件](assets/condition-customer-segment.png){width="600" zoomable="yes"}

   依預設，條件設定為尋找符合條件。 如有需要，請按一下&#x200B;**[!UICONTROL matches]**&#x200B;連結，並將運運算元變更為下列其中一項：

   * `does not match`
   * `is one of`
   * `is not one of`

   ![條件運運算元](assets/price-rule-condition-customer-segment-operator.png){width="600" zoomable="yes"}

1. 若要鎖定特定區段，請按一下[更多&#x200B;**...**]連結以顯示其他選項。 然後，按一下&#x200B;_選擇器_ （![清單圖示](../assets/icon-list-chooser.png)）圖示以顯示客戶區段清單。

1. 在清單中，選取您要以條件定位之每個區段的核取方塊。

   ![購物車價格規則 — 條件選擇器清單](assets/condition-segment-chooser-list.png){width="600" zoomable="yes"}

1. 按一下「**[!UICONTROL Select]**」將選取的客戶區段放入條件中。

1. 視需要完成其餘的價格規則。

1. 完成時，按一下&#x200B;**[!UICONTROL Save]**。
