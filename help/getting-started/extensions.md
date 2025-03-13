---
title: Adobe的擴充功能
description: 檢閱Adobe所發行Adobe Commerce和Magento Open Source擴充功能的相關資訊。
exl-id: 86338edc-c32a-41c8-9594-6aec26f53ac6
feature: Extensions
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '950'
ht-degree: 0%

---

# Adobe的擴充功能

本主題提供Adobe所發行Adobe Commerce和Magento Open Source擴充功能的相關資訊。 擴充功能新增功能、功能、服務及整合至Admin和Storefront。 其中有些擴充功能是透過Magento Open Source社群的貢獻所開發。 有些擴充功能需要個別安裝，有些則預設會安裝。

## 已安裝的擴充功能

有些擴充功能會自動與Adobe Commerce或Magento Open Source一起安裝。

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

## 要新增的擴充功能

[[!DNL Commerce Marketplace]](https://marketplace.magento.com/)是應用程式與服務的全域電子商務資源，這些應用程式與服務會以強大的新功能擴充[!DNL Commerce]解決方案。 Adobe透過[!DNL Marketplace]發行數個擴充功能，這些擴充功能可在Adobe Commerce或Magento Open Source存放區中安裝及設定，以提供增強的整合與功能。

### [!DNL Live Search]

![Adobe Commerce](../assets/adobe-logo.svg)僅限Adobe Commerce

[!DNL Live Search]擴充功能會將您的商店連線至Live Search服務，這是Adobe Commerce的免費搜尋平台，可順暢地讓賣家為客戶提供增強了AI的搜尋體驗。 Intelligent Faceting是以Adobe的人工智慧Adobe Sensei所打造，可移除多面向/篩選的手動工作，協助商戶事半功倍。

如需詳細資訊，請參閱[即時搜尋使用手冊](https://experienceleague.adobe.com/docs/commerce/live-search/guide-overview.html)。

### [!DNL Product Recommendations]

![Adobe Commerce](../assets/adobe-logo.svg)僅限Adobe Commerce

[!DNL Product Recommendations]擴充功能會將您的商店連線至Product Recommendations服務，這是一個強大的行銷工具，可用來增加轉換、收入和參與。 [!DNL Product Recommendations]是由Adobe Commerce所建置，並受其經過戰鬥測試的人工智慧Adobe Sensei所驅動，因此您可以放心地促進參與和轉換。 此功能移除向每位購物者提出相關產品建議所需的手動工作。

如需詳細資訊，請參閱[[!DNL Product Recommendations] 使用手冊](https://experienceleague.adobe.com/docs/commerce/product-recommendations/guide-overview.html?lang=en)。

### [!DNL Catalog Service]

[!DNL Catalog Service]可讓您為客戶提供最佳化的產品體驗，同時提升效能、改善擴充能力及提高轉換率。 如需詳細資訊，請參閱[[!DNL Catalog Service] 使用手冊](https://experienceleague.adobe.com/docs/commerce/catalog-service/guide-overview.html)。

### [!DNL Payment Services]

Adobe Commerce和Magento Open Source的[!DNL Payment services]是完全整合的支付解決方案，可簡化管理付款的程式，並為客戶提供付款的機會。 在Adobe Commerce管理員內安全地調解所有付款和交易資料 — 允許您在一個地方管理訂單和付款，同時提供順暢的結帳。 如需詳細資訊，請參閱[[!DNL Payment Services] 使用手冊](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html)。

### [!DNL Store Fulfillment]

適用於Adobe Commerce和Magento Open Source的Store Fulfillment提供優異的線上購買、到店取貨(BOPIS)客戶體驗，並透過行動裝置提供完整的履行工作流程，讓員工的工作效率最大化。 如需詳細資訊，請參閱[[!DNL Store Fulfillment] 使用手冊](https://experienceleague.adobe.com/docs/commerce/store-fulfillment/guide-overview.html)。

### [!DNL Amazon Sales Channel]

適用於Adobe Commerce的[!DNL Amazon Sales Channel]可讓您將您的Amazon賣方中心清單資料庫與[!DNL Commerce]產品目錄整合，並在Commerce管理員中管理您的Amazon清單和銷售。 如需詳細資訊，請參閱[[!DNL Amazon Sales] 使用手冊](https://experienceleague.adobe.com/docs/commerce-channels/amazon/guide-overview.html)。

### [!DNL Channel Manager]

[!DNL Channel Manager]可讓您將Adobe Commerce或Magento Open Source產品目錄與Walmart Marketplace整合，以增加銷售量、觸及新客戶、簡化營運並節省時間。 安裝並設定擴充功能後，您的員工可以從[!DNL Commerce Admin]順利管理Walmart Marketplace的清單、存貨、訂單、退貨及退款。 如需詳細資訊，請參閱[[!DNL Channel Manager] 使用手冊](https://experienceleague.adobe.com/docs/commerce-channels/channel-manager/guide-overview.html)。
