---
title: 安裝 [!DNL Adobe Commerce B2B] 副檔名
description: 瞭解如何安裝 [!DNL Adobe Commerce B2B] 中繼封裝。
feature: B2B, Install
role: Admin, Developer
exl-id: a6947212-1708-40ae-9e81-874467eba5e1
source-git-commit: be36742aa1214e7e8e7f343051336cd3635099f4
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 0%

---


# 安裝 [!DNL Adobe Commerce B2B] 副檔名

Adobe Commerce B2B擴充功能， `magento/extension-b2b` 適用於所有受支援的Adobe Commerce版本。 它會在安裝Adobe Commerce之後安裝。


## 需求

- [Adobe Commerce](https://business.adobe.com/products/magento/magento-commerce.html)，所有支援的版本
- PHP 8.1 / 8.2 / 8.3
- [!DNL Composer]

## 支援平台

- 雲端基礎結構上的Adobe Commerce (ECE)
- Adobe Commerce內部部署(EE)

## 安裝步驟

>[!BEGINSHADEBOX]

**必要條件**

- 存取目標 [repo.magento.com](https://repo.magento.com/) 以下載擴充功能。 如需金鑰產生與取得必要許可權的相關資訊，請參閱 [取得您的驗證金鑰](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys).

  儲存驗證金鑰以供安裝，方法是在中全域定義 [COMPOSER_HOME](https://getcomposer.org/doc/03-cli.md#composer-home) 目錄。 或者，將其儲存至 [auth.json](https://developer.adobe.com/commerce/contributor/guides/install/clone-repository/#authentication-file) Adobe Commerce應用程式根目錄中的檔案。

- [B2B擴充功能的支援版本](https://experienceleague.adobe.com/en/docs/commerce-operations/release/product-availability) — 決定已部署Adobe Commerce版本支援的最新B2B擴充功能版本。

- 請檢視發行說明，瞭解版本相容性、更新或變更的最新資訊，這些可能會影響安裝或升級需求。

   - [B2B發行說明](release-notes.md)
   - [Adobe Commerce發行說明](https://experienceleague.adobe.com/en/docs/commerce-operations/release/versions)

>[!ENDSHADEBOX]

安裝B2B擴充功能(`magento/b2b-extension`)使用Composer。 此擴充功能是撰寫器中繼資料，其中包括可為Adobe Commerce執行個體啟用B2B功能的模組集合。 如需包含的模組清單，請參閱 [B2B套件](packages.md).

>[!BEGINTABS]

>[!TAB 雲端基礎結構]

>[!TIP]
>
>在雲端基礎結構上安裝Adobe Commerce B2B時，Adobe建議您先將Adobe Commerce應用程式部署至整合或預備環境，再開始進行。

將B2B擴充功能新增至專案時，Adobe建議在開發分支中工作。 如果您沒有分支，請參閱 [建立開發分支](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches). 安裝B2B擴充功能時， `Magento_B2b` 擴充功能名稱會自動插入 `app/etc/config.php` 檔案。 不需要直接編輯檔案。

**安裝B2B擴充功能的方式**：

1. 在本機工作站上，變更至專案目錄。

1. 建立或簽出開發分支。

1. 將B2B擴充功能新增至 `require` 的區段 `composer.json` 檔案。

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
   >將更新推播至雲端環境會啟動Commerce雲端部署流程以套用變更。 從檢視部署狀態 [部署記錄](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process). 如果您遇到部署錯誤，請參閱 [從元件失敗復原](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/recover-failed-deployment).

1. 建置和部署完成後，請使用SSH登入遠端環境，並確認已安裝並啟用B2B擴充功能。

   ```bash
   bin/magento module:status Magento_B2b
   ```

   擴充功能名稱會使用以下格式： `<VendorName>_<ComponentName>`.

   範例回應：

   ```terminal
   Magento_B2b : Module is enabled
   ```

>[!TAB 內部部署]

1. 從Adobe Commerce應用程式根目錄，更新 `composer.json` 新增B2B擴充功能的相依性：

   ```bash
   composer require magento/extension-b2b:<version>
   ```

   如果發生錯誤，例如：

   ```terminal
   [InvalidArgumentException] Could not find a matching version of package magento/extension-b2b.
   ```

   檢查套件拼字、版本限制，以及套件是否可用且符合您的最低穩定性（穩定）要求。

1. 如果出現提示，請輸入您的 [驗證金鑰](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys).

   您的 _公開金鑰_ 是您的使用者名稱；您的 _私密金鑰_ 是您的密碼。 如果您已將公開和私密金鑰儲存在 `auth.json`，系統不會提示您進行驗證。

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
   >在生產模式中，您可能會收到 `Please rerun Magento compile command`. 輸入命令以完成安裝。 Adobe Commerce不會提示您以開發人員模式執行編譯命令。

>[!ENDTABS]

完成安裝之後，請設定並啟動訊息取用者。

## 訊息消費者

Adobe Commerce B2B擴充功能使用MySQL進行訊息佇列管理。 下表列出支援B2B功能的訊息消費者。 安裝擴充功能後，針對您的Commerce店面所需的B2B功能啟動訊息消費者。

| 消費者 | 說明 |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sharedCatalogUpdatePrice` | 更新共用目錄中每個產品的價格。 下列情況下需要 [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) 選項已啟用。 |
| `sharedCatalogUpdateCategoryPermissions` | 更新指派給共用目錄類別的類別。 下列情況下需要 [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) 選項已啟用。 |
| `negotiableQuotePriceUpdate` | 更新可轉讓報價的價格。 下列情況下需要 [**[!UICONTROL Quotes]**](quotes.md) 選項已啟用。 |
| `purchaseorder.toorder` | 將採購單轉換為訂單。 下列情況下需要 [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) 選項已啟用。 |
| `purchaseorder.transactional.email` | 傳送採購單電子郵件。 下列情況下需要 [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) 選項已啟用。 |
| `purchaseorder.validation` | 根據相關驗證採購單 [核准規則](account-dashboard-approval-rules.md). 下列情況下需要 [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) 選項已啟用。 |
| `quoteItemCleaner` | 當產品從目錄中刪除或從購物車中移除時，會刪除無效或無效的報價單。 下列情況下需要 [**[!UICONTROL Quotes]**](quotes.md) 選項已啟用。 |
| `inventoryQtyCounter` | 下訂單或移除產品後，以非同步方式修正股票指數。 下列情況下需要 [**[!UICONTROL Use deferred stock update]**](../configuration-reference/catalog/inventory.md#product-stock-options) 選項已啟用Inventory management的「管理員組態」設定。 另請參閱 [效能最佳實務](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/configuration#deferred-stock-update). |
| `async.operations.all` | 為的每項個別任務建立訊息 [大量作業](https://developer.adobe.com/commerce/php/development/components/message-queues/bulk-operations/) 例如，匯入或匯出料號、變更整批標價以及指定產品至倉庫。 下列情況下需要 [**管理員大量作業**](../configuration-reference/catalog/inventory.md#admin-bulk-operations) 選項 [!DNL Inventory Management] 設為 **非同步執行** 在管理系統組態設定中。 |

{style="table-layout:auto"}

>[!NOTE]
>
>如需所有Adobe Commerce訊息使用者的清單，請參閱 [訊息佇列取用者](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/consumers) 在 _設定指南_.

### 設定訊息使用者

當您執行以下動作時，請新增下列引數，以防止可能的處理問題或延遲 [啟動訊息取用者](#start-message-consumers) B2B功能。

- `--max-messages <value>` — 指定每個使用者必須在終止前處理的最大訊息數(預設值= 10000)。 雖然Adobe不建議這麼做，但您可以使用0來防止消費者終止。 PHP應用程式的最佳實務是重新啟動長時間執行的程式，以防止可能的記憶體流失。

- `--batch-size <value>` — 可讓您限制消費者使用的系統資源（CPU、記憶體）。 使用較小的批次會減少資源使用量，因此會導致處理變慢。  若指定，佇列中的訊息會以以下批次消耗： `<value>` 每個。 此選項僅適用於批次取用者。 如果 `--batch-size` 未定義，批次取用者會接收佇列中所有可用的訊息。

如需其他組態選項的相關資訊，請參閱 [特定組態](https://experienceleague.adobe.com//en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#specific-configuration).

### 啟動訊息取用者

若要為B2B功能啟用非同步作業，您必須啟動多個訊息取用者。

1. 列出可用的訊息取用者：

   ```bash
   bin/magento queue:consumers:list
   ```

   該命令會傳回可用的訊息取用者，包括所有 [B2B訊息消費者](#message-consumers).

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
>若要在背景執行，請附加 `&` 使用指令，返回提示字元並繼續執行指令。 例如： `bin/magento queue:consumers:start sharedCatalogUpdatePrice &`.

如需詳細資訊，請參閱 [管理訊息佇列](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues) 在 _設定指南_.

### 將訊息消費者新增至cron

您可以為以下專案自動化執行排程： `SharedCatalogUpdateCategoryPermissions` 和 `SharedCatalogUpdatePrice` 將排程新增至cron設定檔案以傳送訊息消費者 [/app/code/Magento/MessageQueue/etc/crontab.xml](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#process-management).

```terminal
* * * * * ps ax | grep [s]haredCatalogUpdateCategoryPermissions >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdateCategoryPermissions &
* * * * * ps ax | grep [s]haredCatalogUpdatePrice >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdatePrice &
```

您也可以為訊息使用者設定排程，從 [存放區組態設定](../systems/cron.md) 在Admin中。

## 在管理員中啟用B2B功能

安裝Adobe Commerce B2B擴充功能並啟動訊息消費者後，您也必須 [在管理員中啟用B2B功能](enable-basic-features.md).

