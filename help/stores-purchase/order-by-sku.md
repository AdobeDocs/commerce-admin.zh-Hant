---
title: 依SKU排序
description: 瞭解如何設定您的商店，方便客戶透過SKU訂購。
exl-id: cb39554f-ab76-46d5-8217-e43bc8f9f88d
feature: Orders, Storefront, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '589'
ht-degree: 0%

---

# 依SKU排序

{{ee-feature}}

「SKU」是「庫存單位」。 SKU通常可協助線上賣家識別最重要的產品特性，例如：大小、顏色、價格和材質。 產品ID與SKU不同：

- 此 `Product ID` 是內部使用的連續數字，用於識別產品且不可供客戶使用。
- 此 `SKU` 由賣方產生，通常根據用於行銷或內部追蹤的產品名稱和屬性。 例如：藍色棉色T恤，中號尺寸：T-COT-MED-BL。 如有需要，賣方可能會變更SKU。

通常，SKU會包含一組縮寫，指出產品的不同特徵。 SKU長度上限為64個字元。 SKU對於有效追蹤及管理詳細目錄非常重要，因此正確設定它們對於電子商務至關重要。

_依SKU排序_ 是 [Widget](../content-design/widgets.md) 這些區段可在商店中顯示，方便所有購物者，或僅供特定客戶群組的購物者使用。 購物者可以直接在「依SKU訂購」區塊中輸入SKU和數量資訊，或是從其客戶帳戶上傳csv檔案。 無論設定為何，儲存管理員一律可以依據SKU排序。

![店面中依SKU訂購](./assets/storefront-order-by-sku.png){width="700" zoomable="yes"}

## 依SKU設定訂單

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Sales]** 區段並選擇 **[!UICONTROL Sales]** 底下。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Order by SKU Settings]** 區段。

1. 設定 **[!UICONTROL Enable Order by SKU on my Account in Storefront]** 變更為下列其中一項：

   - `Yes, for Everyone`  — 商店中可供每位購物者使用Order by SKU區塊。
   - `Yes, for Specified Customer Groups`  — 依SKU排序僅適用於特定客戶群組的成員，例如 `Wholesale`.
   - `No`  — 店面中不會顯示「依SKU排序」區塊，客戶帳戶中也不會提供「依SKU排序」頁面。

   ![依SKU設定排序](../configuration-reference/sales/assets/sales-order-by-sku-settings.png){width="600" zoomable="yes"}

1. 按一下 **[!UICONTROL Save Config]**.

![適用於Adobe Commerce的B2B](../assets/b2b.svg) (B2B僅適用於Adobe Commerce) _**若要啟用「依SKU排序」功能，請停用「快速排序」功能：**_

1. 前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中的 _[!UICONTROL General]_，選擇&#x200B;**[!UICONTROL B2B Features]**

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL B2B Features]** 區段。

1. 設定 **[!UICONTROL Enable Quick Order]** 至 `No`.

   此 [快速訂購功能](../b2b/quick-order.md) 可讓客戶和來賓根據SKU或產品名稱快速下訂單。

## 店面體驗

當針對商店設定功能時，客戶可以從任何包含 _依SKU排序_ Widget或其帳戶儀表板中的。

### 從頁面區塊依SKU排序

1. 在 _依SKU排序_ 區塊，客戶進入 **[!UICONTROL SKU]** 和 **[!UICONTROL Qty]** 訂購專案的URL。

1. 若要新增其他專案，請按一下 **[!UICONTROL Add Row]** 並重複此程式。

1. 點擊數 **[!UICONTROL Add to Cart]**.

### 客戶帳戶的SKU訂單

1. 客戶從店面登入其帳戶。

1. 在左側的面板中，選擇 **[!UICONTROL Order by SKU]**.

1. 根據偏好設定新增個別專案：

   _**依SKU新增每個專案：**_

   - 輸入 **[!UICONTROL SKU]** 和 **[!UICONTROL Qty]** 訂購專案的URL。

   - 若要視需要新增其他專案，請按一下 _新增列_ ![加號按鈕](../assets/button-add-item.png) 並視需要重複以上專案。

   - 點擊數 **[!UICONTROL Add to Cart]**.

   _**上傳包含多個專案的CSV檔案：**_

   - 準備 [匯入資料CSV](../systems/data-csv.md) （逗號分隔值）包含下列專案的欄的檔案： `SKU` 和 `Qty`.

   ![要匯入的SKU](./assets/account-dashboard-order-by-sku-import.png){width="500" zoomable="yes"}

   - 若要上傳CSV檔案，請按一下 **[!UICONTROL Choose File]** 並選取要上傳的檔案。

   - 點擊數 **[!UICONTROL Add to Cart]**.

   如果有任何產品有其他選項，則會從購物車提示客戶，告知產品需要注意。

   ![產品需要注意](./assets/account-dashboard-order-by-sku-cart-product-requires-attention.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >如果有重複的SKU，數量會合併至購物車中的一個條列專案。 客戶可以變更任何料號的數量，然後按一下 **[!UICONTROL Update Shopping Cart]** 以重新計算總計。

