---
source-git-commit: a37e67c332140fbba7609db8cc5e22a3625a1c9d
workflow-type: tm+mt
source-wordcount: '2387'
ht-degree: 0%

---
# Adobe Commerce搭配B2B套件

<!-- The 'packages' variable contains the 'packages' node of the '_data/codebase/b2b/composer_lock.json' file
 -->

<!-- The 'packages-dev' variable contains the 'packages-dev' node of the '_data/codebase/b2b/composer_lock.json' file
 -->

<!-- The 'product' variable contains data of the 'magento/product-enterprise-edition' package
 -->

<!-- The edition variable contains `commerce-b2b` value from the _data/names.yml file
 -->

Adobe Commerce B2B使用Composer來管理PHP套件。

`composer.json`檔案會宣告套件清單，而`composer.lock`檔案會儲存用來建置Adobe Commerce B2B安裝的套件完整清單（每個套件的完整版本及其相依性）。

下列參考檔案是從`composer.lock`檔案產生，其涵蓋Adobe Commerce B2B 1.5.2中包含的必要套件。

## 相依性

`magento/extension-b2b 1.5.2`有下列相依性：

- magento/framework： >=103.0.6 &lt;103.0.9
- magento/magento2-b2b-base： 1.5.2
- [magento/module-b2b](https://developer.adobe.com/commerce/php/module-reference/module-b2b/)： 100.5.2
- [magento/module-bundle-negotial-quote](https://developer.adobe.com/commerce/php/module-reference/module-bundle-negotiable-quote/)： 100.5.1
- [magento/module-bundle-requisition-list](https://developer.adobe.com/commerce/php/module-reference/module-bundle-requisition-list/)： 100.5.1
- [magento/module-bundle-requisition-list-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-bundle-requisition-list-graph-ql/)： 1.5.1
- [magento/module-bundle-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-bundle-shared-catalog/)： 100.5.1
- [magento/module-checkout-address-search-negotial-quote](https://developer.adobe.com/commerce/php/module-reference/module-checkout-address-search-negotiable-quote/)： 100.5.1
- [magento/module-checkout-agreements-negotial-quote](https://developer.adobe.com/commerce/php/module-reference/module-checkout-agreements-negotiable-quote/)： 100.5.1
- [magento/module-checkout-agreements-purchase-order](https://developer.adobe.com/commerce/php/module-reference/module-checkout-agreements-purchase-order/)： 1.5.1
- [magento/module-company](https://developer.adobe.com/commerce/php/module-reference/module-company/)： 102.0.2
- [magento/module-company-asynchronous-operations](https://developer.adobe.com/commerce/php/module-reference/module-company-asynchronous-operations/)： 1.5.1
- [magento/module-company-credit](https://developer.adobe.com/commerce/php/module-reference/module-company-credit/)： 100.5.2
- [magento/module-company-credit-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-company-credit-graph-ql/)： 1.5.1
- [magento/module-company-customer-import-export](https://developer.adobe.com/commerce/php/module-reference/module-company-customer-import-export/)： 1.5.0
- [magento/module-company-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-company-graph-ql/)： 1.5.2
- [magento/module-company-angable-quote](https://developer.adobe.com/commerce/php/module-reference/module-company-negotiable-quote/)： 1.5.1
- [magento/module-company-negotial-quote-template](https://developer.adobe.com/commerce/php/module-reference/module-company-negotiable-quote-template/)： 1.5.1
- [magento/module-company-payment](https://developer.adobe.com/commerce/php/module-reference/module-company-payment/)： 100.5.1
- [magento/module-company-quote](https://developer.adobe.com/commerce/php/module-reference/module-company-quote/)： 1.5.2
- [magento/module-company-quote-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-company-quote-graph-ql/)： 1.5.2
- [magento/module-company-relation](https://developer.adobe.com/commerce/php/module-reference/module-company-relation/)： 1.5.2
- [magento/module-company-relation-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-company-relation-shared-catalog/)： 1.5.1
- [magento/module-company-shipping](https://developer.adobe.com/commerce/php/module-reference/module-company-shipping/)： 1.5.1
- [magento/module-configurable-angular-quote](https://developer.adobe.com/commerce/php/module-reference/module-configurable-negotiable-quote/)： 100.5.1
- [magento/module-configurable-requisition-list](https://developer.adobe.com/commerce/php/module-reference/module-configurable-requisition-list/)： 100.5.1
- [magento/module-configurable-requisition-list-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-configurable-requisition-list-graph-ql/)： 1.5.1
- [magento/module-configurable-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-configurable-shared-catalog/)： 100.5.1
- [magento/module-downloadable-company](https://developer.adobe.com/commerce/php/module-reference/module-downloadable-company/)： 1.5.1
- [magento/module-downloadable-requisition-list-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-downloadable-requisition-list-graph-ql/)： 1.5.1
- [magento/module-gift-card-angotiable-quote](https://developer.adobe.com/commerce/php/module-reference/module-gift-card-negotiable-quote/)： 100.5.1
- [magento/module-gift-card-requisition-list](https://developer.adobe.com/commerce/php/module-reference/module-gift-card-requisition-list/)： 100.5.1
- [magento/module-gift-card-requisition-list-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-gift-card-requisition-list-graph-ql/)： 1.5.1
- [magento/module-gift-card-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-gift-card-shared-catalog/)： 100.5.1
- [magento/module-grouped-requisition-list](https://developer.adobe.com/commerce/php/module-reference/module-grouped-requisition-list/)： 100.5.1
- [magento/module-grouped-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-grouped-shared-catalog/)： 100.5.1
- [magento/module-negotial-quote](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote/)： 101.0.2
- [magento/module-negotial-quote-async-order](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-async-order/)： 1.5.1
- [magento/module-negotial-quote-duplicate](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-duplicate/)： 1.5.2
- [magento/module-negotial-quote-duplicate-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-duplicate-graph-ql/)： 1.5.1
- [magento/module-negotial-quote-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-graph-ql/)： 1.5.1
- [magento/module-negotial-quote-requisition-list](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-requisition-list/)： 1.5.1
- [magento/module-negotial-quote-requisition-list-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-requisition-list-graph-ql/)： 1.5.1
- [magento/module-negotial-quote-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-shared-catalog/)： 100.5.1
- [magento/module-negotial-quote-template](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-template/)： 1.5.2
- [magento/module-negotial-quote-template-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-template-graph-ql/)： 1.5.2
- [magento/module-negotial-quote-template-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-template-shared-catalog/)： 1.5.1
- [magento/module-negotial-quote-weee](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-weee/)： 100.5.1
- [magento/module-order-history-search](https://developer.adobe.com/commerce/php/module-reference/module-order-history-search/)： 100.5.2
- [magento/module-paypal-negotial-quote](https://developer.adobe.com/commerce/php/module-reference/module-paypal-negotiable-quote/)： 1.5.1
- [magento/module-paypal-purchase-order](https://developer.adobe.com/commerce/php/module-reference/module-paypal-purchase-order/)： 1.5.1
- [magento/module-purchase-order](https://developer.adobe.com/commerce/php/module-reference/module-purchase-order/)： 100.5.2
- [magento/module-purchase-order-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-purchase-order-graph-ql/)： 1.5.1
- [magento/module-purchase-order-rule](https://developer.adobe.com/commerce/php/module-reference/module-purchase-order-rule/)： 100.5.2
- [magento/module-purchase-order-rule-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-purchase-order-rule-graph-ql/)： 1.5.1
- [magento/module-quick-order](https://developer.adobe.com/commerce/php/module-reference/module-quick-order/)： 100.5.1
- [magento/module-quick-order-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-quick-order-graph-ql/)： 1.5.1
- [magento/module-requisition-list](https://developer.adobe.com/commerce/php/module-reference/module-requisition-list/)： 100.5.2
- [magento/module-requisition-list-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-requisition-list-graph-ql/)： 1.5.1
- [magento/module-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-shared-catalog/)： 100.5.2
- [magento/module-shared-catalog-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-shared-catalog-graph-ql/)： 1.5.1
- magento/security-package-b2b： 1.0.6

## 協力廠商授權

### Apache-2.0、LGPL-2.1-only

<table>
  <thead>
    <tr>
      <th>名稱</th>
      <th>型別</th>
      <th>說明</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/opensearch-project/opensearch-php">opensearch-project/opensearch-php</a>
    </td>
    <td>資料庫</td>
    <td>OpenSearch的PHP使用者端</td>
  </tr>
  </tbody>
</table>

### Apache-2.0

<table>
  <thead>
    <tr>
      <th>名稱</th>
      <th>型別</th>
      <th>說明</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/adobe/stock-api-libphp">astock/stock-api-libphp</a>
    </td>
    <td>資料庫</td>
    <td>Adobe Stock API程式庫</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/awslabs/aws-crt-php">aws/aws-crt-php</a>
    </td>
    <td>資料庫</td>
    <td>適用於PHP的AWS Common Runtime</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/aws/aws-sdk-php">aws/aws-sdk-php</a>
    </td>
    <td>資料庫</td>
    <td>適用於PHP的AWS SDK — 在PHP專案中使用Amazon Web Services</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/opentelemetry-php/api">開放遙測/api</a>
    </td>
    <td>資料庫</td>
    <td>OpenTelemetry PHP的API。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/opentelemetry-php/context">開放遙測/內容</a>
    </td>
    <td>資料庫</td>
    <td>OpenTelemetry PHP的上下文實作。</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree
    </td>
    <td>Metapackage</td>
    <td>Braintree Magento</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/wikimedia/less.php">wikimedia/less.php</a>
    </td>
    <td>資料庫</td>
    <td>LESS處理器的PHP連線埠</td>
  </tr>
  </tbody>
</table>

### BSD-2 — 子句

<table>
  <thead>
    <tr>
      <th>名稱</th>
      <th>型別</th>
      <th>說明</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/Bacon/BaconQrCode">培根/培根 — qr-code</a>
    </td>
    <td>資料庫</td>
    <td>BaconQrCode是PHP的QR程式碼產生器。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/DASPRiD/Enum">dasprid/enum</a>
    </td>
    <td>資料庫</td>
    <td>PHP 7.1列舉實作</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/webimpress/safe-writer">webimpress/safe-writer</a>
    </td>
    <td>資料庫</td>
    <td>安全寫入檔案的工具，避免競爭情況</td>
  </tr>
  </tbody>
</table>

### BSD-3 — 子句

<table>
  <thead>
    <tr>
      <th>名稱</th>
      <th>型別</th>
      <th>說明</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/colinmollenhour/Cm_Cache_Backend_File">colimollenhour/cache-backend-file</a>
    </td>
    <td>Magento-module</td>
    <td>庫存Zend_Cache_Backend_File後端透過標籤進行清除的效能極差，導致隨著快取專案數的增加無法使用。 此後端進行許多變更，大幅提升效能，尤其是標籤清除作業。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/colinmollenhour/php-redis-session-abstract">colimollenhour/php-redis-session-abstract</a>
    </td>
    <td>資料庫</td>
    <td>具有樂觀鎖定的Redis型工作階段處理常式</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/duosecurity/duo_universal_php">duosecurity/duo_universal_php</a>
    </td>
    <td>資料庫</td>
    <td>Duo Universal SDK的PHP實作。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/firebase/php-jwt">firebase/php-jwt</a>
    </td>
    <td>資料庫</td>
    <td>在PHP中編碼和解碼JSON Web權杖(JWT)的簡單程式庫。 應符合目前的規格。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-captcha">laminas/laminas-captcha</a>
    </td>
    <td>資料庫</td>
    <td>使用Figlet、影像、ReCaptcha等專案產生及驗證驗證碼</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-code">laminas/laminas-code</a>
    </td>
    <td>資料庫</td>
    <td>PHP Reflection API、靜態程式碼掃描和程式碼產生的擴充功能</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-config">laminas/laminas-config</a>
    </td>
    <td>資料庫</td>
    <td>提供巢狀物件屬性型使用者介面，用於存取應用程式程式碼內的此設定資料</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-di">laminas/laminas-di</a>
    </td>
    <td>資料庫</td>
    <td>PSR-11容器的自動化相依性插入</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-escaper">laminas/laminas-escaper</a>
    </td>
    <td>資料庫</td>
    <td>安全地逸出HTML、HTML屬性、JavaScript、CSS和URL</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-eventmanager">laminas/laminas-eventmanager</a>
    </td>
    <td>資料庫</td>
    <td>觸發並接聽PHP應用程式中的事件</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-feed">層疊/層疊 — 饋送</a>
    </td>
    <td>資料庫</td>
    <td>提供建立和使用RSS和Atom摘要的功能</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-filter">層疊/層疊 — 篩選</a>
    </td>
    <td>資料庫</td>
    <td>以程式設計方式篩選及標準化資料和檔案</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-http">laminas/laminas-http</a>
    </td>
    <td>資料庫</td>
    <td>提供執行超文字傳輸通訊協定(HTTP)要求的簡易介面</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-i18n">laminas/laminas-i18n</a>
    </td>
    <td>資料庫</td>
    <td>提供應用程式的翻譯，並篩選及驗證國際化值</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-json">laminas/laminas-json</a>
    </td>
    <td>資料庫</td>
    <td>提供了將原生PHP序列化為JSON並將JSON解碼為原生PHP的便利方法</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-loader">laminas/laminas-loader</a>
    </td>
    <td>資料庫</td>
    <td>自動載入和外掛程式載入策略</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-modulemanager">laminas/laminas-modulemanager</a>
    </td>
    <td>資料庫</td>
    <td>適用於Laminas-mvc應用程式的模組化應用程式系統</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-mvc">laminas/laminas-mvc</a>
    </td>
    <td>資料庫</td>
    <td>Laminas的事件導向MVC層，包括MVC應用程式、控制器和外掛程式</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-permissions-acl">laminas/laminas-permissions-acl</a>
    </td>
    <td>資料庫</td>
    <td>提供輕量且有彈性的存取控制清單(ACL)實作，以進行許可權管理</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-recaptcha">laminas/laminas-recaptcha</a>
    </td>
    <td>資料庫</td>
    <td>ReCaptcha Web服務的OOP包裝函式</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-router">層疊/層疊 — 路由器</a>
    </td>
    <td>資料庫</td>
    <td>適用於HTTP和主控台應用程式的彈性路由系統</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-server">laminas/laminas-server</a>
    </td>
    <td>資料庫</td>
    <td>建立反射式RPC伺服器</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-servicemanager">laminas/laminas-servicemanager</a>
    </td>
    <td>資料庫</td>
    <td>工廠驅動相依性注入容器</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-session">laminas/laminas-session</a>
    </td>
    <td>資料庫</td>
    <td>PHP工作階段和儲存的物件導向介面</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-soap">laminas/laminas-soap</a>
    </td>
    <td>資料庫</td>
    <td></td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-stdlib">laminas/laminas-stdlib</a>
    </td>
    <td>資料庫</td>
    <td>SPL擴充功能、陣列公用程式、錯誤處理常式等</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-text">層疊/層疊 — 文字</a>
    </td>
    <td>資料庫</td>
    <td>建立FIGlet和文字型表格</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-translator">laminas/laminas-translator</a>
    </td>
    <td>資料庫</td>
    <td>laminas-i18n的Translator元件介面</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-uri">laminas/laminas-uri</a>
    </td>
    <td>資料庫</td>
    <td>協助處理和驗證「統一資源識別碼(URI)」的元件</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-validator">laminas/laminas-validator</a>
    </td>
    <td>資料庫</td>
    <td>適用於多種網域的驗證類別，以及鏈結驗證器以建立複雜驗證條件的功能</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-view">laminas/laminas-view</a>
    </td>
    <td>資料庫</td>
    <td>彈性檢視層可支援並提供多個檢視層、協助程式等</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/marc-mabe/php-enum">marc-mabe/php-enum</a>
    </td>
    <td>資料庫</td>
    <td>使用原生PHP簡單快速地實作分項清單</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/nikic/PHP-Parser">nikic/php-parser</a>
    </td>
    <td>資料庫</td>
    <td>以PHP撰寫的PHP剖析器</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/phpfui/recaptcha">phpfui/recaptcha</a>
    </td>
    <td>資料庫</td>
    <td>適用於Google reCAPTCHA for PHP 8.4及更高版本的使用者端程式庫</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/tedious/JShrink">tedivm/jshrink</a>
    </td>
    <td>資料庫</td>
    <td>內建於PHP的Javascript Minifier</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/tubalmartin/YUI-CSS-compressor-PHP-port">tubalmartin/cssmin</a>
    </td>
    <td>資料庫</td>
    <td>YUI CSS壓縮器的PHP連線埠</td>
  </tr>
  </tbody>
</table>

### BSD-3 — 條款 — 修改

<table>
  <thead>
    <tr>
      <th>名稱</th>
      <th>型別</th>
      <th>說明</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/colinmollenhour/Cm_Cache_Backend_Redis">colimollenhour/cache-backend-redis</a>
    </td>
    <td>Magento-module</td>
    <td>使用Redis的Zend_Cache後端，完全支援標籤。</td>
  </tr>
  </tbody>
</table>

### ISC

<table>
  <thead>
    <tr>
      <th>名稱</th>
      <th>型別</th>
      <th>說明</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/paragonie/sodium_compat">paragonie/na_compat</a>
    </td>
    <td>資料庫</td>
    <td>libna的純PHP實作；使用PHP擴充功能（如果存在）</td>
  </tr>
  </tbody>
</table>

### LGPL-2.1或更新版本

<table>
  <thead>
    <tr>
      <th>名稱</th>
      <th>型別</th>
      <th>說明</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/ezyang/htmlpurifier">ezyang/htmlpurifier</a>
    </td>
    <td>資料庫</td>
    <td>以PHP撰寫的符合標準的HTML篩選器</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-amqplib/php-amqplib">php-amqplib/php-amqplib</a>
    </td>
    <td>資料庫</td>
    <td>原稱videlalvaro/php-amqplib。  此程式庫是AMQP通訊協定的純PHP實作。 並針對RabbitMQ進行測試。</td>
  </tr>
  </tbody>
</table>

### MIT

<table>
  <thead>
    <tr>
      <th>名稱</th>
      <th>型別</th>
      <th>說明</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/braintree/braintree_php">braintree/braintree_php</a>
    </td>
    <td>資料庫</td>
    <td>Braintree PHP使用者端程式庫</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/brick/math">磚/數學</a>
    </td>
    <td>資料庫</td>
    <td>任意精確度算術程式庫</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/brick/varexporter">brick/varexporter</a>
    </td>
    <td>資料庫</td>
    <td>var_export()的強大替代方案，可在不使用__set_state()的情況下匯出關閉項和物件</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ChristianRiesen/base32">christian-riesen/base32</a>
    </td>
    <td>資料庫</td>
    <td>根據RFC 4648的Base32編碼器/解碼器</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/colinmollenhour/credis">colimollenhour/credis</a>
    </td>
    <td>資料庫</td>
    <td>Credis是Redis索引鍵值存放區的輕量型介面，可在取得phpredis資料庫時將其包裝起來，以提升效能。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/ca-bundle">composer/ca-bundle</a>
    </td>
    <td>資料庫</td>
    <td>可讓您尋找系統CA套件的路徑，並包含Mozilla CA套件的遞補內容。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/class-map-generator">composer/class-map-generator</a>
    </td>
    <td>資料庫</td>
    <td>掃描PHP程式碼和產生類別對映的公用程式。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/composer">撰寫器/撰寫器</a>
    </td>
    <td>資料庫</td>
    <td>Composer可協助您宣告、管理和安裝PHP專案的相依性。 它可確保您隨時隨地擁有正確的棧疊。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/metadata-minifier">composer/metadata-minifier</a>
    </td>
    <td>資料庫</td>
    <td>處理中繼資料縮制和擴充的小型公用程式庫。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/pcre">作曲者/pcre</a>
    </td>
    <td>資料庫</td>
    <td>提供型別安全預浸料取代的PCRE包裝程_*庫。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/semver">composer/semver</a>
    </td>
    <td>資料庫</td>
    <td>提供公用程式、版本限制剖析和驗證的伺服器程式庫。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/spdx-licenses">作曲者/spdx — 授權</a>
    </td>
    <td>資料庫</td>
    <td>SPDX授權清單和驗證程式庫。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/xdebug-handler">composer/xdebug-handler</a>
    </td>
    <td>資料庫</td>
    <td>在不使用Xdebug的情況下重新啟動程式。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/doctrine/lexer">學說/詞法分析工具</a>
    </td>
    <td>資料庫</td>
    <td>PHP Doctrine Lexer剖析器程式庫，可用於自上而下的遞回下降剖析器。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/egulias/EmailValidator">egulias/email-validator</a>
    </td>
    <td>資料庫</td>
    <td>用於針對數個RFC驗證電子郵件的程式庫</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/elastic/elastic-transport-php">彈性/傳輸</a>
    </td>
    <td>資料庫</td>
    <td>HTTP傳輸Elastic產品的PHP程式庫</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/elastic/elasticsearch-php">elasticsearch/elasticsearch</a>
    </td>
    <td>資料庫</td>
    <td>Elasticsearch的PHP使用者端</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/endroid/qr-code">endroid/qr-code</a>
    </td>
    <td>資料庫</td>
    <td>Endroid QR碼</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ezimuel/guzzlestreams">ezimuel/guzzlestreams</a>
    </td>
    <td>資料庫</td>
    <td>要與elasticsearch-php一起使用的guzzle/streams （已捨棄）分支</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ezimuel/ringphp">ezimuel/ringphp</a>
    </td>
    <td>資料庫</td>
    <td>要與elasticsearch-php一起使用的guzzle/RingPHP （已放棄）分支</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/guzzle/guzzle">guzzlehttp/guzzle</a>
    </td>
    <td>資料庫</td>
    <td>Guzzle是PHP HTTP使用者端程式庫</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/guzzle/promises">guzzlehttp/promise</a>
    </td>
    <td>資料庫</td>
    <td>Guzzle promise程式庫</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/guzzle/psr7">guzzlehttp/psr7</a>
    </td>
    <td>資料庫</td>
    <td>PSR-7訊息實作，也提供通用公用程式方法</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/jsonrainbow/json-schema">justinrainbow/json-schema</a>
    </td>
    <td>資料庫</td>
    <td>驗證json結構描述的程式庫。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/thephpleague/flysystem">聯盟/飛控系統</a>
    </td>
    <td>資料庫</td>
    <td>PHP的檔案儲存抽象</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/thephpleague/flysystem-aws-s3-v3">league/flysystem-aws-s3-v3</a>
    </td>
    <td>資料庫</td>
    <td>適用於Flysystem的AWS S3檔案系統配接卡。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/thephpleague/flysystem-local">league/flysystem-local</a>
    </td>
    <td>資料庫</td>
    <td>Flysystem的本機檔案系統配接卡。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/thephpleague/mime-type-detection">league/mime-type-detection</a>
    </td>
    <td>資料庫</td>
    <td>Flysystem的MIME型別偵測</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Seldaek/monolog">獨白/獨白</a>
    </td>
    <td>資料庫</td>
    <td>將您的記錄傳送至檔案、通訊端、收件匣、資料庫和各種網站服務</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/jmespath/jmespath.php">mtdowling/jmespath.php</a>
    </td>
    <td>資料庫</td>
    <td>以宣告方式指定如何從JSON檔案中擷取元素</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/paragonie/constant_time_encoding">paragonie/constant_time_encoding</a>
    </td>
    <td>資料庫</td>
    <td>RFC 4648編碼的常數時間實作(Base-64、Base-32、Base-16)</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/paragonie/random_compat">paragonie/random_compat</a>
    </td>
    <td>資料庫</td>
    <td>PHP 7的random_bytes()和random_int()的PHP 5.x polyfill</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/MyIntervals/emogrifier">pelago/表情符號</a>
    </td>
    <td>資料庫</td>
    <td>將CSS樣式轉換為HTML程式碼中的內嵌樣式屬性</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-http/discovery">php-http/discovery</a>
    </td>
    <td>Composer-plugin</td>
    <td>尋找並安裝PSR-7、PSR-17、PSR-18和HTTPlug實作</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-http/httplug">php-http/httplug</a>
    </td>
    <td>資料庫</td>
    <td>HTTPlug，PHP的HTTP使用者端抽象化</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-http/promise">php-http/promise</a>
    </td>
    <td>資料庫</td>
    <td>用於非同步HTTP請求的Promise</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/PhpGt/CssXPath">phpgt/cssxpath</a>
    </td>
    <td>資料庫</td>
    <td>將CSS選取器轉換為XPath查詢。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/PhpGt/Dom">phpgt/dom</a>
    </td>
    <td>資料庫</td>
    <td>新式DOM API。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/PhpGt/PropFunc">phpgt/propfunc</a>
    </td>
    <td>資料庫</td>
    <td>屬性存取子與變數函式。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/phpseclib/mcrypt_compat">phpseclab/mcrypt_compat</a>
    </td>
    <td>資料庫</td>
    <td>PHP 5.x-8.x polyfill for mcrypt延伸模組</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/phpseclib/phpseclib">phpseclab/phpseclab</a>
    </td>
    <td>資料庫</td>
    <td>PHP Secure Communications Library - RSA、AES、SSH2、SFTP、X.509等的純PHP實作。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/cache">psr/快取</a>
    </td>
    <td>資料庫</td>
    <td>快取程式庫的通用介面</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/clock">psr/時鐘</a>
    </td>
    <td>資料庫</td>
    <td>讀取時鐘的通用介面。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/container">psr/容器</a>
    </td>
    <td>資料庫</td>
    <td>通用容器介面（PHP圖PSR-11）</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/event-dispatcher">psr/event-dispatcher</a>
    </td>
    <td>資料庫</td>
    <td>用於事件處理的標準介面。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/http-client">psr/http-client</a>
    </td>
    <td>資料庫</td>
    <td>HTTP使用者端的通用介面</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/http-factory">psr/http-factory</a>
    </td>
    <td>資料庫</td>
    <td>PSR-17： PSR-7 HTTP訊息處理站的通用介面</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/http-message">psr/http-message</a>
    </td>
    <td>資料庫</td>
    <td>HTTP訊息的通用介面</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/log">psr/log</a>
    </td>
    <td>資料庫</td>
    <td>記錄程式庫的通用介面</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ralouphie/getallheaders">ralouphie/getallheaders</a>
    </td>
    <td>資料庫</td>
    <td>getallheaders的polyfill。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ramsey/collection">ramsey/collection</a>
    </td>
    <td>資料庫</td>
    <td>用於表示和處理集合的PHP程式庫。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ramsey/uuid">ramsey/uuid</a>
    </td>
    <td>資料庫</td>
    <td>用於產生和使用通用唯一識別碼(UUID)的PHP程式庫。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/reactphp/promise">react/promise</a>
    </td>
    <td>資料庫</td>
    <td>PHP的CommonJS Promise/A的輕量級實作</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/MyIntervals/PHP-CSS-Parser">sabberworm/php-css-parser</a>
    </td>
    <td>資料庫</td>
    <td>以PHP撰寫之CSS檔案的剖析器</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Seldaek/jsonlint">seld/jsonlint</a>
    </td>
    <td>資料庫</td>
    <td>JSON Linter</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Seldaek/phar-utils">seld/phar-utils</a>
    </td>
    <td>資料庫</td>
    <td>PHAR檔案格式公用程式，用於當PHP將您變成像片時</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Seldaek/signal-handler">seld/signal-handler</a>
    </td>
    <td>資料庫</td>
    <td>簡單的Unix訊號處理常式，在訊號不支援輕鬆跨平台開發時無訊息失敗</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Spomky-Labs/aes-key-wrap">spomky-labs/aes-key-wrap</a>
    </td>
    <td>資料庫</td>
    <td>PHP的AES金鑰換行。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Spomky-Labs/otphp">spomky-labs/otphp</a>
    </td>
    <td>資料庫</td>
    <td>用於根據RFC 4226 （HOTP演演算法）和RFC 6238 （TOTP演演算法）產生一次性密碼並與Google Authenticator相容的PHP程式庫</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Spomky-Labs/pki-framework">spomky-labs/pki-framework</a>
    </td>
    <td>資料庫</td>
    <td>用於管理公開金鑰基礎結構的PHP架構。 它包含X.509公開金鑰憑證、屬性憑證、憑證要求及憑證路徑驗證。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/config">symfony/config</a>
    </td>
    <td>資料庫</td>
    <td>協助您尋找、載入、組合、自動填寫及驗證任何型別的設定值</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/console">symfony/主控台</a>
    </td>
    <td>資料庫</td>
    <td>輕鬆建立美觀且可測試的指令行介面</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/css-selector">symfony/css-selector</a>
    </td>
    <td>資料庫</td>
    <td>將CSS選取器轉換為XPath運算式</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/dependency-injection">symfony/相依性插入</a>
    </td>
    <td>資料庫</td>
    <td>可讓您標準化並集中處理應用程式中建構物件的方式</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/deprecation-contracts">symfony/deprecation-contracts</a>
    </td>
    <td>資料庫</td>
    <td>用於觸發淘汰通知的通用函式和慣例</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/error-handler">symfony/error-handler</a>
    </td>
    <td>資料庫</td>
    <td>提供管理錯誤和輕鬆偵錯PHP程式碼的工具</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/event-dispatcher">symfony/event-dispatcher</a>
    </td>
    <td>資料庫</td>
    <td>提供工具，可讓您的應用程式元件透過傳送事件並接聽它們來彼此通訊</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/event-dispatcher-contracts">symfony/event-dispatcher-contracts</a>
    </td>
    <td>資料庫</td>
    <td>與分派事件相關的一般抽象概念</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/filesystem">symfony/檔案系統</a>
    </td>
    <td>資料庫</td>
    <td>提供檔案系統的基本公用程式</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/finder">symfony/finder</a>
    </td>
    <td>資料庫</td>
    <td>透過直覺式的流暢介面尋找檔案和目錄</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/http-client">symfony/http-client</a>
    </td>
    <td>資料庫</td>
    <td>提供強大的方法來同步或非同步擷取HTTP資源</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/http-client-contracts">symfony/http-client-contracts</a>
    </td>
    <td>資料庫</td>
    <td>與HTTP使用者端相關的一般抽象概念</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/http-foundation">symfony/http-foundation</a>
    </td>
    <td>資料庫</td>
    <td>定義HTTP規格的物件導向圖層</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/http-kernel">symfony/http-kernel</a>
    </td>
    <td>資料庫</td>
    <td>提供將請求轉換為回應的結構化程式</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/intl">symfony/intl</a>
    </td>
    <td>資料庫</td>
    <td>提供ICU資料庫的本地化資料存取</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/mailer">symfony/mailer</a>
    </td>
    <td>資料庫</td>
    <td>協助傳送電子郵件</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/mime">symfony/mime</a>
    </td>
    <td>資料庫</td>
    <td>允許操控MIME訊息</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-ctype">symfony/polyfill-ctype</a>
    </td>
    <td>資料庫</td>
    <td>Ctype函式的Symfony Polyfill</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-intl-grapheme">symfony/polyfill-intl-grapheme</a>
    </td>
    <td>資料庫</td>
    <td>用於intl的grapheme_*函式的Symfony polyfill</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-intl-idn">symfony/polyfill-intl-idn</a>
    </td>
    <td>資料庫</td>
    <td>intl的idn_to_ascii和idn_to_utf8函式的Symfony Polyfill</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-intl-normalizer">symfony/polyfill-intl-normalizer</a>
    </td>
    <td>資料庫</td>
    <td>intl的Normalizer類別和相關函式的Symfony polyfill</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-mbstring">symfony/polyfill-mbstring</a>
    </td>
    <td>資料庫</td>
    <td>Mbstring延伸的Symfony Polyfill</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php73">symfony/polyfill-php73</a>
    </td>
    <td>資料庫</td>
    <td>Symfony polyfill將一些PHP 7.3+功能回移植到較低的PHP版本</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php80">symfony/polyfill-php80</a>
    </td>
    <td>資料庫</td>
    <td>Symfony polyfill將一些PHP 8.0+功能回移植到較低的PHP版本</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php81">symfony/polyfill-php81</a>
    </td>
    <td>資料庫</td>
    <td>Symfony polyfill將一些PHP 8.1+功能回移植到較低的PHP版本</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php82">symfony/polyfill-php82</a>
    </td>
    <td>資料庫</td>
    <td>Symfony polyfill將一些PHP 8.2+功能回移植到較低的PHP版本</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php83">symfony/polyfill-php83</a>
    </td>
    <td>資料庫</td>
    <td>Symfony polyfill將一些PHP 8.3+功能回移植到較低的PHP版本</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/process">symfony/process</a>
    </td>
    <td>資料庫</td>
    <td>執行子處理序中的命令</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/service-contracts">symfony/服務合約</a>
    </td>
    <td>資料庫</td>
    <td>與撰寫服務相關的一般抽象概念</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/string">symfony/字串</a>
    </td>
    <td>資料庫</td>
    <td>為字串提供物件導向的API，並以統一的方式處理位元組、UTF-8字碼點和字首叢集</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/var-dumper">symfony/var-dumper</a>
    </td>
    <td>資料庫</td>
    <td>提供用於瀏覽任意PHP變數的機制</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/var-exporter">symfony/var-exporter</a>
    </td>
    <td>資料庫</td>
    <td>允許將任何可序列化的PHP資料結構匯出為純PHP程式碼</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/yaml">symfony/yaml</a>
    </td>
    <td>資料庫</td>
    <td>載入和傾印YAML檔案</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/web-token/jwt-framework">web-token/jwt-framework</a>
    </td>
    <td>Symfony套裝</td>
    <td>PHP和Symfony套件組合的JSON物件簽署和加密程式庫。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/webonyx/graphql-php">webonyx/graphql-php</a>
    </td>
    <td>資料庫</td>
    <td>GraphQL參考實作的PHP連線埠</td>
  </tr>
  </tbody>
</table>

### OSL-3.0、AFL-3.0

<table>
  <thead>
    <tr>
      <th>名稱</th>
      <th>型別</th>
      <th>說明</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      paypal/module-braintree-customer-balance
    </td>
    <td>Magento2模組</td>
    <td>不適用</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-gift-card
    </td>
    <td>Magento2模組</td>
    <td>不適用</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-gift-card-account
    </td>
    <td>Magento2模組</td>
    <td>不適用</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-gift-wrapping
    </td>
    <td>Magento2模組</td>
    <td>不適用</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-graph-ql
    </td>
    <td>Magento2模組</td>
    <td>不適用</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-reward
    </td>
    <td>Magento2模組</td>
    <td>不適用</td>
  </tr>
  </tbody>
</table>

### OSL-3.0

<table>
  <thead>
    <tr>
      <th>名稱</th>
      <th>型別</th>
      <th>說明</th>
    </tr>
  </thead>
  <tbody>
  </tbody>
</table>

### PHP

<table>
  <thead>
    <tr>
      <th>名稱</th>
      <th>型別</th>
      <th>說明</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/2tvenom/CBOREncode">2tvenom/cborencode</a>
    </td>
    <td>資料庫</td>
    <td>PHP的CBOR編碼器</td>
  </tr>
  </tbody>
</table>

### Proprietary

<table>
  <thead>
    <tr>
      <th>名稱</th>
      <th>型別</th>
      <th>說明</th>
    </tr>
  </thead>
  <tbody>
  </tbody>
</table>

### proprietary

<table>
  <thead>
    <tr>
      <th>名稱</th>
      <th>型別</th>
      <th>說明</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      paypal/module-braintree-core
    </td>
    <td>Magento2模組</td>
    <td>取自適用於PayPal的Gene Commerce所撰寫的Magento Braintree 2.2.0模組。</td>
  </tr>
  </tbody>
</table>
