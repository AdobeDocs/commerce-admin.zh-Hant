---
title: 『[!DNL Inventory Management] 版本注意事項
description: 檢閱發行說明以瞭解全部資訊 [!DNL Inventory Management] 發行版本。
exl-id: 856b9503-7621-4beb-ac2f-3eb1a240cebc
feature: Inventory, Release Notes
source-git-commit: 7384481d1a4a2a04882d4c99448cca75abc9be31
workflow-type: tm+mt
source-wordcount: '3361'
ht-degree: 0%

---

# [!DNL Inventory Management] 發行說明

以下發行說明說明說明以下版本： [!DNL Inventory Management] 並包含：

![新增](../assets/new.svg) 新功能
![已修正的問題](../assets/fix.svg) 修正和改良
![已知問題](../assets/bug.svg) 已知問題

[!DNL Inventory Management] 是Magento Open Source社群工程特別專案，開放給貢獻者參加。 若要參與並貢獻，請參閱 [github專案](https://github.com/magento/inventory) 存放庫和 [Wiki](https://github.com/magento/inventory/wiki) 以開始使用。 若要討論專案，請加入 [Slack](https://magentocommeng.slack.com/?redir=%2Farchives%2FC5FU5E2HY) 頻道([自我註冊](https://opensource.magento.com/slack))。

[發行排程](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html){target="_blank"} 以取得支援和相容的發行版本。

## v1.2.6

[!DNL Inventory Management] 1.2.6 (模組版本： `magento/inventory-metapackage = 1.2.6`)受到2.4.6版支援，並與2.4.0版Adobe Commerce、雲端基礎結構上的Adobe Commerce及Magento Open Source程式碼基底相容。

![已修正的問題](../assets/fix.svg) 當已售出的子產品退回到庫存中時，店面現在會將複合產品（可配置的、搭售和群組）顯示為庫存中。 之前，店面指出複合產品在這些情況下缺貨。 <!-- ACP2E-1106-->

![已修正的問題](../assets/fix.svg) 如果可設定的產品選項建立時數量設為0且 **[!UICONTROL Display out-of-stock products]** 已啟用。 <!-- ACP2E-1148-->

![已修正的問題](../assets/fix.svg) 當庫存數量變更且產品仍有庫存時，類別頁面快取不再失效。 Adobe Commerce現在會從快取載入頁面，而不是在店麵類別頁面上的產品數量（沒有任何其他變化）變更時重新產生頁面。 <!-- ACP2E-118-->

![已修正的問題](../assets/fix.svg) 現在，以單一來源模式搭配使用詳細目錄時，類別清單產品計數是正確的 **[!UICONTROL Display Out-Of-Stock Products]** 設定已啟用。 Adobe Commerce現在會在計算時檢查產品是否可供銷售。 <!-- ACP2E-1033-->

![已修正的問題](../assets/fix.svg) 啟用「詳細目錄」時，店內傳遞的購物車價格規則現在會如預期運作。 以前，在這些條件下，不會套用購物車價格規則產生的折扣。 <!-- ACP2E-1015-->

![已修正的問題](../assets/fix.svg) 在排程模式下更新產品詳細目錄不再清除所有快取。 之前，「詳細目錄」索引器會清除所有設定快取。 <!-- ACP2E-1003-->

![已修正的問題](../assets/fix.svg) 的值 **[!UICONTROL Allow Multiple Boxes for Shipping]** 進階詳細目錄中產品的屬性現在會如預期儲存。 <!-- ACP2E-992-->

![已修正的問題](../assets/fix.svg) Adobe Commerce現在會對隨店內取貨而下的訂單發出部份退款銷退折讓單，以發放準確的預留補償。 之前，系統會儲存一個錯誤的訂位至 `inventory_reservation` 當管理員使用者未選取以下專案而建立銷退折讓單時 **[!UICONTROL Return to Stock]** 核取方塊。 <!-- ACP2E-979-->

![已修正的問題](../assets/fix.svg) 當其中一個變數已在實作多來源庫存的部署中手動退回庫存時，Adobe Commerce不再將可設定產品顯示為無存貨在店面上。 <!-- ACP2E-952-->

![已修正的問題](../assets/fix.svg) 產品格線上的欄位置(**[!UICONTROL Catalog]** > **[!UICONTROL Products]**)在設定了多個詳細目錄來源的部署中重新載入頁面後，不再回覆至其先前的位置。 <!-- ACP2E-925-->

![已修正的問題](../assets/fix.svg) 在針對虛擬產品簽發銷退折讓單之後，存貨數量現在為正確，當 **[!UICONTROL Back to stock]** 未選取核取方塊。 <!-- ACP2E-908-->

![已修正的問題](../assets/fix.svg) 您現在可以使用自動產品排序來儲存類別，以及指定給非預設庫存的範圍。 之前，Adobe Commerce不會儲存類別並顯示此錯誤： `Something went wrong while saving the category`. <!-- ACP2E-859-->

![已修正的問題](../assets/fix.svg) 使用所有無庫存的可設定變數建立產品時，可設定的產品庫存狀態現在會如預期更新。 <!-- ACP2E-813-->

![已修正的問題](../assets/fix.svg) 現在，保留不一致性分析工具可正確處理包含可設定、搭售及分組產品的部分出貨訂單。 現在會分析複合產品型別。 以前，取消和退款只針對上階產品儲存，而不針對可設定和一起出貨的套裝產品的子產品訂單專案儲存。 <!-- ACP2E-924-->

![已修正的問題](../assets/fix.svg) 當管理員使用者嘗試將200個或更多詳細目錄來源指派給庫存或產品時，Adobe Commerce不再顯示錯誤。 <!-- ACP2E-1180-->

![已修正的問題](../assets/fix.svg) Adobe Commerce現在支援針對已刪除產品的訂單建立銷退折讓單。 先前，建立商業發票後，當訂單中刪除產品時，商家無法建立銷退折讓單。 應用程式顯示這個錯誤： `Following products with requested skus were not found: s00001`. t. <!-- ACP2E-1138-->

![已修正的問題](../assets/fix.svg) 系統現在會根據單一和多重商店ID來篩選商店。 此 `event` 產品屬性代碼已新增至保留屬性代碼清單。 之前，當存貨模組安裝時，「低存貨報表」會擲回例外狀況。 <!-- ACP2E-1017-->

![已修正的問題](../assets/fix.svg) 階層式導覽篩選器現在可如預期運作，而無庫存產品現在可附加至店麵類別產品清單。 新的 `is_out_of_stock` 排序屬性使用storefront產品集合的Elasticsearch動態欄位對應程式。 <!-- ACP2E-748-->

![已修正的問題](../assets/fix.svg) 當子產品庫存狀態由REST變更時，複合產品（捆綁、已分組和可配置）庫存狀態會按預期更新 `POST /rest/V1/inventory/source-items` 呼叫。 <!-- ACP2E-1209-->

## v1.2.5

[!DNL Inventory Management] 1.2.5 (模組版本： `magento/inventory-metapackage = 1.2.5`)受到2.4.5版支援，並與2.4.0版Adobe Commerce、雲端基礎結構上的Adobe Commerce及Magento Open Source程式碼基底相容。

![已修正的問題](../assets/fix.svg) 當商家從管理員建立出貨時，組合和分組產品的預設存貨狀態現在會如預期更新。 以前，在建立出貨後，這些產品的狀態保持不變。 <!--- ACP2E-418-->

![已修正的問題](../assets/fix.svg) 現在，當滿足以下條件之一時，可設定的產品會回到庫存中： 1. 父產品至少有一個已儲存的庫存子項。 2.可設定的產品本身已更新並設為 **有貨** 並且至少有一個孩子有庫存。 <!--- ACP2E-443-->

![已修正的問題](../assets/fix.svg) 透過REST API實作的詳細目錄變更現在會如預期反映在產品詳細資料頁面上。 現在，在比較上次和目前的庫存狀態後，會清除目錄產品的快取。 以前，省略回呼函式會導致不正確評估庫存狀態變更，這不會觸發必要的快取清理。 因此，店面並未反映存貨變更。 <!--- ACP2E-161-->

![已修正的問題](../assets/fix.svg) 使用更新來源專案後，現在店面中會顯示指派給預設庫存且先前已無庫存的產品 `/V1/inventory/source-items`. 之前，此REST API端點設定錯誤 `stock_status`. <!--- ACP2E-562-->

![已修正的問題](../assets/fix.svg) 透過大量動作取消指定存貨來源(**[!UICONTROL Catalog]** > **[!UICONTROL Products]** > **[!UICONTROL Select Products]** > **[!UICONTROL Actions - Unassign Inventory Source]**)現在會如預期運作，當來源包含重複的SKU (前導零除外，例如 `01234` 和 `1234`)。 之前，應用程式不會解除指派詳細目錄來源，並擲回錯誤。 <!--- ACP2E-2641-->

![已修正的問題](../assets/fix.svg) 產品庫存狀態現在一律為 **有貨** 在啟用無限延期交貨訂單時，無論延期交貨的數量為何，產品都會指定給自訂存貨。 過去，即使啟用延期交貨，產品也無庫存。 <!--- ACP2E-664-->

![已修正的問題](../assets/fix.svg) 來源專案更新後，可設定的產品上下階產品庫存現在會正確更新 `POST /V1/inventory/source-items`. 透過API更新子產品後，用於預設庫存檢查的新庫存外掛程式會更新可設定的產品數量和狀態。 <!--- ACP2E-442-->

![已修正的問題](../assets/fix.svg) 無庫存的分組產品不再列在店麵類別頁面上。 <!--- ACP2E-2082-->

![已修正的問題](../assets/fix.svg) 更正中的套件名稱 `CatalogInventory` `composer.json`. <!--- ACP2E-2914-->

![已修正的問題](../assets/fix.svg) 在多來源/存貨部署中下零數量產品的訂單後，現在可在Admin中正確顯示延期交貨訂單狀態。 [GitHub-33756](https://github.com/magento/magento2/issues/33756) <!--- ACP2E-713-->

![已修正的問題](../assets/fix.svg) 從庫存區段更新套裝產品時，沒有庫存的套裝產品不再顯示在店麵類別頁面上。 <!--- ACP2E-2012-->

![已修正的問題](../assets/fix.svg) 與PHP 7.4的相容性問題已解決。 <!--- AC-3192-->

![已修正的問題](../assets/fix.svg) 已改善儲存作業的效能，該作業包含包含包含許多選項（多個100）的套件組合產品。 以前，儲存這些大型套件產品需要幾分鐘的時間，而且有時會在啟用庫存服務的部署中導致逾時。 [GitHub-34732](https://github.com/magento/magento2/issues/34732) <!--- AC-1901-->

![已修正的問題](../assets/fix.svg) 產品大量動作工具(**[!UICONTROL Select Products]** > **[!UICONTROL Actions]** > **[!UICONTROL Assign Inventory Source]**)現在可在重複SKU （行距除外）時，依預期將庫存來源指派給多個產品時 `0` (例如， `01234` 和 `1234`)。 之前，僅指派給一種產品一個詳細目錄來源。 [GitHub-35171](https://github.com/magento/magento2/issues/35171) <!--- AC-2584-->

![已修正的問題](../assets/fix.svg) 此 `ProductInterface.only_x_left_in_stock` 如果詳細目錄為0，欄位現在會傳回0。 之前，它會傳回null。 [GitHub-29932](https://github.com/magento/magento2/issues/29932) <!--- AC-1806-->

![已修正的問題](../assets/fix.svg) 您現在可以從管理員編輯預設庫存 **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**. 以前，當您嘗試新增或移除預設庫存的來源時，控制檯中會顯示JavaScript錯誤，不過您可以將網站指派給預設庫存。 <!--- ACP2E-545-->

![已修正的問題](../assets/fix.svg) <!--- ACP2E-274--> 現在，搭配使用詳細目錄單一來源模式時，類別清單產品計數是正確的 **[!UICONTROL Display Out-Of-Stock Products]** 設定已啟用。 新外掛程式現在使用 `AreProductsSalableInterface` 和 `StockConfigurationInterface` 以判斷產品總數。 之前，類別產品清單傳回錯誤的產品數量。

![已修正的問題](../assets/fix.svg) <!--- ACP2E-322--> 現在，當庫存更新後，可設定的產品會移至產品清單中的最後一個位置， **[!UICONTROL Move out of stock to the bottom]** 設定已啟用。 實施新的自訂資料庫查詢來否定Elasticsearch索引排序順序，這忽略啟用管理員的排序順序。 先前，啟用此設定時，可設定的產品及其子產品不會移至清單底部。

## v1.2.4

Inventory management 1.2.4 (模組版本： `magento/inventory-metapackage = 1.2.4`)受到2.4.4版支援，並與2.4.0版Adobe Commerce、雲端基礎結構上的Adobe Commerce及Magento Open Source程式碼基底相容。

![已修正的問題](../assets/fix.svg) Commerce現在會在管理員產品清單檢視中，顯示所有產品的正確可銷售數量值。 之前，對於庫存產品的可銷售數量，如果其SKU包含特殊字元，則會顯示空白值。 <!--- MC-41936-->

![已修正的問題](../assets/fix.svg) 改善購物車與結帳動作的效能，例如在部署中有許多（約10,000個）庫存來源時將產品新增到購物車。 <!--- MC-42570-->

![已修正的問題](../assets/fix.svg) 此 `bin/magento inventory:reservation:list-inconsistencies` 現在，即使從資料庫遺漏預留且已清除快取，命令仍可正確處理具有部分出貨的訂單。 先前，當使用預先清除的快取執行此命令時，Commerce顯示以下錯誤： `Area code is not set`. <!--- MC-42142-->

![已修正的問題](../assets/fix.svg) 當子項共用時，已分組產品子產品的增量索引不再導致其他已分組產品的索引不正確。 <!--- MC-41963-->

![已修正的問題](../assets/fix.svg) 透過API從類別中移除產品後，店麵類別頁面現在會顯示正確的產品計數。 以前，在重新索引發生之前，類別頁面產品計數不正確。 <!--- MC-42287-->

![已修正的問題](../assets/fix.svg) 現在，當建立銷退折讓單時，可設定的產品可返回到存貨，當 **[!UICONTROL Manage Stock]** 選項已停用。 之前，Commerce不會顯示 **返回庫存** 此選項停用時，銷退折讓單建立頁面上的核取方塊。 <!--- MC-42002-->

![已修正的問題](../assets/fix.svg) 已改善超過10,000個專案的存貨存貨管理。 以前，績效問題有時會阻止商家在啟動其網站之前編輯管理員中的庫存。 <!--- MC-42643-->

![已修正的問題](../assets/fix.svg) 此 **[!UICONTROL User Roles]** 「管理員」中的頁面已更新，為管理員提供傳送方法設定的受限制許可權存取權。 此 _送貨方法_ 區段已重新命名為 _[!UICONTROL Delivery methods]_、和_[!UICONTROL In-Store Pickup]_ 移至底下 _[!UICONTROL Delivery methods]_區段。 [GitHub-30053](https://github.com/magento/magento2/issues/30053)  <!--- MC-41545-->

![已修正的問題](../assets/fix.svg) API更新銷退折讓單後，Adobe Commerce不再建立重複的產品預訂。 <!--- MC-41757-->

![已修正的問題](../assets/fix.svg) 從切換 _[!UICONTROL Pick up in Store]_跳至_[!UICONTROL Shipping]_ 當只有店內收取傳送可用時，結帳工作流程中的索引標籤不再觸發JavaScript錯誤。 <!--- MC-42808-->

![已修正的問題](../assets/fix.svg) 可銷售產品數量與庫存產品數量現在已正確同步。 以前，系統不會為取消的訂單重新建立存貨預留補償。 <!--- MC-42485-->

![已修正的問題](../assets/fix.svg) 驗證器的效能已最佳化，以防止將新來源新增至具有出貨型別的捆綁產品的子產品 `Ship Together`. <!--- MC-43039-->

## 1.2.3

[!DNL Inventory Management] 1.2.3 (模組版本： `magento/inventory-metapackage = 1.2.3`)受到2.4.3版支援，並與2.4.0版Adobe Commerce、雲端基礎結構上的Adobe Commerce及Magento Open Source程式碼基底相容。

![已修正的問題](../assets/fix.svg) 已修正多個與前端複合產品可見性相關的問題。

![已修正的問題](../assets/fix.svg) 以最低需求數量改善購物車頁面管理效能。

![已修正的問題](../assets/fix.svg) 數個修正的目標是解決來源建立、無存貨料號、存貨來源、排序已配置來源、店內交貨及存貨指令等問題。

![已修正的問題](../assets/fix.svg) [!DNL Commerce] 現在支援三位數的加拿大郵遞區號，以供店內遞送。 由於設定的限制，不支援六位數的程式碼 `geonames.org`.

![已修正的問題](../assets/fix.svg) 管理員現在會在上顯示已停用產品的正確預設庫存數量。 **產品** 格線與 **編輯產品** 多存放區部署的頁面。

![已修正的問題](../assets/fix.svg) [!DNL Commerce] 現在，當套件組合產品有庫存時，會重新整理類別產品快取。

## 1.2.2

[!DNL Inventory Management] 1.2.2 (模組版本： `magento/inventory-metapackage = 1.2.2`)受到2.4.2版支援，並與2.4.0版Adobe Commerce、雲端基礎結構上的Adobe Commerce及Magento Open Source程式碼基底相容。

![已修正的問題](../assets/fix.svg) 已修正多個與前端複合產品可見性相關的問題。

![已修正的問題](../assets/fix.svg) 改善B2B數量更新期間的購物車頁面效能。

![已修正的問題](../assets/fix.svg) 有數項修正已鎖定目標，以解決店內收取費用、大量更新和詳細目錄臨界值的問題。

![新增](../assets/new.svg) **功能測試。** 推出新的功能測試，並為現有測試提供修正，使其更穩定。

## 1.2.1

[!DNL Inventory Management] 1.2.1 (模組版本： `magento/inventory-metapackage = 1.2.1`)受到2.4.1版支援，並與2.4.0版Adobe Commerce、雲端基礎結構上的Adobe Commerce及Magento Open Source程式碼基底相容。

![已修正的問題](../assets/fix.svg) 修正的已知問題 `inventory_cleanup_reservations` cron工作並解決與套件組合產品的店內收取功能相關的問題。 此更新也包含存貨計算、套件組合產品支援和延期交貨功能的一般改善。

![新增](../assets/new.svg) **功能測試。** 推出新的功能測試，為店內取貨功能提供額外涵蓋範圍。

## 1.2.0

[!DNL Inventory Management] 1.2.0 (模組版本： `magento/inventory-metapackage = 1.2.0`)的2.4.0版Adobe Commerce、雲端基礎結構上的Adobe Commerce以及Magento Open Source程式碼基底都支援。

![已修正的問題](../assets/fix.svg) 解決來源指派問題、可擴充環境功能支援，以及與PHP 7.4、MySQL 8和PHPUNIT 9的相容性的多項修正。

![新增](../assets/new.svg) **店內傳遞方法。** 新增選項，讓使用者在結帳時選取要作為取車位置的來源。 另請參閱 [店內傳遞](../stores-purchase/shipping-in-store-delivery.md) 在 _銷售和購買體驗指南_.

![新增](../assets/new.svg) **多來源模式的套件組合產品支援。** 詳細目錄支援具有多個來源的所有產品型別。

![新增](../assets/new.svg) **非同步重新編制庫存索引。** 新增非同步重新索引股票的功能，並改善數個關鍵案例的效能。

![新增](../assets/new.svg) **大量介面。** 推出新的大量介面以進行可用性檢查： `\Magento\InventorySalesApi\Api\AreProductsSalableInterface`， `\Magento\InventorySalesApi\Api\AreProductsSalableForRequestedQtyInterface`.

![新增](../assets/new.svg) **增加測試涵蓋範圍。** 自動化測試涵蓋新功能，包括已探索和已修正問題的延伸涵蓋範圍。

![已知問題](../assets/bug.svg) **已知問題。** 「 」不存在 `object_id` 預留中繼資料中的欄位會導致 `inventory_cleanup_reservations` cron工作無法正常運作。 此問題已在中介紹 [magento/inventory#3046](https://github.com/magento/inventory/pull/3046).

**因應措施：** 執行下列MySQL查詢以手動清除保留：

```sql
SELECT GROUP_CONCAT(reservation_id) FROM inventory_reservation GROUP BY stock_id, sku HAVING SUM(quantity) = 0;
DELETE FROM inventory_reservation where reservation_id IN (result_of_the_first_query);
```

## 1.1.6

[!DNL Inventory Management] 1.1.6 (模組版本： `inventory-composer-metapackage = 1.1.6`)受到2.3.6版支援，並與2.3.5、2.3.4、2.3.3、2.3.2、2.3.1和2.3.0版Adobe Commerce、雲端基礎結構上的Adobe Commerce以及Magento Open Source程式碼基底相容。

![已修正的問題](../assets/fix.svg) 修正以解決與延期交貨、銷退折讓單、低庫存報表格線相關的問題、連線至「解決不一致」CLI工具的修正以及一般改善。

![新增](../assets/new.svg) **非同步重新編制庫存索引。** 新增非同步重新索引股票的功能，並改善數個關鍵案例的效能。

## 1.1.5

[!DNL Inventory Management] 1.1.5 (模組版本： `inventory-composer-metapackage = 1.1.5`)受到2.3.5版支援，並與2.3.4、2.3.3、2.3.2、2.3.1和2.3.0版Adobe Commerce、雲端基礎結構上的Adobe Commerce以及Magento Open Source程式碼基底相容。

![新增](../assets/new.svg) **產品SKU變更後更新詳細目錄。** 引入新的配置設定以切換到新行為：「與目錄同步」。

![新增](../assets/new.svg) **功能測試。** 推出新的功能測試，以消除測試涵蓋範圍差距。 修正數個問題，讓測試更穩定可靠)。

![已知問題](../assets/bug.svg) 修正以防止產品過度銷售、店面上的「缺貨」產品可見度、大量針對可擴充環境支援和使用者介面改良的修正。

## 1.1.4

[!DNL Inventory Management] 1.1.4 (模組版本： `inventory-composer-metapackage = 1.1.4`)受到2.3.4版支援，並與2.3.3、2.3.2、2.3.1和2.3.0版Adobe Commerce、雲端基礎結構上的Adobe Commerce以及Magento Open Source程式碼基底相容。

![已修正的問題&#x200B;](../assets/fix.svg)**提升效能。** 針對庫存預留CLI命令引入聚束邏輯，以減少記憶體使用量，並避免程式在未得到任何回應時卡住的情況。

![新增&#x200B;](../assets/new.svg)**增加測試涵蓋範圍。** 推出許多新的功能測試。 幾乎所有手動清查案例都包含自動化測試。

![已知問題](../assets/bug.svg) 針對解決銷退折讓單、分組產品、來源與庫存整批作業問題的多項修正。

## 1.1.3

[!DNL Inventory Management] 1.1.3 (模組版本： `inventory-composer-metapackage = 1.1.3`)受到2.3.3版支援，並與Adobe Commerce的2.3.2、2.3.1和2.3.0版、雲端基礎結構上的Adobe Commerce以及Magento Open Source程式碼基底相容。

![已修正的問題&#x200B;](../assets/fix.svg)**與Adobe Commerce和B2B功能更妥善整合。** [!DNL Inventory Management] 現在，對於使用非預設詳細目錄來源和庫存的網站，可使用下列功能正常運作：

- 依SKU排序(Adobe Commerce)
- 快速訂購(B2B)
- 請購單清單(B2B)

![新增&#x200B;](../assets/new.svg)**提升效能。** 對於執行預設庫存和來源的網站，店面目錄瀏覽效能已有所改善。

![新增&#x200B;](../assets/new.svg)**增加測試涵蓋範圍。** 自動化功能與整合測試的涵蓋範圍已大幅增加。

## 1.1.2

[!DNL Inventory Management] 1.1.2 (模組版本： `inventory-composer-metapackage = 1.1.2`)受到2.3.2版支援，並與2.3.1版、2.3.0版Adobe Commerce、Adobe Commerce on cloud infrastructure和Magento Open Source程式碼基底相容。

![已修正的問題](../assets/fix.svg) 已新增 `source_code` 對GET的回應 `/V1/shipments` REST端點。 <!-- https://github.com/magento/inventory/pull/2142 -->

![已修正的問題](../assets/fix.svg) 已解決在簽發未出貨訂單的銷退折讓單後，正確結清預留及更新產品數量的問題。 當您選取「 」選項時， <!-- https://github.com/magento/inventory/pull/2179 -->

![已修正的問題](../assets/fix.svg) 解決在建立產品期間輸入數量時，正確儲存可設定產品子項數量的問題。 <!-- https://github.com/magento/inventory/pull/2158 -->

的新模組 [!DNL Inventory Management] 1.1.2 Beta版包括：

```php
        'Magento_InventoryGraphQl' => 1,
        'Magento_InventoryReservations' => 1,
        'Magento_InventoryReservationsApi' => 1,
        'Magento_InventoryReservationCli' => 1,
        'Magento_InventoryExportStock' => 0,
        'Magento_InventoryExportStockApi' => 0,
```

![新增](../assets/new.svg) **新增大量部分庫存轉移端點**  — 目前大量移轉端點將所有指定數量從來源移至目的地來源。 新的 `/rest/V1/inventory/bulk-partial-source-transfer` 端點可讓商家以大量作業將部分存貨從來源轉移至來源。 若要移轉特定數量的數量，請輸入對端點的請求，並附上 `sku`， `qty`， `origin_source_code`、和 `destination_source_code`. 傳輸會確認來源已指派給 `sku`，有足夠的數量可轉移，依此類推。 另請參閱 [存貨整批作業](https://developer.adobe.com/commerce/webapi/rest/inventory/bulk-inventory/){target="_blank"} REST API檔案中。 <!-- https://github.com/magento/inventory/pull/2117 -->

![新增](../assets/new.svg) **已新增保留區CLI**  — 新命令可讓您選擇偵測和解決保留時間不一致的問題。 當訂單提交並變更狀態時， [!DNL Inventory Management] 會透過薪酬預留產生初始預留和更新。 這些命令會依訂單ID、SKU和庫存ID傳回偵測到的不一致清單，並建立要解決的預留量。 請參閱 [CLI參考](cli.md) 以取得詳細資訊。 <!-- https://github.com/magento/inventory/pull/2199 https://github.com/magento/inventory/pull/2184 https://github.com/magento/inventory/pull/2171 https://github.com/magento/inventory/pull/2148  -->

![新增](../assets/new.svg) **來源和SSA選項的效能改善**  — 在出貨期間排序和選取來源，會導致來源數量大的存貨效能降低。 此版次在複查及選取出貨的SSA選項時，大幅改善可用來源清單與排序的效能。 <!-- https://github.com/magento/inventory/pull/2056 https://github.com/magento/inventory/pull/2090 -->

![新增](../assets/new.svg) **新增對Inventory management的GraphQL支援**  — 此版本安裝新的 `magento/module-inventory-graph-ql` 模組。 GraphQL [ProductInterface屬性](https://developer.adobe.com/commerce/webapi/graphql/schema/products/interfaces/attributes/){target="_blank"} 現在包含 `only_x_left_in_stock` 和 `stock_status` 屬性 [!DNL Inventory Management] 支援。 <!-- https://github.com/magento/inventory/pull/2124 -->

![新增](../assets/new.svg) **已指派來源的簡化UI**  — 產品頁面中的「指派的來源」表格簡化了內容，使更新更容易，並在顯示許多來源時提高了效能。 依來源名稱列出所有來源(將游標停留在 `source_code`)。

![新增](../assets/new.svg) **匯出彙總的庫存服務**  — 此版本提供新的匯出彙總存量服務（保留系統中的預留），以支援外部Sales Channel，例如Amazon、eBay和Google購物廣告。  <!-- https://github.com/magento/inventory/pull/2067 -->

## 1.1.0

[!DNL Inventory Management] 1.1.0 (模組版本： `inventory-composer-metapackage = 1.1.0`)受到支援，並與Adobe Commerce 2.3.0版、雲端基礎結構上的Adobe Commerce以及Magento Open Source程式碼庫相容。 [!DNL Inventory Management] 1.1.1僅以套件名稱更新形式發行，支援2.3.1版，並與2.3.0版Adobe Commerce、Adobe Commerce on cloud infrastructure和Magento Open Source程式碼基底相容。

![已修正的問題](../assets/fix.svg) **新增對單一和多來源模式Elasticsearch的支援**  — 您現在可以設定並使用包含自訂庫存的Elasticsearch。 另請參閱 [設定Elasticsearch服務](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/service/elasticsearch.html){target="_blank"} 以取得安裝資訊。 <!-- PR https://github.com/magento/inventory/pull/1943 -->

![已修正的問題](../assets/fix.svg) 解決預設庫存的效能問題，大幅提升多項作業的效能。 改善功能可提升單一來源模式、「移轉存貨至來源」、「店面分類」頁面及「可銷售數量」計算的效能。

<!-- All Performance Track issues resolved https://github.com/magento/inventory/issues?q=is%3Aopen+is%3Aissue+label%3APerformance -->

![已修正的問題](../assets/fix.svg) 已解決缺貨狀態和可設定及分組產品的大量存貨移轉至存貨的問題。 選取父級產品並執行大量動作不會影響產品狀態。 如果父產品有庫存，則保持有庫存。

<!-- PR https://github.com/magento/inventory/pull/1972 -->

![新增](../assets/new.svg) **距離優先順序演演算法**  — 距離優先順序演演算法是一種全新的現成來源選取演演算法，適用於以距離為基礎的送貨建議。 此演演算法會將出貨目的地地址的地點與來源地點做比較，以決定最接近完成出貨的來源。 距離可透過實體距離或使用匯入的地理碼位置資料或Google方向（駕駛、步行或騎腳踏車）從一個位置到另一個位置所花費的時間來決定。

![新增](../assets/new.svg) **展開的來源數量清單**  — 擁有大量來源的商家，可透過Product Grid輕鬆暫留及檢視每個產品的所有來源。 每項產品至少會顯示五個來源與相符數量。 將滑鼠游標停留在來源上時，可以捲動瀏覽整個來源清單和目前數量。

![已知問題](../assets/bug.svg) Magento Open Source和Adobe Commerce v2.3.1的已知問題 — 由於主題名稱反映PHP類別和方法名稱的非同步API有所變更，來源之間的非同步移轉資料會遇到問題。 使用同步作業，設定 **[!UICONTROL Run asynchronously]** 至 `No`，建議使用。
