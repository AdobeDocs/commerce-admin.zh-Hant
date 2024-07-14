---
title: 擴充與重組存貨
description: 瞭解如何擴展至多來源商家，或縮小至單一來源商家。
exl-id: 880474e3-6533-4b2f-adf7-4312787ff736
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---

# 擴充與重組存貨

隨著您的企業成長與變更，[!DNL Inventory Management]可支援您的需求。 您可以輕鬆展開至多來源商家，或縮減至單一來源商家。

## 展開至多來源

單一來源的商戶可能會新增商店、倉庫、卸貨託運人等。 擴充只需要新增少量內容和庫存更新，即可擴充至多來源：

1. 為每個新位置新增[自訂來源](sources-add.md)。

   您僅對套件組合產品使用預設Source。

1. 視需要為您的新來源新增[自訂庫存](stocks-add.md)。

   例如，您可能想要根據網站、國家/地區、地區或其他方法建立庫存。 您可以將來源指派給自訂庫存。 您只對組合產品使用「預設庫存」。

1. 更新您產品的[來源指派與數量](quantities-manage.md)。

   您也可以使用[大量動作工具](bulk-assignment.md)和[匯入 — 匯出](inventory-import-export.md)功能，快速新增來源和產品資料。

## 重新建構為單一來源

針對想要將線上銷售減少到單一出貨地點的多來源商家，請修改您的來源、存貨及數量以進行更新：

1. 停用[自訂來源](sources-disable.md)。

1. 將產品詳細目錄轉移至您的預設Source。

   建議使用大量動作。 請參閱[將存貨傳輸至Source](inventory-transfer.md)。

1. 將所有網站指派給[預設庫存](stocks-manage.md)。
