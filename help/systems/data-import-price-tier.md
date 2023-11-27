---
title: 匯入層級價格
description: 瞭解如何匯出階層定價資料及匯入更新的資料。
exl-id: b19d0208-68b3-45ba-9896-318e12ff4131
feature: Products, Data Import/Export
source-git-commit: 55b0672984ce8cdb853daf024299919beaf7ce0b
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---

# 匯入層級價格

不要輸入 [層級價格](../catalog/product-price-tier.md) 手動針對每項產品執行下列作業會更有效率： [匯入](data-import.md) 定價資料。 開始之前，請先建立匯出的層級價格資料範例檔案，以作為範本使用。

![店面範例 — 分層定價](./assets/storefront-tier-pricing-water-bottle.png){width="700" zoomable="yes"}

## 步驟1：匯出層級價格資料

下列範例會匯出單一產品的層級定價資料。 然後，您可以使用匯出的資料作為大量匯入層級價格資料的範本。 若要進一步瞭解匯出進階定價資料，請參閱 [進階定價資料](data-attributes-product.md#advanced-pricing-attributes).

![產品階層式定價](./assets/price-tier-customer-group-discount.png){width="600" zoomable="yes"}

1. 開啟 _管理員_ 側欄，前往  **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. 在 _[!UICONTROL Export Settings]_，設定&#x200B;**[!UICONTROL Entity Type]**至 `Advanced Pricing`.

1. 在 **[!UICONTROL Entity Attributes]** 格點，向下捲動至SKU屬性並執行下列動作：

   - 針對以折扣百分比為基礎的層級價格，輸入要匯出的每個產品的SKU，以逗號分隔。

     ![資料匯出 — 產品SKU](./assets/price-tier-export-sku.png){width="600" zoomable="yes"}

   - 若為以固定金額為基準的層級價格，請輸入各產品的SKU。

   - 向下捲動並按一下 **[!UICONTROL Continue]**.

1. 在網頁瀏覽器的下載位置找到匯出檔案，然後開啟檔案。

   ![範例 — 匯出的客戶群組折扣層價格資料](./assets/price-tier-customer-group-discount-export.png){width="600" zoomable="yes"}

**_已匯出的層級價格資料_**

匯出的資料中包含下列欄：

- `sku`
- `tier_price_website`
- `tier_price_customer_group`
- `tier_price_qty`
- `tier_price`
- `tier_price_value_type`

您可以使用匯出的資料作為匯入層級價格資料的範本。

## 步驟2：更新資料

1. 視需要更新每個產品的層級價格資料。

   任何沒有層級價格更新的產品都可以從CSV檔案中刪除。 不需要重新匯入未變更的產品。

1. **[!UICONTROL Save]** 更新的CSV檔案。

>[!NOTE]
>
>匯入檔案的大小不能大於2 MB。

## 步驟3：匯入更新的資料

1. 開啟 _管理員_ 側欄，前往 **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. 在 _匯入設定_，設定 **[!UICONTROL Entity Type]** 至 `Advanced Pricing`.

1. 設定 **[!UICONTROL Import Behavior]** 至 `Add/Update`.

1. 在 **[!UICONTROL File to Import]**，按一下 **[!UICONTROL Choose File]** 並選取您準備從目錄中匯入的檔案。

1. 在右上角，按一下 **[!UICONTROL Check Data]**.

1. 如果檔案有效，請按一下 **[!UICONTROL Import]**.

   否則，請修正訊息中所列資料的每個問題，然後再次嘗試匯入檔案。
