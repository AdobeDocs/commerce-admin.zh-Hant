---
title: 啟動前檢查清單
description: 使用此清單來檢查所需的組態設定，以在您的商店投入生產之前確定所有專案都正確無誤。
exl-id: 649809c2-7217-4274-b365-c682bfff24ba
feature: Site Management, System
role: Admin, Leader
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 0%

---

# 啟動前檢查清單

在您完成商店的設計、開發和測試後，請檢查下列組態設定，以確保在商店&#x200B;_上線之前，一切都是正確的_。 如需每個組態設定的完整說明，請參閱&#x200B;[_組態參考_](../configuration-reference/guide-overview.md)。

## 一般設定

- [商店URL](../stores-purchase/store-urls.md) — 確認店面和管理員的商店URL對即時生產環境而言是正確的。
- 安全性憑證 — 在啟動存放區之前，請為基底URL中指定的網域安裝100%已簽署和信任的安全性憑證。
- [商店電子郵件地址](../getting-started/store-details.md#store-email-addresses) — 完成用於傳送及接收電子郵件通知的所有電子郵件地址，例如新訂單、發票、出貨、銷退折讓單、產品價格警示及電子報。 請確定每個欄位都包含有效的企業電子郵件地址。

## 行銷設定

- [電子郵件範本](../systems/email-templates.md) — 更新預設電子郵件範本以反映您的品牌。 如果您建立範本，請務必更新設定。
- [銷售通訊](../stores-purchase/introduction.md#order-management-and-operations) — 請確定您的發票和包裝單包含正確的商業資訊，並反映您的品牌。
- [Google Tools](../merchandising-promotions/google-tools.md) - [!DNL Commerce]提供與Google API的整合，讓您的企業可以使用Google Analytics和Google AdWords。

## 銷售設定

- [購物車選項](../stores-purchase/cart-configuration.md) — 檢視購物車組態設定，檢視是否有任何您想要變更的專案，例如設定購物車中價格的最小訂購量和存留期。
- [簽出選項](../stores-purchase/checkout-process.md#checkout-options) — 檢視簽出選項，檢視是否有任何您想要變更的專案，例如設定條款與條件，以及設定來賓簽出。
- [稅捐](../stores-purchase/taxes.md) — 請確定稅捐已根據您的企業稅捐規則與當地要求正確設定。
- [傳遞方法](../stores-purchase/delivery.md) — 啟用公司使用的所有電信業者和傳遞方法。
- [PayPal](../stores-purchase/paypal.md) — 如果您打算為客戶提供使用PayPal付款的便利，請開啟PayPal商家帳戶，並設定付款方式。 在存放區上線之前，以沙箱模式執行一些測試交易。
- [付款方法](../stores-purchase/payments.md) — 啟用您計畫使用的付款方法，並確定已正確設定這些方法。 檢查訂單狀態設定、接受的貨幣、允許的國家/地區等。

## 系統設定

[Cron （排程工作）](../systems/cron.md) - Cron工作用於處理電子郵件、目錄價格規則、電子報、客戶警示、Google Sitemap、更新匯率等。 請確定Cron工作設定為在適當的時間間隔（分鐘）執行。
