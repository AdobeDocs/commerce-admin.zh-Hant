---
title: 安裝 [!DNL Adobe Commerce B2B] 擴充功能
description: 瞭解如何安裝 [!DNL Adobe Commerce B2B] 中繼套件。
feature: B2B, Install
role: Admin, Developer
exl-id: a6947212-1708-40ae-9e81-874467eba5e1
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"
source-git-commit: 25964363ca5c4ec849e231d4eccb5f60b682a499
workflow-type: tm+mt
source-wordcount: '1149'
ht-degree: 0%

---


# 安裝[!DNL Adobe Commerce B2B]擴充功能

Adobe Commerce B2B擴充功能`magento/extension-b2b`適用於所有受支援的Adobe Commerce版本。 它會在安裝Adobe Commerce之後安裝。


## 需求

- [Adobe Commerce](https://business.adobe.com/products/magento/magento-commerce.html)，所有支援的版本
- PHP 8.1、8.2和8.3 （需要B2B 1.5.0）
- [!DNL Composer]

>[!IMPORTANT]
>
>Adobe Commerce B2B 1.4.2+版與PHP 8.3不相容。如果您將Commerce執行個體升級至Commerce 2.4.7+版，請確定執行個體上安裝的PHP版本是PHP 8.2，以保持與B2B 1.4.2+的相容性。

## 支援平台

- 雲端基礎結構上的Adobe Commerce (ECE)
- Adobe Commerce內部部署(EE)

## 安裝步驟

>[!BEGINSHADEBOX]

**必要條件**

- 存取[repo.magento.com](https://repo.magento.com/)以下載擴充功能。 如需金鑰產生與取得必要許可權，請參閱[取得您的驗證金鑰](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys)。

  在[COMPOSER_HOME](https://getcomposer.org/doc/03-cli.md#composer-home)目錄中全域定義驗證金鑰，以儲存驗證金鑰以供安裝。 或者，將它們儲存至Adobe Commerce應用程式根目錄中的[auth.json](https://developer.adobe.com/commerce/contributor/guides/install/clone-repository/#authentication-file)檔案。

- [支援的B2B擴充功能版本](https://experienceleague.adobe.com/en/docs/commerce-operations/release/product-availability) — 決定部署的Adobe Commerce版本支援的最新B2B擴充功能版本。

- 請檢視發行說明，瞭解版本相容性、更新或變更的最新資訊，這些可能會影響安裝或升級需求。

   - [B2B發行說明](release-notes.md)
   - [Adobe Commerce發行說明](https://experienceleague.adobe.com/en/docs/commerce-operations/release/versions)

>[!ENDSHADEBOX]

使用撰寫器安裝B2B擴充功能(`magento/b2b-extension`)。 此擴充功能是撰寫器中繼資料，其中包括可為Adobe Commerce執行個體啟用B2B功能的模組集合。 如需包含的模組清單，請參閱[B2B封裝](packages.md)。

>[!BEGINTABS]

>[!TAB 雲端基礎結構]

>[!TIP]
>
>在雲端基礎結構上安裝Adobe Commerce B2B時，Adobe建議您先將Adobe Commerce應用程式部署至整合或預備環境，再開始進行。

將B2B擴充功能新增至專案時，Adobe建議在開發分支中工作。 如果您沒有分支，請參閱[為開發建立分支](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches)。 安裝B2B副檔名時，`Magento_B2b`副檔名會自動插入`app/etc/config.php`檔案中。 不需要直接編輯檔案。

**若要安裝B2B擴充功能**：

1. 在本機工作站上，變更至專案目錄。

1. 建立或簽出開發分支。

1. 將B2B副檔名新增至`composer.json`檔案的`require`區段。

   ```bash
   composer require magento/extension-b2b --no-update
   ```

1. 更新專案相依性。

   ```bash
   composer update
   ```

1. 新增、提交和推送程式碼變更。

   ```bash
   git add -A
   ```

   ```bash
   git commit -m "Install the B2B extension."
   ```

   ```bash
   git push origin <branch-name>
   ```

   >[!NOTE]
   >
   >將更新推播至雲端環境會啟動Commerce雲端部署流程以套用變更。 從[部署記錄](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process)檢查部署狀態。 如果您遇到部署錯誤，請參閱[從元件失敗復原](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/recover-failed-deployment)。

1. 建置和部署完成後，請使用SSH登入遠端環境，並確認已安裝並啟用B2B擴充功能。

   ```bash
   bin/magento module:status Magento_B2b
   ```

   副檔名使用格式： `<VendorName>_<ComponentName>`。

   範例回應：

   ```
   Magento_B2b : Module is enabled
   ```

>[!TAB 內部部署]

1. 從Adobe Commerce應用程式根目錄中，更新`composer.json`以新增B2B擴充功能的相依性：

   ```bash
   composer require magento/extension-b2b:<version>
   ```

   如果發生錯誤，例如：

   ```
   [InvalidArgumentException] Could not find a matching version of package magento/extension-b2b.
   ```

   檢查套件拼字、版本限制，以及套件是否可用且符合您的最低穩定性（穩定）要求。

1. 如果出現提示，請輸入您的[驗證金鑰](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys)。

   您的&#x200B;_公開金鑰_&#x200B;是您的使用者名稱；_私密金鑰_&#x200B;是您的密碼。 如果您已將您的公開金鑰和私密金鑰儲存在`auth.json`，系統不會提示您進行驗證。

1. 在Composer完成更新模組後執行下列命令：

   ```bash
   bin/magento setup:upgrade
   ```

   ```bash
   bin/magento setup:di:compile
   ```

   ```bash
   bin/magento setup:static-content:deploy -f
   ```

   ```bash
   bin/magento cache:clean
   ```

   >[!NOTE]
   >
   >在生產模式中，您可能會收到傳送給`Please rerun Magento compile command`的訊息。 輸入命令以完成安裝。 Adobe Commerce不會提示您以開發人員模式執行編譯命令。

>[!ENDTABS]

完成安裝之後，請設定並啟動訊息取用者。

## 訊息消費者

Adobe Commerce B2B擴充功能使用MySQL進行訊息佇列管理。 下表列出支援B2B功能的訊息消費者。 安裝擴充功能後，針對您的Commerce店面所需的B2B功能啟動訊息消費者。

| 消費者 | 說明 |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sharedCatalogUpdatePrice` | 更新共用目錄中每個產品的價格。 在系統管理員組態設定中啟用[**[!UICONTROL Shared Catalogs]**](catalog-shared.md)選項時為必要。 |
| `sharedCatalogUpdateCategoryPermissions` | 更新指派給共用目錄類別的類別。 在系統管理員組態設定中啟用[**[!UICONTROL Shared Catalogs]**](catalog-shared.md)選項時為必要。 |
| `negotiableQuotePriceUpdate` | 更新可轉讓報價的價格。 在系統管理員組態設定中啟用[**[!UICONTROL Quotes]**](quotes.md)選項時為必要。 |
| `purchaseorder.toorder` | 將採購單轉換為訂單。 在系統管理員組態設定中啟用[**[!UICONTROL Purchase Orders]**](purchase-order-flow.md)選項時為必要。 |
| `purchaseorder.transactional.email` | 傳送採購單電子郵件。 在系統管理員組態設定中啟用[**[!UICONTROL Purchase Orders]**](purchase-order-flow.md)選項時為必要。 |
| `purchaseorder.validation` | 依據相關[核准規則](account-dashboard-approval-rules.md)驗證採購單。 在系統管理員組態設定中啟用[**[!UICONTROL Purchase Orders]**](purchase-order-flow.md)選項時為必要。 |
| `quoteItemCleaner` | 當產品從目錄中刪除或從購物車中移除時，會刪除無效或無效的報價單。 在系統管理員組態設定中啟用[**[!UICONTROL Quotes]**](quotes.md)選項時為必要。 |
| `inventoryQtyCounter` | 下訂單或移除產品後，以非同步方式修正股票指數。 在管理員組態設定中啟用Inventory management的[**[!UICONTROL Use deferred stock update]**](../configuration-reference/catalog/inventory.md#product-stock-options)選項時為必要。 請參閱[效能最佳實務](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/configuration#deferred-stock-update)。 |
| `async.operations.all` | 為[大量作業](https://developer.adobe.com/commerce/php/development/components/message-queues/bulk-operations/)的每個個別工作建立訊息，例如匯入或匯出料號、變更大量價格，以及將產品指定至倉庫。 當[!DNL Inventory Management]的&#x200B;[**Admin大量作業**](../configuration-reference/catalog/inventory.md#admin-bulk-operations)&#x200B;選項設定為&#x200B;**非同步執行**&#x200B;時，此為必要專案。 |

{style="table-layout:auto"}

>[!NOTE]
>
>如需所有Adobe Commerce訊息使用者的清單，請參閱&#x200B;_設定指南_&#x200B;中的[訊息佇列使用者](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/consumers)。

### 設定訊息使用者

當您針對B2B功能[啟動訊息消費者](#start-message-consumers)時，新增下列引數，以防止可能的處理問題或延遲。

- `--max-messages <value>` — 指定每個取用者在終止前必須處理的訊息數目上限(預設值= 10000)。 雖然Adobe不建議這麼做，但您可以使用0來防止消費者終止。 PHP應用程式的最佳實務是重新啟動長時間執行的程式，以防止可能的記憶體流失。

- `--batch-size <value>` — 可讓您限制消費者使用的系統資源(CPU、記憶體)。 使用較小的批次會減少資源使用量，因此會導致處理變慢。  若指定，佇列中的訊息會以`<value>`批次（每批次）使用。 此選項僅適用於批次取用者。 如果未定義`--batch-size`，則批次取用者會接收佇列中所有可用的訊息。

如需其他組態選項的詳細資訊，請參閱[特定組態](https://experienceleague.adobe.com//en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#specific-configuration)。

### 啟動訊息取用者

若要為B2B功能啟用非同步作業，您必須啟動多個訊息取用者。

1. 列出可用的訊息取用者：

   ```bash
   bin/magento queue:consumers:list
   ```

   命令會傳回可用的訊息消費者，包括所有[B2B訊息消費者](#message-consumers)。

1. 分別啟動每個消費者：

   ```bash
   bin/magento queue:consumers:start [--max-messages=<value>] [--batch-size=<value>] <consumer_name>
   ```

   例如：

   ```bash
   bin/magento queue:consumers:start quoteItemCleaner
   ```

>[!TIP]
>
>若要在背景執行，請在命令中附加`&`，返回提示字元並繼續執行命令。 例如： `bin/magento queue:consumers:start sharedCatalogUpdatePrice &`。

如需詳細資訊，請參閱&#x200B;_設定指南_&#x200B;中的[管理訊息佇列](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues)。

### 將訊息消費者新增至cron

您可以將排程新增至cron組態檔[/app/code/Magento/MessageQueue/etc/crontab.xml](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#process-management)，以自動執行`SharedCatalogUpdateCategoryPermissions`和`SharedCatalogUpdatePrice`訊息使用者的執行排程。

```
* * * * * ps ax | grep [s]haredCatalogUpdateCategoryPermissions >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdateCategoryPermissions &
* * * * * ps ax | grep [s]haredCatalogUpdatePrice >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdatePrice &
```

您也可以從「管理員」的[存放區組態設定](../systems/cron.md)設定訊息取用者的排程。

## 在管理員中啟用B2B功能

安裝Adobe Commerce B2B擴充功能並啟動訊息消費者後，您還必須在管理員中[啟用B2B功能](enable-basic-features.md)。

