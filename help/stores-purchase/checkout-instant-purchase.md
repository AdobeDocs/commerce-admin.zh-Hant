---
title: 立即購買
description: 瞭解立即購買功能，以及它如何提供註冊客戶帳戶的快速結帳。
exl-id: f299f364-d7e3-4567-8c7b-955129011a19
feature: Checkout
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---

# 立即購買

_即時購買_&#x200B;可讓客戶使用儲存在帳戶中的資訊，加速結帳程式。 啟用時，_立即購買_&#x200B;按鈕會顯示在產品頁面上&#x200B;_加入購物車_&#x200B;按鈕下方，供符合需求的客戶使用。

![顯示[立即購買]選項的產品頁面](./assets/storefront-checkout-instant-purchase.png){width="700" zoomable="yes"}

## 客戶需求

- 客戶已[登入](../customers/customer-sign-in.md)其帳戶。

- 客戶帳戶有[預設帳單和送貨地址](../customers/account-dashboard-address-book.md)。

- 在預設送貨地址中指定的國家/地區至少有一個[送貨方法](delivery.md)可供使用。

- 客戶帳戶有已啟用儲存庫的[儲存付款](../stores-purchase/stored-payment-methods.md)方法。

  下列付款方式可用於提供對已儲存信用卡資訊的安全存取：

   - [Braintree信用卡](braintree.md) (若啟用3D Secure，即刻購買無法與Braintree信用卡搭配使用。)
   - [已啟用PayPal的Braintree](braintree.md)
   - [PayPal Payflow Pro](paypal-payflow-pro.md)

## 在店面立即購買

1. 在店面，客戶前往要購買專案的產品頁面。

1. 選取必要的選項並按一下&#x200B;**[!UICONTROL Instant Purchase]**。

   ![確認對話方塊以確認立即購買](./assets/storefront-checkout-instant-purchase-confirmation.png){width="500" zoomable="yes"}

1. 檢閱&#x200B;**[!UICONTROL Instant Purchase Confirmation]**&#x200B;資訊並按一下&#x200B;**[!UICONTROL OK]**&#x200B;以完成交易。

   產品頁面頂端會顯示確認訊息和訂單編號。

## 設定立即購買

### 步驟1：開啟設定頁面

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

### 步驟2：設定付款方式儲存庫

您可以搭配Braintree使用立即購買，或使用Adobe Commerce和Magento Open Source的支付服務。 必須啟用儲存庫，購物者才能使用「立即購買」功能。

瞭解如何設定Braintree或付款服務的付款方式及啟用儲存機制：

- [Braintree](braintree.md)
- [付款服務檔案](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html)

### 步驟3：啟用立即購買

1. 在左側面板的&#x200B;_[!UICONTROL Sales]_&#x200B;區段下，選擇&#x200B;**[!UICONTROL Sales]**。

1. 展開&#x200B;**[!UICONTROL Instant Purchase]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

1. 如果這個變更是針對特定商店檢視，請[選擇套用組態的商店檢視](../configuration-reference/scope-change.md#set-the-scope)。

   出現提示時，按一下&#x200B;**[!UICONTROL OK]**&#x200B;以繼續。

1. 將&#x200B;**[!UICONTROL Enabled]**&#x200B;設為`Yes`。

1. 輸入您要在按鈕上顯示的&#x200B;**[!UICONTROL Button Text]**。

   可針對每個商店檢視變更按鈕文字，或變更語言。 依預設，按鈕文字為`Instant Purchase`。

   ![設定 — 立即購買選項](../configuration-reference/sales/assets/sales-instant-purchase.png){width="600" zoomable="yes"}

   如需這些組態設定的詳細說明，請參閱&#x200B;_組態參考指南_&#x200B;中的[立即購買](../configuration-reference/sales/sales.md#instant-purchase)。

1. 按一下&#x200B;**[!UICONTROL Save Config]**。

1. 當提示更新快取時，按一下系統訊息中的&#x200B;**[!UICONTROL Cache Management]**，然後依照指示排清快取。
