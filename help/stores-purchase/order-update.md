---
title: 更新訂單
description: 瞭解如何在Admin中更新客戶訂單。
exl-id: 15c73d27-f4bd-47d6-8d36-902074f9c3e6
feature: Orders, Customer Service
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 0%

---

# 更新訂單

在協助已下訂單的客戶時，您必須判斷訂單的狀態。 的可用選項 `Pending` 順序與的選項不同 `Processing` 訂購。 如需詳細資訊，請參閱 [處理訂單](order-processing.md).

## 待處理訂單

客戶下訂單後，但在收到付款之前，訂單位於 `Pending` 狀態。 您可以編輯訂單、保留訂單或完全取消訂單。 暫緩訂單的按鈕列會列出訂單可用的動作。

![暫緩訂單選項](./assets/order-button-bar-pending.png){width="600" zoomable="yes"}

如果您修改訂單的主要部分，則會取消原始訂單並產生新訂單。 不過，您可以變更帳單或送貨地址，而不產生新訂單。

| 按鈕 | 說明 |
|--- |--- |
| **[!UICONTROL Back]** | 返回「訂單」頁面而不儲存變更。 |
| **[!UICONTROL Login as Customer]** | 允許管理員使用者協助客戶處理訂單。 |
| **[!UICONTROL Cancel]** | 取消待處理訂單。 |
| **[!UICONTROL Send Email]** | 傳送有關待定訂單的電子郵件給客戶。 |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | 將待處理訂單的狀態變更為 `On Hold`. 若要解除保留，請選擇 _[!UICONTROL Unhold]_. |
| **[!UICONTROL Invoice]** | 建立 [invoice](invoices.md#create-an-invoice) 從暫緩訂單，將訂單轉換為商業發票，並將訂單狀態變更為 `processing`. |
| **[!UICONTROL Ship]** | 建立 [出貨](shipments.md#create-a-shipment) 訂單記錄。 |
| **[!UICONTROL Reorder]** | 建立與目前暫緩訂單重複的新暫緩訂單。 |
| **[!UICONTROL Edit]** | 在編輯模式中開啟擱置訂單。 「編輯」按鈕僅適用於暫緩訂單，或根據議價的訂單 [引號](../b2b/quotes.md). |

{style="table-layout:auto"}

## 處理訂單

訂單輸入 `Processing` 狀態時間：

* 當付款作業設為時，會接收/擷取訂單的付款，並產生商業發票 `Authorize and Capture`.
* 當付款作業設為時，已授權訂單交易，但尚未擷取付款 `Authorize`.

此 [付款動作設定](../configuration-reference/sales/payment-methods.md#payment-actions) 決定建立訂單後可用的訂單動作。

您基本上無法變更 `Processing` 訂單，但您可以編輯帳單和送貨地址。

![處理順序選項](./assets/order-button-bar-processing.png){width="600" zoomable="yes"}

>[!NOTE]
>
>當付款方式的付款作業設為 `Authorize and Capture`，則會在客戶下訂單時自動建立發票。 在此情況下，您可以使用 [銷退折讓單](credit-memo-create.md)，但無法 [取消](#cancel-a-pending-order) 或 [無效](#void-a-processing-order) 訂單。

| 按鈕 | 說明 |
|--- |--- |
| **[!UICONTROL Back]** | 返回「訂單」頁面而不儲存變更。 |
| **[!UICONTROL Send Email]** | 傳送有關訂單的電子郵件給客戶。 |
| **[!UICONTROL Void]** | [空隙](#void-a-processing-order) 訂單異動或部份訂單異動。 |
| **[!UICONTROL Credit Memo]** | 啟動程式以建立 [銷退折讓單](credit-memo-create.md). |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | 將銷售訂單的狀態變更為 `On Hold`. 若要解除銷售訂單的保留，請選擇 _[!UICONTROL Unhold]_. |
| **[!UICONTROL Reorder]** | 根據目前訂單建立新的暫緩訂單。 |
| **[!UICONTROL Create Returns]** | ![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)將程式起始至 [return](returns.md) 訂單中的一或多個專案。 |

{style="table-layout:auto"}

## 讓處理訂單失效

當訂單仍在 `Processing` 狀態且付款整合已設為 `Authorize` (非 `Authorize and Capture`)，您只能作廢交易或取消訂單。 [取消訂單](#cancel-a-pending-order) 也會使授權失效。

使用付款方式下訂單，且付款作業設為時 `Authorize and Capture` 您可以透過銷退折讓單退回資金，但無法取消資金，因為已開立商業發票且已抓取付款。

您的付款方式會決定您可用的付款作業。 另請參閱 [付款動作](../configuration-reference/sales/payment-methods.md#payment-actions) 以取得詳細資訊。

**_若要作廢訂單，請執行下列步驟：_**

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. 在 **[!UICONTROL Action]** 要編輯的順序欄，按一下 **[!UICONTROL View]**.

1. 按一下 **[!UICONTROL Void]** 以作廢訂單。

1. 出現提示時，按一下 **[!UICONTROL OK]** 以作廢訂單。

您可以使用 [銷退折讓單](credit-memo-create.md) 擷取資金之後。 您也可以建立 [退貨授權(RMA)](returns.md) 發行以取得產品退貨。 若要深入瞭解，請參閱 [處理訂單](order-processing.md).

## 編輯待處理訂單

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. 在 **[!UICONTROL Action]** 要編輯的順序欄，按一下 **[!UICONTROL View]**.

1. 按一下 **[!UICONTROL Edit]**.

   ![編輯順序](./assets/order-edit.png){width="600" zoomable="yes"}

1. 出現提示時，按一下 **[!UICONTROL OK]** 以繼續編輯。

1. 視需要更新訂單。

1. 套用您的變更：
   * 若要儲存對帳單或送貨地址所做的變更，請按一下 **[!UICONTROL Save]**.
   * 若要儲存對行專案所做的變更並重新處理訂單，請按一下 **[!UICONTROL Submit Order]**.

## 保留訂單

如果客戶的偏好付款方式無法使用，或料號暫時無庫存，您可以保留訂單。

1. 在 _訂購_ 格線，尋找 `Pending` 要保留的訂單。

1. 在 _動作_ 欄，按一下 **[!UICONTROL View]**.

1. 按一下 **[!UICONTROL Hold]** 以保留訂單。

若要移除訂單的保留，請再次編輯訂單，然後按一下 **[!UICONTROL Unhold]**.

## 取消擱置中的訂單

取消訂單會將其狀態從 `Pending` 至 `Canceled`.

1. 在 _[!UICONTROL Orders]_格線，尋找要取消的暫緩訂單。

1. 在 _[!UICONTROL Action]_欄，按一下&#x200B;**[!UICONTROL View]**.

1. 按一下 **[!UICONTROL Cancel]** 以取消訂單。

訂單的狀態現在為 `Canceled`.
