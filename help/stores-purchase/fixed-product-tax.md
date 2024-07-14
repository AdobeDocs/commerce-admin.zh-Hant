---
title: 固定產品稅金(FPT)
description: 瞭解如何設定必須新增至特定產品型別的固定產品稅(FPT)。
exl-id: f1b475cb-a6fe-4b51-a0c3-7d0a202bd332
feature: Checkout, Invoices, Taxes, Products
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '872'
ht-degree: 0%

---

# 固定產品稅金(FPT)

有些稅捐管轄區有固定稅捐，必須新增至特定型別的產品。 您可以視需要設定&#x200B;_固定產品稅捐_ (FPT)，以計算商店的稅捐。 在某些國家，FPT可用於設定廢棄電子電氣裝置(WEEE)稅。 此稅捐也稱為&#x200B;_生態稅_&#x200B;或&#x200B;_環保稅_，是收集於特定型別的電子產品，以抵消回收成本。 這是固定金額，而不是產品價格的百分比。

根據產品，在料號層次套用固定產品稅捐。 在某些管轄區中，此稅捐會以額外%的稅捐計算為準。 您的稅捐管轄區可能也會有規則，說明產品價格如何顯示給客戶，無論是否含稅。 請務必瞭解規則並據此設定FPT顯示選項。

在電子郵件中引用FPT價格時，請務必小心，因為價格的差異可能會影響客戶對其訂單的信心。 例如，如果您顯示「訂單複查」價格而沒有顯示FPT，則購買具有相關FPT之料號的客戶會看到包含FPT稅捐金額但不包含明細細分的總計。 價格差異可能會導致部分客戶捨棄購物車，因為總額與預期金額不同。

## FPT顯示價格

| FPT | 顯示設定和計算 | |
|--- |--- |---|
| 未納稅 | **[!UICONTROL Excluding FPT]** | FPT會在購物車中顯示為單獨的列，而值會用於適當的稅捐計算。 |
| | **[!UICONTROL Including FPT]** | FPT會加入至料號的基本價格；但不包含在稅捐規則計算中。 |
| | **[!UICONTROL Excluding FPT, FPT Description, Final Price]** | 價格不含FPT金額或說明。 FPT不包含在稅捐規則型計算中。 |
| 已納稅 | **[!UICONTROL Excluding FPT]** | FPT會在購物車中顯示為單獨的列，而值會用於適當的稅捐計算。 |
| | **[!UICONTROL Including FPT]** | FPT包含在料號的價格中，且不需要變更稅捐計算。 |
| | **[!UICONTROL Excluding FPT, FPT Description, Final Price]** | 價格不含FPT金額或說明。 不過，FPT會包含在以稅捐規則為基準的計算中。 |

{style="table-layout:auto"}

## 設定FPT

固定產品稅捐(FPT) [輸入型別](../catalog/attributes-input-types.md)會建立欄位區段，用以管理每個區域的稅捐。

下列指示顯示如何使用「工程變更稅」作為範例，來設定商店的固定產品稅。 在設定稅捐的範圍以及稅捐套用的國家/地區與州之後，根據您選擇的選項，輸入欄位可以根據當地需求變更。 若要深入瞭解，請參閱[建立產品屬性](../catalog/attribute-product-create.md)。

### 步驟1：啟用固定產品稅捐

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Sales]**&#x200B;並選擇&#x200B;**[!UICONTROL Tax]**。

1. 展開&#x200B;**[!UICONTROL Fixed Product Taxes]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

1. 將&#x200B;**[!UICONTROL Enable FPT]**&#x200B;設為`Yes`。

1. 若要決定固定產品稅捐在商店價格中的使用方式，請選擇下列各價格顯示地點的FPT設定：

   - **[!UICONTROL Display Prices in Product Lists]**
   - **[!UICONTROL Display Prices on Product View Page]**
   - **[!UICONTROL Display Prices in Sales Modules]**
   - **[!UICONTROL Display Prices in Emails]**

   選項（每個選項相同）：

   - `Including FPT Only`
   - `Including FPT and FPT description`
   - `Excluding FPT. Including FPT description and final price`
   - `Excluding FPT`

1. 視需要設定&#x200B;**[!UICONTROL Apply Tax to FPT]**。

1. 視需要設定&#x200B;**[!UICONTROL Include FPT in Subtotal]**。

   ![固定產品稅金](../configuration-reference/sales/assets/tax-fixed-product-taxes.png){width="600" zoomable="yes"}

   如需這些組態設定的詳細說明，請參閱&#x200B;_組態參考指南_&#x200B;中的[固定產品稅額](../configuration-reference/sales/tax.md#fixed-product-taxes)。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

### 步驟2：建立FPT屬性

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**。

1. 按一下右上角的&#x200B;**[!UICONTROL Add New Attribute]**&#x200B;並執行下列動作：

   - 針對&#x200B;**[!UICONTROL Default Label]**，輸入識別屬性的標籤。

   - 將&#x200B;**[!UICONTROL Catalog Input for Store Owner]**&#x200B;設為`Fixed Product Tax`。

   ![屬性屬性](./assets/tax-fpt-attribute-properties.png){width="600" zoomable="yes"}

1. 展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Advanced Attribute Properties]**&#x200B;區段並設定屬性選項：

   - **[!UICONTROL Attribute Code]** — 以小寫輸入唯一識別碼，不含空格或特殊字元。 長度上限為30個字元。 您可以將「預設標籤」欄位的文字保留為空白。

   - **[!UICONTROL Add to Column Options]** — 若您希望FPT欄位出現在[產品清單](../catalog/products-list.md)中，請設定為`Yes`。

   - **[!UICONTROL Use in Filter Options]** — 如果您想要能夠根據FPT欄位的值[篩選格線中的](../getting-started/admin-workspace.md)產品，請設定為`Yes`。

   ![進階屬性屬性](./assets/tax-fpt-advanced-attribute-properties.png){width="600" zoomable="yes"}

1. （選擇性）在左側面板中，選擇&#x200B;**[!UICONTROL Manage Labels]**&#x200B;並輸入要使用的標籤，而不是每個商店檢視的預設標籤。

   ![管理標籤](./assets/attribute-new-manage-labels.png){width="600" zoomable="yes"}

1. 完成時，按一下&#x200B;**[!UICONTROL Save Attribute]**。

1. 出現提示時，請重新整理[快取](../systems/cache-management.md)。

### 步驟3：將FPT屬性新增至屬性集

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**。

1. 在清單中，按一下屬性集以在編輯模式中開啟記錄。

   ![屬性集清單](./assets/attribute-sets-list.png){width="600" zoomable="yes"}

1. 將FPT屬性從右側的&#x200B;**[!UICONTROL Unassigned Attributes]**&#x200B;清單拖曳到中心欄中的&#x200B;**[!UICONTROL Groups]**&#x200B;清單。

   每個群組資料夾都與產品資訊的某個區段相對應。 當產品以編輯模式開啟時，您可以將屬性放置到您希望出現的位置。

   ![編輯屬性集](./assets/tax-fpt-attribute-set-drag.png){width="600" zoomable="yes"}

1. 完成時，按一下&#x200B;**[!UICONTROL Save]**。

1. 請針對每個應包含固定產品稅捐的屬性集重複此步驟。

### 步驟4：將FPT套用至特定產品

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Products]**。

1. 在編輯模式中開啟需要固定產品稅的產品。

1. 尋找您新增至屬性集的欄位的&#x200B;**[!UICONTROL FPT]**&#x200B;區段，然後按一下&#x200B;**[!UICONTROL Add Tax]**。

1. 指定產品的適用稅捐：

   加拿大的![固定產品稅](./assets/tax-product-fpt-canada.png){width="600" zoomable="yes"}

   - 如果您的Commerce執行個體有多個網站，請選擇適當的&#x200B;**[!UICONTROL Website]**&#x200B;和基本貨幣。 在此範例中，欄位預設設定為`All Websites [USD]`。

   - 將&#x200B;**[!UICONTROL Country/State]**&#x200B;設定為固定產品稅適用的地區。

   - 針對&#x200B;**[!UICONTROL Tax]**，輸入固定產品稅捐作為小數金額。

1. 若要新增更多固定產品稅捐，請按一下&#x200B;**[!UICONTROL Add Tax]**&#x200B;並重複此程式。

1. 完成時，按一下&#x200B;**[!UICONTROL Save]**。
