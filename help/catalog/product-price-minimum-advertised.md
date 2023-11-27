---
title: 最低廣告價格
description: 瞭解如何使用最低廣告價格(MAP)功能，以符合製造商的特殊定價需求。
exl-id: ccd44cfe-3967-4d82-b5b2-3f92701d152e
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1133'
ht-degree: 0%

---

# 最低廣告價格

商家有時被禁止顯示低於製造商建議零售價(MSRP)的價格。 最低廣告價格(MAP)可讓您符合製造商的要求，同時為客戶提供更優惠的價格。 由於各製造商的需求不盡相同，因此您可以設定商店，以防止在不允許顯示實際價格的頁面上顯示。

MAP功能會新增一個專用的 _按一下以取得價格_ 連結而非一般產品價格。 若您店內的價格低於該產品的最低設定價格，則有兩種方法可以在店面處理價格資訊。 第一種方式是不顯示價格。 如果購買者按一下 _按一下以取得價格_ 按鈕，之後才會顯示您銷售產品的實際價格。 第二種方式是以刪除線顯示清單/市價，強調您的價格較低。

此外，MAP功能可讓您提出一些改善建議。 例如，當客戶將這類產品新增到購物車時，他們不會重新導向到購物車，而是會顯示一些優惠方案，讓購買者：

- 從購物車中移除專案（如果購買者只想釐清價格且尚未做出購買決定，即可完成）

- 將其留在購物車中並繼續購物

- 繼續結帳

## 對應邏輯

有些產品的價格取決於選取的選項，例如自訂選項或具有自己SKU和庫存管理的簡單產品)。 對於這些產品，會根據產品型別和價格設定套用以下邏輯。 實際價格用於訂單管理、客戶管理工具和報表。

## 搭配產品型別使用MAP

| 產品型別 | 說明 |
|--- |--- |
| [簡單](product-create-simple.md)， [虛擬](product-create-virtual.md) | 實際價格不會自動顯示在目錄清單和產品頁面上，但只會根據 [!UICONTROL Display Actual Price] 設定。 自訂選項價格正常顯示。 |
| [已分組](product-create-grouped.md) | 相關簡單產品的價格不會自動出現在目錄清單和產品頁面上，而只會根據 [!UICONTROL Display Actual Price] 設定。 |
| [可設定](product-create-configurable.md) | 實際價格不會自動顯示在目錄清單和產品頁面上，但只會根據 [!UICONTROL Display Actual Price] 設定。 選項價格正常顯示。 |
| [組合](product-create-bundle.md) （含固定價格） | 實際價格不會自動顯示在目錄頁面上，但只會根據 [!UICONTROL Display Actual Price] 設定。 組合專案的價格會正常顯示。 MAP不適用於具有動態定價的套件組合產品。 |
| [可下載](product-create-downloadable.md) | 實際價格不會自動顯示在目錄清單和產品頁面上，但只會根據 [!UICONTROL Display Actual Price] 設定。 每個下載連結的相關價格會正常顯示。 |

{style="table-layout:auto"}

## 搭配價格設定使用MAP

| 價格設定 | 說明 |
|--- |--- |
| 主要價格 | 當將MAP套用至主要價格時，選項、搭售專案和相關產品的價格（會從主要價格中增加或減少）通常會出現。 |
| 相關聯的產品價格 | 如果產品沒有主要價格，且其價格衍生自相關聯的產品價格（例如在群組產品中），則會套用相關聯產品的MAP設定。 |
| [MSRP](product-price-minimum-advertised.md) | 如果購物車中的產品指定了製造商的建議零售價(MSRP)，則不會忽略價格。 |
| [層級價格](product-price-tier.md) | 若已設定層級訂價，則不會在目錄中顯示層級訂價訊息。 在產品頁面上，會顯示通知，指出訂購超過特定數量時價格可能較低，但折扣僅以百分比顯示。 對於已分組產品的相關產品，折扣不會顯示在產品頁面上。 層級價格會根據「顯示實際價格」設定顯示。 |
| [特殊價格](product-price-special.md) | 如果指定了「特價」，則會根據「顯示實際價格」設定來顯示特價。 |

## 地圖設定

依預設不會啟用「最低廣告價格」(MAP)功能。 如果您想要將此功能新增到您的商店，您必須啟用它並設定產品的MAP設定。 MAP設定可套用至目錄中的所有產品，或針對特定產品進行設定。 全球啟用MAP時，店面中的所有產品價格都會隱藏起來，無法檢視。 您可以利用多種組態選項來維持與製造商的合約條款一致，同時仍為客戶提供更優惠的價格。

![實際價格顯示「手勢上」](./assets/storefront-msrp-on-gesture.png){width="700" zoomable="yes"}

在全域層級，您可以啟用或停用MAP，將其套用至所有產品，定義實際價格的顯示方式。 您也可以編輯出現在存放區中的相關訊息和資訊提示的文字。

啟用MAP時，產品層級的MAP設定即變為可用。 您可以輸入MSRP並選擇實際價格在商店中的顯示方式，將MAP套用至個別產品。 產品層級MAP設定會覆寫全域MAP設定。

![按一下以取得價格](./assets/storefront-price-map.png){width="700" zoomable="yes"}

### 步驟1：為存放區檢視啟用MAP

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 如果適用，請設定 **[!UICONTROL Store View]** 位於組態套用所在檢視的右上角。

1. 在左側面板中，展開 **[!UICONTROL Sales]** 並選擇 **[!UICONTROL Sales]** 底下。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 _[!UICONTROL Minimum Advertised Price]_區段。

1. 如有必要，請設定 **啟用地圖** 至 `Yes`.

   ![地圖設定](./assets/sales-minimum-advertised-price.png){width="600" zoomable="yes"}

   如需這些組態選項的詳細清單，請參閱 [_最低廣告價格_](../configuration-reference/sales/sales.md#minimum-advertised-price) 在 _設定參考_.

### 步驟2：設定MAP設定

使用下列其中一種方法來設定MAP設定：

#### 方法1：為所有產品設定MAP

1. 若要決定要在何時何地讓客戶看到實際價格，請執行下列步驟：

   - 若要變更預設值，請取消選取 **[!UICONTROL Use system value]** 核取方塊。

   - 設定 **顯示實際價格** 變更為下列其中一項：
      - `In Cart`
      - `Before Order Confirmation`
      - `On Gesture (on click)`

1. 輸入您要在 **[!UICONTROL Default Popup Text Message]**.

1. 輸入您希望在 **[!UICONTROL Default "What's This" Text Message]**.

1. 完成後，按一下 **[!UICONTROL Save Config]**.

#### 方法2：為單一產品設定MAP

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Catalog]** > **[!UICONTROL Inventory]** > **[!UICONTROL Products]**.

1. 在中開啟產品 **[!UICONTROL Edit]** 模式。

1. 在左側面板中，展開 **[!UICONTROL Advanced Settings]** 並選擇 **[!UICONTROL Advanced Pricing]**.

   >[!NOTE]
   >
   >此 [!UICONTROL Manufacturer's Suggested Retail Price] 和 [!UICONTROL Display Actual Price] 欄位僅在 [最低廣告價格](../configuration-reference/sales/sales.md#minimum-advertised-price) 在設定中啟用。

1. 輸入 **[!UICONTROL Manufacturer's Suggested Retail Price]** (MSRP)。

   在此範例中，產品價格為$54.00，而MSRP為59.95。

   ![製造商建議的零售價](./assets/product-price-msrp.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Display Actual Price]** 變更為下列其中一項：

   - `Use config` - （預設）套用顯示設定為 [已設定](../configuration-reference/sales/sales.md#minimum-advertised-price) 存放區的。 |
   - `On Gesture`  — 當客戶按一下 _按一下以取得價格_ 或 _這是什麼？_ 連結。
   - `In Cart`  — 顯示購物車中的實際產品價格。
   - `Before Order Confirmation`  — 在訂單確認前，於結帳程式結束時顯示實際產品價格。

1. 完成後，按一下 **[!UICONTROL Done]** 然後 **[!UICONTROL Save]**.
