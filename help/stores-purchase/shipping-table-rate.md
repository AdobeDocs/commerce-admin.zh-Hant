---
title: 表格費率運送
description: 瞭解如何為商店設定表格費率運送選項。
exl-id: f73adc9a-4c6c-477d-9553-3a3f28647bdd
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '999'
ht-degree: 3%

---

# 表格費率運送

此 _表格比率_ 送貨方法會參考資料表，以根據各種條件的組合計算運費，包括：

- 權重與目的地
- 價格v.目的地
- 專案數對目的地

舉例來說，如果您的倉儲位於洛杉磯，則運送至聖地亞哥的成本會比運送至佛蒙特州來得低。 您可以使用表格運費將節省金額傳遞給客戶。

用來計算表格比率的資料會在試算表中準備並匯入您的存放區。 當客戶請求報價時，結果會顯示在購物車的送貨預估區段中。

>[!NOTE]
>
>一次只能啟用一組表格速率資料。

![購物車訂單摘要中的表格費率送貨選項](./assets/storefront-cart-table-rate.png){width="700" zoomable="yes"}

## 步驟1：完成預設設定

第一步是完成表格費率的預設設定。 您可以在不變更設定範圍的情況下完成此步驟。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在 _[!UICONTROL Sales]_部分，選擇&#x200B;**[!UICONTROL Delivery Methods]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Table Rates]** 區段。

   >[!NOTE]
   >
   >如有必要，請先清除 **[!UICONTROL Use system value]** 核取方塊來變更下列設定，如所述。

   ![表格費率](../configuration-reference/sales/assets/delivery-methods-table-rates.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Enabled]** 至 `Yes`.

1. 輸入 **[!UICONTROL Title]** 結帳期間要顯示在表格費率區段的「 」標籤。

   預設標題為 `Best Way`.

1. 輸入 **[!UICONTROL Method Name]** ，以便在購物車的計算費率旁邊顯示為標籤。

1. 設定 **[!UICONTROL Condition]** 變更為下列其中一種計算方法：

   - `Weight v. Destination`
   - `Price v. Destination`
   - `Number of Items v. Destination`

1. 若訂單包含虛擬產品，請設定 **[!UICONTROL Include Virtual Products in Price Calculation]** 至 `Yes` 如果您想要將虛擬產品納入計算中。

   >[!NOTE]
   >
   >由於虛擬產品（例如服務）沒有權重，因此無法變更以「權重v.目的地」條件為基礎的計算結果。 不過，虛擬產品可能會變更以「價格v.目的地」或「料號v.目的地」條件為基準的計算結果。

1. 根據您的要求設定手續費選項。

   處理費是選擇性的，且顯示為額外費用，會加到運費中。 如果要包含手續費，請執行下列步驟：

   - 設定 **[!UICONTROL Calculate Handling Fee]**：

      - `Fixed`
      - `Percent`

   - 輸入 **[!UICONTROL Handling Fee]** 根據用於計算費用的方法的費率。

     例如，如果費用是以固定費用為基礎，則以小數點輸入金額，例如 `4.90`. 不過，如果處理費是以訂單的百分比為基準，請以百分比輸入金額。 例如，如果您對訂單的6%計費，則輸入值為 `.06`.

1. 如有需要，請變更 **[!UICONTROL Displayed Error Message]**.

   此文字方塊已預設預設預設預設訊息，但您可以輸入其他訊息，在此傳送方式無法使用時顯示。

1. 設定 **[!UICONTROL Ship to Applicable Countries]**：

   - `All Allowed Countries`  — 來自所有客戶的客戶 [國家/地區](../getting-started/store-details.md#country-options) 在存放區設定中指定時，可以使用此傳送方法。
   - `Specific Countries`  — 選擇此選項時， _[!UICONTROL Ship to Specific Countries]_清單隨即顯示。 選取清單中可使用此傳遞方法的每個國家/地區。

1. 設定 **[!UICONTROL Show Method if Not Applicable]** 至 `Yes` 如果您要一直顯示表格費率

1. 的 **[!UICONTROL Sort Order]**，請輸入數字，以決定結帳期間與其他傳送方式一起列出時，表格費率出貨的顯示順序。

   `0` =第一個， `1` =秒， `2` =第三個，依此類推。

1. 按一下 **[!UICONTROL Save Config]**.

## 步驟2：準備表格速率資料

1. 在左上角，設定 **[!UICONTROL Store View]** 至 `Main Website`，或套用設定的任何其他網站。

   >[!NOTE]
   >
   >如有必要，請先取消選取 **[!UICONTROL Use system value]** 核取方塊來變更下列設定，如所述。

1. 變更 **[!UICONTROL Condition]** 視需要。

1. 按一下 **[!UICONTROL Export CSV]**.

   ![匯出CSV](./assets/shipping-table-rates-export.png){width="700" zoomable="yes"}

1. 儲存 `tablerates.csv` 檔案到您的系統。

1. 在試算表應用程式中開啟檔案。

1. 使用適當的出貨計算條件值完成表格。

   - 使用星號(*)當作萬用字元，代表任何類別中的所有可能值。
   - 此 _[!UICONTROL Country]_欄必須包含 [有效的三字元代碼][1] 每一列。
   - 資料排序依據 _[!UICONTROL Region/State]_因此，特定位置位於清單頂端，而萬用字元位置位於清單底部。 此方法會先處理具有絕對值的規則，稍後再處理萬用字元值。
   - 中的值 _[!UICONTROL Weight (and above)]_欄最多可以有四個小數位數(例如 `2.5075`)。 在資料中使用更多小數位數，會導致匯入失敗。

   ![重量與目的地（澳洲）](./assets/table-rates-weight-destination-csv.png){width="500"}

1. 儲存 `tablerates.csv` 檔案。

## 步驟3：匯入表格比率資料

1. 返回 **[!UICONTROL Table Rates]** 區段設定的。

1. 在左上角，設定 **[!UICONTROL Store View]** 移至使用此方法的網站。

1. 的 **[!UICONTROL Import]**，按一下 **[!UICONTROL Choose File]** 並選取您已完成的 `tablerates.csv` 檔案以匯入費率。

   ![匯入表格費率](./assets/shipping-table-rates-import.png){width="600" zoomable="yes"}

1. 按一下 **[!UICONTROL Save Config]**.

## 步驟4：驗證費率

為確保表格費率資料正確無誤，請使用數個不同的地址進行付款處理，以確保運費與處理費率計算正確。

### 範例1：價格與目的地

此範例使用「價格v.目的地」條件，根據美國大陸、阿拉斯加和夏威夷的訂單小計金額，建立一組三種不同的運費。 星號(*)是代表所有值的萬用字元。

| 國家 | 地區/州 | 郵遞區號 | 訂單小計（及以上） | 送貨價格 |
|--- |--- |--- |--- |--- |
| 美國 | 您好 | * | 100 | 10 |
| 美國 | 您好 | * | 50 | 15 |
| 美國 | 您好 | * | 0 | 20 |
| 美國 | AK | * | 100 | 10 |
| 美國 | AK | * | 50 | 15 |
| 美國 | AK | * | 0 | 20 |
| 美國 | * | * | 100 | 5 |
| 美國 | * | * | 50 | 10 |
| 美國 | * | * | 0 | 15 |

{style="table-layout:auto"}

### 範例2：權重與目的地

此範例使用「重量v.目的地」條件，根據訂單重量建立不同的出貨率。

| 國家 | 地區/州 | 郵遞區號 | 重量（及以上） | 送貨價格 |
|--- |--- |--- |--- |--- |
| AUS | NT | * | 9 | 39.95 |
| AUS | NT | * | 0 | 19.95 |
| AUS | VIC | * | 9 | 19.95 |
| AUS | VIC | * | 0 | 5.95 |
| AUS | WA | * | 9 | 39.95 |
| AUS | WA | * | 0 | 19.95 |
| AUS | * | * | 9 | 29.95 |
| AUS | * | * | 0 | 9.95 |

{style="table-layout:auto"}

### 範例3：限制免費送貨至美國大陸

1. 建立 `tablerates.csv` 此檔案包含您願意提供免費運送的所有州目的地。

1. 使用下列設定完成表格速率設定：

   | 設定 | 值 |
   |----------|-------|
   | [!UICONTROL Condition] | `Price v. Destination` |
   | [!UICONTROL Method Name] | `Free Shipping` |
   | [!UICONTROL Ship to Applicable Countries] | `Specific Countries` |
   | [!UICONTROL Ship to Specific Countries] | `Select only United States` |
   | [!UICONTROL Show method if not applicable] | `No` |

   {style="table-layout:auto"}

1. 在左上角，設定 **[!UICONTROL Store View]** 至 `Main Website`，或套用設定的任何其他網站。

1. 的 **[!UICONTROL Import]**，按一下 **[!UICONTROL Choose File]** 並選取您已完成的 `tablerates.csv` 檔案以匯入費率。


[1]: https://en.wikipedia.org/wiki/ISO_3166-1_alpha-3
