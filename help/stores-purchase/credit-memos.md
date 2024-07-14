---
title: 銷退折讓單
description: 瞭解銷退折讓單，以及如何使用銷退折讓單發出部分或全部退款。
exl-id: dc2faf86-0182-4661-9543-bc6e00e06dbf
feature: Orders, Invoices, Returns
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 0%

---

# 銷退折讓單

_銷退折讓單_&#x200B;是一份檔案，會顯示客戶應支付的全部或部分退款金額。 金額可用於購買或退款給客戶。 您可以列印單一訂單的銷退折讓單，或將多個訂單的銷退折讓單列印成批次。 必須先為訂單產生銷退折讓單，才能列印銷退折讓單。 _銷退折讓單_&#x200B;頁面列出已核發給客戶的銷退折讓單。

![銷退折讓單](./assets/credit-memos.png){width="700" zoomable="yes"}

## 退款方法

訂單的[付款方式](payments.md)在一定程度上決定您退款訂單的方式。

您可以用三種方式退款：

- 帳戶銷退折讓 — 使用銷退折讓帳戶支付的訂單可以退款為帳戶銷退折讓：
   - ![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce) [商店點數](../customers/store-credit-using.md)
   - ![Adobe Commerce B2B](../assets/b2b.svg) (可與Adobe Commerce B2B搭配使用) [帳戶付款](../b2b/enable-basic-features.md#configure-payment-on-account) （離線方法）
   - ![Adobe Commerce B2B](../assets/b2b.svg) (可與Adobe Commerce B2B搭配使用) [公司點數](../b2b/credit-company.md)
- [線上退款](payments.md#online-payment-methods) — 信用卡透過付款閘道(例如PayPal或Braintree)支付的訂單，會透過付款處理程式線上退款。
- [離線退款](payments.md#offline-payment-methods) — 以「貨到付款」（[貨到付款](cash-on-delivery.md)）或[支票或匯票](check-money-order.md)支付的訂單會離線退款。

您可以針對任何付款方式核發離線退款或帳戶貸項（如果已啟用）。

已由「貨到付款」（[貨到付款](cash-on-delivery.md)）或[支票或匯票](check-money-order.md)支付的訂單已離線退款。

## 退款工作流程

1. **付款動作** — 如果[付款動作](credit-memo-create.md#payment-action-setting)組態設定為`Authorize`，您必須先產生商業發票，才能建立銷退折讓單 — 請繼續執行步驟2。 若設為`Authorize and Capture`，表示已產生發票 — 請繼續執行步驟3。

1. **產生商業發票** - [建立訂單的商業發票](invoices.md#create-an-invoice)，以便透過銷退折讓單將退款傳送給客戶。

1. **建立銷退折讓單** - [在管理員中針對[銷退折讓購買](credit-memo-create.md#issue-a-refund-for-a-credit-purchase)或[支票或匯票](credit-memo-create.md#issue-an-offline-refund-for-check-or-money-order)發出銷退折讓單](credit-memo-create.md)。

## 欄說明

| 欄 | 說明 |
|--- |--- |
| [!UICONTROL Select] | 選取要接受作業之銷退折讓單專案的核取方塊，或使用欄標題中的選取控制項。 選項： `Select All` / `Deselect All` |
| [!UICONTROL Credit Memo] | 提交銷退折讓單請求時指派的唯一數值識別碼。 |
| [!UICONTROL Created] | 採購員首次提交銷退折讓單請求的日期和時間。 |
| [!UICONTROL Order#] | 退貨產品的訂單訂單識別碼。 |
| [!UICONTROL Order Date] | 採購員下訂單的日期和時間。 |
| [!UICONTROL Bill-to Name] | 負責支付訂單的人員名稱。 |
| [!UICONTROL Status] | 表示銷退折讓單請求的目前狀態。 |
| [!UICONTROL Refunded] | 從訂單退款的總金額。 |
| [!UICONTROL Actions] | **[!UICONTROL View]** — 開啟銷退折讓單請求，並維護買賣雙方之間的議價記錄。 |
| [!UICONTROL Order Status] | 表示訂單狀態。 |
| [!UICONTROL Purchased From] | 表示下訂單的網站、商店和商店檢視。 |
| [!UICONTROL Billing Address] | 下訂單的客戶的帳單地址。 |
| [!UICONTROL Shipping Address] | 訂單的送貨地址。 |
| [!UICONTROL Customer Name] | 下訂單的客戶的名字和姓氏。 |
| [!UICONTROL Email] | 下訂單者的電子郵件地址。 |
| [!UICONTROL Customer Group] | 客戶被指派到的客戶群組。 |
| [!UICONTROL Payment Method] | 用於付款的付款方式。 |
| [!UICONTROL Shipping Information] | 用於出貨訂單的方法。 |
| [!UICONTROL Subtotal] | 訂單小計，不含運費與處理費以及稅金。 |
| [!UICONTROL Shipping & Handling] | 運費和處理費。 |
| [!UICONTROL Adjustment Refund] | 新增至退款總金額的金額，作為額外退款。 |
| [!UICONTROL Adjustment Fee] | 從退款總額減去的金額。 |
| [!UICONTROL Grand Total] | 訂單總計。 |

{style="table-layout:auto"}
