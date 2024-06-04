---
title: 設定共用目錄定價與結構
description: 透過Adobe Commerce B2B，瞭解如何設定共用目錄的定價和結構。
exl-id: 67caf56f-1b31-44bb-98dc-ea6ea7d8a4d5
feature: B2B, Companies, Catalog Management
role: Admin
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1305'
ht-degree: 0%

---

# 設定共用目錄定價與結構

設定共用型錄的定價與結構有兩個步驟。 您在程式中的目前位置會在頁面頂端的進度列中顯示一個數字。 您可以隨時按一下進度列來檢視程式中的其他步驟。 例如，如果您正在處理自訂定價，您可能想要返回產品選擇頁面以供參考。 只需按一下 **[!UICONTROL Products]** ，然後按一下「 」 **[!UICONTROL Pricing]** 以返回自訂定價頁面。 您的工作在此過程中不會遺失。

![目錄中的產品](./assets/shared-catalog-products-workspace.png){width="700" zoomable="yes"}

在標準類別樹狀結構中，根類別是最上層的容器，稱為 _預設類別_ 在範例資料中。 不過，啟用共用目錄時，類別樹狀結構會有一個名為的外部容器 _根目錄_. 根目錄包含系統中存在的所有其他類別結構。 如需詳細資訊，請參閱 [目錄範圍](../catalog/introduction.md#catalog-scope).

## 步驟1：開啟共用型錄訂價與結構組態

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**

1. 對於格線中的共用目錄，請移至 _[!UICONTROL Action]_欄並按一下&#x200B;**[!UICONTROL Set Pricing and Structure]**.

   ![設定共用型錄的定價和結構](./assets/shared-catalog-set-pricing-structure.png){width="700" zoomable="yes"}

1. 第一次設定共用目錄時，請按一下 **[!UICONTROL Configure]** 以繼續下列步驟。

## 步驟2：選擇產品

此程式的第一個步驟是選擇要包含在共用目錄中的產品。 產品選擇頁面提供 [類別樹狀結構](../catalog/category-create.md) 和右側同步的產品格線。 如果按一下樹狀結構中的類別，該類別中的產品會出現在格線中。

只有已選取產品的類別才會出現在 [上層導覽](../catalog/navigation-top.md) 從店面檢視共用目錄時。 依預設，只有前三個類別層級會包含在店面導覽中，不包括根類別。

1. 使用 **儲存** 選擇器設定 [範圍](../catalog/introduction.md#product-scope) 設定的。

   只有在第一次儲存共用目錄之前，才能設定設定的範圍。 如果您稍後編輯產品選擇，將無法使用「商店」選擇器。

   ![選擇存放區](./assets/shared-catalog-products-scope.png){width="600" zoomable="yes"}

1. 在類別樹狀結構中，執行下列任一項作業：

   - 若要包含所有產品，請按一下 **[!UICONTROL Select all]** 或選取父類別的核取方塊。
   - 若要包含特定類別的產品，請選取您要包含的每個類別的核取方塊。
   - 若要包含或排除個別產品，請選取或取消選取產品的核取方塊。

   樹狀結構中每個類別下方的標籤法會顯示目前包含在共用目錄中的類別產品數量。 下方記號 [根類別](../catalog/category-root.md) 顯示目前為共用目錄選取之所有類別的產品總數。

1. 若要檢視格線中的類別產品，請按一下樹狀結構中的類別名稱。 選取類別時，會發生下列情況：

   - 格線第一欄的切換設定為綠色 _開啟_ 每個所選產品的位置。
   - 如果產品被指派給多個類別，且未在其中一個類別中選取，則它仍可透過其他類別使用，在使用時也可使用 [目錄搜尋](../catalog/search.md).
   - 系統會自動設定 [類別許可權](../catalog/category-permissions.md) 至 `Allow` 所選產品的。

1. 如有必要，請使用篩選條件和其他格線控制項來尋找要包含在共用目錄中的產品。

   您可以按一下第一欄中的切換，個別選取或省略個別產品。

   如果您選取的類別沒有產品，但連結至CMS內容或外部連結，則會顯示在店面的頂端導覽區域中。

   在儲存組態之前，您所做的類別設定不會永久記錄在資料庫中。 不過，當您處理結構和定價時，它們會暫時儲存。

1. 按一下 **[!UICONTROL Next]**.

   ![選取目錄產品](./assets/shared-catalog-select-products-step-1.png){width="600" zoomable="yes"}

## 步驟3：設定自訂價格

您可以個別設定每個產品的自訂價格，或使用 _[!UICONTROL Action]_控制項以將自訂訂訂價設定為多個產品記錄的固定金額或百分比。

- **[!UICONTROL Fixed]**：指定最終產品價格。 例如，如果您輸入$10.00的固定價格，則對應公司的店面價格為$10.00。

  >[!NOTE]
  >
  >「基本價格」與輸入的「固定」值之間的最小值會用作最終產品價格。

  >[!NOTE]
  >
  >**_固定價格_** 產品可自訂選項包括 _非_ 受「群組價格」、「層級價格」、「特殊價格」或「型錄價格」規則影響。

- **[!UICONTROL Percentage]**：根據折扣百分比決定自訂價格。 例如，若要提供10%的折扣，請將自訂價格型別設為 `Percentage` 並輸入 `10`. 折扣的自訂價格是原始產品價格的90%。

若要針對下列產品型別將折扣設定為固定金額或百分比，請使用 _[!UICONTROL Custom Price]_格線中的欄：

- [簡單](../catalog/product-create-simple.md) （包括可設定的產品變體）
- [組合](../catalog/product-create-bundle.md)
- [可下載](../catalog/product-create-downloadable.md)
- [虛擬](../catalog/product-create-virtual.md)

自訂價格欄是空白的 [可設定](../catalog/product-create-configurable.md) 和 [已分組](../catalog/product-create-grouped.md) 產品型別和 [禮品卡](../catalog/product-gift-card-create.md).

格線中的產品選擇無法從 _自訂價格_ 頁面。 不過，您可以使用頁面頂端的進度指示器來返回上一個步驟，並變更產品選擇。

![選取目錄產品](./assets/shared-catalog-custome-prices-step-3.png){width="600" zoomable="yes"}

### 套用自訂價格

1. 若為多站台安裝，請設定 **[!UICONTROL Website]** 至套用自訂價格的網站。

   ![選擇網站](./assets/shared-catalog-scope-pricing.png){width="600" zoomable="yes"}

1. 使用下列其中一種方法，選取要套用自訂訂訂價的產品。

   - 使用類別樹狀結構來選取特定類別中的所有產品。
   - 設定 _[!UICONTROL Mass Actions]_標題中的控制項至 `Select All`.
   - 選取個別產品的核取方塊。

   格線會顯示目前選取類別中的產品，您可以使用標準控制項來尋找產品並篩選清單。

   ![全選](./assets/shared-catalog-custom-pricing-mass-actions.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Actions]** 變更為下列其中一項：

   - `Set Discount`  — 將折扣百分比套用至所有選取的產品。 每個受影響的產品價格都會顯示為 **_已折扣_** 價格。
   - `Adjust Fixed Price`  — 將固定價格折扣百分比套用至所有選取的產品。 每個受影響的產品價格會顯示為 **_已調整固定_** 價格。

   ![作業控制 — 設定折扣](./assets/shared-catalog-set-custom-prices-discount-action.png){width="600" zoomable="yes"}

1. 出現提示時，輸入折扣或價格調整，然後按一下 **[!UICONTROL Apply]**.

   ![設定折扣](./assets/shared-catalog-set-custom-prices-discount.png){width="400"}<br/>

   ![調整固定價格](./assets/shared-catalog-set-custom-fixed-prices.png){width="400"}

   折扣會套用至所有已選取的產品，以及 _自訂價格_ 欄位會反映折扣和套用金額的型別。

   ![具有折扣的自訂價格欄](./assets/shared-catalog-set-custom-prices-discount-applied.png){width="600" zoomable="yes"}

### 套用層級價格

[層級定價](../catalog/product-price-tier.md) 可讓您為共用目錄中的產品提供數量折扣。 此 _層級價格_ 格線的欄包含連結至 _進階定價_ 特別適用於共用目錄的選項。 如果產品已包含層級定價，則現有層級的數量會顯示在連結後的括弧中。

下列指示說明如何將層級定價套用至單一產品。 若要將層級定價套用至多種產品，請參閱 [匯入層級價格](../systems/data-import-price-tier.md).

1. 對於格線中的產品，請移至 _層級價格_ 欄並按一下 **[!UICONTROL Configure]**.

   ![設定層級價格](./assets/shared-catalog-tier-price-configure.png){width="600" zoomable="yes"}

1. 在 _進階定價_ 頁面，按一下 **[!UICONTROL Add Price]** 並執行下列動作：

   ![目錄與階層價格](./assets/shared-catalog-tier-price-configure-add-price.png){width="600" zoomable="yes"}

   - 設定 **[!UICONTROL Website]** 至套用層級價格的網站。
   - 輸入必須購買才能獲得折扣的產品數量。
   - 設定 **[!UICONTROL Price]** 折扣型態：
      - `Fixed`
      - `Discount`
   - 輸入折扣金額。
   - 若要輸入其他階層，請按一下 **新增價格** 並重複此程式以定義下一個階層。

   ![多層價格](./assets/shared-catalog-tier-price-configure-multiple-tiers.png){width="600" zoomable="yes"}

1. 完成後，按一下 **[!UICONTROL Done]**.

   在格線中，層數會顯示在中的括弧中 _[!UICONTROL Tier Price]_欄。

   ![多層](./assets/shared-catalog-tier-price-configure-parentheses.png){width="600" zoomable="yes"}

## 儲存結構和定價

當自訂定價完成時，按一下 **[!UICONTROL Generate Catalog]** 則 **[!UICONTROL Save]**.

共用目錄現在會儲存至資料庫。 其名稱會顯示在 _[!UICONTROL Shared Catalog]_的欄_[!UICONTROL Products]_ 格線。 下一步是 [將共用目錄指派給公司](./catalog-shared-assign-companies.md).
