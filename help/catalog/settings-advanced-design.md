---
title: 產品設定 —  [!UICONTROL Design]
description: 對於產品， [!UICONTROL Design] 設定可讓您將不同的主題套用至產品頁面並變更版面。
exl-id: 8606ddc7-ca81-4503-94e5-a8276506c0a1
feature: Catalog Management, Products, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# 產品設定 —  [!UICONTROL Design]

此 _[!UICONTROL Design]_設定可讓不同的主題套用至產品頁面、變更欄版面配置、決定產品選項出現的位置，以及輸入自訂XML程式碼。

![設計](./assets/product-design-ee.png){width="600" zoomable="yes"}

>[!NOTE]
>
>將相同產品指派給數個類別，且每個類別的設計設定不同時，建議設定 **[!UICONTROL Use Categories Path for Product URLs]** = `Yes` 在 [搜尋引擎最佳化組態選項](../configuration-reference/catalog/catalog.md#search-engine-optimization). 若要存取此設定，請前往  **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**，展開&#x200B;**[!UICONTROL Catalog]**並選擇&#x200B;**[!UICONTROL Catalog]**，然後展開&#x200B;**[!UICONTROL Search Engine Optimization]**區段建立關聯。

| 欄位 | [範圍](../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|---|---|----|
| [!UICONTROL Theme] | 存放區檢視 | ![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)可讓您將不同的主題套用至產品。 選項： （所有可用主題） |
| [!UICONTROL Layout] | 存放區檢視 | 可讓您套用不同的 [版面](../content-design/page-layout.md) 至產品頁面。 選項： <br/>**[!UICONTROL No layout updates]**— 依預設，配置更新不適用於產品頁面。<br/>**[!UICONTROL Empty]**  — 可讓您定義自己的版面，例如4欄式頁面。 （需要瞭解XML。） <br/>**[!UICONTROL 1 column]**— 將一欄式版面配置套用至產品頁面。<br/>**[!UICONTROL 2 columns with left bar]**  — 將具左側欄的雙欄版面配置套用至產品頁面。 <br/>**[!UICONTROL 2 columns with right bar]**— 將具右側欄的雙欄版面配置套用至產品頁面。<br/>**[!UICONTROL 3 columns]**  — 將三欄版面配置套用至產品頁面。 <br/>**[!UICONTROL Page -- Full Width]**- (需要 [[!DNL Page Builder]](../page-builder/introduction.md))將CMS頁面的完整版面配置套用至產品頁面。<br/>**[!UICONTROL Category -- Full Width]** - (需要 [!DNL Page Builder])將類別頁面的全寬度版面配置套用至產品頁面。 <br/>**[!UICONTROL Product -- Full Width]**- (需要 [!UICONTROL Page Builder])將產品頁面的全寬度版面配置套用至產品頁面。 |
| [!UICONTROL Display Product Options In] | 存放區檢視 | 決定產品選項在產品頁面上出現的位置。 選項： `Product Info Column` / `Block after Info Column` |
| [!UICONTROL Custom Layout Update] | 存放區檢視 | 用於存取更新產品頁面上自訂配置的選項。 |

{style="table-layout:auto"}
