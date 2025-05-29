---
title: Adobe的擴充功能
description: 檢閱Adobe所發行Adobe Commerce和Magento Open Source擴充功能的相關資訊。
exl-id: 86338edc-c32a-41c8-9594-6aec26f53ac6
feature: Extensions
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"
source-git-commit: 77e7eb00e9f8d5af6361059c287707993180c4c4
workflow-type: tm+mt
source-wordcount: '1357'
ht-degree: 0%

---

# Adobe的擴充功能

本主題提供Adobe所發行Adobe Commerce和Magento Open Source的PHP擴充功能相關資訊。

擴充功能新增功能、功能、服務及整合至Admin和Storefront。 其中有些擴充功能是透過Magento Open Source社群的貢獻所開發。 有些擴充功能會依預設安裝，有些則需要個別安裝。

+++進一步瞭解擴充Adobe Commerce

Adobe提供兩種主要方法來擴充或自訂Adobe Commerce專案：

- 處理中的擴充功能：使用在Adobe Commerce應用程式處理序中執行的自訂程式碼和擴充功能，例如PHP擴充功能。 這種傳統方法允許深度整合，但在升級期間需要謹慎管理。

- 程式外擴充功能：使用獨立於核心軟體的自訂程式碼和應用程式。 此現代方法有助於降低總體擁有成本，方法如下：

   - 由於擴充功能與核心是分離的，因此可簡化升級
   - 讓開發人員更能掌控實作時機和方法
   - 啟用擴充功能元件的獨立縮放與維護

Adobe Commerce提供策略與工具，可支援兩種型別的擴充性。 若要深入瞭解，請參閱[Adobe Commerce擴充性](https://developer.adobe.com/commerce/extensibility/)。

+++

## 預設情況下安裝的Adobe擴充功能

Adobe Commerce隨附下列Adobe擴充功能，並自動透過Adobe Commerce應用程式進行安裝。 如擴充功能說明所述，部分擴充功能需要在Admin中進一步設定或啟用。

### [!DNL Inventory Management]

[!DNL Commerce] [[!DNL Inventory Management]](../inventory-management/introduction.md)透過並行結帳保護和出貨比對演演算法，在一或多個地點和銷售管道提供增強的存貨和出貨管理。 追蹤存貨數量、提供精確的可銷售存貨數量給客戶，並根據建議或手動選擇出貨以控制整個存貨。 針對每個來源和每個產品進行全域管理設定。

>[!NOTE]
>
>此擴充功能是透過Community Engineering Program開發為[[!DNL Inventory Management]](https://github.com/magento/inventory) （原為MSI）專案的一部分。

[!DNL Inventory Management]安裝，預設會啟用所有功能。 啟用這些詳細目錄功能不需要額外的步驟。 如需[!DNL Inventory Management]功能的詳細資訊，請參閱[[!DNL Inventory Management] 使用手冊](../inventory-management/guide-overview.md)。

### Braintree

PayPal與Gene Commerce共同開發適用於Commerce 2.4.x商店的官方Braintree擴充功能。 此更新包含的PayLater選項，可於購物和結帳期間自動向消費者顯示相關的PayLater訊息和按鈕，提供改良的結帳體驗，旨在促進轉換。

此擴充功能預設為已安裝，但需要[Braintree帳戶](https://www.braintreepayments.com/)以及Admin中的設定，才能為您的商店啟用。 若要確定使用Braintree處理交易時適用的費用，請檢查[Braintree定價](https://www.braintreepayments.com/braintree-pricing)。

如需Admin中Braintree設定的相關資訊，請參閱&#x200B;_銷售和購買體驗指南_&#x200B;中的[Braintree](../stores-purchase/braintree.md)主題。

### Google reCAPTCHA

Google reCAPTCHA提供的店面和管理員UI的安全性比標準CAPTCHA更高，並讓您能夠：

- 驗證客戶何時建立帳戶、擷取密碼、登入帳戶或連絡您的公司。
- 增強管理員使用者登入時的安全性。

它減少了輸入驗證碼時潛在的使用者錯誤，並鼓勵在結帳期間在不增加障礙的情況下轉換購物車。 [使用隱藏或互動式檢查來啟用及設定reCAPTCHA](../systems/security-google-recaptcha.md)，以加強對[!DNL Commerce]管理員和店面的安全存取。

### 雙因素驗證

[!DNL Commerce]管理員提供您商店、訂單和客戶資料的所有存取權。 [雙因素驗證](../systems/security-two-factor-authentication.md) （2FA或TFA）除了標準登入名稱與密碼之外，還需要其他驗證，才能從所有裝置存取[!DNL Commerce] Admin，藉以改善安全性。 擴充功能支援多個驗證器，包括Google Authenticator、Authy、[!DNL Duo]和U2F金鑰。 此驗證僅適用於Admin使用者。 店面客戶帳戶無法使用此功能。

預設會啟用這些功能。 每位管理員使用者都必須安裝並設定其中一個支援的驗證者。

>[!NOTE]
>
>為管理員啟用Adobe Identity Management Services (IMS)驗證的Adobe Commerce商店已停用原生Commerce 2FA。 使用其Adobe憑證登入管理員的使用者，不需要為許多管理員工作重新驗證。 當管理員使用者登入目前的工作階段時，驗證會由Adobe IMS處理。 請參閱[Adobe Identity Management Service (IMS)整合總覽](./adobe-ims-integration-overview.md)。

## 需要安裝的Adobe擴充功能

Adobe提供其他擴充功能，必須使用Composer個別安裝。 這些擴充功能可透過不同管道使用：

- 存放庫存取權(repo.magento.com)

  下列擴充功能需要帳戶布建和認證才能安裝。 請聯絡您的Adobe客戶代表以尋求協助。

   - [Adobe Commerce B2B](#adobe-commerce-b2b)
   - [適用於Commerce的AEM Assets整合](#assets-integration-for-commerce)

- Adobe Commerce Marketplace

  下列Adobe擴充功能可在[marketplace.magento.com](https://marketplace.magento.com)公開存取。 這些擴充功能不需額外付費。

   - [即時搜尋](#live-search)
   - [產品推薦](#product-recommendations)
   - [目錄服務](#catalog-service)
   - [付款服務](#payment-services)

### [!DNL Adobe Commerce B2B]

![僅限Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce，需要單獨的授權。

[!DNL Adobe Commerce B2B]是整合式擴充功能，可將標準Commerce商店轉換為全方位的企業對企業平台。 它可讓公司管理複雜的組織結構，在統一的公司帳戶下擁有多個購買者、自訂角色和購買許可權。 主要功能包括特定公司的目錄與定價、可協商的報價、採購單管理、請購單清單，以及快速訂購功能。 此解決方案在單一執行個體上同時支援B2B和B2C模型，可因應各種業務需求而具備彈性。 此擴充功能需要獨立的授權，且與Adobe Commerce的核心功能緊密整合，以提供完整的B2B電子商務解決方案。

如需布建的相關資訊，請聯絡您的Adobe客戶代表。 如需實作詳細資料和設定步驟，請參閱[[!DNL B2B for Adobe Commerce] 使用手冊](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html)。

### [!DNL AEM Assets Integration for Commerce]

![僅限Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce，也需要Adobe Experience Manager (AEM) Assets和AEM Dynamic Media的授權。

[!DNL AEM Assets Integration for Commerce]已將Adobe Commerce與Adobe Experience Manager的數位資產管理(DAM)系統連線，以集中控制所有數位資產。 此整合可跨商務存放區啟用自動資產同步、即時更新和有效的內容重複使用。 結合AEM強大的資產管理功能與Commerce，企業可透過雲端架構的基礎架構獲益於簡化的工作流程、一致的品牌體驗及最佳化的媒體交付。

如需布建的相關資訊，請聯絡您的Adobe客戶代表。 如需實作詳細資料和設定步驟，請參閱[[!DNL Assets Integration] 使用手冊](../content-design/aem-assets-integration.md)。

### [!DNL Live Search]

![Adobe Commerce](../assets/adobe-logo.svg)僅限Adobe Commerce

Live Search是Adobe Commerce的獨家功能，提供AI支援的搜尋解決方案，並具有即時「隨型別搜尋」功能。 它可以在購物者輸入商品時，透過產品縮圖提供快速的相關結果，並具備智慧型多面向功能，可依據購物行為自動調整篩選器。 此解決方案包括用於產品提升與掩藏、同義字管理和搜尋分析的銷售功能。 [!DNL Live Search]免費隨附於Adobe Commerce，以更複雜的SaaS式搜尋體驗取代預設的搜尋功能。 它需要最少的設定才能開始。

如需實作詳細資料和技術需求，請參閱[即時搜尋使用手冊](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html)。

### [!DNL Product Recommendations]

![Adobe Commerce](../assets/adobe-logo.svg)僅限Adobe Commerce

[!DNL Product Recommendations]是Adobe Commerce專屬功能，由Adobe Sensei AI技術支援，可在整個客戶購物歷程中提供個人化產品建議。 解決方案會即時分析購物者行為和產品關係，以自動產生相關建議，不需要手動銷售規則。 此AI導向方法有助於提高轉換率和收入潛力，同時為購物者打造更吸引人的產品探索體驗。

如需實作詳細資料和最佳實務，請參閱[[!DNL Product Recommendations] 使用手冊](https://experienceleague.adobe.com/docs/commerce/product-recommendations/overview.html)。

### [!DNL Catalog Service]

[!BADGE 支援]{type=Informative tooltip="支援"} Adobe Commerce和Magento Open Source安裝

[!DNL Catalog Service]是適用於Adobe Commerce和Magento Open Source的高效能解決方案，可讓您透過GraphQL端點以最佳化方式存取目錄資料。 它維護獨立的同步資料庫，內含產品詳細資料和相關資訊，略過直接應用程式通訊，提供更快速的頁面載入時間。 此服務對產品詳細資料頁面、類別清單和搜尋結果頁面尤其有用，因此非常適合用於傳統和Headless商務實施。

如需設定指示與技術詳細資訊，請參閱[[!DNL Catalog Service] 使用手冊](https://experienceleague.adobe.com/docs/commerce/catalog-service/guide-overview.html)。

>[!NOTE]
>
>啟用「即時搜尋」或「產品建議」時，目錄服務會自動安裝。 不需要手動安裝。

### [!DNL Payment Services]

[!BADGE 支援]{type=Informative tooltip="支援"} Adobe Commerce和Magento Open Source安裝

[!DNL Payment Services]是適用於Adobe Commerce和Magento Open Source商店的全包式支付解決方案，提供完整的支付處理功能。 此服務整合了安全支付閘道功能與內建的詐騙保護功能，同時提供多種支付選項，包括信用卡/借記卡、PayPal、Venmo (US)和PayLater計畫。 它透過Commerce管理介面提供統一的交易報告及訂單管理，讓商家可以輕鬆地在一個地方追蹤付款、管理現金流量及調節財務資料。

如需詳細的設定步驟與付款選項，請參閱[[!DNL Payment Services] 使用手冊](https://experienceleague.adobe.com/en/docs/commerce/payment-services/overview)。
