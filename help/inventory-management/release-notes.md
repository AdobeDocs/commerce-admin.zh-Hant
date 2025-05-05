---
title: '[!DNL Inventory Management]發行說明'
description: 檢閱發行說明，瞭解所有 [!DNL Inventory Management] 發行版本的相關資訊。
exl-id: 856b9503-7621-4beb-ac2f-3eb1a240cebc
feature: Inventory, Release Notes
source-git-commit: fdc14758788fa5cd0391371ebfafb478dadec8a4
workflow-type: tm+mt
source-wordcount: '3462'
ht-degree: 0%

---

# [!DNL Inventory Management]發行說明

這些發行說明說明[!DNL Inventory Management]的發行版本，包括：

![新](../assets/new.svg)新功能
![已修正問題](../assets/fix.svg)修正和改良
![已知問題](../assets/bug.svg)已知問題

[!DNL Inventory Management]是開放給貢獻者的Magento Open Source社群工程特殊專案。 若要參與並貢獻內容，請參閱[GitHub專案](https://github.com/magento/inventory)存放庫和[Wiki](https://github.com/magento/inventory/wiki)以開始使用。 若要討論專案，請加入[Slack](https://magentocommeng.slack.com/?redir=%2Farchives%2FC5FU5E2HY)管道（[自我註冊](https://opensource.magento.com/slack)）。

支援及相容發行的[發行排程](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html?lang=zh-Hant){target="_blank"}。

## v1.2.7

[!DNL Inventory Management] 1.2.7發行說明包含在[core 2.4.7發行說明](https://experienceleague.adobe.com/zh-hant/docs/commerce-operations/release/notes/adobe-commerce/2-4-7#inventory-management-1)中。

## v1.2.6

[!DNL Inventory Management] 1.2.6 （模組版本： `magento/inventory-metapackage = 1.2.6`）受2.4.6版支援，並與2.4.0版Adobe Commerce、雲端基礎結構上的Adobe Commerce以及Magento Open Source程式碼基底相容。

![已修正問題](../assets/fix.svg)當已售出的子產品退回庫存時，店面現在會將複合產品（可設定、套件組合及群組）顯示為庫存中。 之前，店面指出複合產品在這些情況下缺貨。<!-- ACP2E-1106-->

![已修正問題](../assets/fix.svg)如果選項是以數量設為0且已啟用&#x200B;**[!UICONTROL Display out-of-stock products]**&#x200B;的方式建立，則可設定的產品選項現在會如預期般顯示在店面上，且無庫存。<!-- ACP2E-1148-->

![已修正問題](../assets/fix.svg)當庫存數量變更且產品仍有庫存時，類別頁面快取不再失效。 Adobe Commerce現在會從快取載入頁面，而不是在店麵類別頁面上的產品數量（沒有任何其他變化）變更時重新產生頁面。<!-- ACP2E-118-->

![已修正問題](../assets/fix.svg)以單一來源模式使用庫存並啟用&#x200B;**[!UICONTROL Display Out-Of-Stock Products]**&#x200B;設定時，類別清單產品計數現在正確。 Adobe Commerce現在會在計算時檢查產品是否可供銷售。<!-- ACP2E-1033-->

![已修正問題](../assets/fix.svg)啟用詳細目錄時，店內傳遞的購物車價格規則現在可如預期運作。 以前，在這些條件下，不會套用購物車價格規則產生的折扣。<!-- ACP2E-1015-->

![已修正問題](../assets/fix.svg)在排程模式下更新產品詳細目錄不再清除所有快取。 之前，「詳細目錄」索引器會清除所有設定快取。<!-- ACP2E-1003-->

![已修正問題](../assets/fix.svg)進階詳細目錄中產品的&#x200B;**[!UICONTROL Allow Multiple Boxes for Shipping]**&#x200B;屬性值現在已如預期儲存。<!-- ACP2E-992-->

![已修正問題](../assets/fix.svg) Adobe Commerce現在會在針對隨店內取貨的訂單發出部份退款銷退折讓單後，發出正確的預留補償。 以前，當管理員使用者未選取&#x200B;**[!UICONTROL Return to Stock]**&#x200B;核取方塊即建立銷退折讓單時，儲存到`inventory_reservation`資料表的預訂不正確。<!-- ACP2E-979-->

![已修正問題](../assets/fix.svg) Adobe Commerce不再於店面將可設定的產品顯示為無庫存，當其其中一個變數已在實作多來源庫存的部署中手動退回庫存時。<!-- ACP2E-952-->

![已修正問題](../assets/fix.svg)產品格線上的欄位置(**[!UICONTROL Catalog]** > **[!UICONTROL Products]**)在設定了多個詳細目錄來源的部署中重新載入頁面後，不再回復到先前的位置。<!-- ACP2E-925-->

![已修正問題](../assets/fix.svg)未選取&#x200B;**[!UICONTROL Back to stock]**&#x200B;核取方塊時，為虛擬產品簽發銷退折讓單後，庫存數量現在已正確。<!-- ACP2E-908-->

![已修正問題](../assets/fix.svg)您現在可以使用自動產品排序和指派給非預設庫存的範圍來儲存類別。 之前，Adobe Commerce未儲存類別並顯示此錯誤： `Something went wrong while saving the category`。<!-- ACP2E-859-->

![已修正問題](../assets/fix.svg)當以所有無庫存的可設定變數建立產品時，可設定的產品庫存狀態現在會如預期更新。<!-- ACP2E-813-->

![已修正問題](../assets/fix.svg)預訂不一致性分析工具現在可正確處理包含可設定、組合及分組產品的部分出貨訂單。 現在會分析複合產品型別。 以前，取消和退款只針對上階產品儲存，而不針對可設定和一起出貨的套裝產品的子產品訂單專案儲存。<!-- ACP2E-924-->

![已修正問題](../assets/fix.svg)當管理員使用者嘗試將200個或更多詳細目錄來源指派給庫存或產品時，Adobe Commerce不再顯示錯誤。<!-- ACP2E-1180-->

![已修正問題](../assets/fix.svg) Adobe Commerce現在支援為已刪除產品的訂單建立銷退折讓單。 先前，建立商業發票後，當訂單中刪除產品時，商家無法建立銷退折讓單。 應用程式顯示這個錯誤： `Following products with requested skus were not found: s00001`。 t. <!-- ACP2E-1138-->

![已修正問題](../assets/fix.svg)商店現在已根據單一和多重商店識別碼進行篩選。 `event`產品屬性代碼已新增至保留的屬性代碼清單。 之前，當存貨模組安裝時，「低存貨報表」會擲回例外狀況。<!-- ACP2E-1017-->

![已修正問題](../assets/fix.svg)階層式導覽篩選器現在可如預期運作，無存貨產品現在已附加至店麵類別產品清單。 新的`is_out_of_stock`排序屬性使用店面產品集合的Elasticsearch動態欄位對應程式。<!-- ACP2E-748-->

![已修正問題](../assets/fix.svg)當子產品庫存狀態由REST `POST /rest/V1/inventory/source-items`呼叫變更時，複合產品（套件、已分組和可設定）庫存狀態會如預期更新。<!-- ACP2E-1209-->

## v1.2.5

[!DNL Inventory Management] 1.2.5 （模組版本： `magento/inventory-metapackage = 1.2.5`）受2.4.5版支援，並與2.4.0版Adobe Commerce、雲端基礎結構上的Adobe Commerce以及Magento Open Source程式碼基底相容。

![已修正問題](../assets/fix.svg)當商家從管理員建立出貨時，套裝與分組產品的預設存貨狀態現在會如預期更新。 以前，在建立出貨後，這些產品的狀態保持不變。<!--- ACP2E-418-->

![已修正問題](../assets/fix.svg)當符合下列其中一項條件時，可設定的產品現在會回到庫存中： 1. 父產品至少有一個已儲存的庫存子項。 2.可設定的產品本身已更新並設定為&#x200B;**庫存**，而且至少有一個子項庫存。<!--- ACP2E-443-->

![已修正問題](../assets/fix.svg)透過REST API實作的詳細目錄變更現在會如預期反映在產品詳細資料頁面上。 現在，在比較上次和目前的庫存狀態後，會清除目錄產品的快取。 以前，省略回呼函式會導致不正確評估庫存狀態變更，這不會觸發必要的快取清理。 因此，店面並未反映存貨變更。<!--- ACP2E-161-->

![已修正問題](../assets/fix.svg)使用`/V1/inventory/source-items`更新來源專案後，店面現在會顯示指派給預設庫存且先前無庫存的產品。 之前，此REST API端點設定了錯誤的`stock_status`。<!--- ACP2E-562-->

![已修正問題](../assets/fix.svg)透過大量動作(**[!UICONTROL Catalog]** > **[!UICONTROL Products]** > **[!UICONTROL Select Products]** > **[!UICONTROL Actions - Unassign Inventory Source]**)取消指派存貨來源現在可如預期運作，因為來源包含的SKU重複專案，前導零除外（例如`01234`和`1234`）。 之前，應用程式不會解除指派詳細目錄來源，並擲回錯誤。<!--- ACP2E-2641-->

![已修正問題](../assets/fix.svg)啟用無限延期交貨訂單且產品已指派給自訂存貨時，無論延期交貨數量為何，產品存貨狀態現在一律為&#x200B;**庫存**。 過去，即使啟用延期交貨，產品也無庫存。<!--- ACP2E-664-->

![已修正問題](../assets/fix.svg)來源專案以`POST /V1/inventory/source-items`更新後，可設定的產品上下階產品庫存現在已正確更新。 透過API更新子產品後，用於預設庫存檢查的新庫存外掛程式會更新可設定的產品數量和狀態。<!--- ACP2E-442-->

![已修正問題](../assets/fix.svg)庫存不足的分組產品不再列在店麵類別頁面上。<!--- ACP2E-2082-->

![已修正問題](../assets/fix.svg)已在`CatalogInventory` `composer.json`中修正封裝名稱。<!--- ACP2E-2914-->

![已修正問題](../assets/fix.svg)在多來源/存貨部署中下零數量產品的訂單後，管理員現在可正確顯示延期交貨訂單狀態。 [GitHub-33756](https://github.com/magento/magento2/issues/33756) <!--- ACP2E-713-->

![已修正問題](../assets/fix.svg)當從庫存區段更新套裝產品時，沒有庫存的套裝產品不再顯示在店麵類別頁面上。<!--- ACP2E-2012-->

![已修正問題](../assets/fix.svg)已解決PHP 7.4的相容性問題。<!--- AC-3192-->

![已修正問題](../assets/fix.svg)已改善儲存作業的效能，該儲存作業包含包含許多選項（多個100）的套件組合產品。 以前，儲存這些大型套件產品需要幾分鐘的時間，而且有時會在啟用庫存服務的部署中導致逾時。 [GitHub-34732](https://github.com/magento/magento2/issues/34732) <!--- AC-1901-->

![已修正問題](../assets/fix.svg)產品大量動作工具(**[!UICONTROL Select Products]** > **[!UICONTROL Actions]** > **[!UICONTROL Assign Inventory Source]**)現在可如預期運作，當SKU重複時，將庫存來源指派給多個產品，前導的`0`除外（例如`01234`和`1234`）。 之前，僅指派給一種產品一個詳細目錄來源。 [GitHub-35171](https://github.com/magento/magento2/issues/35171) <!--- AC-2584-->

![已修正問題](../assets/fix.svg)如果詳細目錄為0，`ProductInterface.only_x_left_in_stock`欄位現在會傳回0。 之前，它會傳回null。 [GitHub-29932](https://github.com/magento/magento2/issues/29932) <!--- AC-1806-->

![已修正問題](../assets/fix.svg)您現在可以從管理員&#x200B;**[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**&#x200B;編輯預設庫存。 以前，當您嘗試從預設庫存新增或移除來源時，控制檯中會顯示JavaScript錯誤，不過您可以將網站指派給預設庫存。<!--- ACP2E-545-->

![已修正問題](../assets/fix.svg) <!--- ACP2E-274-->使用已啟用&#x200B;**[!UICONTROL Display Out-Of-Stock Products]**&#x200B;設定的詳細目錄單一來源模式時，類別清單產品計數現在正確。 新的外掛程式現在使用`AreProductsSalableInterface`和`StockConfigurationInterface`來判斷產品總數。 之前，類別產品清單傳回錯誤的產品數量。

![已修正問題](../assets/fix.svg) <!--- ACP2E-322-->啟用&#x200B;**[!UICONTROL Move out of stock to the bottom]**&#x200B;設定後，庫存更新後，可設定的產品現在會移至產品清單中的最後一個位置。 實施新的自訂資料庫查詢來否定Elasticsearch索引排序順序，這忽略啟用管理員的排序順序。 先前，啟用此設定時，可設定的產品及其子產品不會移至清單底部。

## v1.2.4

Inventory management 1.2.4 （模組版本： `magento/inventory-metapackage = 1.2.4`）支援2.4.4版，並與Adobe Commerce 2.4.0版、雲端基礎結構上的Adobe Commerce以及Magento Open Source程式碼基底相容。

![已修正問題](../assets/fix.svg) Commerce現在會在管理員產品清單檢視中顯示所有產品的正確可銷售數量值。 之前，對於庫存產品的可銷售數量，如果其SKU包含特殊字元，則會顯示空白值。<!--- MC-41936-->

![已修正問題](../assets/fix.svg)購物車與結帳動作的效能已改善，例如在有許多（約10,000個）詳細目錄來源的部署中將產品加入購物車。<!--- MC-42570-->

![已修正問題](../assets/fix.svg) [!BADGE 僅限PaaS]{type=Informative url="https://experienceleague.adobe.com/zh-hant/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"} `bin/magento inventory:reservation:list-inconsistencies`命令現在會正確處理具有部分出貨的訂單，即使資料庫遺漏預留且快取已清除亦然。 先前，當這個命令以預先清除的快取執行時，Commerce會顯示下列錯誤： `Area code is not set`。<!--- MC-42142-->


![已修正問題](../assets/fix.svg)當子項共用時，群組產品子產品的增量索引不再導致其他群組產品的索引不正確。<!--- MC-41963-->

![已修正問題](../assets/fix.svg)透過API從類別中移除產品後，店麵類別頁面現在會顯示正確的產品計數。 以前，在重新索引發生之前，類別頁面產品計數不正確。<!--- MC-42287-->

![已修正問題](../assets/fix.svg)當停用&#x200B;**[!UICONTROL Manage Stock]**&#x200B;選項時，可設定的產品現在可在建立銷退折讓單時傳回庫存。 以往，停用此選項時，Commerce不會在銷退折讓單建立頁面上顯示&#x200B;**返回存貨**&#x200B;核取方塊。<!--- MC-42002-->

![已修正問題](../assets/fix.svg)超過10,000個專案的存貨存貨管理已改善。 以前，績效問題有時會阻止商家在啟動其網站之前編輯管理員中的庫存。<!--- MC-42643-->

![已修正問題](../assets/fix.svg) Admin中的&#x200B;**[!UICONTROL User Roles]**&#x200B;頁面已更新，為管理員提供傳遞方法設定的受限制許可權存取權。 _送貨方法_&#x200B;區段已重新命名為&#x200B;_[!UICONTROL Delivery methods]_，且&#x200B;_[!UICONTROL In-Store Pickup]_&#x200B;已移至&#x200B;_[!UICONTROL Delivery methods]_&#x200B;區段下方。 [GitHub-30053](https://github.com/magento/magento2/issues/30053) <!--- MC-41545-->

![已修正問題](../assets/fix.svg) API更新銷退折讓單後，Adobe Commerce不再建立重複的產品預訂。<!--- MC-41757-->

![已修正問題](../assets/fix.svg)在結帳工作流程中，從&#x200B;_[!UICONTROL Pick up in Store]_&#x200B;標籤切換至&#x200B;_[!UICONTROL Shipping]_&#x200B;標籤時，若只有店內收取傳遞可用，將不再觸發JavaScript錯誤。<!--- MC-42808-->

![已修正問題](../assets/fix.svg)可銷售產品數量與庫存產品數量現在已正確同步。 以前，系統不會為取消的訂單重新建立存貨預留補償。<!--- MC-42485-->

![已修正問題](../assets/fix.svg)驗證程式的效能已最佳化，以防止將新來源新增至出貨型別為`Ship Together`的捆綁產品的子產品。<!--- MC-43039-->

## 1.2.3

[!DNL Inventory Management] 1.2.3 （模組版本： `magento/inventory-metapackage = 1.2.3`）受2.4.3版支援，並與2.4.0版Adobe Commerce、雲端基礎結構上的Adobe Commerce以及Magento Open Source程式碼基底相容。

![已修正問題](../assets/fix.svg)已修正多個與前端複合產品可見性相關的問題。

![已修正問題](../assets/fix.svg)以最低必要數量改善購物車頁面管理效能。

![已修正問題](../assets/fix.svg)針對解決來源建立、無存貨料號、存貨來源、排序已配置來源、店內交貨及存貨命令等問題的數個修正。

![已修正問題](../assets/fix.svg) [!DNL Commerce]現在支援店內傳遞的加拿大郵遞區號（3位數）。 由於`geonames.org`所設定的限制，不支援六位數的代碼。

![已修正問題](../assets/fix.svg)管理員現在會在&#x200B;**產品**&#x200B;格線和&#x200B;**編輯產品**&#x200B;頁面上針對多存放區部署，顯示已停用產品的正確預設庫存數量。

![已修正問題](../assets/fix.svg) [!DNL Commerce]現在會在套件產品有庫存時重新整理類別產品快取。

## 1.2.2

[!DNL Inventory Management] 1.2.2 （模組版本： `magento/inventory-metapackage = 1.2.2`）受2.4.2版支援，並與2.4.0版Adobe Commerce、雲端基礎結構上的Adobe Commerce以及Magento Open Source程式碼基底相容。

![已修正問題](../assets/fix.svg)已修正多個與前端複合產品可見性相關的問題。

![已修正問題](../assets/fix.svg)在B2B的數量更新期間改善購物車頁面效能。

![已修正問題](../assets/fix.svg)數個修正已鎖定目標，以解決店內取貨、大量更新和存貨臨界值的問題。

![新](../assets/new.svg) **功能測試。**&#x200B;引進了新的功能測試，並為現有測試提供修正，使其更穩定。

## 1.2.1

[!DNL Inventory Management] 1.2.1 （模組版本： `magento/inventory-metapackage = 1.2.1`）受2.4.1版支援，並與2.4.0版Adobe Commerce、雲端基礎結構上的Adobe Commerce以及Magento Open Source程式碼基底相容。

![已修正問題](../assets/fix.svg)已修正與`inventory_cleanup_reservations` cron工作相關的已知問題，並已解決與套件組合產品的店內收取功能相關的問題。 此更新也包含存貨計算、套件組合產品支援和延期交貨功能的一般改善。

![新](../assets/new.svg) **功能測試。**&#x200B;引入新的功能測試，以提供額外的店內收取功能涵蓋範圍。

## 1.2.0

[!DNL Inventory Management] 1.2.0 （模組版本： `magento/inventory-metapackage = 1.2.0`）支援Adobe Commerce 2.4.0版、雲端基礎結構上的Adobe Commerce以及Magento Open Source程式碼基底。

![已修正問題](../assets/fix.svg)許多修正可解決來源指派、可擴充環境功能支援，以及與PHP 7.4、MySQL 8和PHPUNIT 9的相容性問題。

![新的](../assets/new.svg) **店內傳遞方法。**&#x200B;新增選項，讓使用者選取要做為結帳期間取車位置的來源。 請參閱&#x200B;_銷售和購買體驗指南_&#x200B;中的[店內傳遞](../stores-purchase/shipping-in-store-delivery.md)。

![新](../assets/new.svg) **多來源模式的套件組合產品支援。**&#x200B;詳細目錄支援具有多個來源的所有產品型別。

![新增](../assets/new.svg) **非同步庫存重新索引。**&#x200B;已新增非同步重新索引股票的功能，並改善數個關鍵案例的效能。

![新](../assets/new.svg) **大量介面。**&#x200B;引入新的大量介面以進行可用性檢查： `\Magento\InventorySalesApi\Api\AreProductsSalableInterface`，`\Magento\InventorySalesApi\Api\AreProductsSalableForRequestedQtyInterface`。

![新](../assets/new.svg) **已增加測試涵蓋範圍。**&#x200B;自動化測試涵蓋新功能，包括探索及修正問題的延伸涵蓋範圍。

![已知問題](../assets/bug.svg) **已知問題。**&#x200B;保留中繼資料中缺少`object_id`欄位，導致`inventory_cleanup_reservations` cron工作無法正常運作。 此問題已在[magento/inventory#3046](https://github.com/magento/inventory/pull/3046)中引入。

**因應措施：**&#x200B;執行下列MySQL查詢以手動清除保留：

```sql
SELECT GROUP_CONCAT(reservation_id) FROM inventory_reservation GROUP BY stock_id, sku HAVING SUM(quantity) = 0;
DELETE FROM inventory_reservation where reservation_id IN (result_of_the_first_query);
```

## 1.1.6

[!DNL Inventory Management] 1.1.6 （模組版本： `inventory-composer-metapackage = 1.1.6`）受到版本2.3.6的支援，並與Adobe Commerce版本2.3.5、2.3.4、2.3.3、2.3.2、2.3.1和2.3.0、雲端基礎結構上的Adobe Commerce以及Magento Open Source程式碼基底相容。

![已修正問題](../assets/fix.svg)修正以解決延期交貨、銷退折讓單、低庫存報表格線、連線至「解決不一致」CLI工具的修正及一般改善相關的問題。

![新增](../assets/new.svg) **非同步庫存重新索引。**&#x200B;已新增非同步重新索引股票的功能，並改善數個關鍵案例的效能。

## 1.1.5

[!DNL Inventory Management] 1.1.5 （模組版本： `inventory-composer-metapackage = 1.1.5`）受到版本2.3.5的支援，並與Adobe Commerce版本2.3.4、2.3.3、2.3.2、2.3.1和2.3.0、雲端基礎結構上的Adobe Commerce以及Magento Open Source程式碼基底相容。

![新](../assets/new.svg) **產品SKU變更後更新詳細目錄。**&#x200B;引入新的組態設定以切換至新的行為：「與目錄同步」。

![新](../assets/new.svg) **功能測試。**&#x200B;引入新功能測試以消除測試涵蓋範圍差距。 修正數個問題，讓測試更穩定可靠)。

![已知問題](../assets/bug.svg)修正以防止產品過度銷售、店面上的「無庫存」產品可見度、大量針對可擴充環境支援和使用者介面改良的修正。

## 1.1.4

[!DNL Inventory Management] 1.1.4 （模組版本： `inventory-composer-metapackage = 1.1.4`）受到版本2.3.4的支援，並與Adobe Commerce版本2.3.3、2.3.2、2.3.1和2.3.0、雲端基礎結構上的Adobe Commerce以及Magento Open Source程式碼基底相容。

![已修正問題&#x200B;](../assets/fix.svg)**效能提高。**&#x200B;已針對清查保留區CLI命令引入聚束邏輯，以減少記憶體使用量，並避免處理程式停滯且沒有任何回應的情況。

![新&#x200B;](../assets/new.svg)**增加測試涵蓋範圍。**&#x200B;引進了許多新功能測試。 幾乎所有手動清查案例都包含自動化測試。

![已知問題](../assets/bug.svg)許多修正都是針對解決銷退折讓單、分組產品、來源與庫存整批作業的問題。

## 1.1.3

[!DNL Inventory Management] 1.1.3 （模組版本： `inventory-composer-metapackage = 1.1.3`）支援2.3.3版，並與Adobe Commerce版本2.3.2、2.3.1和2.3.0、雲端基礎結構上的Adobe Commerce以及Magento Open Source程式碼基底相容。

![已修正問題&#x200B;](../assets/fix.svg)**與Adobe Commerce和B2B功能更整合。** [!DNL Inventory Management]現在可搭配下列功能正常運作，適用於使用非預設庫存來源和庫存的網站：

- 依SKU排序(Adobe Commerce)
- 快速訂購(B2B)
- 請購單清單(B2B)

![新&#x200B;](../assets/new.svg)**效能提高。針對執行預設詳細目錄庫存和來源的網站，**&#x200B;店面目錄瀏覽效能已有所改善。

![新&#x200B;](../assets/new.svg)**增加測試涵蓋範圍。**&#x200B;自動化功能和整合測試的涵蓋範圍已大幅增加。

## 1.1.2

[!DNL Inventory Management] 1.1.2 （模組版本： `inventory-composer-metapackage = 1.1.2`）受到版本2.3.2的支援，並且與Adobe Commerce版本2.3.1和2.3.0、雲端基礎結構上的Adobe Commerce以及Magento Open Source程式碼基底相容。

![已修正問題](../assets/fix.svg)已新增`source_code`至GET `/V1/shipments` REST端點的回應。<!-- https://github.com/magento/inventory/pull/2142 -->

![已修正問題](../assets/fix.svg)已解決下列問題：在未出貨訂單發出銷退折讓單之後，正確清除預留並更新產品數量。 當您選取<!-- https://github.com/magento/inventory/pull/2179 -->的選項時

![已修正問題](../assets/fix.svg)已解決問題，以在產品建立期間輸入數量時，正確儲存可設定產品子項的數量。<!-- https://github.com/magento/inventory/pull/2158 -->

[!DNL Inventory Management] 1.1.2 Beta的新模組包括：

```php
        'Magento_InventoryGraphQl' => 1,
        'Magento_InventoryReservations' => 1,
        'Magento_InventoryReservationsApi' => 1,
        'Magento_InventoryReservationCli' => 1,
        'Magento_InventoryExportStock' => 0,
        'Magento_InventoryExportStockApi' => 0,
```

![新](../assets/new.svg) **新增大量部分存貨移轉端點** — 目前的大量移轉端點會將所有指派的數量從來源移至目的地來源。 新的`/rest/V1/inventory/bulk-partial-source-transfer`端點可讓商家以大量作業將部分存貨從來源轉移到來源。 若要轉移特定數量的數量，請輸入具有`sku`、`qty`、`origin_source_code`和`destination_source_code`的端點要求。 傳輸確認來源已指派給`sku`、有足夠數量可供傳輸，以此類推。 請參閱REST API檔案中的[詳細目錄大量動作](https://developer.adobe.com/commerce/webapi/rest/inventory/bulk-inventory/){target="_blank"}。<!-- https://github.com/magento/inventory/pull/2117 -->

![新](../assets/new.svg) **新增的保留專案CLI** — 新命令為您提供偵測和解決保留專案不一致問題的選項。 當訂單提交並變更狀態時，[!DNL Inventory Management]會透過報酬預留產生初始預留和更新。 這些命令會依訂單ID、SKU和庫存ID傳回偵測到的不一致清單，並建立要解決的預留量。 如需詳細資訊，請參閱[CLI參考](cli.md)。<!-- https://github.com/magento/inventory/pull/2199 https://github.com/magento/inventory/pull/2184 https://github.com/magento/inventory/pull/2171 https://github.com/magento/inventory/pull/2148  -->

![新](../assets/new.svg) **來源和SSA選項的效能改善** — 在出貨期間排序和選取來源導致來源數量高的存貨效能降低。 此版次在複查及選取出貨的SSA選項時，大幅改善可用來源清單與排序的效能。<!-- https://github.com/magento/inventory/pull/2056 https://github.com/magento/inventory/pull/2090 -->

![新](../assets/new.svg) **已新增Inventory management的GraphQL支援** — 此版本會安裝新的`magento/module-inventory-graph-ql`模組。 GraphQL [ProductInterface屬性](https://developer.adobe.com/commerce/webapi/graphql/schema/products/interfaces/attributes/){target="_blank"}現在包含[!DNL Inventory Management]支援的`only_x_left_in_stock`和`stock_status`屬性。<!-- https://github.com/magento/inventory/pull/2124 -->

![新](../assets/new.svg) **指派來源的簡化UI** — 產品頁面中的「指派的來源」表格已簡化內容，以便更輕鬆更新，並且在顯示許多來源時提高效能。 依來源名稱列出所有來源（將游標停留在`source_code`上）。

![新的](../assets/new.svg) **匯出彙總存量服務** — 此版本提供新的匯出彙總存量服務（保留系統中的預留）以支援外部銷售管道，例如Amazon、eBay和Google購物廣告。 <!-- https://github.com/magento/inventory/pull/2067 -->

## 1.1.0

[!DNL Inventory Management] 1.1.0 （模組版本： `inventory-composer-metapackage = 1.1.0`）受到支援，並且與Adobe Commerce 2.3.0版、雲端基礎結構上的Adobe Commerce以及Magento Open Source程式碼基底相容。 [!DNL Inventory Management] 1.1.1僅以套件名稱更新的形式發行，支援2.3.1版，並與2.3.0版Adobe Commerce、雲端基礎結構上的Adobe Commerce以及Magento Open Source程式碼基底相容。

![已修正問題](../assets/fix.svg) **新增對單一和多來源模式Elasticsearch的支援** — 您現在可以設定並使用具有自訂庫存的Elasticsearch。 如需安裝資訊，請參閱[設定Elasticsearch服務](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/service/elasticsearch.html?lang=zh-Hant){target="_blank"}。<!-- PR https://github.com/magento/inventory/pull/1943 -->

![已修正問題](../assets/fix.svg)已解決預設庫存的效能問題，以大幅提升許多作業的效能。 改良功能可提升單一來源模式、「移轉存貨至Source」、「店麵類別」頁面及「可銷售數量」計算的效能。

<!-- All Performance Track issues resolved https://github.com/magento/inventory/issues?q=is%3Aopen+is%3Aissue+label%3APerformance -->

![已修正問題](../assets/fix.svg)已解決無存貨狀態的問題，以及可設定組態產品與分組產品的大量存貨移轉至存貨。 選取父級產品並執行大量動作不會影響產品狀態。 如果父產品有庫存，則保持有庫存。

<!-- PR https://github.com/magento/inventory/pull/1972 -->

![新的](../assets/new.svg) **距離優先順序演演算法** — 距離優先順序演演算法是全新的現成Source選擇演演算法，適用於以距離為基礎的送貨建議。 此演演算法會將出貨目的地地址的地點與來源地點做比較，以決定最接近完成出貨的來源。 距離可透過實體距離或使用匯入的地理碼位置資料或Google方向（駕駛、步行或騎腳踏車）從一個位置到另一個位置所花費的時間來決定。

![新](../assets/new.svg) **擴充來源數量清單** — 擁有大量來源的商家，可透過「產品格線」輕鬆暫留並檢視每個產品的所有來源。 每項產品至少會顯示五個來源與相符數量。 將滑鼠游標停留在來源上時，可以捲動瀏覽整個來源清單和目前數量。

![已知問題](../assets/bug.svg) Magento Open Source和Adobe Commerce v2.3.1的已知問題 — 由於主題名稱反映PHP類別和方法名稱的非同步API有所變更，來源之間的非同步資料移轉會遇到問題。 建議使用同步作業，將&#x200B;**[!UICONTROL Run asynchronously]**&#x200B;設定為`No`。
