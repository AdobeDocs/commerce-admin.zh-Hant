---
title: 付款總覽
description: 瞭解Adobe Commerce和Magento Open Source本機支援的付款方法與服務。
exl-id: 474bf6df-96e2-4db3-ad3c-1804b5de33b0
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '647'
ht-degree: 0%

---

# 付款總覽

Adobe Commerce和Magento Open Source支援各種付款方法和服務，讓您能更輕鬆結帳和方便客戶。 此清單包含數種離線付款方式，包括支票或匯票付款，以及貨到付款(COD)。 此外，還有許多線上支付解決方案和閘道的原生整合功能，包括供應商開發的套件式Braintree擴充功能。

>[!TIP]
>
>Adobe Commerce和Magento Open Source的支付服務提供全包式自助服務解決方案，包括沙箱測試和簡單的設定，提供穩定且安全的支付處理作業。 若要深入瞭解此強大的工具集，以及此工具集如何提供您所需的深入分析和控制力，讓購買者獲得最佳體驗，請參閱 [Payment Services使用手冊](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html).

>[!NOTE]
>
>檢閱 [PCI法規遵循指南](../getting-started/compliance-pci.md) 概述支付卡產業(PCI)針對接受透過網際網路以信用卡付款的企業所設定的需求。

## 2.4中的變更

2.4.x版移除了部分付款整合和隨附的擴充功能，並移至Commerce Marketplace。 您可在以下網址找到最新正式的付款整合延伸模組： [Commerce Marketplace](https://marketplace.magento.com/extensions/payments-security.html){：target=&quot;_blank&quot;}。

- **Amazon Pay** 和 **卡拉納**：Adobe Commerce和Magento Open Source版本2.4.0到2.4.3包含這些廠商開發的擴充功能。 從2.4.4版開始，這些擴充功能不再與核心版本搭配，必須從Commerce Marketplace安裝和更新。 此Marketplace也可讓您存取擴充功能開發人員提供的目前檔案。

  如果您已啟用並設定這些隨附的擴充功能之一，則必須在2.4.4升級程式中更新composer.json檔案，並管理以後的擴充功能更新。 另請參閱 [升級模組](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) 在 _升級指南_ 以取得詳細資訊。

- **Worldpay**， **Eway**， **網路來源**、和 **Authorize.Net**：如需從這些付款整合進行安全轉換的詳細資訊，請參閱 [DevBlog](https://community.magento.com/t5/Magento-DevBlog/Deprecation-of-Magento-core-payment-integrations/ba-p/426445){：target=&quot;_blank&quot;}。

## 離線付款方法

Adobe Commerce和Magento Open Source包含多種內建的離線付款方法，不需要協力廠商付款處理公司的服務：

- [零小計簽出](zero-subtotal-checkout.md)
- [貨到付款](cash-on-delivery.md)
- [銀行轉帳付款](bank-transfer.md)
- [支票/匯票](check-money-order.md)
- [採購單](purchase-order.md)
- [分期付款](../b2b/enable-basic-features.md#configure-payment-on-account) ![適用於Adobe Commerce的B2B](../assets/b2b.svg) (適用於Adobe Commerce的B2B提供)

## 線上付款方法

Adobe Commerce和Magento Open Source支援多種支付解決方案，為世界各地的商家提供商業服務。 與將控制權轉移到其他地點以完成交易的付款解決方案不同，付款閘道讓您能夠直接從您的商店接受信用卡付款，而無需客戶離開您的地點。

### 建議的解決方案

- [付款服務](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html)
- [PayPal Express簽出](paypal-express-checkout.md)
- [Braintree](braintree.md)

### 其他PayPal支付解決方案

另請參閱 [PayPal支付解決方案](paypal.md) 以取得PayPal付款方式選項的詳細資訊。

#### 多合一PayPal解決方案

- [PayPal付款進階](paypal-payments-advanced.md)
- [PayPal Payments Pro](paypal-payments-pro.md)
- [PayPal支付標準](paypal-payments-standard.md)

#### PayPal付款閘道

- [PayPal Payflow Pro](paypal-payflow-pro.md)
- [PayPal Payflow連結](paypal-payflow-link.md)

## 欺詐保護

欺詐保護服務和篩選器會在交易處理之前檢查提交的訂單，以偵測欺詐性的訂單，並保護您免於費用退回。 Adobe Commerce和Magento Open Source支援下列防欺詐解決方案：

- [PayPal詐騙管理篩選器](paypal.md#paypal-fraud-management-filters)

- [Marketplace上的防欺詐解決方案][1]

>[!NOTE]
>
>為了支援安全性法規遵循的更新，從2.4.0版開始，已從Commerce中移除欺詐保護。 如果您一直在2.3.x或舊版中使用Signifyd整合，建議您轉換至 [顯著的詐騙和借項衝回保護延伸功能](https://marketplace.magento.com/signifyd-module-connect.html){：target=&quot;_blank&quot;}。 請務必根據供應商指引維護擴充功能的更新。

## 疑難排解資源

如需疑難排解付款問題的說明，請參閱 [支援知識庫](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/overview.html?lang=en).

[1]: https://marketplace.magento.com/catalogsearch/result?q=fraud%20protection
