---
title: 群組定價
description: 瞭解如何使用群組定價，根據您商店中的客戶群組來設定折扣專案的價格。
exl-id: bc5be23f-64eb-47c3-beda-01168abfbf96
feature: Catalog Management, Products, Customers
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 0%

---

# 群組定價

您可以使用「管理員」中的產品組態設定，根據商店中的客戶群組來設定折扣專案的價格。 此策略定價模型稱為 _群組定價_.

當購物者登入其帳戶時，任何產品的折扣價格都可向特定客戶群組的成員提供。 客戶群組價格會與一般價格一起顯示在產品頁面上，讓購物者可以輕鬆比較價格並據以行動。 當他們將產品新增到購物車後，一般價格會由根據客戶群組的群組價格取代。

客戶群組的定價是以下專案的元件： [階層式定價](product-price-tier.md) 和的設定方式類似。 唯一的差異在於客戶群組價格的數量為1。

![客戶群組折扣](./assets/storefront-price-group.png){width="600" zoomable="yes"}

## 使用群組定價的好處

- 適合批發買家

- 鼓勵客戶升級其客戶群組，以利用折扣

- 目標式行銷活動

- 獎勵忠實客戶，建立信任和信譽

## 設定群組價格

1. 在編輯模式中開啟產品。

1. 在 _[!UICONTROL Price]_欄位，按一下&#x200B;**[!UICONTROL Advanced Pricing]**.

1. 在 _[!UICONTROL Customer Group Price]_區段，按一下&#x200B;**[!UICONTROL Add]**.

   如果您的商店包括 [Adobe Commerce B2B](../b2b/introduction.md) 和 [共用目錄](../b2b/catalog-shared.md) 已啟用，此區段標示為 _[!UICONTROL Catalog and Tier Price]_.

   ![進階定價](./assets/product-price-group.png){width="600" zoomable="yes"}

1. 設定群組價格：

   - 如果是多站台安裝，請選擇 **[!UICONTROL Website]** 適用群組價格的地方。

   - 選擇 **[!UICONTROL Customer Group]** 即會收到折扣。

   - 輸入 **[!UICONTROL Quantity]** 之 `1`.

   - 的 **[!UICONTROL Price]**，設定訂價型別和金額：

      - `Fixed`  — 輸入折扣產品價格。

      - `Discount`  — 以產品價格的百分比輸入折扣價格。

     ![客戶群組定價](./assets/product-price-group-discount.png){width="600" zoomable="yes"}

1. 若要新增其他群組價格，請按一下 **[!UICONTROL Add]** 並重複上一步驟。

1. 完成後，按一下 **[!UICONTROL Done]** 然後 **[!UICONTROL Save]**.

>[!NOTE]
>
>此 **_final_** 產品價格的計算方式為 **_最小值_** 相關價格，使用下列公式： <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_固定價格_** 產品可自訂選項包括 _非_ 受「群組價格」、「層級價格」、「特殊價格」或「型錄價格」規則影響。
