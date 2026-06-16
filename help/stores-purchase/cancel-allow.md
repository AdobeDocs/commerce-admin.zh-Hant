---
title: 允許取消訂單
description: 瞭解如何為客戶提供取消功能。
feature: Orders, Storefront
exl-id: 5a8ef668-f929-4188-8574-0bccdd076f3e
TQID: https://experienceleague.adobe.com/a0jMKgF4a0qXUe15oT2syai6-kGSegU1BX56PO9SSKs
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 291
ht-degree: 0%

---

# 允許取消訂單

啟用後，您可以直接從客戶帳戶取消訂單。 取消預設為停用。

## 為訂單啟用的取消條件

- 必須啟用&#x200B;_允許取消訂單_&#x200B;組態選項。

- 如果訂單處於`Hold`、`Canceled`、`Complete`或`Closed`狀態，店面就會停用取消選項。

- 如果訂單中的任何料號已出貨，店面就會停用取消選項。

- 如果有已付款的料號，則會啟用取消選項，並為該料號建立退款。

- 如果訂單處於`Pending`或`Processing`狀態，則店面會啟用取消選項。

## 設定以允許客戶取消並自訂取消原因

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Sales]**&#x200B;並選取&#x200B;**[!UICONTROL Sales]**。

1. 展開&#x200B;**[!UICONTROL Order cancellation]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![訂單取消選項](../configuration-reference/sales/assets/sales-order-cancellation.png){width="600" zoomable="yes"}

1. 將&#x200B;**[!UICONTROL Order cancellation through GraphQL]**&#x200B;設為`Yes`。

   此設定會從店面的客戶帳戶啟用取消功能。

1. 在&#x200B;**[!UICONTROL Order Order cancellation reasons]**&#x200B;中，您可以新增、刪除或修改任何取消原因。

   透過此設定，當客戶取消訂單時，取消原因會顯示在店面中。
請確定您至少指定了一個原因。

1. 按一下&#x200B;**[!UICONTROL Save Config]**。

## 從店面取消

客戶可以從下列三個頁面啟動特定訂單的取消功能：

- _我的訂單_&#x200B;頁面

- _訂單檢視_&#x200B;頁面

- _我的帳戶_&#x200B;頁面

### 我的訂單

如果可以取消訂單，「我的訂單」頁面中會顯示&#x200B;_取消訂單_&#x200B;按鈕。

![店面範例 — 我的訂單頁面](./assets/my-order-page-view-cancel.png){width="700" zoomable="yes"}

### 訂單檢視頁面

如果可以取消訂單，「檢視訂單」頁面中會顯示&#x200B;_取消訂單_&#x200B;按鈕。

![訂單詳細資料頁面](./assets/order-view-page-cancel.png){width="700" zoomable="yes"}

### 我的帳戶

如果可以取消訂單，_取消訂單_&#x200B;按鈕會顯示在「我的帳戶」頁面的「最近訂單」區段中。

![我的帳戶頁面](./assets/my-account-page-view-cancel.png){width="700" zoomable="yes"}
