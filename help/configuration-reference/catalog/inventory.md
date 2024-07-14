---
title: '[!UICONTROL Catalog] &amp；gt； [!UICONTROL Inventory]'
description: 檢閱Commerce管理員的[!UICONTROL Catalog] &amp；gt； [!UICONTROL Inventory]頁面上的組態設定。
exl-id: 80113a31-3585-4ee1-95af-31efc09389eb
feature: Configuration, Inventory
source-git-commit: 768c9fdc37127b408230983e39e98b11149713a7
workflow-type: tm+mt
source-wordcount: '1195'
ht-degree: 0%

---

# [!UICONTROL Catalog] > [!UICONTROL Inventory]

{{config}}

>[!NOTE]
>
>適用於Adobe Commerce和Magento Open Source的[!DNL Inventory Management]提供您管理產品詳細目錄的工具。 擁有單一商店到多個倉庫、商店、取貨地點、卸貨託運人等等的商家，可以使用這些功能來維護銷售數量，並處理出貨以完成訂單。 如需這些功能以及如何使用這些功能來管理多個位置中的庫存的詳細資訊，請參閱[_[!DNL Inventory Management]使用手冊&#x200B;_](https://experienceleague.adobe.com/docs/commerce-admin/inventory/introduction.html)。

## [!UICONTROL Stock Options]

![股票期權](./assets/catalog-inventory-stock-options.png)<!-- zoom -->

<!-- [Stock Options](https://docs.magento.com/user-guide/catalog/inventory-options-global.html) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Decrease Stock When Order is Placed] | 全域 | 如果設為`Yes`，會在下訂單時減少庫存數量。 啟用&#x200B;_管理存貨_&#x200B;後，會輸入訂購產品與數量的預留。 選項： `Yes` / `No` |
| [!UICONTROL Set Items' Status to be in Stock When Order is Cancelled] | 存放區檢視 | 若設為`Yes`，則取消訂單時會將專案退回存貨。 啟用&#x200B;_管理存貨_&#x200B;後，已取消產品與數量的預訂會被清除。 選項： `Yes` / `No` |
| [!UICONTROL Display Out of Stock Products] | 全域 | 如果設為`Yes`，會顯示無庫存的產品。 如果產品警報也啟用，客戶可以註冊以在產品上市時收到通知。 選項： `Yes` / `No` |
| [!UICONTROL Only X left Threshold] | 網站 | 建立`Only x left`訊息的臨界值。 例如，如果設為3，當庫存中有三個或更少專案時，訊息便會出現。 如果值設為`0`，則不會顯示訊息。 |
| [!UICONTROL Display products availability in Stock on Storefront] | 存放區檢視 | 若設為`Yes`，會在產品頁面上顯示`In Stock`或`Out of Stock`訊息。 選項： `Yes` / `No` |
| [!UICONTROL Enable Inventory Check On Cart Load] | 全域 | 決定在購物車中載入產品時是否執行庫存檢查。 停用此詳細目錄檢查可改善結帳步驟的效能，尤其是購物車中有許多專案時。 但是，如果您略過預先驗證，客戶稍後在結帳程式中可能會看到&#x200B;_缺貨_&#x200B;錯誤。 選項： `Yes` / `No` |
| [!UICONTROL Synchronize with Catalog] | 全域 | 設定為`Yes`時，庫存資料會根據目錄變更（例如產品移除、產品SKU變更和產品型別變更）進行調整，並保持庫存與目錄的一致性。 選項： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Product Stock Options]

![產品庫存選項](./assets/catalog-inventory-product-stock-options.png)<!-- zoom -->

<!-- [Product Stock Options](https://docs.magento.com/user-guide/catalog/inventory-options-global.html) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Manage Stock] | 全域 | 決定您是否使用完整存貨控制來管理目錄中的料號。 選項： <br/>**是** — 啟用完整存貨控制以追蹤目前庫存中的專案數。 <br/>**否** — 不追蹤目前庫存中的專案數。 |
| [!UICONTROL Backorders] | 全域 | 決定商店管理延期交貨的方式。 延交訂單不會變更訂單的處理狀態。 無論產品是否有庫存，下訂單時仍會立即授權或擷取資金。 當產品可供使用時，即會出貨。 選項： <br/>**沒有延期交貨** — 產品無庫存時，不接受延期交貨。 <br/>**允許數量低於0** — 當數量低於零時接受延期交貨。 <br/>**允許數量低於0並通知客戶** — 在數量低於零時接受延期交貨，但通知客戶仍然可以下訂單。 |
| [!UICONTROL Use deferred Stock update] | 全域 | ![Adobe Commerce](../../assets/adobe-logo.svg) (僅限Adobe Commerce)若允許延期交貨，決定是否延遲庫存更新（_延期交貨_&#x200B;選項已設定為`No backorders`預設值以外的任何專案）。 它適用於單一產品或整個網站，並使用&#x200B;_工作佇列_&#x200B;機制來允許存貨數量指標在訂購後以非同步方式更新。 此選項也可搭配[非同步訂購](https://experienceleague.adobe.com/docs/commerce-operations/performance-best-practices/high-throughput-order-processing.html#asynchronous-order-placement)和[Inventory management](../../inventory-management/introduction.md)使用。 |
| 購物車中允許的最大數量 | 全域 | 決定單一訂單可購買的最大產品數量。 依預設，最大數量設為10,000。 |
| [!UICONTROL Out-of-Stock Threshold] | 全域 | 決定產品被視為無庫存的庫存水準。 選項： <br/>**正金額** — 停用&#x200B;_延期交貨_&#x200B;時，請輸入正金額。 啟用「延期交貨」時，此金額會被忽略。 <br/>**零** — 啟用&#x200B;_延期交貨_，輸入`0`可允許無限延期交貨。 <br/>**負數金額** — 啟用&#x200B;_延期交貨_&#x200B;時，我們建議您輸入負數金額。 此金額會新增至「可銷售數量」。 例如，輸入–50以允許此金額以下的訂單。 |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | 全域 | 根據客戶群組決定可供採購的料號最小金額。 依預設，最小數量設為1。 按一下&#x200B;**[!UICONTROL Add Minimum Qty]**&#x200B;為特定客戶群組輸入不同的值。 |
| [!UICONTROL Notify for Quantity Below] | 全域 | 決定傳送通知的存貨層次，存貨已低於臨界值。 |
| [!UICONTROL Enable Qty Increments] | 全域 | 決定料號是否可以數量遞增方式出售。 選項： `Yes` / `No` |
| [!UICONTROL Qty Increments] | 全域 | 建立構成數量增量的產品數量。 |
| [!UICONTROL Automatically Return Credit Memo Item to Stock] | 全域 | 決定是否自動將銷退折讓單中包含的料號退回存貨。 選項： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Admin Bulk Operations]

![管理員大量作業](./assets/catalog-inventory-admin-bulk-operations.png)<!-- zoom -->

<!-- [Admin Bulk Operations](https://docs.magento.com/user-guide/catalog/inventory-options-global.html) -->

>[!NOTE]
>
>若要設定並支援&#x200B;**非同步佇列管理員**，您必須使用命令列。 這可能需要開發人員協助。 請參閱&#x200B;_設定指南_&#x200B;中的[開始訊息佇列消費者](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html)。

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Run asynchronously] | 全域 | 決定您是否以非同步方式執行大量產品動作，包括[批次](../../inventory-management/bulk-assignment.md)指派來源、取消指派來源，以及[將存貨轉移至來源](../../inventory-management/inventory-transfer.md)。 它會收集最多&#x200B;_[!UICONTROL Asynchronous batch size]_個大量動作，然後執行這些動作。 此功能預設為停用。 我們建議您在啟用前先檢閱大量動作的效能。 選項：<br/>**`Yes`**— 非同步執行[!DNL Inventory Management]的所有大量作業。 若要啟用，您必須設定非同步佇列管理員。<br/>**`No`**— 預設。 不會以非同步方式執行大量作業。 |
| [!UICONTROL Asynchronous batch size] | 全域 | 將&#x200B;**[!UICONTROL Run asynchronously]**&#x200B;設為`Yes`以輸入&#x200B;_[!UICONTROL Asynchronous batch size]_欄位的值。 <br/>預設批次大小為100。 當大量程式達到此數量時，就會執行。 |

{style="table-layout:auto"}

## [!UICONTROL Inventory Indexer Settings]

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Stock/Source reindex strategy] | 全域 | 決定用於庫存/來源重新索引的策略。 選項： `Synchronous` / `Asynchronous` （必須為非同步模式設定非同步佇列管理員） |

{style="table-layout:auto"}

>[!NOTE]
>
> 由於訂單相關活動的存貨更新相依性，無論`Synchronous`或`Asynchronous`設定為何，產品儲存時也會觸發存貨索引器。


## [!UICONTROL Distance Provider for Distance Based SSA]

以距離為基礎的SSA的![距離提供者](./assets/catalog-inventory-distance-provider.png)<!-- zoom -->

<!-- [Distance Providers for Distance Based SSA](https://docs.magento.com/user-guide/catalog/inventory-configure-distance-priority.html) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Provider] | 全域 | 決定用於「距離優先順序Source選擇演演算法」的提供者。 此功能預設為啟用。 選項： <br/>**`Google MAP`**— 使用Google服務計算送貨目的地地址與來源位置（地址與GPS座標）之間的距離與時間。 此選項需要Google API金鑰，並可能透過Google產生費用。<br/>**`Offline Calculation`** — 使用內嵌的資料庫來計算距離，以判斷最接近出貨目的地地址的來源。 若要使用此選項，您可能需要開發人員協助，才能使用命令列，針對您送抵的所有國家/地區先下載資料庫位置內容。 |

{style="table-layout:auto"}

## [!UICONTROL Google Distance Provider]

![Google距離提供者](./assets/catalog-inventory-distance-provider-settings.png)<!-- zoom -->

<!-- [Google Distance Provider](https://docs.magento.com/user-guide/catalog/inventory-configure-distance-priority.html) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Google API key] | 全域 | 輸入Google MAP提供者的Google API金鑰。 金鑰來自[!DNL Google Maps Platform]，應該已啟用[!DNL Geocoding API]和[!DNL Distance Matrix API]。 如需詳細資訊，請參閱&#x200B;_Inventory management指南_&#x200B;中的[設定距離優先順序演演算法](../../inventory-management/distance-priority-algorithm.md#configure-the-distance-priority-algorithm)。 |
| [!UICONTROL Computation mode] | 全域 | 決定方向與路徑，以計算與出貨地址及指定給庫存之所有來源的距離。 依預設，計算使用驅動模式。 選項： <br/>**`Driving`**— 預設設定，使用道路網路要求標準行車方向。<br/>**`Walking`** — 使用人行道和人行道（如果可用）來要求步行路線。 <br/>**`Bicycling`**— 使用腳踏車道和偏好的街道，要求腳踏車騎行路線（目前僅在美國和部分加拿大城市可用）。 |
| [!UICONTROL Value] | 全域 | 表示來源地點與出貨目的地地址之間的距離與時間計算與傳回的專案。 「距離優先順序演演算法」會建議來源與出貨目的地地址之間的距離或時間最短，而出貨速度更快，而且可能更便宜。 選項： <br/>**`Distance`**— 傳回以公制（公里與公尺）或英制（英里與英尺）為單位的點之間的距離。<br/>**`Time to Destination`** — 傳回從來源地點到運送地址所需的時間（小時與分鐘）。 |

{style="table-layout:auto"}
