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

產品更新可依排程套用，並隨其他內容變更分組。 您可以使用 [內容分段](../content-design/content-staging.md) ，以根據排程的產品變更建立行銷活動，或將變更套用至現有的行銷活動。

>[!NOTE]
>
>此 [!UICONTROL Set Product as New From] 和 [!UICONTROL To] 欄位和 [!UICONTROL Schedule Design Update] 標籤已在中移除 ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce ，且無法直接在產品上修改。 您必須為這些啟用建立排定的更新。

>[!NOTE]
>
>所有排定的更新都會連續套用，這表示任何實體一次只能有一個排定的更新。 任何排定的更新都會套用至其時間範圍內的所有存放區檢視。 因此，一個實體無法同時擁有不同存放區檢視的不同排程更新。 所有存放區檢視中的所有實體屬性值（不受目前排程更新影響）都是從預設值取得，而不是從先前的排程更新取得。

>[!NOTE]
>
>排程更新的測試預覽一律從 **預設** 商店檢視，可模擬客戶在中繼更新促銷活動中導覽的體驗。

## 建立排定的更新

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 選取現有產品並按一下 **[!UICONTROL Edit]**.

1. 按一下 **[!UICONTROL Schedule New Update]**.

1. 選取 **[!UICONTROL Save as a New Update]**.

1. 的 **[!UICONTROL Update Name]**，輸入新內容預備行銷活動的名稱。

1. 輸入簡報 **[!UICONTROL Description]** 以及如何使用。

1. 使用行事曆(![行事曆圖示](../assets/icon-calendar.png))工具來選擇 **[!UICONTROL Start Date]** 和 **[!UICONTROL End Date]** 促銷活動。

   >[!NOTE]
   >
   >Campaign **[!UICONTROL Start Date]** 和 **[!UICONTROL End Date]** 必須透過以下方式定義： **_預設_** 管理時區，從每個網站的當地時區轉換。 例如，若您有多個網站位在不同時區，且您想根據美國時區啟動促銷活動，則必須針對每個當地時區分別排程更新。 設定 **[!UICONTROL Start Date]** 和 **[!UICONTROL End Date]** 都會從當地網站時區轉換為預設管理時區。

   ![排程為新的更新](./assets/product-schedule-as-new.png){width="600" zoomable="yes"}

1. 向下捲動至 _[!UICONTROL Price]_並按一下&#x200B;**[!UICONTROL Advanced Pricing]**.

1. 輸入 **[!UICONTROL Special Price]** 在排程行銷活動期間提供產品資訊，然後按一下 **[!UICONTROL Done]**.

1. 完成後，按一下 **[!UICONTROL Save]**.

## 指派給現有更新

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 選取現有產品並按一下 **[!UICONTROL Edit]**.

1. 按一下 **[!UICONTROL Schedule New Update]**.

1. 選取 **[!UICONTROL Assign to Existing Campaign]**.

1. 在清單中，選取要修改的行銷活動。

   ![指派給現有行銷活動](./assets/scheduled-changes-assign-to-existing-campaign.png){width="600" zoomable="yes"}

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) **[!UICONTROL Content]**.

1. 完成後，按一下 **[!UICONTROL Save]**.

## 檢視排定的變更

排定的變更會顯示在產品頁面的頂端，其中包含行銷活動的開始和結束日期。

![排定的變更](./assets/view-product-scheduled-changes.png){width="600" zoomable="yes"}

## 編輯排定的變更

1. 在 _[!UICONTROL Scheduled Changes]_方塊中，按一下&#x200B;**[!UICONTROL View/Edit]**.

1. 進行排程更新所需的任何變更。

1. 按一下 **[!UICONTROL Save]**.

## 移除排定的變更

1. 在 _[!UICONTROL Scheduled Changes]_方塊中，按一下&#x200B;**[!UICONTROL View/Edit]**.

1. 在頂端列上，按一下 **[!UICONTROL Remove from Update]**.

   ![移除排定的變更](./assets/remove-product-scheduled-changes.png){width="600" zoomable="yes"}

1. 在對話方塊中選取 **[!UICONTROL Delete the Update]** 並按一下 **[!UICONTROL Done]**.

   >[!NOTE]
   >
   >產品會從更新中移除，且所有已排程的變更都會遺失。

## 排程設計更新

{{ce-feature}}

此 _[!UICONTROL Schedule Design Update]_區段可讓您暫時變更產品頁面的外觀。 您可以為季節、促銷活動排程設計變更，或只是為了更新內容。 設計變更可以提前排程，以便生效，或者_&#x200B;滴水&#x200B;_，根據您定義的排程進行。

![排程的設計更新](./assets/product-design-update-scheduled-ce.png){width="600" zoomable="yes"}


| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Schedule Update From/To] | 決定套用自訂配置至產品的日期範圍。 |
| [!UICONTROL New Theme] | 將自訂主題套用至產品。 |
| [!UICONTROL New Layout] | 將不同的配置套用至產品頁面。 選項： <br/>**[!UICONTROL No layout updates]**— 依預設，配置更新不適用於產品頁面。<br/>**[!UICONTROL Empty]**  — 可讓您定義自己的版面，例如4欄式頁面。 （需要瞭解XML。） <br/>**[!UICONTROL 1 column]**— 將一欄式版面配置套用至產品頁面。<br/>**[!UICONTROL 2 columns with left bar]**  — 將具左側欄的雙欄版面配置套用至產品頁面。 <br/>**[!UICONTROL 2 columns with right bar]**— 將具右側欄的雙欄版面配置套用至產品頁面。<br/>**[!UICONTROL 3 columns]**  — 將三欄版面配置套用至產品頁面。 |

{style="table-layout:auto"}
