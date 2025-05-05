---
title: 稅捐類別
description: 瞭解如何設定用於稅捐規則的稅捐類別。
exl-id: dd867eba-3f1e-45a8-9332-9e668a2092e1
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 0%

---

# 稅捐類別

稅捐類別可指定給客戶、產品和出貨。 Commerce會分析每位客戶的購物車，並根據客戶類別、購物車中產品的類別以及地區計算適當的稅捐。 地區由客戶的送貨地址、帳單地址或送貨來源所決定。 定義[稅捐規則](tax-rules.md)時，可以建立新的稅捐類別。

- **客戶** — 您可以視需要建立儘可能多的客戶稅捐類別，並將其指派給[客戶群組](../customers/customer-groups.md)。 例如，在某些管轄區，批發交易不徵稅，但零售交易徵稅。 您可以將「批發客戶」群組的成員與「批發」稅捐類別建立關聯。

- **產品** — 在計算中使用產品類別，以決定購物車套用的正確稅率。 當您建立產品時，產品會指定給特定的稅捐類別。 例如，食物可能不徵稅，或按不同的稅率徵稅。

- **送貨** — 如果您的商店對送貨收取額外的稅金，您應該指定送貨的特定產品稅類。 然後在設定中，將其指定為用於出貨的稅捐類別。

## 設定稅捐類別

用於送貨的稅捐類別，以及[產品與客戶](#add-a-product-tax-class)的預設稅捐類別是在&#x200B;_[!UICONTROL Sales]_&#x200B;組態中設定的。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Sales]**&#x200B;並選擇&#x200B;**[!UICONTROL Tax]**。

1. 展開&#x200B;**[!UICONTROL Tax Classes]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![組態 — 稅捐類別](../configuration-reference/sales/assets/tax-tax-classes.png){width="600" zoomable="yes"}

1. 選擇下列各項的稅捐類別：

   - **[!UICONTROL Set Tax Class for Shipping]**
   - **[!UICONTROL Tax Class for Gift Options]**
   - **[!UICONTROL Default Tax Class for Product]**
   - **[!UICONTROL Default Tax Class for Customer]**

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

## 新增稅捐類別

您可以輕鬆新增客戶與產品的稅捐類別，然後將其指派給個別客戶與產品，並用於稅捐規則。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**。

1. 按一下&#x200B;**[!UICONTROL Add New Tax Rule]**。

1. 展開&#x200B;**[!UICONTROL Additional Settings]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![新增稅捐類別](./assets/tax-class-additional-settings.png){width="600" zoomable="yes"}

1. 在&#x200B;_客戶稅捐類別_&#x200B;下，按一下&#x200B;**[!UICONTROL Add New Tax Class]**。

1. 在文字方塊中輸入新稅捐類別的&#x200B;**[!UICONTROL Name]**。

   ![新增稅捐類別](./assets/tax-class-customer-add-new.png){width="600" zoomable="yes"}

1. 若要將新類別新增至可用客戶稅捐類別清單，請按一下核取記號。

   ![新稅捐類別](./assets/tax-classes-updated.png){width="600" zoomable="yes"}

## 新增產品稅捐類別

1. 在&#x200B;_產品稅捐類別_&#x200B;下，按一下&#x200B;**[!UICONTROL Add New Tax Class]**。

1. 在文字方塊中輸入新稅捐類別的&#x200B;**[!UICONTROL Name]**。

1. 若要將新類別新增至可用產品稅捐類別清單，請按一下核取記號。

1. 完成後，按一下按鈕列中的&#x200B;**[!UICONTROL Back]**&#x200B;以返回&#x200B;_稅捐規則_&#x200B;格線。

## 預設稅捐目的地

預設的稅捐目的地設定會決定用來作為稅捐計算基礎的國家、州、郵遞區號或郵遞區號。

**_若要設定計算的預設稅捐目的地：_**

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Sales]**&#x200B;並選擇&#x200B;**[!UICONTROL Tax]**。

1. 展開&#x200B;**[!UICONTROL Default Tax Destination Calculation]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![預設稅捐目的地計算](../configuration-reference/sales/assets/tax-default-tax-destination-calculation.png){width="600" zoomable="yes"}

1. 將&#x200B;**[!UICONTROL Default Country]**&#x200B;設為稅捐計算所依據的國家/地區。

1. 將&#x200B;**[!UICONTROL Default State]**&#x200B;設為用來作為稅捐計算基礎的州或省。

1. 將&#x200B;**[!UICONTROL Default Post Code]**&#x200B;設為郵遞區號，作為當地稅捐計算的基礎。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。
