---
title: 類別許可權
description: 瞭解如何使用類別來控制產品價格的顯示，決定哪些客戶群組可以將產品新增到購物車並指定登陸頁面。
exl-id: d80a0545-918e-4c08-9f37-4aa3cd7771f4
feature: Catalog Management, Categories, Customers, Configuration
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '779'
ht-degree: 0%

---

# 類別許可權

{{ee-feature}}

類別存取權可限製為特定客戶群組，或完全受限。 您可以控制產品價格的顯示，以及決定哪些客戶群組可以將產品新增到購物車，並指定登入頁面。

>[!NOTE]
>
>類別許可權具有全域範圍，啟用時，會根據其個別許可權限制每個類別的存取權。 依預設，不會啟用類別許可權。

例如，如果您只銷售給批發客戶，則可以允許任何人瀏覽目錄，但只針對&#x200B;_批發_&#x200B;客戶群組中的購物者顯示價格並允許購買。 在下列範例中，只有登入的使用者才能存取「集合」類別。 若是來賓，「系列」選項不會出現在主功能表中。

![登入的使用者看到「集合」類別](./assets/storefront-category-permissions-logged-in.png){width="600" zoomable="yes"}

啟用後，「類別」頁面上會出現新的&#x200B;_[!UICONTROL Category Permissions]_&#x200B;區段，可讓您對每個類別套用所需的存取權。 您可以為不同的網站和客戶群組，將多個許可權規則新增至每個類別。

## 步驟1：設定類別許可權

>[!IMPORTANT]
>
>啟用&#x200B;**_[!UICONTROL Shared Catalog]_**&#x200B;功能時，目錄中的&#x200B;**_所有_**&#x200B;類別會忽略所有現有的[群組許可權設定](../configuration-reference/catalog/catalog.md#category-permissions)。 [!UICONTROL Shared Catalog]在啟用時可完全控制目錄中的所有類別許可權。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Catalog]**&#x200B;並在下方選擇&#x200B;**[!UICONTROL Catalog]**。

1. 展開&#x200B;**[!UICONTROL Category Permissions]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![類別許可權](../configuration-reference/catalog/assets/catalog-category-permissions.png){width="600" zoomable="yes"}

   如需這些選項的詳細清單，請參閱&#x200B;_組態參考_&#x200B;中的[類別許可權](../configuration-reference/catalog/catalog.md#category-permissions)。

1. 將&#x200B;**[!UICONTROL Enable]**&#x200B;設為`Yes`。

1. 根據您要允許或限制商店的內容完成其他選項（請參閱下列章節）。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

1. 當提示更新快取時，請按一下系統訊息中的&#x200B;**[!UICONTROL Cache Management]**&#x200B;連結，然後依照指示重新整理快取。

### [!UICONTROL Allow Browsing Category]

此選項適用於[網站](../getting-started/websites-stores-views.md)中的所有類別。

若要允許&#x200B;**_特定客戶群組_**&#x200B;的成員瀏覽類別產品，請執行下列動作：

1. 將&#x200B;**[!UICONTROL Allow Browsing Category]**&#x200B;設為`Specified Customer Groups`。

1. 在&#x200B;**[!UICONTROL Customer Groups]**&#x200B;方塊中，選取每個允許瀏覽類別中產品的群組。

   若要選取多個群組，請按住Ctrl鍵(PC)或Command鍵(Mac)並按一下每個群組。

   ![允許批發客戶群組瀏覽](./assets/category-permissions-allow-browsing-customer-groups.png){width="600" zoomable="yes"}

若要&#x200B;**_限制存取權並重新導向至登陸頁面_**，請執行下列動作：

1. 將&#x200B;**[!UICONTROL Allow Browsing Category]**&#x200B;設為`No, Redirect to Landing Page`。

1. 選擇重新導向訪客的&#x200B;**[!UICONTROL Landing Page]**。

   ![重新導向至首頁](./assets/category-permissions-browse-category-landing-page.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >雖然&#x200B;_[!UICONTROL Allow Browsing Category]_&#x200B;設定適用於網站中的所有類別，但您可以為每個商店檢視設定不同的登陸頁面。

### [!UICONTROL Display Product Prices]

此選項適用於[網站](../getting-started/websites-stores-views.md)中的所有類別。

若要僅允許&#x200B;**_特定客戶群組_**&#x200B;的成員檢視類別中的產品價格，請執行下列動作：

1. 將&#x200B;**[!UICONTROL Display Product Prices]**&#x200B;設為`Yes, for Specified Customer Groups`。

1. 在&#x200B;**[!UICONTROL Customer Groups]**&#x200B;方塊中，選取每個允許檢視類別中產品價格的群組。

   若要選取多個群組，請按住Ctrl鍵(PC)或Command鍵(Mac)，同時按一下每個群組。

   ![只有批發客戶群組能看到價格](./assets/category-permissions-price-customer-groups.png){width="600" zoomable="yes"}

### [!UICONTROL Allow Adding to Cart]

此選項適用於[網站](../getting-started/websites-stores-views.md)中的所有類別。

若要僅允許&#x200B;**_特定客戶群組_**&#x200B;的成員將類別產品放入購物車，請執行下列動作：

1. 將&#x200B;**[!UICONTROL Allow Adding to Cart]**&#x200B;設為`Yes, for Specified Customer Groups`。

1. 在&#x200B;**[!UICONTROL Customer Groups]**&#x200B;方塊中，選取每個允許從類別新增產品至購物車的群組。

   若要選取多個群組，請按住Ctrl鍵(PC)或Command鍵(Mac)並按一下每個群組。

   ![只有批發客戶群組才能將產品放入購物車](./assets/category-permissions-cart-customer-groups.png){width="600" zoomable="yes"}

### [!UICONTROL Disallow Catalog Search]

設定此選項可防止特定客戶群組的成員使用目錄搜尋。 它適用於[網站](../getting-started/websites-stores-views.md)中的所有類別。

- 若要允許&#x200B;**_僅登入客戶_**&#x200B;使用目錄搜尋，請選取`NOT LOGGED IN`。

- 若要允許&#x200B;**_僅特定客戶群組_**&#x200B;使用目錄搜尋，請選取要使用類別搜尋排除的每個群組。

  若要選取多個群組，請按住Ctrl鍵(PC)或Command鍵(Mac)並按一下每個群組。

  ![不允許一般客戶群組的目錄搜尋](./assets/category-permissions-disallow-category-search.png){width="600" zoomable="yes"}

## 步驟2：套用類別許可權

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Categories]**。

1. 在類別樹狀結構中，選取目標類別。

1. 展開頁面上的![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Category Permissions]**，然後執行下列動作：

   - 若要建立許可權規則，請按一下&#x200B;**[!UICONTROL New Permission]**。

     ![類別許可權區段](./assets/category-permissions-section-admin.png){width="600" zoomable="yes"}

   - 選擇適用的&#x200B;**[!UICONTROL Website]**&#x200B;和&#x200B;**[!UICONTROL Customer Group]**。

   - 視需要設定個別許可權。

   >[!NOTE]
   >
   >為任何父類別設定`Browsing Category` = `Deny`許可權時，子類別頁面的[階層連結路徑](navigation-breadcrumb-trail.md)上不會顯示該許可權。

1. 完成時，按一下&#x200B;**[!UICONTROL Save]**。

>[!NOTE]
>
>如果為`Root Category`設定了任何&#x200B;**_允許_**&#x200B;許可權，則這些許可權會自動套用至`Catalog`中的所有子類別和所有產品。 如果有任何產品被指派給多個類別，而且它至少有一個類別有任何&#x200B;**_允許_**&#x200B;許可權，它就會自動對所有指派的類別有相同的&#x200B;**_允許_**&#x200B;許可權。
