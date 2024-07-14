---
title: 層級定價
description: 瞭解如何使用層級定價，從產品清單或產品頁面提供數量折扣。
exl-id: b5810899-31a6-4288-9acc-09f7f4dfbd43
feature: Catalog Management, Products
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%

---

# 層級定價

層級定價可讓您從店面的產品清單或產品頁面提供數量折扣。 折扣可套用至特定商店檢視或客戶群組或共用目錄。

如果您有許多產品要更新，匯入層級價格變更比個別輸入更有效率。 如需詳細資訊，請參閱[匯入層級價格](../systems/data-import-price-tier.md)。

店面產品頁面上的![層級價格](./assets/product-price-tier-storefront.png){width="700" zoomable="yes"}

產品頁面會計算數量折扣，並顯示下列訊息：

`Buy 6 for $5.95 each and save 15%`

店面中的價格會從最高數量優先至最低數量。 若您有數量為`5`的層級價格，且有`10`的層級價格，而客戶新增五、六、七、八或九個專案至購物車，則客戶會收到數量為`5`的層級折扣價格。 當客戶新增第十個專案時，為數量`10`層級指定的折扣價格會取代數量`5`的層級，且適用`10`的折扣價格。

## 新增產品的價格層級

1. 在編輯模式中開啟產品。

1. 在&#x200B;_[!UICONTROL Price]_欄位下方，按一下&#x200B;**[!UICONTROL Advanced Pricing]**。

1. 在&#x200B;_[!UICONTROL Tier Price]_區段中，按一下&#x200B;**[!UICONTROL Add]**。

   如果您要建立多個價格的階層，請按一下每個額外階層&#x200B;**[!UICONTROL Add]**，以便同時處理所有階層。 群組中的每個層級都有相同的網站和客戶群組或共用目錄指派，但數量和價格不同。

## 設定價格層

1. 如果您的商店有多個網站，請選擇套用層級定價的&#x200B;**[!UICONTROL Website]**。

1. 如有必要，請選取&#x200B;**[!UICONTROL Customer Group]**&#x200B;或&#x200B;**[!UICONTROL Shared Catalog]**&#x200B;來限制訂價層的可用性(![Adobe Commerce B2B](../assets/b2b.svg)僅適用於[Adobe Commerce B2B](./b2b/../introduction.md))。

1. 針對&#x200B;**[!UICONTROL Qty]**，輸入必須訂購才能收到折扣的數量。

   - **方法1：**&#x200B;輸入價格作為固定金額

     將&#x200B;**[!UICONTROL Price]**&#x200B;設為`Fixed`，並輸入該層級中一個單位的調整後價格。

     將![層級價格作為固定金額](./assets/product-price-tier-fixed.png){width="600" zoomable="yes"}

   - **方法2：**&#x200B;以百分比輸入價格

     將&#x200B;**[!UICONTROL Price]**&#x200B;設為`Discount`，並輸入折扣價格，做為產品基準價格的百分比。

     例如，若是15%的折扣，請輸入數字`15`。 （價格會以兩個小數點位置儲存，例如`15.00`。）

     >[!NOTE]
     >
     >若要取得折扣價格，已定義的百分比是根據&#x200B;_[!UICONTROL Price]_欄位中定義的值（而非_[!UICONTROL Special Price]_&#x200B;欄位）計算。

     以百分比形式![層級價格](./assets/product-price-tier-discount.png){width="600" zoomable="yes"}

## 完成價格設定

1. 若要為不同的網站或客戶群組新增另一組層級定價，請重複上述步驟。

1. 完成時，按一下&#x200B;**[!UICONTROL Done]**，然後按一下&#x200B;**[!UICONTROL Save]**。

>[!NOTE]
>
>使用下列公式，以&#x200B;**_最低_**&#x200B;相關價格計算&#x200B;**_最終_**&#x200B;產品價格： <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_固定價格_**&#x200B;產品可自訂選項&#x200B;_不_&#x200B;受群組價格、層級價格、特殊價格或目錄價格規則影響。
