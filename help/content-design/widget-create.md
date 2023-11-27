---
title: 建立和管理Widget
description: 瞭解如何建立及管理Widget，藉以自動更新您商店的內容。
exl-id: 680f2f41-ec51-4ac6-9e92-2817591af3e6
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 1%

---

# 建立和管理Widget

Widget是可重複使用的元件。 您可以輕鬆地建立Widget並修改現有元件，以自動更新整個商店的內容。 您也可以刪除不再使用的Widget。

![Widget](./assets/widgets.png){width="700" zoomable="yes"}

## 建立 Widget

每個元件建立Widget的流程幾乎相同 [Widget型別](widgets.md#widget-types). 您可以依照指示的第一部分操作，然後針對您想要的特定型別Widget完成最後一部分。

### 步驟1：選擇型別

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. 按一下 **[!UICONTROL Add Widget]**.

1. 在 _[!UICONTROL Settings]_區段：

   - 設定 **[!UICONTROL Type]** 至您要建立的Widget型別。

   - 確認 **[!UICONTROL Design Theme]** 設定為目前佈景主題。

     ![Widget設定](./assets/widget-settings.png){width="600" zoomable="yes"}

1. 按一下 **[!UICONTROL Continue]**.

### 步驟2：指定店面屬性和佈局

1. 在 _[!UICONTROL Storefront Properties]_區段：

   - 的 **[!UICONTROL Widget Title]**，輸入Widget的描述性標題。

     此標題只會從管理員看到。

   - 的 **[!UICONTROL Assign to Store Views]**，選取您希望Widget顯示的商店檢視。

     您可以選取特定的商店檢視，或 `All Store Views`. 若要選取多個檢視，請按住Ctrl鍵(PC)或Command鍵(Mac)並按一下每個選項。

   - （選用） For **[!UICONTROL Sort Order]**，請輸入數字以決定此專案在頁面相同部分與其他專案一起出現的順序。 (`0` =第一個， `1` =秒， `3` =第三個，依此類推。)

     ![店面屬性](./assets/widget-storefront-properties.png){width="600" zoomable="yes"}

1. 在 _[!UICONTROL Layout Updates]_區段，按一下&#x200B;**[!UICONTROL Add Layout Update]**.

1. 設定 **[!UICONTROL Display On]** 至要顯示的頁面型別。

1. 在 **[!UICONTROL Container]** 清單中，選擇要置入的頁面版面配置區域。

   ![版面更新](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

1. 如果介面工具集為連結，請設定 **[!UICONTROL Template]** 變更為下列其中一項：

   - `Block Template`  — 設定內容格式，以便能以獨立單位的形式放置在頁面上。
   - `Inline Template`  — 格式化內容，使其可置於其他內容內。 例如，文欄位落中的連結。

### 步驟3：完成Widget選項

各種Widget型別的選項稍有不同，但程式基本相同。 下列範例顯示特定類別的產品清單，具有分頁控制項。

1. 在左側面板中，選擇 **[!UICONTROL Widget Options]**.

1. 按一下 **[!UICONTROL Select Block]**.

1. 輸入 **[!UICONTROL Title]** 顯示在清單上方，例如 `Featured Products`.

1. 針對分頁控制項，設定 **[!UICONTROL Display Page Control]** 至 `Yes`  並執行下列動作：

   - 輸入 **[!UICONTROL Number of Products per Page]**.

   - 輸入總計 **[!UICONTROL Number of Products to Display]**.

   - 設定 **[!UICONTROL Condition]** 至要精選的產品類別。

     此程式與為設定條件相同 [價格規則](../merchandising-promotions/price-rules-catalog.md).

### 步驟4：儲存並檢查結果

1. 完成後，按一下 **[!UICONTROL Save]**.

1. 出現提示時，請依照工作區頂端的指示，視需要更新快取。

1. 返回您的店面以驗證Widget是否正常運作。

   若要將其移至其他位置，您可以重新開啟Widget，然後嘗試不同的頁面或區塊參考。

## Widget建立示範

若要瞭解如何建立Widget，請觀看此影片：

>[!VIDEO](https://video.tv.adobe.com/v/343786?quality=12)

## 編輯Widget

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. 使用格線上方的篩選條件來尋找Widget，然後按一下Widget名稱。

1. 進行必要的變更。

   如需有關Widget選項的資訊，請檢閱建立Widget的步驟。

1. 按一下 **[!UICONTROL Save]**.

## 刪除Widget

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. 使用格線上方的篩選條件來找出介面工具集，然後選取要刪除之介面工具集的核取方塊。

1. 在清單的左上角，設定 **[!UICONTROL Actions]** 至 `Delete`.

1. 完成後，按一下 **[!UICONTROL Submit]**.

1. 若要確認動作，請按一下 **[!UICONTROL OK]**.
