---
title: 允許取消訂單
description: 瞭解如何為客戶提供取消功能。
feature: Orders, Storefront
source-git-commit: 613c081c02dd9b5e55de37dccd021af4e429d424
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 0%

---


# 允許取消訂單

啟用後，您可以直接從客戶帳戶取消訂單。 取消預設為停用。

## 為訂單啟用的取消條件

- 此 _允許取消訂單_ 必須啟用組態選項。

- 如果順序為 `Hold`， `Canceled`， `Complete`，或 `Closed` 狀態，店面的取消選項會停用。

- 如果訂單中的任何料號已出貨，店面就會停用取消選項。

- 如果有已付款的料號，則會啟用取消選項，並為該料號建立退款。

- 如果順序為 `Pending` 或 `Processing` 狀態，店面已啟用取消選項。

## 設定以允許客戶取消並自訂取消原因

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Sales]** 並選取 **[!UICONTROL Sales]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Order cancellation]** 區段。

   ![訂單取消選項](../configuration-reference/sales/assets/sales-order-cancellation.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Order cancellation through GraphQL]** 至 `Yes`.

   此設定會從店面的客戶帳戶啟用取消功能。

1. 在 **[!UICONTROL Order Order cancellation reasons]** 您可以新增、刪除或修改任何取消原因。

   透過此設定，當客戶取消訂單時，取消原因會顯示在店面中。
請確定您至少指定了一個原因。

1. 按一下 **[!UICONTROL Save Config]**.

## 從店面取消

客戶可以從下列三個頁面啟動特定訂單的取消功能：

- _我的訂單_ 頁面

- _訂單檢視_ 頁面

- _我的帳戶_ 頁面

### 我的訂單

此 _取消訂單_ 如果可以取消訂單，則會在「我的訂單」頁面中顯示按鈕。

![店面範例 — 我的訂單頁面](./assets/my-order-page-view-cancel.png){width="700" zoomable="yes"}

### 訂單檢視頁面

此 _取消訂單_ 如果訂單可以取消，則會在「檢視訂單」頁面中顯示按鈕。

![訂單詳細資訊頁面](./assets/order-view-page-cancel.png){width="700" zoomable="yes"}

### 我的帳戶

此 _取消訂單_ 如果可以取消訂單，則會在「我的帳戶」頁面的「最近訂單」區段中顯示按鈕。

![我的帳戶頁面](./assets/my-account-page-view-cancel.png){width="700" zoomable="yes"}


