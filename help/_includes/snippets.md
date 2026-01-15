---
title: 代碼片段
description: 重複使用附註和視覺元素，以記下套用至特定版本的功能或頁面
source-git-commit: 37013190b0ddfff6c70aeb5bc7ba1693959c01d1
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 0%

---

# 代碼片段

## 僅供檢視的功能 {#ee-feature}

<table style="border:1px solid red">
<tr><td><img alt="Adobe Commerce功能" src="../assets/adobe-logo.svg" width="20" height="20" /> 只有Adobe Commerce才有專屬功能（<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">深入瞭解</a>）</td></tr>
</table>

## 僅限B2B功能 {#b2b-feature}

<table style="border:1px solid green">
<tr><td><img alt="Adobe Commerce B2B功能" src="../assets/b2b.svg" width="20" height="20" /> 只有<a href="https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html">Adobe Commerce B2B</a>才提供專屬功能</td></tr>
</table>

## 僅限CE的功能 {#ce-feature}

<table style="border:1px solid orange">
<tr><td><img alt="Magento Open Source功能" src="../assets/open-source.svg" width="20" height="20" /> Magento Open Source需要替代方法（<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">深入瞭解</a>）</td></tr>
</table>

## IMS管理驗證注意事項 {#ims-admin-note}

>[!NOTE]
>
>擁有Adobe ID且想要簡化登入Adobe Commerce和Adobe業務產品的Adobe Commerce商戶可整合Commerce管理員驗證與Adobe IMS驗證工作流程。 為您的Commerce商店啟用此整合後，每個管理員使用者都必須使用其Adobe憑證(而非其Commerce帳戶憑證)才能登入。 請參閱[整合Adobe Commerce與Adobe IMS概述](/help/getting-started/adobe-ims-integration-overview.md)。

## GTag API注意事項 {#gtag-api-note}

>[!NOTE]
>
>自2.4.5版開始，Google服務整合已更新，以支援使用GTag API。 GTag是整合網頁之Google功能的統一機制，可支援透過Google服務追蹤及管理內容的最新功能與機會。

## URL重寫自動略過備註 {#url-rewrite-skip}

>[!NOTE]
>
>當啟用自動重新導向且儲存類別時，所有產品和類別重寫都會即時產生，並依預設儲存在重寫表格中。 此程式可能會導致許多指派產品的類別出現重大效能問題。 解決方案是變更此預設值，並跳過產生類別/產品URL重寫產品以儲存類別。 在這種情況下，只會針對標準產品URL產生產品重寫。 如需詳細資訊，請參閱[自動產品重新導向](/help/merchandising-promotions/url-redirect-product-automatic.md)。

## URL重寫引數注意 {#url-rewrite-params}

>[!IMPORTANT]
>
>在重新導向的過程中，基於安全考量，會移除URL中指定的所有GET引數。

## 新價格規則 {#new-price-rule}

>[!NOTE]
>
>價格規則會與其他系統規則一起自動處理。 處理頻率取決於[cron組態](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html)。 建立價格規則時，請留出足夠的時間讓價格規則進入系統。 確定已在系統中後，請測試規則。

## 組態設定 {#config}

若要存取商店組態設定，請從&#x200B;**[!UICONTROL Stores]**&#x200B;管理員&#x200B;_[!UICONTROL Settings]_&#x200B;側邊欄中選擇&#x200B;**[!UICONTROL Configuration]**>_ > _。

## UPS API淘汰 {#ups-api}

>[!IMPORTANT]
>
>自2024年6月起，Adobe Commerce商家將無法再透過目前的UPS整合進行交易。 這是因為原生Adobe Commerce整合使用的United Parcel Service (UPS) API目前不支援必要的OAuth 2.0安全性模型。 若要啟用整合，請[在UPS開發人員平台](https://developer.ups.com/get-started)上建立應用程式，以取得OAuth 2.0所需的認證。在Commerce UPS送貨設定中將新認證用作`username`和`password`。 若要深入瞭解安全性模式變更，請參閱[開發人員入口網站存取金鑰移轉指南_](https://developer.ups.com/oauth-developer-guide)。<br/>
>
>商家應該[套用品質修補程式更新](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/ups-shipping-method-integration-migration-from-soap-to-restful-api.html)至其商店，以便從SOAP API移轉至RESTful API （支援OAuth 2.0驗證通訊協定）。


## 可用檔案 {#docs-links}

| 檔案資源 | 說明 |
|----------------------- | ----------- |
| [Adobe Commerce 2.4管理員使用手冊](../landing/home.md) | 在Admin中工作的商戶適用的檔案和資源。 |
| [Adobe Commerce服務檔案](https://experienceleague.adobe.com/docs/commerce/user-guides/home.html) | 支援銷售服務集合的檔案，可協助商家將其業務的關鍵元件與商店整合。 |
| [雲端基礎結構上的Commerce指南](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/overview.html) | 在受管理、自動託管式雲端平台上部署Adobe Commerce的逐步程式。 |
| [Adobe Commerce 2.4作業指南](https://experienceleague.adobe.com/docs/commerce-operations/operational-guides/home.html) | 有關在雲端和內部部署專案上開發、部署及維護Adobe Commerce的概念、流程、工具和最佳實務的系統檔案。 |
| [Adobe Commerce 2.4開發人員檔案](https://developer.adobe.com/commerce/docs) | 以開發人員為中心的檔案，用於自訂Adobe Commerce及與協力廠商系統整合。 |

{style="table-layout:auto"}

## B2B相容性 {#b2b-compatibility}

>[!IMPORTANT]
>
>Adobe Commerce B2B 1.4.2+版相容於PHP 8.2。如果您將Commerce執行個體升級至2.4.7+版，請確定執行個體使用PHP 8.2版，以保持與Adobe Commerce B2B發行版本的相容性。 此外，B2B 1.4.2+版本不支援[GraphQL應用程式伺服器](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/concepts/application-server)。

## reCAPTCHA表單清單 {#recaptcha-forms-list}

- [!UICONTROL Enable for Customer Login]
- [!UICONTROL Enable for Forgot Password]
- [!UICONTROL Enable for Create New Customer Account]
- [!UICONTROL Enable for Edit Customer Account]
- [!UICONTROL Enable for Create New Company Account] (僅適用於Adobe Commerce B2B)
- [!UICONTROL Enable for Contact Us]
- [!UICONTROL Enable for Product Review]
- [!UICONTROL Enable for Newsletter Subscription]
- [!UICONTROL Enable for Gift Card] (僅限Adobe Commerce)
- [!UICONTROL Enable for Invitation Create Account]
- [!UICONTROL Enable for Send To Friend] — 僅[!BADGE 個PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"}
- [!UICONTROL Enable for Checkout/Placing Order]
- [!UICONTROL Enable for Wishlist Sharing]
- [!UICONTROL Enable for Coupon Codes]
- [!UICONTROL Enable for PayPal PayflowPro payment form] — 僅[!BADGE 個PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"}
