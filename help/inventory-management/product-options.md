---
title: 設定 [!DNL Inventory Management] 產品選項
description: 瞭解如何設定 [!DNL Inventory Management] 產品組態選項。
exl-id: b5cff7d2-5197-4362-9503-b07c80793ac7
feature: Inventory, Products
source-git-commit: 67cbb0d05f9f63ef51ccff3580cd27df86645fd0
workflow-type: tm+mt
source-wordcount: '909'
ht-degree: 0%

---

# 設定[!DNL Inventory Management]產品選項

這些設定只會套用至已編輯的產品，並覆寫全球網站層級的所有設定。 在編輯產品時，透過&#x200B;_[!UICONTROL Sources]_&#x200B;區段和&#x200B;_[!UICONTROL Advanced Inventory]_&#x200B;頁面修改這些設定。

- 依來源設定產品選項
- 設定進階詳細目錄的產品選項

## 依來源的產品選項

針對產品的[新增來源](sources-add.md)設定數量與其他設定。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Products]**。

1. 在編輯模式中開啟產品。

1. 展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Sources]**&#x200B;區段，並設定每個來源的產品設定：

   - 輸入&#x200B;**[!UICONTROL Qty]** （數量）金額。

   - 將&#x200B;**[!UICONTROL Source Item Status]**&#x200B;設為`In Stock`或`Out of Stock`。

   - 若要修改「通知每個來源的數量低於」，請清除或選取&#x200B;**[!UICONTROL Notify Quantity Use Default]**&#x200B;核取方塊。

     如果清除，請輸入觸發料號缺貨通知的存貨層次金額。 輸入金額會從存貨層次之料號的「可銷售數量」中扣除。

     `Select to use Default` - [!DNL Commerce]會檢查產品進階詳細目錄選項中的組態設定。
     `Clear to Modify` — 輸入「通知數量」的值，覆寫「進階清查」與「商店」組態設定。

   產品![&#128279;](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}的來源區段

1. 完成時，按一下&#x200B;**[!UICONTROL Done]**，然後按&#x200B;**[!UICONTROL Save]**。

### 欄位說明

| 欄位 | 範圍 | 說明 |
|--|--|--|
| [!UICONTROL Source Code] | 全域 | [來源](sources-manage.md)的唯一代碼。 |
| [!UICONTROL Name] | 全域 | 來源的唯一名稱。 |
| [!UICONTROL Status] | 全域 | 產品在目錄中啟用或停用。 |
| [!UICONTROL Source Item Status] | 全域 | 決定產品目前的可用性。 選項：<br />`In Stock` — 讓產品可供購買。<br />`Out of Stock` — 除非啟用延期交貨，否則會防止產品可供購買，並從目錄中移除清單。 |
| [!UICONTROL Qty] | 全域 | 每個來源或地點的庫存量。 |
| [!UICONTROL Notify Quantity] | 全域 | 如果未選取&#x200B;_[!UICONTROL Notify Quantity Use Default]_，則此特定來源的&#x200B;_[!UICONTROL Notify for Quantity Below]_&#x200B;金額。 |
| [!UICONTROL Notify Quantity Use Default] | 全域 | 表示要在產品&#x200B;_[!UICONTROL Advanced Inventory]_&#x200B;中使用&#x200B;_[!UICONTROL Notify for Quantity Below]_&#x200B;的預設設定，或在商店設定中使用全域設定。 |

## 進階產品選項

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Products]**。

1. 在編輯模式中開啟產品。

1. 展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Sources]**&#x200B;區段，然後按一下&#x200B;**[!UICONTROL Advanced Inventory]**。

1. 若要啟用目錄的[庫存控制](enable.md)，請將&#x200B;**[!UICONTROL Manage Stock]**&#x200B;設為`Yes`。

   >[!NOTE]
   >
   >子產品中的[!UICONTROL Manage Stock]設定會覆寫可設定的產品。

   ![產品的進階詳細目錄](assets/inventory-backorders-product-settings.png){width="600" zoomable="yes"}

1. 輸入&#x200B;**[!UICONTROL Out-of-Stock Threshold]**&#x200B;的金額：

   | 值 | 說明 |
   | ----- | ----- |
   | 正數 | 停用&#x200B;_[!UICONTROL Backorders]_&#x200B;後，請輸入正值。 |
   | 零 | 啟用&#x200B;_[!UICONTROL Backorders]_&#x200B;後，輸入`0`可允許無限延交訂單。 |
   | 負數金額 | 啟用&#x200B;_[!UICONTROL Backorders]_&#x200B;後，建議輸入負值。 此金額會新增至「可銷售數量」。 例如，輸入`-50`以允許此金額以下的訂單。 |

1. 輸入&#x200B;**[!UICONTROL Minimum Qty Allowed in Shopping Cart]**。

1. 輸入&#x200B;**[!UICONTROL Maximum Qty Allowed in Shopping Cart]**。

1. 如果客戶在輸入訂購數量時可使用小數值而非整數，請將&#x200B;**[!UICONTROL Qty uses Decimals]**&#x200B;設為`Yes`。

1. 如果產品可以單獨銷售，請將&#x200B;**[!UICONTROL Allow Multiple Boxes for Shipping]**&#x200B;設為`Yes` （多盒內）。 僅當&#x200B;**[!UICONTROL Qty Uses Decimals]**&#x200B;設定為`Yes`時，此選項才可見。

1. 將&#x200B;**[!UICONTROL Backorders]**&#x200B;設定為下列其中一項：

   | 選項 | 說明 |
   | ----- | ----- |
   | `No Backorders` | 當產品無存貨時，不接受延期交貨。 |
   | `Allow Qty Below 0` | 若要在數量低於零時接受延期交貨，請執行下列步驟： |
   | `Allow Qty Below 0 and Notify Customer` | 若要在數量低於零時接受延期交貨，並通知客戶仍可下訂單。 |

   如需詳細資訊，請參閱[設定延期交貨](backorders.md)。

1. 若要啟用產品的數量增加，請將&#x200B;**[!UICONTROL Enable Qty Increments]**&#x200B;設為`Yes`，並在&#x200B;**[!UICONTROL Qty Increments]**&#x200B;欄位中輸入必須購買的專案數，以符合需求。

   例如，以6為增量銷售的專案可以以6、12、18等數量購買。

   **[!UICONTROL Qty Increments]**&#x200B;欄位設定必須購買多少產品專案作為單一產品，以及可設定、分組和套件產品的子產品。

1. 完成時，按一下&#x200B;**[!UICONTROL Done]**，然後按一下&#x200B;**[!UICONTROL Save]**。

### 欄位說明

| 欄位 | 範圍 | 說明 |
|--|--|--|
| [!UICONTROL Manage Stock] | 全域 | 決定是否使用存貨控制來管理目錄中的此產品。 設定為啟用或停用所有[!DNL Inventory Management]功能。 當您完成退貨或銷退折讓單時，產品數量會自動退回至受影響的來源數量。 如果使用協力廠商ERP系統，您可能會想要停用。 |
| [!UICONTROL Out-of-Stock Threshold] | 全域 | 決定產品被視為無庫存的庫存水準。 選項：<br />正值 — 如果停用延期交貨，請輸入正值。<br />零(0) — 啟用「延期交貨」時，輸入零允許無限延期交貨。<br />負值 — 啟用延期交貨時，建議輸入負值。 此金額會新增至「可銷售數量」。 例如，輸入`-50`以允許此金額以下的訂單。 |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | 全域 | 決定單一訂單可購買的產品最小數量。 |
| [!UICONTROL Maximum Qty Allowed in Shopping Cart] | 全域 | 決定單一訂單可購買的最大產品數量。 |
| [!UICONTROL Qty Uses Decimals] | 全域 | 決定客戶在輸入訂購數量時，是否可以使用小數值而非整數。 選項：<br />`Yes` — 允許以小數輸入值，而非整數。 小數位數適用於以重量、體積或長度出售的產品。<br />`No` — 要求以整數輸入數量值。 |
| [!UICONTROL Allow Multiple Boxes for Shipping] | 全域 | 決定產品的零件是否可以單獨出貨。 當&#x200B;**[!UICONTROL Qty Uses Decimals]** = `Yes`時，會顯示此選項。 |
| [!UICONTROL Backorders] | 全域 | 決定如何管理延期交貨。 延交訂單不會變更訂單的處理狀態。 無論產品是否有庫存，下訂單時仍會立即授權或擷取資金。 產品一推出即開始出貨。 啟用時，建議您為「缺貨臨界值」輸入負值。 選項：<br/>`No Backorders` — 當產品無存貨時，不接受延期交貨。<br />`Allow Qty Below 0` — 當數量低於零時，接受延期交貨。<br />`Allow Qty Below 0 and Notify Customer` — 在數量低於零時接受延期交貨，但通知客戶仍然可以下訂單。 |
| [!UICONTROL Enable Qty Increments] | 全域 | 決定產品是否可以數量遞增方式銷售。 增量可設定必須作為單一產品購買的產品專案數量，以及作為可配置、分組和捆綁產品的子產品的數量。 |

>[!NOTE]
>
>簡單產品設定會覆寫特定產品可設定的產品設定。
