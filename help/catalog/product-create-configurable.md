---
title: 可設定的產品
description: 瞭解如何建立可設定的產品，為購物者提供各種選擇。
exl-id: 2066fd20-5227-41e9-b213-31825a58ebd9
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '2416'
ht-degree: 0%

---

# 可設定的產品

可設定的產品看起來就像單一產品，有每個變數的下拉式清單。 每個清單專案實際上是一個單獨的簡單產品，具有唯一的SKU，因此可以追蹤每個產品變體的存貨。 您可以使用具有自訂選項的簡單產品來達到類似的效果，但無法追蹤每個變數的詳細目錄。

下列指示會示範使用來建立可設定產品的程式 [產品範本](attribute-sets.md)、必填欄位和基本設定。 每個必填欄位都標有紅色星號(`*`)。 當您完成基本功能後，您可以視需要完成其他產品設定。

![可設定的產品](./assets/product-configurable.png){width="700" zoomable="yes"}

## 第1部分：建立可設定的產品

雖然可設定的產品使用較多SKU，且一開始可能需要較長時間進行設定，但最終可為您節省時間。 如果您計畫拓展業務，可設定的產品型別對於具有多種選項的產品來說是個不錯的選擇。

開始之前，請準備 [屬性集](attribute-sets.md) 其屬性會針對每個產品變數設定為其中一個允許的輸入型別。 例如，屬性集可能包含顏色和大小的下拉式清單屬性。

用於可設定產品變數的每個屬性的屬性必須具有下列設定：

### 產品變數屬性需求

| 屬性 | 設定 |
|--- |--- |
| [!UICONTROL Scope] | `Global` |
| [!UICONTROL Catalog Input Type for Store Owner] | 用於產品變數的任何屬性的輸入型別必須是下列其中一項： `Dropdown`， `Visual Swatch`，或 `Text Swatch`. |
| [!UICONTROL Values Required] | `Yes` |

{style="table-layout:auto"}

### 步驟1：選擇產品型別

1. 在 _管理員_ 側欄，前往  **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 在 _[!UICONTROL Add Product]_( ![選單箭頭](../assets/icon-menu-down-arrow-red.png){width="25"} )功能表，選擇&#x200B;**[!UICONTROL Configurable Product]**.

   ![新增可設定的產品](./assets/product-add-configurable.png){width="700" zoomable="yes"}

### 步驟2：選擇屬性集

此 [屬性集](attribute-sets.md) 決定產品中使用的欄位選擇。 下列範例中使用的屬性集具有顏色和大小的屬性。 屬性集的名稱會顯示在頁面頂端，且一開始會設為 `Default`.

1. 若要選擇產品的屬性集，請按一下頁面頂端的欄位，然後執行下列任一項作業：

   - 的 **[!UICONTROL Search]**，輸入屬性集的名稱。
   - 在清單中，選擇要使用的屬性集。

   表單會更新以反映變更。

1. 如果要將另一個屬性加入屬性集，請按一下 **[!UICONTROL Add Attribute]** 並依照中的指示操作 [新增屬性](product-attributes-add.md).

   ![選擇範本](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

### 步驟3：完成必要的設定

1. 輸入產品 **[!UICONTROL Product Name]**.

1. 接受預設值 **[!UICONTROL SKU]** 根據產品名稱或輸入其他名稱。

1. 輸入產品 **[!UICONTROL Price]**.

1. 由於產品尚未準備好發佈，請設定 **[!UICONTROL Enable Product]** 至 `No`.

1. 按一下 **[!UICONTROL Save]** 並繼續。

   儲存產品時， [存放區檢視](introduction.md#product-scope) 選擇器會出現在左上角。

1. 選擇 **[!UICONTROL Store View]** 產品可用的位置。

   ![選擇商店檢視](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

### 步驟4：完成基本設定

1. 設定 **[!UICONTROL Tax Class]** 變更為下列其中一項：

   - `None`
   - `Taxable Goods`

1. 此 **[!UICONTROL Quantity]** 由產品變數決定，因此您可以保留空白。

1. 離開 **[!UICONTROL Stock Status]** 依預設。

   可設定產品的「庫存狀態」取決於每個關聯的組態。 由於儲存產品時未輸入數量，因此 **[!UICONTROL Stock Status]** 設為 `Out of Stock`.

   >[!NOTE]
   >
   >此 **庫存狀態** 可設定產品的 **_半手動_** 控制設定。 它部分受到其子產品的庫存狀態所控制。 它是 **_多條件_** 庫存狀態計算，詳見 [設定庫存狀態](#configure-the-stock-status) 區段。

1. 輸入產品 **[!UICONTROL Weight]**.

>[!NOTE]
>
>可設定的產品必須一律有權重。 如果您選取 **[!UICONTROL This item has no weight]** 從下拉式清單中，會自動變更為 **[!UICONTROL This item has weight]** 儲存產品之後。

1. 接受預設值 **[!UICONTROL Visibility]** 設定 `Catalog, Search`.

1. 若要在產品清單中推出產品 [新產品](../content-design/widget-new-products-list.md)，選取 **[!UICONTROL Set Product as New]** 核取方塊。

1. 若要將類別指派給產品，請按一下 **[!UICONTROL Select…]** 方塊並執行下列任一項作業：

   **選擇現有類別**：

   - 開始在方塊中輸入內容，直到找到相符專案為止。

   - 選取要指派的類別的核取方塊。

   ![選取套裝產品的一或多個類別](./assets/product-create-categories.png){width="600" zoomable="yes"}

   **建立類別**：

   - 按一下 **[!UICONTROL New Category]**.

   - 輸入 **[!UICONTROL Category Name]** 並選擇 **[!UICONTROL Parent Category]**，這會決定其在功能表結構中的位置。

   s — 按一下 **[!UICONTROL Create Category]**.

1. 選擇 **[!UICONTROL Country of Manufacture]**.

   可能會有其他屬性用於描述產品。 選取範圍會因屬性集而異，您稍後可以完成它們。

### 步驟5：儲存並繼續

現在是儲存工作的好時機。 在右上角，按一下 **[!UICONTROL Save]**. 在接下來的幾個步驟中，您將針對產品的每個變化來設定設定。

## 第2部分：新增組態

下列範例說明如何新增三種顏色和三種大小的組態。 共有9種簡單產品是以唯一的SKU建立的，涵蓋各種變數的可能組合。 依預設，每個變數的產品名稱和SKU都以屬性值和上層產品名稱或SKU為基礎。

頁面頂端的進度列會顯示您在程式中的位置，並引導您完成每個步驟。

### 步驟1：選擇屬性

1. 從上方繼續，向下捲動至 _[!UICONTROL Configurations]_區段並按一下&#x200B;**[!UICONTROL Create Configurations]**.

   ![設定](./assets/product-configurable-create-configurations.png){width="600" zoomable="yes"}

1. 選取每個要納入設定的屬性的核取方塊。

   在此範例中， `color` 和 `size` 已選取。

   ![選取屬性](./assets/product-create-configurable-step1.png){width="600" zoomable="yes"}

   清單包括屬性集中可用於可設定產品的所有屬性。

1. 如果要新增屬性，請按一下 **[!UICONTROL Create New Attribute]** 並執行下列動作：

   - 完成屬性屬性。

   - 按一下 **[!UICONTROL Save Attribute]**.

   - 選取屬性的核取方塊。

1. 在右上角，按一下 **[!UICONTROL Next]**.

### 步驟2：輸入屬性值

1. 針對每個屬性，選取套用至產品的值核取方塊。

   ![屬性值](./assets/product-create-configurable-step2.png){width="600" zoomable="yes"}

1. 若要重新排列屬性，請抓取 _重新排序_ ( ![排序順序圖示](../assets/icon-sort-order.png) )圖示並將區段移至新位置。

   順序會決定下拉式清單在產品頁面上的位置。

1. 在進度列中，按一下 **[!UICONTROL Next]**.

### 步驟3：設定影像、價格和數量

此步驟會決定每個設定的影像、定價和數量。 每個的可用選項都相同，您只能選擇一個。 您可以將相同的設定套用至所有SKU、將唯一的設定套用至每個SKU，或暫時略過這些設定。

選擇適用的組態選項。

使用下列其中一種方法來設定 **[!UICONTROL images]**：

**方法1：** 將單一影像集套用至所有SKU

1. 選取 **[!UICONTROL Apply single set of images to all SKUs]**.

1. 瀏覽至每個要包含在產品相簿中的影像，或將它們拖曳至方塊。

![對所有SKU使用相同的影像](./assets/product-configurations-images-apply-single-set.png){width="600" zoomable="yes"}

**方法2：** 為每個SKU套用唯一的影像

由於上層產品的影像已上傳，因此您可以使用此選項上傳每種顏色的影像。 當有人以特定顏色購買商品時，您可以新增顯示在購物車中的不同影像。

1. 選取 **[!UICONTROL Apply unique images by attribute to each SKU]**.

1. 選取 **[!UICONTROL Attribute]** 這些影像會加以說明，例如 `color`.

1. 對於每個屬性值，請瀏覽至您要用於該設定的影像，或將它們拖曳至方塊。

   如果您將影像拖曳至數值方塊，它也會出現在其他值的區段中。 如果您要刪除影像，請按一下 _垃圾桶_ (![垃圾桶圖示](../assets/icon-delete-trashcan-solid.png))圖示。

   ![每個SKU的不重複影像](./assets/product-configurable-create-configurations-add-images-unique.png){width="600" zoomable="yes"}

使用下列其中一種方法來設定 **[!UICONTROL prices]**：

**方法1：** 對所有SKU套用相同價格

1. 如果所有變數的價格都相同，請選取 **[!UICONTROL Apply single price to all SKUs]**.

1. 輸入 **[!UICONTROL Price]**.

   ![每個SKU的價格相同](./assets/product-configurable-create-configurations-price-all-skus.png){width="600" zoomable="yes"}

**方法2：** 為每個SKU套用不同的價格

1. 如果每個產品的價格或某些產品的價格不同，請選取 **[!UICONTROL Apply unique prices by attribute to each SKU]**.

1. 選取 **[!UICONTROL Attribute]** 這是價格差異的基礎。

1. 輸入 **[!UICONTROL Price]** 每個屬性值。

   在此範例中，XL大小的成本較高。

   ![每個SKU的不重複價格](./assets/product-configurable-create-configurations-price-unique.png){width="600" zoomable="yes"}

使用下列其中一種方法來設定 **[!UICONTROL Quantity]**：

**方法1：** 將相同數量套用至所有SKU

如果所有SKU的數量都相同，請選取 **[!UICONTROL Apply single quantity to each SKU]** 並指定數量。

_單一來源商家_  — 輸入 **[!UICONTROL Quantity]**.

_多來源商家使用 [Inventory management](../inventory-management/introduction.md)_  — 為所有產生的產品系列指定來源及新增數量：

1. 選取 **[!UICONTROL Apply single quantity to each SKU]** 選項。

1. 若要新增來源，請按一下 **[!UICONTROL Assign Sources]**.

1. 瀏覽或搜尋您要新增的來源。 選取您要為產品新增的來源旁的核取方塊。

1. 輸入每個來源的庫存量數量。

   ![所有SKU的單一數量，指定來源](./assets/inventory-configure-product-quantity.png){width="600" zoomable="yes"}

**方法2：** 依屬性套用不同的數量

_單一來源商家_  — 輸入 **[!UICONTROL Quantity]**.

_多來源商家使用 [Inventory management](../inventory-management/introduction.md)_  — 為所有產生的產品系列指定來源及新增數量：

1. 如果每個SKU的數量不同，請選取 **[!UICONTROL Apply unique quantity by attribute to each SKU]**.

1. 輸入 **[!UICONTROL Quantity]** （每個）。

   ![每個屬性的不同數量](./assets/product-configurations-quantity-different.png){width="600" zoomable="yes"}

影像、價格和數量的設定完成後，請按一下 **[!UICONTROL Next]** 位於右上角。

### 步驟4：產生產品組態

請稍候片刻，讓產品清單顯示，然後執行下列任一項作業：

- 如果您對組態滿意，請按一下 **[!UICONTROL Generate Products]**.

- 若要進行更正，請按一下 **[!UICONTROL Back]**.

![產生產品變數前先檢閱摘要](./assets/product-create-configurable-summary.png){width="600" zoomable="yes"}

目前的產品變數會出現在頁面底部 _設定_ 區段。

![目前的設定](./assets/product-create-configurable-generated.png){width="600" zoomable="yes"}

### 步驟5：新增產品影像

1. 向下捲動並展開 ![展開選擇器](../assets/icon-display-expand.png) 此 _[!UICONTROL Images and Videos]_區段。

1. 按一下 _相機_ 並瀏覽至您要用於可設定產品的主要影像。

如需詳細資訊，請參閱 [影像和視訊](product-images-and-video.md).

### 步驟6：完成產品資訊

視需要向下捲動並填入下列章節中的資訊：

- [內容](product-content.md)

- [相關產品、向上銷售和交叉銷售](related-products-up-sells-cross-sells.md)

- [搜尋引擎最佳化](product-search-engine-optimization.md)

- [可自訂的選項](settings-advanced-custom-options.md)

- [網站中的產品](settings-basic-websites.md)

- [設計](settings-advanced-design.md)

- [贈品選項](product-gift-options.md)

### 步驟7：發佈產品

1. 如果您已準備好在目錄中發佈產品，請設定 **[!UICONTROL Enable Product]** 至 `Yes` 並執行下列任一項作業：

   - **方法1：** 儲存並預覽

      - 在右上角，按一下 **[!UICONTROL Save]**.

      - 若要檢視您商店中的產品，請選擇 **[!UICONTROL Customer View]** 於 _管理員_ ( ![選單箭頭](../assets/icon-menu-down-arrow-black.png) )功能表。

     該存放區會在新的瀏覽器標籤中開啟。

     ![客戶檢視](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **方法2：** 儲存並關閉

     在 _[!UICONTROL Save]_( ![選單箭頭](../assets/icon-menu-down-arrow-red.png){width="25"} )功能表，選擇&#x200B;**[!UICONTROL Save & Close]**.

### 步驟8：設定購物車縮圖

如果您每個變數都有不同的影像，您可以設定為使用購物車縮圖的正確影像。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Sales]** 並選擇 **[!UICONTROL Checkout]** 底下。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 _[!UICONTROL Shopping Cart]_區段。

1. 設定 **[!UICONTROL Configurable Product Image]** 至 `Product Thumbnail Itself`.

1. 完成後，按一下 **[!UICONTROL Save Config]**.

   ![購物車 — 可設定的產品影像](./assets/config-checkout-configurable-product.png){width="600" zoomable="yes"}

## 設定庫存狀態

可設定的產品庫存狀態與簡單產品的庫存狀態不同，後者是產品可用性的直接表示。 對於可設定產品，庫存狀態是的一部分 **_多條件_** 庫存狀態計算。

### 概觀

「庫存狀態」關係的主要原則如下：

- 當您變更 **[!UICONTROL Stock Status]** 可設定產品的 `Out of Stock` 並按一下 **[!UICONTROL Save]**，它是 **_未控制_** 依其子產品的庫存狀態。 它一律顯示為 `Out of Stock` 在管理員和店面中。

- 當您設定 **[!UICONTROL Stock Status]** 可設定產品的 `In Stock` 並按一下 **[!UICONTROL Save]**，它是 **_僅部分控制_** 依其子產品的庫存狀態，這些狀態會反映在管理員和店面中。

### 詳細說明

此 _庫存狀態_ 可設定產品的Stock Status會根據其子產品的部份控制，並依據下列專案 **_多條件_** 庫存狀態計算：

#### 僅使用預設來源/庫存：

- 如果可設定的產品Stock狀態為 **_手動_** 設為 `Out of Stock` 透過管理員使用者、檔案匯入或API呼叫，它保持為 `Out of Stock` 在兩個 **_管理員_** 和 **_店面_** 直到  **_手動_** 已變更為 `In stock` 由管理員使用者、檔案匯入或API呼叫。 無法由其子產品的庫存狀態控制。

- 如果可設定的產品Stock狀態為 **_手動_** 設為 `In Stock` 透過管理員使用者、檔案匯入或API呼叫，其庫存狀態為 **_自動_** 由兩者上其子產品的庫存狀態所控制 **_管理員_** 和 **_店面_**.

>[!NOTE]
>
>自訂庫存和來源屬於 [Inventory management](../inventory-management/sources-stocks.md) 擴充功能，強烈建議您將此工具專門用於管理庫存和來源。 預設來源和庫存函式是 `CatalogInventory` 模組，現已棄用。

#### 至少具有一個自訂來源/庫存：

- 如果可設定的產品「庫存狀態」值為 **_手動_** 設為 `Out of Stock` 透過管理員使用者、檔案匯入或API呼叫，它保持為 `Out of Stock` 在兩個 **_管理員_** 和 **_店面_** 直到 **_手動_** 已變更為 `In Stock` 由管理員使用者、檔案匯入或API呼叫。 It **_無法_** 由其子產品的庫存狀態所控制。

- 如果可設定的產品「庫存狀態」值為 **_手動_** 設為 `In Stock` 透過管理員使用者、檔案匯入或API呼叫，其庫存狀態為 **_自動_** 由上其子產品的庫存狀態所控制 **_店面_** 僅限。

- 如果可設定的產品「庫存狀態」值為 **_手動_** 設為 `In Stock` 透過管理員使用者、檔案匯入或API呼叫，它保持為 `In Stock` 在 **_管理員_** 直到 **_手動_** 已變更為 `Out of Stock` 由管理員使用者、檔案匯入或API呼叫。 It **_無法_** 由其子產品的庫存狀態所控制。

## 注意事項

- 可設定的產品可讓購物者從下拉式清單、多選、視覺色票和文字色票輸入型別中選擇選項。 每個選項都是一個獨立的、簡單的產品。

- [庫存狀態](../inventory-management/sources-stocks.md) 對於可配置產品，則是半手動控制的設定。 它與簡單產品的庫存狀態不同，在這種庫存狀態中，它是產品可用性的直接表示。 對於可設定產品，庫存狀態是多條件庫存狀態計算的一部分。

- 可設定的子產品可以是簡單或虛擬產品 **沒有自訂選項**. 若要讓自訂子產品成為虛擬，您必須選取 `Тhis item has no weight` 針對 **[!UICONTROL Weight]** 分別設定。

- 用於產品變異的屬性必須具有全域範圍，且必須要求客戶選擇值。 產品變數屬性必須包含在用作可設定產品範本的屬性集中。

- 作為可設定產品範本使用的屬性集必須包含包含每個產品變數所需的值的屬性。

- 購物車中的縮圖影像可設定為顯示來自可設定產品記錄或產品變數的影像。

- [色票屬性](swatches.md#create-swatches-for-products) 可設定為透過設定色票而選取時不會顯示對應的簡單產品影像。 **[!UICONTROL Update Product Preview Image]** 選項值至 `No` 在「管理員」的「屬性編輯」頁面上。

- 主題可控制使用者在產品設定之間切換時，影像館的行為。 的預設行為 _空白_ 主題是使用所選的產品變數覆寫父級可設定產品影像。 對於Luma主題，預設行為是將所選產品變數影像附加到父級可配置產品影像之前。
