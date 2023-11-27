---
title: 版面更新
description: 瞭解如何使用版面更新來自訂頁面版面。
exl-id: e2d8261f-cae1-4bd4-a047-f861dd7ca14e
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '1007'
ht-degree: 0%

---

# 版面更新

開始使用自訂版面更新之前，請務必瞭解商店頁面的建構方式以及字詞之間的差異 *版面* 和 *版面更新*. 版面配置是指頁面的視覺和結構組成。 版面配置更新是指一組特定的XML指示，這些指示可以覆寫或自訂頁面的建構方式。

您的XML配置 [!DNL Commerce] 存放區是容器和區塊的階層結構。 有些元素會出現在每個頁面上，有些則只會出現在特定頁面上。 若要進一步瞭解版面、容器和區塊，請參閱 [版面概觀](https://developer.adobe.com/commerce/frontend-core/guide/layouts/) 在 _前端開發人員指南_.

此 [Widget](widgets.md) 工具是新增現有專案的簡單方法 [內容區塊](blocks.md) 至頁面的預設版面。 如需更進階的更新，您必須將XML配置更新程式碼儲存在伺服器上，然後以自訂配置更新的形式參照檔案。 如需程式概述，請參閱 [使用版面更新](layout-updates.md#place-a-block-using-layout-updates).

下圖中，參照容器的名稱為黑色，而區塊型別（或區塊類別路徑）為藍色。

![標準區塊配置圖](./assets/page-layout-default.png){width="500" zoomable="yes"}

| 區塊型別 | 說明 |
|--- |--- |
| `page/html` | 此區塊的名稱為 `root` 而且是版面配置中少數的根區塊之一。 您也可以建立自己的區塊並為其命名 `root`，此為此類區塊的標準名稱。 每頁只能有一個此型別的區塊。 |
| `page/html_head` | 區塊名稱為 `head` 而且是根區塊的子項。 每個頁面只能有一個此型別的區塊，且不得移除。 |
| `page/html_notices` | 區塊名稱為 `global_notices` 而且是根區塊的子項。 如果從版面配置中移除此區塊，全域通知不會顯示在頁面上。 每頁只能有一個此型別的區塊。 |
| `page/html_header` | 區塊名稱為 `header` 而且是根區塊的子項。 此區塊對應至頁面頂端的視覺化標頭，並包含數個標準區塊。 每個頁面只能有一個此型別的區塊，且不得移除。 |
| `page/html_wrapper` | 雖然此區塊包含在預設版面中，但已遭取代，僅為了確保回溯相容性包含此區塊。 請勿使用此型別的區塊。 |
| `page/html_breadcrumbs` | 此區塊的名稱為 `breadcrumbs` 而且是標頭區塊的子項。 此區塊會顯示目前頁面的階層連結。 每頁只能有一個此型別的區塊。 |
| `page/html_footer` | 區塊名稱為 `footer` 而且是根區塊的子項。 頁尾區塊對應至頁面底部的視覺頁尾，並包含數個標準區塊。 每個頁面只能有一個此型別的區塊，且不得移除。 |
| `page/template_links` | 標準版面配置中有兩種此型別的區塊。 此 `top.links` 區塊是標題區塊的子項，與頂端導覽功能表相對應。 此 `footer_links` 區塊是頁尾區塊的子項，與底部導覽功能表相對應。 <br/><br/>**_注意：_**您可以操控範本連結，如範例所示。 |
| `page/switch` | 在標準版面配置中，此型別有兩個區塊。 此 `store_language` 區塊是標頭區塊的子項，並對應至上層語言切換器。 此 `store_switcher` 區塊是頁尾區塊的子項，與底部存放區切換器相對應。 |
| 核心/訊息 | 在標準版面配置中，此型別有兩個區塊。 此 `global_messages` 區塊會顯示全域訊息。 此 `messages` 區塊用於顯示所有其他訊息。 如果您移除這些區塊，客戶看不到任何訊息。 |
| `core/text_list` | 此型別的區塊在整個中廣為使用 [!DNL Commerce] 做為呈現子區塊的預留位置。 |
| `core/profiler` | 每頁只有一個這種區塊型別的執行個體。 它用於內部 [!DNL Commerce] 效能評測器，且不可用於任何其他目的。 |

{style="table-layout:auto"}

## 使用版面配置更新置入區塊

[版面更新](layout-updates.md) 可以自訂頁面的版面。 版面更新提供比 [Widget](widgets.md)，但需要存取伺服器並具備XML的基本知識。

下列步驟說明如何使用版面配置更新在頁面上放置區塊。 如需語法的特定範例和說明，請參閱 [常見版面自訂任務](https://developer.adobe.com/commerce/frontend-core/guide/layouts/) 在 _前端開發人員指南_.

### 步驟1：建立區塊

1. 建立 [區塊](block-add.md) 要放置的位置。

1. 記下 `block_id`，因為它用於版面配置更新指示中。

### 步驟2：以XML撰寫版面更新

1. 以XML撰寫版面配置指示至 [參考CMS區塊](https://developer.adobe.com/commerce/frontend-core/guide/layouts/xml-manage/).

1. 儲存 [配置指示](https://developer.adobe.com/commerce/frontend-core/guide/layouts/xml-instructions/) 在伺服器上為主題儲存XML檔案的佈局資料夾中。

   例如：

   `<theme_dir>/<Namespace>_<Module>/layout`

   配置控制代碼是開頭為的檔案名稱 `cms_page_view_selectable_`，然後是CMS頁面的URL鍵、版面更新選項以及 `xml` 檔案字尾。 在以下範例中， `customer-service` 是頁面的URL索引鍵，以及 `ChatTool` 是您選取將版面配置更新套用至頁面的選項。

   `cms_page_view_selectable_`&lt;`customer-service`>`_`&lt;`ChatTool`>`.xml`

   | 元素 | 說明 |
   |--- |--- |
   | CMS頁面識別碼 | 包含任何正斜線(`/`)取代為底線(`_`)。 |
   | 版面配置更新名稱 | 針對以下專案顯示的選項 _自訂配置更新_. |

   {style="table-layout:auto"}

### 步驟3：從頁面參考版面更新

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. 尋找您要放置區塊的頁面，並以編輯模式開啟該頁面。

1. 向下捲動並展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Design]** 區段。

1. 若要顯示與頁面相關聯的所有可用版面更新，請按一下 **[!UICONTROL Custom Layout Update]** 功能表。

   ![自訂配置更新清單](./assets/page-design-custom-layout-update.png){width="400" zoomable="yes"}

1. 選取您要套用至頁面的版面配置更新。

### 步驟4：儲存並重新整理快取

1. 完成後，按一下 **[!UICONTROL Save & Close]**.

1. 在工作區頂端的訊息中，按一下 **[!UICONTROL Cache Management]** 並重新整理所有無效的快取專案。
