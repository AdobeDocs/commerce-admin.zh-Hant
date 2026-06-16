---
title: 擴充與重組存貨
description: 瞭解如何擴展至多來源商家，或縮小至單一來源商家。
exl-id: 880474e3-6533-4b2f-adf7-4312787ff736
feature: Inventory, Configuration
TQID: https://experienceleague.adobe.com/w4TV-BQrg0RzlHn4DVSdHFPD2M5CF11wA7I5OyA7jsY
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 219
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
