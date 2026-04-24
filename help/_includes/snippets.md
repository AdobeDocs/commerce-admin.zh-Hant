---
title: 代碼片段
description: 重複使用附註和視覺元素，以記下套用至特定版本的功能或頁面
source-git-commit: 35147f5ec256445d4cb1dfb2d48d9cfcdc1ff47e
workflow-type: tm+mt
source-wordcount: '818'
ht-degree: 0%

---

# 代碼片段

## 僅供檢視的功能 {#ee-feature}

<table style="border:1px solid red">
<tr><td><img alt="Adobe Commerce功能" src="../assets/adobe-logo.svg" width="20" height="20" /> 這是僅於Adobe Commerce中提供的專屬功能，無法在Magento Open Source中使用。 （<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html?lang=zh-Hant#product-editions">深入瞭解</a>）</td></tr>
</table>

## 僅限B2B功能 {#b2b-feature}

<table style="border:1px solid green">
<tr><td><img alt="Adobe Commerce B2B功能" src="../assets/b2b.svg" width="20" height="20" /> 只有<a href="https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=zh-Hant">Adobe Commerce B2B</a>才提供專屬功能</td></tr>
</table>

## CE only feature {#ce-feature}

<table style="border:1px solid orange">
<tr><td><img alt="Magento Open Source feature" src="../assets/open-source.svg" width="20" height="20" /> Alternative method is required for Magento Open Source (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html?lang=zh-Hant#product-editions">Learn more</a>)</td></tr>
</table>

## IMS admin authentication note {#ims-admin-note}

>[!NOTE]
>
>Adobe Commerce merchants who have an Adobe ID and want a streamlined login to Adobe Commerce and Adobe Business products can integrate Commerce Admin authentication with the Adobe IMS authentication workflow. After this integration is enabled for your Commerce store, each Admin user must use their Adobe credentials — not their Commerce account credentials — to log in. See [Integrating Adobe Commerce with Adobe IMS overview](/help/getting-started/adobe-ims-integration-overview.md).

## GTag APIs note {#gtag-api-note}

>[!NOTE]
>
>Starting with the 2.4.5 release, the Google services integration is updated to support use of the GTag APIs. GTag is a unified mechanism for integration with Google functionality for web pages and supports the newest capabilities and opportunities for tracking and managing content through Google Services.

## URL rewrite automatic skip note {#url-rewrite-skip}

>[!NOTE]
>
>When automatic redirects are enabled and you save a category, all product and category rewrites are generated in real time and stored in rewrite tables by default. This process could result in significant performance issues for categories with many assigned products. The solution is to change this default and skip the generation of category/products URL rewrites of products for category save. In this case, product rewrites are generated only for the canonical product URL. See [Automatic product redirects](/help/merchandising-promotions/url-redirect-product-automatic.md) for more information.

## URL rewrite parameters note {#url-rewrite-params}

>[!IMPORTANT]
>
>In the process of redirection, all GET parameters specified in the URL are removed for security reasons.

## New price rule {#new-price-rule}

>[!NOTE]
>
>Price rules are automatically processed with other system rules. Processing frequency depends on the [cron configuration](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html?lang=zh-Hant). When you create a price rule, allow enough time for it to get into the system. WHen you are sure it is in the system, test the rule.

## Configuration settings {#config}

若要存取商店組態設定，請從&#x200B;_管理員_&#x200B;側邊欄中選擇&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

## UPS API淘汰 {#ups-api}

>[!IMPORTANT]
>
>自2024年6月起，Adobe Commerce商家將無法再透過目前的UPS整合進行交易。 這是因為原生Adobe Commerce整合使用的United Parcel Service (UPS) API目前不支援必要的OAuth 2.0安全性模型。 若要啟用整合，請[在UPS開發人員平台](https://developer.ups.com/get-started)上建立應用程式，以取得OAuth 2.0所需的認證。 在Commerce UPS送貨設定中使用新認證做為`username`和`password`。 若要深入瞭解安全性模式變更，請參閱[開發人員入口網站存取金鑰移轉指南_](https://developer.ups.com/oauth-developer-guide)。<br/>
>
>商家應該[套用品質修補程式更新](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/ups-shipping-method-integration-migration-from-soap-to-restful-api.html?lang=zh-Hant)至其商店，以便從SOAP API移轉至RESTful API （支援OAuth 2.0驗證通訊協定）。


## 可用檔案 {#docs-links}

| 檔案資源 | 說明 |
|----------------------- | ----------- |
| [Adobe Commerce 2.4管理員使用手冊](../landing/home.md) | 在Admin中工作的商戶適用的檔案和資源。 |
| [Adobe Commerce服務檔案](https://experienceleague.adobe.com/docs/commerce/user-guides/home.html?lang=zh-Hant) | 支援銷售服務集合的檔案，可協助商家將其業務的關鍵元件與商店整合。 |
| [雲端基礎結構上的Commerce指南](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/overview.html?lang=zh-Hant) | 在受管理、自動託管式雲端平台上部署Adobe Commerce的逐步程式。 |
| [Adobe Commerce 2.4作業指南](https://experienceleague.adobe.com/docs/commerce-operations/operational-guides/home.html?lang=zh-Hant) | 有關在雲端和內部部署專案上開發、部署及維護Adobe Commerce的概念、流程、工具和最佳實務的系統檔案。 |
| [Adobe Commerce 2.4開發人員檔案](https://developer.adobe.com/commerce/docs) | 以開發人員為中心的檔案，用於自訂Adobe Commerce及與協力廠商系統整合。 |

{style="table-layout:auto"}

## B2B相容性 {#b2b-compatibility}

>[!IMPORTANT]
>
>Adobe Commerce B2B 1.4.2+版相容於PHP 8.2。 如果您將Commerce執行個體升級至2.4.7+版，請確定執行個體使用PHP 8.2版，以保持與Adobe Commerce B2B發行版本的相容性。 此外，B2B 1.4.2+版本不支援[GraphQL應用程式伺服器](https://experienceleague.adobe.com/zh-hant/docs/commerce-operations/performance-best-practices/concepts/application-server)。

## reCAPTCHA表單清單 {#recaptcha-forms-list}

- [!UICONTROL Enable for Customer Login]
- [!UICONTROL Enable for Forgot Password]
- [!UICONTROL Enable for Create New Customer Account]
- [!UICONTROL Enable for Edit Customer Account]
- [!UICONTROL Enable for Create New Company Account] (Available with Adobe Commerce B2B only)
- [!UICONTROL Enable for Contact Us]
- [!UICONTROL Enable for Product Review]
- [!UICONTROL Enable for Newsletter Subscription]
- [!UICONTROL Enable for Gift Card] (Adobe Commerce only)
- [!UICONTROL Enable for Invitation Create Account]
- [!UICONTROL Enable for Send To Friend] - [!BADGE PaaS only]{type=Informative url="https://experienceleague.adobe.com/zh-hant/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案（Adobe管理的PaaS基礎結構）和內部部署專案的Adobe Commerce 。"}
- [!UICONTROL Enable for Checkout/Placing Order]
- [!UICONTROL Enable for Wishlist Sharing]
- [!UICONTROL Enable for Coupon Codes]
- [!UICONTROL Enable for PayPal PayflowPro payment form] - [!BADGE PaaS only]{type=Informative url="https://experienceleague.adobe.com/zh-hant/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案（Adobe管理的PaaS基礎結構）和內部部署專案的Adobe Commerce 。"}
