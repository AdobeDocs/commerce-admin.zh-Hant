---
title: 頁面配置
description: 瞭解頁面配置區段以及如何設定預設配置。
exl-id: 397a92cf-6f20-4729-8d7c-c5f672fc1c9a
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '871'
ht-degree: 0%

---

# 頁面配置

商店中每個頁面的版面配置都包含定義頁面頁首、頁尾和內容區域的不同區段或容器。 視版面配置而定，每個頁面可能會有一欄、兩欄、三欄或更多欄。 您可以將版面配置想成 _平面圖_ ，並指派特定版面配置以用作CMS、產品和類別頁面的預設值。

在頁面上，內容區塊會根據 [頁面配置](layout-updates.md) 指定其出現的位置。 請注意，如果您將版面配置從三欄變更為兩欄，主區域的內容會展開以填滿可用空間。 另請注意，與未使用側邊列關聯的任何區塊似乎都會消失。 不過，如果您恢復三欄版面配置，區塊會重新出現。 流暢的方法，或 _液體版面配置_，可以變更頁面版面配置而不需重新處理內容。 如果您習慣於使用個別HTML頁面，此模組化 _建置區塊_ 方法需要不同的思考方式。

![標準兩欄，左側條狀頁面配置](./assets/storefront-2-column-ee.png){width="700" zoomable="yes"}

## 設定預設版面

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中的 _[!UICONTROL General]_，選擇&#x200B;**[!UICONTROL Web]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Default Layouts]** 區段。

   ![預設版面](./assets/web-default-layouts.png){width="600" zoomable="yes"}

1. 選擇 **[!UICONTROL Default Product Layout]** 要用於產品頁面的屬性。

   此設定決定預設用於產品頁面的版面。

   - `No layout updates`  — 無法使用產品頁面的版面更新。
   - `Empty`  — 使用產品頁面的空白版面配置。
   - `1 column`  — 針對產品頁面使用單一欄配置。
   - `2 columns with left bar`  — 針對產品頁面，使用左側邊欄的兩欄式配置。
   - `2 columns with right bar`  — 對於產品頁面，使用右側具側欄的雙欄版面配置。
   - `3 columns`  — 針對產品頁面，使用左右兩側有側欄的三欄式配置。

   時間 [頁面產生器](../page-builder/introduction.md) 已啟用，則提供其他完整寬度選項。 然後您可以使用頁面產生器內容工具來設計產品頁面的版面。

   - `Page -- Full Width`  — 使用 _頁面 — 全寬_  產品頁面的配置。
   - `Category -- Full Width`  — 使用 _類別 — 完整寬度_ 產品頁面的配置。
   - `Product -- Full Width` - （建議）使用 _產品 — 全寬_ 產品頁面的配置。

1. 選擇 **[!UICONTROL Default Category Layout]** 要用於類別頁面的設定檔。

   此設定會決定類別頁面預設使用的版面。

   - `No layout updates`  — 配置更新不適用於類別頁面。
   - `Empty`  — 使用空白版面配置來處理類別頁面。
   - `1 column`  — 對類別頁面使用單一欄配置。
   - `2 columns with left bar`  — 針對類別頁面，使用左側邊欄的雙欄版面配置。
   - `2 columns with right bar`  — 針對類別頁面，使用右側具側欄的雙欄版面配置。
   - `3 columns`  — 對類別頁面使用左右兩側有側欄的三欄式配置。

   時間 [頁面產生器](../page-builder/introduction.md) 已啟用，則提供其他完整寬度選項。 接著，您可以使用頁面產生器內容工具，設計類別頁面的版面。

   - `Page -- Full Width`  — 使用 _頁面 — 全寬_ 類別頁面的版面。
   - `Category -- Full Width` - （建議）使用 _類別 — 完整寬度_ 類別頁面的版面。
   - `Product -- Full Width`  — 使用 _產品 — 全寬_ 類別頁面的版面。

1. 選擇 **[!UICONTROL Default Page Layout]** 要用於CMS頁面的物件。

   此設定決定了CMS頁面預設使用的版面。

   - `No layout updates` - CMS頁面無法使用版面更新。
   - `Empty`  — 對CMS頁面使用空白版面。
   - `1 column`  — 對CMS頁面使用單欄配置。
   - `2 columns with left bar`  — 針對CMS頁面，使用具有左側邊欄的雙欄版面。
   - `2 columns with right bar`  — 針對CMS頁面使用帶有右側邊欄的雙欄版面。
   - `3 columns`  — 針對CMS頁面，使用左右兩側有側欄的三欄式配置。

   時間 [頁面產生器](../page-builder/introduction.md) 已啟用，則提供其他完整寬度選項。 然後您可以使用頁面產生器內容工具來設計CMS頁面的版面。

   - `Page -- Full Width` - （建議）使用 _頁面 — 全寬_ CMS頁面的版面。
   - `Category - Full Width`  — 使用 _類別 — 完整寬度_ CMS頁面的版面。
   - `Product - Full Width`  — 使用 _產品 — 全寬_ CMS頁面的版面。

1. 完成後，按一下 **[!UICONTROL Save Config]**.

## 標準版面配置

### 一欄

![圖表 — 一欄式配置](./assets/layout-1-col-th.png){zoomable=&quot;yes&quot;}

此 _[!UICONTROL 1 Column]_版面配置可用來建立具有大型影像或焦點的戲劇化首頁。 這也非常適合用於登入頁面，或包含文字、影像和視訊組合的任何其他頁面。

### 兩欄（含左列）

![圖表 — 雙欄式左條佈局](./assets/layout-2-col-lft-bar-th.png){zoomable=&quot;yes&quot;}

此 _[!UICONTROL 2 Columns with Left Bar]_佈局通常用於左側導覽的頁面，例如具有階層式導覽的目錄或搜尋結果頁面。 對於需要在左側額外導覽或支援內容區塊的首頁，這也是絕佳選擇。

### 兩欄（含右列）

![圖表 — 兩欄式配置，帶右長條](./assets/layout-2-col-rt-bar-th.png){zoomable=&quot;yes&quot;}

使用 _[!UICONTROL 2 Columns with Right Bar]_版面配置中，主要內容區域夠大，足以呈現吸引人的影像或橫幅。 此版面通常也用於右側具有支援內容區塊的產品頁面。

### 三欄

![圖表 — 三欄式配置](./assets/layout-3-col-th.png){zoomable=&quot;yes&quot;}

此 _[!UICONTROL 3 Column]_版面配置有一個中間的欄，其寬度足以容納頁面的主要文字，兩側都有空間可額外導覽及支援內容的區塊。

### 空白

![圖表 — 空版面配置](./assets/layout-blank-th.png){zoomable=&quot;yes&quot;}

此 _[!UICONTROL Empty]_layout可用來定義自訂頁面配置。
