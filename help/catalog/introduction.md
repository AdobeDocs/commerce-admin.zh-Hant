---
title: 目錄管理簡介
description: 瞭解目錄和產品範圍如何在目錄管理中運作。
exl-id: 3c58fc1c-d7a3-4f51-8a78-6bf2fd0dbeee
source-git-commit: f36925217230e558043078fdc274f5e69c096c1e
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 0%

---

# 目錄管理簡介

Adobe Commerce和Magento Open Source使用術語&#x200B;_目錄_&#x200B;來指稱整個產品資料庫。

建立和管理商店的最重要領域之一是產品建立和類別。 管理員提供數種工具，可用於商店的初始設定、商店的維護及業務最佳化。

>[!TIP]
>
>適用於Adobe Commerce和Magento Open Source的Inventory management提供管理工具，可管理您的產品詳細目錄。 擁有單一商店到多個倉庫、商店、取貨地點、卸貨託運人等等的商家，可以使用這些功能來維護銷售數量，並處理出貨以完成訂單。 如需這些功能以及如何使用這些功能來管理多個位置中的庫存的詳細資訊，請參閱[Inventory management使用手冊](../inventory-management/introduction.md)。

## 目錄範圍

存取目錄資料是由數個因素所決定，包括[領域](../getting-started/websites-stores-views.md#scope-settings)設定、目錄組態以及指派給存放區的[根類別](category-root.md)。 目錄包括已啟用且可供銷售的產品，以及目前不提供以供銷售的產品。

在銷售中，_目錄_&#x200B;一詞通常是指可供銷售之精選產品。 例如，商店可能有「Spring Catalog」和「Fall Catalog」。

如同列印目錄的內容表，您商店的主功能表（或&#x200B;_最上層導覽_）會依類別組織產品，讓客戶更容易找到他們想要的東西。 主要功能表是以&#x200B;_根類別_&#x200B;為基礎，這是指派給商店的功能表容器。 因為特定選單選項是在商店檢視層級定義的，所以每個檢視都可以根據相同的根類別有不同的主選單。 在每個功能表中，您都可以提供適合該商店的精選產品。

![目錄階層圖表](./assets/catalog-hierarchy-scope.svg){width="550"}

## 產品範圍

對於具有多個網站、商店和檢視的安裝，[範圍](../getting-started/websites-stores-views.md#scope-settings)設定會決定產品銷售的位置，以及每個商店檢視可用的產品資訊。 最初，您建立的所有產品都會發佈至預設的網站、商店和商店檢視。

![多網站存放區圖表](./assets/scope-multisite.svg){width="550"}

如果您只有一個具有預設檢視的單一商店，您可以在[單一商店模式](../getting-started/websites-stores-views.md#single-store-mode)下執行商店以隱藏範圍設定。 但是，如果您的存放區有多個檢視，則每個欄位的名稱下方會顯示一個範圍指示器。

- 若要編輯特定檢視的產品資訊，請使用左上角的&#x200B;_商店檢視_&#x200B;控制項來選擇檢視。 可在存放區檢視層級編輯的任何欄位都可使用其他控制項。

- 若要定義多站台安裝中的產品範圍，請參閱產品資訊的[網站中的產品](settings-basic-websites.md)區段。

針對商店檢視編輯產品的程式，就像新增檢視特有的產品資訊層一樣。

您只能編輯或指派您擁有許可權之網站的產品，不能編輯或指派所有指派了產品的網站。

雖然在以下範例中選取了&#x200B;_Spanish_&#x200B;商店檢視，但產品資訊仍會以預設商店檢視的原始語言顯示。 若要翻譯產品資訊，您必須切換至&#x200B;_西班牙文_&#x200B;商店檢視並翻譯文字欄位，例如產品標題、說明和中繼資料。 如需詳細資訊，請參閱[將產品本地化](../stores-purchase/store-localize.md#localize-products)。

## 編輯不同檢視的產品

>[!NOTE]
>
>當產品也發佈在允許的範圍以外時，對於限制在特定範圍的管理員使用者，已停用&#x200B;_所有存放區檢視_&#x200B;範圍。 預設會選取第一個可編輯的範圍，因為受限制的使用者無法執行&#x200B;_全域_&#x200B;動作或影響他們無權存取之範圍的動作。

1. 在左上角，將&#x200B;**[!UICONTROL Store View]**&#x200B;設定為要編輯的特定檢視。

1. 若要確認範圍變更，請按一下&#x200B;**[!UICONTROL OK]**。

1. 使用存放區檢視的新值更新欄位。

   任何可針對存放區檢視編輯的欄位下都會出現核取方塊。 若要覆寫預設值，請取消選取&#x200B;**使用預設值**&#x200B;核取方塊。

   ![翻譯西班牙文商店檢視的產品名稱](./assets/product-translate-field-french.png){width="600" zoomable="yes"}

1. 完成時，按一下&#x200B;**[!UICONTROL Save]**。

1. 在左上角，將&#x200B;**[!UICONTROL Store View]**&#x200B;選擇器設定回預設值。

1. 若要驗證您商店中的變更，請執行下列動作：

   - 在右上角，按一下&#x200B;_管理員_&#x200B;功能表箭頭，然後選擇&#x200B;**[!UICONTROL Customer View]**。

     ![客戶檢視](./assets/product-admin-menu-customer-view.png){width="600" zoomable="yes"}

   - 在商店的右上角，將&#x200B;**[!UICONTROL Language Chooser]**&#x200B;設定為您所編輯產品的商店檢視，並尋找您針對檢視編輯的產品。

     ![語言選擇器](./assets/storefront-language-chooser.png){width="700" zoomable="yes"}
