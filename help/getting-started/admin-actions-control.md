---
title: 動作控制
description: 瞭解如何使用Actions控制項，將操作套用至Admin中的一或多個記錄。
exl-id: 03f313a9-bc17-4151-a2c8-8906342f025d
TQID: https://experienceleague.adobe.com/N8RFNMBc2i4Surct0luNp7z-qF0lbP6r8T-uEMQ7y-w
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 430
ht-degree: 0%

---

# 動作控制

使用網格中的記錄集合時，您可以使用「動作」控制項將作業套用至一或多個記錄。 Actions控制項會列出特定資料型別可用的每項作業。 例如，您可以使用Actions控制項來更新所選產品的屬性、將狀態從`Disabled`變更為`Enabled`，或從資料庫中刪除記錄。

您可以視需要進行多次變更，然後在單一步驟中更新記錄。 這比個別變更每個產品的設定更有效率。 將編輯套用至記錄批次是一項非同步操作，會在背景執行，因此您可以繼續在Admin中工作，而不需要等候操作完成。 當工作完成時，系統會顯示訊息。

可用動作的選擇因清單而異，並且可能會顯示其他選項，具體取決於所選的動作。 例如，變更記錄群組的狀態時，「動作」控制項旁邊會出現&#x200B;_[!UICONTROL Status]_&#x200B;方塊，並附上其他選項。

## 步驟1：選取記錄

清單第一欄中的核取方塊會識別作為動作目標的每個記錄。 [篩選器控制項](admin-grid-controls.md)可用來將清單縮小至您要針對動作鎖定的記錄。

1. 如有需要，請在每欄頂端設定篩選器，以僅顯示您要包含的記錄。

1. 選取作為動作目標的每個記錄的核取方塊，或使用欄選擇器來選擇大量選取專案。

![選取或取消選取頁面](./assets/action-change-selection.png){width="500"}上的全部或全部

## 步驟2：將動作套用至選取的記錄

1. 將&#x200B;**[!UICONTROL Actions]**&#x200B;控制項設定為您要套用的作業。

   **_Example:_**&#x200B;更新屬性

   - 在清單中，選取要更新之每筆記錄的核取方塊。

   - 將&#x200B;**[!UICONTROL Actions]**&#x200B;控制項設為`Update Attributes`。

     ![選取更新屬性動作](./assets/action-select.png){width="450"}

   - 按一下&#x200B;**[!UICONTROL Submit]**。

     「更新屬性」頁面會依左側面板中的群組來列出所有可用的屬性。

     ![更新屬性頁面](./assets/action-update-attributes.png){width="700" zoomable="yes"}

   - 選取每個屬性旁的&#x200B;**[!UICONTROL Change]**&#x200B;核取方塊，並進行必要的變更。

   - 按一下&#x200B;**[!UICONTROL Save]**&#x200B;以更新所選記錄群組的屬性。

1. 完成時，按一下&#x200B;**[!UICONTROL Submit]**。

## 核取方塊動作

| 動作 | 說明 |
|--- |--- |
| [!UICONTROL Select All] | 選取清單中所有記錄的核取方塊。 |
| [!UICONTROL Unselect All] | 清除清單中所有記錄的核取方塊。 |
| [!UICONTROL Select All on This Page] | 選取目前頁面上顯示的記錄核取方塊。 |
| [!UICONTROL Deselect All on This Page] | 清除目前頁面上顯示的記錄核取方塊。 |

{style="table-layout:auto"}
