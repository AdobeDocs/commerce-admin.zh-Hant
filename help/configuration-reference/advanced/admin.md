---
title: '[!UICONTROL Advanced] &amp；gt； [!UICONTROL Admin]'
description: 檢閱Commerce管理員的[!UICONTROL Advanced] &amp；gt； [!UICONTROL Admin]頁面上的組態設定。
exl-id: 546b8d01-9611-4415-ab2b-29be560316f5
role: Admin
feature: Configuration, Admin Workspace
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1209'
ht-degree: 0%

---

# 進階>管理員

{{config}}

## [!UICONTROL Admin User Emails]

![管理員使用者電子郵件](./assets/admin-admin-user-emails.png)<!-- zoom -->

如需有關變更這些設定的詳細資訊，請參閱[忘記密碼並重設電子郵件](../../systems/permissions-users-all.md#forgotten-password-and-reset-emails)。

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|---------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Forgot Password Email Template] | 全域 | 識別在管理員使用者忘記密碼時用於傳送之訊息的電子郵件範本。 預設範本： `Forgot Admin Password` |
| [!UICONTROL Forgot and Reset Email Sender] | 全域 | 識別顯示為&#x200B;_忘記密碼_&#x200B;電子郵件寄件者的商店連絡人。 預設寄件者： `General Contact`<br/>其他寄件者選項： `Sales Representative`、`Customer Support`、`Custom Email` |
| [!UICONTROL User Notification Template] | 全域 | 決定用來作為管理員通知預設值的電子郵件範本。 預設範本： `User Notification` |

{style="table-layout:auto"}

## [!UICONTROL Startup Page]

![啟動頁面](./assets/admin-startup-page.png)<!-- zoom -->

如需有關變更這些設定的詳細資訊，請參閱&#x200B;_快速入門手冊_&#x200B;中的[變更啟動頁面](../../getting-started/admin-dashboard.md#change-the-startup-page)。

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|---------------------------|------------------------------------------------------------------------|------------------------------------------------------------------|
| [!UICONTROL Startup Page] | 全域 | 決定您登入後所顯示的管理員登陸頁面。 |

{style="table-layout:auto"}

### [!UICONTROL Startup Page]選項

| 區域 |                                                                                                                                                                                                                                                                                                                                                                           | 選項 |
|---------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [`Dashboard`](../../getting-started/admin-dashboard.md) |                                                                                                                                                                                                                                                                                                                                                                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| `Sales` | `Operations` | [`Quotes`](../../b2b/quotes.md) ![Adobe Commerce B2B](../../assets/b2b.svg) <br/>[`Orders`](../../stores-purchase/orders.md)<br/>[`Invoices`](../../stores-purchase/invoices.md)<br/>[`Shipments`](../../stores-purchase/shipments.md)<br/>[`Credit Memos`](../../stores-purchase/credit-memos.md)<br/>[`Billing Agreements`](../../stores-purchase/paypal-billing-agreements.md)<br/>[`Returns`](../../stores-purchase/returns.md) ![Adobe Commerce](../../assets/adobe-logo.svg) </span><br/>[`Transactions`](../../stores-purchase/transactions.md)<br/>`Braintree Virtual Terminal` |
| `Catalog` | [`Inventory`](../../inventory-management/introduction.md) | [`Products`](../../catalog/products-list.md)<br/>[`Categories`](../../catalog/categories.md)<br/>[`Shared Catalog`](../../b2b/catalog-shared-create.md) ![Adobe Commerce B2B](../../assets/b2b.svg) |
| `Customers` | [`All Customers`](../../customers/customers-all.md)<br/>[`Now Online`](../../customers/now-online.md)<br/>[`Customer Groups`](../../customers/customer-groups.md)<br/>[`Segments`](../../customers/customer-segments.md) ![Adobe Commerce](../../assets/adobe-logo.svg) <br/>[`Companies`](../../b2b/account-companies.md)![Adobe Commerce B2B](../../assets/b2b.svg) |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| `Marketing` | `Promotions` | [`Catalog Price Rule`](../../merchandising-promotions/price-rules-catalog.md) <br/>[`Cart Price Rules`](../../merchandising-promotions/price-rules-cart.md)) <br/>[`Related Products Rules`](../../merchandising-promotions/product-related-rules.md) ![Adobe Commerce](../../assets/adobe-logo.svg) <br/>[`Gift Card Accounts`](../../stores-purchase/product-gift-card-accounts.md) ![Adobe Commerce](../../assets/adobe-logo.svg) |
|                                                         | [`Private Sales`](../../merchandising-promotions/events-private-sales.md) ![Adobe Commerce](../../assets/adobe-logo.svg) | [`Events`](../../merchandising-promotions/event-configure.md) <br/>[`Invitations`](../../merchandising-promotions/invitations.md) |
|                                                         | `Communications` | [`Email Templates`](../../systems/email-templates.md) <br/>[`Newsletter Template`](../../merchandising-promotions/newsletter-template.md) <br/>[`Newsletter Queue`](../../merchandising-promotions/newsletter-queue.md) <br/>[`Newsletter Subscribers`](../../merchandising-promotions/newsletter-subscribers.md) <br/>[`Email Reminders`](../../merchandising-promotions/email-reminder-rules.md) ![Adobe Commerce](../../assets/adobe-logo.svg) |
|                                                         | `SEO & Search` | [`Search Terms`](../../catalog/search-terms.md) <br/>[`Search Synonyms`](../../catalog/search-terms.md#search-synonyms) ![Adobe Commerce](../../assets/adobe-logo.svg)<br/>[`URL Rewrites`](../../merchandising-promotions/url-rewrite.md) <br/>[`Site Map`](../../merchandising-promotions/sitemap-xml.md) |
|                                                         | [`User Content`](../../catalog/settings-advanced-product-reviews.md) | [`All Reviews`](../../catalog/settings-advanced-product-reviews.md) <br/>[`Pending Reviews`](../../merchandising-promotions/product-reviews-moderate.md) <br/> |
| `Content` | `Elements` | [`Pages`](../../content-design/pages.md)<br/>[`Hierarchy`](../../content-design/page-hierarchy.md) ![Adobe Commerce](../../assets/adobe-logo.svg)<br/>[`Blocks`](../../content-design/blocks.md)<br/>[`Dynamic Blocks`](../../content-design/dynamic-blocks.md) ![Adobe Commerce](../../assets/adobe-logo.svg)<br/>[`Widgets`](../../content-design/widgets.md)<br/>[`Media Gallery`](../../content-design/media-storage.md) |
|                                                         | `Design` | [`Configuration`](../../content-design/configuration.md)<br/>[`Themes`](../../content-design/themes.md)<br/>[`Schedule`](../../content-design/schedule.md) |
|                                                         | `Content Staging` ![Adobe Commerce](../../assets/adobe-logo.svg)<br /> | [儀表板](../../content-design/content-staging.md) |
| `Reports` | [`Marketing`](../../getting-started/marketing-reports.md) | `Products in Cart`<br />`Search Terms`<br />`Abandoned Carts`<br />`Newsletter Problem Reports` |
|                                                         | [`Reviews`](../../getting-started/review-reports.md) | `By Customer`<br/> `By Products`<br/> |
|                                                         | [`Sales`](../../getting-started/sales-reports.md) | `Orders`<br/>`Tax`<br/>`Invoiced`<br/>`Shipping`<br/>`Refunds`<br/>`Coupons`<br/>`PayPal Settlement`<br/>`Braintree Settlement` |
|                                                         | `System Insights` | [`Site-Wide Analysis Tool`](https://experienceleague.adobe.com/docs/commerce-operations/tools/site-wide-analysis-tool/access.html) ![Adobe Commerce](../../assets/adobe-logo.svg) |
|                                                         | [`Customers`](../../getting-started/customer-reports.md) | `Order Total`<br/>`Order Count`<br/>`New`<br/>`Wish Lists`<br/>`Segments`<br/> |
|                                                         | [`Products`](../../getting-started/product-reports.md) | `Views`<br/>`Bestsellers`<br/>`Low Stock`<br/>`Ordered`<br/>`Downloads` |
|                                                         | [`Private Sales`](../../getting-started/private-sales-reports.md) ![Adobe Commerce](../../assets/adobe-logo.svg) | `Invitations`<br/>`Invited Customers`<br/>`Conversions` |
|                                                         | `Statistics` | [`Refresh Statistics`](../../getting-started/sales-reports.md#refresh-statistics) |
|                                                         | [`Business Intelligence`](../../getting-started/business-intelligence.md) | `Advanced Reporting`<br/>`BI Essentials`<br/> |
|                                                         | `Customer Engagement` | `Dashboard`<br/>`Importer Status`<br/>`Automation Enrollment`<br/>`Campaign Sends`<br/>`SMS Sends`<br/>`Cron Tasks`<br/>`Log Viewer`<br/>`Abandoned Carts` |
| `Stores` | `Settings` | [`All Stores`](../../stores-purchase/stores.md)<br/>[`Configuration`](../../configuration-reference/guide-overview.md)<br/>[`Terms and Conditions`](../../stores-purchase/terms-and-conditions.md)<br/>[`Order Status`](../../stores-purchase/order-status.md) |
|                                                         | [`Inventory`](../../inventory-management/introduction.md) | [`Sources`](../../inventory-management/sources-stocks.md#sources)<br/>[`Stocks`](../../inventory-management/sources-stocks.md#stocks) |
|                                                         | [`Taxes`](../../stores-purchase/taxes.md) | [`Tax Rules`](../../stores-purchase/tax-rules.md)<br/>[`Tax Zones and Rates`](../../stores-purchase/tax-zones-rates.md) |
|                                                         | [`Currency`](../../stores-purchase/currency.md) | [`Currency Rates`](../../stores-purchase/currency-configuration.md)<br/>[`Currency Symbols`](../../stores-purchase/currency-configuration.md#step-5-customize-currency-symbols-optional) |
|                                                         | `Attributes` | [`Customer`](../../systems/data-attributes-customer.md)<br/>[`Customer Address`](../../systems/data-attributes-customer.md#customer-addresses)<br/>[`Product`](../../systems/data-attributes-product.md)<br/>[`Attribute Set`](../../catalog/attribute-sets.md)<br/>[`Returns`](../../stores-purchase/attributes-returns.md)<br/>[`Ratings`](../../merchandising-promotions/product-reviews.md#create-custom-ratings) |
|                                                         | `Other Settings` | [`Reward Exchange Rates`](../../merchandising-promotions/reward-exchange-rates.md)<br/>[`Gift Wrapping`](../../stores-purchase/cart-configuration.md#gift-wrap)<br/>[`Gift Registry`](../../merchandising-promotions/gift-registry-create.md) |
| `System` | [`Data Transfer`](../../systems/data-transfer.md) | [`Import`](../../systems/data-import.md)<br/>[`Export`](../../systems/data-export.md)<br/>[`Import/Export Tax Rates`](../../systems/data-transfer-tax-rates.md)<br/>[`Import History`](../../systems/data-import.md#import-history)<br/>[`Scheduled Import/Export`](../../systems/data-scheduled-import-export.md) |
|                                                         | `Extensions` | [`Integrations`](../../systems/integrations.md) |
|                                                         | `Tools` | [`Cache Management`](../../systems/cache-management.md)<br/>[`Index Management`](../../systems/index-management.md) |
|                                                         | `Support` | [`Data Collector`](../../systems/support.md#data-collector)<br/>[`System Report`](../../systems/support.md#system-reports) |
|                                                         | `Permissions` | [`All Users`](../../systems/permissions-users-all.md)<br/>[`Locked Users`](../../systems/permissions-users-all.md#locked-users)<br/>[`User Roles`](../../systems/permissions-user-roles.md) |
|                                                         | `Action Log` ![Adobe Commerce](../../assets/adobe-logo.svg) | [`Report`](../../systems/action-log.md)<br/>[`Archive`](../../systems/action-log-archive.md)<br/>[`Bulk Actions`](../../systems/action-log-bulk-actions.md) |
|                                                         | `Other Settings` | [`Notifications`](../../systems/notifications.md)<br/>[`Custom Variables`](../../systems/variables-custom.md)<br/>[`Manage Encryption Key`](../../systems/encryption-key.md) |
| `Find Partners & Extensions` |                                                                                                                                                                                                                                                                                                                                                                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |

{style="table-layout:auto"}

<!-- Feature still in development 
## [!UICONTROL Unified Experience]

![Store Configuration for Unified Experience](./assets/admin-uex-configuration.png)

The [!UICONTROL Unified Experience] option is available in Adobe Commerce deployments that have the Commerce Admin Unified Experience extension loaded. This extension enables integration with Experience Cloud to streamline cross-application workflows between Commerce and other Experience Cloud solutions. See [Adobe Experience Cloud Integration for Commerce Admin](../../getting-started/admin-unified-experience-integration-overview.md).

| Field        | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Description                                                                                                                                                                                                                                                                                                                                                                    |
|--------------|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Enable       | Global                                                                 | Determines if the Commerce instance uses the Experience Cloud integration. Before enabling this feature, review the [requirements and configuration instructions](../../getting-started/admin-unified-experience-integration-overview.md). Options: Yes/No.                                                                                                                    |
| Project Name | Global                                                                 | Identifies the instance in the Experience Cloud Commerce Projects workspace when the Unified Experience is enabled. The name can contain only alphanumeric characters and spaces. Defaults to the [cloud environment name](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-architecture.html?lang=en#pro-environment-architecture). |

{style="table-layout:auto"}

-->

## [!UICONTROL Admin Base URL]

![管理基底URL](./assets/admin-admin-base-url.png)<!-- zoom -->

如需有關設定這些選項的詳細資訊，請參閱&#x200B;_存放和購買體驗指南_&#x200B;中的[設定基底URL](../../stores-purchase/store-urls.md#configure-the-base-url)。

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|------------------------------------|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Use Custom Admin URL] | 全域 | 決定是否使用自訂URL來存取管理員。 選項： `Yes` / `No` |
| [!UICONTROL Custom Admin URL] | 全域 | 指定存取管理員的自訂URL。 依預設，管理員URL與基底URL相同。<br/>**重要：**&#x200B;管理員URL必須位於相同的Commerce安裝中，並且具有與店面相同的檔案根目錄。 |
| [!UICONTROL Use Custom Admin Path] | 全域 | 決定是否使用自訂路徑來存取管理員。 預設路徑為`admin`。 選項： `Yes` / `No` |
| [!UICONTROL Custom Admin Path] | 全域 | 將預設管理員路徑名稱變更為難以猜測的名稱。 以小寫字元輸入自訂路徑名稱。 例如： `aardvark` |

{style="table-layout:auto"}

## [!UICONTROL Security]

![安全性](./assets/admin-security.png)<!-- zoom -->

如需有關設定這些選項的詳細資訊，請參閱&#x200B;_管理系統指南_&#x200B;中的[設定管理安全性](../../systems/security-admin.md)。

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Admin Account Sharing] | 存放區檢視 | 決定管理員使用者是否可從不同裝置同時登入相同帳戶。 選項： <br/>**`Yes`**— 允許來自同一個Admin帳戶的多個作用中工作階段。<br/>**`No`** — 每個管理員帳戶只允許一個使用中的工作階段。 |
| [!UICONTROL Password Reset Protection Type] | 存放區檢視 | 決定用來管理密碼重設要求的方法。 選項： <br/>**`By IP and Email`**— 收到通知的回應後，可以將密碼重設到與Admin帳戶關聯的電子郵件地址。<br/>**`By IP`** — 密碼可以線上上重設，不需要其他確認。 <br/>**`By Email`**— 密碼只能透過電子郵件回應傳送至與Admin帳戶相關之電子郵件地址的通知來重設。<br/>**`None`** — 密碼只能由存放區管理員重設。 |
| [!UICONTROL Recovery Link Expiration Period (hours)] | 全域 | 決定密碼復原連結保持有效的小時數。 |
| [!UICONTROL Max Number of Password Reset Requests] | 存放區檢視 | 決定每小時可提交的最大密碼要求數。 |
| [!UICONTROL Min Time Between Password Reset Requests] | 存放區檢視 | 決定密碼重設要求之間的最小分鐘數。 |
| [!UICONTROL Add Secret Key to URLs] | 全域 | 啟用後，會將秘密金鑰附加至管理員URL，作為防範利用漏洞的預防措施。 選項： `Yes` / `No` |
| [!UICONTROL Login Is Case Sensitive] | 全域 | 判斷使用者輸入的登入認證是否必須符合儲存的認證大小寫。 選項： `Yes` / `No` |
| [!UICONTROL Admin Session Lifetime (seconds)] | 全域 | 決定管理員工作階段的長度（以秒為單位）。 |
| [!UICONTROL Maximum Login Failures to Lockout Account] | 全域 | 決定鎖定帳戶前，管理員使用者可嘗試登入的次數。 如果欄位為空，則不會設定最小值。 預設值： `6` |
| [!UICONTROL Lockout Time (minutes)] | 全域 | 決定系統管理員帳戶在使用者嘗試重新登入前被鎖定的分鐘數。 預設值： `30` |
| [!UICONTROL Password Lifetime (days)] | 全域 | 決定管理員密碼過期的天數。 如果欄位為空，則不會設定存留期。 預設值： `90` |
| [!UICONTROL Password Change] | 全域 | 決定是否要求管理員使用者變更密碼。 選項： <br/>**`Forced`**— 要求系統管理員使用者在設定帳戶之後變更密碼。<br/>**`Recommended`** — 建議管理員使用者在設定帳戶後變更密碼。 |

{style="table-layout:auto"}

## [!UICONTROL Dashboard]

![儀表板](./assets/admin-dashboard.png)<!-- zoom -->

如需有關設定這些選項的詳細資訊，請參閱&#x200B;_快速入門手冊_&#x200B;中的[管理員儀表板](../../getting-started/admin-dashboard.md)。

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|----------------------------|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Charts] | 全域 | 決定儀表板是否包含從目前銷售資料產生的圖表。 選項： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Admin Grids]

![管理網格](./assets/admin-admin-grids.png)<!-- zoom -->

如需有關設定這些選項的詳細資訊，請參閱&#x200B;_目錄管理指南_&#x200B;中的[限制產品顯示](../../catalog/products-list.md#limit-product-display)。

>[!NOTE]
>
>若要改善大型型錄的效能，建議您限制格線中顯示的產品數目。

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|-----------------------------------------------|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Limit Number of Products in Grid] | 全域 | 決定格線顯示的產品數目是否限製為&#x200B;_[!UICONTROL Records Limit]_值。 選項： `Yes` / `No` |
| [!UICONTROL Records Limit] | 全域 | 設定產品格線中的產品數限制。 預設最小值為`20000`。 |

## [!UICONTROL CAPTCHA]

![驗證碼](./assets/admin-captcha.png)<!-- zoom -->

如需有關設定這些選項的詳細資訊，請參閱&#x200B;_系統管理系統指南_&#x200B;中的[驗證碼](../../systems/security-captcha.md)。

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|-------------------------------------------------------|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable CAPTCHA in Admin] | 全域 | 啟用驗證碼以供管理員登入。 選項： `Yes` / `No` |
| [!UICONTROL Font] | 全域 | 決定用於顯示驗證碼的字型。 若要新增您自己的字型，請將字型檔案放在與您的Commerce執行個體相同的目錄中，並將宣告新增至config.xml檔案的`app/code/Magento/Captcha/etc`預設字型：` LinLibertine` |
| [!UICONTROL Forms] | 全域 | 決定使用CAPTCHA的表單。 選項： `Admin Login` / `Admin Forgot Password` |
| [!UICONTROL Displaying Mode] | 全域 | 決定驗證碼何時出現。 選項： <br/>**`Always`**— 登入一律需要CAPTCHA。<br/>**`After number of attempts to login`** — 顯示[!UICONTROL Number of Unsuccessful Attempts to Login]欄位。 輸入允許的登入嘗試次數。 值0 （零）類似於將「顯示模式」設定為「一律顯示」。 此選項不會涵蓋「忘記密碼」和「建立使用者」表單。 如果已啟用驗證碼並設定為顯示，則會始終將其包含在表單中。<br />**注意**：若要追蹤失敗的登入嘗試次數，每個嘗試使用一個電子郵件地址和一個IP位址登入都會被計入。 允許來自相同IP位址的登入嘗試次數上限為1,000。 此限制僅在啟用驗證碼時適用。 |
| [!UICONTROL Number of Unsuccessful Attempts to Login] | 全域 | 決定帳戶鎖定前使用者可嘗試登入的次數。 為了追蹤失敗的登入嘗試次數，系統會從單一IP位址追蹤一個電子郵件地址的嘗試。 允許來自相同IP位址的最大嘗試次數為1,000。 此限制僅在啟用驗證碼時適用。 |
| [!UICONTROL CAPTCHA Timeout (minutes)] | 全域 | 決定目前驗證碼的存留期。 驗證碼過期時，使用者必須重新載入頁面。 |
| [!UICONTROL Number of Symbols] | 全域 | 決定驗證碼中使用的符號數。 允許的最大值為`8`。 您也可以指定範圍，例如`5-8`。 |
| [!UICONTROL Symbols Used in CAPTCHA] | 全域 | 決定驗證碼中使用的符號。 只允許使用字母（a-z和A-Z）和數字(0-9)。 此欄位中建議的預設符號集不包括相似符號，例如i、l或1。 在驗證碼中顯示這些符號，會降低使用者正確辨識驗證碼的機會。 |
| [!UICONTROL Case Sensitive] | 全域 | 判斷驗證碼中使用的字元是否區分大小寫。 選項： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Admin Actions Logging]

{{ee-feature}}

![管理動作記錄](./assets/admin-actions-logging.png)<!-- zoom -->

如需有關設定這些選項的詳細資訊，請參閱&#x200B;_系統管理系統指南_&#x200B;中的[動作記錄檔封存](../../systems/action-log-archive.md)。

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|-----------------------------|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Actions] | 全域 | 為每個選取的動作啟用動作記錄： <br/>`Admin My Account` <br/>`Admin Permission Roles` <br/>`Admin Permission Users` <br/>`Admin Sign In` <br/>`CMS Blocks` <br/>`CMS Hierarchy` <br/>`CMS Pages` <br/>`Cache Management` <br/>`Cart Price Rules` <br/>`Catalog Attributes` <br/>`Catalog Categories` <br/>`Catalog Events` <br/>`Catalog Price Rules` <br/>`Catalog Product Tax Classes` <br/>`Catalog Product Templates` <br/>`Catalog Products` <br/>`Catalog Ratings` <br/>`Catalog Reviews` <br/>`Catalog Search` <br/>`Checkout Terms and Conditions` <br/>`Companies` <br/>`Company Credit` <br/>`Custom Variables` <br/>`Customer Groups` <br/>`Customer Invitations` <br/>`Customer Tax Classes` <br/>`Customers` <br/>`Design Configuration` <br/>`Gift Card Accounts` <br/>`Gift Registry Entity` <br/>`Gift Registry Type` <br/>`Index Management` <br/>`Login as a Customer` <br/>`Manage Currency Rates` 3} <br/>`Manage Customer Address Attributes` <br/>`Manage Customer Attributes` <br/>`Manage Design` <br/>`Manage Dynamic Blocks` <br/>`Manage Segments` <br/>`Manage Store Views` <br/>`Manage Stores` <br/>`Manage Websites` <br/>`Negotiable Quotes` <br/>`Newsletter Queue` <br/>`Newsletter Subscribers` <br/>`Newsletter Templates` <br/>`PayPal Settlement Reports` <br/>`Reports` <br/> `Reward Points Rates` <br/>`Rule-Based Product Relations` <br/>`Sales Archive` <br/>`Sales Credit Memos` <br/>`Sales Invoices` <br/>`Sales Order Status` <br/>`Sales Orders` <br/>`Sales Shipments` <br/>`Shared Catalog` <br/>`Shopping Cart Management` <br/>`Store Credit` <br/>`System Backups` <br/>`System Configuration` <br/>`Tax Rates` <br/>`Tax Rules` <br/>`Transactional Emails` <br/>`URL Rewrites` <br/>`Widget` <br/>`XML Sitemap` |

{style="table-layout:auto"}

## [!UICONTROL Admin Usage]

![管理員使用情形](./assets/admin-usage.png)<!-- zoom -->

如需有關設定這些選項的詳細資訊，請參閱&#x200B;_快速入門手冊_&#x200B;中的[使用狀況資料集合](../../getting-started/admin.md#usage-data-collection)。

| 欄位 | 範圍 | 說明 |
|------------------------------------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Admin Usage Tracking] | 全域 | 授予Adobe收集管理員使用資料的許可權，以改善使用&#x200B;_管理員_&#x200B;及相關產品和服務的體驗。 允許資料收集也會啟用&#x200B;_產品內指引_，其設計可為&#x200B;_管理員_&#x200B;提供互動式內容，例如說明、工具提示、逐步指南、上線資訊、功能公告等。 使用資料中未識別個別管理員。 選項：<br />**`Yes`**— 允許資料收集並啟用&#x200B;_產品內指引_。<br />**`No`** — 不允許資料收集或啟用&#x200B;_產品內指引_。 |

{style="table-layout:auto"}
