---
title: 產品色票
description: 瞭解如何為可設定的產品清單定義色票。
exl-id: 6163cec4-5d84-4e2c-ba5c-3c22ac4e3f28
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1160'
ht-degree: 0%

---

# 產品色票

客戶對選擇顏色有很高的期望，產品描述必須準確呈現每種可用的顏色、圖樣或紋理。 例如，下列範例中的褲子不提供紅色、綠色和藍色。 相反地，它們只能以紅色、綠色和藍色的特定色調提供，這些可能是此產品所獨有的。

![產品頁面上的色票](./assets/storefront-color-swatches.png){width="700" zoomable="yes"}

的 [可設定的產品](product-create-configurable.md)，能以視覺色票、文字色票或輸入控制項來指示顏色。 色票可用於產品頁面、產品清單及 [分層導覽](navigation-layered.md). 在產品頁面上，色票會同步處理，以便在選取色票時顯示對應的產品影像。 當客戶選取色票時，對應的值會出現在輸入欄位中，且色票會概述為目前的選取專案。

>[!NOTE]
>
>您可以設定色票屬性，以便在選取色票時，不顯示對應的簡單產品影像。 _[!UICONTROL Update Product Preview Image]_選項值至 `No` 於 [!UICONTROL Attribute Edit] 頁面。

## 文字色票

如果色票沒有影像，屬性值會顯示為文字。 文字型色票就像具有文字標籤的按鈕，其行為與具有影像的色票相同。 使用文字色票來顯示可用大小時，會去除任何不可用的大小。

![文字型色票選取範圍會顯示無庫存大小](./assets/storefront-swatch-size-out-of-stock.png){width="700" zoomable="yes"}

## 分層導覽中的色票

如果符合下列條件，則色票也可用於分層導覽： _[!UICONTROL Use in Layered Navigation]_color屬性的屬性設為 `Yes`. 下列範例顯示分層導覽中的文字和彩色影像色票。

![以分層導覽方式顯示的色票](./assets/storefront-swatches-layered-navigation.png){width="700" zoomable="yes"}

## 建立產品的色票

色票可定義為 `color` 屬性或針對特定產品在本機設定，並上傳為 [產品影像](product-image.md#upload-an-image).

在先前的範例中，「Sylvia Capri」褲子可用於的特定值 `red`， `green`、和 `blue`. 因為色票是從產品影像中擷取的，所以每個色票都是顏色的真實表示法。 此 `color` attribute可用來管理所有產品顏色和色票的資訊。

### 步驟1：建立色票

使用下列其中一種方法來建立產品的色票。

#### 方法1：新增色票

1. 若要擷取產品的真正顏色，請在像片編輯器中開啟影像，並使用滴管工具來識別確切的顏色，並記下相等的十六進位值。

   ![十六進位色彩值](./assets/swatch-hex-values.png){width="400"}

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. 在格線中，開啟 _顏色_ 編輯模式中的屬性。

1. 確認 **[!UICONTROL Catalog Input Type for Store Owner]** 設為 `Visual Swatch`.

1. 如果您不想在產品顯示頁面上選取色票時顯示對應的簡單產品影像，請設定 **[!UICONTROL Update Product Preview Image]** 至 `No`.

1. 在 _[!UICONTROL Manage Swatch (Values of Your Attribute)]_，按一下&#x200B;**[!UICONTROL Add Swatch]**並執行下列動作：

   ![管理色票值](./assets/attribute-color-manage-swatch-values.png){width="600" zoomable="yes"}

   - 在 _色票_ 欄，按一下新色票並選取 **[!UICONTROL Choose a color]** 功能表中。

     ![選擇色票顏色](./assets/attribute-color-swatch-menu.png){width="500" zoomable="yes"}

   - 在檢色器中，將游標置於 **#** 欄位，刪除目前值，然後輸入新顏色的十六進位值。

     ![輸入十六進位值](./assets/attribute-swatch-color-picker-hex-value.png){width="500" zoomable="yes"}

   - 若要儲存色票，請按一下 _色輪_ ( ![顏色圖示](../assets/icon-color-wheel.png) )圖示來檢視色彩。

   - 在 _管理員_ 欄，輸入標籤以向商店管理員說明顏色。

     如果適用，您也可以針對支援的每種語言輸入顏色的翻譯。 在以下範例中，SKU包含在以下範例中以供參考： _管理員_ 標籤，因為顏色僅用於特定產品。 您可以在標籤中加入空格或底線，但不能加入連字型大小。

   - 在 _為預設_ 欄，選取要作為預設選項的色票。

   - 若要變更色票的順序，請按一下 _[!UICONTROL Order]_![排序順序圖示](../assets/icon-sort-order.png) 圖示並將專案拖曳至清單中的新位置。

     ![色票標籤](./assets/attribute-swatch-labels.png){width="400"}

1. 完成後，按一下 **[!UICONTROL Save Attribute]** 並在出現提示時重新整理快取。

1. 在編輯模式中開啟每個產品並更新 **顏色** 具有正確色票的屬性。

   若要同時更新多個產品，請遵循下列步驟。

#### 方法2：上傳色票影像

1. 若要擷取色票的影像，請在像片編輯器中開啟產品影像，並儲存影像中描述顏色、圖樣或紋理的方形區域。

   如有需要，您可以對產品的每個變化重複此動作。

   色票的大小和尺寸由主題決定。 一般而言，將影像儲存為正方形有助於保留圖樣的外觀比例。

   ![色票影像](./assets/swatch-samples.png){width="400"}

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. 在格線中，開啟 **[!UICONTROL color]** 編輯模式中的屬性。

1. 確認 **[!UICONTROL Catalog Input Type for Store Owner]** 設為 `Visual Swatch`.

1. 如果您不想在產品顯示頁面上選取色票時顯示對應的簡單產品影像，請設定 **[!UICONTROL Update Product Preview Image]** 至 `No`.

1. 在 _[!UICONTROL Manage Swatch]_（屬性的值），按一下&#x200B;**[!UICONTROL Add Swatch]**並執行下列動作：

   - 在 _[!UICONTROL Swatch]_欄，按一下新色票以顯示功能表並選擇&#x200B;**[!UICONTROL Upload a file]**.

   - 導覽至您準備的色票檔案，然後選擇要上傳的檔案。

   - 對每個色票影像重複這些步驟。

   - 輸入管理員和店面的標籤。

     在此範例中，SKU包含在管理員標籤中以供參考，因為這些顏色僅用於特定產品。 您可以在標籤中加入空格或底線，但不可加入連字型大小。

     ![輸入標籤](./assets/swatch-upload.png){width="500" zoomable="yes"}

1. 完成後，按一下 **[!UICONTROL Save Attribute]** 並在出現提示時重新整理快取。

1. 在編輯模式中開啟每個產品並更新 **[!UICONTROL Color]** 具有正確色票的屬性。

   若要同時更新多個產品，請遵循下列步驟。

### 步驟2：更新產品

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 使用 **[!UICONTROL Filter]** 以依名稱或SKU顯示清單，並僅包含適用的產品。

1. 在格線中，選取要套用色票之每個產品的核取方塊。

1. 設定 **[!UICONTROL Actions]** 至 `Update Attributes`.

   在此範例中，會選取褲子的所有藍色組態。

   ![更新產品色票屬性](./assets/swatch-apply-update-attributes.png){width="600" zoomable="yes"}

1. 向下捲動至 **[!UICONTROL Color]** 屬性並選取 **[!UICONTROL Change]** 核取方塊。

   ![變更核取方塊](./assets/swatch-update-attributes-choose-color.png){width="400"}

1. 選擇套用至所選產品的色票，然後按一下 **[!UICONTROL Save]**.

1. 出現提示時，請重新整理快取。

   ![色票在店面中顯示](./assets/swatch-blue-schmear.png){width="200"}

## 將色票新增至簡單產品

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 在編輯模式下開啟產品，檢查產品狀態（應啟用）。

1. 按一下 **[!UICONTROL Create Configurations]** 按鈕(在 `Configurations` 標籤)。

1. 在彈出式視窗中，選擇「顏色」屬性，然後 **[!UICONTROL Next]**.

1. 從要包含在此產品中的屬性中選取色票。

1. 在進度列中，按一下 **[!UICONTROL Next]**.

1. [設定影像、價格和數量](product-create-configurable.md#step-3-configure-the-images-price-and-quantity).

   在此步驟中，設定每個設定的影像、定價和數量。 每個的可用選項都相同，您只能選擇一個。 您可以將相同的設定套用至所有SKU、將唯一的設定套用至每個SKU，或暫時略過這些設定。

1. 影像、價格和數量的設定完成後，請按一下 **[!UICONTROL Next]** 位於右上角。

   目前的產品變數會出現在設定區段的底部。 如果您對組態滿意，請按一下 **[!UICONTROL Generate Products]**.
