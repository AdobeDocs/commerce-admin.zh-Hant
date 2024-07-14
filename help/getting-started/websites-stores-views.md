---
title: 網站、存放區和檢視範圍
description: 瞭解您可用來為客戶提供購物體驗的網站、商店和商店檢視的階層。
exl-id: 80fc1b73-c869-4f1c-b1a1-d61823b91d83
feature: System, Site Management
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---

# 網站、存放區和檢視範圍

每個Adobe Commerce和Magento Open Source安裝都有網站、商店和商店檢視的[階層](../stores-purchase/stores.md)。 術語&#x200B;_範圍_&#x200B;決定資料庫實體（例如產品、屬性或類別）內容元素或組態設定在階層中套用的位置。 網站、商店和商店檢視具有一對多的父/子關係。 單一安裝可擁有多個網站，而每個網站可擁有多個商店和商店檢視。

>[!NOTE]
>
>若要深入瞭解，請參閱[!DNL Commerce]開發人員檔案中的[多個網站或商店](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html)。

## 網站

安裝從單一[網站](../stores-purchase/stores.md#add-websites)開始，預設為&#x200B;_主要網站_。 您也可以為單一安裝設定多個網站，每個網站都有自己的IP位址和網域。

## 商店

單一網站可以有多個[商店](../stores-purchase/stores.md#add-stores)，每個都有自己的主功能表。 商店會共用產品目錄，但可以有不同的產品和設計選擇。 相同網站下的所有商店都會共用管理員和結帳。

## 存放區檢視

根據特定的&#x200B;_[檢視](../stores-purchase/store-views.md)_，呈現每個可供客戶使用的商店。 最初，商店有單一預設檢視。 可新增其他商店檢視來支援不同語言或其他用途。 客戶可以在標頭中使用語言選擇器來變更商店檢視。

使用網站、商店和商店檢視時，請牢記下列事項：

- Commerce執行個體有階層式模型：全域→網站→商店→商店檢視。
- 每個網站至少有一個預設商店和商店檢視。
- 每個商店檢視可以有不同的基本URL。
- 網站的主要功能是設定頂層功能。
- 存放區的主要功能是根類別設定。
- 商店檢視的主要功能是轉譯資訊和貨幣符號設定。

## 範圍設定

如果您的Adobe Commerce或Magento Open Source安裝具有網站、商店或檢視的階層，您可以設定內容或組態設定的&#x200B;_範圍_。 也可以為許多資料庫實體的內容指派特定範圍，以決定如何在存放區階層中使用它。 若要深入瞭解，請參閱[產品範圍](../catalog/introduction.md#product-scope)和[價格範圍](../catalog/catalog-price-scope.md)。

部分組態設定（例如郵遞區號）具有全域範圍，因為系統內會使用相同的值。 [網站](../stores-purchase/stores.md#add-websites)範圍會套用至階層中該層級之下的任何存放區，包括所有存放區及其檢視。 每個存放區檢視的範圍皆可設定[存放區檢視](../stores-purchase/store-views.md)的任何專案，通常用於支援多種語言。 若要覆寫組態設定的預設值，請參閱[設定範圍](../configuration-reference/scope-change.md#set-the-scope)。

除非存放區以[單一存放區模式](#single-store-mode)執行，否則每個組態設定的範圍都會顯示在欄位標籤下方的小型文字中。 如果您的安裝包含多個網站、商店或檢視，請先選擇套用設定的[商店檢視](../stores-purchase/store-views.md)，然後再進行任何變更。

![網站、商店和商店檢視的階層](./assets/scope-multisite.svg){width="550"}

| 範圍 | 說明 |
|--- |--- |
| [!UICONTROL Global] | 整個安裝過程中可用的系統範圍設定和資源。 |
| [!UICONTROL Website] | 限制在目前網站的設定和資源。 每個網站都有預設商店。 |
| [!UICONTROL Store] | 限制在目前商店的設定和資源。 每個商店都有預設根類別（主功能表）和預設商店檢視。 |
| [!UICONTROL Store View] | 設為目前商店檢視的設定和資源。 |

{style="table-layout:auto"}

## 單一存放區模式

如果您的Commerce安裝只有單一商店和商店檢視，您可以透過關閉所有商店檢視選項和範圍指示器來簡化顯示。 如果您[稍後新增更多商店檢視](../stores-purchase/store-views.md)，單一商店模式會被覆寫。

![範圍 — 單一檢視](./assets/scope-single-view.svg){width="550"}

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在&#x200B;**[!UICONTROL General]**&#x200B;底下，向下捲動至頁面底部並展開&#x200B;**[!UICONTROL Single-Store Mode]**&#x200B;區段。

1. 將&#x200B;**[!UICONTROL Enable Single-Store Mode]**&#x200B;設為`Yes`。

   ![一般設定 — 啟用單一存放區模式](./assets/general-single-store-mode.png){width="400"}

1. 按一下&#x200B;**[!UICONTROL Save Config]**。

1. 當提示重新整理快取時，請執行下列動作：

   - 按一下頁面頂端系統訊息中的&#x200B;**[!UICONTROL Cache Management]**&#x200B;連結。

     ![系統訊息 — 快取管理](../catalog/assets/msg-cache-management.png){width="600" zoomable="yes"}

   - 選取&#x200B;**[!UICONTROL Page Cache]**&#x200B;核取方塊。

   - 在&#x200B;**[!UICONTROL Actions]**&#x200B;設定為`Refresh`的情況下，按一下&#x200B;**[!UICONTROL Submit]**
