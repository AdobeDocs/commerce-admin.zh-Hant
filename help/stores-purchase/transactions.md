---
title: 交易
description: 瞭解「交易」頁面，以及如何使用它來追蹤您的商店與付款系統之間的活動。
exl-id: 5970db88-146d-4caf-aab4-d9315357a4fe
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---

# 交易

此 _交易_ 頁面會列出您的商店與付款系統之間發生的所有付款活動，並提供更詳細資訊的存取權。

## 檢視交易

在 _管理員_ 側欄，前往 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Transactions]**.

![交易格線](./assets/transactions.png){width="600" zoomable="yes"}

| 欄 | 說明 |
|--- |--- |
| [!UICONTROL ID] | 指派給每個交易的唯一數值識別碼。 |
| [!UICONTROL Order ID] | 客戶下訂單時指派的唯一識別碼。 |
| [!UICONTROL Transaction ID] | 當客戶下訂單後發生交易時指派的唯一數值識別碼。 |
| [!UICONTROL Parent Transaction ID] | 父交易的識別碼。 |
| [!UICONTROL Payment Method] | 與交易相關聯的付款方法。 |
| [!UICONTROL Transaction Type] | 交易的型態，可以是「訂購」、「授權」、「擷取」、「作廢」或「退款」。 |
| [!UICONTROL Closed] | 交易是否已關閉。 |
| [!UICONTROL Created] | 建立交易的時間和日期。 |

{style="table-layout:auto"}

## 檢視交易詳細資料

按一下您要檢視的專案。

在交易詳細資訊頁面上，您可以檢視交易詳細資訊和子項交易網格。

### 交易資料

本節包含有關交易的資訊，並提供中訂單頁面的連結。 **訂單ID** 欄。

| 欄 | 說明 |
|--- |--- |
| [!UICONTROL Transaction ID] | 交易ID編號。 |
| [!UICONTROL Parent Transaction ID] | 上層交易的對應ID號碼（如適用）。 |
| [!UICONTROL Transaction Type] | 交易的型態，可以是「訂購」、「授權」、「擷取」、「作廢」或「退款」。 |
| [!UICONTROL Is Closed] | 交易是否已關閉。 |
| [!UICONTROL Created At] | 建立交易的時間和日期。 |

{style="table-layout:auto"}

### 子交易

為建立商業發票之後，網格中會顯示子交易 [訂購](orders.md). 此格式可讓您在交易階層之後追蹤交易歷史記錄。

### [!UICONTROL Transaction Details]

本節包含指定交易的其他資訊。 資訊會以索引鍵和值的形式顯示。 可用的索引鍵包括：

- authAmount
- authCode
- Vsresponse
- 帳單寄送地點
- cardCodeResponse
- 客戶
- customerIP
- lineItems
- marketType
- 訂購
- 付款
- 產品
- recurringBilling
- responseCode
- responseReasonCode
- responseReasonDescription
- settlamount
- 解決方案
- submitTimeLocal
- submitTimeUTC
- taxExempt
- transactionstatus

>[!NOTE]
>
>如果交易詳細資料無法使用或已過時，請按一下 **[!UICONTROL Fetch]** 以更新它們。
