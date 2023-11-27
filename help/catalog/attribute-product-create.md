---
title: 建立及刪除產品屬性
description: 瞭解如何建立和移除產品屬性，這些屬性用於描述目錄中產品的特定特性。
exl-id: fd0e5d5b-a917-4e55-8ec2-7ebb040d3d06
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1159'
ht-degree: 0%

---

# 建立及刪除產品屬性

您可以在處理產品時建立屬性，或從 _[!UICONTROL Product Attributes]_頁面。 下列步驟說明如何從建立屬性_[!UICONTROL Stores]_ 功能表。

## 步驟1：說明基本屬性特性

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. 按一下 **[!UICONTROL Add New Attribute]**.

   ![新增屬性屬性](./assets/attribute-properties.png){width="600" zoomable="yes"}

1. 的 **[!UICONTROL Default Label]**，輸入可識別屬性的標籤。

1. 若要判斷用於資料輸入的輸入控制項型別，請設定 **[!UICONTROL Catalog Input Type for Store Owner]** 變更為下列其中一項：

   | 屬性 | 說明 |
   |--- |--- |
   | `Text Field` | 單行文字輸入欄位。 |
   | `Text Area` | 用於輸入文欄位落（如產品說明）的多行輸入欄位。 您可以使用WYSIWYG編輯器將文字格式化為HTML標籤，或直接在文字中輸入標籤。 |
   | `Text Editor` | 屬性位置的完整文字編輯器。 |
   | 日期 | 在中顯示日期值 [偏好的格式](attributes-input-types.md#date-and-time-options) 和 [時區](../getting-started/store-details.md#locale-options). 日期值可從清單或行事曆中選取( ![行事曆圖示](../assets/icon-calendar.png) )。 <br/><br/>**_注意：_**根據您的系統組態，_管理員&#x200B;_使用者可以直接在欄位中輸入日期，或從行事曆或清單中選取日期。 如需有關指定日期和時間值的資訊，請參閱 [日期和時間選項](attributes-input-types.md#date-and-time-options). |
   | `Yes/No` | 顯示含有預先定義選項的下拉式清單： `Yes` 和 `No`. |
   | `Dropdown` | 顯示只接受單一選取專案的下拉式值清單。 下拉式清單輸入型別是的關鍵元件 [可設定的產品](product-create-configurable.md). |
   | `Multiple Select` | 顯示接受多個選取專案的下拉式值清單。 |
   | `Price` | 此輸入型態可用來建立預先定義屬性以外的價格欄位：「價格」、「特殊價格」、「層級價格」及「成本」。 使用的貨幣由您的系統組態決定。 |
   | `Media Image` | 將額外的影像與產品建立關聯，例如產品標誌、護理指示或食品標籤的成分。 將媒體影像屬性新增至產品的屬性集時，該屬性會變成額外的影像型別，連同基底、小型和縮圖。 媒體影像屬性可以從 [店面媒體瀏覽器](catalog-images-video.md#storefront-media-browser). |
   | `Fixed Product Tax` | 可讓您定義 [FPT率](../stores-purchase/fixed-product-tax.md) 根據您的地區設定需求。 |
   | `Visual Swatch` | 顯示描述可設定產品顏色、紋理或圖樣的色票。 A [視覺色票](swatches.md) 可以用十六進位顏色值填色，或顯示代表選項顏色、材質、紋理或圖樣的上傳影像。 |
   | `Text Swatch` | 經常用於尺寸的可設定產品選項的文字表示。 [文字色票](swatches.md#text-based-swatches) 也可以包含十六進位色彩值。 |
   | `Page Builder` | 功能齊全的 [頁面產生器](../page-builder/introduction.md) 工作區位於屬性位置，可讓您輕鬆將吸引人的內容新增至產品頁面。 |

   {style="table-layout:auto"}

1. 如果您想在客戶購買產品之前要求選擇選項，請設定 **[!UICONTROL Values Required]** 至 `Yes`.

1. 的 [!UICONTROL Dropdown] 和 [!UICONTROL Multiple Select] 輸入型別，請執行下列動作：

   - 在 _[!UICONTROL Manage Options]_，按一下&#x200B;**[!UICONTROL Add Option]**.

   - 輸入您要在清單中顯示的第一個值。

     您可以為管理員輸入一個值，並為每個商店檢視輸入值的翻譯。 如果您只有一個商店檢視，則只能輸入管理員值，且該值也會用於店面。

   - 按一下 **[!UICONTROL Add Option]** 並對要包含在清單中的每個選項重複之前的步驟。

   - 選取 **[!UICONTROL Is Default]** 以使用選項作為預設值。

   ![產品屬性 — 管理選項](./assets/product-attribute-add-values-colors.png){width="600" zoomable="yes"}

## 步驟2：視需要說明進階屬性

1. 輸入唯一值 **[!UICONTROL Attribute Code]** 小寫字元，不含空格。

   ![產品屬性 — 進階屬性](./assets/product-attribute-advanced-attribute-properties.png){width="600" zoomable="yes"}

   可用的選項取決於 _[!UICONTROL Catalog Input Type for Store Owner]_設定。

1. 設定 **[!UICONTROL Scope]** 以指示在您的 [存放區階層](../getting-started/websites-stores-views.md) 屬性才能使用。

1. 如果您要防止任何重複值輸入，請設定 **[!UICONTROL Unique Value]** 至 `Yes`.

1. 對於輸入值的輸入型別，透過設定對輸入到文字欄位中的任何資料執行有效性測試 **[!UICONTROL Input Validation for Store Owner]** 欄位應包含的資料型別。

   此欄位不適用於已選取值的輸入型別。 此測試可驗證下列任一專案：

   - `Decimal Number`
   - `Integer Number`
   - `Email`
   - `URL`
   - `Letters`
   - `Letters (a-z, A-Z) or Numbers (0-9)`

   ![輸入驗證](./assets/product-attribute-input-validation.png){width="400"}

1. 若要將此屬性新增至 [產品清單](products-list.md)，將下列選項設為 `Yes`.

   - **新增至欄選項**  — 將屬性作為欄包含在 _[!UICONTROL Products]_清單。
   - **在篩選選項中使用**  — 將篩選控制項新增至中的欄標題 _[!UICONTROL Products]_清單。

## 步驟3：輸入欄位標籤

1. 在左側導覽列中，選擇 **[!UICONTROL Manage Labels]**.

1. 輸入 **[!UICONTROL Title]** 做為欄位標籤。

   如果您的商店提供不同語言版本，您可以為每個檢視輸入翻譯的標題。

   ![產品屬性 — 管理標題](./assets/product-attribute-add-manage-titles.png){width="600" zoomable="yes"}

## 步驟4：說明店面屬性

1. 在左側導覽列中，選擇 **[!UICONTROL Storefront Properties]**.

   ![產品屬性 — 店面屬性](./assets/product-attribute-add-storefront-properties.png){width="600" zoomable="yes"}

   可用的選項取決於 _[!UICONTROL Catalog Input Type for Store Owner]_設定。

1. 如果要搜尋屬性，請設定 **[!UICONTROL Use in Search]** 至 `Yes`.

   - 設定 **[!UICONTROL Search Weight]** 控制專案在搜尋結果中出現的位置的值： 1 （最低重量）到10 （最高重量）。

   - 設定 **[!UICONTROL Visible in Advanced Search]** 視需要。 進一步瞭解 [進階搜尋](search.md#advanced-search).

1. 若要在產品比較中包含屬性，請設定 **[!UICONTROL Comparable on Storefront]** 至 `Yes`.

1. 針對下拉式清單、多重選取及價格欄位，執行下列作業：

   - 若要在分層導覽中使用屬性作為篩選器，請設定 **[!UICONTROL Use in Layered Navigation]** 至 `Yes`.

   - 若要在搜尋結果頁面的階層式導覽中使用屬性，請設定 **[!UICONTROL Use in Search Results Layered Navigation]** 至 `Yes`.

   - 的 **[!UICONTROL Position]**，請輸入數字，以指出屬性在階層式導覽區塊中的相對位置。

1. 若要在價格規則中使用屬性，請設定 **[!UICONTROL Use for Promo Rule Conditions]** 至 `Yes`.

1. 若要允許文字使用HTML格式化，請設定 **[!UICONTROL Allow HTML Tags on Frontend]** 至 `Yes`.

   此設定使得WYSIWYG編輯器可用於欄位。

1. 若要在產品頁面上包含屬性，請設定 **[!UICONTROL Visible on Catalog Pages on Storefront]** 至 `Yes`.

1. 如果您的主題支援，請完成下列設定：

   - 若要在產品清單中包含屬性，請設定 **[!UICONTROL Used in Product Listing]** 至 `Yes`.

   - 若要使用屬性作為產品清單的排序引數，請設定 **[!UICONTROL Used for Sorting in Product Listing]** 至 `Yes`.

1. 完成後，按一下 **[!UICONTROL Save Attribute]**.

## 步驟5：將建立的屬性指派給屬性集

若要讓屬性顯示在產品建立頁面上，請將其新增至特定屬性集。

1. 完成先前步驟後，請前往 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

1. 在清單中選取您需要的屬性集，然後在編輯模式中開啟它。

1. 將建立的屬性從 **[!UICONTROL Unassigned Attributes]** 清單至中的適當資料夾 **群組** 欄。

1. 完成後，按一下 **[!UICONTROL Save]**.

## 可設定產品的屬性

任何用作選項下拉式清單的屬性 [可設定的產品](product-create-configurable.md) 必須具有以下屬性：

| 屬性 | 值 |
|----------|------ |
| 存放區所有者的目錄輸入型別 | 下拉式清單 |
| 範圍 | 全域 |

{style="table-layout:auto"}

## 刪除屬性

刪除屬性時，該屬性會從任何相關的產品和屬性集中移除。 系統屬性是存放區核心功能的一部分，無法刪除。

在刪除屬性之前，請確定您目錄中的任何產品目前都沒有使用屬性。 若要判斷屬性是否正在使用中，一個簡單的方法就是使用 [匯出](../systems/data-export.md) 用於檢查產品實體屬性清單的工具。 如果屬性未包含在清單中，則目錄中的任何產品都不會使用它。

**_若要刪除屬性，請執行下列動作：_**

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. 在清單中尋找屬性，並在編輯模式中開啟。

1. 按一下 **[!UICONTROL Delete Attribute]**.

   ![刪除屬性](./assets/attribute-delete.png){width="600" zoomable="yes"}

1. 提示確認時，按一下 **[!UICONTROL OK]**.
