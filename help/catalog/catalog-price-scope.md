---
title: 價格範圍
description: 瞭解用於產品價格的範圍，其可設定為在全域或網站層級套用。
exl-id: 3726b16b-4ed5-4286-a7fd-69ed6677f87a
feature: Catalog Management, Products
source-git-commit: bc3977f29c8048a1b8578aa21fa55fa1a4d903f2
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 0%

---

# 價格範圍

用於產品價格的[基本貨幣](../stores-purchase/currency-configuration.md)範圍可以設定為套用至全域或網站層級。 如果套用至全域層級，整個商店階層都會使用相同的價格。 如果套用至網站層級，則會以不同價格，從與不同網站相關聯的商店取得相同的產品。 依預設，產品定價的範圍是全球性的。

不同的因素可能會影響同一產品在不同地點的價格，而非不同地點。 例如，產品可能有額外的銷售成本，以及其他會影響特定商店中銷售產品價格的考量因素。 下圖顯示將基本貨幣設定為網站層級的多站台安裝。 與每個網站相關聯的商店和商店檢視會反映在網站層級設定的產品定價。

![Adobe Commerce B2B](../assets/b2b.svg)如果您使用共用目錄，請參考[Adobe Commerce B2B指南](../b2b/catalog-shared-pricing-structure.md)中的&#x200B;_設定共用目錄定價和結構_。

![價格範圍圖表](./assets/catalog-price-scope.svg){width="550"}

## 設定價格範圍

1. 在&#x200B;_管理員_&#x200B;功能表中，前往&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Catalog]**&#x200B;並在下方選擇&#x200B;**[!UICONTROL Catalog]**。

1. 向下捲動至&#x200B;**[!UICONTROL Price]**&#x200B;區段，並將&#x200B;**[!UICONTROL Catalog Price Scope]**&#x200B;設定為下列其中一項：

   - `Global`
   - `Website`

   您選擇的範圍設定會顯示在目錄的價格欄位下方。

   ![目錄價格範圍](./assets/catalog-price.png){width="600" zoomable="yes"}

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

## 使用範圍設定產品價格

Commerce不允許為每個商店設定產品價格。 但您可以變更每個網站的價格：

1. 在&#x200B;_管理員_&#x200B;功能表中，前往&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Catalog]**&#x200B;並在下方選擇&#x200B;**[!UICONTROL Catalog]**。

1. 在&#x200B;**[!UICONTROL Price]**&#x200B;索引標籤中，將價格範圍設定為`Website`而非`Global`。

1. 開啟產品編輯頁面，選取左上方的範圍，然後輸入每個網站的新價格，藉此設定價格。

在極少數情況下，當價格範圍設定為`Global`時，Commerce資料庫在網站層級上仍可能有不同的價格。 這可能是由於Commerce外部的同步問題而發生。 在這些情況下，商家必須在商店層級執行價格清理，並透過Commerce服務執行目錄同步。