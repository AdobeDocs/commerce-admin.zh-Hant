---
title: 虛擬產品
description: 瞭解如何建立代表非實體專案的虛擬產品，例如會籍、服務、保固或訂閱。
exl-id: 8788ba04-e911-429e-9e48-ce589f0c9fa1
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 0%

---

# 虛擬產品

虛擬產品（或數位產品）代表無形的專案，例如會籍、服務、保固，或書籍、音樂、視訊或其他產品的訂閱和數位下載。 虛擬產品可以單獨銷售，也可以包含在 [已分組的產品](product-create-grouped.md)， [可設定的產品](product-create-configurable.md)，或 [套裝產品](product-create-bundle.md) 產品型別。

除了沒有 _[!UICONTROL Weight]_欄位，建立虛擬產品的程式與簡單產品的程式相同。 下列指示示範使用建立虛擬產品的程式 [產品範本](attribute-sets.md)、必填欄位和基本設定。 當您完成基本功能後，您可以視需要完成其他產品設定。

>[!NOTE]
>
>PayPal已取代透過PayPal Express Checkout支援數位商品銷售。 他們建議您使用 [PayPal支付標準](../stores-purchase/paypal-payments-standard.md) 或任何其他PayPal付款閘道，以處理包括虛擬產品的任何訂單。

![虛擬產品](./assets/product-virtual-membership.png){width="700" zoomable="yes"}

## 步驟1：選擇產品型別

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 在 _[!UICONTROL Add Product]_( ![選單箭頭](../assets/icon-menu-down-arrow-red.png){width="25"} )功能表，選擇&#x200B;**[!UICONTROL Virtual Product]**.

   ![新增虛擬產品](./assets/product-add-virtual.png){width="700" zoomable="yes"}

## 步驟2：選擇屬性集

若要選擇 [屬性集](attribute-sets.md) 作為產品的範本，請執行下列任一項作業：

- 按一下 **[!UICONTROL Attribute Set]** 欄位並輸入屬性集的全部或部分名稱。

- 在顯示的清單中，選擇要使用的屬性集。

表單會更新以反映變更。

![選擇屬性集](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## 步驟3：完成必要的設定

1. 輸入 **[!UICONTROL Product Name]**.

1. 接受預設值 **[!UICONTROL SKU]** 根據產品名稱或輸入其他名稱。

1. 輸入產品 **[!UICONTROL Price]**.

1. 由於產品尚未準備好發佈，請設定 **[!UICONTROL Enable Product]** 至 `No`.

1. 按一下 **[!UICONTROL Save]** 並繼續。

   儲存產品時， [存放區檢視](introduction.md#product-scope) 選擇器會出現在左上角。

1. 選擇 **[!UICONTROL Store View]** 產品可用的位置。

   ![選擇存放區檢視](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## 步驟4：完成基本設定

1. 設定 **[!UICONTROL Tax Class]** 變更為下列其中一項：

   - `None`
   - `Taxable Goods`

1. 輸入 **[!UICONTROL Quantity]** 庫存產品的屬性，並執行下列動作：

   - 接受預設值 **[!UICONTROL Stock Status]** 設定 `In Stock`.

     由於虛擬產品尚未出貨，因此 **[!UICONTROL Weight]** 欄位未使用。

   - 接受預設值 **[!UICONTROL Visibility]** 設定 `Catalog, Search`.

   >[!NOTE]
   >
   >如果您啟用 [Inventory management](../inventory-management/introduction.md)，單一來源商家在此區段中設定數量。 多來源商家在「來源」區段中新增來源與數量。 請參閱下列內容 _指定來源與數量(Inventory management)_ 區段。

1. 要指派 **[!UICONTROL Categories]** 若要存取產品，請按一下 **[!UICONTROL Select…]** 方塊並執行下列任一項作業：

   **選擇現有類別**：

   - 開始在方塊中輸入內容，直到找到相符專案為止。

   - 選取要指派的類別的核取方塊。

   **建立類別**：

   - 按一下 **[!UICONTROL New Category]**.

   - 輸入 **[!UICONTROL Category Name]** 並選擇 **[!UICONTROL Parent Category]**，這會決定其在功能表結構中的位置。

   - 按一下 **[!UICONTROL Create Category]**.

   可能有其他個別屬性可說明產品。 選取範圍會因屬性集而異，您稍後可以完成。

### 指定來源與數量([!DNL Inventory Management])

{{$include /help/_includes/inventory-assign-sources.md}}

## 步驟5：完成產品資訊

視需要填寫下列章節中的資訊：

- [內容](product-content.md)
- [影像和影片](product-images-and-video.md)
- [搜尋引擎最佳化](product-search-engine-optimization.md)
- [相關產品、向上銷售和交叉銷售](related-products-up-sells-cross-sells.md)
- [可自訂的選項](settings-advanced-custom-options.md)
- [網站中的產品](settings-basic-websites.md)
- [設計](settings-advanced-design.md)
- [贈品選項](product-gift-options.md)

>[!NOTE]
>
>此 _[!UICONTROL Is this downloadable product?]_選項預設為停用。 為虛擬產品啟用此功能可製造產品 [可下載](product-create-downloadable.md#downloadable-product).

## 步驟6：發佈產品

1. 如果您已準備好在目錄中發佈產品，請設定 **[!UICONTROL Enable Product]** 至 `Yes`.

1. 執行下列任一項作業：

   - **方法1：** 儲存並預覽

      - 在右上角，按一下 **[!UICONTROL Save]**.

      - 若要檢視您商店中的產品，請選擇 **[!UICONTROL Customer View]** 於 _管理員_ ( ![選單箭頭](../assets/icon-menu-down-arrow-black.png) )功能表。

     該存放區會在新的瀏覽器標籤中開啟。

     ![客戶檢視](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **方法2：** 儲存並關閉

     在 _[!UICONTROL Save]_(![選單箭頭](../assets/icon-menu-down-arrow-red.png){width="25"} )功能表，選擇&#x200B;**[!UICONTROL Save & Close]**.

## 注意事項

- 虛擬產品用於非實體產品，例如服務、訂閱和保固。

- 虛擬產品就像簡單的產品，但沒有重量。

- 除非購物車中有實際產品，否則結帳期間不會顯示送貨選項。
