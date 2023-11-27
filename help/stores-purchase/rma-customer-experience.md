---
title: 傳回店面體驗
description: 瞭解您的客戶如何從店面的帳戶管理產品退貨。
exl-id: c276ca2c-3d8b-4019-a9aa-e7631080f331
feature: Returns, Storefront
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 1%

---

# 傳回店面體驗

{{ee-feature}}

客戶可使用下列其中一種方式，向店面請求RMA：

- [訂單與退貨Widget](../content-design/widget-orders-returns.md) 在側欄中
- _訂購與退貨_ 頁尾中的連結

最佳做法是，確保在客戶服務政策中包含RMA需求和程式的說明。

>[!NOTE]
>
>如果您想要收集與退貨相關的其他資訊，可以新增自己的自訂 [傳回屬性](attributes-returns.md).

所有客戶RMA資訊都會顯示在 **[!UICONTROL My Returns]** 客戶帳戶控制面板中的頁面。

![我的退貨](./assets/my-returns-page.png){width="700" zoomable="yes"}

## 請求RMA

客戶在店面完成下列步驟以提交RMA：

1. 在頁尾中，按一下 **[!UICONTROL Orders and Returns]**.

1. 輸入訂單資訊：

   - 訂單ID
   - 帳單姓氏
   - 電子郵件

1. 點擊數 **[!UICONTROL Continue]**.

   ![訂購與退貨](./assets/storefront-orders-and-returns.png){width="700" zoomable="yes"}

1. 在訂購日期下方，按一下 **[!UICONTROL Return]**.

   ![訂單詳細資料](./assets/storefront-orders-and-returns-order-information.png){width="700" zoomable="yes"}

1. 選擇要傳回的專案，並輸入 **[!UICONTROL Quantity to Return]**.

1. 集合 **[!UICONTROL Resolution]** 變更為下列其中一項：

   - Exchange
   - [退款](../customers/refunds-customer-account.md)
   - [商店點數](../customers/store-credit-using.md)

1. 集合 **[!UICONTROL Item Condition]** 變更為下列其中一項：

   - `Unopened`
   - `Opened`
   - `Damaged`

1. 集合 **[!UICONTROL Reason to Return]** 變更為下列其中一項：

   - `Wrong Color`
   - `Wrong Size`
   - `Out of Service`
   - `Other`

   ![建立新退貨](./assets/storefront-orders-and-returns-create-new-return.png){width="700" zoomable="yes"}

1. 如有需要，設定 **[!UICONTROL Contact Email Address]** 和 **[!UICONTROL Comments]**.

   >[!NOTE]
   >
   >如果訂單包含數個料號，而客戶想要退回其他料號，可以按一下 **[!UICONTROL Add Item To Return]**，選取專案，然後設定所有提及的選項。

1. 點擊數 **[!UICONTROL Submit]**.
