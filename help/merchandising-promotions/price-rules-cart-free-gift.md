---
title: 免費贈品促銷活動
description: 瞭解如何使用購物車價格規則設定免費贈品促銷活動，以便在符合一組條件時提供免費贈品。
feature: Merchandising, Price Rules, Shopping Cart, Shipping/Delivery
TQID: https://experienceleague.adobe.com/FR-q4Qj-ZDDzmfEKSvSj-BlwsM7ro-BqAE1yCppTaXE
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 3cddc90c619a27b1404e0be7bb4b2c9a3b77e443
workflow-type: tm+mt
source-wordcount: 349
ht-degree: 0%

---


# 免費贈品促銷活動

*免費贈品*&#x200B;促銷活動可讓您設定[購物車價格規則](price-rules-cart.md)，在特定條件下將免費專案新增至購物車。

>[!NOTE]
>
>Luma店面不支援此功能。 可透過[GraphQL](https://developer.adobe.com/commerce/webapi/graphql/schema/cart/mutations/select-free-gift/)存取，並可在Edge Delivery Services (EDS)店面取得。

## 建立免費贈品促銷活動

本節說明如何使用下列格式來建立免費贈品促銷活動：

**購買X產品，免費取得Y產品**

1. [建立購物車價格規則](price-rules-cart.md#step-1-add-a-rule)並免費贈品促銷活動。

1. [描述購物車指示的條件](price-rules-cart.md#step-2-describe-the-conditions)，以定義價格規則的條件。 這是可新增至規則的多個條件中的第一個，並決定何時觸發規則。 此維度可能以下列專案組合為基礎：

   - 產品屬性
   - 產品
   - 購物車屬性
   - Adobe Commerce客戶區段

   如果保留為空白，系統會為每個購物車觸發規則。

   ![購物車價格規則 — 條件](./assets/conditions.png){width="600" zoomable="yes"}

1. 定義購物車價格規則的動作：

   1. 展開 (../assets/icon-display-expand.png) **[!UICONTROL Actions]**&#x200B;區段並輸入下列資訊：

   - 將&#x200B;**[!UICONTROL Apply]**&#x200B;設為`Free Gift`。
   - 在&#x200B;**[!UICONTROL Gift SKU(s)]**&#x200B;中，選取一或多個客戶可選擇作為免費贈品的SKU。
   - 將&#x200B;**[!UICONTROL Free Gift Discount Type]**&#x200B;設為&#x200B;**[!UICONTROL Price Based]**&#x200B;或&#x200B;**[!UICONTROL Discount Based]**。
   - 在&#x200B;**[!UICONTROL Gift Qty]**&#x200B;中，輸入客戶收到的免費贈品數量。 例如，如果您希望客戶收到兩個免費專案，請輸入`2`。
   - 若要防止套用其他折扣，請將&#x200B;**[!UICONTROL Discard subsequent rules]**&#x200B;設為`Yes`。

   1. 按一下「**[!UICONTROL Save and Continue Edit]**」並視需要完成規則的其餘部分。

1. [完成購物車價格規則指示的標籤](price-rules-cart.md)，以輸入結帳時顯示的標籤。

![購物車價格規則 — 免費贈品標籤](./assets/free-gift-promotion-label.png){width="600" zoomable="yes"}

{{new-price-rule}}

1. 當您的規則完成時，按一下&#x200B;**[!UICONTROL Save Rule]**。

## 變數

您可以透過多種不同方式自訂購物車價格規則。 免費贈品功能可設定為兩種不同的折扣型別：

- **以價格為基礎** ：以`0`的價格新增禮品專案。
- **以折扣為基礎** ：全額折扣套用至禮品專案。
