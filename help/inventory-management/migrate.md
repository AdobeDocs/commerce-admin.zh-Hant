---
title: 『[!DNL Commerce] 升級
description: 瞭解Adobe Commerce和Magento Open Source升級如何影響目錄和 [!DNL Inventory Management] 設定。
exl-id: ba640b91-0f29-46df-bfd9-1c43433a751f
feature: Inventory, Upgrade
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 0%

---

# [!DNL Commerce] 升級

如果您在舊版中使用單一來源詳細目錄，此資訊會提供現有目錄和詳細目錄組態的新功能和變更的詳細資訊。

[!DNL Inventory Management] Adobe Commerce適用的和Magento Open Source包含的功能、增強功能和開發人員支援，可增強和更新所有產品庫存管理並新增功能。 所有功能皆可立即使用，包括「來源選擇演演算法」與「並行結帳」，以比對訂單數量與來源及訂單履行。 根據您的網站、商店和商家型別，您可以建立額外的存貨和來源、指定存貨金額等。 如需完整資訊，請參閱 [Inventory management](introduction.md).

安裝Magento Open Source 2.4.x或Adobe Commerce 2.4.x時，會發生下列初始變更：

- [Inventory management](enable.md) 會在全域商店或產品層級啟用。 「管理存貨」選項可啟用或停用存貨數量追蹤、彙總可銷售數量的計算以及預留管理，以追蹤採購到商業發票與出貨的進度。 您可以停用此選項，以使用ERP和其他協力廠商服務來管理存貨、訂單及出貨。 如需詳細資訊，請參閱 [!DNL Inventory Management] 以下的模組。

- A [預設來源](sources-manage.md) 和 [預設庫存](stocks-manage.md) 將新增到系統。 請勿停用或移除這些預設值。 [!DNL Commerce] 將現有和新匯入的產品指派給這些預設值。

  >[!IMPORTANT]
  >
  >強烈建議不要使用「預設坯件」和「預設來源」，因為它們是 `CatalogInventory` 模組，現已棄用。 建議您建立並使用自訂庫存和來源。

   - 存貨提供彙總的虛擬可銷售數量，並預留位置以追蹤購物車與訂單，確保同時結帳。

   - 目錄中的所有現有產品都會指派至預設來源。 在新增來源之前，產品介面不會變更。 如果您只從一個地點出貨產品，則來源沒有其他差異。 您可以建立自訂 [來源](sources-add.md) 和 [指定數量](quantities-manage.md) 每個出貨地點。

   - 您可以將來源設定為「取車地點」，並且 [指定數量](quantities-manage.md) 用於該來源。

   - 您的網站會指定給「預設庫存」。 您可以建立自訂 [庫存](stocks-add.md) 連線銷售管道（網站）和來源（位置）。

- 其他 [設定選項](configuration.md) 新增至您的產品和全域商店。 部分現有設定選項會收到更新的選項和行為：

   - 「通知以下的數量」會傳送通知並從「可銷售數量」中扣除。

   - 「無庫存臨界值」支援正數、零數和負數。 啟用「延期交貨」時，會忽略正金額，視為零（或無限）。

   - 延期交貨支援零（無限）與負數金額。 啟用時，「通知以下的數量」不會從「可銷售數量」中扣除。

- 「新預留」會追蹤潛在銷售，在訂單出貨時轉換為數量扣減。 您永遠無法直接存取或建立預留。 [!DNL Commerce] 透過訂單、出貨及銷退折讓單，在幕後建立與管理預留。

- [訂單與出貨](shipments.md) 納入新功能，以使用「來源選取演演算法」來建議出貨，並支援來自多個來源的部分出貨，以履行訂單。

- 新增 [匯入/匯出特徵](inventory-import-export.md) 可讓您針對目錄中的所有SKU，整批新增來源、更新存貨數量及設定存貨狀態（庫存中/庫存不足）。 這些功能可讓您修改一個、選取或所有來源。

- 透過「產品格線」頁面新增的大量選項支援大量 [指派和取消指派來源](bulk-assignment.md)、和 [移轉存貨至來源](inventory-transfer.md).

- [!DNL Inventory Management] 支援B2B目錄。 目前，所有B2B產品都必須指派給「預設來源」和「預設庫存」。

## [!DNL Commerce Order Management] 和 [!DNL Inventory Management]

[Commerce Order Management (MCOM)][1] 與不相容 [!DNL Inventory Management]. 安裝後，MCOM模組會提供所有清查管理功能 [!DNL Commerce]，包括單一來源和多來源管理、庫存、預留等。 此 [!DNL Inventory Management] 模組預設為停用。

MCOM為進階全通路訂單管理、全球存貨與多來源、從商店到倉儲的履行，以及集中化客戶服務提供廣泛的功能與服務。 如需完整的功能清單，請參閱 [MCOM功能清單][2].

[!DNL Inventory Management] 擴充現有 [!DNL Commerce] 包含額外選項的功能，可追蹤處理中訂單、庫存量、庫存的可用存貨，以及擴充功能開發的API。

## [!DNL Inventory Management] 模組

您可能想要停用 [!DNL Inventory Management] 模組至：

- 加速目前在Adobe Commerce或Magento Open Source 2.0/2.1/2.2/2.3上並移轉至2.4.x的商家升級。

- 使用自訂或協力廠商存貨與訂單管理模組。

- 使用 [!DNL Order Management System] 用於庫存管理。 目前的聯結器不支援 [!DNL Inventory Management] 介面。 對於升級至Adobe Commerce 2.4.0的OMS商家，他們必須停用這些模組。

如需完整詳細資訊，請參閱 [安裝與更新](install-update.md).

[1]: https://omsdocs.magento.com/
[2]: https://omsdocs.magento.com/en/getting-started/feature-list/
