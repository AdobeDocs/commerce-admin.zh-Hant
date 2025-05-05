---
title: 依SKU排序
description: 瞭解如何設定您的商店，方便客戶透過SKU訂購。
exl-id: cb39554f-ab76-46d5-8217-e43bc8f9f88d
feature: Orders, Storefront, Configuration
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 0%

---

# 依SKU排序

{{ee-feature}}

「SKU」是「庫存單位」。 SKU通常可協助線上賣家識別最重要的產品特性，例如：大小、顏色、價格和材質。 產品ID與SKU不同：

- `Product ID`為內部用於識別產品的連續數字序列，不適用於客戶。
- `SKU`由賣家產生，通常根據行銷或內部追蹤的產品名稱和屬性。 例如：藍色棉色T恤，中號尺寸：T-COT-MED-BL。 如有需要，賣方可能會變更SKU。

通常，SKU會包含一組縮寫，指出產品的不同特徵。 SKU長度上限為64個字元。 SKU對於有效追蹤及管理詳細目錄非常重要，因此正確設定它們對於電子商務至關重要。

_Order by SKU_&#x200B;是[Widget](../content-design/widgets.md)，可在商店中顯示，方便所有購物者，或僅供特定客戶群組的購物者使用。 購物者可以直接在「依SKU訂購」區塊中輸入SKU和數量資訊，或是從其客戶帳戶上傳csv檔案。 無論設定為何，儲存管理員一律可以依據SKU排序。

![在店面中由SKU訂購](./assets/storefront-order-by-sku.png){width="700" zoomable="yes"}

## 依SKU設定訂單

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Sales]**&#x200B;區段並在下方選擇&#x200B;**[!UICONTROL Sales]**。

1. 展開&#x200B;**[!UICONTROL Order by SKU Settings]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

1. 將&#x200B;**[!UICONTROL Enable Order by SKU on my Account in Storefront]**&#x200B;設定為下列其中一項：

   - `Yes, for Everyone` — 每個購物者皆可在商店中使用Order by SKU區塊。
   - `Yes, for Specified Customer Groups` - Order by SKU僅適用於特定客戶群組（例如`Wholesale`）的成員。
   - `No` — 「依SKU訂購」區塊未出現在店面，且「依SKU訂購」頁面在客戶帳戶中無法使用。

   ![依SKU設定排序](../configuration-reference/sales/assets/sales-order-by-sku-settings.png){width="600" zoomable="yes"}

1. 按一下&#x200B;**[!UICONTROL Save Config]**。

![Adobe Commerce B2B](../assets/b2b.svg) (僅限Adobe Commerce B2B) _&#x200B;**若要啟用Order by SKU功能，請停用Quick Order功能：**&#x200B;_

1. 前往&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左面板&#x200B;_[!UICONTROL General]_&#x200B;下，選擇&#x200B;**[!UICONTROL B2B Features]**

1. 展開&#x200B;**[!UICONTROL B2B Features]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

1. 將&#x200B;**[!UICONTROL Enable Quick Order]**&#x200B;設為`No`。

   [快速訂購功能](../b2b/quick-order.md)可讓客戶和來賓根據SKU或產品名稱快速下訂單。

## 店面體驗

當針對商店設定功能時，客戶可以從任何包含&#x200B;_Order by SKU_ Widget的頁面或其帳戶儀表板透過SKU訂購。

### 從頁面區塊依SKU排序

1. 在&#x200B;_Order by SKU_&#x200B;區塊中，客戶輸入要訂購的專案的&#x200B;**[!UICONTROL SKU]**&#x200B;與&#x200B;**[!UICONTROL Qty]**。

1. 若要新增其他專案，請按一下&#x200B;**[!UICONTROL Add Row]**&#x200B;並重複此程式。

1. 按一下&#x200B;**[!UICONTROL Add to Cart]**。

### 客戶帳戶的SKU訂單

1. 客戶從店面登入其帳戶。

1. 在左側的面板中，選擇&#x200B;**[!UICONTROL Order by SKU]**。

1. 根據偏好設定新增個別專案：

   _&#x200B;**依SKU新增每個專案：**&#x200B;_

   - 輸入要訂購的專案的&#x200B;**[!UICONTROL SKU]**&#x200B;與&#x200B;**[!UICONTROL Qty]**。

   - 若要視需要新增其他專案，請按一下&#x200B;_新增列_ ![加號按鈕](../assets/button-add-item.png)，然後視需要重複多個專案。

   - 按一下&#x200B;**[!UICONTROL Add to Cart]**。

   _&#x200B;**上傳包含多個專案的CSV檔案：**&#x200B;_

   - 準備包含`SKU`與`Qty`欄的[匯入資料CSV](../systems/data-csv.md) （逗號分隔值）檔案。

   要匯入的![SKU](./assets/account-dashboard-order-by-sku-import.png){width="500" zoomable="yes"}

   - 若要上傳CSV檔案，請按一下&#x200B;**[!UICONTROL Choose File]**&#x200B;並選取要上傳的檔案。

   - 按一下&#x200B;**[!UICONTROL Add to Cart]**。

   如果有任何產品有其他選項，則會從購物車提示客戶，告知產品需要注意。

   ![產品需要注意](./assets/account-dashboard-order-by-sku-cart-product-requires-attention.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >如果有重複的SKU，數量會合併至購物車中的一個條列專案。 客戶可以變更任何專案的數量，然後按一下&#x200B;**[!UICONTROL Update Shopping Cart]**&#x200B;以重新計算總計。

