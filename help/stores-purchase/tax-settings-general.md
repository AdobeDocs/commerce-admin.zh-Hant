---
title: 稅捐組態設定
description: 瞭解如何設定基本稅捐設定，包括稅捐類別、計算及預設稅捐目的地。
exl-id: e32747f9-20d0-4717-9cee-aa1bcffebb65
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1052'
ht-degree: 0%

---

# 稅捐組態設定

下列指示會帶您瞭解Commerce執行個體的基本稅務設定。 在設定您的稅捐之前，請確定您熟悉[地區設定](store-localize.md#step-3-change-the-locale-of-the-store-view)的稅捐需求。 接著，根據您的需求完成稅捐設定。

管理員[許可權](../systems/permissions.md)可設定為根據業務&#x200B;_需要知道_，限制[對稅務資源的存取權](../systems/permissions-user-roles.md)。 若要建立可存取稅捐設定的「管理員」角色，請選擇「銷售/稅捐」與「系統/稅捐」資源。 如果為不同於預設出貨點的地區設定網站，您也必須允許存取角色的「系統/出貨」資源。 出貨設定會決定用於型錄價格的商店稅率。

## 設定一般稅捐設定

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 若為多站台組態，請將&#x200B;**[!UICONTROL Store View]**&#x200B;設定為組態目標的網站和商店。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Sales]**&#x200B;並選擇&#x200B;**[!UICONTROL Tax]**。

1. 完成下列組態設定。

   如有必要，請清除任何變暗設定的&#x200B;**[!UICONTROL Use system value]**&#x200B;核取方塊。

### [!UICONTROL Tax Classes]

1. 展開&#x200B;**[!UICONTROL Tax Classes]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![稅捐類別](../configuration-reference/sales/assets/tax-tax-classes.png){width="600" zoomable="yes"}

   - **送貨稅捐類別** — 設定為適當的類別。 預設類別為： `None`和`Taxable Goods`
   - 贈品選項的&#x200B;**稅捐類別** — ![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)設定為適當的類別。 預設類別為： `None`和`Taxable Goods`
   - **產品的預設稅捐類別** — 設定為適當的類別。 預設類別為： `None`和`Taxable Goods`
   - **客戶的預設稅捐類別** — 設定為適當的類別。 預設類別為： `Retail Customer`和`Wholesale Customer`

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

### [!UICONTROL Calculation Settings]

1. 展開&#x200B;**[!UICONTROL Calculation Settings]**&#x200B;區段。

   ![計算設定](../configuration-reference/sales/assets/tax-calculation-settings.png){width="600" zoomable="yes"}

1. 將&#x200B;**[!UICONTROL Tax Calculation Method Based On]**&#x200B;設定為下列其中一項：

   - `Unit Price` — 每個產品的價格
   - `Row Total` — 訂單中的明細專案總計，減去折扣
   - `Total` — 訂單總計

1. 將&#x200B;**[!UICONTROL Tax Calculation Based On]**&#x200B;設定為下列其中一項：

   - `Shipping Address` — 將運送訂單的地址
   - `Billing Address` — 客戶或公司的帳單地址
   - `Shipping Origin` — 指定為您商店的[來源點](shipping-settings.md#point-of-origin)的地址

1. 將&#x200B;**[!UICONTROL Catalog Prices]**&#x200B;設為`Excluding Tax`或`Including Tax`。

1. 將&#x200B;**[!UICONTROL Shipping Prices]**&#x200B;設為`Excluding Tax`或`Including Tax`。

1. 將&#x200B;**[!UICONTROL Apply Customer Tax]**&#x200B;設為下列其中一項，以決定稅捐是套用至原始價格還是折扣價格： `After Discount`或`Before Discount`

1. 將&#x200B;**[!UICONTROL Apply Discount on Prices]**&#x200B;設為下列其中一項，以決定折扣是否包含或排除稅捐： `Excluding Tax`或`Including Tax`

1. 將&#x200B;**[!UICONTROL Apply Tax On]**&#x200B;設為`Custom price if available`或`Original price only`。

1. 將&#x200B;**[!UICONTROL Enable Cross-Border Trade]**&#x200B;設定為下列其中一項：

   - `Yes` — 在不同稅率間使用一致的定價。 如果型錄價格包含稅捐，請選擇此設定以修正價格，而不論客戶稅率為何。
   - `No` — 依稅率變更價格。

   >[!IMPORTANT]
   >
   >如果[跨境貿易](#cross-border-price-consistency)已啟用，利潤率會依稅率變更。 利潤由公式(`Revenue - CustomerVAT - CostOfGoodsSold`)決定。 若要啟用跨境貿易，必須將價格設定為包含稅捐。

### [!UICONTROL Default Tax Destination Calculation]

1. 展開&#x200B;**[!UICONTROL Default Tax Destination Calculation]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![預設稅捐目的地計算](../configuration-reference/sales/assets/tax-default-tax-destination-calculation.png){width="600" zoomable="yes"}

1. 指定稅捐計算的&#x200B;**[!UICONTROL Default Country]**。

1. 如果適用，請指定稅捐計算的&#x200B;**[!UICONTROL Default State]**。

1. 如果適用，請指定稅捐計算的&#x200B;**[!UICONTROL Default Post Code]**。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

### [!UICONTROL Price Display Settings]

>[!IMPORTANT]
>
>某些與價格顯示相關的設定組合（包含與排除稅捐）可能會讓客戶感到困惑。 若要避免觸發警告訊息，請參閱[建議的設定](taxes.md#warning-messages)。

1. 展開&#x200B;**[!UICONTROL Price Display Settings]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![價格顯示設定](../configuration-reference/sales/assets/tax-price-display-settings.png){width="600" zoomable="yes"}

1. 將&#x200B;**[!UICONTROL Display Product Prices in Catalog]**&#x200B;設定為下列其中一項：

   - `Excluding Tax` — 店面中顯示的目錄價格不含稅金。
   - `Including Tax` — 只有當稅捐規則符合稅捐來源，或客戶的地址符合稅捐規則時，店面中的型錄價格才會包含稅捐。 客戶建立帳戶、登入或使用購物車中的預估稅金和送貨工具後，可能會發生此狀況。
   - `Including and Excluding Tax` — 在店面中顯示的目錄價格會同時顯示含稅與不含稅。

1. 將&#x200B;**[!UICONTROL Display Shipping Prices]**&#x200B;設為`Excluding Tax`、`Including Tax`或`Including and Excluding Tax`。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

### [!UICONTROL Shopping Cart Display Settings]

1. 展開&#x200B;**[!UICONTROL Shopping Cart Display Settings]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![購物車顯示設定](../configuration-reference/sales/assets/tax-shopping-cart-display-settings.png){width="600" zoomable="yes"}

1. 針對下列各項設定，根據您的商店和地區設定要求，選擇稅金和價格在購物車中的顯示方式：

   - 將&#x200B;**[!UICONTROL Display Prices]**&#x200B;設為`Excluding Tax`、`Including Tax`或`Including and Excluding Tax`。

   - 將&#x200B;**[!UICONTROL Display Subtotal]**&#x200B;設為`Excluding Tax`、`Including Tax`或`Including and Excluding Tax`。

   - 將&#x200B;**[!UICONTROL Display Shipping Amount]**&#x200B;設為`Excluding Tax`、`Including Tax`或`Including and Excluding Tax`。

   - ![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)將&#x200B;**[!UICONTROL Display Gift Wrapping Prices]**&#x200B;設為`Excluding Tax`、`Including Tax`或`Including and Excluding Tax`。

   - ![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)將&#x200B;**[!UICONTROL Display Printed Card Prices]**&#x200B;設為`Excluding Tax`、`Including Tax`或`Including and Excluding Tax`。

1. 根據您的需求，將下列顯示選項設定為`Yes`或`No`：

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

### [!UICONTROL Orders, Invoices, Credit Memos Display Settings]

1. 展開![展開](../assets/icon-display-expand.png) **[!UICONTROL Orders, Invoices, Credit Memos Display Settings]**&#x200B;區段。

   ![訂單、發票、銷退折讓單顯示設定](../configuration-reference/sales/assets/tax-orders-invoices-credit-memos-display-settings.png){width="600" zoomable="yes"}

1. 指定訂單、商業發票及銷退折讓單中價格與稅捐的顯示方式：

   - 將&#x200B;**[!UICONTROL Display Prices]**&#x200B;設為`Excluding Tax`、`Including Tax`或`Including and Excluding Tax`。

   - 將&#x200B;**[!UICONTROL Display Subtotal]**&#x200B;設為`Excluding Tax`、`Including Tax`或`Including and Excluding Tax`。

   - 將&#x200B;**[!UICONTROL Display Shipping Amount]**&#x200B;設為`Excluding Tax`、`Including Tax`或`Including and Excluding Tax`。

   - ![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)將&#x200B;**[!UICONTROL Display Gift Wrapping Prices]**&#x200B;設為`Excluding Tax`、`Including Tax`或`Including and Excluding Tax`。

   - ![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)將&#x200B;**[!UICONTROL Display Printed Card Prices]**&#x200B;設為`Excluding Tax`、`Including Tax`或`Including and Excluding Tax`。

1. 根據您的需求，將下列顯示選項設定為`Yes`或`No`：

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

### [!UICONTROL Fixed Product Taxes]

1. 展開&#x200B;**[!UICONTROL Fixed Product Taxes]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![固定產品稅金](../configuration-reference/sales/assets/tax-fixed-product-taxes.png){width="600" zoomable="yes"}

1. 根據您的需求，將&#x200B;**[!UICONTROL Enable FPT]**&#x200B;設定為`Yes`或`No`。

1. 如果已啟用FPT，請指定FPT顯示選項：

   - **[!UICONTROL Display Prices in Product Lists]**
   - **[!UICONTROL Display Price On Product view Page]**
   - **[!UICONTROL Display Prices in Sales Modules]**
   - **[!UICONTROL Display Prices in Emails]**

   - `Including FPT Only` — 顯示的價格包含固定產品稅金。 FPT金額不會單獨顯示。
   - `Including FPT and FPT description` — 顯示的價格包含固定產品稅金。 FPT金額會個別顯示。
   - `Excluding FPT. Including FPT description and final price` — 顯示的價格不包含固定的產品稅金。 FPT金額會個別顯示。
   - `Excluding FPT` — 顯示的價格不包含固定的產品稅金。 FPT金額不會單獨顯示。

1. 根據您的需求，將&#x200B;**[!UICONTROL Apply Discounts to FPT]**&#x200B;設為`Yes`或`No`。

1. 設定&#x200B;**[!UICONTROL FPT Tax Configuration]**&#x200B;以決定如何計算FPT。

   - `Not Taxed` — 如果您的課稅管轄區不對FPT課稅，請選取此選項。 （例如，加州。）
   - `Taxed` — 如果您的課稅管轄區對FPT課稅，請選取此選項。 （例如，加拿大。）
   - `Loaded and Displayed with Tax` — 如果在套用稅捐之前將FPT加入訂單總計，請按一下此選項。 （例如，歐盟國家。）

1. 根據您的需求，將&#x200B;**[!UICONTROL Include FPT in Subtotal]**&#x200B;設為`Yes`或`No`。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

## 跨境價格一致性

跨境貿易（也稱為價格一致性）支援歐盟(EU)和其他商家，這些商家的稅率與商店稅率不同的客戶，會維持一致價格。

在地區和地理區域之間運作的商家，可以將稅捐納入產品價格中，以顯示單一價格。 無論不同國家/地區的稅捐結構與稅率有何差異，訂價都是乾淨且整潔的。 這些設定需要從[Marketplace](../getting-started/commerce-marketplace.md) （例如&#x200B;_Vertex Cloud_）安裝稅捐計算延伸。

>[!NOTE]
>
>啟用跨境交易時，利潤率會依稅率變更。 利潤由下列公式決定：<br>
>`Revenue - CustomerVAT - CostOfGoodsSold`

**_若要啟用跨境價格一致性：_**

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 若為多站台組態，請將&#x200B;**[!UICONTROL Store View]**&#x200B;設定為組態目標的網站和商店。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Sales]**&#x200B;並選擇&#x200B;**[!UICONTROL Tax]**。

1. 展開&#x200B;**[!UICONTROL Calculation Settings]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

1. 將&#x200B;**[!UICONTROL Catalog Prices]**&#x200B;設為`Including Tax`。

1. 若要啟用跨境價格一致性，請將&#x200B;**[!UICONTROL Enable Cross Border Trade]**&#x200B;設為`Yes`。

   ![啟用跨境交易設定](./assets/cross-border-calculations-settings.png){width="600" zoomable="yes"}

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。
