---
title: 具有多個SKU的目錄價格規則
description: 瞭解如何將單一目錄價格規則套用至多個SKU。
exl-id: 99023460-0501-45cd-8990-5f2b9ed7b4a2
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---

# 具有多個SKU的目錄價格規則

單一目錄價格規則可套用至多個SKU，因此可以根據產品、品牌或類別建立各種促銷活動。 建立此規則時，您想要設定符合所選SKU的條件。 建立規則時，您可以輕鬆地瀏覽並從格線選取SKU。

## 步驟1. 驗證產品屬性的店面屬性

開始之前，請確定`sku`屬性的[Storefront屬性](../catalog/attribute-product-create.md#step-4-describe-the-storefront-properties)設定為`Use in Promo Rules`。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**。

1. 在&#x200B;_[!UICONTROL Attribute Code]_欄頂端的搜尋篩選中，輸入`sku`並按一下&#x200B;**[!UICONTROL Search]**。

1. 按一下以編輯模式開啟`sku`屬性。

1. 在左側面板中，按一下&#x200B;**[!UICONTROL Storefront Properties]**&#x200B;並確定&#x200B;**[!UICONTROL Use for Promo Rule Conditions]**&#x200B;已設為`Yes`。

1. 如果您變更了屬性的值，請按一下&#x200B;**[!UICONTROL Save Attribute]**。

## 步驟2. 將價格規則套用至多個SKU

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Catalog Price Rules]**。

1. 執行下列任一項作業：

   - 依照指示建立[目錄價格規則](price-rules-catalog.md)。
   - 開啟現有的型錄價格規則。

1. 展開![展開選擇器](../assets/icon-display-expand.png) **[!UICONTROL Conditions]**&#x200B;區段，然後執行下列動作：

   - 在第一行中，將第一個引數設為`ANY`。

     ![目錄價格規則條件 — ANY](./assets/multiple-skus-condition1.png){width="600" zoomable="yes"}

   - 在下一行的開頭按一下&#x200B;_新增_ （![新增圖示](../assets/icon-add-green-circle.png)），然後在&#x200B;**[!UICONTROL Product Attribute]**&#x200B;下的清單中按一下`SKU`。

     ![目錄價格規則條件 — SKU是](./assets/multiple-skus-condition1a.png){width="600" zoomable="yes"}其中之一

   - 您可以透過選項進行比較。 若您想從SKU清單中找出至少一個，`select is one of`。 如果您要尋找所有必須找到以套用的SKU群組，請選取`is`。 我們建議選取`is one of`。

     ![目錄價格規則條件 — SKU是](./assets/multiple-skus-condition1b.png){width="600" zoomable="yes"}其中之一

   - 若要完成條件，請按一下更多(**...**)連結，然後按一下可用產品清單的&#x200B;_選擇器_ （![清單圖示](../assets/icon-list-chooser.png)）圖示。

     ![目錄價格規則條件 — 多個SKU](./assets/multiple-skus-condition2b.png){width="600" zoomable="yes"}

   - 瀏覽、篩選或搜尋以尋找您要新增的SKU。 在清單中，選取每個要納入之產品的核取方塊。

   - 按一下&#x200B;**[!UICONTROL Save and Apply]**&#x200B;將SKU新增至條件。

     ![目錄價格規則條件 — 多個SKU](./assets/multiple-skus-condition2.png){width="600" zoomable="yes"}

1. 完成規則，包括符合條件時要採取的任何[動作](price-rules-catalog.md)。

1. 當您的規則完成時，按一下&#x200B;**[!UICONTROL Save]**。

{{new-price-rule}}
