---
title: '"設定 [!DNL Inventory Management] 產品選項」'
description: 瞭解如何設定 [!DNL Inventory Management] 產品組態選項。
exl-id: b5cff7d2-5197-4362-9503-b07c80793ac7
feature: Inventory, Products
source-git-commit: ccd93a54b6fa23a7a54fb423f8232c72cd8fe027
workflow-type: tm+mt
source-wordcount: '859'
ht-degree: 0%

---

# 設定 [!DNL Inventory Management] 產品選項

這些設定只會套用至已編輯的產品，並覆寫全球網站層級的所有設定。 編輯產品時，請透過 _[!UICONTROL Sources]_區段和_[!UICONTROL Advanced Inventory]_ 頁面。

- 依來源設定產品選項
- 設定進階詳細目錄的產品選項

## 依來源的產品選項

設定數量和其他設定，依據 [已新增來源](sources-add.md) 用於產品。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 在編輯模式中開啟產品。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Sources]** 區段並設定每個來源的產品設定：

   - 輸入 **[!UICONTROL Qty]** （數量）金額。

   - 設定 **[!UICONTROL Source Item Status]** 作為 `In Stock` 或 `Out of Stock`.

   - 若要修改「通知每個來源的數量低於」，請清除或選取 **[!UICONTROL Notify Quantity Use Default]** 核取方塊。

     如果清除，請輸入觸發料號缺貨通知的存貨層次金額。 輸入金額會從存貨層次之料號的「可銷售數量」中扣除。

     `Select to use Default` - [!DNL Commerce] 檢查產品進階詳細目錄選項以取得組態設定。
     `Clear to Modify`  — 輸入「通知數量」的值，覆寫「進階存貨」與「商店」組態設定。

   ![產品的來源區段](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. 完成後，按一下 **[!UICONTROL Done]**，然後 **[!UICONTROL Save]**.

### 欄位說明

| 欄位 | 範圍 | 說明 |
|--|--|--|
| [!UICONTROL Source Code] | 全域 | 的唯一代碼 [來源](sources-manage.md). |
| [!UICONTROL Name] | 全域 | 來源的唯一名稱。 |
| [!UICONTROL Status] | 全域 | 產品在目錄中啟用或停用。 |
| [!UICONTROL Source Item Status] | 全域 | 決定產品目前的可用性。 選項：<br />`In Stock`  — 讓產品可供購買。<br />`Out of Stock`  — 除非已啟用「延期交貨」，否則會防止產品可供購買，並從目錄中移除清單。 |
| [!UICONTROL Qty] | 全域 | 每個來源或地點的庫存量。 |
| [!UICONTROL Notify Quantity] | 全域 | 的金額 _[!UICONTROL Notify for Quantity Below]_特定來源的ID_[!UICONTROL Notify Quantity Use Default]_ 未選取。 |
| [!UICONTROL Notify Quantity Use Default] | 全域 | 指示使用預設設定 _[!UICONTROL Notify for Quantity Below]_在產品中_[!UICONTROL Advanced Inventory]_ 或存放區設定中的全域設定。 |

## 進階產品選項

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 在編輯模式中開啟產品。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Sources]** 區段並按一下 **[!UICONTROL Advanced Inventory]**.

1. 若要啟用 [詳細目錄控制](enable.md) 針對您的目錄，設定 **[!UICONTROL Manage Stock]** 至 `Yes`.

   >[!NOTE]
   >
   >[!UICONTROL Manage Stock] 子項產品中的設定會覆寫可設定的產品。

   ![產品的進階詳細目錄](assets/inventory-backorders-product-settings.png){width="600" zoomable="yes"}

1. 輸入金額 **[!UICONTROL Out-of-Stock Threshold]**：

   | 值 | 說明 |
   | ----- | ----- |
   | 正數 | 替換為 _[!UICONTROL Backorders]_已停用，請輸入正值。 |
   | 零 | 替換為 _[!UICONTROL Backorders]_已啟用，請輸入 `0` 允許無限延期交貨。 |
   | 負數金額 | 替換為 _[!UICONTROL Backorders]_已啟用，建議輸入負值。 此金額會新增至「可銷售數量」。 例如，輸入 `-50` 允許訂單達到此金額。 |

1. 輸入 **[!UICONTROL Minimum Qty Allowed in Shopping Cart]**.

1. 輸入 **[!UICONTROL Maximum Qty Allowed in Shopping Cart]**.

1. 設定 **[!UICONTROL Qty uses Decimals]** 至 `Yes` 若客戶在輸入訂購數量時，可使用小數值而非整數。

1. 設定 **[!UICONTROL Allow Multiple Boxes for Shipping]** 至 `Yes` 如果產品可以單獨銷售，則需使用多個盒子。 出現以下情況時可看見此選項： **[!UICONTROL Qty Uses Decimals]** 設為 `Yes` 僅限。

1. 設定 **[!UICONTROL Backorders]** 變更為下列其中一項：

   | 選項 | 說明 |
   | ----- | ----- |
   | `No Backorders` | 當產品無存貨時，不接受延期交貨。 |
   | `Allow Qty Below 0` | 若要在數量低於零時接受延期交貨，請執行下列步驟： |
   | `Allow Qty Below 0 and Notify Customer` | 若要在數量低於零時接受延期交貨，並通知客戶仍可下訂單。 |

   如需詳細資訊，請參閱 [設定延期交貨](backorders.md).

1. 若要啟動產品的數量增加，請設定 **[!UICONTROL Enable Qty Increments]** 至 `Yes` 並輸入必須採購的專案數目，以符合 **[!UICONTROL Qty Increments]** 欄位。

   例如，以6為增量銷售的專案可以以6、12、18等數量購買。

1. 完成後，按一下 **[!UICONTROL Done]** 然後 **[!UICONTROL Save]**.

### 欄位說明

| 欄位 | 範圍 | 說明 |
|--|--|--|
| [!UICONTROL Manage Stock] | 全域 | 決定是否使用存貨控制來管理目錄中的此產品。 設定為全部啟用或停用 [!DNL Inventory Management] 功能。 當您完成退貨或銷退折讓單時，產品數量會自動退回至受影響的來源數量。 如果使用協力廠商ERP系統，您可能會想要停用。 |
| [!UICONTROL Out-of-Stock Threshold] | 全域 | 決定產品被視為無庫存的庫存水準。 選項：<br />正值 — 停用延期交貨時，請輸入正金額。<br />零(0) — 啟用「延期交貨」時，輸入零允許無限延期交貨。<br />負值 — 啟用延期交貨時，建議輸入負值。 此金額會新增至「可銷售數量」。 例如，輸入 `-50` 允許訂單達到此金額。 |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | 全域 | 決定單一訂單可購買的產品最小數量。 |
| [!UICONTROL Maximum Qty Allowed in Shopping Cart] | 全域 | 決定單一訂單可購買的最大產品數量。 |
| [!UICONTROL Qty Uses Decimals] | 全域 | 決定客戶在輸入訂購數量時，是否可以使用小數值而非整數。 選項：<br />`Yes`  — 允許以小數輸入值，而非整數。 小數位數適用於以重量、體積或長度出售的產品。<br />`No`  — 要求以整數輸入數量值。 |
| [!UICONTROL Allow Multiple Boxes for Shipping] | 全域 | 決定產品的零件是否可以單獨出貨。 出現以下情況時可看見此選項： **[!UICONTROL Qty Uses Decimals]** = `Yes`. |
| [!UICONTROL Backorders] | 全域 | 決定如何管理延期交貨。 延交訂單不會變更訂單的處理狀態。 無論產品是否有庫存，下訂單時仍會立即授權或擷取資金。 產品一推出即開始出貨。 啟用時，建議您為「缺貨臨界值」輸入負值。 選項：<br/>`No Backorders`  — 產品無庫存時，不接受延期交貨。<br />`Allow Qty Below 0`  — 當數量低於零時，接受延期交貨。<br />`Allow Qty Below 0 and Notify Customer`  — 在數量低於零時接受延期交貨，但通知客戶仍可下訂單。 |
| [!UICONTROL Enable Qty Increments] | 全域 | 決定產品是否可以數量遞增方式銷售。 |

>[!NOTE]
>
>簡單產品設定會覆寫特定產品可設定的產品設定。
