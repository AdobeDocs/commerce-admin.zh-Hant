---
title: 『[!DNL Page Builder] 逐步解說第3部分：目錄內容
description: 瞭解如何將產品清單新增至 [!DNL Page Builder] 頁面。
exl-id: f2a0dc29-6d8f-4b97-a947-72659c01d0cb
feature: Page Builder, Page Content
source-git-commit: 2299beb6c11af801076d3aff0b026d41b9dbd212
workflow-type: tm+mt
source-wordcount: '1481'
ht-degree: 0%

---

# [!DNL Page Builder] 逐步解說第3部分：目錄內容

此練習示範將產品清單新增至頁面、自訂產品頁面，以及建立可新增 [!DNL Page Builder] 工作區至產品屬性集。

![產品清單](./assets/pb-add-content-products-list.png){width="600" zoomable="yes"}

本練習假設您已完成 [第1部分：簡單頁面](1-simple-page.md) 和 [第2部分：區塊](2-blocks.md)，包括必要條件和下載的範例檔案。 依序依照本練習的三個部分操作。

## 第1部分：新增產品清單

[!DNL Page Builder] 可讓您輕鬆將產品清單新增至「舞台」。 在此範例中，產品清單會直接新增至頁面。

### 步驟1：將產品清單新增至階段

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. 尋找 _簡單頁面_ 您在第一個練習中建立並在第二個練習中修改的內容，然後選取 **[!UICONTROL Edit]** 在 _[!UICONTROL Action]_欄。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Content]** 區段並按一下 **[!UICONTROL Edit with Page Builder]** 或在內容預覽區域內。

1. 在 [!DNL Page Builder] 下的面板 _[!UICONTROL Layout]_，拖曳&#x200B;**[!UICONTROL Row]**到舞台頂端。

1. 在 [!DNL Page Builder] 面板，展開 **[!UICONTROL Add Content]** 並拖曳 **[!UICONTROL Products]** 新列的預留位置。

   ![將產品預留位置拖曳至列](./assets/pb-add-content-products-drag.png){width="600" zoomable="yes"}

### 步驟2：撰寫條件

1. 將滑鼠懸停在空的產品容器上以顯示工具箱，然後選擇 _設定_ ( ![設定圖示](./assets/pb-icon-settings.png){width="20"} )圖示。

   ![產品工具箱](./assets/pb-add-content-products-toolbox.png){width="600" zoomable="yes"}

1. 的 **[!UICONTROL Select Products By]**，選擇 `Condition`.

1. 新增條件：

   - 按一下 _新增_ (![「新增」圖示](../assets/icon-add-green-circle.png))圖示。

   - 在 _[!UICONTROL Product Attribute]_，選擇&#x200B;**[!UICONTROL Category]**.

     ![選擇條件的類別屬性](./assets/pb-add-content-products-settings-condition.png){width="600" zoomable="yes"}

   - 完成 _[!UICONTROL Category is]..._ 按一下更多(...)圖示，然後按一下 _選擇器_ (![選擇器圖示](../assets/icon-list-chooser.png))圖示。

     ![定義條件](./assets/pb-add-content-products-settings-condition-category-is.png){width="600" zoomable="yes"}

   - 在類別樹狀結構中，向下展開至 **女式>上衣** 類別並選取 **T恤** 核取方塊。

     ![在樹狀結構中選取類別](./assets/pb-add-content-products-settings-condition-category-tree.png){width="600" zoomable="yes"}

   - 按一下核取記號(![勾選圖示](../assets/icon-checkmark-green-circle.png))圖示。

     對應的類別ID會顯示在欄位中，以完成條件。

### 步驟3：完成設定

1. 輸入 **[!UICONTROL Number of Products to Display]**.

   依預設，清單會顯示五個產品。

1. 視需要完成其餘的設定。

   如有需要，請使用 [新增內容 — 產品](products.md) 頁面以供參考。

1. 完成後，按一下 **[!UICONTROL Save]** 以儲存設定並返回 [!DNL Page Builder] 工作區。

   ![階段中的產品清單](./assets/pb-add-content-products-list-stage.png){width="600" zoomable="yes"}

1. 在舞台的右上角，按一下 _關閉全熒幕_ ( ![關閉全熒幕圖示](./assets/pb-icon-reduce.png){width="20"} )圖示。

   按一下此圖示會返回 _[!UICONTROL Content]_顯示預覽之頁面的區段。

1. 在右上角，按一下 **[!UICONTROL Save]** 箭頭並選擇 **[!UICONTROL Save & Close]**.

## 第2部分：自訂產品頁面

>[!NOTE]
>
>管理員使用者必須具備 [!UICONTROL Content] 的許可權 [角色範圍](../systems/permissions-user-roles.md) 以檢視 [!UICONTROL Edit with Page Builder] 按鈕的下拉式選單，以及能夠使用頁面產生器的按鈕。

在本練習的這一部分，您將瞭解將影片放在產品頁面的一組索引標籤下方，以自訂產品頁面是多麼容易。 更新的程式 [類別頁面](../catalog/categories-content-settings.md) 內容基本相同。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 尋找可用於此範例的簡單產品，並在編輯模式下開啟它。

1. 向下捲動並展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Content]** 區段。

1. 旁邊 _[!UICONTROL Description]_，按一下&#x200B;**[!UICONTROL Edit with Page Builder]**.

   ![產品說明內容](./assets/pb-catalog-product-content.png){width="600" zoomable="yes"}

   如果之前輸入的產品說明沒有 [!DNL Page Builder]，目前的說明會以HTML形式顯示於 [HTML代碼](html-code.md) 容器。 使用Luma佈景主題時，產品說明會出現在「詳細資訊」標籤上。

1. 在 [!DNL Page Builder] 下的面板 _[!UICONTROL Layout]_，拖曳&#x200B;**[!UICONTROL Row]**放到「舞台」上，將程式碼放到HTML程式碼容器下方。

   當列位於正確位置時，請尋找要顯示的紅色建議。

   ![將列拖曳到舞台](./assets/catalog-product-content-stage-row-drag.png){width="600" zoomable="yes"}

1. 在 [!DNL Page Builder] 面板，展開 **[!UICONTROL Media]** 並拖曳 **[!UICONTROL Video]** 新列的預留位置。

   ![列中的視訊預留位置](./assets/tutorial3-product-drag-video.png){width="600" zoomable="yes"}

1. 將滑鼠懸停在空白的視訊容器上以顯示工具箱，然後選擇 _設定_ ( ![設定圖示](./assets/pb-icon-settings.png){width="20"} )圖示。

   ![視訊工具箱](./assets/pb-tutorial3-product-video-toolbox.png){width="500" zoomable="yes"}

1. 輸入 **[!UICONTROL Video URL]**.

   視訊可以託管在 [YouTube][1] 或 [Vimeo][2]. 此範例中的影片可從YouTube的以下URL找到：

   `https://www.youtube.com/watch?v=ZpFrNyD4100`

   ![編輯視訊](./assets/pb-tutorial3-product-edit-video.png){width="500" zoomable="yes"}

1. 輸入 **[!UICONTROL Maximum Width]** 視訊顯示的畫素。

   如果將此選項保留為空白，視訊會填滿可用空間。

1. 按一下 **[!UICONTROL Save]** 以儲存設定並返回 [!DNL Page Builder] 工作區。

   ![內容階段中的影片](./assets/pb-tutorial3-product-video.png){width="600" zoomable="yes"}

1. 在舞台的右上角，按一下 _關閉全熒幕_ ( ![關閉全熒幕圖示](./assets/pb-icon-reduce.png){width="20"} )圖示。

   按一下此圖示會返回 _[!UICONTROL Content]_顯示預覽之頁面的區段。

1. 在右上角，按一下 **[!UICONTROL Save]** 箭頭並選擇 **[!UICONTROL Save & Close]**.

在店面中，影片會顯示在標籤組的下方。 若要檢視頁面在行動裝置上的外觀，您可以調整視窗大小。

![產品頁面上顯示的影片](./assets/pb-tutorial3-product-video-storefront.png){width="600" zoomable="yes"}

**恭喜！** 您已完成目錄內容教學課程的第二部分。 保留您建立的工作，以便稍後參考。

## 第3部分：新增自訂屬性

使用 [!DNL Page Builder] 自訂屬性以新增完整功能 [!DNL Page Builder] 工作區至產品頁面，您可以用來建立吸引人的內容。 在練習的這部分，您將瞭解如何使用 [!DNL Page Builder] 輸入型別，並將其套用至目錄中的產品頁面。 如需這些屬性的詳細資訊，請參閱 [產品屬性](../catalog/product-attributes.md).

### 步驟1：建立產品

為避免您的即時商店發生變更，請使用所述的屬性建立產品。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 在右上角，按一下 **[!UICONTROL Add Product]**.

1. 建立具有以下屬性的產品：

   - 
     [！UICONTROL屬性集]: Default
   - [!UICONTROL Product Name]：我的產品
   - 
     [!UICONTROL SKU]: Tutorial
   - 
     [!UICONTROL Price]: 75.00
   - 
     [!UICONTROL Quantity]: 100
   - [!UICONTROL Stock Status]：有貨
   - 
     [!UICONTROL Weight]: 1
   - [!UICONTROL Categories]：女性>上衣>T恤

1. 在右上角，按一下 **[!UICONTROL Save]** 箭頭並選擇 **[!UICONTROL Save & Close]**.

### 步驟2：建立自訂屬性

在此步驟中，您將建立兩個新的自訂屬性，以顯示 [!DNL Page Builder] 和文字編輯器輸入型別。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. 在右上角，按一下 **[!UICONTROL Add New Attribute]**.

1. 輸入 **[!UICONTROL Default Label]** 屬性的。

   在此範例中，使用 `My Page Builder Attribute` 以取得標籤。

1. 設定 **[!UICONTROL Catalog Input Type for Store Owner]** 至 `Page Builder`.

   建立自訂屬性時，您可以將最適合應用程式的編輯器指定為 `Page Builder` 或標準WYSIWYG `Text Editor`.

   ![[!DNL Page Builder] 輸入型別](./assets/pb-attribute-page-builder.png){width="600" zoomable="yes"}

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Advanced Attribute Properties]** 並執行下列設定：

   - [!UICONTROL Attribute Code]：以小寫字元輸入屬性代碼，使用連字型大小而非空格。 在此範例中，使用 `my_page_builder_attribute`.
   - [!UICONTROL Scope]：接受預設值， `Store View`.
   - [!UICONTROL Default Value]：輸入屬性的預設值。
   - 
     [!UICONTROL Unique Value]: `No`
   - 
     [!UICONTROL Add to Column Options]: `No`
   - 
     [!UICONTROL Use in Filter Options]: `Yes`

1. 在 _[!UICONTROL Attribute Information]_在左側面板，選擇&#x200B;**[!UICONTROL Storefront Properties]**並進行下列設定：

   - 
     [!UICONTROL Use for Promo Rule Conditions]: `Yes`
   - 
     [!UICONTROL Visible on Catalog Pages on Storefront]: `Yes`
   - 
     [!UICONTROL Used in Product Listing]: `Yes`

1. 完成後，按一下 **[!UICONTROL Save Attribute]**.

1. 重複上述步驟，以建立具有相同基本屬性，但文字編輯器輸入型別的第二個屬性，如下所示：

   - [!UICONTROL Default Label]：我的文字編輯器屬性
   - [!UICONTROL Catalog Input Type for Store Owner]：文字編輯器
   - 
     [！UICONTROL屬性代碼]: `my_text_editor_attribute`

### 步驟3：更新產品屬性集

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

   在此範例中，您會暫時將新屬性新增至 `default` 屬性集。 在本練習結束時，請從屬性集中移除屬性，以免影響您的目錄。

   >[!NOTE]
   >
   >如果您不想要變更您的即時商店，您可以跟著而不更新屬性集。

1. 尋找 _[!UICONTROL Default]_屬性集，並連按兩下以在編輯模式中開啟。

1. 在 _未指派的屬性_ 清單，尋找您建立的新屬性，並將每個屬性拖曳至 _[!UICONTROL Groups]_欄，在&#x200B;**[!UICONTROL Content]**.

   屬性在中的位置 [!UICONTROL Groups] 欄會決定其顯示在頁面上的位置。

   ![新增屬性至內容群組](./assets/pb-product-attribute-set.png){width="600" zoomable="yes"}

1. 按一下 **[!UICONTROL Save]** 以返回「屬性集」清單。

1. 出現提示時，按一下 **[!UICONTROL Cache Management]** 頁面頂端的連結，並重新整理任何無效的快取。

### 步驟4：更新產品

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 在產品格線中，尋找 _我的產品_ 並以編輯模式開啟。

1. 向下捲動並展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Content]** 區段。

   在區段頂端，有兩個產品內容的標準屬性：

   - _簡短說明_，使用標準WYSIWYG [編輯者](../content-design/editor.md).
   - _說明_，會顯示 [!DNL Page Builder] 預覽。

   ![產品內容](./assets/pb-product-content-edit-with-page-builder.png){width="600" zoomable="yes"}

   當您捲動到區段的下半部時，您會建立並指派兩個屬性：

   - _我的 [!DNL Page Builder] 屬性_，會顯示 [!DNL Page Builder] 預覽。
   - _我的文字編輯器屬性_，此編輯器使用標準的WYSIWYG編輯器。

   ![產品內容編輯](./assets/pb-product-content-my-attributes.png){width="600" zoomable="yes"}

1. 在 **我的文字編輯器屬性** 編輯者，輸入 `Text Editor Attribute placeholder text`.

   - 在右上角，按一下 **[!UICONTROL Save]** 箭頭並選擇 **[!UICONTROL Save & Close]**.

1. 的 **我的頁面產生器屬性**，按一下 **[!UICONTROL Edit with Page Builder]** 並新增說明文字：

   - 在 [!DNL Page Builder] 面板，展開 **[!UICONTROL Elements]** 並拖曳 **[!UICONTROL Text object]** 到舞台。

   - 輸入 `Page Builder attribute placeholder text`.

   - 在舞台的右上角，按一下 _關閉全熒幕_ ( ![關閉全熒幕圖示](./assets/pb-icon-reduce.png){width="20"} )圖示。

     ![具有預留位置文字的自訂屬性](./assets/pb-product-content-attributes.png){width="600" zoomable="yes"}

1. 向上捲動至 **[!UICONTROL Description]**，按一下 **[!UICONTROL Edit with Page Builder]**，並使用與上一步相同的方法新增任何您喜歡的文字。

1. 在產品頁面的右上角，按一下 **[!UICONTROL Save]** 箭頭並選擇 **[!UICONTROL Save & Close]**.

1. 如果出現提示，請按一下 **[!UICONTROL Cache Management]** 頁面頂端訊息中的連結，並重新整理任何無效的快取。

### 步驟5：檢視結果

1. 導覽至店面的範例產品頁面。

   在此範例中，產品位於頂端導覽列中的「女性>頂端>T恤」下。

1. 向下捲動至 _我的頁面產生器屬性_ 資訊。

   屬性在產品頁面上的位置由主題決定。 在Luma主題中，新屬性位於產品說明後面。

   ![[!DNL Page Builder] 和店面中的文字編輯器屬性](./assets/pb-storefront-product-attribute.png){width="600" zoomable="yes"}

您已完成 [!DNL Page Builder] 「目錄內容」練習。 保留您建立的工作，以便稍後參考。

[1]: https://www.youtube.com/
[2]: https://vimeo.com/
