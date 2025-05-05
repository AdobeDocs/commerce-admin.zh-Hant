---
title: 安裝、更新及移除 [!DNL Inventory Management]
description: 瞭解如何管理 [!DNL Inventory Management] 中繼資料。
exl-id: d088ff35-c0e1-41c8-89fb-78180eaefbf7
level: Experienced
feature: Inventory, Install
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hant/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 0%

---

# 安裝、更新及移除[!DNL Inventory Management]

[!DNL Inventory Management]模組為單一來源和多來源商家提供所有存貨功能與選項，以管理銷售管道的產品數量與存貨。 Adobe Commerce和Magento Open Source的2.4.x版提供這些功能。

這些功能和擴充功能是透過Magento Open Source社群工程計劃開發為[詳細目錄專案](https://github.com/magento/inventory)的一部分。

[!DNL Inventory Management]安裝在Adobe Commerce和Magento Open Source的2.3.x和2.4.x版本中，並依預設啟用所有功能。 啟用這些詳細目錄功能不需要額外的步驟。 從v2.1.x或2.2.x升級可能需要額外的步驟。 請參閱[升級Inventory management](#upgrade-inventory-management)。

建議根據[快速入門內部部署安裝](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/composer.html?lang=zh-Hant){target="_blank"}進行安裝。 使用中繼安裝以接收所有[!DNL Inventory Management]模組。

`composer.json`中繼封裝中的下列行安裝[!DNL Inventory Management]：

```json
        magento/inventory-composer-metapackage = 1.1.3
```

如需[!DNL Inventory Management]中繼套件版本的清單，請參閱[發行說明](release-notes.md)。

[!DNL Inventory Management]安裝程式將所有模組新增至`<Magento_installation_directory>/app/etc/config.php`檔案。 `1`值表示對應的模組已啟用。 已新增下列模組清單：

```php
        'Magento_Inventory' => 1,
        'Magento_InventoryAdminUi' => 1,
        'Magento_InventoryAdvancedCheckout' => 1,
        'Magento_InventoryApi' => 1,
        'Magento_InventoryBundleProduct' => 1,
        'Magento_InventoryBundleProductAdminUi' => 1,
        'Magento_InventoryCatalog' => 1,
        'Magento_InventorySales' => 1,
        'Magento_InventoryCatalogAdminUi' => 1,
        'Magento_InventoryCatalogApi' => 1,
        'Magento_InventoryCatalogSearch' => 1,
        'Magento_InventoryConfigurableProduct' => 1,
        'Magento_InventoryConfigurableProductAdminUi' => 1,
        'Magento_InventoryConfigurableProductIndexer' => 1,
        'Magento_InventoryConfiguration' => 1,
        'Magento_InventoryConfigurationApi' => 1,
        'Magento_InventoryDistanceBasedSourceSelection' => 1,
        'Magento_InventoryDistanceBasedSourceSelectionAdminUi' => 1,
        'Magento_InventoryDistanceBasedSourceSelectionApi' => 1,
        'Magento_InventoryElasticsearch' => 1,
        'Magento_InventoryExportStockApi' => 1,
        'Magento_InventoryIndexer' => 1,
        'Magento_InventorySalesApi' => 1,
        'Magento_InventoryGroupedProduct' => 1,
        'Magento_InventoryGroupedProductAdminUi' => 1,
        'Magento_InventoryGroupedProductIndexer' => 1,
        'Magento_InventoryImportExport' => 1,
        'Magento_InventoryCache' => 1,
        'Magento_InventoryLowQuantityNotification' => 1,
        'Magento_InventoryLowQuantityNotificationApi' => 1,
        'Magento_InventoryMultiDimensionalIndexerApi' => 1,
        'Magento_InventoryProductAlert' => 1,
        'Magento_InventoryRequisitionList' => 1,
        'Magento_InventoryReservations' => 1,
        'Magento_InventoryReservationCli' => 1,
        'Magento_InventoryReservationsApi' => 1,
        'Magento_InventoryExportStock' => 1,
        'Magento_InventorySalesAdminUi' => 1,
        'Magento_InventorySalesFrontendUi' => 1,
        'Magento_InventorySetupFixtureGenerator' => 1,
        'Magento_InventoryShipping' => 1,
        'Magento_InventorySourceDeductionApi' => 1,
        'Magento_InventorySourceSelection' => 1,
        'Magento_InventorySourceSelectionApi' => 1,
        'Magento_InventoryLowQuantityNotificationAdminUi' => 1,
        'Magento_InventoryShippingAdminUi' => 1,
        'Magento_InventoryGraphQl' => 1,
```

## 啟用[!DNL Inventory Management]功能

安裝、升級或更新時，預設啟用Admin中的&#x200B;_[!UICONTROL Manage Stock]_&#x200B;選項。 此選項可啟用存貨追蹤和管理，但不會影響模組狀態。 若要停用模組，請參閱下一節。

如需設定的詳細資訊，請參閱[設定Inventory management](configuration.md)。

## 停用Inventory management

>[!IMPORTANT]
>
>強烈建議使用預設的[!DNL Inventory Management]模組。 用於停用[!DNL Inventory Management]模組的系統的替代[!DNL CatalogInventory]模組現已棄用。 停用[!DNL Inventory Management]模組可能會造成系統不穩定，並導致各種問題。

您可能要停用[!DNL Inventory Management]模組以：

* 加速從2.0.x、2.1.x、2.2.x或2.3.x移轉至2.4.x的商戶升級流程。
* 使用自訂或第三方存貨及訂單管理系統模組。

請參閱&#x200B;_安裝指南_&#x200B;中的[啟用或停用模組](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html?lang=zh-Hant)頁面，瞭解如何停用適用模組的相關資訊。

完成時，系統會在`<Magento_installation_directory>/app/etc/config.php`中提供模組和值的清單，開頭為：

```php
   'Magento_Inventory' => 0,
   'Magento_InventoryAdminUi' => 0,
   'Magento_InventoryAdvancedCheckout' => 0,
   ...
```

>[!IMPORTANT]
>
>如果您已安裝OMS Connector模組，請確定您沒有停用`Magento_InventoryMessageBus`模組，此模組為聯結器模組。 需要搭配OMS使用聯結器。

## 移除Inventory management

>[!IMPORTANT]
>
>強烈建議使用預設的[!DNL Inventory Management]模組。 替代[!DNL CatalogInventory]模組用於已移除[!DNL Inventory Management]模組的系統，現已棄用。 移除[!DNL Inventory Management]模組可能會造成系統不穩定，並導致各種問題。

如果您選擇不使用[!DNL Inventory Management]功能，可以移除（解除安裝）這些模組。 若要透過Composer檔案移除所有模組，請將下列專案新增至`composer.json`：

```
"replace": {
        "magento/module-inventory": "*",
        "magento/module-inventory-admin-ui": "*",
        "magento/module-inventory-advanced-checkout": "*",
        "magento/module-inventory-api": "*",
        "magento/module-inventory-bundle-product": "*",
        "magento/module-inventory-bundle-product-admin-ui": "*",
        "magento/module-inventory-cache": "*",
        "magento/module-inventory-catalog": "*",
        "magento/module-inventory-catalog-admin-ui": "*",
        "magento/module-inventory-catalog-api": "*",
        "magento/module-inventory-catalog-search": "*",
        "magento/module-inventory-configurable-product": "*",
        "magento/module-inventory-configurable-product-admin-ui": "*",
        "magento/module-inventory-configurable-product-indexer": "*",
        "magento/module-inventory-configuration": "*",
        "magento/module-inventory-configuration-api": "*",
        "magento/module-inventory-distance-based-source-selection": "*",
        "magento/module-inventory-distance-based-source-selection-admin-ui": "*",
        "magento/module-inventory-distance-based-source-selection-api": "*",
        "magento/module-inventory-export-stock": "*",
        "magento/module-inventory-export-stock-api": "*",
        "magento/module-inventory-elasticsearch": "*",
        "magento/module-inventory-graph-ql": "*",
        "magento/module-inventory-grouped-product": "*",
        "magento/module-inventory-grouped-product-admin-ui": "*",
        "magento/module-inventory-grouped-product-indexer": "*",
        "magento/module-inventory-import-export": "*",
        "magento/module-inventory-indexer": "*",
        "magento/module-inventory-low-quantity-notification": "*",
        "magento/module-inventory-low-quantity-notification-admin-ui": "*",
        "magento/module-inventory-low-quantity-notification-api": "*",
        "magento/module-inventory-multi-dimensional-indexer-api": "*",
        "magento/module-inventory-product-alert": "*",
        "magento/module-inventory-requisition-list": "*",
        "magento/module-inventory-reservations": "*",
        "magento/module-inventory-reservations-api": "*",
        "magento/module-inventory-reservation-cli": "*",
        "magento/module-inventory-sales": "*",
        "magento/module-inventory-sales-admin-ui": "*",
        "magento/module-inventory-sales-api": "*",
        "magento/module-inventory-sales-frontend-ui": "*",
        "magento/module-inventory-setup-fixture-generator": "*",
        "magento/module-inventory-shipping": "*",
        "magento/module-inventory-shipping-admin-ui": "*",
        "magento/module-inventory-source-deduction-api": "*",
        "magento/module-inventory-source-selection": "*",
        "magento/module-inventory-source-selection-api": "*",
        "magento/module-inventory-visual-merchandiser": "*",
        "magento/module-inventory-swatches-frontend-ui": "*",
        "magento/module-inventory-quote-graph-ql": "*",
        "magento/module-inventory-in-store-pickup": "*",
        "magento/module-inventory-in-store-pickup-sales": "*",
        "magento/module-inventory-in-store-pickup-admin-ui": "*",
        "magento/module-inventory-in-store-pickup-sales-admin-ui": "*",
        "magento/module-inventory-in-store-pickup-api": "*",
        "magento/module-inventory-in-store-pickup-sales-api": "*",
        "magento/module-inventory-in-store-pickup-frontend": "*",
        "magento/module-inventory-in-store-pickup-shipping": "*",
        "magento/module-inventory-in-store-pickup-graph-ql": "*",
        "magento/module-inventory-in-store-pickup-shipping-admin-ui": "*",
        "magento/module-inventory-in-store-pickup-multishipping": "*",
        "magento/module-inventory-in-store-pickup-shipping-api": "*",
        "magento/module-inventory-in-store-pickup-quote": "*",
        "magento/module-inventory-in-store-pickup-webapi-extension": "*",
        "magento/module-inventory-in-store-pickup-quote-graph-ql": "*",
        "magento/module-inventory-configurable-product-frontend-ui": "*",
        "magento/module-inventory-catalog-search-configurable-product": "*",
        "magento/module-inventory-catalog-search-bundle-product": "*",
        "magento/module-inventory-catalog-frontend-ui": "*",
        "magento/module-inventory-bundle-import-export": "*",
        "magento/module-inventory-bundle-product-indexer": "*"
    }
```

完成此變更後，請執行撰寫器安裝，並自動移除這些Inventory management模組。

## 升級Inventory management

### 先前的[!DNL Commerce]版本

將現有的2.1.x、2.2.x或2.3.x安裝升級或更新為Adobe Commerce或Magento Open Source 2.4.x時，預設會停用[!DNL Inventory Management]模組。 此預設設定是避免升級與舊版不相容，以及更支援Order Management (OMS)的預防措施。

>[!NOTE]
>
>Order Management不支援[!DNL Inventory Management]。 升級時，[!DNL Inventory Management]模組已停用，以允許OMS和[!DNL Commerce] 2.3.x順暢地運作。


若要啟用[!DNL Inventory Management]模組：

1. 編輯`<Commerce_installation_directory>/app/etc/config.php`檔案。
1. 將所有詳細目錄模組從`0`修改為`1`以啟用。
1. 更新資料庫：

   ```bash
   bin/magento setup:upgrade
   ```

1. 清除快取：

   ```bash
   bin/magento cache:clean
   ```

建議您在升級後使用[保留不一致命令](cli.md)。 升級時，您的所有產品都會新增至預設庫存。 如果您有暫緩訂單，這些指令會正確更新銷售與訂單履行的可銷售數量與預留。

### 先前的[!DNL Inventory Management]版本

從舊版[!DNL Inventory Management]升級至最新版本時，請遵循一般擴充功能升級步驟。

如需最新資訊，請更新您的中繼資料版本：

```json
        magento/inventory-composer-metapackage = 1.1.3
```

請參閱下列指南，以取得有關Commerce升級的詳細資訊：

* [Commerce更新指南](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/overview.html?lang=zh-Hant){target="_blank"}
* [啟用或停用模組](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html?lang=zh-Hant){target="_blank"}
