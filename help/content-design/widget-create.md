---
title: 建立和管理Widget
description: 瞭解如何建立及管理Widget，藉以自動更新您商店的內容。
exl-id: 680f2f41-ec51-4ac6-9e92-2817591af3e6
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 0%

---

# 建立和管理Widget

Widget是可重複使用的元件。 您可以輕鬆地建立Widget並修改現有元件，以自動更新整個商店的內容。 您也可以刪除不再使用的Widget。

![介面工具集](./assets/widgets.png){width="700" zoomable="yes"}

## 建立小工具

每個[Widget型別](widgets.md#widget-types)的建立Widget程式幾乎相同。 您可以依照指示的第一部分操作，然後針對您想要的特定型別Widget完成最後一部分。

### 步驟1：選擇型別

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**。

1. 按一下&#x200B;**[!UICONTROL Add Widget]**。

1. 在&#x200B;_[!UICONTROL Settings]_區段中：

   - 將&#x200B;**[!UICONTROL Type]**&#x200B;設定為您要建立的Widget型別。

   - 確認&#x200B;**[!UICONTROL Design Theme]**&#x200B;已設定為目前主題。

     ![Widget設定](./assets/widget-settings.png){width="600" zoomable="yes"}

1. 按一下&#x200B;**[!UICONTROL Continue]**。

### 步驟2：指定店面屬性和佈局

1. 在&#x200B;_[!UICONTROL Storefront Properties]_區段中：

   - 針對&#x200B;**[!UICONTROL Widget Title]**，輸入Widget的描述性標題。

     此標題只會從管理員看到。

   - 針對&#x200B;**[!UICONTROL Assign to Store Views]**，選取您要顯示Widget的存放區檢視。

     您可以選取特定的商店檢視，或`All Store Views`。 若要選取多個檢視，請按住Ctrl鍵(PC)或Command鍵(Mac)並按一下每個選項。

   - （選擇性）針對&#x200B;**[!UICONTROL Sort Order]**，輸入數字以決定此專案在頁面相同部分與其他專案一起出現的順序。 （`0` =第一個，`1` =第二個，`3` =第三個，依此類推。）

     ![店面屬性](./assets/widget-storefront-properties.png){width="600" zoomable="yes"}

1. 在&#x200B;_[!UICONTROL Layout Updates]_區段中，按一下&#x200B;**[!UICONTROL Add Layout Update]**。

1. 將&#x200B;**[!UICONTROL Display On]**&#x200B;設定為要顯示的頁面型別。

1. 在&#x200B;**[!UICONTROL Container]**&#x200B;清單中，選擇要置入的頁面配置區域。

   ![配置更新](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

1. 如果介面工具集是連結，請將&#x200B;**[!UICONTROL Template]**&#x200B;設定為下列其中一項：

   - `Block Template` — 設定內容格式，以便能作為獨立單位放置在頁面上。
   - `Inline Template` — 將內容格式化，以便可以放在其他內容中。 例如，文欄位落中的連結。

### 步驟3：完成Widget選項

各種Widget型別的選項稍有不同，但程式基本相同。 下列範例顯示特定類別的產品清單，具有分頁控制項。

1. 在左側面板中選擇&#x200B;**[!UICONTROL Widget Options]**。

1. 按一下&#x200B;**[!UICONTROL Select Block]**。

1. 輸入要在清單上方顯示的&#x200B;**[!UICONTROL Title]**，例如`Featured Products`。

1. 針對分頁控制項，請將&#x200B;**[!UICONTROL Display Page Control]**&#x200B;設為`Yes`並執行下列動作：

   - 輸入&#x200B;**[!UICONTROL Number of Products per Page]**。

   - 輸入總計&#x200B;**[!UICONTROL Number of Products to Display]**。

   - 將&#x200B;**[!UICONTROL Condition]**&#x200B;設定為要精選的產品類別。

     此程式與設定[價格規則](../merchandising-promotions/price-rules-catalog.md)的條件相同。

### 步驟4：儲存並檢查結果

1. 完成時，按一下&#x200B;**[!UICONTROL Save]**。

1. 出現提示時，請依照工作區頂端的指示，視需要更新快取。

1. 返回您的店面以驗證Widget是否正常運作。

   若要將其移至其他位置，您可以重新開啟Widget，然後嘗試不同的頁面或區塊參考。

## Widget建立示範

若要瞭解如何建立Widget，請觀看此影片：

>[!VIDEO](https://video.tv.adobe.com/v/343786?quality=12&learn=on)

## 編輯Widget

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**。

1. 使用格線上方的篩選條件來尋找Widget，然後按一下Widget名稱。

1. 進行必要的變更。

   如需有關Widget選項的資訊，請檢閱建立Widget的步驟。

1. 按一下&#x200B;**[!UICONTROL Save]**。

## 刪除Widget

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**。

1. 使用格線上方的篩選條件來找出介面工具集，然後選取要刪除之介面工具集的核取方塊。

1. 在清單的左上角，將&#x200B;**[!UICONTROL Actions]**&#x200B;設定為`Delete`。

1. 完成時，按一下&#x200B;**[!UICONTROL Submit]**。

1. 若要確認動作，請按一下&#x200B;**[!UICONTROL OK]**。
