---
title: 匯入及匯出詳細目錄
description: 使用具有展開 [!DNL Inventory Management] 選項的原生匯入和匯出功能，以透過SKU更新來源和數量。
exl-id: cb2d2e0d-aef8-4b18-b013-9a7b0ab448bd
feature: Inventory, Data Import/Export
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 0%

---

# 匯入及匯出詳細目錄

對於包含許多產品的目錄，請使用具有擴充[!DNL Inventory Management]選項的原生匯入和匯出功能，以透過SKU更新來源和數量。 使用這些選項，您可以新增來源並更新所有或特定來源的存貨數量。 例如，您可以匯出德國來源的產品而不影響法國、英國或美國來源的產品資訊。

- 升級[!DNL Commerce]或匯入新產品時，[!DNL Commerce]會自動指派預設Source給您的產品。 如果您匯入指派了自訂來源的產品，仍會新增「預設Source」的數量0。 若要更新來源與數量，請使用這些匯入指示。

- 單一來源商家使用匯入僅更新產品數量。 所有現有和新增產品都會指派至預設Source。

- 多來源商家使用匯入功能，在每個SKU的每列新增多個來源和數量。

若要匯入更新，請先匯出特定或所有來源的CSV檔案。 編輯CSV檔案，並為每個來源和數量每個SKU新增一列。 新增來源及新增庫存數量時，您需要原始程式碼。 您無法使用匯入 — 匯出特徵來新增或更新庫存。

## CSV檔案內容

匯出 — 匯入檔案會根據來源包含下列資訊：

- `source_code` - [!DNL Commerce]中來源的程式碼。 每個來源和SKU都有一列。
- `sku` - [!DNL Commerce]中產品的SKU。 SKU必須符合您商店中的產品，才能正確更新[!DNL Inventory Management]資料。
- `status` - 0表示無庫存。 1表示有庫存。 此值必須是1，才能從此來源購買存貨。
- `quantity` — 此SKU和來源可用的庫存總金額。

使用CSV檔案來快速更新多個產品和指派的來源，以更新及更正存貨記錄中的任何不準確專案，而非一次透過應用程式介面更新及更正一個。 對於基礎檔案，請先匯出並根據需要更新。

![匯入的範例CSV檔案 — 匯出詳細目錄資料](assets/inventory-import-export-data.png){width="600" zoomable="yes"}

## 匯出所有來源的產品資料

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**。

1. 針對&#x200B;**[!UICONTROL Entity Type]**，請選擇`Stock Sources`。

   匯出只會擷取含有SKU之產品的資料。

1. 按一下&#x200B;**[!UICONTROL Continue]**。

   檔案會產生並下載以開啟和編輯。

更新庫存數量和產品資料後，將檔案匯回[!DNL Commerce]。

![匯出產品資料和來源的庫存來源](assets/inventory-export-stock-sources.png){width="350" zoomable="yes"}

## 匯出特定來源的產品資料

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**。

1. 針對&#x200B;**[!UICONTROL Entity Type]**，請選擇`Stock Sources`。

   匯出只會擷取含有SKU之產品的資料。

1. 使用&#x200B;**[!UICONTROL Entity Attributes]**&#x200B;篩選特定來源的匯出產品。

   針對`source_code`，在篩選欄位中輸入來原始碼。

1. 按一下&#x200B;**[!UICONTROL Continue]**。

   檔案會產生並下載以開啟和編輯。

更新庫存數量和產品資料後，將檔案匯回[!DNL Commerce]。

## 匯入產品資料

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**。

1. 針對&#x200B;**[!UICONTROL Entity Type]**，請選擇`Stock Sources`。

   匯出只會擷取含有SKU之產品的資料。

1. 選取&#x200B;**[!UICONTROL Import Behavior]**&#x200B;的組態。

1. 選取要匯入的.csv檔案。

1. 按一下&#x200B;**[!UICONTROL Check Data]**&#x200B;並完成匯入。

![匯入產品資料和來源](assets/inventory-import-sources.png){width="600" zoomable="yes"}
