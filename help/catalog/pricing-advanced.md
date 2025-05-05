---
title: 進階定價
description: 瞭解Adobe Commerce提供的進階價格控制項。
exl-id: 0f353341-1b6b-4093-bba9-4a1b88323f8a
feature: Catalog Management, Products
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '874'
ht-degree: 0%

---

# 進階定價

Adobe Commerce和Magento Open Source支援各種價格選項，可用於促銷活動，或符合製造商的最低廣告定價需求。 產品定價的變更可以依排程進行，或依產品層級或購物車中套用的價格規則進行。

使用進階價格管理您產品的價格，為客戶提供更優惠的價格，鼓勵消費者增加支出、增加您網站的流量，並清除舊存貨。

_[!UICONTROL Advanced Pricing]_&#x200B;設定定義特定客戶群組或共用目錄可用的特殊定價所需條件。 進階定價可套用至簡單、虛擬、可下載和套裝等產品。 若要將折扣價格套用至其他產品型別，請使用[目錄價格規則](../merchandising-promotions/price-rules-catalog.md)。 如需詳細資訊，請參閱[價格範圍](catalog-price-scope.md)。

進階定價資料會與產品頁面同步。 例如，如果您更新層級價格數量，系統會更新產品頁面上的值。

![Adobe Commerce B2B](../assets/b2b.svg) (僅適用於[Adobe Commerce B2B](./b2b/../introduction.md))如果您使用共用目錄，進階定價資料會與產品頁面和共用目錄同步。 例如，如果您更新層級價格數量，則系統會更新共用目錄和產品頁面上的值。 共用目錄中所指示的任何自訂訂訂價格都會優先於客戶群組定價。 另請參閱&#x200B;_Adobe Commerce B2B指南_&#x200B;中的[設定共用目錄定價和結構](https://experienceleague.adobe.com/docs/commerce-admin/b2b/shared-catalogs/define/catalog-shared-pricing-structure.html?lang=zh-Hant)。

![進階價格](./assets/product-pricing-advanced-link.png){width="600" zoomable="yes"}

## 存取進階訂價選項

1. 在編輯模式中開啟產品。

1. 在&#x200B;**[!UICONTROL Price]**&#x200B;底下，按一下&#x200B;**[!UICONTROL Advanced Pricing]**。

1. 請遵循所需進階訂價型態的指示。

   - [群組價格](product-price-group.md)

   - [特殊價格](product-price-special.md)

   - [層級價格](product-price-tier.md)

   - [最低廣告價格](product-price-minimum-advertised.md)

## 頁面引用

### [!UICONTROL Special Price]

若要在指定的時段或排程行銷活動期間提供折扣價格，請輸入特殊價格。 有特殊價格可用時，系統會略過零售價格，並在下方以粗體大寫文字顯示特殊價格。

#### [!UICONTROL Special Price From]日期

{{ce-feature}}

| 欄位 | 說明 |
| ---- | ----------- |
| [!UICONTROL From] | 設定可使用特殊價格的第一個日期。 您可以輸入日期或從行事曆中選取日期。 |
| [!UICONTROL To] | 設定可使用特殊價格的最後日期。 您可以輸入日期或從行事曆中選取日期。 |

{style="table-layout:auto"}

### [!UICONTROL Cost]

輸入料號的實際成本。

### [!UICONTROL Customer Group Price]

![進階價格](./assets/product-pricing-advanced-group-price.png){width="600" zoomable="yes"}

設定特定客戶群組的促銷與階層價格。

| 專案 | 說明 |
| ---- | ----------- |
| [!UICONTROL Website] | 識別套用群組價格規則的網站。 只有在安裝有多個網站時，才會顯示此選項。 |
| [!UICONTROL Customer Group] | （必要）識別符合接收折扣價格資格的客戶群組。 當群組或目錄欄位中的值變更時，符合先前設定的對應自訂價格列將會從共用目錄中刪除。 <br/>**[!UICONTROL ALL GROUPS]**— 將規則套用至所有客戶群組。<br/>**[!UICONTROL NOT LOGGED IN]** — 套用未登入其帳戶的規則來賓和客戶。 |
| [!UICONTROL Quantity] | 指定接收層級價格所需的數量。 |
| [!UICONTROL Price] | （必要）指定特定網站中客戶群組成員的固定或折扣產品價格。 選項： <br/>**[!UICONTROL Fixed]**- （預設）折扣價格會以固定的十進位值輸入。 例如，輸入`9.99`作為折扣價。<br/>**[!UICONTROL Discount]** — 折扣價格是以基礎產品價格的百分比(%)輸入。 例如，輸入`10`以取得10%的折扣。 |
| ![垃圾桶圖示](../assets/icon-delete-trashcan-solid.png) | 刪除目前的規則。 |
| **[!UICONTROL Add]** | 為新規則插入另一列。 |

{style="table-layout:auto"}

### [!UICONTROL Catalog and Tier Price]

設定特定共用型錄與客戶群組的促銷與階層價格。

{{b2b-feature}}

![具有共用目錄之B2B存放區的進階定價](./assets/product-pricing-advanced.png){width="600" zoomable="yes"}

| 專案 | 說明 |
|----|-----------|
| [!UICONTROL Website] | 識別套用群組價格規則的網站。 只有在安裝有多個網站時，才會顯示此選項。 <br>**_重要：_**&#x200B;請在[目錄價格範圍](catalog-price-scope.md)組態中選取_網站&#x200B;_，否則會顯示&#x200B;**所有&#x200B;**&#x200B;網站的設定進階價格。 |
| [!UICONTROL Group or Catalog] | （必要）識別符合接收折扣價格資格的客戶群組或共用型錄。 當群組或目錄欄位中的值變更時，符合先前設定的對應自訂價格列將會從共用目錄中刪除。 <br/>**[!UICONTROL ALL GROUPS]**— 將規則套用至所有客戶群組。 此值不會套用至共用目錄，且進階定價資料中的變更不會與共用目錄同步。<br/>**[!UICONTROL NOT LOGGED IN]** — 套用未登入其帳戶的規則來賓和客戶。<br/>**[!UICONTROL Shared Catalogs]**— 將規則套用至特定的共用目錄。 |
| 數量 | 指定接收層級價格所需的數量。 |
| [!UICONTROL Price] | （必要）指定特定網站中客戶群組成員的固定或折扣產品價格。 選項： <br/>**[!UICONTROL Fixed]**- （預設）折扣價格會以固定的十進位值輸入。 例如，輸入`9.99`作為折扣價。<br/>**[!UICONTROL Discount]** — 折扣價格是以基礎產品價格的百分比(%)輸入。 例如，輸入`10`以取得10%的折扣。 |
| ![垃圾桶圖示](../assets/icon-delete-trashcan-solid.png) | 刪除目前的規則。 |
| **[!UICONTROL Add]** | 為新規則插入另一列。 |

{style="table-layout:auto"}

### [!UICONTROL Minimum Advertised Price]

產品的最低廣告價格(MAP)。

### [!UICONTROL Display Actual Price]

決定客戶看到產品實際價格的位置。

| 專案 | 說明 |
|----|-----------|
| [!UICONTROL Use Config] | 使用目前的組態設定進行價格顯示。 |
| [!UICONTROL On Gesture] | 在快顯視窗中顯示實際產品價格，以回應&#x200B;_價格點按_&#x200B;或&#x200B;_這是什麼？_&#x200B;連結。 |
| [!UICONTROL In Cart] | 顯示購物車中的實際產品價格。 |
| [!UICONTROL Before Order Confirmation] | 在訂單提交前，於結帳程式結束時顯示實際產品價格。 |

{style="table-layout:auto"}
