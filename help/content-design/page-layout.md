---
title: 頁面配置
description: 瞭解頁面配置區段以及如何設定預設配置。
exl-id: 397a92cf-6f20-4729-8d7c-c5f672fc1c9a
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '861'
ht-degree: 0%

---

# 頁面配置

商店中每個頁面的版面配置都包含定義頁面頁首、頁尾和內容區域的不同區段或容器。 視版面配置而定，每個頁面可能會有一欄、兩欄、三欄或更多欄。 您可以將該版面配置視為頁面的&#x200B;_平面圖_，並指派特定版面配置作為CMS、產品及類別頁面的預設值。

在頁面上，內容區塊會根據[頁面配置](layout-updates.md)中指派顯示它們的區段，浮動以填滿可用空間。 請注意，如果您將版面配置從三欄變更為兩欄，主區域的內容會展開以填滿可用空間。 另請注意，與未使用側邊列關聯的任何區塊似乎都會消失。 不過，如果您恢復三欄版面配置，區塊會重新出現。 這種流動式方法，或&#x200B;_流動式版面_，可以變更頁面版面，而不需要重新處理內容。 如果您習慣使用個別HTML頁面，這種模組化的&#x200B;_建置區塊_&#x200B;方法需要不同的思考方式。

![標準兩欄式左條頁面配置](./assets/storefront-2-column-ee.png){width="700" zoomable="yes"}

## 設定預設版面

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板的&#x200B;_[!UICONTROL General]_下，選擇&#x200B;**[!UICONTROL Web]**。

1. 展開&#x200B;**[!UICONTROL Default Layouts]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![預設版面配置](./assets/web-default-layouts.png){width="600" zoomable="yes"}

1. 選擇您要用於產品頁面的&#x200B;**[!UICONTROL Default Product Layout]**。

   此設定決定預設用於產品頁面的版面。

   - `No layout updates` — 產品頁面沒有配置更新可用。
   - `Empty` — 對產品頁面使用空白配置。
   - `1 column` — 對產品頁面使用單一欄配置。
   - `2 columns with left bar` — 針對產品頁面使用左側邊欄的雙欄配置。
   - `2 columns with right bar` — 針對產品頁面使用右側具側欄的雙欄配置。
   - `3 columns` — 對產品頁面使用左右兩側有側欄的三欄式配置。

   啟用[頁面產生器](../page-builder/introduction.md)時，會有其他可用的完整寬度選項。 然後您可以使用頁面產生器內容工具來設計產品頁面的版面。

   - `Page -- Full Width` — 使用產品頁面的&#x200B;_頁面 — 全寬_&#x200B;配置。
   - `Category -- Full Width` — 使用產品頁面的&#x200B;_類別 — 完整寬度_&#x200B;配置。
   - `Product -- Full Width` - （建議）使用產品頁面的&#x200B;_Product - Full Width_&#x200B;配置。

1. 選擇您要用於類別頁面的&#x200B;**[!UICONTROL Default Category Layout]**。

   此設定會決定類別頁面預設使用的版面。

   - `No layout updates` — 配置更新不適用於類別頁面。
   - `Empty` — 對類別頁面使用空白配置。
   - `1 column` — 對類別頁面使用單一欄配置。
   - `2 columns with left bar` — 針對類別頁面使用左側邊欄的雙欄配置。
   - `2 columns with right bar` — 針對類別頁面使用右側具側欄的雙欄版面配置。
   - `3 columns` — 對類別頁面使用左右兩側有側欄的三欄式配置。

   啟用[頁面產生器](../page-builder/introduction.md)時，會有其他可用的完整寬度選項。 接著，您可以使用頁面產生器內容工具，設計類別頁面的版面。

   - `Page -- Full Width` — 使用類別頁面的&#x200B;_頁面 — 全寬_&#x200B;配置。
   - `Category -- Full Width` - （建議使用）類別頁面使用&#x200B;_類別 — 完整寬度_&#x200B;配置。
   - `Product -- Full Width` — 使用類別頁面的&#x200B;_產品 — 全寬_&#x200B;配置。

1. 選擇您要用於CMS頁面的&#x200B;**[!UICONTROL Default Page Layout]**。

   此設定決定了CMS頁面預設使用的版面。

   - `No layout updates` - CMS頁面無法使用版面更新。
   - `Empty` — 針對CMS頁面使用空白版面。
   - `1 column` — 針對CMS頁面使用單一欄配置。
   - `2 columns with left bar` — 針對CMS頁面使用左側邊欄的雙欄配置。
   - `2 columns with right bar` — 針對CMS頁面使用右側具側欄的雙欄配置。
   - `3 columns` — 針對CMS頁面使用左右兩側有側欄的三欄式配置。

   啟用[頁面產生器](../page-builder/introduction.md)時，會有其他可用的完整寬度選項。 然後您可以使用頁面產生器內容工具來設計CMS頁面的版面。

   - `Page -- Full Width` - （建議）使用CMS頁面的&#x200B;_頁面 — 完整寬度_&#x200B;配置。
   - `Category - Full Width` — 使用CMS頁面的&#x200B;_類別 — 完整寬度_&#x200B;配置。
   - `Product - Full Width` — 使用CMS頁面的&#x200B;_Product — 全寬_&#x200B;配置。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

## 標準版面配置

### 一欄

![圖表 — 一欄式配置](./assets/layout-1-col-th.png){zoomable="yes"}

_[!UICONTROL 1 Column]_版面配置可用來建立具有大型影像或焦點的戲劇化首頁。 這也非常適合用於登入頁面，或包含文字、影像和視訊組合的任何其他頁面。

### 兩欄（含左列）

![圖表 — 雙欄式配置，左邊列](./assets/layout-2-col-lft-bar-th.png){zoomable="yes"}

_[!UICONTROL 2 Columns with Left Bar]_配置通常用於左側導覽的頁面，例如目錄或具有階層式導覽的搜尋結果頁面。 對於需要在左側額外導覽或支援內容區塊的首頁，這也是絕佳選擇。

### 兩欄（含右列）

![圖表 — 右橫條的雙欄式配置](./assets/layout-2-col-rt-bar-th.png){zoomable="yes"}

使用&#x200B;_[!UICONTROL 2 Columns with Right Bar]_版面配置時，主要內容區域已足夠大，足以呈現吸引人的影像或橫幅。 此版面通常也用於右側具有支援內容區塊的產品頁面。

### 三欄

![圖表 — 三欄式配置](./assets/layout-3-col-th.png){zoomable="yes"}

_[!UICONTROL 3 Column]_版面配置有一個中心欄，其寬度足以容納頁面的主要文字，兩側都有空間可額外導覽及支援內容的區塊。

### 空白

![圖表 — 空的配置](./assets/layout-blank-th.png){zoomable="yes"}

_[!UICONTROL Empty]_配置可用來定義自訂頁面配置。
