---
title: 將屬性新增至產品
description: 瞭解如何將屬性新增至目錄中的產品。
exl-id: 1f92807a-2362-48a2-8d3a-4aef90a5671f
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 0%

---

# 將屬性新增至產品

雖然屬性主要由 [商店](../stores-purchase/stores-menu.md) 功能表，您也可以新增屬性 _即時進行_ 處理產品時。 您可以從現有屬性清單中選擇，或建立屬性。 新屬性會新增至 [屬性集](../catalog/attribute-sets.md) 產品的基礎。

## 步驟1：新增屬性

1. 在編輯模式中開啟產品。

1. 在右上角，按一下 **[!UICONTROL Add Attribute]**.

   ![具有預設屬性集的新產品](./assets/product-attribute-add.png){width="600" zoomable="yes"}

1. 若要將現有屬性新增至產品，請使用 [篩選控制項](../getting-started/admin-grid-controls.md) 若要在格線中尋找屬性，請執行下列動作：

   - 在要新增的每個屬性的第一欄中選取核取方塊。

   - 按一下 **[!UICONTROL Add Selected]**.

   ![選取屬性](./assets/product-attribute-add-select.png){width="600" zoomable="yes"}

1. 若要定義新屬性，請按一下 **[!UICONTROL Create New Attribute]** 並完成步驟2中的專案。

## 步驟2：說明基本屬性特性

![屬性屬性](./assets/product-attribute-add-new.png){width="600" zoomable="yes"}

1. 在 _[!UICONTROL Attribute Properties]_，輸入&#x200B;**[!UICONTROL Attribute Label]**以識別屬性。

1. 設定 **[!UICONTROL Catalog Input Type for Store Owner]** 至型別 [輸入控制項](attributes-input-types.md) 用於資料輸入。

   如果屬性用於 [可設定的產品](product-create-configurable.md)，選擇 `Dropdown`. 然後，設定 **[!UICONTROL Required]** 至 `Yes`.

1. 的 `Dropdown` 和 `Multiple Select` 輸入型別，請執行下列動作：

   - 在 **[!UICONTROL Values]**，按一下 **[!UICONTROL Add Value]**.

   - 輸入您要在清單中顯示的第一個值。

     您可以為管理員輸入一個值，並為每個商店檢視輸入值的翻譯。 如果您只有一個商店檢視，則只能輸入「管理員」值，且該值也會用於店面。

   - 按一下 **[!UICONTROL Add Value]** 並對要包含在清單中的每個選項重複之前的步驟。

   - 選取 **[!UICONTROL Is Default]** 以使用選項作為預設值。

   ![值](./assets/product-attribute-add-values-colors.png){width="600" zoomable="yes"}

1. 如果您想要求客戶在購買產品之前先選擇選項，請設定 **[!UICONTROL Required]** 至 `Yes`.

## 步驟3：說明進階屬性（選擇性）

![進階屬性特性](./assets/product-attribute-advanced-attribute-properties.png){width="600" zoomable="yes"}

1. 輸入唯一值 **[!UICONTROL Attribute Code]** 小寫字元，不含空格。

1. 設定 **[!UICONTROL Scope]** 以指出可在存放區階層的哪個位置使用屬性。

   如果屬性用於 [可設定的產品](product-create-configurable.md)，選擇 `Global`.

1. 如果此屬性僅適用於此產品，請設定 **[!UICONTROL Unique Value]** 至 `Yes`.

1. 若要針對輸入到文字欄位中的任何資料執行有效性測試，請設定 **[!UICONTROL Input Validation for Store Owner]** 欄位應包含的資料型別。

   此欄位不適用於已選取值的輸入型別。 輸入驗證可用於下列任一專案：

   - `Decimal Number`
   - `Integer Number`
   - `Email`
   - `URL`
   - `Letters`
   - `Letters (a-z, A-Z) or Numbers (0-9)`

   ![輸入驗證](./assets/product-attribute-input-validation.png){width="500"}

1. 如果您想要將屬性加入為Products格線中的欄，請設定 **[!UICONTROL Add to Column Options]** 至 `Yes`.

1. 如果您想要能夠篩選 _[!UICONTROL Products]_依此欄格線，設定&#x200B;**[!UICONTROL Use in Filter Options]**至 `Yes`.

## 步驟4：輸入欄位標籤

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Manage titles]** 區段。

1. 輸入 **[!UICONTROL Title]** 做為欄位標籤。

   如果您的商店提供不同語言版本，您可以為每個檢視輸入翻譯的標題。

   ![管理標題](./assets/product-attribute-add-manage-titles.png){width="600" zoomable="yes"}

## 步驟5：說明店面屬性

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Storefront Properties]** 區段。

   ![店面屬性](./assets/product-attribute-add-storefront-properties.png){width="600" zoomable="yes"}

1. 若要讓屬性可供搜尋，請設定 **[!UICONTROL Use in Search]** 至 `Yes`.

1. 若要在產品比較中包含屬性，請設定 **[!UICONTROL Comparable on Storefront]** 至 `Yes`.

1. 若要在階層式導覽中包含下拉式清單、多選或價格屬性，請設定 **[!UICONTROL Use in Search Results Layered Navigation]** 變更為下列其中一項：

   - `Filterable (with results)`  — 階層導覽僅包含可找到相符產品的篩選器。 任何已套用至清單中所有產品的屬性值不會顯示為可用篩選器。 可用篩選器清單中也會忽略計數為零(0)產品相符的屬性值。<br/><br/>產品篩選清單僅包含符合篩選的產品。 只有在選取的篩選器變更顯示內容時，產品清單才會更新。

   - `Filterable (no results)`  — 階層式導覽包含所有可用屬性值的篩選器及其產品計數，包括零(0)產品相符的產品。 如果屬性值是色票，則該值會顯示為篩選條件，但會被劃掉。

1. 若要在搜尋結果頁面上用於分層導覽，請設定 **[!UICONTROL Use in Search Results Navigation]** 至 `Yes` 並在 **[!UICONTROL Position]** 欄位。

   位置編號表示屬性在分層導覽區塊中的相對位置。

1. 若要在價格規則中使用屬性，請設定 **[!UICONTROL Use for Promo Rule Conditions]** 至 `Yes`.

1. 若要允許文字使用HTML格式化，請設定 **[!UICONTROL Allow HTML Tags on Storefront]** 至 `Yes`.

   此設定可讓WYSIWYG編輯器在編輯欄位時使用。

1. 若要在產品頁面上包含屬性，請設定 **[!UICONTROL Visible on Catalog Pages on Storefront]** 至 `Yes`.

1. 完成主題支援的下列設定：

   - 若要在產品清單中包含屬性，請設定 **[!UICONTROL Used in Product Listing]** 至 `Yes`.

   - 若要使用屬性作為產品清單的排序引數，請設定 **[!UICONTROL Used for Sorting in Product Listing]** 至 `Yes`.

1. 完成後，按一下 **[!UICONTROL Save Attribute]**.
