---
title: 管理存貨數量
description: 瞭解如何為新產品指派來源和數量或變更現有產品。
exl-id: b3d4a4c0-725a-4e62-854f-efb6a5709f73
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# 管理存貨數量

下列資訊詳細說明如何為新產品指定來源與數量或變更現有產品。

建立產品時，請在建立產品期間指定來源和數量。 如需完整指示，請參閱[建立產品](../catalog/product-create.md)。 這些頁面包含單一來源及多重來源資訊，以取得每個來源的來源及數量。

第一次存取具有[!DNL Inventory Management]的已升級[!DNL Commerce]時，所有產品和數量都會指派給預設Source。 透過.csv檔案匯入新產品時，這些產品也會指派給預設Source。

單一來源和多來源商家可以更新來源、存貨數量及每項產品或大量產品的臨界值。

- 單一來源商家可以更新預設Source的產品數量。 此數量是可供銷售的產品總數。

- 多來源商戶可以為每個地點（倉儲、商店、製造商卸貨等）指定每個產品的多個來源和數量。 建議您在設定產品存貨數量之前先新增來源。

將來源和數量新增至產品時，您可以透過「產品格線」檢視金額。 如果您有大量的來源，將滑鼠游標停留在&#x200B;_[!UICONTROL Quantity per Source]_&#x200B;上可檢視具有目前數量的完整可捲動來源清單。

![每個來源的產品數量](assets/inventory-product-quantity.png){width="600" zoomable="yes"}

您有以下選項可指派存貨給產品：

- [為每個產品指派來源](sources-assign-per-product.md) — 手動指派目錄中每個產品的來源。

- [指定每個產品的數量](quantities-assign-per-product.md) — 將庫存量新增至每個來源的產品。 此資訊是多來源商家專屬的。

- [大量指派與取消指派來源](bulk-assignment.md) — 以整批動作將來源指派給選取的產品。 如果要轉移存貨並移除來源，請使用[轉移存貨到Source](inventory-transfer.md)選項。

- [將存貨移轉至Source](inventory-transfer.md) — 將所有存貨從一個來源來源大量移轉至目的地來源。

- [匯入與匯出數量](inventory-import-export.md) — 使用匯入與匯出功能，以來源與存貨數量更新多個產品SKU。
