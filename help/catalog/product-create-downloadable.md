---
title: 可下載的產品
description: 瞭解如何建立可作為數位檔案交付的可下載產品。
exl-id: c3dd4c5f-adc1-4a8f-a9da-7f0dedd1ee34
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1619'
ht-degree: 0%

---

# 可下載的產品

可下載的產品可以是任何可做為檔案提供的產品，例如電子書、音樂、視訊、軟體應用程式或更新。 您可以提供專輯以供銷售，並單獨銷售每首歌。 您也可以使用可下載的產品來交付產品目錄的電子版本。

由於下載要等到購買後才能提供，因此您可以提供範例，例如書籍的節選、音訊檔案的剪輯，或視訊的尾部。 範例是客戶在購買產品之前可以嘗試的東西。 可供下載的檔案可以上傳至您的伺服器或從其他伺服器上傳。

![可下載的產品](./assets/storefront-product-downloadable.png){width="700" zoomable="yes"}

可下載的產品可設定為要求客戶登入帳戶以接收連結，或透過電子郵件傳送並與他人共用。 下載變為可用之前的訂單狀態，預設值和其他傳送選項均在設定中設定。 在規劃可下載的目錄新增專案時，請注意下列事項：

- 可下載的產品可上傳至伺服器，或從網際網路上的其他伺服器連結至。

- 您可以決定客戶可下載產品的次數。

- 購買可下載產品的客戶可能需要先登入，才能進行結帳。

- 訂單位於以下任一位置時，可傳送可下載的產品： `Pending` 或 `Invoiced` 狀態。

- 由於可下載的產品尚未出貨，因此 _送貨_ 當購物車僅包含可下載的產品時，會跳過結帳步驟。


## 設定下載選項

可下載的組態設定會決定可下載產品的預設值和傳送選項，並指定訪客是否可以購買下載專案。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Catalog]** 並選擇 **[!UICONTROL Catalog]** 底下。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 _[!UICONTROL Downloadable Product Options]_區段。

   ![可下載的產品選項](../configuration-reference/catalog/assets/catalog-downloadable-product-options.png){width="700" zoomable="yes"}

   如需這些組態選項的詳細清單，請參閱 [_可下載的產品選項_](../configuration-reference/catalog/catalog.md#downloadable-product-options) 在 _設定參考_.

1. 若要在下載可用時判斷訂購程式的狀態，請設定 **[!UICONTROL Order Item Status to Enable Downloads]** 變更為下列其中一項：

   - `Pending`
   - `Invoiced`

1. 若要設定單一客戶可進行的下載次數的預設限制，請輸入 **[!UICONTROL Default Maximum Number of Downloads]**.

1. 設定 **[!UICONTROL Shareable]** 變更為下列其中一項：

   - `Yes`  — 允許客戶透過電子郵件將下載連結傳送給其他人。
   - `No`  — 要求客戶登入其帳戶以存取下載連結，以防止客戶與其他人共用下載連結。

1. 的 **[!UICONTROL Default Sample Title]**，輸入要在範例選取範圍上顯示的標題。

   ![範例標題](./assets/product-downloadable-config-sample-title.png){width="400"}

1. 的 **[!UICONTROL Default Link Title]**，輸入您要用於下載連結的預設文字。

1. 如果您希望下載連結在新的瀏覽器視窗中開啟，請設定 **[!UICONTROL Opens Links in New Window]** 至 `Yes`.

   此設定是用來讓您的商店保持開啟瀏覽器視窗。

1. 若要判斷可下載內容如何傳遞，請設定 **[!UICONTROL Use Content Disposition]** 變更為下列其中一項：

   - `Attachment`  — 以電子郵件傳送下載連結作為附件。
   - `Inline`  — 以網頁連結的形式傳遞下載連結。

1. 如果您想要求購買者先註冊客戶帳戶並登入，再購買下載專案，請設定 **[!UICONTROL Disable Guest Checkout if Cart Contains Downloadable Items]** 至 `Yes`.

1. 完成後，按一下 **[!UICONTROL Save Config]**.

## 建立可下載的產品

下列指示示範使用建立可下載產品的程式 [產品範本](attribute-sets.md)、必填欄位和基本設定。 每個必填欄位都標有紅色星號(`*`)。 當您完成基本功能後，您可以視需要完成其他產品設定。

>[!NOTE]
>
>可下載的檔案名稱可包含字母和數字。 您可以使用破折號或底線字元來表示字詞之間的空格。 檔案名稱中的任何無效字元都會取代為底線。

### 步驟1：選擇產品型別

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 在 _[!UICONTROL Add Product]_( ![選單箭頭](../assets/icon-menu-down-arrow-red.png){width="25"} )功能表，選擇 `Downloadable Product`.

   ![新增可下載的產品](./assets/product-add-downloadable.png){width="700" zoomable="yes"}

### 步驟2：選擇屬性集

範例資料包括 [屬性集](attribute-sets.md) 已呼叫 _可下載_ 具有可下載產品的特殊欄位。 您可以使用現有的範本，或在儲存產品之前建立另一個範本。

若要選擇用來作為產品範本的屬性集，請執行下列其中一項作業：

- 的 **[!UICONTROL Search]**，輸入屬性集的名稱。

- 在清單中，選擇 `Downloadable` 屬性集。

表單會更新以反映變更。

![選擇屬性集](./assets/product-create-choose-attribute-set-downloadable.png){width="600" zoomable="yes"}

### 步驟3：完成必要的設定

1. 輸入 **[!UICONTROL Product Name]**.

1. 接受預設值 **[!UICONTROL SKU]** 根據產品名稱或輸入其他名稱。

1. 輸入產品 **[!UICONTROL Price]**.

1. 由於產品尚未準備好發佈，請設定 **[!UICONTROL Enable Product]** 至 `No`.

1. 按一下 **[!UICONTROL Save]** 並繼續。

   儲存產品時， [存放區檢視](introduction.md#product-scope) 選擇器會出現在左上角。

1. 選擇 **[!UICONTROL Store View]** 產品可用的位置。

   ![選擇存放區檢視](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

### 步驟4：完成基本設定

1. 設定 **[!UICONTROL Tax Class]** 變更為下列其中一項：

   - `None`
   - `Taxable Goods`

1. 輸入 **[!UICONTROL Quantity]** 有庫存的產品的ID。

   請注意下列事項：

   - 根據預設， **[!UICONTROL Stock Status]** 設為 `Out of Stock`.

   - 由於可下載的產品尚未出貨，因此 **[!UICONTROL Weight]** 欄位未使用。 如果您啟用此功能，它就會變成 [簡單產品](product-create-simple.md) 和 _此產品是否可下載？_ 索引標籤無法使用。

   >[!NOTE]
   >
   >如果您啟用 [Inventory management](../inventory-management/introduction.md)，單一來源商家會設定本節中的數量。 多來源商家在「來源」區段中新增來源與數量。 請參閱下列內容 _指定來源與數量(Inventory management)_ 區段。

1. 接受預設值 **[!UICONTROL Visibility]** 設定 `Catalog, Search`.

1. 若要在中推出產品 [新產品清單](../content-design/widget-new-products-list.md)，選取 **[!UICONTROL Set Product as New]** 核取方塊。

1. 要指派 _[!UICONTROL Categories]_若要存取產品，請按一下&#x200B;**[!UICONTROL Select…]**方塊並執行下列任一項作業：

   **選擇現有類別**：

   - 開始在方塊中輸入內容，直到找到相符專案為止。

   - 選取要指派的每個類別的核取方塊。

   **建立類別**：

   - 按一下 **[!UICONTROL New Category]**.

   - 輸入 **[!UICONTROL Category Name]** 並選擇 **[!UICONTROL Parent Category]**，這會決定其在 [功能表結構](category-root.md).

   - 按一下 **[!UICONTROL Create Category]**.

1. 設定 **[!UICONTROL Format]** 變更為下列其中一項：

   - `Download`
   - `DVD`

   如有需要，您可以編輯 [屬性](attribute-product-create.md) 以新增更多值。

   可能有其他屬性可說明產品。 選取範圍會因屬性集而異，您稍後可以完成。

#### 指定來源與數量([!DNL Inventory Management])

{{$include /help/_includes/inventory-assign-sources.md}}

### 步驟5：完成可下載的資訊

向下捲動，展開 ![展開選擇器](../assets/icon-display-expand.png) 此 _[!UICONTROL Downloadable Information]_區段，並選取&#x200B;**[!UICONTROL Is this downloadable product?]**核取方塊。

啟用時， _[!UICONTROL Downloadable Information]_區段有兩個部分。 第一部分說明每個下載連結，第二部分說明每個範例檔案。 其中許多選項的預設值皆可在 [設定](#configure-the-download-options).

![可下載的資訊](./assets/product-downloadable-information.png){width="600" zoomable="yes"}

#### 完成連結

1. 在 _[!UICONTROL Links]_區段，輸入&#x200B;**[!UICONTROL Title]**要用作下載連結標題的專案。

1. 如果適用，請選取 **[!UICONTROL Links can be purchased separately]** 核取方塊。

1. 按一下 **[!UICONTROL Add Link]** 並執行下列動作：

   - 輸入 **[!UICONTROL Title]** 和 **[!UICONTROL Price]** 下載的。

   - 針對兩者 **[!UICONTROL File]** 和 **[!UICONTROL Sample]** 檔案時，選擇下列其中一種下載分發方法：

      - `Upload File`  — 選擇此方法，將散發檔案上傳至伺服器。 瀏覽至檔案並選取它以上傳。
      - `URL`  — 選擇此方法可從URL存取散發檔案。 輸入下載檔案的完整URL。

   >[!NOTE]
   >
   >您無法使用外部資源的連結作為可下載的產品。 有效的連結網域需以程式設計方式預先定義於 `env.php` 檔案(請參閱 [env.php參考](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/files/config-reference-envphp.html) 在 _設定指南_)。

   - 設定 **[!UICONTROL Shareable]** 變更為下列其中一項：

      - `No`  — 要求客戶登入其帳戶才能存取下載連結。

      - `Yes`  — 透過電子郵件傳送連結，以供客戶與其他人共用。

      - `Use Config`  — 使用中指定的方法 [可下載的產品選項](../configuration-reference/catalog/catalog.md) 設定。

   - 執行下列任一項作業：

      - 若要限制每位客戶的下載次數，請為 **[!UICONTROL Max. Downloads]**.
      - 若要允許無限制的下載，請選取 **[!UICONTROL Unlimited]** 核取方塊。

   ![連結詳細資料](./assets/product-downloadable-link-detail.png){width="600" zoomable="yes"}

1. 若要新增其他連結，請按一下 **[!UICONTROL Add Link]** 並重複這些步驟。

#### 完成範例

1. 在 _[!UICONTROL Samples]_區段，輸入&#x200B;**[!UICONTROL Title]**要用作範例標題的專案。

1. 若要完成每個範例的資訊，請按一下 **[!UICONTROL Add Link]**.

   ![範例](./assets/product-downloadable-samples.png){width="600" zoomable="yes"}

1. 依照以下步驟完成連結詳細資料：

   - 輸入 **[!UICONTROL Title]** 個別範例的。

   - 選擇下列其中一種分配方法：

      - `Upload File`  — 選擇此方法，將散發檔案上傳至伺服器。 瀏覽至檔案並選取它以上傳。
      - `URL`  — 選擇此方法可從URL存取散發檔案。 輸入下載檔案的完整URL。

   - 若要新增其他範例，請按一下 **[!UICONTROL Add Link]** 並重複這些步驟。

   - 若要變更範例的順序，請抓取 _變更順序_ ( ![位置控制器](../assets/icon-sort-order.png) )圖示並將範例拖曳到新位置。

### 步驟6：完成產品資訊

視需要向下捲動並填入下列章節中的資訊：

- [內容](product-content.md)
- [影像和影片](product-images-and-video.md)
- [搜尋引擎最佳化](product-search-engine-optimization.md)
- [相關產品、向上銷售和交叉銷售](related-products-up-sells-cross-sells.md)
- [可自訂的選項](settings-advanced-custom-options.md)
- [網站中的產品](settings-basic-websites.md)
- [設計](settings-advanced-design.md)
- [贈品選項](product-gift-options.md)

### 步驟7：發佈產品

如果您已準備好在目錄中發佈產品，請設定 **[!UICONTROL Enable Product]** 至 `Yes` 並執行下列任一項作業：

**方法1：** 儲存並預覽

- 在右上角，按一下 **[!UICONTROL Save]**.

- 若要檢視您商店中的產品，請選擇 **[!UICONTROL Customer View]** 於 _管理員_ ( ![選單箭頭](../assets/icon-menu-down-arrow-black.png) )功能表。

  該存放區會在新的瀏覽器標籤中開啟。

  ![客戶檢視](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

**方法2：** 儲存並關閉

在 _[!UICONTROL Save]_( ![選單箭頭](../assets/icon-menu-down-arrow-red.png){width="25"} )功能表，選擇&#x200B;**[!UICONTROL Save & Close]**.

## 店面體驗

在客戶帳戶控制面板中， _[!UICONTROL My Downloadable Products]_每個可下載產品訂單的頁面連結。 訂單完成時，便可從客戶帳戶取得下載內容。

![我的可下載產品](./assets/customer-account-my-downloadable-products.png){width="700" zoomable="yes"}

下表說明 _我的可下載產品_ 值：

| 欄 | 說明 |
|--- |--- |
| [!UICONTROL Order#] | 此 [訂購](../stores-purchase/orders.md) 購買可下載產品的位置。 提供訂單詳細資料的連結。 |
| [!UICONTROL Date] | 訂單建立日期。 |
| [!UICONTROL Title] | 與訂單一起購買的可下載產品名稱。 提供可下載產品的連結。 |
| [!UICONTROL Status] | 訂單處理狀態。 |
| [!UICONTROL Remaining Downloads] | 已下載產品的可用下載次數。 |

_**若要從帳戶儀表板下載產品檔案**_

1. 在其帳戶儀表板中，客戶選擇 **[!UICONTROL My Downloadable Products]**.

1. 尋找清單中的順序，然後按一下標題後面的連結。

1. 在下載視窗的右下角，按一下 _下載_ 圖示。

1. 將檔案儲存在其下載位置，並將檔案儲存到所需的位置。
