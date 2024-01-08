---
title: 禮卡產品
description: 瞭解如何建立禮品卡產品，該產品會產生唯一代碼，以供收件者客戶在結帳時兌換。
exl-id: bc4b60fe-10b3-4d17-85ce-35c2720c90a2
feature: Catalog Management, Products, Gift
source-git-commit: e72977596c4479d2e94b1e066ee166d22cb12405
workflow-type: tm+mt
source-wordcount: '962'
ht-degree: 0%

---

# 禮卡產品

{{ee-feature}}

每個禮品卡都有唯一代碼，在結帳時僅能由一位客戶兌換。 A [程式碼集區](../stores-purchase/product-gift-card-accounts.md#step-3-establish-the-gift-card-code-pool) 必須先建立才能銷售禮品卡。 另請參閱 [禮卡工作流程](../stores-purchase/product-gift-card-workflow.md) 有關如何兌換購物車中禮品卡的資訊。

![禮卡產品頁面](./assets/storefront-giftcard-product-page.png){width="700" zoomable="yes"}

禮卡產品有三種：

- **虛擬**  — 虛擬禮品卡會傳送至收件者的電子郵件地址，這是購買禮品卡時所需的電子郵件地址。 不需要送貨地址。

- **實體**  — 實體禮卡會運送至收件者的地址，在購買禮卡時需使用此地址。

- **已合併**  — 合併的禮品卡已出貨，並透過電子郵件傳送給收件者。 購買禮品卡時，需要收件者的電子郵件和送貨地址。

## 建立禮品卡產品

下列指示示範使用建立禮卡的過程 [產品範本](attribute-sets.md)、必填欄位和基本設定。 每個必填欄位都標有紅色星號(`*`)。 當您完成基本功能後，您可以視需要完成其他產品設定。

### 步驟1：選擇產品型別

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 在右上角 _[!UICONTROL Add Product]_( ![選單箭頭](../assets/icon-menu-down-arrow-red.png){width="25"}  )功能表，選擇&#x200B;**[!UICONTROL Gift Card]**.

   ![新增禮品卡](./assets/product-add-gift-card.png){width="700" zoomable="yes"}

### 步驟2：選擇屬性集

您可以使用預設值 `Gift Card` 屬性集或選擇其他屬性。 若要選擇用來作為產品範本的屬性集，請執行下列其中一項作業：

- 按一下 **[!UICONTROL Attribute Set]** 欄位並輸入屬性集的全部或部分名稱。

- 在顯示的清單中，選擇要使用的屬性集。

![選擇屬性集](./assets/product-create-choose-attribute-set-gift-card.png){width="600" zoomable="yes"}

### 步驟3：完成必要的設定

1. 輸入 **[!UICONTROL Product Name]** 作為禮品卡。

   您也可以在名稱中指明禮品卡的型別。 例如， _Luma虛擬禮品卡_.

1. 輸入 **[!UICONTROL SKU]** 用於產品。

   依預設，「產品名稱」會用作預設SKU。

1. 設定 **[!UICONTROL Card Type]** 變更為下列其中一項：

   - `Virtual`  — 虛擬禮品卡會透過電子郵件傳送給收件者。
   - `Physical`  — 實體禮品卡可以預先大量生產，並使用唯一代碼進行浮雕。
   - `Combined`  — 組合式禮卡兼具虛擬和實體禮卡兩種特色。

   ![禮卡型別](./assets/product-create-gift-card-type.png){width="600" zoomable="yes"}

1. 若要讓客戶選擇固定金額，請按一下 **[!UICONTROL Add Amount]** 並輸入卡片的第一個固定值作為小數。

   若要輸入固定金額的選擇，請對每個重複此步驟。

1. 若要讓客戶能夠設定禮品卡的價值，請執行下列步驟：

   - 設定 **[!UICONTROL Open Amount]** 至 `Yes`.

   - 若要定義最小與最大可接受值的範圍，請輸入 **[!UICONTROL Open Amount From]** 和 **[!UICONTROL To]** 值。

   您可以建立固定訂價、未結金額訂價或兩者的禮品卡。

   >[!NOTE]
   >
   >禮品卡產品在目錄中沒有自己的價格。 禮品卡價格是從購買期間所選取的禮品卡金額衍生而得。

   ![禮卡金額](./assets/product-create-gift-card-amounts.png){width="600" zoomable="yes"}

### 步驟4：完成基本設定

1. 對於實體或組合禮品卡，請輸入 **[!UICONTROL Quantity]** 有庫存。

1. 如果要出貨的禮品卡，請輸入 **[!UICONTROL Weight]** 封裝的。

1. 在 **[!UICONTROL Categories]** 欄位，選擇 `Gift Card`.

可能有其他個別屬性可說明產品。 選取範圍會改變屬性集，您稍後可以完成它們。

### 步驟5：完成禮卡資訊

此 _[!UICONTROL Gift Card Information]_區段的「產品設定」可用來覆寫 [禮品卡設定](../configuration-reference/sales/gift-cards.md) 決定卡片管理方式的設定。

1. 向下捲動至 _[!UICONTROL Gift Card Information]_區段。

   此段落中的預設設定由系統組態決定。

   ![禮卡資訊](./assets/product-gift-card-information.png){width="600" zoomable="yes"}

1. 根據您想要的禮品卡運作方式變更其他欄位：

   - **[!UICONTROL Treat Balance as Store Credit]**  — 決定禮品卡持有人是否可將餘額兌換為商店貸方。

   - **[!UICONTROL Lifetime (days)]**  — 決定購買後到禮品卡過期的天數。 如果您不想設定卡片存留期的限制，請將此欄位留空。

   - **[!UICONTROL Allow Message]**  — 決定禮品卡的購買者是否可以為收件者輸入訊息。 虛擬（電子郵件）和實體（出貨）禮品卡都可以包含禮品訊息。

   - **[!UICONTROL Email Template]**  — 決定傳送給禮品卡收件者的通知所使用的電子郵件範本。

### 步驟6：完成產品資訊

視需要填寫下列章節中的資訊：

- [內容](product-content.md)
- [影像和影片](product-images-and-video.md)
- [相關產品、向上銷售和交叉銷售](related-products-up-sells-cross-sells.md)
- [搜尋引擎最佳化](product-search-engine-optimization.md)
- [可自訂的選項](settings-advanced-custom-options.md)
- [網站中的產品](settings-basic-websites.md)
- [設計](settings-advanced-design.md)
- [贈品選項](product-gift-options.md)

### 步驟7：發佈產品

1. 如果您已準備好在目錄中發佈產品，請設定 **啟用產品** 切換至 `Yes`.

1. 執行下列任一項作業：

   **方法1：** 儲存並預覽

   - 在右上角，按一下 **[!UICONTROL Save]**.

   - 若要檢視您商店中的產品，請選擇 **[!UICONTROL Customer View]** 於 _管理員_ ( ![選單箭頭](../assets/icon-menu-down-arrow-black.png) )功能表，

   ![客戶檢視](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   **方法2：** 儲存並關閉

   在 _[!UICONTROL Save]_( ![選單箭頭](../assets/icon-menu-down-arrow-red.png){width="25"} )功能表，選擇&#x200B;**[!UICONTROL Save & Close]**.

## 注意事項

- A _程式碼集區_ 必須產生唯一編號的組合，才能提供禮卡銷售。

- 禮品卡可以設為 `Redeemable` 或 `Non-Redeemable`.

- 稅金為 **_未套用_** 在禮卡購買期間轉換到禮卡。 只有當購買的禮品卡是用來購買產品時，才會對產品徵稅。

- 禮品卡的存留期可以不受限制，或設為指定的天數。

- 禮卡值可以設定為固定金額，或設定為最小值和最大值之未結金額。

- 禮品卡產品在目錄中沒有自己的價格。 禮品卡價格是從購買期間所選取的禮品卡金額衍生而得。

- 您可以在下訂單或開立商業發票時，建立客戶的禮品卡帳戶。
