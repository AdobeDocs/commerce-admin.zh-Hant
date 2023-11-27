---
title: 『[!DNL Page Builder] 逐步解說第2部分：區塊
description: 瞭解使用時，簡單區塊和動態區塊之間的差異 [!DNL Page Builder].
exl-id: 864a3078-8cb3-4add-bdb7-14189aba535e
feature: Page Builder, Page Content
source-git-commit: 2299beb6c11af801076d3aff0b026d41b9dbd212
workflow-type: tm+mt
source-wordcount: '2053'
ht-degree: 0%

---

# [!DNL Page Builder] 逐步解說第2部分：區塊

下列練習將說明兩者之間的差異 [簡單區塊](../content-design/blocks.md) 和 [動態區塊](dynamic-block.md)，以及如何使用 [!DNL Page Builder] 以建立每種型別的區塊。

>[!NOTE]
>
>[!DNL Page Builder] 具有名為的新內容型別 _橫幅_，此專案在第一個逐步解說練習中特別顯示，且與先前的橫幅功能無關。 中先前的Banner選項是什麼 [內容功能表](../content-design/content-menu.md)，現在為 _動態區塊_.

![店面中的動態區塊](./assets/pb-tutorial2-dynamic-block-storefront.png){width="700" zoomable="yes"}

本練習假設您已完成 [第1部分：簡單頁面](1-simple-page.md)，包括必要條件和 [下載的範例檔案](./assets/simple-page-assets.zip). 依序依照此逐步解說練習的部分進行。

>[!NOTE]
>
>這些逐步解說練習已更新，以反映最近對 [!DNL Page Builder] 2.4.1版本中的workspace 。 如果您使用舊版Adobe Commerce，請使用 [!DNL Page Builder] 包含在中的練習 [[!DNL Commerce] 2.3使用手冊](https://docs.magento.com/user-guide/v2.3/cms/page-builder-learn.html).

## 第1部分：建立簡單區塊

在這個逐步解說練習中，您會建立一個簡單的區塊，其內容來自 [!DNL Google Maps]. 簡單區塊有時稱為 _CMS區塊_ 或 _靜態區塊_，因為內容不會變更。 簡單區塊適用於您可能想要重複使用的內容。

### 步驟1：建立區塊

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. 在右上角，按一下 **[!UICONTROL Add New Block]**.

1. 的 **[!UICONTROL Block Title]**，輸入 `Google Map`.

1. 的 **[!UICONTROL Identifier]**，輸入 `google-map`.

1. 選擇 **[!UICONTROL Store View]** 區塊可用的位置。

   ![區塊資訊](./assets/pb-tutorial2-block-new-google-map.png){width="600" zoomable="yes"}

1. 在右上角，按一下 **[!UICONTROL Save]**.

### 步驟2：新增 [!DNL Google Map]

1. 向下捲動至 [!DNL Page Builder] 內容預覽（目前空白）並按一下 **[!UICONTROL Edit with Page Builder]**.

1. 在 [!DNL Page Builder] 面板，展開 **[!UICONTROL Media]** 並拖曳 **[!UICONTROL Map]** 舞台的預留位置。

   ![將地圖拖曳到舞台](./assets/pb-media-map-drag.png){width="600" zoomable="yes"}

   如果符合下列條件，則會顯示商店位置的地圖： [!DNL Google Maps] 已針對您的存放區進行設定。

   ![為您的商店設定Google Map](./assets/pb-tutorial2-google-map.png){width="600" zoomable="yes"}

   出現預留位置對應，如果 [!DNL Google Maps] 尚未為您的存放區設定。

   ![[!DNL Google Maps] 預留位置](./assets/pb-tutorial2-media-map-not-configured.png){width="600" zoomable="yes"}

1. 在舞台的右上角，按一下 _關閉全熒幕_ (![關閉全熒幕圖示](./assets/pb-icon-reduce.png))圖示。

   按一下此圖示會返回 _[!UICONTROL Content]_顯示預覽之區塊的區段。

1. 在右上角，按一下 **[!UICONTROL Save]** 箭頭並選擇 **[!UICONTROL Save & Close]**.

### 步驟3：設定 [!DNL Google Maps]

如果 [!DNL Google Maps] 已針對您的商店進行設定，您可以略過此步驟，並繼續下一步。

1. 前往 [Google雲端平台主控台](https://console.cloud.google.com/google/maps-apis/overview).

1. 按一下專案下拉式清單，然後選取或建立您要新增API金鑰的專案。

1. 若要設定您的API認證，請依照 [指示][1] 在 [!DNL Google Maps] 檔案。

1. 將API金鑰複製到剪貼簿。

1. 返回 [!DNL Commerce] 管理並前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中的 _[!UICONTROL General]_，選擇&#x200B;**[!UICONTROL Content Management]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

   ![進階內容工具](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

   如需關於的詳細資訊 [!UICONTROL Content Management Advanced Tools] 組態選項，請參閱 [_設定參考指南_](../configuration-reference/general/content-management.md).

1. 的 **[!UICONTROL Google Maps API Key]**，貼上您複製的金鑰。

1. 按一下 **[!UICONTROL Test Key]**.

   如果您的金鑰發生問題，請返回 [!DNL Google Maps] 平台網站以解決問題。 然後再試一次。

1. 在您的金鑰通過驗證後，按一下 **[!UICONTROL Save Config]**.

### 步驟4：將區塊新增至頁面

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. 在格線中，尋找 _[!UICONTROL Simple Page]_您在第一個教學課程中建立並選取&#x200B;**[!UICONTROL Edit]**在_[!UICONTROL Action]_ 欄。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Content]** 區段並按一下 **[!UICONTROL Edit with Page Builder]** 或在內容預覽區域內。

1. 在 [!DNL Page Builder] 下的面板 _[!UICONTROL Layout]_，拖曳&#x200B;**[!UICONTROL Row]**舞台頂端的預留位置。

   ![將列新增至舞台頂端](./assets/pb-tutorial2-elements-row-drag-top.png){width="600" zoomable="yes"}

1. 在 [!DNL Page Builder] 面板，展開 **[!UICONTROL Add Content]** 並拖曳 **[!UICONTROL Block]** 新列的預留位置。

1. 將滑鼠懸停在空白的區塊容器上以顯示工具箱，然後選擇 _設定_ (![設定圖示](./assets/pb-icon-settings.png){width="20"} )圖示。

   ![區塊工具箱](./assets/pb-add-content-block-toolbox.png){width="600" zoomable="yes"}

1. 在編輯區塊頁面上，按一下 **[!UICONTROL Select Block]**.

   ![選取區塊](./assets/pb-add-content-block-settings-block-select.png){width="600" zoomable="yes"}

1. 在搜尋方塊中，輸入 `map` 並按Enter/Return鍵以尋找您建立的區塊。

   ![在清單中尋找區塊](./assets/pb-add-content-block-settings-block-find.png){width="600" zoomable="yes"}

1. 在格線中，按一下 **[!UICONTROL Select]** 以選擇 [!DNL Google Maps] 區塊。

1. 在右上角，按一下 **[!UICONTROL Save]** 以儲存設定並返回 [!DNL Page Builder] 工作區。

1. 在舞台的右上角，按一下 _關閉全熒幕_ (![關閉全熒幕圖示](./assets/pb-icon-reduce.png))圖示。

   按一下此圖示會返回 _[!UICONTROL Content]_顯示預覽之頁面的區段。

1. 在右上角，按一下 **[!UICONTROL Save]** 箭頭並選擇 **[!UICONTROL Save & Close]**.

**恭喜！** 您已完成「區塊」練習的第一部分。 請務必保留您的工作以作參考。

## 第2部分：建立動態區塊

動態區塊所包含的邏輯會判斷區塊出現的位置、時間以及對象。 在此逐步解說練習中，您可以針對符合價格規則條件時所觸發的促銷，建立動態區塊，此區塊只會顯示給特定客戶區段。 此範例的結果類似於第一個練習中建立的橫幅，但有邏輯控制其出現在店面中的時間。

![Luma Tee促銷活動範例](./assets/pb-tutorial2-dynamic-block-row-page.png){width="600" zoomable="yes"}

### 步驟1：建立新的動態區塊

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

   ![動態區塊清單](./assets/pb-tutorial2-block-dynamic-add.png){width="700" zoomable="yes"}

1. 在右上角，按一下 **[!UICONTROL Add Dynamic Block]**.

   ![新增動態區塊頁面](./assets/pb-tutorial2-block-dynamic-new.png){width="600" zoomable="yes"}

1. 完成新動態區塊的基本設定：

   - 設定 **[!UICONTROL Enable Dynamic Block]** 至 `Yes`.

   - 的 **[!UICONTROL Dynamic Block Name]**，輸入 `Tee Shirt Promo`.

   - 設定 **[!UICONTROL Dynamic Block Type]** 至 `Content Area` 並按一下 **[!UICONTROL Done]**.

     動態區塊型別決定了 [頁面配置](../content-design/page-layout.md) 區塊已放置的位置。 為商店設定動態區塊時，請考慮頁面配置和 [主題](../content-design/themes.md)，讓您可以善用可用空間。 有些存放區具有限定為固定寬度的作用中內容區域，有些則延伸熒幕的完整寬度。

     ![動態區塊型別設定](./assets/pb-dynamic-block-type.png){width="600" zoomable="yes"}

   - 的 **[!UICONTROL Customer Segment]**，勾選您要套用至動態區塊之每個區段的核取方塊，然後按一下 **完成** 以儲存區段清單。

     在下列範例中，有兩種 [客戶區段](../customers/customer-segments.md) 依性別識別註冊客戶的服務。 此動態區塊僅會顯示在註冊女性客戶在您的商店購物時登入其帳戶中。

     ![選擇客戶區段](./assets/pb-dynamic-block-customer-segment.png){width="600" zoomable="yes"}

### 步驟2：完成設定

向下捲動至 _[!UICONTROL Content]_區段，顯示空白 [!DNL Page Builder] 內容預覽，然後按一下&#x200B;**[!UICONTROL Edit with Page Builder]**. 接著，完成下列作業：

**工作1：** 新增背景影像

1. 將滑鼠懸停在列容器上以顯示工具箱，然後選擇 _設定_ (![設定圖示](./assets/pb-icon-settings.png){width="20"} )圖示。

1. 在 _[!UICONTROL Appearance]_，選擇&#x200B;**[!UICONTROL Full Bleed]**.

1. 的 **[!UICONTROL Minimum Height]**，輸入 `400px`.

1. 捲動至 _[!UICONTROL Background]_區段並設定&#x200B;**[!UICONTROL Background Image]**按一下&#x200B;**[!UICONTROL Select from Gallery]**並選取 `wide-banner-background.png` 已在第一個教學課程中上傳影像。

1. 在右上角，按一下 **[!UICONTROL Save]** 以套用設定並返回 [!DNL Page Builder] 工作區。

   ![含有影像的列](./assets/pb-tutorial2-row-image.png){width="600" zoomable="yes"}

**工作2：** 新增欄

在 [!DNL Page Builder] 下的面板 _[!UICONTROL Layout]_，拖曳&#x200B;**[!UICONTROL Column]**列上的預留位置。

![將欄型別拖曳到列](./assets/pb-tutorial2-column-drag.png){width="600" zoomable="yes"}

該列現在分成兩個寬度相等的欄。

**工作3：** 新增文字

1. 在 [!DNL Page Builder] 面板，展開 **[!UICONTROL Elements]** 並拖曳 **文字** 第二欄的預留位置。

   ![將文字方塊拖曳到第二欄](./assets/pb-tutorial2-column-text-drag.png){width="600" zoomable="yes"}

1. 在編輯器中輸入下列三行文字：

   `Even more ways to mix and match.`

   `Buy 3 Luma tees and get a 4th free.`

   `Shop Tees >`

   ![輸入欄文字](./assets/pb-tutorial2-column-text-editor.png){width="600" zoomable="yes"}

1. 選取全部三行文字，並使用工具列設定 **行高** 至 `40px`.

   ![設定行高](./assets/pb-tutorial2-column-text-editor-line-height.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Font Size]** 每行如下：

   | 折線圖 | 字型大小 |
   |-----| ---------- |
   | 第1行： | `28px` |
   | 第2行： | `24px` |
   | 第3行： | `18px` |

   由於此區塊可放置在頁面上的任何位置，因此請使用預設的段落樣式，而不是標題層級。 此外，也無須擔心欄中的文字尚未正確換行。  

   ![格式化文字](./assets/pb-tutorial2-column-text-editor-text-formatted.png){width="600" zoomable="yes"}

**工作4：** 新增連結

在第一個練習中，您已瞭解如何使用 [按鈕](buttons.md) 內容型別以建立連結。 此範例說明如何從編輯器工具列插入連結。

1. 在另一個瀏覽器標籤中，開啟店面並導覽至將成為連結目標目的地的頁面。

   您可以使用完整限定的URL或省略商店網域參照的相對URL。

   完整URL ： `https://mystore.com/women/tops-women/tees-women.html`

   相對URL ： `../women/tops-women/tees-women.html`

1. 返回 [!DNL Page Builder] 工作區索引標籤和文字編輯器，選取 `Shop Tees >` 在第三行輸入文字，然後選擇 **粗體** (![粗體按鈕](./assets/editor-btn-bold.png))時，退出該頁面。

1. 使用 `Shop Tees >` 在第三行仍被選取的文字，選擇 **插入/編輯連結** (![插入/編輯連結按鈕](./assets/pb-icon-add-link.png))時，退出該頁面。

   ![插入連結](./assets/pb-tutorial2-column-text-editor-link-insert.png){width="600" zoomable="yes"}

1. 的 **[!UICONTROL URL]**，輸入您準備的相對連結。

1. 設定 **[!UICONTROL Target]** 至 `None`.

   此設定會在相同的瀏覽器視窗中開啟頁面，而非開啟新標籤。

1. 的 **[!UICONTROL Title]**，輸入 `Shop Tees`.

   有些瀏覽器會將「標題」連結屬性當做工具提示使用。

1. 若要儲存連結並返回 [!DNL Page Builder] 工作區，按一下 **[!UICONTROL OK]**.

   ![連結詳細資料](./assets/pb-tutorial2-column-text-editor-link-insert-detail.png){width="600" zoomable="yes"}

1. 在舞台的右上角，按一下 _關閉全熒幕_ (![關閉全熒幕圖示](./assets/pb-icon-reduce.png))圖示。

   按一下此圖示會返回 _[!UICONTROL Content]_顯示預覽的動態區塊的區段。

1. 在右上角，按一下 **[!UICONTROL Save]**.

### 步驟3：新增價格規則

1. 開啟 _T恤促銷_ 再次在編輯模式下編輯動態區塊。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Related Promotions]** 區段並按一下 **[!UICONTROL Add Cart Price Rules]**.

   ![相關促銷活動](./assets/pb-dynamic-blocks-related-promotions.png){width="600" zoomable="yes"}

1. 在 _新增相關的購物車價格規則_ 頁面上，勾選的核取方塊 _購買3件T恤並免費購買4件_ 價格規則與點按 **[!UICONTROL Add Selected]**.

   ![新增相關的購物車價格規則](./assets/pb-dynamic-block-add-related-cart-price-rules.png){width="600" zoomable="yes"}

   價格規則會顯示在 _相關促銷活動_ 區段，在 _相關購物車價格規則_. 您可以將多個價格規則與動態區塊產生關聯。 不過，這個簡單的範例只使用一個。

   ![選取的購物車價格規則](./assets/pb-dynamic-block-related-cart-price-rule-list.png){width="600" zoomable="yes"}

1. 在右上角，按一下 **[!UICONTROL Save]**.

### 步驟4：將動態區塊新增至頁面

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**

1. 尋找 _簡單頁面_ 您建立於 [第一次逐步解說練習](1-simple-page.md) 並以編輯模式開啟。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Content]** 區段並按一下 **[!UICONTROL Edit with Page Builder]**.

1. 將滑鼠停留在頂端列（與動態區塊有相同的影像），以顯示工具箱和 _移除_ ( ![移除圖示](./assets/pb-icon-remove.png){width="20"} )圖示。

   若要確認從頁面中移除該列，請按一下  **[!UICONTROL OK]** .

1. 在 [!DNL Page Builder] 下的面板 _[!UICONTROL Layout]_，拖曳新的&#x200B;**[!UICONTROL Row]**舞台頂端的預留位置。

1. 在 [!DNL Page Builder] 面板，展開 **[!UICONTROL Add Content]** 並拖曳 **[!UICONTROL Dynamic Block]** 新列的預留位置。

   ![將動態區塊拖曳至列](./assets/pb-dynamic-block-drag.png){width="600" zoomable="yes"}

1. 將游標停留在動態區塊容器上以顯示工具箱，然後選擇 _設定_ ( ![設定圖示](./assets/pb-icon-settings.png){width="20"} )圖示。

   ![動態區塊工具箱](./assets/pb-dynamic-block-settings.png){width="600" zoomable="yes"}

1. 在 _[!UICONTROL Edit Dynamic Block]_頁面，按一下&#x200B;**[!UICONTROL Select Dynamic Block]**.

   ![選取動態區塊](./assets/pb-dynamic-block-select.png){width="600" zoomable="yes"}

1. 尋找 _[!DNL Tee Shirt Promo]_您建立並按一下「 」的動態區塊&#x200B;**[!UICONTROL Select]**.

   動態區塊資訊的摘要會顯示於下方。

   ![動態區塊資訊](./assets/pb-tutorial2-dynamic-block-edit.png){width="600" zoomable="yes"}

1. 接受預設值 **[!UICONTROL Template]**， `Dynamic Block Block Template`.

1. 完成後，按一下 **[!UICONTROL Save]** 以儲存設定並返回 [!DNL Page Builder] 工作區。

   ![頁面預覽中的動態區塊](./assets/pb-tutorial2-dynamic-block-on-page.png){width="600" zoomable="yes"}

1. 在舞台的右上角，按一下 _關閉全熒幕_ (![關閉全熒幕圖示](./assets/pb-icon-reduce.png))圖示。

   按一下此圖示會返回 _[!UICONTROL Content]_顯示預覽之頁面的區段。

1. 在右上角，按一下 **[!UICONTROL Save]** 箭頭並選擇 **[!UICONTROL Save & Close]**.

您已完成「區塊」練習的第二部分。 請務必保留您的工作以作參考。

## 第3部分：更新動態區塊

在本練習的最後一部分，您會在頁面在您的存放區中上線時，編輯動態區塊。 然後，以客戶區段成員的身分登入存放區，讓區塊出現。

![店面中的動態區塊範例](./assets/pb-tutorial2-dynamic-block-storefront.png){width="600" zoomable="yes"}

### 步驟1：編輯動態區塊

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

1. 尋找您的 _[!DNL Tee Shirt Promo]_格線中的動態區塊，並在編輯模式中開啟。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Content]** 區段並按一下 **[!UICONTROL Edit with Page Builder]**.

1. 變更欄寬：

   - 將游標停留在兩欄之間的邊框上。

   - 按住滑鼠鍵，並將邊框向左拖曳兩個區段。

     ![格線分割](./assets/pb-tutorial2-dynamic-block-edit-column-width.png){width="600" zoomable="yes"}

     第一欄現在是12 (4/12)個網格分割槽中的4個分割槽，第二欄是12 (8/12)個分割槽中的8個分割槽。

     ![兩個不相等的欄](./assets/pb-tutorial2-dynamic-block-edit-column-width-changed.png){width="600" zoomable="yes"}

1. 變更文字色彩：

   - 選取前兩行文字。

   - 在編輯器工具列上，選擇 **[!UICONTROL Text Color]** 並按一下 **[!UICONTROL White]** 色票。

   ![文字顏色](./assets/pb-tutorial2-dynamic-block-edit-text-color.png){width="600" zoomable="yes"}

1. 在舞台的右上角，按一下 _關閉全熒幕_ (![關閉全熒幕圖示](./assets/pb-icon-reduce.png))圖示。

   按一下此圖示會返回 _[!UICONTROL Content]_顯示預覽的動態區塊的區段。

1. 在右上角，按一下 **[!UICONTROL Save]**.

### 步驟2：檢視動態區塊

由於此動態區塊僅對特定客戶區段的成員可見，因此您必須以客戶區段成員的客戶身分登入，才能檢視促銷活動。 在此範例中，區塊僅對女性客戶顯示。

1. 開啟瀏覽器視窗到您的店面。

1. 若要檢視範例頁面，請修改網址列中的URL，如下所示：

   mystore.com/sample-page

   如果您的存放區設定為包含html尾碼，請依照以下方式包含尾碼：

   mystore.com/sample-page.html

1. 以女性客戶身分登入：

   - 在首頁的右上角，按一下 **[!UICONTROL Sign In]**.

   - 如果您的系統上已安裝範例Luma資料，請使用以下憑證：

     **[!UICONTROL Email]** - `roni_cost@example.com`

     **[!UICONTROL Password]** -  `roni_cost3@example.com`

   - 按一下 **[!UICONTROL Sign In]**.

   - 返回範例頁面，以檢視您以T恤促銷活動建立的動態區塊。

   ![為客戶區段顯示的動態區塊](./assets/pb-tutorial2-dynamic-block-storefront.png){width="700" zoomable="yes"}

您已完成「區塊」練習。 請務必保留您的工作以作參考。

準備就緒後，請繼續前往 [第3部分：目錄內容](3-catalog-content.md)

[1]: https://developers.google.com/maps/documentation/javascript/get-api-key
