---
title: 建立類別
description: 您可以根據組態中設定的最大選單深度，視需要建立任意數量的其他子類別。
exl-id: 8ba5fc1a-3bf2-4a29-bbc3-709fc0ad7497
feature: Catalog Management, Categories
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1125'
ht-degree: 0%

---

# 建立類別

型錄的類別結構就像上下顛倒的樹狀結構，其根位於頂端。 樹狀結構的每個區段都可以展開和摺疊。 任何停用或隱藏的類別都會呈現灰色。 第一層級的類別(在 [根](category-root.md))通常會顯示為中的選項 [主功能表](navigation-top.md). 您可以根據組態中設定的最大選單深度，視需要建立任意數量的其他子類別。 類別可以拖放至樹狀結構中的其他位置。 類別ID編號會顯示在頁面頂端類別名稱后的括弧中。

針對具有多個專案的網站 [商店](../stores-purchase/stores.md#add-stores)，您可以為每個存放區建立不同的根類別，以定義用於的類別集 [上層導覽](navigation-top.md).

![類別樹狀結構](./assets/category-selected.png){width="700" zoomable="yes"}

## 最佳實務

計畫和建立類別時，請使用這些最佳實務。

### 類別結構

主功能表中的類別結構可能會影響客戶體驗和效能。 作為最佳實務，您應該識別一個首要的頂層類別，並避免有其他具有相同名稱的類別。 例如，不要讓「小孩」在不同部門下組織多個類別，例如 `Clothing/Kids`， `Shoes/Kids`， `Accessories/Kids`. 建立頂層父級類別會更有效率 `Kids`，然後視需要在下方建立子類別。 請和類別結構保持一致，並對目錄中的所有產品型別使用相同的方法。

### 商業規則和自動化

使用商業邏輯在目錄頁面上顯示類似專案，或設定個人化促銷、自動化流程或搜尋條件時，請考慮類別結構和可用的屬性值。 例如，如果您指定「polo」作為父類別，結果可能會包含性別和年齡不適當的混合產品。 不過，如果您符合特定次類別的polo襯衫，結果會比較窄，而且可能會吸引特定客戶。 結合其他以特定客戶為目標的屬性值時，結果可能更具體一些。 參考特定類別路徑時，請考慮必須篩選及擷取的產品數量。 結果差異可能非常大。 考量下列類別路徑傳回的不同結果：

- `[Category:  All Products/Shirts/Father's Day/Polos/Sale]`
- `[Category Path: Men/Shirts/Polos]`
- `[Child Category: Polos]`

請務必明確定義分類關係，例如：

- 父類別
- 子類別
- 類別路徑

也定義任何關聯的關鍵字和屬性，例如：

- 可用性
- 售價
- 品牌
- 大小
- 顏色

## 步驟1：建立類別

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. 設定 **[!UICONTROL Store View]** 以判斷新類別在何處可用。

1. 在類別樹狀結構中，選取新類別的父類別。

   父級比新類別高一個層級。

   如果您從頭開始，沒有資料，清單中可能只有兩個類別： _預設類別_，這是根，以及 _範例類別_

1. 按一下 **[!UICONTROL Add Subcategory]**.

## 步驟2：完成基本資訊

1. 如果您想要讓類別立即位於商店中，請設定 **[!UICONTROL Enable Category]** 至 `Yes`.

1. 若要將類別包含在 [上層導覽](navigation-top.md)，設定 **[!UICONTROL Include in Menu]** 至 `Yes`.

1. 輸入 **[!UICONTROL Category Name]**.

   ![基本類別資訊](./assets/catalog-categories-currently-active.png){width="500" zoomable="yes"}

1. 按一下 **[!UICONTROL Save]** 並繼續。

## 步驟3：完成類別內容

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Content]** 區段。

   ![類別內容](./assets/category-content.png){width="600" zoomable="yes"}

1. 若要顯示 **[!UICONTROL Category Image]** 在頁面頂端，您可以上傳自己的影像，或使用中存在的影像 [媒體儲存](../content-design/media-storage.md).

   - 若要上傳您自己的影像，請按一下 **[!UICONTROL Upload]** 並選擇要代表類別的影像。

   - 若要使用「媒體儲存體」中的影像，請按一下 **[!UICONTROL Select from Gallery]** 並選取您要代表類別的影像。

   >[!NOTE]
   >
   >在「媒體集」內，您也可以使用 [Adobe Stock整合](../content-design/adobe-stock.md) 若要尋找適當的影像，請按一下 **[!UICONTROL Search Adobe Stock]**.

1. 的 **[!UICONTROL Description]**，輸入您要顯示在類別登入頁面上的文字或其他內容。

   如需詳細資訊，請參閱 [類別內容](categories-content-settings.md).

1. 若要在類別登入頁面上加入內容區塊，請選擇 **[!UICONTROL CMS Block]** 您希望顯示的專案。

1. 按一下 **[!UICONTROL Save]** 並繼續。

## 步驟4：完成顯示設定

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Display Setting]** 區段。

   ![顯示設定](./assets/category-display-settings.png){width="600" zoomable="yes"}

   如需這些選項的詳細資訊，請參閱如需這些選項的詳細資訊，請參閱  [顯示設定](categories-display-settings.md).

1. 設定 **[!UICONTROL Display Mode]** 變更為下列其中一項：

   - `Products Only`
   - `Static Block Only`
   - `Static Block and Products`

1. 如果您希望類別頁面包含 _`Filter by Attribute`_分層導覽的區段，設定&#x200B;**[!UICONTROL Anchor]**至 `Yes`.

1. 對於 **[!UICONTROL Available Product Listing Sort By]** 選項，選取一或多個可供客戶排序清單的可用值。 此設定不適用於 [!DNL Live Search] [產品清單頁面Widget](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/plp-styling).

   依預設，會包含所有可用的值。 取消選取 **[!UICONTROL Use All]** 核取方塊以變更選取專案。 例如，值可能包括：

   - `Position`
   - `Product Name`
   - `Price`

1. 若要設定類別的預設排序順序，請選擇 **[!UICONTROL Default Product Listing Sort By]** 值。 此設定不適用於 [!DNL Live Search] [產品清單頁面Widget](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/plp-styling).

1. 變更預設圖層導覽 [價格步驟](navigation-layered.md#configure-price-navigation) 設定，請執行下列動作：

   - 取消選取 **[!UICONTROL Use Config Settings]** 核取方塊。

   - 輸入要做為分層導覽之增量價格步驟的值。

1. 按一下 **[!UICONTROL Save]** 並繼續。

## 步驟5：完成搜尋引擎最佳化設定

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Search Engine Optimization Settings]** 區段。

   ![搜尋引擎最佳化](./assets/categories-search-engine-optimization.png){width="600" zoomable="yes"}

   如需這些選項的詳細資訊，請參閱 [搜尋引擎最佳化](categories-search-engine-optimization.md).

1. 完成下列作業 [中繼資料](../merchandising-promotions/meta-data.md) 類別為：

   - [!UICONTROL Meta Title]
   - [!UICONTROL Meta Keywords]
   - [!UICONTROL Meta Description]

1. 按一下 **[!UICONTROL Save]** 並繼續。

## 步驟6：選擇類別中的產品

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Products in Category]** 區段。

   ![類別中的產品](./assets/category-products-in-category.png){width="600" zoomable="yes"}

   如需這些選項的詳細資訊，請參閱 [類別中的產品](categories-product-assignments.md).

1. 如有需要，請使用 [篩選器](../getting-started/admin-grid-controls.md) 以尋找產品。

   若要顯示類別中尚未包含的所有記錄，請將第一欄中的記錄選擇器設為 `No` 並按一下 **[!UICONTROL Search]**.

1. 在第一欄中，針對要包含在類別中的每個產品選取核取方塊。

1. 按一下 **[!UICONTROL Save]** 並繼續。

## 步驟7：設定類別許可權

{{ee-feature}}

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Category Permissions]** 區段。

1. 如果是多站台安裝，請選擇 **[!UICONTROL Website]** 類別許可權適用的位置。

1. 選擇 **[!UICONTROL Customer Group]** 類別許可權適用的位置。

   ![Adobe Commerce B2B](../assets/b2b.svg) ([Adobe Commerce B2B](../b2b/introduction.md) 僅限)如有需要，您可以選擇 **[!UICONTROL Shared Catalog]** 而非。

1. 視需要設定下列許可權：

   - [!UICONTROL Browsing Category]
   - [!UICONTROL Display Product Prices]
   - [!UICONTROL Add to Cart]

1. 若要新增其他許可權規則，請按一下 **[!UICONTROL New Permission]** 並重複此程式。

   ![類別許可權](./assets/category-create-permissions.png){width="600" zoomable="yes"}

## 步驟8：完成設計設定

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Design]** 區段。

1. 視需要設定設計設定：

   - ([Adobe Commerce B2B](../b2b/introduction.md) 僅限)若要將父類別設計設定套用至此類別，請設定 **[!UICONTROL Use Parent Category Settings]** 至 `Yes`.

   - 若要變更類別頁面的設計，請選擇 **[!UICONTROL Theme]** 要套用的資訊。

   - 若要變更類別頁面的欄配置，請選擇 **[!UICONTROL Layout]** 要套用的資訊。

   - 若要輸入自訂程式碼，請在 **[!UICONTROL Layout Update XML]** 方塊。

   - 若要對產品頁面使用相同設計，請設定 **[!UICONTROL Apply Design to Products]** 至 `Yes`.

   ![設計設定](./assets/category-design.png){width="600" zoomable="yes"}

1. ![Magento Open Source](../assets/open-source.svg) (僅限Magento Open Source)若要排程特定時段的設計更新，請執行下列動作：

   - 展開 _[!UICONTROL Schedule Design Update]_區段。

   - 使用行事曆(![行事曆圖示](../assets/icon-calendar.png))以選擇排程更新 **[!UICONTROL from]** 和 **[!UICONTROL to]** 日期。

   ![排程的設計更新](./assets/category-scheduled-design-update.png){width="600" zoomable="yes"}

1. 完成後，按一下 **[!UICONTROL Save]**.
