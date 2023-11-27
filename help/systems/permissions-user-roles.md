---
title: 使用者角色
description: 瞭解如何建立使用者角色和相關許可權，以管理對管理員功能的存取。
exl-id: a70f74d4-72b4-4639-a67d-9fc13df65924
feature: Admin Workspace, Roles/Permissions, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '659'
ht-degree: 0%

---

# 使用者角色

若要將受限存取權授予某人，第一步是建立具有適當許可權等級的角色。 儲存角色後，您可以新增使用者並指派受限制角色，以授予他們管理員受限制的存取權。

![管理員 — 使用者角色](./assets/permissions-role-grid.png){width="600" zoomable="yes"}

## 定義角色

1. 在 _管理員_ 側欄，前往 **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**.

1. 在右上角，按一下 **[!UICONTROL Add New Role]**.

1. 完成步驟以定義角色：

### 步驟1：新增角色名稱

1. 在 _[!UICONTROL Role Information]_，輸入描述性&#x200B;**[!UICONTROL Role Name]**.

1. 在 _[!UICONTROL Current User Identity Verification]_，輸入您的密碼。

   ![系統許可權 — 角色資訊](./assets/permissions-role-info.png){width="600" zoomable="yes"}

### 步驟2：指派資源

>[!IMPORTANT]
>
>指派資源時，如果您限制指定角色的存取權，請務必停用許可權工具的存取權。 否則，使用者可以修改自己的許可權。

1. 設定 **[!UICONTROL Role Scopes]** 變更為下列其中一項：

   - `All`
   - `Custom`

   如果設為 `Custom` 若為多站台安裝，請選取要使用角色的網站和存放區核取方塊。

   ![使用者角色資源 — 自訂範圍](./assets/permissions-role-scope-custom.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >使用者具有 `Custom` 角色範圍無法建立網站和類別、將產品指派至類別，或在 _[!UICONTROL All Store Views]_當它們被指派至受限制的存放區時的範圍。 這些使用者也無法執行其他作業_&#x200B;全域&#x200B;_會影響他們無權存取之範圍的動作。

1. 在 _[!UICONTROL Roles Resources]_，設定&#x200B;**[!UICONTROL Resource Access]**至 `Custom`.

1. 在 **[!UICONTROL Resource]** 樹狀結構中，選取角色可存取之每個管理員權能的核取方塊。

   若要建立可存取稅捐設定的「管理員」角色，請選擇「銷售/稅捐」與「系統/稅捐」資源。 如果為不同於預設值的區域設定網站 [出貨地點來源](../stores-purchase/shipping-settings.md#point-of-origin)，您必須允許角色存取系統/送貨資源。 出貨設定會決定用於型錄價格的商店稅率。

   ![已指派的使用者角色資源](./assets/permissions-role-resources-product.png){width="600" zoomable="yes"}

   可用許可權清單可能包含套件和已安裝擴充功能的其他選項。 選取每個功能的最上層許可權，您即可指派所有使用者可用的許可權。

   >[!NOTE]
   >
   >管理員使用者必須具備 **[!UICONTROL Sales / Archive]** 其角色範圍的許可權，以檢視 _[!UICONTROL Invoices]_，_[!UICONTROL Credit Memos]_、和 _[!UICONTROL Shipments]_訂購 [索引標籤](../stores-purchase/order-processing.md).

1. 完成後，按一下 **[!UICONTROL Save Role]**.

   角色現在會顯示在網格中，並可指派給使用者帳戶。

## 指派角色給使用者

1. 從 _[!UICONTROL Roles]_格線中，以編輯模式開啟記錄。

1. 在 _[!UICONTROL Current User Identity Verification]_，輸入您的使用者帳戶密碼。

1. 在左側面板中，選擇 **[!UICONTROL Role Users]**.

   此 _[!UICONTROL Role Users]_選項僅在儲存新角色後顯示。

   ![指派給角色的使用者帳戶](./assets/permissions-role-users.png){width="600" zoomable="yes"}

1. 若要搜尋特定使用者記錄，請執行下列動作：

   - 在欄頂端的搜尋篩選器中輸入值，然後按 **輸入**.

   - 當您準備好返回完整清單時，請按一下 **[!UICONTROL Reset Filter]**.

1. 選取要指派給角色的任何使用者的核取方塊。

1. 按一下 **[!UICONTROL Save Role]**.

## 編輯角色

1. 在 _管理員_ 側欄，前往 **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**.

1. 使用格線上方的篩選條件來找出角色，然後按一下角色名稱。

1. 進行必要的變更。

   檢閱建立使用者角色的步驟，以取得角色設定的相關資訊。

1. 出現提示時，請輸入您的密碼以確認您的身分。

1. 按一下 **[!UICONTROL Save Role]**.

## 刪除角色

1. 在 _管理員_ 側欄，前往 **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**.

1. 使用格線上方的篩選條件來找出角色，並在編輯模式下開啟。

1. 在右上角，按一下 **[!UICONTROL Delete Role]**.

1. 若要確認動作，請按一下 **[!UICONTROL OK]**.

## 使用者角色示範

觀看此影片以瞭解管理使用者角色的相關資訊：

>[!VIDEO](https://video.tv.adobe.com/v/343654?quality=12)

## 角色資源

可將下列資源的存取權指派給自訂角色。 請參閱連結的頁面，以進一步瞭解與每個資源相關聯的功能。

![Adobe Commerce](../assets/adobe-logo.svg)  — 僅限Adobe Commerce

![適用於Adobe Commerce的B2B](../assets/b2b.svg)  — 僅適用於Adobe Commerce的B2B

| 資源 |   |   |
| --- | --- | --- |
| [`Dashboard`](../getting-started/admin-dashboard.md) |  |  |
| [`Sales`](../stores-purchase/sales-menu.md) | [`Operations`](../stores-purchase/orders.md) |  |
|  | [`Quotes`](../b2b/quotes.md) ![適用於Adobe Commerce的B2B](../assets/b2b.svg) <br/>[`Orders`](../stores-purchase/orders.md)<br/>[`Invoices`](../stores-purchase/invoices.md)<br/>[`Shipments`](../stores-purchase/shipments.md)<br/>[`Credit Memos`](../stores-purchase/credit-memos.md)<br/>[`Billing Agreements`](../stores-purchase/paypal-billing-agreements.md)<br/>[`Returns`](../stores-purchase/returns.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Transactions`](../stores-purchase/transactions.md) |
|  | [`Archive`](action-log-archive.md)![Adobe Commerce] |  |
|  | [`Shopping Cart Management`](../stores-purchase/cart.md) |  |
| [`Catalog`](../catalog/catalog-menu.md) | [`Category Permissions`](../catalog/categories.md) ![Adobe Commerce](../assets/adobe-logo.svg) |  |
|  | [`Inventory`](../inventory-management/introduction.md) | [`Products`](../catalog/products-list.md)<br/>[`Categories`](../catalog/categories.md) |
|  | [`Shared Catalog`](../b2b/catalog-shared-create.md) ![適用於Adobe Commerce的B2B](../assets/b2b.svg) | [`Manage Shared Catalog`](../b2b/catalog-shared-manage.md) |
| [`Customers`](../customers/guide-overview.md) | [`All Customers`](../customers/customers-all.md)<br/>[`Now Online`](../customers/now-online.md)<br/>[`Customer Groups`](../customers/customer-groups.md)<br/>[`Segments`](../customers/customer-segments.md) ![Adobe Commerce](../assets/adobe-logo.svg) |  |
|  | [`Login as Customer`](../customers/login-as-customer.md) | `Allow Login as Customer Button`<br/>`View Login as Customer Log` ![Adobe Commerce](../assets/adobe-logo.svg) |
|  | [`Companies`](../b2b/account-companies.md) ![適用於Adobe Commerce的B2B](../assets/b2b.svg) | [`Manage Companies`](../b2b/account-company-manage.md) <br/>`Add New Company` <br/>`Delete Company` <br/>`Reimburse Balance` |
| [`Carts`](../stores-purchase/shopping-assisted-cart-manage.md) | [`Manage carts`](../stores-purchase/shopping-assisted-cart-manage.md) |  |
| [`My Account`](../customers/account-dashboard-my-account.md) |  |  |
| [`Marketing`](../merchandising-promotions/marketing-menu.md) | [`Promotions`](../merchandising-promotions/marketing-menu.md#uicontrol-promotions) | [`Catalog Price Rule`](../merchandising-promotions/price-rules-catalog.md) <br/>[`Cart Price Rules`](../merchandising-promotions/price-rules-cart.md) <br/>[`Related Products Rules`](../merchandising-promotions/product-related-rules.md)![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Gift Card Accounts`](../stores-purchase/product-gift-card-accounts.md) ![Adobe Commerce](../assets/adobe-logo.svg) |
|  | [`Private Sales`](../merchandising-promotions/events-private-sales.md) ![Adobe Commerce](../assets/adobe-logo.svg) | [`Events`](../merchandising-promotions/event-create.md) <br/>[`Invitations`](../merchandising-promotions/invitations.md) |
|  | `Communications` | [`Email Templates`](email-templates.md) <br/>[`Newsletter Template`](../merchandising-promotions/newsletter-template.md) <br/>[`Newsletter Queue`](../merchandising-promotions/newsletter-queue.md) <br/>[`Newsletter Subscribers`](../merchandising-promotions/newsletter-subscribers.md) <br/>[`Email Reminders`](../merchandising-promotions/email-reminder-rules.md) |
|  | `Sales Channel` | [`Amazon Sales Channel`](https://experienceleague.adobe.com/docs/commerce-channels/amazon/overview.html) |
|  | [`SEO & Search`](../merchandising-promotions/marketing-menu.md#uicontrol-seo--search) | [`Search Terms`](../catalog/search-terms.md) <br/>[`Search Synonyms`](../catalog/search-terms.md#search-synonyms) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`URL Rewrites`](../merchandising-promotions/url-rewrite-custom.md) <br/>[`Site Map`](../merchandising-promotions/sitemap-xml.md) |
|  | [`User Content`](../merchandising-promotions/product-reviews-moderate.md) | [`All Reviews`](../merchandising-promotions/product-reviews.md) <br/>[`Pending Reviews`](../merchandising-promotions/product-reviews-moderate.md) <br/> |  |
| [`Content`](../content-design/content-menu.md) | [`Elements`](../content-design/content-menu.md#uicontrol-elements)) | [`Pages`](../content-design/pages.md)<br/>[`Hierarchy`](../content-design/page-hierarchy.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Blocks`](../content-design/blocks.md)<br/>[`Dynamic Blocks`](../content-design/dynamic-blocks.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Widgets`](../content-design/widgets.md)<br/>[`Media Gallery`](../content-design/media-gallery.md) |  |
|  | [`Design`](../content-design/introduction.md#design) | [`Themes`](../content-design/themes.md)<br/>[`Schedule`](../content-design/schedule.md) |  |
|  | [內容分段](../content-design/content-staging.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br /> |  |
| [`Reports`](../getting-started/reports-menu.md) | [`Marketing`](../getting-started/marketing-reports.md) | `Shopping Cart`<br />[`Search Terms`](../catalog/search-terms.md#search-terms-report)<br />`Newsletter Problem Reports` |  |
|  | [`Reviews`](../getting-started/review-reports.md)<br /> |  |
|  | [`Sales`](../getting-started/sales-reports.md) |  |
|  | `System Insights` ![Adobe Commerce](../assets/adobe-logo.svg) | [`Site-Wide Analysis Tool`](https://experienceleague.adobe.com/docs/commerce-operations/tools/site-wide-analysis-tool/access.html) |
|  | [`Customers`](../getting-started/customer-reports.md)<br/>[`Products`](../getting-started/product-reports.md)<br/>[`Private Sales`](../getting-started/private-sales-reports.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br />[`Statistics`](../getting-started/reports-menu.md#uicontrol-statistics)<br />[`Business Intelligence`](../getting-started/business-intelligence.md) |  |
| [`Stores`](../stores-purchase/stores.md) | [`Settings`](../stores-purchase/stores-menu.md) | [`All Stores`](../stores-purchase/stores.md)<br/>[`Configuration`](../configuration-reference/guide-overview.md)<br/>[`Terms and Conditions`](../stores-purchase/terms-and-conditions.md)<br/>[`Order Status`](../stores-purchase/order-status.md) |  |
|  | [`Inventory`](../inventory-management/sources-stocks.md) | [`Sources`](../inventory-management/sources-manage.md)<br/>[`Stocks`](../inventory-management/stocks-manage.md) |  |
|  | [`Taxes`](../stores-purchase/taxes.md) |  |  |
|  | [`Currency`](../stores-purchase/currency.md) | [`Currency Rates`](../stores-purchase/currency-update.md)<br/>[`Currency Symbols`](../stores-purchase/currency-configuration.md#step-5-customize-currency-symbols-optional) |  |
|  | [`Attributes`](../catalog/product-attributes.md) | [`Product`](../catalog/attribute-product-create.md)<br/>[`Update Attributes`](../catalog/attribute-product-create.md)<br/>[`Attribute Set`](../catalog/attribute-sets.md)<br/>[`Ratings`](../merchandising-promotions/product-reviews.md#create-custom-ratings) |
|  | [`Other Settings`](../stores-purchase/stores-menu.md) | [`Customer Groups`](../customers/customer-groups.md) |
| [`System`](system-menu.md) | [`Data Transfer`](data-transfer.md) | [`Import`](data-import.md)<br/>[`Export`](data-export.md)<br/>[`Import/Export Tax Rates`](data-transfer-tax-rates.md)<br/>[`Import History`](data-import.md#import-history) |  |
|  | [`Magento Connect`](../getting-started/commerce-marketplace.md) | `Connect Manager`<br/>`Package Extensions` |  |
|  | [`Tools`](system-menu.md#tools) | [`Cache Management`](cache-management.md)<br/>[`Backups`](backups.md)<br/>[`Index Management`](index-management.md)<br/>[`Change Indexer Mode`](index-management.md) |  |
|  | [`Permissions`](permissions.md) | [`All Users`](permissions-users-all.md)<br/>[`Locked Users`](permissions-users-all.md#locked-users)<br/>[`User Roles`](permissions-user-roles.md) |
| [`Action Log`](action-log.md)![Adobe Commerce](../assets/adobe-logo.svg) | [`Report`](action-log.md)<br/>[`Archive`](action-log-archive.md) |
|  | [`Other Settings`](system-menu.md) | [`Notifications`](notifications.md)<br/>[`Custom Variables`](variables-custom.md)<br/>[`Manage Encryption Key`](encryption-key.md) |  |
| [`Global Search`](../getting-started/admin-workspace.md#workspace-search) |  |  |

{style="table-layout:auto"}
