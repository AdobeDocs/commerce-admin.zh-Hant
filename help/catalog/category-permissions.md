---
title: 類別許可權
description: 瞭解如何使用類別來控制產品價格的顯示，決定哪些客戶群組可以將產品新增到購物車並指定登陸頁面。
exl-id: d80a0545-918e-4c08-9f37-4aa3cd7771f4
feature: Catalog Management, Categories, Customers, Configuration
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '777'
ht-degree: 0%

---

# 類別許可權

{{ee-feature}}

類別存取權可限製為特定客戶群組，或完全受限。 您可以控制產品價格的顯示，以及決定哪些客戶群組可以將產品新增到購物車，並指定登入頁面。

>[!NOTE]
>
>類別許可權具有全域範圍，啟用時，會根據其個別許可權限制每個類別的存取權。 依預設，不會啟用類別許可權。

例如，如果您只向批發客戶銷售，您可以允許任何人瀏覽目錄，但只顯示價格並只允許以下位置的購物者購買： _批發_ 客戶群組。 在下列範例中，只有登入的使用者才能存取「集合」類別。 若是來賓，「系列」選項不會出現在主功能表中。

![登入的使用者請參閱「集合」類別](./assets/storefront-category-permissions-logged-in.png){width="600" zoomable="yes"}

啟用時，新增 _[!UICONTROL Category Permissions]_區段會顯示在「類別」頁面上，可讓您為每個類別套用所需的存取權。 您可以為不同的網站和客戶群組，將多個許可權規則新增至每個類別。

## 步驟1：設定類別許可權

>[!IMPORTANT]
>
>所有現有 [群組許可權設定](../configuration-reference/catalog/catalog.md#category-permissions) 被忽略 **_全部_** 目錄中的類別，當 **_[!UICONTROL Shared Catalog]_** 功能已啟用。 [!UICONTROL Shared Catalog] 完全控制啟用目錄時目錄中的所有類別許可權。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Catalog]** 並選擇 **[!UICONTROL Catalog]** 底下。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Category Permissions]** 區段。

   ![類別許可權](../configuration-reference/catalog/assets/catalog-category-permissions.png){width="600" zoomable="yes"}

   如需這些選項的詳細清單，請參閱 [類別許可權](../configuration-reference/catalog/catalog.md#category-permissions) 在 _設定參考_.

1. 設定 **[!UICONTROL Enable]** 至 `Yes`.

1. 根據您要允許或限制商店的內容完成其他選項（請參閱下列章節）。

1. 完成後，按一下 **[!UICONTROL Save Config]**.

1. 提示更新快取時，按一下 **[!UICONTROL Cache Management]** 連結，然後依照指示重新整理快取。

### [!UICONTROL Allow Browsing Category]

此選項適用於 [網站](../getting-started/websites-stores-views.md).

允許的成員 **_特定客戶群組_** 若要瀏覽類別產品，請執行下列動作：

1. 設定 **[!UICONTROL Allow Browsing Category]** 至 `Specified Customer Groups`.

1. 在 **[!UICONTROL Customer Groups]** 方塊中，選取每個允許瀏覽類別中產品的群組。

   若要選取多個群組，請按住Ctrl鍵(PC)或Command鍵(Mac)並按一下每個群組。

   ![允許依批發客戶群組瀏覽](./assets/category-permissions-allow-browsing-customer-groups.png){width="600" zoomable="yes"}

至 **_限制存取並重新導向至登陸頁面_**，請執行下列動作：

1. 設定 **[!UICONTROL Allow Browsing Category]** 至 `No, Redirect to Landing Page`.

1. 選擇 **[!UICONTROL Landing Page]** 重新導向訪客的位置。

   ![重新導向至首頁](./assets/category-permissions-browse-category-landing-page.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >雖然 _[!UICONTROL Allow Browsing Category]_此設定適用於網站中的所有類別，您可以為每個商店檢視設定不同的登陸頁面。

### [!UICONTROL Display Product Prices]

此選項適用於 [網站](../getting-started/websites-stores-views.md).

僅允許成員 **_特定客戶群組_** 若要檢視類別中的產品價格，請執行下列步驟：

1. 設定 **[!UICONTROL Display Product Prices]** 至 `Yes, for Specified Customer Groups`.

1. 在 **[!UICONTROL Customer Groups]** 方塊中，選取每個允許檢視類別中產品價格的群組。

   若要選取多個群組，請按住Ctrl鍵(PC)或Command鍵(Mac)，同時按一下每個群組。

   ![只有批發客戶群組才能看到價格](./assets/category-permissions-price-customer-groups.png){width="600" zoomable="yes"}

### [!UICONTROL Allow Adding to Cart]

此選項適用於 [網站](../getting-started/websites-stores-views.md).

僅允許成員 **_特定客戶群組_** 若要將類別產品放入購物車，請執行以下操作：

1. 設定 **[!UICONTROL Allow Adding to Cart]** 至 `Yes, for Specified Customer Groups`.

1. 在 **[!UICONTROL Customer Groups]** 方塊中，選取每個允許從類別新增產品至購物車的群組。

   若要選取多個群組，請按住Ctrl鍵(PC)或Command鍵(Mac)並按一下每個群組。

   ![只有批發客戶群組可以將產品放入購物車](./assets/category-permissions-cart-customer-groups.png){width="600" zoomable="yes"}

### [!UICONTROL Disallow Catalog Search]

設定此選項可防止特定客戶群組的成員使用目錄搜尋。 它適用於 [網站](../getting-started/websites-stores-views.md).

- 允許 **_僅登入的客戶_** 若要使用目錄搜尋，請選取 `NOT LOGGED IN`.

- 允許 **_僅限特定客戶群組_** 若要使用目錄搜尋，請選取要使用「類別搜尋」排除的每個群組。

  若要選取多個群組，請按住Ctrl鍵(PC)或Command鍵(Mac)並按一下每個群組。

  ![不允許一般客戶群組的目錄搜尋](./assets/category-permissions-disallow-category-search.png){width="600" zoomable="yes"}

## 步驟2：套用類別許可權

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. 在類別樹狀結構中，選取目標類別。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) **[!UICONTROL Category Permissions]** ，並執行下列動作：

   - 若要建立許可權規則，請按一下 **[!UICONTROL New Permission]**.

     ![類別許可權區段](./assets/category-permissions-section-admin.png){width="600" zoomable="yes"}

   - 選擇適用的 **[!UICONTROL Website]** 和 **[!UICONTROL Customer Group]**.

   - 視需要設定個別許可權。

   >[!NOTE]
   >
   >時間 `Browsing Category` = `Deny` 已針對任何父類別設定許可權，但不會顯示在 [階層連結路徑](navigation-breadcrumb-trail.md) 在子類別頁面上。

1. 完成後，按一下 **[!UICONTROL Save]**.

>[!NOTE]
>
>若有 **_允許_** 已為設定許可權 `Root Category`，這些許可權就會自動套用至「 」內的所有子類別和所有產品 `Catalog`. 如果有任何產品被指派到多個類別，而且它有任何 **_允許_** 至少一個類別的許可權，會自動具有相同的許可權 **_允許_** 所有指定類別的許可權。
