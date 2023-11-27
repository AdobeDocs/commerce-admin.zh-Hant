---
title: 頁面階層
description: 瞭解頁面階層系統如何讓您組織內容頁面，以及新增分頁、導覽和功能表。
exl-id: 2ce79b85-1420-4640-a4f7-0143a608a71a
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '931'
ht-degree: 0%

---

# 頁面階層

{{ee-feature}}

商店頁面階層系統可讓您組織內容頁面，以及新增分頁、導覽和功能表。 範例資料中的「隱私權原則」頁面是左側有功能表的頁面的範例。 如果您定期發佈大量內容，可使用頁面階層來組織您的內容，讓他人輕鬆找到感興趣的文章。

頁面階層系統使用節點來識別內容的相關片段，並將內容頁面組織成父/子關係。 父節點就像資料夾，其中可能包含子節點和頁面。 階層中每個節點和頁面的相對位置會顯示為 _樹_ 結構。 節點可能包含其他節點和內容頁面，而單一內容頁面可能和父/子或芳鄰關係中的多個節點和其他內容頁面相關聯。

![具左側導覽的頁面](./assets/storefront-privacy-policy.png){width="600" zoomable="yes"}

## 設定頁面階層

組態設定會啟動頁面階層系統和中繼資料，並決定預設功能表配置。

![CMS頁面階層](./assets/content-management-cms-page-hierarchy.png){width="600" zoomable="yes"}

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中的 _[!UICONTROL General]_，選擇&#x200B;**[!UICONTROL Content Management]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) **[!UICONTROL CMS Page Hierarchy]**  並進行任何必要的變更。

1. 完成後，按一下 **[!UICONTROL Save Config]**.

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Enable Hierarchy Functionality] | 為您的內容頁面啟用頁面階層。 選項： `Yes` / `No` |
| [!UICONTROL Enable Hierarchy Metadata] | 啟用此選項後，您可以將中繼資料與階層中的頁面建立關聯。 選項： `Yes` / `No` |
| [!UICONTROL Default Layout for Hierarchy Menu] | 決定預設選單樣式。 選項： `Content` / `Left Column` / `Right Column` |

{style="table-layout:auto"}

## 新增階層節點

下列範例說明如何建立節點，並透過簡單導覽至相關內容頁面。 雖然節點沒有關聯的內容頁面，但它的確有URL金鑰，可在網站的其他位置參照。

例如，您可以建立一個名為 _新聞稿_ 可瀏覽至個別新聞稿。 之後，您便可以將連結加入您的 _關於我們_ 頁面移至節點。 或者，您可以為新聞稿的舊版集合建立一個節點。

若要連結至節點，請使用 [Widget](widgets.md) 工具來建立CMS階層節點連結，並將Widget放置在內容區塊或頁面中。

![關於我們頁面上的導覽選單範例](./assets/page-navigation-storefront.png){width="600" zoomable="yes"}

### 步驟1：建立節點

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Hierarchy]**.

   ![CMS頁面格線](./assets/page-hierarchy-cms-pages.png){width="600" zoomable="yes"}

1. 在格線上方，按一下 **[!UICONTROL Add Node...]**.

1. 在 _[!UICONTROL Page Properties]_，輸入&#x200B;**[!UICONTROL Title]**適用於節點和適當的&#x200B;**[!UICONTROL URL Key]**.

   URL索引鍵會提供節點的唯一網址。 必須全部為小寫字元，使用連字型大小來分隔單字，而非空格。

   ![頁面屬性](./assets/page-hierarchy-add-node-page-properties.png){width="500" zoomable="yes"}

1. 按一下 **[!UICONTROL Save]**.

   節點會在頁面左側的樹狀結構中顯示為資料夾。

### 步驟2：將頁面新增至節點

1. 在階層樹狀結構中，按一下以選取節點。

1. 按一下 **[!UICONTROL Add Selected Pages(s) to Tree]**.

   您可以向上捲動，檢視每個選取的頁面是否出現在節點資料夾下方的樹狀結構中。

### 步驟3：定義結構

1. 如有必要，請將頁面拖曳至適當位置，以反映它們在功能表中出現的順序。

   ![將頁面拖曳至適當位置](./assets/page-hierarchy-drag-to-position.png){width="500" zoomable="yes"}

1. 按一下階層頂端的節點。

   此 _[!UICONTROL Page Properties]_區段現在會顯示有關節點的資訊。

1. 在 **[!UICONTROL Render Metadata in HTML Head]**，請執行下列動作：

   ![演算中繼資料設定](./assets/page-hierarchy-render-metadata.png){width="400" zoomable="yes"}

   - 若要將節點識別為階層的頂端，請設定 **[!UICONTROL First]** 至 `Yes`.

   - 若要顯示分頁控制項，請設定 **[!UICONTROL Next/Previous]** 至 `Yes`.

   - 若要將階層中的頁面組織為報表簿，請設定 **[!UICONTROL Enable Chapter/Section]** 至 `Yes`.

     如果您不想要將節點包含在報表簿中，請保留預設值 `No`.

   - 若要將節點指派給書冊的特定部分，請設定 **[!UICONTROL Chapter/Section]** 變更為下列其中一項：

      - `No`  — 不會將節點定義為章節/區段。
      - `Chapter`  — 將目前節點指派為章節。
      - `Section`  — 將目前節點指派為區段。
      - `Both`  — 將目前節點同時指派為章節和區段。

### 步驟4：新增分頁控制項

1. 在 _巢狀頁面的分頁選項_，設定 **[!UICONTROL Enable Pagination]** 至 `Yes`.

1. 的 **[!UICONTROL Frame]**，輸入分頁控制項中要包含的頁面連結數。

   如果階層中有更多頁面可包含在分頁控制項中。

1. 的 **[!UICONTROL Frame Skip]**，輸入您想要針對下一組分頁連結而向前跳過（或向後跳過）的頁數。

### 步驟5：選擇功能表配置

如果要讓節點出現在選單中，請執行下列動作：

1. 在 _頁面導覽功能表選項_，設定 **[!UICONTROL Show in navigation menu]** 至 `Yes`.

   此設定決定是否產生頁面階層的導覽功能表。

   ![頁面導覽功能表選項](./assets/page-hierarchy-page-navigation-menu-options.png){width="300" zoomable="yes"}

1. 若要指定選單相對於內容的位置，請設定 **[!UICONTROL Menu Layout]**：

   - `Content`  — 功能表配置在內容中。
   - `Use Default`  — 使用中指定的功能表樣式 [設定](../configuration-reference/general/content-management.md).
   - `Left Column`  — 功能表會出現在內容的左側。
   - `Right Column`  — 功能表會出現在內容的右側。

1. 若要指定功能表中包含多少細節，請設定 **[!UICONTROL Menu Detalization]** 變更為下列其中一項：

   - `Only Children`  — 僅包含功能表中的子頁面。
   - `Neighbours and Children`  — 包含子頁面和位於階層中相同層級的其他頁面。

1. 若要決定選單的深度，請輸入 **[!UICONTROL Maximal Depth]** 要納入的層級數目上限。

1. 若要格式化功能表，請選擇 **[!UICONTROL List Type]**：

   - `Unordered`  — 功能表選項未編號，無論是否使用專案符號都可以格式化。 未排序清單型別的選項：預設/圓形/磁碟/正方形
   - `Ordered`  — 功能表選項會以數字編號，並可以大寫或小寫格式設定為數字、字母或羅馬數字。

1. 設定 **[!UICONTROL List Style]** 變更為下列其中一項：

   - `Circle`
   - `Disc`
   - `Square`

1. 如果您也想要在導覽功能表中顯示節點，請捲動至 _主要導覽功能表選項_ 並設定 **[!UICONTROL Show in Navigation menu]** 至 `Yes`.

   ![主要導覽功能表選項](./assets/page-hierarchy-main-navigation-menu-options.png){width="250" zoomable="yes"}

1. 按一下 **[!UICONTROL Save]**.
