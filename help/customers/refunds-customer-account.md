---
title: 客戶帳戶儀表板中的退款
description: 商店客戶可在帳戶控制面板中檢視與訂單相關聯的退款資訊。
exl-id: 8fd6d4e7-74ba-4f39-9a19-7c77ee63b913
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 0%

---

# 客戶帳戶儀表板中的退款

{{ee-feature}}

如果已針對訂單發出退款，則客戶可以在帳戶儀表板中檢視與訂單相關的退款資訊。 如果您已啟用[商店信用組態](../customers/credit-configure.md)的&#x200B;[!UICONTROL _向客戶顯示商店信用記錄_]&#x200B;選項，客戶也可以存取其[商店信用記錄](../customers/store-credit.md)記錄。

## 檢視店面的退款

1. 客戶從店面登入其帳戶。

1. 使用下列其中一種方法來尋找其訂單：

   * 正在尋找&#x200B;**最近訂單**&#x200B;清單中的訂單，並按一下&#x200B;**[!UICONTROL View]**。
   * 在左側面板中選擇&#x200B;**[!UICONTROL My Orders]**。 然後，在清單中尋找順序並按一下&#x200B;**[!UICONTROL View]**。

1. 客戶按一下&#x200B;**[!UICONTROL Refunds]**&#x200B;標籤以檢視退款的詳細資料。

   店面上的![退款詳細資料](assets/customer-account-order-refunds.png){width="700" zoomable="yes"}

## 在店面檢視商店貸方餘額和歷史記錄

方法1：從客戶帳戶儀表板&#x200B;****

1. 客戶從店面登入帳戶。

1. 如果退款已套用至商店點數，請在左側面板中選擇&#x200B;**[!UICONTROL Store Credit]**。

1. 退款給其店舖銷退折讓的金額會顯示在含有動作日期與時間的清單中。

   ![儲存點數退款的金額](assets/customer-account-store-credit.png){width="700" zoomable="yes"}

   >[!INFO]
   >
   >「商店信用卡」頁面也提供客戶贖回[禮品卡](../stores-purchase/product-gift-card-workflow.md#check-status-and-balance-of-the-gift-card)的連結。

方法2：從&#x200B;_檢閱與付款_&#x200B;頁面&#x200B;**中的**

1. 客戶新增產品至購物車。

2. 繼續到&#x200B;_簽出_&#x200B;頁面。

3. 通過&#x200B;**[!UICONTROL Shipping]**&#x200B;步驟。

4. 如果有商店點數可用，則客戶按一下&#x200B;**[!UICONTROL Use Store Credit]**。

   ![儲存來自[檢閱與付款]頁面的信用額度](assets/customer-account-order-refund-from-checkout.png){width="700" zoomable="yes"}

5. 如果客戶改變使用商店點數的想法，請按一下&#x200B;_訂單摘要_&#x200B;區段中的&#x200B;**[!UICONTROL Remove]**。

## 管理員中的付款動作

您可以設定特定[付款方式](../configuration-reference/sales/payment-methods.md)的付款動作。 每種付款方式都有不同的付款動作集。

| 付款動作 | 說明 |
|--- |---|
| [!UICONTROL Capture Online] | 提交商業發票時，系統會從第三方付款閘道擷取付款。 然後，管理員使用者可以建立銷退折讓單，並作廢商業發票。 |
| [!UICONTROL Capture Offline] | 提交商業發票時，系統不會擷取付款。 假設付款是透過閘道直接擷取，而付款無法透過Adobe Commerce擷取。 然後，管理員使用者可以建立銷退折讓單，但無法作廢商業發票。 （即使訂單使用線上付款，商業發票基本上是離線商業發票。） |
| [!UICONTROL Not Capture] | 提交商業發票時，系統不會擷取付款。 我們假設付款是稍後透過Adobe Commerce擷取。 完成的發票中有&#x200B;[!UICONTROL _Capture_]&#x200B;按鈕。 擷取之前，您可以取消商業發票。 擷取之後，您可以建立銷退折讓單並作廢商業發票。 |

{style="table-layout:auto"}

>[!WARNING]
>
>選取&#x200B;[!UICONTROL _不擷取_]&#x200B;選項，除非您確定稍後將透過Adobe Commerce擷取付款。 您必須先使用&#x200B;[!UICONTROL _擷取_]&#x200B;按鈕擷取付款，才能建立銷退折讓單。
