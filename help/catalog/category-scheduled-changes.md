---
title: 類別的已排程變更
description: 瞭解如何排程類別變更以支援行銷活動和商店促銷活動。
exl-id: 9e25082f-4e76-4148-b76e-dca0b14971eb
feature: Catalog Management, Categories
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---

# 類別的已排程變更

{{ee-feature}}

類別更新可以依排程套用，並和其他內容變更一起分組。 您可以根據類別已排程的變更來建立行銷活動，或將變更套用至現有的行銷活動。 若要深入瞭解，請參閱 [內容分段](../content-design/content-staging.md).

>[!NOTE]
>
>所有排定的更新都會連續套用，這表示任何實體一次只能有一個排定的更新。 任何排定的更新都會套用至其時間範圍內的所有存放區檢視。 因此，一個實體無法同時擁有不同存放區檢視的多個排程更新。 所有存放區檢視中的所有實體屬性值（不受目前排程更新影響）都是從預設值取得，而不是從先前的排程更新取得。

## 為類別排程更新

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. 在左側的類別樹狀結構中，選擇要修改的類別。

1. 在 _排定的變更_ 方塊中，按一下 **[!UICONTROL Schedule New Update]**.

   ![排定的變更](./assets/category-scheduled-changes.png){width="600" zoomable="yes"}

1. 使用 **[!UICONTROL Save as a New Update]** 選取的選項，設定更新的基本引數：

   - 的 **[!UICONTROL Update Name]**，輸入新內容預備行銷活動的名稱。

   - 輸入簡報 **[!UICONTROL Description]** 以及如何使用。

   - 使用行事曆( ![行事曆圖示](../assets/icon-calendar.png) )工具來選擇 **[!UICONTROL Start Date]** 和 **[!UICONTROL End Date]** 促銷活動。

   >[!IMPORTANT]
   >
   >Campaign **[!UICONTROL Start Date]** 和 **[!UICONTROL End Date]** 必須透過以下方式定義： **_預設_** 管理時區，由每個網站的當地時區加以轉換。 例如，若您有多個網站位在不同時區，且您想根據美國時區啟動促銷活動，則必須針對每個當地時區分別排程更新。 您設定 **[!UICONTROL Start Date]** 和 **[!UICONTROL End Date]** 「 」會從本機網站時區轉換為預設管理員時區。

   ![排定的變更](./assets/category-scheduled-changes-new-update.png){width="600" zoomable="yes"}

1. 進行排程更新所需的任何變更。

1. 若要預覽變更，請按一下 **[!UICONTROL Preview]** 在右上角的按鈕列中。

1. 完成後，按一下 **[!UICONTROL Save]**.

## 指派給現有更新

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. 在左側的類別樹狀結構中，選擇要修改的類別。

1. 在 _排定的變更_ 方塊中，按一下 **[!UICONTROL Schedule New Update]**.

1. 選取 **[!UICONTROL Assign to Existing Campaign]**.

1. 在清單中，找到所需的行銷活動，然後按一下 **[!UICONTROL Select]**.

1. 對排程更新進行必要的變更。

1. 完成後，按一下 **[!UICONTROL Save]**.
