---
title: 排程的產品更新
description: 瞭解如何排程產品清單變更，以支援行銷活動和促銷方案。
exl-id: ce1aebe6-9032-438d-b950-4b13116b8ed3
feature: Catalog Management, Products
source-git-commit: 3d04e7213d90bb4c323acce69ac31c1dbcb7ca49
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 0%

---

# 排程產品更新

{{ee-feature}}

產品更新可依排程套用，並隨其他內容變更分組。 您可以使用[內容測試](../content-design/content-staging.md)，根據排程的產品變更來建立行銷活動，或將變更套用至現有的行銷活動。

>[!NOTE]
>
>![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce中的[!UICONTROL Set Product as New From]及[!UICONTROL To]欄位和[!UICONTROL Schedule Design Update]索引標籤已移除，無法直接在產品上修改。 您必須為這些啟用建立排定的更新。

>[!NOTE]
>
>所有排定的更新都會連續套用，這表示任何實體一次只能有一個排定的更新。 任何排定的更新都會套用至其時間範圍內的所有存放區檢視。 因此，一個實體無法同時擁有不同存放區檢視的不同排程更新。 所有存放區檢視中的所有實體屬性值（不受目前排程更新影響）都是從預設值取得，而不是從先前的排程更新取得。

>[!NOTE]
>
>排程更新的預備預覽一律從&#x200B;**預設**&#x200B;存放區檢視開始，這模擬客戶瀏覽預備更新行銷活動的體驗。

## 建立排定的更新

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Products]**。

1. 選取現有產品並按一下&#x200B;**[!UICONTROL Edit]**。

1. 按一下&#x200B;**[!UICONTROL Schedule New Update]**。

1. 選取&#x200B;**[!UICONTROL Save as a New Update]**。

1. 針對&#x200B;**[!UICONTROL Update Name]**，輸入新內容預備行銷活動的名稱。

1. 請輸入簡短的更新&#x200B;**[!UICONTROL Description]**&#x200B;及其使用方式。

1. 使用行事曆（![行事曆圖示](../assets/icon-calendar.png)）工具為行銷活動選擇&#x200B;**[!UICONTROL Start Date]**&#x200B;和&#x200B;**[!UICONTROL End Date]**。

   >[!NOTE]
   >
   >行銷活動&#x200B;**[!UICONTROL Start Date]**&#x200B;和&#x200B;**[!UICONTROL End Date]**&#x200B;必須使用從每個網站的當地時區轉換而來的&#x200B;**_預設_**&#x200B;管理時區來定義。 例如，若您有多個網站位在不同時區，且您想根據美國時區啟動促銷活動，則必須針對每個當地時區分別排程更新。 設定&#x200B;**[!UICONTROL Start Date]**&#x200B;和&#x200B;**[!UICONTROL End Date]** （針對每一個），並將它從本機網站時區轉換為預設管理時區。

   ![排程為新更新](./assets/product-schedule-as-new.png){width="600" zoomable="yes"}

1. 向下捲動至&#x200B;_[!UICONTROL Price]_並按一下&#x200B;**[!UICONTROL Advanced Pricing]**。

1. 在排定的行銷活動期間輸入產品的&#x200B;**[!UICONTROL Special Price]**，然後按一下&#x200B;**[!UICONTROL Done]**。

1. 完成時，按一下&#x200B;**[!UICONTROL Save]**。

## 指派給現有更新

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Products]**。

1. 選取現有產品並按一下&#x200B;**[!UICONTROL Edit]**。

1. 按一下&#x200B;**[!UICONTROL Schedule New Update]**。

1. 選取&#x200B;**[!UICONTROL Assign to Existing Campaign]**。

1. 在清單中，選取要修改的行銷活動。

   ![指派至現有的行銷活動](./assets/scheduled-changes-assign-to-existing-campaign.png){width="600" zoomable="yes"}

1. 展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Content]**。

1. 完成時，按一下&#x200B;**[!UICONTROL Save]**。

## 檢視排定的變更

排定的變更會顯示在產品頁面的頂端，其中包含行銷活動的開始和結束日期。

![排程變更](./assets/view-product-scheduled-changes.png){width="600" zoomable="yes"}

## 編輯排定的變更

1. 在頁面頂端的&#x200B;_[!UICONTROL Scheduled Changes]_方塊中，按一下&#x200B;**[!UICONTROL View/Edit]**。

1. 進行排程更新所需的任何變更。

1. 按一下&#x200B;**[!UICONTROL Save]**。

## 移除排定的變更

1. 在頁面頂端的&#x200B;_[!UICONTROL Scheduled Changes]_方塊中，按一下&#x200B;**[!UICONTROL View/Edit]**。

1. 按一下頂端列上的&#x200B;**[!UICONTROL Remove from Update]**。

   ![移除排定的變更](./assets/remove-product-scheduled-changes.png){width="600" zoomable="yes"}

1. 在對話方塊中，選取&#x200B;**[!UICONTROL Delete the Update]**&#x200B;並按一下&#x200B;**[!UICONTROL Done]**。

   >[!NOTE]
   >
   >產品會從更新中移除，且所有已排程的變更都會遺失。

## 排程設計更新

{{ce-feature}}

_[!UICONTROL Schedule Design Update]_區段可讓您暫時變更產品頁面的外觀。 您可以為季節、促銷活動排程設計變更，或只是為了更新內容。 設計變更可以預先排程，以便按照您定義的排程生效，或_&#x200B;滴水&#x200B;_。

![排程的設計更新](./assets/product-design-update-scheduled-ce.png){width="600" zoomable="yes"}


| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Schedule Update From/To] | 決定套用自訂配置至產品的日期範圍。 |
| [!UICONTROL New Theme] | 將自訂主題套用至產品。 |
| [!UICONTROL New Layout] | 將不同的配置套用至產品頁面。 選項： <br/>**[!UICONTROL No layout updates]**— 依預設，產品頁面無法使用配置更新。<br/>**[!UICONTROL Empty]** — 可讓您定義自己的版面配置，例如4欄式頁面。 （需要瞭解XML。） <br/>**[!UICONTROL 1 column]**— 將一欄式配置套用至產品頁面。<br/>**[!UICONTROL 2 columns with left bar]** — 將具左側欄的雙欄版面配置套用至產品頁面。 <br/>**[!UICONTROL 2 columns with right bar]**— 將具右側欄的雙欄版面配置套用至產品頁面。<br/>**[!UICONTROL 3 columns]** — 將三欄式配置套用至產品頁面。 |

{style="table-layout:auto"}
