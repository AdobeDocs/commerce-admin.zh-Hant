---
title: 匯入套件組合產品
description: 檢閱匯入套件產品的產品資料範例。
exl-id: 52146979-9911-449b-9f14-54377e2ae9f4
feature: Products, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 0%

---

# 匯入套件組合產品

套件產品提供多種商品，客戶可選擇購買哪些商品。 組成束的所有專案都會以其中一種形式存在於目錄中 [簡單產品](../catalog/product-create-simple.md) 或 [虛擬產品](../catalog/product-create-virtual.md). 通常，套件組合產品會從管理員建立和更新。 不過，您也可以匯入資料以建立組合產品，或者可以匯出現有的組合產品、編輯資料並將它們匯回目錄中。 Sprite Yoga Companion Kit是範例資料中的組合產品，用於下列範例。

![套裝產品](../catalog/assets/product-bundle.png){width="700" zoomable="yes"}

## 變更組合專案的順序

有兩種方式可變更組合產品中的專案順序。

### 方法1：拖放

使用時 [組合](../catalog/product-create-bundle.md) 從管理員取得產品後，您可以將專案和區段拖放至適當位置。

![組合包專案](../catalog/assets/product-bundle-items-move.png){width="600" zoomable="yes"}

### 方法2：編輯產品資料

瞭解套件產品結構的最佳方式是匯出產品，並在試算表中檢查資料。 您可以匯出產品並將位置引數加入每個專案的資料中，以變更束專案的順序。 專案資料位於 `bundle_values` 已匯出產品的欄。 在試算表中開啟時，與產品相關聯的所有專案都會在單一儲存格中成為長字串。 此 `bundle_values` 欄包含每個專案的下列元素：

- 專案區段的名稱
- 輸入控制項
- 必要專案指標
- SKU
- 顏色
- 價格
- 預設選項指示器
- 預設數量
- 價格型別
- 可編輯數量指示器

#### 步驟1：匯出套件組合產品

在此步驟中，Sprite Yoga Companion Kit會匯出為([CSV](data-csv.md) 檔案。 您可以使用目錄中的任何其他套裝產品。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. 在 _匯出設定_，設定 **[!UICONTROL Entity Type]** 至 `Products`.

1. 在產品屬性清單中，向下捲動至 **[!UICONTROL SKU]** 並輸入您要匯出的套件組合產品的SKU。

   SKU是 `24-WG080` 在此範例的產品中設定。

1. 向下捲動至區段底部，然後按一下 **[!UICONTROL Continue]**.

1. 在 _[!UICONTROL Action]_的欄_[!UICONTROL File name]_ 格點，按一下 **[!UICONTROL Select]** 並選擇 `Download`.

   檔案會顯示在瀏覽器使用的下載位置。

#### 步驟2：編輯資料

1. 在試算表中開啟下載的CSV檔案。

1. 捲動至最右邊，直到您可以看到 `bundle_values` 欄。

   在 `bundle_values` 資料時，每個元素會以逗號分隔，每個束專案會以垂直列與下一個束專案分隔。 （最後一個專案的結尾不是垂直長條。） 您匯出的組合資料應該看起來類似下列範例：

   ![組合值](./assets/product-bundle-values-export-data.png){width="600" zoomable="yes"}

1. 為了更方便編輯，您可以複製 `bundle_values` 資料，並將其貼到文字編輯器中，然後在每個專案後新增分行符號，讓每個專案位於不同的行。

1. 編輯資料後，請小心移除分行符號，並將編輯的資料貼回中 `bundle_values` 欄。

   在下圖中， `position=[number]` 引數會新增至每個瑜伽帶，以變更商店清單中的專案順序。

   ![位置引數](./assets/product-bundle-values-position-parameter.png){width="500" zoomable="yes"}

1. 編輯資料後， **[!UICONTROL Save]** CSV檔案。

#### 步驟3：匯入更新的產品

1. 在 _管理員_ 側欄，前往 **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. 在 _[!UICONTROL Import Settings]_，設定&#x200B;**[!UICONTROL Entity Type]**至 `Products`.

1. 設定 **[!UICONTROL Import Behavior]** 至 `Replace`.

   此選項會覆寫套件產品的先前資料，而非將變更新增為其他專案。

1. 向下捲動至 _要匯入的檔案_ 區段並按一下 **[!UICONTROL Choose File]**.

1. 選取您編輯的CSV檔案。

1. 按一下 **[!UICONTROL Check Data]** 並稍候片刻以檢查資料。

1. 如果檔案有效，請按一下 **[!UICONTROL Import]**.

1. 程式完成後，請前往 **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**並按一下&#x200B;**[!UICONTROL Flush Cache Storage]**.

   這可確保更新的產品立即在店面中可用。
