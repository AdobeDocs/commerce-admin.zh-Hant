---
title: 產品設定 —  [!UICONTROL Customizable Options]
description: 對於產品， [!UICONTROL Customizable Options] 設定可讓您提供包含文字、選取範圍及日期輸入型別的選項選擇。
exl-id: 7d23c5c5-2b2a-4f2a-b843-9c27b851be5f
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '811'
ht-degree: 0%

---

# 產品設定 —  [!UICONTROL Customizable Options]

將可自訂選項新增至產品是提供包含文字、選擇和日期輸入型別之選項選項的簡單方法。 如果您的清查需求很簡單，可自訂選項就是很好的解決方案。 但是，因為它們是根據單一SKU的變化，所以無法用於管理庫存或作為價格規則條件的基礎。 如果您有多個具有相同選項的產品，您可以設定一個產品並將選項匯入至其他產品。

當客戶購買具有可自訂選項的產品時，每個所選選項的說明會出現在產品說明下方，而任何相關的加價（或Markdown）會自動套用至料號的價格。

![可自訂選項的產品詳細資料](./assets/storefront-customizable-option-product-detail.png){width="700" zoomable="yes"}

如果購物車價格規則是由購買所觸發，則初始計算會先套用至產品價格，然後套用至明細行料號價格，再套用適用可自訂選項的任何調整。 在下列範例中，客戶以$74.00購買一個公事包，加上一個可自訂的字母組合選項。 基礎產品價格會套用$14.80的加價，而調整後的價格會顯示為$88.80。在此情況下，購買餃子包會根據產品SKU觸發購物車價格規則，並對購買套用折扣，加上免運費。 雖然可自訂選項不會觸發購物車價格規則，但會將折扣套用至購物車內容，包括可自訂選項的加價。

![包含可自訂選項與價格規則的購物車](./assets/storefront-customizable-option-cart-price-rule.png){width="700" zoomable="yes"}

>[!NOTE]
>
>型錄價格規則折扣不會套用至固定價格可自訂選項。

## 建立可自訂的選項

1. 在編輯模式中開啟產品。

1. 向下捲動並展開 ![展開選擇器](../assets/icon-display-expand.png) 此 _[!UICONTROL Customizable Options]_區段。

1. 按一下 **[!UICONTROL Add Option]**.

   ![可自訂的選項](./assets/product-customizable-options.png){width="600" zoomable="yes"}

1. 完成新的選項設定：

   - 的 **[!UICONTROL Option Title]**，輸入選項的名稱。

   - 設定 **[!UICONTROL Option Type]** 以取得資料專案型別。

   - 如果購買產品不需要選項，請取消選取 **[!UICONTROL Required]** 核取方塊。

1. 根據資料輸入型別完成欄位：

   - 的 **[!UICONTROL Title]**，輸入此選項的名稱。

   - （選用） For **[!UICONTROL Price]**，請輸入適用此選項之基本產品價格的任何加價或減價。

   - 設定 **[!UICONTROL Price Type]** 變更為下列其中一項：

      - `Fixed`  — 變數的價格與基本產品的價格不同，有固定的金額，例如$1。
      - `Percentage`  — 變化價格與基本產品的價格有百分比差異，例如10%。

   - （選擇性）輸入 **[!UICONTROL SKU]** （適用於選項）。 選項SKU是新增至產品SKU的字尾。

   - 如果 _[!UICONTROL Option Type]_是 `File`，設定檔案的引數。 的&#x200B;**[!UICONTROL Compatible File Extensions]**，請輸入有效的副檔名做為逗號分隔值(例如 `png, jpg, gif`)。 的&#x200B;**[!UICONTROL Maximum Image Size]**，輸入影像大小上限（畫素）。 如果是文字專案，請輸入&#x200B;**[!UICONTROL Maximum Characters]**.

   ![新增自訂選項的值](./assets/product-customizable-options-add-values.png){width="600" zoomable="yes"}

1. （選擇性）如果要新增其他可自訂的選項，請按一下 **[!UICONTROL Add Option]**.

   - 如前完成設定。

   - 若要變更選項的順序，請按一下 _[!UICONTROL Order]_![排序順序圖示](../assets/icon-sort-order.png) 圖示並將選項拖曳至清單中的新位置。

   對每個要新增的選項重複此步驟。

1. 完成後，按一下 **[!UICONTROL Save]**.

## 匯入可自訂的選項

1. 在 _可自訂的選項_ 區段，按一下 **[!UICONTROL Import Options]**.


1. 所有具有可自訂選項的產品都會顯示在格線中。

1. 在清單中，選取包含您要匯入之選項之產品的核取方塊。

1. 按一下 **[!UICONTROL Import]**.

1. 完成後，您可以繼續新增更多自訂選項，或按一下 **[!UICONTROL Save and Close]**.

## 輸入型別

| 型別 | 說明 |
|---------------------|---------------|
| [!UICONTROL Text] | 客戶可在其中輸入所需資訊的輸入行或文字方塊。 選項：<br />**[!UICONTROL Field]**— 單行文字輸入欄位。<br />**[!UICONTROL Area]**  — 多行輸入欄位。 此型別不支援進階格式，例如HTML。 使用最大字元數來限制可輸入的文字長度，並確保在Admin中輸入的文字有正確表示。 |
| [!UICONTROL File] | 允許客戶上傳檔案。 |
| [!UICONTROL Select] | 允許客戶根據使用的輸入型別，選取單一選項或多個選項。 選項：<br />**[!UICONTROL Drop-down]**— 僅允許一個選取範圍的選項下拉式清單。<br />**[!UICONTROL Radio Buttons]**  — 一組僅允許一個選取範圍的選項。<br />**[!UICONTROL Checkbox]**— 核取方塊是「是/否」選項的變體。 如果產品有多個核取方塊，則可以進行多個選取。<br />**[!UICONTROL Multiple Select]**  — 接受多個選取專案的下拉式選項清單方塊。 若要選擇多個選項，請按住Ctrl (PC)或Command (Mac)鍵並按一下每個選項。 |
| [!UICONTROL Date] | 允許客戶輸入日期或時間，或從工作歷選擇值。 選項： <br />**[!UICONTROL Date]**— 日期值的輸入欄位。 可以直接在欄位中輸入日期，或從清單或行事曆中選取日期。 輸入方法和格式由 [日期和時間選項](attributes-input-types.md#date-and-time-options) 設定。<br />**[!UICONTROL Date & Time]**  — 日期和時間值的輸入欄位。<br />**[!UICONTROL Time]**— 時間值的輸入欄位。 |

{style="table-layout:auto"}
