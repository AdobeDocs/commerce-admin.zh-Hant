---
title: 商店和購買體驗簡介
description: 瞭解用於建構和管理您的線上商店的功能，以及客戶的購買體驗。
exl-id: 7ced9cbc-49b4-48f7-aae2-fcb48fdb888f
source-git-commit: a56509eeedbb30a1e9cacfd521ea4c18e0241d94
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 0%

---

# 商店和購買體驗簡介

Adobe Commerce和Magento Open Source提供全方位的功能，可建構和管理您的線上商店和客戶的購買體驗。 在您的Commerce執行個體中，您可以管理網站、商店和檢視的商店階層。 您也可以針對多重地區設定執行商店所需的稅捐與幣別匯率，包括產品與客戶群組的稅捐類別。

## 存放區結構

Adobe Commerce或Magento Open Source的單一例項可支援使用不同屬性和內容的多個網站、商店或商店檢視。 常見的案例是在不同網域中設定具有不同選項的商店。 例如，您可能想要一個網域上的一組類別和產品，以及不同網域上另一組類別和產品使用另一種語言。 商家可以在「管理員」中設定網站、商店和商店檢視。

當 [階層](stores.md) 已定義，您可以根據以下專案套用組態設定： [範圍](../getting-started/websites-stores-views.md#scope-settings) 因此每個網站、商店和商店檢視都會提供您想要的產品目錄和店面體驗。

## 購買點

Adobe Commerce和Magento Open Source在提交訂單前，會自動驗證所有料號的SKU和可用性，以減少訂購錯誤。 您可以設定 [購物車](cart.md) 和 [簽出選項](checkout-process.md) 提供最佳的購買體驗，從交易到傳遞。 已登入帳戶的客戶可以快速完成結帳，因為許多資訊已存在於其帳戶中。 此 _簽出_ 頁面會引導客戶完成訂單異動的每個處理步驟。 若您啟用 [立即購買](checkout-instant-purchase.md)，客戶可使用儲存在其帳戶中的資訊來加速結帳程式。

>[!TIP]
>
>![適用於Adobe Commerce的B2B](../assets/b2b.svg) 安裝及啟用Adobe Commerce適用的B2B後，您可以設定 _快速訂購_ 適用於與公司帳戶相關聯的客戶。 當客戶知道要訂購產品的名稱或SKU時，此函式會將訂購流程簡化為幾次點按。 您也可以為公司帳戶設定可轉讓報價的支援。 如需B2B功能的詳細資訊，請參閱 [Adobe Commerce適用的B2B使用指南](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).

## 購物協助

客戶有時需要協助才能完成購買。 有些客戶喜歡線上購物，但偏好透過電話訂購。 已向您商店註冊帳戶的訪客和客戶均可提供即時協助。

- [管理購物車](shopping-assisted-cart-manage.md)
- [建立訂單](customer-account-create-order.md) 適用於註冊客戶
- [更新訂單](order-update.md)

![購物車](./assets/storefront-cart-price-group-discount.png){width="700" zoomable="yes"}

觀看此影片，瞭解賣家輔助購物：

>[!VIDEO](https://video.tv.adobe.com/v/343662/?quality=12)

## 訂單管理與作業

在「管理員」中，商戶可存取訂單工作流程與處理訂單各階段的資訊：

- 此 [訂購](orders.md) 頁面為商家提供可輕鬆存取的所有目前訂單清單，並包含工具來編輯及處理現有訂單，以及代表客戶建立訂單。

- 此 [發票](invoices.md) 頁面清單商業發票是以臨時銷售訂單為基礎，並提供訂單的永久記錄。

- 此 [出貨](shipments.md) 頁面列出每張準備出貨的商業發票的出貨記錄。

- 此 [銷退折讓單](credit-memos.md) 頁面可讓商家處理及管理銷退折讓單，這是顯示缺客戶金額的檔案。 金額可用於購買或退款給客戶。

- ![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce) [傳回](returns.md) 頁面列出目前退回的商品請求(RMA)，並用來輸入新的退回請求。

- 此 [交易](transactions.md) 頁面會列出您的商店與付款系統之間發生的所有付款活動，並提供更詳細資訊的存取權。

## 送貨與傳遞

研究表明，商店為客戶提供數種選擇 [傳遞方法](delivery.md) 比使用單一方法的存放區具有更高的轉換率。 「管理員」提供多種工具，商家可透過這些工具設定多種傳遞方式與 [出貨承運商](carriers.md)，並列印 [送貨標籤](shipping-labels.md).
