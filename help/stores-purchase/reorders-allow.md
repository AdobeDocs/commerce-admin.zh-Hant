---
title: 允許重新排序
description: 瞭解如何為客戶提供重新排序功能。
exl-id: 9fe4c4fb-8596-4fd0-a93b-927ebdfc0c94
feature: Orders, Storefront
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# 允許重新排序

啟用後，可以直接從客戶帳戶或從中的原始訂單進行重新訂購 _管理員_. 依預設會啟用重新排序。

![管理員中的客戶重新排序連結](./assets/customer-reorder.png){width="700" zoomable="yes"}

## 為訂單啟用重新排序的條件

- 此 _允許重新排序_ 必須啟用組態選項。

- 如果順序為 `Hold` 或 `Payment Review` 狀態，重新排序選項會停用。

- 如果訂單中的任何專案無法使用、無存貨或停用，店面就會停用重新排序選項。

- 一個 _管理員_ 即使任何專案已無庫存或已停用，仍可重新排序。

## 設定以允許客戶重新訂購

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Sales]** 並選擇 **[!UICONTROL Sales]** 底下。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Reorder]** 區段。

   ![重新排序選項](../configuration-reference/sales/assets/sales-reorder.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Allow Reorder]** 至 `Yes`.

   此設定可啟用重新排序功能，其來源為「管理員」中店面或訂單清單上的客戶帳戶。

1. 按一下 **[!UICONTROL Save Config]**.

## 從店面重新排序

客戶可以從兩個頁面啟動特定訂單的再訂購功能：

- _我的訂單_ 頁面

- _訂單檢視_ 頁面

### 我的訂單

此 _重新排序_ 按鈕一律會顯示在含有「訂單」的清單中（即使訂單中的所有產品都無法重新排序）。

![店面範例 — 我的訂單頁面](./assets/my-order-page-view.png){width="700" zoomable="yes"}

**案例1.** 訂單中的所有產品為 **可用** 進行重新排序

系統會將使用者重新導向至購物車，並將所有產品新增至購物車

![購物車](./assets/shopping-cart-page.png){width="700" zoomable="yes"}

**案例2.** 訂單中的部分/所有產品為 **不可用** 進行重新排序

>[!NOTE]
>
>可以重新排序 `Not Visible Individually` 產品。

此 _重新排序_ 按鈕未出現在 _我的訂單_ 和 _檢視訂單_ 頁面。

![我的訂單頁面1](./assets/my-orders-view-page1.png){width="700" zoomable="yes"}

### 訂單檢視頁面

**案例1.** 訂單中的所有產品都可供重新訂購

系統會將使用者重新導向至購物車，並將所有產品新增至購物車

**案例2.** 訂單中的部分/所有產品為 **不可用** 進行重新排序

>[!NOTE]
>
>可以重新排序 `Not Visible Individually` 產品。

此 _重新排序_ 按鈕未出現在 _我的訂單_ 和 _檢視訂單_ 頁面。

![訂單詳細資訊頁面](./assets/order-view-page.png){width="700" zoomable="yes"}

### 購物車不是空的

如果購物車非空白且使用者點按 **[!UICONTROL Reorder]** (來自 _我的訂單_  或 _訂單檢視_ 頁面)，現有產品會保留在購物車中，並新增重新訂購產品。

![重新排序專案](./assets/shopping-cart-view1.png){width="700" zoomable="yes"}

## 從管理員重新排序

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. 找到訂單並在中開啟 **[!UICONTROL View]** 模式。

1. 按一下 **[!UICONTROL Reorder]** ，即會顯示在頂端按鈕列中。

   ![在Admin中檢視訂單詳細資料](./assets/order-view-admin.png){width="600" zoomable="yes"}

   在您按一下 **[!UICONTROL Reorder]**，則 _建立新訂單_ 隨即開啟頁面，其中顯示重新訂購的產品。

   ![建立重新排序](./assets/create-reorder-page.png){width="600" zoomable="yes"}

1. 視需要填寫所有必填欄位。

1. 若要提交訂單，請按一下 **[!UICONTROL Submit Order]**.
