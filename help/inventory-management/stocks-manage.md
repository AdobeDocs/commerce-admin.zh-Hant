---
title: 管理存貨存量
description: 瞭解如何使用存貨來代表您銷售管道來源的虛擬彙總產品詳細目錄。
exl-id: 076b1325-2de4-46d3-9976-d900bd2cef47
TQID: https://experienceleague.adobe.com/IeG1bA1etAjxiDjSWY83GLNugllHT1mUrZBde45Ha8g
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 524
ht-degree: 0%

---

# 管理庫存

庫存代表您銷售管道（網站）來源的虛擬彙總產品詳細目錄。 根據您的網站組態，庫存可能會指派給一個或多個銷售管道。 每個銷售管道只能指派一個庫存，而且可以將單一庫存指派給多個銷售管道。 透過存貨，您可以修改當訂單通過銷售管道時所使用的來源優先順序。

您一開始會使用無法移除或停用的「預設庫存」。 您只能新增其他銷售管道到庫存。 唯一指派的來源為預設Source。 此庫存供單一來源商家、第三方整合和匯入的產品使用。

銷售管道代表銷售存貨的實體。 依預設，[!DNL Commerce]會將您的商店網站作為銷售管道提供。 銷售管道可延伸以支援其他管道，例如B2B客戶群組及商店檢視。 每個銷售管道只能與一個庫存相關聯。

- **Sales Channel支援** — 銷售管道目前包含現成的網站。 您可以擴充銷售管道，以包含B2B客戶群組及商店檢視等自訂選項。 每個銷售管道只能指派單一存貨。 單一庫存可指派給多個銷售管道。
- **對應至來源** — 每個存貨都可以指派一或多個已啟用或已停用的來源，以計算每個產品的虛擬彙總存貨。
- **優先順序訂單履行** — 完成訂單時，Source選擇演演算法的現成優先順序演演算法會從上到下使用庫存的來源清單。

下圖可協助定義「存貨」如何與「腳踏車商店」商家的「來源」和「銷售管道」相關運作。

![商店庫存的圖表](assets/diagram-stock.png){width="600" zoomable="yes"}

## 山地腳踏車和商店的庫存範例

所有商店都以預設庫存開始。 由於下列原因，它必須保持為`Enabled`：

- 匯入新產品時，會使用它，自動將產品指派給預設來源及庫存，以立即存取[!DNL Inventory Management]。
- 您無法新增預設Source以外的其他來源至此庫存。
- 單一來源商家、套裝產品和群組產品都需要並使用它。

針對多來源商家，建立並設定庫存，以最符合您的商店和訂單履行。 當您為銷售管道指派新庫存時，該銷售管道中任何預先存在的庫存都會被取消指派。

如果是多商店安裝，預設庫存最初會指派給[主要網站](../stores-purchase/stores.md#add-websites){target="_blank"}和預設商店。 在&#x200B;**[!UICONTROL Products]**&#x200B;格線檢視中，已啟用和已停用的產品會顯示正確的庫存和數量。

![管理庫存](assets/inventory-stock.png){width="600" zoomable="yes"}

## 按鈕列

| 按鈕 | 說明 |
|--|--|
| [!UICONTROL Add New Stock] | 開啟&#x200B;_[!UICONTROL New Stock]_&#x200B;表單，此表單用於輸入新的存貨存量，以將存貨對應至銷售管道。 |

## 管理Stock欄說明

| 欄 | 說明 |
|--|--|
| [!UICONTROL ID] | 為股票專案產生的唯一數值ID。 |
| [!UICONTROL Name] | 可識別庫存的唯一名稱。 |
| [!UICONTROL Sales Channels] | 將庫存指派給特定網站作為&#x200B;_銷售管道_，以定義庫存的範圍。 |
| [!UICONTROL Assigned sources] | 指定給存貨的來源，可提供所有產品數量。 |
| [!UICONTROL Action] | **[!UICONTROL Edit]** — 在編輯模式下開啟存貨記錄。 |
