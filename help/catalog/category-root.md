---
title: 根類別和階層
description: 瞭解類別階層和根類別，後者可作為類別樹狀結構中主要功能表的容器。
exl-id: b419cb45-4fe5-42c4-be20-667c7e1e4354
feature: Catalog Management, Categories, Site Navigation
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 0%

---

# 根類別和階層

主要功能表中的產品是由指派給[存放區](../stores-purchase/stores.md#add-stores)的根類別所決定。 根類別基本上是類別樹狀結構中主要功能表的容器。 您可以使用全新的產品集建立根類別，或從現有的根類別複製產品。 根類別可指派給目前商店或相同網站中的任何其他商店。

![目錄階層圖表](./assets/catalog-hierarchy-scope.svg){width="550"}

在Admin中，類別結構就像上下倒置的樹狀結構，而根位於頂端。 根目錄有名稱，但沒有URL索引鍵，而且未出現在存放區的[頂端導覽](navigation-top.md)中。 功能表中的所有其他類別都會巢狀置於根之下。 由於根類別是目錄的最高層級，因此您的存放區一次只能有一個作用中的根類別。 不過，您可以為替代型錄結構和不同存放區建立其他根類別。

下列範例顯示如何建立根類別並將其指派給其他存放區。

## 步驟1：建立根類別

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Categories]**。

1. 按一下左側的&#x200B;**[!UICONTROL Add Root Category]**。

   ![新根類別](./assets/category-root-ee.png){width="600" zoomable="yes"}

1. 輸入&#x200B;**[!UICONTROL Category Name]**。

   您選擇的名稱一開始會被指派給所有商店檢視。

1. 如果要將產品從目前目錄新增到目錄，請執行下列動作：

   - 展開![展開選擇器](../assets/icon-display-expand.png) 「類別&#x200B;_」中的_&#x200B;產品。

   - 使用[搜尋篩選器](../getting-started/admin-grid-controls.md)來尋找您想要的產品，並選取每個要複製到新目錄之產品的核取方塊。

1. 完成時，按一下&#x200B;**[!UICONTROL Save]**。

## 步驟2：建置主功能表

1. 在左側，選取您在上一步中建立的新根類別。

1. 若要建立主功能表的[類別結構](category-create.md)，請按一下&#x200B;**[!UICONTROL Add Subcategory]**&#x200B;並依照指示進行。

## 步驟3：將根類別指派給存放區

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**。

1. 在網格的&#x200B;_存放區_&#x200B;欄中，按一下您要指派新目錄的存放區。

1. 將&#x200B;**[!UICONTROL Root Category]**&#x200B;設定為您建立的新根類別。

1. 確定已指派存放區&#x200B;**[!UICONTROL Default Store View]**。

   存放區必須至少有一個[存放區檢視](../stores-purchase/store-views.md)。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Store]**。

1. 若要確認存放區是否具有新目錄，請執行下列動作：

   - 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Products]**。

     複製到新目錄的任何產品都會顯示在格線中。

   - 若要確認新目錄和主功能表是否正常運作，請造訪店面。
