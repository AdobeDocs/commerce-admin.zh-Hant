---
title: 層級定價
description: 瞭解如何使用層級定價，從產品清單或產品頁面提供數量折扣。
exl-id: b5810899-31a6-4288-9acc-09f7f4dfbd43
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# 層級定價

層級定價可讓您從店面的產品清單或產品頁面提供數量折扣。 折扣可套用至特定商店檢視或客戶群組或共用目錄。

如果您有許多產品要更新，匯入層級價格變更比個別輸入更有效率。 如需詳細資訊，請參閱 [匯入層級價格](../systems/data-import-price-tier.md).

![店面產品頁面上的層級價格](./assets/product-price-tier-storefront.png){width="700" zoomable="yes"}

產品頁面會計算數量折扣，並顯示下列訊息：

`Buy 6 for $5.95 each and save 15%`

店面中的價格會從最高數量優先至最低數量。 如果您有數量的層級價格 `5` 一個用於 `10`，而客戶新增五、六、七、八或九個專案至購物車，則客戶會收到數量的折扣價格 `5` 層級。 當客戶新增第十個專案時，為數量指定的折扣價格 `10` 層級會取代數量為 `5`，和折扣價 `10` 適用。

## 新增產品的價格層級

1. 在編輯模式中開啟產品。

1. 在 _[!UICONTROL Price]_欄位，按一下&#x200B;**[!UICONTROL Advanced Pricing]**.

1. 在 _[!UICONTROL Tier Price]_區段，按一下&#x200B;**[!UICONTROL Add]**.

   如果您要建立多個價格的階層，請按一下 **[!UICONTROL Add]** 針對每個額外層級，讓您可同時處理所有層級。 群組中的每個層級都有相同的網站和客戶群組或共用目錄指派，但數量和價格不同。

## 設定價格層

1. 如果您的商店有多個網站，請選擇 **[!UICONTROL Website]** 適用於的層級定價。

1. 如有必要，請選取 **[!UICONTROL Customer Group]** 或 **[!UICONTROL Shared Catalog]** (![適用於Adobe Commerce的B2B](../assets/b2b.svg) 提供方式 [適用於Adobe Commerce的B2B](./b2b/../introduction.md) 僅限)。

1. 的 **[!UICONTROL Qty]**，輸入必須訂購才能收到折扣的數量。

   - **方法1：** 輸入固定金額的價格

     設定 **[!UICONTROL Price]** 至 `Fixed` 並輸入該層級中一個單位的調整後價格。

     ![固定金額形式的層級價格](./assets/product-price-tier-fixed.png){width="600" zoomable="yes"}

   - **方法2：** 以百分比輸入價格

     設定 **[!UICONTROL Price]** 至 `Discount` 並輸入折扣價格，以產品基準價格的百分比表示。

     例如，若是15%的折扣，請輸入數字 `15`. (儲存價格時會有兩個小數位數，例如 `15.00`.)

     >[!NOTE]
     >
     >若要取得折扣價格，定義的百分比是根據 _[!UICONTROL Price]_ 欄位，而非 _[!UICONTROL Special Price]_ 欄位。

     ![百分比形式的層級價格](./assets/product-price-tier-discount.png){width="600" zoomable="yes"}

## 完成價格設定

1. 若要為不同的網站或客戶群組新增另一組層級定價，請重複上述步驟。

1. 完成後，按一下 **[!UICONTROL Done]** 然後 **[!UICONTROL Save]**.

>[!NOTE]
>
>此 **_final_** 產品價格的計算方式為 **_最小值_** 相關價格，使用下列公式： <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_固定價格_** 產品可自訂選項包括 _非_ 受「群組價格」、「層級價格」、「特殊價格」或「型錄價格」規則影響。
