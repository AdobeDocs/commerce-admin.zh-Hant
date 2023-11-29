---
title: 『[!UICONTROL Catalog] &gt； [!UICONTROL Inventory]『
description: 檢閱上的組態設定 [!UICONTROL Catalog] &gt； [!UICONTROL Inventory] 商務管理員頁面。
exl-id: 80113a31-3585-4ee1-95af-31efc09389eb
feature: Configuration, Inventory
source-git-commit: 768c9fdc37127b408230983e39e98b11149713a7
workflow-type: tm+mt
source-wordcount: '1205'
ht-degree: 0%

---

# [!UICONTROL Catalog] > [!UICONTROL Inventory]

{{config}}

>[!NOTE]
>
>[!DNL Inventory Management] 適用於Adobe Commerce和Magento Open Source的工具，可讓您管理產品詳細目錄。 擁有單一商店到多個倉庫、商店、取貨地點、卸貨託運人等等的商家，可以使用這些功能來維護銷售數量，並處理出貨以完成訂單。 有關這些功能以及如何使用這些功能來管理多個位置中的庫存的更多資訊，請參閱 [_[!DNL Inventory Management] 使用手冊&#x200B;_](https://experienceleague.adobe.com/docs/commerce-admin/inventory/introduction.html).

## [!UICONTROL Stock Options]

![股票期權](./assets/catalog-inventory-stock-options.png)<!-- zoom -->

<!-- [Stock Options](https://docs.magento.com/user-guide/catalog/inventory-options-global.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Decrease Stock When Order is Placed] | 全域 | 如果設為 `Yes`，會減少下訂單時的庫存數量。 替換為 _管理庫存_ 啟用時，系統會輸入訂購產品與數量的預留。 選項： `Yes` / `No` |
| [!UICONTROL Set Items' Status to be in Stock When Order is Cancelled] | 存放區檢視 | 如果設為 `Yes`，取消訂單時會將專案退回存貨。 替換為 _管理庫存_ 啟用時，會針對已取消的產品與數量清除預留。 選項： `Yes` / `No` |
| [!UICONTROL Display Out of Stock Products] | 全域 | 如果設為 `Yes`，會顯示無庫存的產品。 如果產品警報也啟用，客戶可以註冊以在產品上市時收到通知。 選項： `Yes` / `No` |
| [!UICONTROL Only X left Threshold] | 網站 | 建立閾值 `Only x left` 訊息。 例如，如果設為3，當庫存中有三個或更少專案時，訊息便會出現。 如果值設定為，則不會出現訊息 `0`. |
| [!UICONTROL Display products availability in Stock on Storefront] | 存放區檢視 | 如果設為 `Yes`，顯示 `In Stock` 或 `Out of Stock` 訊息。 選項： `Yes` / `No` |
| [!UICONTROL Enable Inventory Check On Cart Load] | 全域 | 決定在購物車中載入產品時是否執行庫存檢查。 停用此詳細目錄檢查可改善結帳步驟的效能，尤其是購物車中有許多專案時。 不過，如果您略過預先驗證，客戶可能會看到 _無庫存_ 稍後在結帳程式中發生錯誤。 選項： `Yes` / `No` |
| [!UICONTROL Synchronize with Catalog] | 全域 | 當設定為 `Yes`，庫存資料會根據目錄變更（例如產品移除、產品SKU變更和產品型別變更）進行調整，並保持庫存和目錄之間的一致性。 選項： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Product Stock Options]

![產品庫存選項](./assets/catalog-inventory-product-stock-options.png)<!-- zoom -->

<!-- [Product Stock Options](https://docs.magento.com/user-guide/catalog/inventory-options-global.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Manage Stock] | 全域 | 決定您是否使用完整存貨控制來管理目錄中的料號。 選項： <br/>**是**  — 啟用完整存貨控制以追蹤目前庫存中的專案數。 <br/>**否**  — 不會追蹤目前庫存中的專案數。 |
| [!UICONTROL Backorders] | 全域 | 決定商店管理延期交貨的方式。 延交訂單不會變更訂單的處理狀態。 無論產品是否有庫存，下訂單時仍會立即授權或擷取資金。 當產品可供使用時，即會出貨。 選項： <br/>**無延期交貨**  — 產品無庫存時，不接受延期交貨。 <br/>**允許數量低於0**  — 當數量低於零時，接受延期交貨。 <br/>**允許數量低於0並通知客戶**  — 在數量低於零時接受延期交貨，但通知客戶仍可下訂單。 |
| [!UICONTROL Use deferred Stock update] | 全域 | ![Adobe Commerce](../../assets/adobe-logo.svg) (僅限Adobe Commerce)決定是否要在允許延期交貨時延遲存貨更新( _延期交貨_ 選項已設定為以下專案以外的任何專案： `No backorders` 預設值)。 它適用於單一產品或整個網站，並使用 _工作佇列_ 允許存貨數量指標在訂購後以非同步方式更新的機制。 此選項也可搭配 [非同步下單](https://experienceleague.adobe.com/docs/commerce-operations/performance-best-practices/high-throughput-order-processing.html#asynchronous-order-placement) 搭配 [Inventory management](../../inventory-management/introduction.md). |
| 購物車中允許的最大數量 | 全域 | 決定單一訂單可購買的最大產品數量。 依預設，最大數量設為10,000。 |
| [!UICONTROL Out-of-Stock Threshold] | 全域 | 決定產品被視為無庫存的庫存水準。 選項： <br/>**正數**  — 具有 _延期交貨_ 已停用，請輸入正數。 啟用「延期交貨」時，此金額會被忽略。 <br/>**零**  — 具有 _延期交貨_ 已啟用，請輸入 `0` 允許無限延期交貨。 <br/>**負數金額**  — 具有 _延期交貨_ 已啟用，建議您輸入負值。 此金額會新增至「可銷售數量」。 例如，輸入–50以允許此金額以下的訂單。 |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | 全域 | 根據客戶群組決定可供採購的料號最小金額。 依預設，最小數量設為1。 按一下 **[!UICONTROL Add Minimum Qty]** 以輸入特定客戶群組的不同值。 |
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
>設定和支援 **非同步佇列管理員**，您必須使用命令列。 這可能需要開發人員協助。 另請參閱 [啟動訊息佇列取用者](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html) 在 _設定指南_.

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Run asynchronously] | 全域 | 決定您是否要以非同步方式執行大量產品動作，包括 [大量](../../inventory-management/bulk-assignment.md) 指派來源、取消指派來源及 [將存貨移轉至來源](../../inventory-management/inventory-transfer.md). 它會收集最多 _[!UICONTROL Asynchronous batch size]_，然後執行這些動作。 此功能預設為停用。 我們建議您在啟用前先檢閱大量動作的效能。 選項：<br/>**`Yes`**— 執行所有大量作業 [!DNL Inventory Management] 非同步處理。 若要啟用，您必須設定非同步佇列管理員。<br/>**`No`**— 預設。 不會以非同步方式執行大量作業。 |
| [!UICONTROL Asynchronous batch size] | 全域 | 設定 **[!UICONTROL Run asynchronously]** 至 `Yes` 輸入值 _[!UICONTROL Asynchronous batch size]_欄位。 <br/>預設批次大小為100。 當大量程式達到此數量時，就會執行。 |

{style="table-layout:auto"}

## [!UICONTROL Inventory Indexer Settings]

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Stock/Source reindex strategy] | 全域 | 決定用於庫存/來源重新索引的策略。 選項： `Synchronous` / `Asynchronous` （非同步模式必須設定非同步佇列管理員） |

{style="table-layout:auto"}

>[!NOTE]
>
> 由於訂單相關活動的存貨更新相依性，因此無論在何時進行產品儲存，都會觸發存貨索引器， `Synchronous` 或 `Asynchronous` 設定。


## [!UICONTROL Distance Provider for Distance Based SSA]

![距離型SSA的距離提供者](./assets/catalog-inventory-distance-provider.png)<!-- zoom -->

<!-- [Distance Providers for Distance Based SSA](https://docs.magento.com/user-guide/catalog/inventory-configure-distance-priority.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Provider] | 全域 | 決定要用於「距離優先順序來源選取演演算法」的提供者。 此功能預設為啟用。 選項： <br/>**`Google MAP`**— 使用Google服務計算運送目的地地址與來源位置（地址和GPS座標）之間的距離和時間。 此選項需要Google API金鑰，並可能透過Google產生費用。<br/>**`Offline Calculation`**  — 使用內嵌的資料庫來計算距離，以判斷最接近出貨目的地地址的來源。 若要使用此選項，您可能需要開發人員協助，才能使用命令列，針對您送抵的所有國家/地區先下載資料庫位置內容。 |

{style="table-layout:auto"}

## [!UICONTROL Google Distance Provider]

![Google距離提供者](./assets/catalog-inventory-distance-provider-settings.png)<!-- zoom -->

<!-- [Google Distance Provider](https://docs.magento.com/user-guide/catalog/inventory-configure-distance-priority.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Google API key] | 全域 | 輸入Google MAP提供者的Google API金鑰。 索引鍵是來自 [!DNL Google Maps Platform] 而且應該有 [!DNL Geocoding API] 和 [!DNL Distance Matrix API] 已啟用。 如需詳細資訊，請參閱 [設定距離優先順序演演算法](../../inventory-management/distance-priority-algorithm.md#configure-the-distance-priority-algorithm) 在 _Inventory management指南_. |
| [!UICONTROL Computation mode] | 全域 | 決定方向與路徑，以計算與出貨地址及指定給庫存之所有來源的距離。 依預設，計算使用驅動模式。 選項： <br/>**`Driving`**— 預設設定，會使用道路網路來要求標準行車方向。<br/>**`Walking`**  — 使用人行道和人行道（如果可用）來要求步行路線。 <br/>**`Bicycling`**— 使用腳踏車道和偏好的街道要求腳踏車騎行路線（目前僅在美國和部分加拿大城市提供）。 |
| [!UICONTROL Value] | 全域 | 表示來源地點與出貨目的地地址之間的距離與時間計算與傳回的專案。 「距離優先順序演演算法」會建議來源與出貨目的地地址之間的距離或時間最短，而出貨速度更快，而且可能更便宜。 選項： <br/>**`Distance`**— 傳回公制（公里和公尺）或英制（英里和英尺）中點之間的距離。<br/>**`Time to Destination`**  — 傳回從來源地點前往運送地址所需的時間（小時與分鐘）。 |

{style="table-layout:auto"}
