---
title: 『[!UICONTROL Sales] &gt； [!UICONTROL Sales]『
description: 檢閱上的組態設定 [!UICONTROL Sales] &gt； [!UICONTROL Sales] 商務管理員頁面。
exl-id: 29091aab-e608-4e68-a6fe-f2808c78581c
feature: Configuration, Orders
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '1066'
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Sales]

{{config}}

{{beta-updates}}

## [!UICONTROL General]

![一般](./assets/sales-general.png)<!-- zoom -->

<!-- [General](https://docs.magento.com/user-guide/marketing/sales-documents-ref-id.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Hide Customer IP] | 存放區檢視 | 決定客戶IP位址是否出現在訂單、商業發票、出貨及銷退折讓單上。 選項： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Checkout Totals Sort Order]

![結帳總計排序順序](./assets/sales-checkout-totals-sort-order.png)<!-- zoom -->

<!-- [Checkout Totals Sort Order](https://docs.magento.com/user-guide/sales/checkout-totals-sort-order.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Subtotal] | 網站 | 決定小計與其他結帳總計的計算時間數字。 預設值： `10` |
| [!UICONTROL Discount] | 網站 | 決定折扣何時計算與其他結帳總金額相關的數字。 預設值： `20` |
| [!UICONTROL Shipping] | 網站 | 決定與其他結帳總計相關時計算運費的數字。 預設值： `30` |
| [!UICONTROL Tax] | 網站 | 決定與其他結帳總計相關計算稅捐的數字。 預設值： `40` |
| [!UICONTROL Fixed Product Tax] | 網站 | 決定何時計算與其他結帳總計相關之固定產品稅捐的數字。 預設值： `50` |
| [!UICONTROL Grand Total] | 網站 | 決定總計與其他結帳總計之計算時間的數字。 預設值： `100` |

{style="table-layout:auto"}

## [!UICONTROL Reorder]

![重新排序](./assets/sales-reorder.png)<!-- zoom -->

<!-- [Reorder](https://docs.magento.com/user-guide/sales/reorders-allow.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Allow Reorder] | 存放區檢視 | 決定客戶是否可以從其帳戶重新排序。 選項： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Allow Zero Grand Total]

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Allow Zero Grand Total for Credit Memo] | 存放區檢視 | 決定以零總計建立銷退折讓單的可能性。 選項： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Invoice and Packing Slip Design]

![商業發票與裝箱單設計](./assets/sales-invoice-packing-slip-design.png)<!-- zoom -->

<!-- [Invoice and Packing Slip Design](https://docs.magento.com/user-guide/marketing/sales-document-pdf-logo.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Logo for PDF Print-outs] | 存放區檢視 | 識別出現在PDF發票與包裝單頁首的標誌檔案。 允許的檔案型別： <br/>JPG/JPEG <br/>TIF/TIFF <br/>PNG |
| [!UICONTROL Logo for HTML Print View] | 存放區檢視 | 識別出現在商業發票與包裝單HTML列印檢視表頭中的標誌檔案。 允許的檔案型別： <br/>JPG/JPEG <br/>GIF <br/>PNG |
| [!UICONTROL Address] | 存放區檢視 | 您要顯示在商業發票與包裝單上的商店地址。 |

{style="table-layout:auto"}

## [!UICONTROL Minimum Order Amount]

![最小訂購金額](./assets/sales-minimum-order-amount.png)<!-- zoom -->

<!-- [Minimum Order Amount](https://docs.magento.com/user-guide/sales/cart-minimum-order-amount.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable] | 網站 | 決定是否設定網站的最小訂單金額。 選項： `Yes` / `No` |
| [!UICONTROL Minimum Amount] | 網站 | 指定套用折扣後的最小小計、訂單。 |
| [!UICONTROL Include Discount Amount] | 網站 | 決定最小訂單金額是否包含套用的折扣。 選項： `Yes` / `No` |
| [!UICONTROL Include Tax to Amount] | 網站 | 決定最小訂單金額是否包含稅捐。 選項： `Yes` / `No` |
| [!UICONTROL Description Message] | 存放區檢視 | 決定當購物車總計小於最小訂購量時顯示在購物車頂端的訊息。 如果保留為空白，會顯示下列預設訊息： `Minimum order amount is $[minimum_amount]` |
| [!UICONTROL Error to Show in Shopping Cart] | 存放區檢視 | 決定當訂單量小於所需的最小訂單量時，從迷你購物車或結帳連結顯示的訊息。 如果保留為空白，則會顯示預設訊息。 |
| [!UICONTROL Validate Each Address Separately in Multi-address Checkout] | 網站 | 針對多料號訂單，會決定要分送地址的訂單料號是否大幅符合最小訂單金額。 選項： `Yes` / `No` |
| [!UICONTROL Multi-address Description Message] | 存放區檢視 | 針對多地址訂單，如果傳送至地址的專案小於最小訂購量，則會決定顯示在購物車中的訊息。 |
| [!UICONTROL Multi-address Error to Show in Shopping Cart] | 存放區檢視 | 針對多地址訂單，當訂單金額小於所需的最小訂單金額時，會決定從迷你購物車或結帳連結顯示的訊息。 如果保留為空白，則會顯示預設訊息。 |

{style="table-layout:auto"}

## [!UICONTROL Dashboard]

![儀表板](./assets/sales-dashboard.png)<!-- zoom -->

<!-- [Dashboard](https://docs.magento.com/user-guide/stores/admin-dashboard.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Use Aggregated Data] | 全域 | 決定是否使用即時彙總的銷售資料來產生儀表板快照報表。 如果您要處理大量資料，關閉即時資料的顯示可以改善效能。 選項： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Orders Cron Settings]

![訂單Cron設定](./assets/sales-orders-cron-settings.png)<!-- zoom -->

<!-- [Orders Cron Settings](https://docs.magento.com/user-guide/system/cron.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Pending Payment Order Lifetime] | 網站 | 決定擱置訂單的期限（分鐘）。 預設設定： `480` 分鐘（8小時） |

{style="table-layout:auto"}

## [!UICONTROL Gift Options]

![贈品選項](./assets/sales-gift-options.png)<!-- zoom -->

<!-- [Gift Options](https://docs.magento.com/user-guide/sales/gift-options.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Allow Gift Messages on Order Level] | 網站 | 指定是否可以為整個訂單新增禮品訊息。 |
| [!UICONTROL Allow Gift Messages on Order Items] | 網站 | 指定是否可以為個別訂單專案新增贈品訊息。 |
| [!UICONTROL Allow Gift Wrapping on Order Level] | 網站 | ![Adobe Commerce](../../assets/adobe-logo.svg) (僅限Adobe Commerce)指定是否可針對整張訂單新增贈品包裝。 |
| [!UICONTROL Allow Gift Wrapping for Order Items] | 網站 | ![Adobe Commerce](../../assets/adobe-logo.svg) (僅限Adobe Commerce)指定是否可以為個別訂購專案新增贈品包裝。 |
| [!UICONTROL Allow Gift Receipt] | 網站 | ![Adobe Commerce](../../assets/adobe-logo.svg) (僅限Adobe Commerce)指定是否可以為訂單新增禮品收據。 |
| [!UICONTROL Allow Printed Card] | 網站 | ![Adobe Commerce](../../assets/adobe-logo.svg) (僅限Adobe Commerce)指定是否可以為訂單新增列印卡片。 |
| [!UICONTROL Default Price for Printed Card] | 網站 | ![Adobe Commerce](../../assets/adobe-logo.svg) (僅限Adobe Commerce)指定列印卡片的預設價格。 |

{style="table-layout:auto"}

## [!UICONTROL Minimum Advertised Price]

![最低廣告價格](./assets/sales-minimum-advertised-price.png)<!-- zoom -->

<!-- [Minimum Advertised Price](https://docs.magento.com/user-guide/catalog/product-price-minimum-advertised.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable MAP] | 網站 | 為您的商店啟用最低廣告價格。 選項： `Yes` / `No` |
| [!UICONTROL Display Actual Price] | 網站 | 決定客戶看到產品實際價格的位置。 選項： <br/>**`In Cart`**— 顯示購物車中的實際產品價格。<br/>**`Before Order Confirmation`**  — 在訂單確認前，於結帳程式結束時顯示實際產品價格。 <br/>**`On Gesture`**— 當客戶按一下「價格點選」或「這是什麼？」時，在快顯視窗中顯示實際產品價格。 連結。 |
| [!UICONTROL Default Popup Text Message] | 存放區檢視 | 當客戶從分類清單或產品檢視頁面選取「按一下以取得價格」連結時顯示的文字訊息。 |
| [!UICONTROL Default "What's This" Text Message] | 存放區檢視 | 客戶按一下「這是什麼？」時顯示的文字訊息。 從產品檢視頁面連結。 |
| [!UICONTROL Manufacturer's Suggested Retail Price] | 全域 | 製造商建議的零售價(MSRP)。 |

{style="table-layout:auto"}

## [!UICONTROL Order by SKU Settings]

{{ee-feature}}

![依SKU設定排序](./assets/sales-order-by-sku-settings.png)<!-- zoom -->

<!-- [Order by SKU Settings](https://docs.magento.com/user-guide/customers/account-dashboard-order-by-sku.html) -->

![依客戶群組SKU設定排序](./assets/sales-order-by-sku-settings.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable Order by SKU on My Account in Storefront] | 網站 | 決定客戶帳戶儀表板中是否提供「依SKU排序」。 選項： <br/>**`Yes, for Everyone`**— 「依SKU排序」標籤會出現在所有客戶的帳戶控制面板中。<br/>**`Yes, for Specified Customer Groups`**  — 指定群組或共用目錄成員的帳戶控制面板中會顯示「依SKU排序」標籤。 <br/>**`No`**— 客戶帳戶中無法使用「依SKU排序」頁標。 |
| [!UICONTROL Customer Groups] | 網站 | 決定客戶群組。 選項： `General` / `Retailer` / `Wholesale` |

{style="table-layout:auto"}

## [!UICONTROL Instant Purchase]

![立即購買](./assets/sales-instant-purchase.png)<!-- zoom -->

<!-- [Instant Purchase](https://docs.magento.com/user-guide/sales/checkout-instant-purchase.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 存放區檢視 | 如果付款方式(例如Braintree)已啟用儲存庫，則為商店檢視啟用「立即購買」。 選項： `Yes` / `No` |
| [!UICONTROL Button Text] | 存放區檢視 | 指定立即購買按鈕上顯示的文字。 預設文字為 `Instant Purchase`. |

{style="table-layout:auto"}

## [!UICONTROL Orders, Invoices, Shipments, Credit Memos Archiving]

{{ee-feature}}

![訂單、商業發票、出貨、銷退折讓單存檔](./assets/sales-orders-invoices-shipments-credit-memos-archiving.png)<!-- zoom -->

如需有關變更這些設定的詳細資訊，請參閱 [設定訂單封存](../../stores-purchase/order-archive.md#configure-the-order-archive) 在 _商店和購買體驗指南_.

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable Archiving] | 全域 | 決定是否啟用封存。 選項： `Yes` / `No` |
| [!UICONTROL Archive Orders Purchased] | 全域 | 決定完成訂單存檔前的天數。 預設值： `30` |
| [!UICONTROL Order  Statuses to be Archived] | 全域 | 決定 [狀態](../../stores-purchase/order-status.md) 要封存的訂單數量。 依預設，系統會封存狀態為「完成」或「已結」的訂單。 選項： `Pending` / `Processing` / `Suspected Fraud` / `Complete` / `Closed` / `Canceled` / `On Hold` |

{style="table-layout:auto"}

## [!UICONTROL RMA Settings]

{{ee-feature}}

![RMA設定](./assets/sales-rma-settings.png)<!-- zoom -->

如需有關變更這些設定的詳細資訊，請參閱 [設定傳回](../../stores-purchase/rma-configure.md) 在 _商店和購買體驗指南_.

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable RMA on Storefront] | 網站 | 決定客戶是否可以從店面建立和檢視RMA請求。 RMA可同時套用至新訂單與現有訂單。 依預設，店面不會啟用RMA。 選項： `Yes` / `No` |
| [!UICONTROL Enable RMA on Product Level] | 網站 | 決定產品資訊中「啟用RMA」欄位的預設值。 |
| [!UICONTROL Use Store Address] | 網站 | 決定用於退回商品出貨的聯絡人名稱與地址。 選項： <br/>**`Yes`**— 使用 [原點](../../stores-purchase/shipping-settings.md#point-of-origin) 來自「送貨設定」的地址。<br/>**`No`**  — 開啟地址表單，以便輸入替代地址。 |

{style="table-layout:auto"}
