---
title: 將屬性新增至產品
description: 瞭解如何將屬性新增至目錄中的產品。
exl-id: 1f92807a-2362-48a2-8d3a-4aef90a5671f
feature: Catalog Management, Products
source-git-commit: 99049260b4ff490845affd1c98fa4d2536edebd7
workflow-type: tm+mt
source-wordcount: '790'
ht-degree: 0%

---

# 將屬性新增至產品

雖然屬性主要是從[商店](../stores-purchase/stores-menu.md)功能表管理，但您也可以在使用產品時立即新增屬性&#x200B;__。 您可以從現有屬性清單中選擇，或建立屬性。 新屬性已新增至產品所依據的[屬性集](../catalog/attribute-sets.md)。

## 步驟1：新增屬性

1. 在編輯模式中開啟產品。

1. 按一下右上角的&#x200B;**[!UICONTROL Add Attribute]**。

   ![預設屬性集的新產品](./assets/product-attribute-add.png){width="600" zoomable="yes"}

1. 若要將現有屬性加入產品中，請使用[篩選控制項](../getting-started/admin-grid-controls.md)在格線中尋找屬性，並執行下列動作：

   - 在要新增的每個屬性的第一欄中選取核取方塊。

   - 按一下&#x200B;**[!UICONTROL Add Selected]**。

   ![選取屬性](./assets/product-attribute-add-select.png){width="600" zoomable="yes"}

1. 若要定義新屬性，請按一下&#x200B;**[!UICONTROL Create New Attribute]**&#x200B;並完成步驟2中的專案。

## 步驟2：說明基本屬性特性

![屬性屬性](./assets/product-attribute-add-new.png){width="600" zoomable="yes"}

1. 在&#x200B;_[!UICONTROL Attribute Properties]_&#x200B;底下，輸入&#x200B;**[!UICONTROL Attribute Label]**&#x200B;以識別屬性。

1. 將&#x200B;**[!UICONTROL Catalog Input Type for Store Owner]**&#x200B;設定為要用於資料輸入的[輸入控制項](attributes-input-types.md)的型別。

   如果屬性用於[可設定的產品](product-create-configurable.md)，請選擇`Dropdown`。 然後，將&#x200B;**[!UICONTROL Required]**&#x200B;設定為`Yes`。

1. 針對`Dropdown`和`Multiple Select`輸入型別，請執行下列動作：

   - 在&#x200B;**[!UICONTROL Values]**&#x200B;底下，按一下&#x200B;**[!UICONTROL Add Value]**。

   - 輸入您要在清單中顯示的第一個值。

     您可以為管理員輸入一個值，並為每個商店檢視輸入值的翻譯。 如果您只有一個商店檢視，則只能輸入「管理員」值，且該值也會用於店面。

   - 按一下「**[!UICONTROL Add Value]**」，然後針對您想要加入清單的每個選項重複上一步驟。

   - 選取&#x200B;**[!UICONTROL Is Default]**&#x200B;以使用選項作為預設值。

   ![值](./assets/product-attribute-add-values-colors.png){width="600" zoomable="yes"}

1. 如果您想要要求客戶在購買產品之前選擇選項，請將&#x200B;**[!UICONTROL Required]**&#x200B;設為`Yes`。

## 步驟3：說明進階屬性（選擇性）

![進階屬性屬性](./assets/product-attribute-advanced-attribute-properties.png){width="600" zoomable="yes"}

1. 以小寫字元輸入唯一的&#x200B;**[!UICONTROL Attribute Code]**，不含空格。

1. 設定&#x200B;**[!UICONTROL Scope]**&#x200B;以指示可在存放區階層中使用屬性的位置。

   如果屬性用於[可設定的產品](product-create-configurable.md)，請選擇`Global`。

1. 如果此屬性只適用於此產品，請將&#x200B;**[!UICONTROL Unique Value]**&#x200B;設定為`Yes`。

1. 若要針對輸入文字欄位的任何資料執行有效性測試，請將&#x200B;**[!UICONTROL Input Validation for Store Owner]**&#x200B;設定為欄位應包含的資料型別。

   此欄位不適用於已選取值的輸入型別。 輸入驗證可用於下列任一專案：

   - `Decimal Number`
   - `Integer Number`
   - `Email`
   - `URL`
   - `Letters`
   - `Letters (a-z, A-Z) or Numbers (0-9)`

   ![輸入驗證](./assets/product-attribute-input-validation.png){width="500"}

1. 如果您想要將屬性加入為Products格線中的資料行，請將&#x200B;**[!UICONTROL Add to Column Options]**&#x200B;設為`Yes`。

1. 如果您想要能夠依此資料行篩選&#x200B;_[!UICONTROL Products]_&#x200B;網格，請將&#x200B;**[!UICONTROL Use in Filter Options]**&#x200B;設為`Yes`。

## 步驟4：輸入欄位標籤

1. 展開&#x200B;**[!UICONTROL Manage titles]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

1. 輸入要做為欄位標籤的&#x200B;**[!UICONTROL Title]**。

   如果您的商店提供不同語言版本，您可以為每個檢視輸入翻譯的標題。

   ![管理標題](./assets/product-attribute-add-manage-titles.png){width="600" zoomable="yes"}

## 步驟5：說明店面屬性

1. 展開&#x200B;**[!UICONTROL Storefront Properties]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![店面屬性](./assets/product-attribute-add-storefront-properties.png){width="600" zoomable="yes"}

1. 若要讓屬性可供搜尋，請將&#x200B;**[!UICONTROL Use in Search]**&#x200B;設為`Yes`。

1. 若要在產品比較中包含屬性，請將&#x200B;**[!UICONTROL Comparable on Storefront]**&#x200B;設為`Yes`。

1. 若要在階層式導覽中包含下拉式清單、多選或價格屬性，請將&#x200B;**[!UICONTROL Use in Search Results Layered Navigation]**&#x200B;設定為下列其中一項：

   - `Filterable (with results)` — 階層式導覽僅包含可找到相符產品的篩選器。 任何已套用至清單中所有產品的屬性值不會顯示為可用篩選器。 可用篩選器清單中也會忽略計數為零(0)產品相符的屬性值。<br/><br/>篩選的產品清單只包含符合篩選的產品。 只有在選取的篩選器變更顯示內容時，產品清單才會更新。

   - `Filterable (no results)` — 階層式導覽包含所有可用屬性值的篩選器及其產品計數，包括零(0)產品相符的產品。 如果屬性值是色票，則該值會顯示為篩選條件，但會被劃掉。

   >[!NOTE]
   >
   >當&#x200B;_[!UICONTROL Use in Search]_&#x200B;設定設為`No`時，不會顯示&#x200B;_[!UICONTROL Use in Search Results Layered Navigation]_&#x200B;設定，且產品屬性不會用於具有任何[!UICONTROL Use in Layered Navigation]設定值的搜尋。

1. 若要在搜尋結果頁面的階層式導覽中使用屬性，請將&#x200B;**[!UICONTROL Use in Search Results Layered Navigation]**&#x200B;設為`Yes`，並在&#x200B;**[!UICONTROL Position]**&#x200B;欄位中輸入數字。

   位置編號表示屬性在分層導覽區塊中的相對位置。

   >[!NOTE]
   >
   >_[!UICONTROL Position]_&#x200B;欄位預設為灰色，您必須先儲存屬性，才能修改此設定。

1. 若要在價格規則中使用屬性，請將&#x200B;**[!UICONTROL Use for Promo Rule Conditions]**&#x200B;設為`Yes`。

1. 若要允許文字使用HTML格式化，請將&#x200B;**[!UICONTROL Allow HTML Tags on Storefront]**&#x200B;設為`Yes`。

   此設定可讓WYSIWYG編輯器在編輯欄位時使用。

1. 若要在產品頁面上包含屬性，請將&#x200B;**[!UICONTROL Visible on Catalog Pages on Storefront]**&#x200B;設為`Yes`。

1. 完成主題支援的下列設定：

   - 若要在產品清單中包含屬性，請將&#x200B;**[!UICONTROL Used in Product Listing]**&#x200B;設為`Yes`。

   - 若要使用屬性作為產品清單的排序引數，請將&#x200B;**[!UICONTROL Used for Sorting in Product Listing]**&#x200B;設為`Yes`。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Attribute]**。
