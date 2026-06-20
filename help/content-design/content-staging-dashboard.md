---
title: 內容中繼儀表板
description: 使用內容測試儀表板來存取所有使用中和即將來臨的行銷活動的概觀。
exl-id: 67c18c1c-94c3-4d89-ae1e-868a465431e3
feature: Page Content, Staging
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hant/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案（Adobe管理的PaaS基礎結構）和內部部署專案的Adobe Commerce 。"
TQID: https://experienceleague.adobe.com/Hwrb3dYdJlggWN-Z-nUKxVBhsejFMZR-yWIgRzfJifQ
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 452
ht-degree: 0%

---

# 內容中繼儀表板

{{ee-feature}}

[!UICONTROL Content Staging]儀表板提供所有使用中和即將來臨的行銷活動的概觀。 圖示板的格式可從格線變更為時間軸。 您也可以使用篩選器來尋找行銷活動、自訂欄版面配置，以及儲存格線的不同檢視。 如需工作區控制項的詳細資訊，請參閱[管理員工作區](../getting-started/admin-workspace.md)。

![網格檢視中的暫存儀表板](./assets/content-staging-grid-view.png){width="600" zoomable="yes"}

## 檢視測試儀表板

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Content Staging]_>**[!UICONTROL Dashboard]**。

1. 若要變更儀表板的格式，請將&#x200B;**[!UICONTROL View As]**&#x200B;控制項設為`list`、`Grid`或`Timeline`。

   ![時間表檢視](./assets/content-staging-dashboard-timeline.png){width="600" zoomable="yes"}

   顯示時間軸時，可使用右下角的滑桿將檢視從一週調整為四周。 每一欄代表一天。

1. 如果顯示時間軸，請將滑桿拖曳至最右邊的`4w`位置，以檢視較長的時間範圍。

   ![四周檢視](./assets/content-staging-timeline-4-week-view.png){width="600" zoomable="yes"}

1. 若要顯示促銷活動的一般資訊，請按一下頁面上的任何專案。

   - 若要開啟行銷活動，請按一下&#x200B;**[!UICONTROL View/Edit]**。

   - 若要檢視促銷活動當天商店中客戶的外觀，請按一下&#x200B;**[!UICONTROL Preview]**。

   ![行銷活動資訊](./assets/content-staging-campaign-info.png){width="600" zoomable="yes"}

## 中繼儀表板欄說明

| 欄 | 說明 |
|--- |--- |
| [!UICONTROL Status] | 行銷活動的狀態。 `Active`或`Upcoming`。 |
| [!UICONTROL Update Name] | 行銷活動的名稱。 |
| [!UICONTROL Includes] | 定義行銷活動中包含多少物件。 |
| [!UICONTROL Start Time] | 行銷活動開始的日期。 |
| [!UICONTROL End Time] | 行銷活動結束的日期。 |
| [!UICONTROL Description] | 每個行銷活動的額外說明。 |
| [!UICONTROL Action] | 可套用至個別記錄的動作包括： <br/>**[!UICONTROL View/Edit]**— 在編輯模式下開啟行銷活動。<br/>**[!UICONTROL Preview]**  — 在預覽模式下顯示行銷活動。 |

{style="table-layout:auto"}

## 編輯行銷活動

除了沒有結束日期的價格規則行銷活動外，您都可以從測試儀表板編輯現有的行銷活動物件。

>[!NOTE]
>
>如果最初建立的有效行銷活動沒有結束日期，則無法在稍後編輯行銷活動以包含結束日期。 在這種情況下，必須建立重複的行銷活動並輸入所需的結束日期。

![行銷活動詳細資料](./assets/content-staging-dashboard-view-edit.png){width="600" zoomable="yes"}

此範例中的行銷活動包含兩個類別和三個個別產品。

請依照下列步驟，編輯此行銷活動中的任何物件。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Content Staging]_>**[!UICONTROL Dashboard]**。

1. 在顯示的清單或時間軸中尋找促銷活動，並開啟它以存取詳細資訊：

   - 若要顯示清單，請按一下&#x200B;**[!UICONTROL Select]**，然後在&#x200B;_[!UICONTROL Action]_&#x200B;欄中按一下&#x200B;**[!UICONTROL View/Edit]**。
   - 若要顯示時間表，請按一下以顯示摘要，然後按一下&#x200B;**[!UICONTROL View/Edit]**。

1. 視需要更新&#x200B;_[!UICONTROL General]_&#x200B;區段中的任何設定。

1. 展開![展開選取器](../assets/icon-display-expand.png)包含要編輯之專案的任何區段。

   ![正在更新行銷活動專案的指派產品](./assets/content-staging-campaign-edit-products.png){width="600" zoomable="yes"}

1. 按一下&#x200B;**[!UICONTROL Save]**。
