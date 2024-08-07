---
title: '[!UICONTROL My Requisition Lists]'
description: 瞭解申購清單的客戶體驗（可在客戶帳戶控制面板中取得）。
exl-id: ed1b41aa-9c36-49f8-80f2-ad0eb151b7a5
feature: B2B, Companies
source-git-commit: c94d4e8d13c32c1c1b1d37440fdb953c8527b76c
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# [!UICONTROL My Requisition Lists]

維護請購單清單的主要原因是為了方便您重新訂購產品。 授權客戶可以輕鬆將請購單清單中的專案重新排序，方法是將其新增至購物車，並將專案從一個清單移動或複製到另一個清單。

![我的請購單清單](./assets/account-dashboard-my-requisition-lists.png){width="700" zoomable="yes"}

## 開啟請購單清單

1. 客戶從帳戶儀表板選擇&#x200B;**[!UICONTROL My Requisition Lists]**。

1. 找到要開啟的請購單清單，然後按一下&#x200B;**[!UICONTROL View]**&#x200B;並執行下列任一項作業：

### 新增產品至購物車

1. 客戶執行下列任一項作業來選取要新增的產品：

   - 選取每個專案的核取方塊。
   - 按一下&#x200B;**[!UICONTROL Select All]**。

1. 輸入要加入購物車的&#x200B;**[!UICONTROL Qty]**。

1. 若要變更任何產品選項，請執行下列動作：

   - 在行專案中，按一下&#x200B;_編輯_ （![鉛筆圖示](../assets/icon-edit-pencil.png)）圖示。
   - 變更任何必要的選項。
   - 按一下&#x200B;**[!UICONTROL Update Requisition List]**。

1. 按一下&#x200B;**[!UICONTROL Add to Cart]**。

   ![請購單清單詳細資料](./assets/requisition-list-view.png){width="700" zoomable="yes"}

### 將專案複製到其他清單

1. 客戶會選取每個要移動專案的核取方塊。

1. 按一下&#x200B;**[!UICONTROL Copy Selected]**&#x200B;並執行下列任一項作業：

   - 選擇現有的請購單清單。
   - 按一下&#x200B;**[!UICONTROL Create New Requisition List]**。

### 匯出清單

1. 客戶開啟要匯出的請購單清單。

1. 按一下&#x200B;**[!UICONTROL Export]**&#x200B;連結。

Adobe Commerce會產生並下載包含`sku`和`qty`值的CSV清單。

### 將專案移至其他清單

1. 客戶會選取每個要移動專案的核取方塊。

1. 按一下&#x200B;**[!UICONTROL Move Selected]**&#x200B;並執行下列任一項作業：

   - 選擇現有的請購單清單。
   - 按一下&#x200B;**[!UICONTROL Create New Requisition List]**。

### 列印清單

1. 在清單的右上角，客戶按一下&#x200B;**[!UICONTROL Print]**。

1. 驗證輸出裝置，然後按一下&#x200B;**[!UICONTROL Print]**。

   ![列印請購單清單](./assets/requisition-list-print.png){width="500" zoomable="yes"}

### 編輯產品選項

若要編輯清單中的產品選項，客戶需執行下列動作：

1. 按一下&#x200B;_鉛筆_ （![鉛筆圖示](../assets/icon-edit-pencil.png)）圖示以開啟產品頁面。

1. 變更任何必要的選項。

1. 按一下&#x200B;**[!UICONTROL Update Requisition List]**。

   ![更新請購單清單](./assets/requisition-list-update.png){width="700" zoomable="yes"}

在下列情況下，可以編輯請購單清單中的產品：

- 產品有&#x200B;**[!UICONTROL all options set]** （當它是請購單清單中的[已設定產品](../catalog/product-create-configurable.md)時）。

  產品為&#x200B;**[!UICONTROL added to this Requisition List]**。

- 此產品是[具有選項](../catalog/settings-advanced-custom-options.md)的簡單產品

- 允許編輯產品型別。

### 移除專案

1. 客戶選取每個要移除專案的核取方塊。

1. 按一下&#x200B;**[!UICONTROL Remove Selected]**。

1. 提示確認時，按一下&#x200B;**[!UICONTROL Delete]**。

### 重新命名清單

1. 在清單標題之後，客戶按一下&#x200B;**[!UICONTROL Rename]**。

1. 輸入不同的&#x200B;**[!UICONTROL Requisition List Name]**。

1. 按一下&#x200B;**[!UICONTROL Save]**。

   ![重新命名請購單清單](./assets/requisition-list-rename.png){width="300"}


### 移除請購單清單

1. 客戶開啟要刪除的請購單清單。

1. 按一下&#x200B;**[!UICONTROL Delete Requisition List]**。

1. 提示確認時，按一下&#x200B;**[!UICONTROL Delete]**。

>[!NOTE]
>
>此動作無法復原。

## 動作

| 動作 | 說明 |
|--- |--- |
| [!UICONTROL Rename] | 讓您能夠重新命名請購單清單，並更新說明。 |
| [!UICONTROL Export] | 將請購單清單匯出至CSV檔案。 |
| [!UICONTROL Print] | 列印目前的請購單清單。 |
| [!UICONTROL Select] | 管理要成為動作主旨的專案選擇。 <br/>**[!UICONTROL Select All]**— 選取請購單清單中的所有專案。<br/>**[!UICONTROL Remove Selected]** — 從請購單清單移除所有選取的專案。 <br/>**[!UICONTROL Copy Selected]**— 將所有選取的專案複製到其他請購單清單。 |
| [!UICONTROL Add to Cart] | 將選取的專案新增至購物車。 |
| [!UICONTROL Update List] | 重新計算小計以反映數量的變更。 |
| [!UICONTROL Delete Requisition List] | 從公司使用者的帳戶中刪除請購單清單。 |

{style="table-layout:auto"}
