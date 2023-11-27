---
title: 客戶帳戶儀表板中的退款
description: 商店客戶可在帳戶控制面板中檢視與訂單相關聯的退款資訊。
exl-id: 8fd6d4e7-74ba-4f39-9a19-7c77ee63b913
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 0%

---

# 客戶帳戶儀表板中的退款

{{ee-feature}}

如果已針對訂單發出退款，則客戶可以在帳戶儀表板中檢視與訂單相關的退款資訊。 如果您已啟用 [!UICONTROL _向客戶顯示商店信用記錄_] 選項 [存放區信用設定](../customers/credit-configure.md)，客戶也可以存取 [商店點數](../customers/store-credit.md) 歷史記錄。

## 檢視店面的退款

1. 客戶從店面登入其帳戶。

1. 使用下列其中一種方法來尋找其訂單：

   * 尋找清單中的順序 **最近的訂單** 並按一下 **[!UICONTROL View]**.
   * 在左側面板中，選擇 **[!UICONTROL My Orders]**. 接著，在清單中找出順序，然後按一下 **[!UICONTROL View]**.

1. 客戶按一下 **[!UICONTROL Refunds]** 頁標，以檢視退款的詳細資料。

   ![店面的退款詳細資料](assets/customer-account-order-refunds.png){width="700" zoomable="yes"}

## 在店面檢視商店貸方餘額和歷史記錄

方法1： **從客戶帳戶儀表板**

1. 客戶從店面登入帳戶。

1. 如果退款已沖銷至商店退款，則選擇 **[!UICONTROL Store Credit]** 在左側面板中。

1. 退款給其店舖銷退折讓的金額會顯示在含有動作日期與時間的清單中。

   ![退還給商店貸方的金額](assets/customer-account-store-credit.png){width="700" zoomable="yes"}

   >[!INFO]
   >
   >「商店業績」頁面也會提供客戶兌換的連結。 [禮品卡](../stores-purchase/product-gift-card-workflow.md#check-status-and-balance-of-the-gift-card).

方法2： **從 _稽核與付款_ 頁面**

1. 客戶新增產品至購物車。

2. 繼續前往 _簽出_ 頁面。

3. 傳遞 **[!UICONTROL Shipping]** 步驟。

4. 如果有商店點數可用，則客戶按一下 **[!UICONTROL Use Store Credit]**.

   ![儲存複查與付款的信用頁](assets/customer-account-order-refund-from-checkout.png){width="700" zoomable="yes"}

5. 如果客戶改變使用商店點數的想法，請按一下 **[!UICONTROL Remove]** 在 _訂單摘要_ 區段。

## 管理員中的付款動作

您可以針對您的特定專案設定付款動作 [付款方法](../configuration-reference/sales/payment-methods.md). 每種付款方式都有不同的付款動作集。

| 付款動作 | 說明 |
|--- |---|
| [!UICONTROL Capture Online] | 提交商業發票時，系統會從第三方付款閘道擷取付款。 然後，管理員使用者可以建立銷退折讓單，並作廢商業發票。 |
| [!UICONTROL Capture Offline] | 提交商業發票時，系統不會擷取付款。 假設付款是透過閘道直接擷取，而付款無法透過Adobe Commerce擷取。 然後，管理員使用者可以建立銷退折讓單，但無法作廢商業發票。 （即使訂單使用線上付款，商業發票基本上是離線商業發票。） |
| [!UICONTROL Not Capture] | 提交商業發票時，系統不會擷取付款。 我們假設付款是稍後透過Adobe Commerce擷取。 有一個 [!UICONTROL _Capture_] 已完工商業發票中的按鈕。 擷取之前，您可以取消商業發票。 擷取之後，您可以建立銷退折讓單並作廢商業發票。 |

{style="table-layout:auto"}

>[!WARNING]
>
>選取 [!UICONTROL _Not Capture_] 選項，除非您確定稍後會透過Adobe Commerce擷取付款。 您必須先使用擷取付款，才能建立銷退折讓單 [!UICONTROL _Capture_] 按鈕。
