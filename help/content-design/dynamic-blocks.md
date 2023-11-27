---
title: 動態區塊
description: 使用動態區塊來建立由價格規則和客戶區段中的邏輯驅動的豐富互動式內容。
exl-id: 0c842ad9-2e46-48aa-9a12-2f74a54c352e
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# 動態區塊

{{ee-feature}}

建立由邏輯驅動的豐富互動式內容 [價格規則](../merchandising-promotions/introduction.md#price-rules) 和 [客戶區段](../customers/customer-segments.md). 現有 [動態區塊](../page-builder/dynamic-block.md) 可直接新增至 [!DNL Page Builder] [階段](../page-builder/workspace.md). 如需使用動態區塊的詳細逐步範例，請參閱 [教學課程2：區塊](../page-builder/2-blocks.md).

>[!NOTE]
>
>此 _[!UICONTROL Banner]_中的選項 [[!UICONTROL Content] 功能表](content-menu.md) 2.3.1已棄用，2.4.0已移除。其功能已由動態區塊取代。

![[!DNL Page Builder]  — 具有價格規則和客戶區段的動態區塊](../page-builder/assets/pb-tutorial2-dynamic-block-storefront.png){width="600" zoomable="yes"}

## 步驟1：建立動態區塊

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

   ![動態區塊清單](../page-builder/assets/pb-tutorial2-block-dynamic-add.png){width="600" zoomable="yes"}

1. 在右上角，按一下 **[!UICONTROL Add Dynamic Block]**.

   ![新增動態區塊](../page-builder/assets/pb-tutorial2-block-dynamic-new.png){width="600" zoomable="yes"}

1. 如果適用，請設定 **[!UICONTROL Store View]** 至將出現動態區塊的特定存放區檢視。

1. 若要啟用動態區塊，請設定 **[!UICONTROL Enable Dynamic Block]** 至 `Yes`.

1. 如需內部參考，請輸入描述性 **[!UICONTROL Dynamic Block Name]**.

1. 設定 **[!UICONTROL Dynamic Block Type]** 移至您要顯示動態區塊的頁面區域，然後按一下 **[!UICONTROL Done]**.

   ![設定動態區塊型別](../page-builder/assets/pb-dynamic-block-type.png){width="500" zoomable="yes"}

1. 在 **[!UICONTROL Customer Segment]** 清單中，選取您要檢視動態區塊的每個區段核取方塊，然後按一下 **[!UICONTROL Done]** 以儲存設定。

   ![選擇客戶區段](../page-builder/assets/pb-dynamic-block-customer-segment.png){width="500" zoomable="yes"}

   >[!NOTE]
   >
   >- 如果未建立任何區段，則每個人都可以看見動態區塊。
   >- 如果客戶不屬於任何區段，且已針對所有區段建立動態區塊，仍會顯示動態區塊的內容。
   >- 如果刪除指派給動態區塊的所有客戶區段，其內容便會顯示給每個人。

### 在動態區塊中使用Real-Time CDP對象

如果您 [已安裝](../customers/audience-activation.md#install-the-extension) 和 [已設定](../customers/audience-activation.md#configure-the-extension) 此 [!DNL Audience Activation] 擴充功能中，您會看到名為 **[!UICONTROL Audiences]**.

![選擇Real-Time CDP對象](./assets/dynamic-block-rtcdp.png){width="600" zoomable="yes"}

在 **[!UICONTROL Real-Time CDP Audience]** 清單中，選取您要檢視動態區塊之每個對象的核取方塊，然後按一下 **[!UICONTROL Done]** 以儲存設定。

## 步驟2：完成內容

使用 [!DNL Page Builder] [工作區](../page-builder/workspace.md) 以完成內容。

![[!DNL Page Builder]  — 動態區塊工作區](../page-builder/assets/pb-dynamic-block-workspace.png){width="600" zoomable="yes"}

## 步驟3：選擇相關促銷活動

1. 向下捲動並展開 ![展開選擇器](../assets/icon-display-expand.png) **[!UICONTROL Related Promotions]**.

1. 按一下您要與動態區塊關聯的促銷活動型別：

   - **[!UICONTROL Add Cart Price Rules]** (請參閱 [購物車價格規則](../merchandising-promotions/price-rules-cart.md))

   - **[!UICONTROL Add Catalog Price Rules]** (請參閱 [目錄價格規則](../merchandising-promotions/price-rules-catalog.md))

   >[!NOTE]
   >
   >Real-Time CDP受眾不支援目錄價格規則。

1. 在可用規則清單中，選取要使用的每個規則的核取方塊，然後按一下 **[!UICONTROL Add Selected]**.

1. 當動態區塊完成時，按一下 **[!UICONTROL Save]**.

## 步驟4：將動態區塊新增至頁面

1. 開啟您要顯示動態區塊的頁面。

1. 使用 [[!UICONTROL Add Dynamic Block]](../page-builder/dynamic-block.md) 內容型別，將動態區塊新增至「舞台」。

## 欄位和工具說明

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Store View] | 指定動態區塊可用的存放區檢視。 |
| [!UICONTROL Enable Dynamic Block] | 啟用或停用動態區塊。 選項：是/否 |
| [!UICONTROL Dynamic Block Name] | 在Admin中識別動態區塊的描述性名稱。 |
| [!UICONTROL Dynamic Block Type] | 識別 [標準頁面配置](layout-updates.md) 動態區塊的放置位置。 選項： <br/>**[!UICONTROL Content Area]**— 將動態區塊放置在主要區塊中 [內容區域](layout-updates.md) 頁面的「 」。<br/>**[!UICONTROL Footer]**  — 將動態區塊放置在頁面中 [頁尾](page-setup.md#footer). <br/>**[!UICONTROL Header]**— 將動態區塊放置在頁面中 [頁首](page-setup.md#header).<br/>**[!UICONTROL Left Column]**  — 將動態區塊放入 [左側欄](page-layout.md#standard-page-layouts) 兩欄或三欄配置圖的。 <br/>**[!UICONTROL Right Column]**— 將動態區塊放入 [右側邊欄](page-layout.md#standard-page-layouts) 兩欄或三欄配置圖的URL。 |
| 客戶區段 | 將客戶區段與動態區塊建立關聯，以決定哪些客戶可以看到它。 |
| Real-Time CDP對象 | 關聯 [Real-Time CDP對象](../customers/audience-activation.md) ，用於判斷哪些客戶可以看到它。 |

{style="table-layout:auto"}

### 內容

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Layout] | 將列、欄或標籤新增至舞台。 |
| [!UICONTROL Elements] | 將文字、標題、按鈕、分隔線和HTML程式碼新增至「舞台」上的任何版面容器。 |
| [!UICONTROL Media] | 將影像、影片、橫幅、滑桿和Google地圖新增至「舞台」上任何現有的版面容器。 |
| [!UICONTROL Add Content] | 將現有區塊、動態區塊和產品新增到舞台。 |

{style="table-layout:auto"}

### 相關促銷活動

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Related Cart Price Rule] | **[!UICONTROL Add Cart Price Rules]**  — 關聯現有的 [購物車價格規則](../merchandising-promotions/price-rules-cart.md) 將動態區塊作為促銷活動。 |
| [!UICONTROL Related Catalog Price Rule] | **[!UICONTROL Add Catalog Price Rules]**  — 關聯現有的 [型錄價格規則](../merchandising-promotions/price-rules-catalog.md) 將動態區塊作為促銷活動。 |

{style="table-layout:auto"}
