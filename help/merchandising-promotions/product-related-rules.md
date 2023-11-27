---
title: 相關產品規則
description: 瞭解相關的產品規則，以及如何使用這些規則來動態向您的客戶呈現相關產品、向上銷售和交叉銷售。
exl-id: ff566e13-cbe8-42f1-be3a-684e364b86dd
feature: Merchandising, Products, Storefront
source-git-commit: 91e6c63f1f6f16b957366f9d5cc651f9eded31c8
workflow-type: tm+mt
source-wordcount: '823'
ht-degree: 0%

---

# 相關產品規則（目標規則）

{{ee-feature}}

相關產品規則可讓您鎖定向客戶呈現為相關產品、向上銷售和交叉銷售的產品選擇。 每個產品規則都可以與 [客戶區段](../customers/customer-segments.md) 以產生目標銷售的動態顯示。

由於可同時觸發數個作用中規則，因此您可以為每個規則設定優先順序。 它會定義套用規則的順序以及產品在頁面上的顯示順序。

若要存取相關的產品規則，請前往 **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Related Product Rules]**.

![相關產品規則清單](./assets/related-products-rules.png){width="700" zoomable="yes"}

## 欄說明

| 欄 | 說明 |
|--- |--- |
| [!UICONTROL ID] | 指派給每個相關產品規則的唯一數值識別碼 |
| [!UICONTROL Rule] | 相關產品規則的名稱 |
| [!UICONTROL Start] | 使用動態行事曆欄位(_[!UICONTROL To:]_和_[!UICONTROL From:]_)，以根據建立規則時定義的規則開始日期來篩選清單。 |
| [!UICONTROL End] | 使用動態行事曆欄位(_[!UICONTROL To:]_和_[!UICONTROL From:]_)，以根據建立規則時定義的規則結束日期來篩選清單。 |
| [!UICONTROL Priority] | 在此欄位中輸入文字，以根據為規則定義的優先順序來篩選清單。 |
| [!UICONTROL Applies To] | 此選項會篩選套用至「 」的規則清單 `Related Products`， `Up-sells`、和 `Cross-sells`. |
| [!UICONTROL Status] | 使用此選項可依據規則狀態來篩選清單(`Active` 或 `Inactive`)。 |

{style="table-layout:auto"}

## 規則優先順序

在任何指定時間，都可能會觸發數個作用中規則來顯示相關產品、向上銷售和交叉銷售。 每個規則的優先順序會決定產品在頁面上出現的順序。 此值可設為任何整數，具有 `1` 有最高優先順序。

產品關係規則中可包含的產品ID數量由 `Result Limit` 值，其上限為20。 此 `Result Limit` 值，與 `Configurable Maximum` 對於特定規則型產品促銷活動，會變成 `Real Limit`，和會決定清單中可顯示的實際相符產品數量。

[結果限制] + [可設定的最大值] = [實際限制]

例如，假設您有三個規則的優先順序為 `1`， `2`、和 `3`.

- 有兩個相符的產品傳回 _規則1_，六個相符的產品 _規則2_&#x200B;和20種相符產品 _規則3_.
- 在設定中， _[!UICONTROL Maximum Number of Products for Related Products List]_設為 `6`.

  | 規則 | 優先順序 | 相符產品 |
  |---|---|-----|
  | 規則1 | `1` | `2` |
  | 規則2 | `2` | `6` |
  | 規則3 | `3` | `20` |

如果第一個規則傳回的比對產品多於 _可設定的最大限制_，但小於 _實際限制_，系統會使用其他規則中相符的產品（依優先順序），直到 _實際限制_ 已到達。

依優先順序，相符產品會從傳回 _規則1_ 可先用來填滿所有26個可用的插槽。 因為規則1隻傳回兩個相符的產品，所以還有24個的空間。 _規則2_ 具有次高優先順序，並傳回六個相符的產品。 現在有18個可用的位置需要填滿。 _規則3_ 擁有下一層級的優先順序，相符產品足以填滿剩餘的18個位置。 當所有可用的位置已填滿時，根據設定的旋轉模式，產品可能會依每個優先順序內的ID進行隨機或排序，然後減少到可設定的最大限制。 在此案例中，其餘六個產品會出現在商店中。

>[!NOTE]
>
>無論旋轉模式為何，選取的產品一律會顯示在規則型產品之前。

## 設定規則型產品關係

產品關係規則及相符產品顯示的行為取決於組態設定。 這些設定決定可顯示多少符合規則的產品及其顯示順序。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側的面板中，展開 **[!UICONTROL Catalog]** 並選擇 **[!UICONTROL Catalog]** 底下。

1. 展開 ![擴充](../assets/icon-display-expand.png) 此 **[!UICONTROL Rules-Based Product Relations]** 區段。

   ![目錄組態 — 規則型產品關係](../configuration-reference/catalog/assets/catalog-rule-based-product-relations.png){width="600" zoomable="yes"}

1. 輸入 **[!UICONTROL Maximum Number of Products in the Related Products List]**.

1. 設定 **[!UICONTROL Show Related Products]** 變更為下列其中一項：

   - `Both Selected and Rule Based`
   - `Selected Only`
   - `Rule-Based Only`

1. 設定 **[!UICONTROL Rotation Mode for Products in Related Product List]** 變更為下列其中一項：

   - `By Priority, Then by ID`
   - `By Priority, Then Random`
   - `Weighted Random`

1. 若要完成交叉銷售產品設定，請執行下列動作：

   - 輸入 **[!UICONTROL Maximum Number of Products in the Cross-Sell Product List]**.

   - 設定 **[!UICONTROL Show Cross-Sell Products]** 變更為下列其中一項：

      - `Both Selected and Rule Based`
      - `Selected Only`
      - `Rule-Based Only`

   - 設定 **[!UICONTROL Rotation Mode for Products in Cross-Sell Product List]** 變更為下列其中一項：

      - `By Priority, Then by ID`
      - `By Priority, Then Random`
      - `Weighted Random`

1. 若要完成追加銷售產品設定，請執行下列動作：

   - 輸入 **[!UICONTROL Maximum Number of Products in the Upsell Product List]**.

   - 設定 **[!UICONTROL Show Upsell Products]** 變更為下列其中一項：

      - `Both Selected and Rule Based`
      - `Selected Only`
      - `Rule-Based Only`

   - 設定 **[!UICONTROL Rotation Mode for Products in Upsell Product List]** 變更為下列其中一項：

      - `By Priority, Then by ID`
      - `By Priority, Then Random`
      - `Weighted Random`

1. 完成後，按一下 **[!UICONTROL Save Config]**.

### 旋轉模式

| 模式 | 說明 |
|---|---|
| [!UICONTROL By Priority, Then by ID] | 產品先依優先順序排序，然後依每個優先順序內的ID重新排序。 只有在高優先順序規則中沒有產品可填滿可用位置時，低優先順序規則的產品才會出現。 |
| [!UICONTROL By Priority, Then Random] | 產品會依優先順序排序，然後在每個優先順序內隨機化。 只有在高優先順序規則中沒有產品可填滿可用位置時，低優先順序規則的產品才會出現。 |
| [!UICONTROL Weighted Random] | 產品會隨機化，所以優先順序較高的規則所屬產品會比優先順序較低的規則所屬產品出現的可能性更高。 然後，產品會減少到可設定的最大限制，並按優先順序重新分組。 此模式讓較低優先順序的產品有機會偶爾出現，即使剩餘的插槽中可能已有較高優先順序的規則產品填滿 |

{style="table-layout:auto"}
