---
title: 管理工具和工作區
description: 瞭解管理員工作區，此工作區可讓您存取用來執行商店的所有工具、資料和內容。
exl-id: 61cc53ab-e1c5-4349-b306-a15eb7c5ab57
source-git-commit: 7b6d70e2f3052af69075790cec1f396e2505bf8b
workflow-type: tm+mt
source-wordcount: '530'
ht-degree: 0%

---

# 管理工具和工作區

Admin工作區可讓您存取所有用於執行存放區的工具、資料和內容。 預設啟動頁面可在設定中設定。 許多「管理」頁面都有列出區段資料的網格，內含一組搜尋、排序、篩選、選取和套用動作的工具。 根據預設， [儀表板](admin-dashboard.md) 是管理員的啟動頁面。 不過，您可以選擇在登入時作為啟動頁面顯示的任何其他頁面。 您可以按一下管理員側邊欄中的標誌，以返回管理員啟動頁面。

![管理員 — 工作區](./assets/admin-workspace.png){zoomable=&quot;yes&quot;}

## 工作區控制項

| 控制 | 說明 |
|--- |--- |
| [!UICONTROL Global Search] | 右上方的搜尋圖示可用來尋找資料庫中的任何值，包括產品、客戶和訂單記錄。 |
| [!UICONTROL Grid Search] | 格線上方的搜尋方塊可用來根據在記錄中找到的關鍵字快速篩選格線顯示。 |
| [!UICONTROL Sort] | 每欄的標題可用於依遞增或遞減順序排序清單。 |
| [!UICONTROL Filters] | 定義一組搜尋引數，用來決定顯示在格線中的記錄。 此外，部分欄標題中的篩選器可用於將清單限製為特定值。 有些篩選器具有可從清單方塊選取的其他選項。 |
| [!UICONTROL Default View] | 決定格線的預設欄配置。 |
| [!UICONTROL Columns] | 決定要選取的 [欄](admin-grid-controls.md) 以及它們在格線中的順序。 欄配置可以變更並儲存為 _檢視_. 依預設，網格中只包含某些欄。 |
| [!UICONTROL Paginate] | 分頁控制項是用來檢視結果的其他頁面。 |
| [!UICONTROL Actions] | 「動作」控制項會將作業套用至所有選取的記錄。 |
| [!UICONTROL Select] | Select控制項用來選取作為動作目標的多個記錄。 選項： `Select All` / `Deselect All` |

{style="table-layout:auto"}

## 工作區搜尋

若要在資料庫中尋找任何記錄，請使用標題中的放大鏡圖示 _管理員_. 結果可包含客戶、產品、訂單或任何相關屬性。 例如，如果您輸入客戶名稱，結果可能會包含客戶記錄及與該名稱相關聯的任何訂單。

![管理員搜尋工具](./assets/admin-search.png){width="700" zoomable="yes"}

1. 在標題中，按一下 _搜尋_ (![放大鏡](../assets/icon-magnify-search.png))圖示以開啟搜尋方塊。

1. 執行下列任一項作業：

   - 若要尋找最接近的相符專案，請輸入要尋找專案的前幾個字母。
   - 若要尋找完全相符的專案，請輸入要尋找的一個或多個單字。

1. 在顯示的搜尋結果中，按一下任何專案以開啟記錄。

## 變更管理員啟動頁面

此 [儀表板](admin-workspace.md#the-dashboard) 是Admin的預設啟動頁面，不過您可以設定不同的啟動頁面。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側導覽面板中的 **[!UICONTROL Advanced]**，選擇 **[!UICONTROL Admin]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Startup Page]** 區段。

   ![進階設定 — 管理啟動頁面設定](./assets/admin-startup-page.png){width="600"}

1. 設定 **[!UICONTROL Startup Page]** 至您登入Admin後要先顯示的頁面。

   如需所有管理員選項的詳細清單，請參閱 [管理員](../configuration-reference/advanced/admin.md) 在 _設定參考_.

1. 完成後，按一下 **[!UICONTROL Save Config]**.
