---
title: 建立產品
description: 瞭解您可以為目錄建立的產品型別。
exl-id: ff90bf8a-a64d-403f-bd09-5c8167a36f0b
feature: Catalog Management, Products
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '689'
ht-degree: 0%

---

# 建立產品

選擇產品型別是建立產品必須執行的首要操作之一。 如果您剛開始建立產品目錄，您可以建立一些範例產品來實驗每種產品型別。 除了基本產品型別之外，術語&#x200B;_複雜產品_&#x200B;有時也用來指代具有多個選項的產品，例如可設定且有多種顏色和大小的產品。

>[!NOTE]
>
>如需更深入的瞭解，請參閱目錄[導覽](navigation.md)、如何設定[類別](categories.md)和[屬性](product-attributes.md)，以及可用的目錄[URL選項](catalog-urls.md)。 瞭解這些概念後，將許多產品新增到目錄的最有效率方式是從CSV檔案[匯入](../systems/data-import.md)這些產品。

店面上的![產品頁面](./assets/storefront-product-page.png){width="700" zoomable="yes"}

## 產品型別

**[簡單產品](product-create-simple.md)** — 簡單產品是指具有單一SKU的實體專案。 簡單產品有各種定價和輸入控制項，因此可以銷售產品的各種變體。 簡單產品可與群組、套件組合和可設定產品關聯使用。

**[可設定的產品](product-create-configurable.md)** — 可設定的產品似乎是單一產品，包含每個變數的選項清單。 不過，每個選項代表個別的簡單產品，並具有不同的SKU，因此可以追蹤每個變數的詳細目錄。

**[已分組的產品](product-create-grouped.md)** — 已分組的產品會將多個獨立的產品顯示為群組。 您可以提供單一產品的變體，或將它們分組以進行促銷。 這些產品可以單獨購買或分組購買。

**[虛擬產品](product-create-virtual.md)** — 虛擬產品不是有形產品，通常用於服務、會員資格、保固和訂閱等產品。 虛擬產品可與分組和套裝產品結合使用。

**[套裝產品](product-create-bundle.md)** — 套裝產品可讓客戶從一連串選項「建立自己的產品」。 此套裝可以是禮品籃、電腦或任何其他可自訂的專案。 套件組合中的每個專案都是獨立的獨立產品。

**[可下載的產品](product-create-downloadable.md)** — 可數位下載的產品包含一或多個已下載的檔案。 這些檔案可以位於您的伺服器上，或以URL的形式提供給任何其他伺服器。

**[禮品卡](product-gift-card-create.md)** - (僅限[Adobe Commerce](../landing/home.md#product-editions))禮品卡有三種。 _虛擬_&#x200B;禮品卡是以電子郵件傳送。 _實體_&#x200B;禮品卡已寄給收件者。 _虛擬與實體結合的_&#x200B;禮品卡。 每個檔案都有唯一代碼，在結帳時可兌換。 禮品卡也可包含在分組產品中。

## 產品設定

最常使用的產品設定和屬性會顯示在頁面頂端，後面接著自訂屬性。 任何其他產品設定均位於頁面底部的可展開區段中。

![產品設定](./assets/product-settings.png){width="600" zoomable="yes"}

| 設定 | 說明 |
|--- |--- |
| [[!UICONTROL Sources]](../inventory-management/sources-assign-per-product.md) | （啟用[[!DNL Inventory Management]](../inventory-management/introduction.md)時）列出可分發產品的來源。 |
| [[!UICONTROL Content]](product-content.md) | 用於輸入和編輯顯示在店面產品頁面上的主要產品說明。 |
| [[!UICONTROL Configurations]](product-configurations.md) | 列出產品的任何現有變數，並可用來產生變數，以與可設定的產品型別搭配使用。 |
| [[!UICONTROL Product Reviews]](settings-advanced-product-reviews.md) | 列出客戶針對產品提交的所有評論。 |
| [[!UICONTROL Search Engine Optimization]](product-search-engine-optimization.md) | 指定URL索引鍵和中繼資料欄位，搜尋引擎會使用這些欄位為產品編制索引。 |
| [[!UICONTROL Related Products, Up-Sells, and Cross-Sells]](related-products-up-sells-cross-sells.md) | 用於在店面設定簡單的促銷區塊，呈現客戶可能感興趣的其他產品選擇。 |
| [[!UICONTROL Customizable Options]](settings-advanced-custom-options.md) | 將可自訂的選項新增至產品。 |
| [[!UICONTROL Product in Websites]](settings-basic-websites.md) | 根據商店階層識別可使用該產品的每個網站。 |
| [[!UICONTROL Design]](settings-advanced-design.md) | 用於將不同的主題套用至產品頁面、變更欄版面配置、決定產品選項出現的位置，以及輸入自訂XML程式碼。 |
| [[!UICONTROL Gift options]](product-gift-options.md) | 用於在產品層級結帳時啟用或停用禮品訊息選項。 |
| [[!UICONTROL Product In Shared Catalogs]](../b2b/catalog-shared.md) | ![Adobe Commerce B2B](../assets/b2b.svg) (僅適用於[Adobe Commerce B2B](../b2b/introduction.md))可讓您使用自訂價格維護不同公司的共用目錄。 |
| [[!UICONTROL Downloadable Information]](product-create-downloadable.md#step-5-complete-the-downloadable-information) | 用於定義產品下載的引數。 |

{style="table-layout:auto"}

## 進階訂價與存貨

若要存取進階訂價與存貨設定，請按一下&#x200B;**[!UICONTROL Price]**&#x200B;與&#x200B;**[!UICONTROL Quantity]**&#x200B;下方的連結。 如需詳細資訊，請參閱[管理定價](pricing-advanced.md)和[Inventory management](../inventory-management/introduction.md)。
