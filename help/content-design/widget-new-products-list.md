---
title: 新產品清單Widget
description: 瞭解如何使用新產品清單Widget顯示最近新增產品的清單。
exl-id: bdff3655-cd14-4a19-a51f-4cabeb274d2a
feature: Page Content, Products
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 0%

---

# 新產品清單Widget

新產品清單是動態內容的範例，由從產品目錄提取的即時資料組成。 根據預設， _新產品_ 清單包括最近新增的前8項產品。 不過，您也可以將其設定為僅包含指定日期範圍內的產品。

![店面首頁上的新產品清單](./assets/storefront-home-page-new-products.png){width="700" zoomable="yes"}

## 步驟1：將每項產品設為新產品

![Magento Open Source](../assets/open-source.svg) 此步驟僅適用於Magento Open Source。

![Adobe Commerce](../assets/adobe-logo.svg) 如需Adobe Commerce商店的相關資訊，請參閱 [排程更新](content-staging-scheduled-update.md) 然後繼續本頁面上的步驟2。

_[!UICONTROL Set Product as New]_日期範圍設定只能在排程更新中設定。

將產品設定為新將產品新增至 _新產品_ 清單。 當您不再想要將設定加入清單時，隨時都可以變更回設定。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 尋找您想要功能的每項產品，並在編輯模式中開啟。

1. 的 **[!UICONTROL Set Product as New]**，切換是否將產品設定為新產品的選項。

   ![將產品設定為新產品](./assets/product-set-as-new.png){width="400" zoomable="yes"}

1. 完成後，按一下 **[!UICONTROL Save]**.

1. 當系統提示您重新索引和重新整理頁面快取時，請按一下頁面頂端的連結，然後依照指示進行。

## 步驟2：建立Widget

決定新產品清單內容及其在商店中的位置的程式碼，會由Widget工具產生。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. 在右上角，按一下 **[!UICONTROL Add Widget]**.

1. 在 _[!UICONTROL Settings]_區段，請執行下列動作：

   - 設定 **[!UICONTROL Type]** 至 `Catalog New Products List`.

   - 選擇 **[!UICONTROL Design Theme]** 由商店使用。

1. 按一下 **[!UICONTROL Continue]**.

   ![新增產品清單Widget設定](./assets/widget-settings.png){width="600" zoomable="yes"}

1. 在 _[!UICONTROL Storefront Properties]_區段，請執行下列動作：

   - 的 **[!UICONTROL Widget Title]**，輸入Widget的描述性標題。 (此標題只會從 _管理員_.)

   - 的 **[!UICONTROL Assign to Store Views]**，選取顯示Widget的商店檢視。

     您可以選取特定的商店檢視，或 `All Store Views`. 若要選取多個檢視，請按住Ctrl鍵(PC)或Command鍵(Mac)並按一下每個選項。

   - （選用） For **[!UICONTROL Sort Order]**，請輸入數字以決定此專案在頁面相同部分與其他專案一起出現的順序。 (`0` =第一個， `1` =秒， `3` =第三個，依此類推。)

   ![版面更新](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

## 步驟3：選擇位置

1. 在 _[!UICONTROL Layout Updates]_區段，按一下&#x200B;**[!UICONTROL Add Layout Update]**.

1. 設定 **[!UICONTROL Display On]** 至 `Specified Page.`

1. 設定 **[!UICONTROL Page]** 至 `CMS Home Page`.

1. 設定 **[!UICONTROL Block Reference]** 至 `Main Content Area`.

1. 設定 **[!UICONTROL Template]** 變更為下列其中一項：

   - `New Product List Template`
   - `New Products Grid Template`

     ![版面更新](./assets/widget-layout-update-new-products-list.png){width="600" zoomable="yes"}

1. 按一下 **[!UICONTROL Save and Continue Edit]**.

   現在，您可以忽略訊息以重新整理快取。

## 步驟4：設定清單

1. 在左側面板中，選擇 **[!UICONTROL Widget Options]**.

1. 設定 **[!UICONTROL Display Products]** 變更為下列其中一項：

   - `All Products`  — 依序列出產品，從最近新增的產品開始。
   - `New Products`  — 僅列出識別為的產品 _新_. 在中指定的日期範圍內，產品會被視為新產品 _[!UICONTROL Set Product As New From/To]_. 如果日期範圍到期，但未定義任何新產品，則清單為空白。

1. 若要為具有多個頁面的清單提供導覽控制項，請設定 **[!UICONTROL Display Page Control]** 至 `Yes`.

   的 **[!UICONTROL Number of Products per Page]**，輸入您想在各個頁面上顯示的產品數目。

1. 設定 **[!UICONTROL Number of Products to Display]** 要包含在清單中的新產品數目的選項。

   預設設定為 `10`.

1. 的 **[!UICONTROL Cache Lifetime (Seconds)]**，選擇您重新整理新產品清單的頻率。

   快取預設為86,400秒（24小時）。

   ![Widget選項](./assets/widget-options-new-product-list.png){width="600" zoomable="yes"}

1. 完成後，按一下 **[!UICONTROL Save]**.

1. 當提示重新整理快取時，請按一下頁面頂端訊息中的連結，然後依照指示進行。

## 步驟5：預覽您的工作

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. 在方格中尋找頁面，其中 _新產品_ 清單隨即顯示，請按一下 **[!UICONTROL Preview]** 中的連結 _[!UICONTROL Action]_欄。
