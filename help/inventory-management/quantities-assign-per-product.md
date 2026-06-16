---
title: 指定每個產品的存貨數量
description: 瞭解如何更新產品的存貨數量，以及追蹤庫存量、可用存貨量。
exl-id: 935385bb-6657-4d49-980e-96a3d0d3a187
feature: Inventory, Products
TQID: https://experienceleague.adobe.com/0OBXyHUbsWVXmEnWEWd0CGcBNhci57w8HGtDCGCWuOk
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 210
ht-degree: 0%

---

# 指定每個產品的數量

新增[來源](sources-assign-per-product.md)之後，請更新產品的存貨數量。 這些值會追蹤庫存量、可用庫存量。

若要在不移除來源的情況下隱藏來源的存貨，請將&#x200B;_[!UICONTROL Source Item Status]_設為`Out of Stock`。 SSA和出貨選項只會存取列為`In Stock`且有可用存貨數量的來源。

所有更新的數量和來源都會顯示在產品格線中。

## 更新數量

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Products]**。

1. 在編輯模式中尋找並開啟產品。

1. 展開&#x200B;**[!UICONTROL Sources]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

1. 將&#x200B;**[!UICONTROL Source Item Status]**&#x200B;設為`In Stock`。

1. 若要更新庫存量，請輸入&#x200B;**[!UICONTROL Qty]**&#x200B;的金額。

1. 若要設定存貨數量的通知，請執行下列其中一項作業：

   - 自訂通知數量 — 取消選取&#x200B;**[!UICONTROL Use Default]**&#x200B;核取方塊，並在&#x200B;**[!UICONTROL Notify Qty]**&#x200B;中輸入金額。
   - 預設通知數量 — 選取&#x200B;**[!UICONTROL Use Default]**&#x200B;核取方塊。 [!DNL Commerce]檢查並使用&#x200B;_[!UICONTROL Advanced Inventory]_或全域存放區組態中的設定。

   ![根據Source更新產品數量](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. 執行下列任一項作業以儲存：

   - 按一下&#x200B;**[!UICONTROL Save]**。

   - 在&#x200B;**[!UICONTROL Save]** （![功能表箭頭](../assets/icon-menu-down-arrow-red.png)）功能表上，選擇&#x200B;**[!UICONTROL Save & Close]**。


「產品格線」會以所有來源和相關數量的清單更新。 對於擁有超過五個指派來源的產品，將游標暫留在&#x200B;_[!UICONTROL Quantity per Source]_欄上可檢視完整清單。

![每個來源的產品數量](assets/inventory-product-quantity.png){width="600" zoomable="yes"}
