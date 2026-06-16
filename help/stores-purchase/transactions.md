---
title: 交易
description: 瞭解「交易」頁面，以及如何使用它來追蹤您的商店與付款系統之間的活動。
exl-id: 5970db88-146d-4caf-aab4-d9315357a4fe
feature: Payments
TQID: https://experienceleague.adobe.com/WyZwtVw-F-pGxxfcHMU-UTz8GVROVyM-YYaLzivMLBM
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 318
ht-degree: 0%

---

# 交易

_交易_&#x200B;頁面會列出您的商店與付款系統之間發生的所有付款活動，並提供更詳細資訊的存取權。

## 檢視交易

在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Transactions]**。

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

此區段包含有關交易的資訊，並提供&#x200B;**訂單ID**&#x200B;欄中訂單頁面的連結。

| 欄 | 說明 |
|--- |--- |
| [!UICONTROL Transaction ID] | 交易ID編號。 |
| [!UICONTROL Parent Transaction ID] | 上層交易的對應ID號碼（如適用）。 |
| [!UICONTROL Transaction Type] | 交易的型態，可以是「訂購」、「授權」、「擷取」、「作廢」或「退款」。 |
| [!UICONTROL Is Closed] | 交易是否已關閉。 |
| [!UICONTROL Created At] | 建立交易的時間和日期。 |

{style="table-layout:auto"}

### 子交易

建立[訂單](orders.md)的商業發票之後，網格中會顯示子交易。 此格式可讓您在交易階層之後追蹤交易歷史記錄。

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
>如果交易詳細資料無法使用或已過時，請按一下按鈕列中的&#x200B;**[!UICONTROL Fetch]**&#x200B;以更新它們。
