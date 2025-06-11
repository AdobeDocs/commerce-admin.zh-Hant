---
title: 版面更新
description: 瞭解如何使用版面更新來自訂頁面版面。
exl-id: e2d8261f-cae1-4bd4-a047-f861dd7ca14e
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '1006'
ht-degree: 0%

---

# 版面更新

開始使用自訂配置更新之前，請務必瞭解商店的頁面建構方式，以及術語&#x200B;*配置*&#x200B;和&#x200B;*配置更新*&#x200B;之間的差異。 版面配置是指頁面的視覺和結構組成。 版面配置更新是指一組特定的XML指示，這些指示可以覆寫或自訂頁面的建構方式。

[!DNL Commerce]存放區的XML配置是容器和區塊的階層結構。 有些元素會出現在每個頁面上，有些則只會出現在特定頁面上。 若要深入瞭解配置、容器和區塊，請參閱&#x200B;_前端開發人員指南_&#x200B;中的[配置概觀](https://developer.adobe.com/commerce/frontend-core/guide/layouts/)。

使用[Widget](widgets.md)工具可輕鬆將現有的[內容區塊](blocks.md)新增至頁面的預設版面配置。 如需更進階的更新，您必須將XML配置更新程式碼儲存在伺服器上，然後以自訂配置更新的形式參照檔案。 如需程式概述，請參閱[使用配置更新](layout-updates.md#place-a-block-using-layout-updates)。

下圖中，參照容器的名稱為黑色，而區塊型別（或區塊類別路徑）為藍色。

![標準區塊配置圖](./assets/page-layout-default.png){width="500" zoomable="yes"}

| 區塊型別 | 說明 |
|--- |--- |
| `page/html` | 此區塊的名稱為`root`，是配置中少數幾個根區塊之一。 您也可以建立自己的區塊，並將其命名為`root`，這是此型別區塊的標準名稱。 每頁只能有一個此型別的區塊。 |
| `page/html_head` | 區塊名稱為`head`，是根區塊的子系。 每個頁面只能有一個此型別的區塊，且不得移除。 |
| `page/html_notices` | 區塊名稱為`global_notices`，是根區塊的子系。 如果從版面配置中移除此區塊，全域通知不會顯示在頁面上。 每頁只能有一個此型別的區塊。 |
| `page/html_header` | 區塊名稱為`header`，是根區塊的子系。 此區塊對應至頁面頂端的視覺化標頭，並包含數個標準區塊。 每個頁面只能有一個此型別的區塊，且不得移除。 |
| `page/html_wrapper` | 雖然此區塊包含在預設版面中，但已遭取代，僅為了確保回溯相容性包含此區塊。 請勿使用此型別的區塊。 |
| `page/html_breadcrumbs` | 此區塊的名稱為`breadcrumbs`，而且是標頭區塊的子系。 此區塊會顯示目前頁面的階層連結。 每頁只能有一個此型別的區塊。 |
| `page/html_footer` | 區塊名稱為`footer`，是根區塊的子系。 頁尾區塊對應至頁面底部的視覺頁尾，並包含數個標準區塊。 每個頁面只能有一個此型別的區塊，且不得移除。 |
| `page/template_links` | 標準版面配置中有兩種此型別的區塊。 `top.links`區塊是標頭區塊的子項，且與頂端導覽功能表相對應。 `footer_links`區塊是頁尾區塊的子項，且與底部導覽功能表相對應。 <br/><br/>**_注意：_**可以操縱範本連結，如範例所示。 |
| `page/switch` | 在標準版面配置中，此型別有兩個區塊。 `store_language`區塊是標頭區塊的子項，且與頂端語言切換器相對應。 `store_switcher`區塊是頁尾區塊的子項，且與底部存放區切換器相對應。 |
| 核心/訊息 | 在標準版面配置中，此型別有兩個區塊。 `global_messages`區塊會顯示全域訊息。 `messages`區塊是用來顯示所有其他訊息。 如果您移除這些區塊，客戶看不到任何訊息。 |
| `core/text_list` | 此型別的區塊在整個[!DNL Commerce]中廣泛用作呈現子區塊的預留位置。 |
| `core/profiler` | 每頁只有一個這種區塊型別的執行個體。 它用於內部[!DNL Commerce]分析工具，不應該用於任何其他目的。 |

{style="table-layout:auto"}

## 使用版面配置更新置入區塊

[版面配置更新](layout-updates.md)可以自訂頁面的版面。 版面配置更新提供比[介面工具](widgets.md)更多的彈性，但需要存取伺服器並具備XML的基本知識。

下列步驟說明如何使用版面配置更新在頁面上放置區塊。 如需特定範例和語法說明，請參閱&#x200B;_前端開發人員指南_&#x200B;中的[一般版面自訂工作](https://developer.adobe.com/commerce/frontend-core/guide/layouts/)。

### 步驟1：建立區塊

1. 建立您要放置的[區塊](block-add.md)。

1. 記下`block_id`，因為它用於配置更新指示中。

### 步驟2：以XML撰寫版面更新

1. 以XML撰寫配置指示以[參考CMS區塊](https://developer.adobe.com/commerce/frontend-core/guide/layouts/xml-manage/)。

1. 將[配置指示](https://developer.adobe.com/commerce/frontend-core/guide/layouts/xml-instructions/)儲存在伺服器上的配置資料夾中，其中儲存主題的XML檔案。

   例如：

   `<theme_dir>/<Namespace>_<Module>/layout`

   配置控制代碼是以`cms_page_view_selectable_`開頭的檔案名稱，後面接著CMS頁面的URL索引鍵、配置更新選項和`xml`檔案字尾。 在下列範例中，`customer-service`是頁面的URL索引鍵，`ChatTool`是您選取將版面配置更新套用至頁面的選項。

   `cms_page_view_selectable_`&lt;`customer-service`>`_`&lt;`ChatTool`>`.xml`

   | 元素 | 說明 |
   |--- |--- |
   | CMS頁面識別碼 | 具有任何正斜線(`/`)的頁面的URL索引鍵會以底線(`_`)取代。 |
   | 版面配置更新名稱 | 為&#x200B;_自訂配置更新_&#x200B;顯示的選項。 |

   {style="table-layout:auto"}

### 步驟3：從頁面參考版面更新

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**。

1. 尋找您要放置區塊的頁面，並以編輯模式開啟該頁面。

1. 向下捲動並展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Design]**&#x200B;區段。

1. 若要顯示與頁面相關聯的所有可用版面配置更新，請按一下&#x200B;**[!UICONTROL Custom Layout Update]**&#x200B;功能表。

   ![自訂配置更新清單](./assets/page-design-custom-layout-update.png){width="400" zoomable="yes"}

1. 選取您要套用至頁面的版面配置更新。

### 步驟4：儲存並重新整理快取

1. 完成時，按一下&#x200B;**[!UICONTROL Save & Close]**。

1. 在工作區頂端的郵件中，按一下&#x200B;**[!UICONTROL Cache Management]**&#x200B;並重新整理所有無效的快取專案。
