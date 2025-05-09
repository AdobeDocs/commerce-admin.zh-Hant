---
title: 付款總覽
description: 瞭解Adobe Commerce和Magento Open Source原生支援的支付方法和服務。
exl-id: 474bf6df-96e2-4db3-ad3c-1804b5de33b0
feature: Payments
source-git-commit: 489c72652693a15ffe1c745277bbaa9da084dcba
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---

# 付款總覽

Adobe Commerce和Magento Open Source支援多種支付方法和服務。 這包括數種離線付款方式，包括支票或匯票付款，以及貨到付款(COD)。 此外，還有許多線上支付解決方案和閘道的原生整合功能，包括供應商開發套件式Braintree擴充功能。

>[!TIP]
>
>Adobe Commerce和Magento Open Source的Payment Services提供全包式自助服務解決方案，包括沙箱測試和簡單的設定，以提供穩定且安全的付款處理。 若要進一步瞭解此強大的工具組，以及它如何提供您所需的insight和控制功能，讓您為買家建立最佳體驗，請參閱[付款服務使用手冊](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html)。 這是[Adobe Commerce as a Cloud Service](https://experienceleague.adobe.com/en/docs/commerce/cloud-service/overview)中的預設付款解決方案。

>[!NOTE]
>
>檢閱[PCI法規遵循准則](../getting-started/compliance-pci.md)，其中概述支付卡產業(PCI)針對接受透過網際網路信用卡付款的企業所設定的需求。

## 2.4中的變更

僅[!BADGE 個PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"}

部分支付整合和隨附的擴充功能在2.4.x版中已移除，並移至Commerce Marketplace。 您可以在[Commerce Marketplace](https://marketplace.magento.com/extensions/payments-security.html){:target="_blank"}中找到最新的正式付款整合延伸模組。

- **Amazon Pay**&#x200B;和&#x200B;**Klarna**： Adobe Commerce和Magento Open Source版本2.4.0到2.4.3包含這些廠商開發的擴充功能。 從2.4.4版開始，核心版本不再隨附這些擴充功能，而必須從Commerce Marketplace安裝及更新。 此Marketplace也可讓您存取擴充功能開發人員提供的目前檔案。

  如果您已啟用並設定這些隨附的擴充功能之一，則必須在2.4.4升級程式中更新composer.json檔案，並管理以後的擴充功能更新。 如需詳細資訊，請參閱&#x200B;_升級指南_&#x200B;中的[升級模組](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html)。

- **Worldpay**、**Eway**、**CyberSource**&#x200B;和&#x200B;**Authorize.Net**：如需從這些付款整合進行安全轉換的詳細資訊，請參閱[DevBlog](https://community.magento.com/t5/Magento-DevBlog/Deprecation-of-Magento-core-payment-integrations/ba-p/426445){:target="_blank"}。

## 離線付款方法

Adobe Commerce和Magento Open Source包含數種內建的離線付款方法，這些方法不需要協力廠商付款處理公司的服務：

- [零小計簽出](zero-subtotal-checkout.md)
- [貨到付款](cash-on-delivery.md)
- [銀行轉帳付款](bank-transfer.md)
- [支票/匯票](check-money-order.md)
- [採購單](purchase-order.md)
- [帳戶付款](../b2b/enable-basic-features.md#configure-payment-on-account) ![Adobe Commerce B2B](../assets/b2b.svg) (適用於Adobe Commerce B2B)

## 線上付款方法

Adobe Commerce和Magento Open Source支援多種支付解決方案，為世界各地的商家提供商業服務。 與將控制權轉移到其他地點以完成交易的付款解決方案不同，付款閘道讓您能夠直接從您的商店接受信用卡付款，而無需客戶離開您的地點。

### 建議的解決方案

- [付款服務](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html)
- 僅[!BADGE PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"} [PayPal Express簽出](paypal-express-checkout.md)
- 僅[!BADGE PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"} [Braintree](braintree.md)

### 其他PayPal支付解決方案

僅[!BADGE 個PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"}

請參閱[PayPal付款解決方案](paypal.md)，以取得有關PayPal付款方式選項的詳細資訊。

#### 多合一PayPal解決方案

僅[!BADGE 個PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"}

- [PayPal付款進階](paypal-payments-advanced.md)
- [PayPal Payments Pro](paypal-payments-pro.md)
- [PayPal支付標準](paypal-payments-standard.md)

#### PayPal付款閘道

僅[!BADGE 個PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"}

- [PayPal Payflow Pro](paypal-payflow-pro.md)
- [PayPal Payflow連結](paypal-payflow-link.md)

## 欺詐保護

僅[!BADGE 個PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"}

欺詐保護服務和篩選器會在交易處理之前檢查提交的訂單，以偵測欺詐性的訂單，並保護您免於費用退回。 Adobe Commerce和Magento Open Source支援下列防欺詐解決方案：

- [PayPal詐騙管理篩選器](paypal.md#paypal-fraud-management-filters)

- [市集上的詐騙保護解決方案][1]

>[!NOTE]
>
>為了支援安全性法規遵循的更新，從2.4.0版開始，Commerce已移除詐騙防護功能。 如果您已在2.3.x或舊版中使用Signifyd整合，建議您改用[Signifyd Fraud &amp; Chargeback Protection擴充功能](https://marketplace.magento.com/signifyd-module-connect.html){:target="_blank"}。 請務必根據供應商指引維護擴充功能的更新。

## 疑難排解資源

僅[!BADGE 個PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"}

如需疑難排解付款問題的說明，請參閱[支援知識庫](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/overview.html?lang=en)。

[1]: https://marketplace.magento.com/catalogsearch/result?q=fraud%20protection
