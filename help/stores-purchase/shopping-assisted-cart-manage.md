---
title: 管理購物車
description: 瞭解如何直接從管理員協助客戶處理購物車。
exl-id: beb41dfa-ef87-4065-96fd-0649a5c4c21c
feature: Customer Service, Shopping Cart
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 1%

---

# 管理購物車

{{ee-feature}}

若要開始輔助購物工作階段，客戶必須從店面登入其帳戶才能取得資訊。 如果客戶沒有帳戶，您可以 [建立一個](../customers/account-create.md).

![客戶帳戶中的購物車](./assets/customer-account-manage-cart-items.png){width="600" zoomable="yes"}

## 動作控制

| 選項 | 說明 |
|--- |--- |
| [!UICONTROL Remove] | 從目前的購物車移除專案 |
| [!UICONTROL Move to Wish List] | 將專案移至選取的客戶願望清單 |

{style="table-layout:auto"}

## 控制按鈕

| 按鈕 | 說明 |
|--- |--- |
| [!UICONTROL Clear my shopping cart] | 清除所有產品中的目前購物車。 |
| [!UICONTROL Update Items and Quantities|]在「 」中輸入所需數量 **[!UICONTROL Qty]** 欄位並更新購物車中的專案數。 |
| [!UICONTROL Add selections to my cart] | 將所有區段的產品新增至購物車。 |

{style="table-layout:auto"}

## 驗證客戶是否已登入

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Customers]** > **[!UICONTROL Now Online]**.

   所有商店訪客和登入客戶都會出現在清單中。

   ![客戶現已上線](./assets/customers-now-online.png){width="700" zoomable="yes"}

## 優惠方案輔助購物

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. 在清單中，以編輯模式開啟客戶記錄。

   >[!TIP]
   >
   >若要快速找到客戶記錄，請使用 [篩選器](../getting-started/admin-grid-controls.md) 控制。

   在客戶設定檔中的 _[!UICONTROL Personal Information]_，則_[!UICONTROL Last Logged In]_ 日期和時間顯示客戶已上線。

   ![線上客戶的客戶設定檔](./assets/customer-account-manage-cart.png){width="600" zoomable="yes"}

1. 若要進入輔助購物模式，請按一下 **[!UICONTROL Manage Shopping Cart]** 頂端按鈕列中的。

   ![輔助購物模式](./assets/customer-manage-shopping-cart.png){width="600" zoomable="yes"}

## 依屬性將產品新增至購物車

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Products]** 區段。

1. 使用每一欄頂端的任一篩選器來尋找產品。

1. 按一下 **[!UICONTROL Search]**.

1. 根據產品型別，使用下列其中一個步驟：

### 新增簡單產品

1. 按一下您要訂購的產品。

   此動作會選取記錄並設定 **[!UICONTROL Quantity]** 至的預設值 `1`.

1. 如有必要，請更新訂購數量。

1. 在格線左上方，按一下 **[!UICONTROL Add selections to my cart]**.

   ![新增產品至購物車](./assets/customer-account-manage-cart-order-products.png){width="600" zoomable="yes"}

   條列專案會新增至頁面頂端的購物車。

   ![購物車已更新](./assets/customer-account-manage-cart-update-cart.png){width="600" zoomable="yes"}

### 新增產品與設定

在新增到購物車之前，必須設定三種型別的產品： `Bundle Product`， `Configurable Product`、和 `Grouped Product`.

1. 在格線中，按一下 **[!UICONTROL Configure]** 產品名稱旁。

   ![設定產品](./assets/customer-account-manage-cart-order-configurable-product.png){width="600" zoomable="yes"}

1. 在 _關聯的產品_ 對話方塊中，選擇每個產品選項來說明要訂購的料號，然後輸入 **[!UICONTROL Quantity]**，然後按一下 **[!UICONTROL OK]**.

   以核取記號選取產品，且訂購數量會顯示在格線中。

1. 若要將產品加入購物車，請按一下 **[!UICONTROL Add selections to my cart]**.

   ![購物車中的可設定產品](./assets/customer-account-manage-cart-order-configurable-product-cart.png){width="600" zoomable="yes"}

1. 視需要更新購物車中的產品選項：

   - 按一下 **[!UICONTROL Configure]**.

   - 更新選項，然後按一下 **[!UICONTROL OK]**.

## 依SKU新增產品

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Add to Shopping Cart by SKU]** 區段。

1. 個別新增產品依據 **[!UICONTROL SKU]** 或透過上傳CSV檔案來新增產品。

### 依SKU個別新增專案

1. 輸入 **[!UICONTROL SKU]** 和 **[!UICONTROL Qty]** 訂購專案的URL。

1. 若要訂購其他產品，請按一下 **[!UICONTROL Add another]**.

   ![依SKU新增產品](./assets/customer-account-manage-cart-order-product-by-sku.png){width="600" zoomable="yes"}

1. 按一下 **[!UICONTROL Add selections to my cart]**.

1. 如果專案是可設定的產品，請在提示時選擇產品選項，然後按一下 **[!UICONTROL Add to Shopping Cart]**.

### 透過上傳CSV檔案來新增產品

1. 準備 [csv檔案](../systems/data-csv.md) ，並將專案新增至購物車。

   檔案只能包含兩欄，其中 `sku` 和 `qty` 在標題中。

1. 上傳準備的檔案：

   - 按一下 **[!UICONTROL Choose File]**.

   - 選取要從目錄中上傳的檔案。

## 轉移專案

您可以從客戶的願望清單以及最近檢視、比較或訂購的專案，將專案轉移至購物車。 每個區段中的專案數會顯示在區段標題後面的括弧中。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 下列其中一節：

   - [!UICONTROL Wish List]
   - [!UICONTROL Products in the Comparison List]
   - [!UICONTROL Recently Compared Products]
   - [!UICONTROL Recently Viewed Products]
   - [!UICONTROL Last Ordered Items]

1. 在方格中，選取要訂購的每一件產品，並輸入 **[!UICONTROL Quantity]**.

1. 若要輸入可設定產品的選項，請按一下 **[!UICONTROL Configure]** 並視需要設定產品選項。

1. 按一下 **[!UICONTROL Add selections to my cart]**.

1. 套用優惠券代碼（如果可用）：

   - 的 **[!UICONTROL Apply Coupon Code]**，請輸入有效的抵用券代碼。

   - 按一下 _套用_ ( ![箭頭圖示](../assets/icon-apply-arrow.png) )箭頭。

1. 視需要調整訂購數量：

   - 在 **[!UICONTROL Qty]** 要調整之產品的欄位，請輸入正確的金額。

   - 按一下 **[!UICONTROL Update Items and Quantities]**.

## 建立訂單

1. 按一下 **[!UICONTROL Create Order]**.

   此 _[!UICONTROL Create New Order]_頁面會顯示購物車中的專案，以及運送和付款資訊。

1. 填寫運送與付款資訊。

1. 按一下 **[!UICONTROL Submit Order]**.

若要深入瞭解，請參閱 [建立訂單](customer-account-create-order.md).
