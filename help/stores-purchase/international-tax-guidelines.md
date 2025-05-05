---
title: 依國家/地區的稅捐准則
description: 根據國家/地區複查建議的稅捐設定。
exl-id: 027da0a2-0ff4-40a7-9b9c-eefad888bb7a
feature: Taxes
source-git-commit: f8254db7d69e58c8e9a78948ee6e40f5ea88cea0
workflow-type: tm+mt
source-wordcount: '1311'
ht-degree: 0%

---

# 依國家/地區的稅捐准則

## 美國稅捐組態

這些建議的設定可用於美國境內商店的大部分稅務設定。

| 稅捐選項 | 建議 |
|--- |--- |
| 載入目錄價格 | 排除稅金 |
| FPT | 否，因為FPT不納稅。 |
| 稅捐依據 | 送貨來源 |
| 稅捐計算 | 總計 |
| 稅金運送？ | 否 |
| 套用折扣 | 稅前 |
| 註解 | 所有稅捐區域都具有相同的優先順序；理想情況下，州會有一個區域，而郵遞區號會有一或多個區域進行查詢。 |

{style="table-layout:auto"}

### 稅捐類別

| 稅捐類別 | 建議的設定 |
|--- |--- |
| 出貨的稅捐類別 | 無 |

{style="table-layout:auto"}

### 計算設定

| 選項 | 建議的設定 |
|--- |--- |
| [!UICONTROL Tax Calculation Method Based On] | `Total` |
| [!UICONTROL Tax Calculation Based On] | `Shipping Origin` |
| [!UICONTROL Catalog Prices] | `Excluding Tax` |
| [!UICONTROL Shipping Prices] | `Excluding Tax` |
| [!UICONTROL Apply Customer Tax] | `After Discount` |
| [!UICONTROL Apply Discount on Prices] | `Excluding Tax` |

{style="table-layout:auto"}

### 預設稅捐目的地計算

| 選項 | 建議的設定 |
|--- |--- |
| [!UICONTROL Default Country] | `United States` |
| [!UICONTROL Default State] | 企業所在的州。 |
| [!UICONTROL Default Post Code] | 用於稅捐區的郵遞區號。 |

{style="table-layout:auto"}

### 價格顯示設定

| 選項 | 建議的設定 |
|--- |--- |
| [!UICONTROL Display Product Prices in Catalog] | `Excluding Tax` |
| [!UICONTROL Display Shipping Prices] | `Excluding Tax` |

{style="table-layout:auto"}

### 購物車顯示設定

| 選項 | 建議的設定 |
|--- |--- |
| [!UICONTROL Display Prices] | `Excluding Tax` |
| [!UICONTROL Display Subtotal] | `Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | `Excluding Tax` |
| [!UICONTROL Display Gift Wrapping Prices] | `Excluding Tax` |
| [!UICONTROL Display Printed Card Prices] | `Excluding Tax` |
| [!UICONTROL Include Tax in Grand Total] | `Yes` |
| [!UICONTROL Display Full Tax Summary] | `Yes` |
| [!UICONTROL Display Zero Tax Subtotal] | `Yes` |

{style="table-layout:auto"}

### 訂單、商業發票、銷退折讓單及顯示設定

| 選項 | 建議的設定 |
|--- |--- |
| [!UICONTROL Display Prices] | `Excluding Tax` |
| [!UICONTROL Display Subtotal] | `Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | `Excluding Tax` |
| [!UICONTROL Include Tax in Grand Total] | `Yes` |
| [!UICONTROL Display Full Tax Summary] | `Yes` |
| [!UICONTROL Display Zero Tax Subtotal] | `Yes` |

{style="table-layout:auto"}

### 固定產品稅金(FPT)

| 選項 | 建議的設定 |
|--- |--- |
| [!UICONTROL Enable FPT] | `No`，加州除外。 |

{style="table-layout:auto"}

## 英國稅捐組態

這些建議的設定可用於英國境內商店的大部分稅務設定。

### 英國B2C稅捐組態

| 稅捐選項 | 建議 |
|--- |--- |
| 載入目錄價格 | 排除稅金 |
| FPT | 是，包括FPT與說明 |
| 稅捐依據 | [!UICONTROL Shipping Address] |
| 稅捐計算 | 總計 |
| 稅金運送？ | 是 |
| 套用折扣 | 稅前折扣，價格包含稅金。 |
| 註解 | 適用於標示供應商商業發票（包括加值稅）的商家。 |

{style="table-layout:auto"}

### 英國B2B稅捐組態

| 稅捐選項 | 建議 |
|--- |--- |
| 載入目錄價格 | 排除稅金 |
| FPT | 是，包括FPT與說明 |
| 稅捐依據 | [!UICONTROL Shipping Address] |
| 稅捐計算 | 專案 |
| 稅金運送？ | 是 |
| 套用折扣 | 稅前折扣，價格包含稅金。 |
| 註解 | 讓B2B商家提供更簡單的VAT供應鏈考量事項。 資料列上的稅捐計算也有效；不過，請洽詢您的稅捐管轄區。 設定假設商家位於供應鏈中，且已售出貨品由其他廠商用於增值稅退稅等。 此定義可讓您輕鬆依料號識別稅捐，以加快產生返利的時間。 <br/><br/>**_備註：_**&#x200B;某些管轄區需要Commerce目前不支援的不同舍入策略，而且並非所有管轄區都允許專案或列層級稅捐。 |

{style="table-layout:auto"}

## 加拿大稅務組態

>[!IMPORTANT]
>
>位於GST/PST省份(Montreal)的商戶應建立一個稅捐規則，並顯示合併稅捐金額。 如有任何問題，請務必洽詢合格的稅務機關。

| 稅捐選項 | 建議 |
|--- |--- |
| 載入目錄價格 | 排除稅金 |
| FPT | 是，包括FPT、說明，以及對FPT套用稅捐。 |
| 稅捐依據 | 送貨來源 |
| 稅捐計算 | 總計 |
| 稅金運送？ | 是 |
| 套用折扣 | 稅前 |

{style="table-layout:auto"}

下列範例顯示如何設定加拿大的GST稅率與薩斯喀徹溫省的PST稅率，以及計算並顯示兩種稅率的稅捐規則。 此資訊會概述組態範例；請務必驗證您稅捐管轄區的正確稅率與規則。 設定稅捐時，請設定商店範圍，將設定套用至所有適用的商店和網站。

- 相關商品的固定產品稅包含在產品屬性中。
- 在魁北克，PST稱為TVQ。 如果您想要設定Quebec的費率，請務必使用TVQ做為識別碼。

### 步驟1：完成稅捐計算設定

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 若為多站台組態，請將&#x200B;**[!UICONTROL Store View]**&#x200B;設定為組態目標的網站和商店。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Sales]**&#x200B;並選擇&#x200B;**[!UICONTROL Tax]**。

1. 按一下以展開頁面上的每個區段，並完成下列設定：

#### 稅捐計算設定

| 欄位 | 建議的設定 |
|--- |--- |
| [!UICONTROL Tax Calculation Method Based On] | `Total` |
| [!UICONTROL Tax Calculation Based On] | `Shipping Address` |
| [!UICONTROL Catalog Prices] | `Excluding Tax` |
| [!UICONTROL Shipping Prices] | `Excluding Tax` |
| [!UICONTROL Apply Customer Tax] | `After Discount` |
| [!UICONTROL Apply Discount on Prices] | `Excluding Tax` |
| [!UICONTROL Apply Tax On] | `Custom Price` （如果有的話） |

{style="table-layout:auto"}

#### 稅捐類別

| 欄位 | 建議的設定 |
|--- |--- |
| [!UICONTROL Tax Class for Shipping] | `Shipping` （運費已納稅） |

{style="table-layout:auto"}

#### 預設稅捐目的地計算

| 欄位 | 建議的設定 |
|--- |--- |
| [!UICONTROL Default Country] | `Canada` |
| [!UICONTROL Default State] | （視情況而定） |
| [!UICONTROL Default Postal Code] | `*` （星號） |

{style="table-layout:auto"}

#### 購物車顯示設定

| 欄位 | 建議的設定 |
|--- |--- |
| [!UICONTROL Include Tax in Grand Total] | `Yes` |
| [!UICONTROL Display Full Tax Summary] | `Yes` |
| [!UICONTROL Display Zero in Tax Subtotal] | `Yes` |

{style="table-layout:auto"}

#### 固定產品稅金

| 欄位 | 建議的設定 |
|--- |--- |
| [!UICONTROL Enable FPT] | `Yes` |
| 所有FPT顯示設定 | `Including FPT and FPT description` |
| [!UICONTROL Apply Discounts to FPT] | `No` |
| [!UICONTROL Apply Tax to FPT] | `Yes` |
| [!UICONTROL Include FPT in Subtotal] | `No` |

{style="table-layout:auto"}

### 步驟2：設定加拿大商品與服務稅(GST)

若要在商業發票與其他銷售檔案上列印GST編號，請將其納入適用稅率的名稱。 GST會作為任何訂單彙總上的GST金額的一部分顯示。

#### 管理稅區與稅率

| 欄位 | 建議的設定 |
|--- |--- |
| [!UICONTROL Tax Identifier] | `Canada-GST` |
| [!UICONTROL Country] | `Canada` |
| [!UICONTROL State] | `*` （星號） |
| [!UICONTROL Zip/Post is Range] | `No` |
| [!UICONTROL Zip/Post Code] | `*` （星號） |
| [!UICONTROL Rate Percent] | `5.0000` |

{style="table-layout:auto"}

### 步驟3：設定加拿大省營業稅(PST)

設定適用省份的其他稅率。

#### 稅率資訊

| 欄位 | 建議的設定 |
|--- |--- |
| [!UICONTROL Tax Identifier] | `Canada-SK-PST` |
| [!UICONTROL Country] | `Canada` |
| [!UICONTROL State] | `Saskatchewan` |
| [!UICONTROL Zip/Post is Range] | `No` |
| [!UICONTROL Zip/Post Code] | `*` （星號） |
| [!UICONTROL Rate Percent] | `5.0000` |

{style="table-layout:auto"}

### 步驟4：建立GST稅捐規則

若要避免複合稅捐，並針對GST與PST將已計算的稅捐正確顯示為個別的明細專案，請為每個規則設定不同的優先順序，並選取&#x200B;**僅計算小計**&#x200B;核取方塊。 每項稅捐都會顯示為個別的明細專案，但不會複合稅捐金額。

#### 稅捐規則資訊

| 欄位 | 建議的設定 |
|--- |--- |
| 名稱 | `Retail-Canada-GST` |
| [!UICONTROL Customer Tax Class] | `Retail Customer` |
| [!UICONTROL Product Tax Class] | `Taxable GoodsShipping` |
| [!UICONTROL Tax Rate] | `Canada-GST` |
| [!UICONTROL Priority] | `0` |
| [!UICONTROL Calculate off subtotal only] | 選取此核取方塊。 |
| [!UICONTROL Sort Order] | `0` |

{style="table-layout:auto"}

### 步驟5：建立薩斯喀徹溫省的PST稅捐規則

針對此稅捐規則，請確定將優先順序設為0，並選取&#x200B;**僅計算小計**&#x200B;核取方塊。 每項稅捐都會顯示為個別的明細專案，但不會複合稅捐金額。

#### 稅捐規則資訊

| 欄位 | 建議的設定 |
|--- |--- |
| [!UICONTROL Name] | `Retail-Canada-PST` |
| [!UICONTROL Customer Tax Class] | `Retail Customer` |
| [!UICONTROL Product Tax Class] | `Taxable GoodsShipping` |
| [!UICONTROL Tax Rate] | `Canada-SK-PT` |
| [!UICONTROL Priority] | `1` |
| [!UICONTROL Calculate off subtotal only] | 選取此核取方塊。 |
| [!UICONTROL Sort Order] | `0` |

{style="table-layout:auto"}

### 步驟6：儲存並測試結果

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

1. 返回店面並建立樣本訂單以測試結果。

## 歐盟稅捐組態

下列範例說明一間位於法國的商店，在法國銷售10萬歐元以上，在德國銷售10萬歐元以上。

- 稅捐計算是在網站層級管理。
- 幣別兌換與稅捐顯示選項是在商店檢視層級個別控制（選取「使用網站」核取方塊以覆寫預設值）。
- 藉由設定預設稅捐國家，您可以動態顯示管轄區的正確稅捐。
- 相關商品的固定產品稅包含在產品屬性中。
- 您可能需要編輯目錄，以確保它顯示在正確的類別/網站/商店檢視中。

### 步驟1：建立三個產品稅捐類別

在此範例中，假設不需要多個「VAT減少」產品稅捐類別。

1. 建立「VAT標準」產品稅捐類別。

1. 建立VAT減少的產品稅捐類別。

1. 建立免加值稅產品稅捐類別。

### 步驟2：建立法國和德國的稅率

建立下列稅率：

| 稅率 | 設定 |
|--- |--- |
| 法國 — StandardVAT | 國家：法國<br/>州/地區： * <br/>郵遞區號： * <br/>費率： 20% |
| 法國 — ReducedVAT | 國家：法國<br/>州/地區： * <br/>郵遞區號： * <br/>費率： 5% |
| 德國 — StandardVAT | 國家：德國<br/>州/地區： * <br/>郵遞區號： *費率： 19% |
| 德國 — ReductedVAT | 國家：德國<br/>州/地區： * <br/>郵遞區號： * <br/>費率： 7% |

{style="table-layout:auto"}

### 步驟3：設定稅捐規則

建立下列稅捐規則：

| 稅捐規則 | 設定 |
|--- |--- |
| Retail-France-StandardVAT | 客戶類別：零售客戶<br/>稅捐類別： VAT標準<br/>稅率：法國StandardVAT <br/>優先順序： 0 <br/>排序順序： 0 |
| Retail-France-ReducedVAT | 客戶類別：零售客戶<br/>稅捐類別：VAT減少<br/>稅率：法國 — 減少VAT <br/>優先順序： 0 <br/>排序順序： 0 |
| Retail-Germany-StandardVAT | 客戶類別：零售客戶<br/>稅捐類別： VAT標準<br/>稅率：德國 — 標準VAT <br/>優先順序： 0 <br/>排序順序： 0 |
| Retail-Germany-ReductedVAT | 客戶類別：零售客戶<br/>稅捐類別：VAT減少<br/>稅率：德國 — 減少VAT <br/>優先順序： 0 <br/>排序順序： 0 |

{style="table-layout:auto"}

### 步驟4：設定德國的商店檢視

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**。

1. 在預設網站下，建立&#x200B;**[!UICONTROL Germany]**&#x200B;的商店檢視。

1. 接著，執行下列動作：

   - 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

   - 在左上角，將&#x200B;**[!UICONTROL Default Config]**&#x200B;設定為法文商店。

   - 在[一般]頁面上，展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Countries Options]**&#x200B;區段，並將預設國家/地區設定為`France`。

   - 視需要完成地區設定選項。

1. 在左上角，選擇德文&#x200B;**[!UICONTROL Store View]**。

1. 在&#x200B;_一般_&#x200B;頁面上，展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Countries Options]**，並將預設國家/地區設定為`Germany`。

1. 視需要完成地區設定選項。

### 步驟5：設定法國的稅捐設定

完成下列一般稅捐設定：

| 欄位 | 建議的設定 |
|--- |--- |
| [[!UICONTROL Tax Classes]](../configuration-reference/sales/tax.md#tax-classes) |  |
| [!UICONTROL Tax Class for Shipping] | `Shipping` （運費已納稅） |
| [[!UICONTROL Calculation Settings]](../configuration-reference/sales/tax.md#calculation-settings) |  |
| [!UICONTROL Tax Calculation Method Based On] | `Total` |
| [!UICONTROL Tax Calculation Based On] | `Shipping Address` |
| [!UICONTROL Catalog Prices] | `Including Tax` |
| [!UICONTROL Shipping Prices] | `Including Tax` |
| [!UICONTROL Apply Customer Tax] | `After Discount` |
| [!UICONTROL Apply Discount on Prices] | `Including Tax` |
| [!UICONTROL Apply Tax On] | `Custom Price if available` |
| [[!UICONTROL Default Tax Destination Calculation]](../configuration-reference/sales/tax.md#default-tax-destination-calculation) |  |
| [!UICONTROL Default Country] | `France` |
| [!UICONTROL Default State] |  |
| [!UICONTROL Default Postal Code] | `*` （星號） |
| [[!UICONTROL Fixed Product taxes]](../configuration-reference/sales/tax.md#fixed-product-taxes) |  |
| [!UICONTROL Enable FPT] | `Yes` |
| [!UICONTROL All FPT Display Settings] | `Including FPT and FPT description` |
| [!UICONTROL Apply Discounts to FPT] | `No` |
| [!UICONTROL Apply Tax to FPT] | `Yes` |
| [!UICONTROL Include FPT in Subtotal] | `Yes` |

{style="table-layout:auto"}

### 步驟6：設定德國的稅捐設定

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在右上角，將&#x200B;**[!UICONTROL Store View]**&#x200B;設定為德文商店的檢視，然後按一下&#x200B;**[!UICONTROL OK]**&#x200B;確認。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Sales]**&#x200B;並選擇&#x200B;**[!UICONTROL Tax]**。

1. 在&#x200B;**[!UICONTROL Default Tax Destination Calculation]**&#x200B;區段中，執行下列動作：

   - 清除每個欄位後面的&#x200B;**[!UICONTROL Use Website]**&#x200B;核取方塊，

   - 若要符合您網站的送貨設定[來源點](shipping-settings.md#point-of-origin)，請更新下列值：

      - 預設國家
      - 預設狀態
      - 預設郵遞區號

     此設定可確保在產品價格包含稅捐時正確計算稅捐。

     ![預設稅捐目的地計算](./assets/destination-calc-french.png){width="600" zoomable="yes"}

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。
