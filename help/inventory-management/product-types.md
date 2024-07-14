---
title: 產品型別
description: 瞭解 [!DNL Inventory Management] 如何支援所有Adobe Commerce和Magento Open Source產品型別的庫存和訂單管理。
exl-id: c800168a-e8b2-4d72-bd3d-68f46ece8a5e
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# 產品型別

[!DNL Inventory Management]支援Adobe Commerce和Magento Open Source中所有產品型別的庫存和訂單管理：簡單、可設定、虛擬、可下載、套件組合和群組。 不同產品型別的來源、庫存和運送選項和需求可能有所不同。

- [單一來源商家](merchant-sourcing.md#single-source-merchants)建立並更新產品設定和數量，而不需要其他更新。 所有建立和新匯入的產品都會自動指派給預設Source和預設庫存，如果啟用且有庫存，客戶將立即可用。

- [多來源商家](merchant-sourcing.md#multi-source-merchants)在建立產品期間或之後指定來源、每個來源的數量及設定。 [!DNL Commerce]會將所有新匯入的產品指派給預設Source，而需要額外的編輯才能指派來源和數量。

| 產品型別 | 送貨與Source選擇演演算法 |
|--|--|
| [[!UICONTROL Simple]](../catalog/product-create-simple.md){target="_blank"} | 支援送貨時的SSA建議和覆寫。 |
| [[!UICONTROL Configurable]](../catalog/product-create-configurable.md){target="_blank"} | 支援送貨時的SSA建議和覆寫。 |
| [[!UICONTROL Virtual]](../catalog/product-create-virtual.md){target="_blank"} | 一律使用SSA建議。 系統會在建立商業發票時隱含地執行演演算法，並一律使用建議的結果。<br/>您無法調整這些結果。 |
| [[!UICONTROL Downloadable]](../catalog/product-create-downloadable.md){target="_blank"} | 一律使用SSA建議。 系統會在建立商業發票時隱含地執行演演算法，並一律使用建議的結果。 <br/>您無法調整這些結果。 |
| [[!UICONTROL Bundle]](../catalog/product-create-bundle.md){target="_blank"} | 支援送貨時的SSA建議和覆寫。 |
| [[!UICONTROL Grouped]](../catalog/product-create-grouped.md){target="_blank"} | 支援送貨時的SSA建議和覆寫。 |
