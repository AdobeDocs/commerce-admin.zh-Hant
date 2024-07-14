---
title: 客戶區段
description: 客戶區段可讓您動態地向特定客戶顯示內容和促銷活動。
exl-id: b254a6ac-cb0b-46c1-9ef7-ffc97360a98e
source-git-commit: 0b9f394a792171e93ee72f3b4ebb904b96ea1051
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 0%

---

# 客戶區段

客戶區段可讓您根據各種屬性，以動態方式向特定客戶顯示內容和促銷活動。 例如客戶地址、訂單歷史記錄和購物車內容。 您可以根據具有購物車價格規則的目標區段，最佳化行銷方案。 您也可以產生報表並匯出目標客戶的清單。 由於客戶區段資訊會持續更新，因此當客戶在您的商店購物時，他們可能會與區段建立關聯或解除關聯。

若要更清楚瞭解[客戶群組](../customers/customer-groups.md)與客戶區段之間的差異，請注意其使用位置：

|  | 客戶區段 | 客戶群組 |
|--- |--- |--- |
| 目錄價格規則 |  | ✔️ |
| 購物車價格規則 | ✔️ | ✔️ |
| 層級價格 |  | ✔️ |
| 相關產品規則 | ✔️ |  |
| 動態區塊 | ✔️ |  |
| 獎勵匯率 |  | ✔️ |
| 類別許可權 |  | ✔️ |
| 邀請 |  | ✔️ |

{style="table-layout:auto"}

## 客戶區段屬性

客戶區段屬性的定義方式與購物車和目錄價格規則類似。 若要在客戶區段條件中使用屬性，_[!UICONTROL Use in Customer Segment]_[屬性](attribute-properties.md#)必須設定為`Yes`。 客戶區段條件可併入下列屬性型別：

| 屬性 | 說明 |
|---|---|
| `Customer Address Fields` | 您可以定義任何位址列位，例如城市或國家。 客戶通訊錄中的任何地址都可以符合這些條件，以便客戶符合。 或者，您可以指定只使用預設帳單或送貨地址來比對客戶。 客戶地址屬性僅適用於已登入其帳戶的客戶。 |
| `Customer Information Fields` | 您可以定義其他客戶資訊，包括客戶群組、名稱、電子郵件、電子報訂閱狀態以及商店信用餘額。 客戶資訊僅適用於已登入其帳戶的客戶。 |
| `Cart Fields` | 購物車屬性可以是根據購物車內容的數量（條列專案或總數量）或值（例如總計、稅金和禮品卡）。 |
| `Products` | 您可以參考目前位於購物車或願望清單中的產品，或先前已檢視或訂購的產品。 您也可以設定發生事件的日期範圍。 產品是使用產品屬性定義的。 |
| `Order Fields` | 過去訂單的訂單特性可根據訂單中的帳單/出貨地址、訂單的總金額（或平均值）或數量，或訂單總數來定義。 您也可以設定發生的日期範圍，以及符合這些條件的訂單狀態。 僅適用於已登入的客戶。 為未登入的購物者設定的條件會在他們登入時停止運作。 |

{style="table-layout:auto"}

如需定義客戶區段的詳細資訊，請參閱[建立及刪除客戶區段](../customers/customer-segment-create.md)。

## eBooks

- **客戶細分** — 取得[電子書](https://business.adobe.com/resources/identifying-your-most-profitable-customers-introduction-customer-segmentation.html)，瞭解如何提高利潤和整體客戶滿意度。
- **分段戰術** — 取得[電子書](https://business.adobe.com/resources/3-segmentation-tactics-ignite-conversion.html)以改進訊息和促銷活動的目標定位，與您的客戶建立有意義的對話。
