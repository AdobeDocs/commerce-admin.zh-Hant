---
title: 管理Newsletter訂閱者
description: 瞭解如何使用作用中訂閱的簡單清單管理您的新聞稿訂閱者。
exl-id: c7e8e642-e3fd-4979-9ea3-2d96839730b2
feature: Customers, Communications
TQID: https://experienceleague.adobe.com/l4Kmwm62UeLYZva-SCsVHPmf4IbKQhgoyN9N7zo4O0g
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 509
ht-degree: 0%

---

# 管理Newsletter訂閱者

您應定期管理訂閱清單，並確保處理任何取消訂閱的請求，此為最佳作法。 在某些司法權區，法律規定在特定期間內處理取消訂閱的請求。

您可以使用作用中訂閱的簡單清單，輕鬆管理訂閱者。 當客戶提交取消訂閱請求時，您只需將&#x200B;_取消訂閱_&#x200B;動作套用至一或多個選取的訂閱即可。

在具有多個商店檢視的單一網站設定中，客戶帳戶訂閱可以與特定商店檢視相關聯。

在具有全域[客戶帳戶範圍](../customers/customer-account-scope.md)的多存放區和多網站設定中，客戶帳戶可以訂閱多個網站/存放區的電子報。 在這種情況下，您可能想要編輯客戶帳戶以管理訂閱群組，或取消特定網站/商店的訂閱以履行請求。

如果您想要使用協力廠商服務來傳送電子報，可以將訂閱清單匯出為CSV或XML檔案。

## 管理客戶的訂閱

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL All Customers]**。

1. 在格線中尋找客戶，然後按一下&#x200B;_[!UICONTROL Action]_&#x200B;欄中的&#x200B;**[!UICONTROL Edit]**。

1. 按一下左側面板中的&#x200B;**[!UICONTROL Newsletter]**。

1. 根據您的網站/商店設定修改客戶的訂閱。

   若是單一網站/單一商店設定，您只需選取或清除「**[!UICONTROL Subscribed to Newsletter]**」核取方塊即可。

   ![單一商店客戶電子報訂閱核取方塊](./assets/newsletter-customer-single-store.png){width="500" zoomable="yes"}

   若是單一網站/多存放區設定，您可以選取或清除&#x200B;**[!UICONTROL Subscribed to Newsletter]**&#x200B;核取方塊，並將&#x200B;**[!UICONTROL Subscribed on Store View]**&#x200B;設定為訂閱的正確存放區檢視。

   ![多商店客戶電子報訂閱核取方塊和商店檢視選擇器](./assets/newsletter-customer-multi-store.png){width="500" zoomable="yes"}

   針對具有全域客戶帳戶範圍的多地點/多商店設定，頁面會顯示所有地點的訂閱狀態。 您可以選取或清除「**[!UICONTROL Subscribed]**」核取方塊及/或變更訂閱的&#x200B;**[!UICONTROL Store View]**。

   ![多網站客戶電子報訂閱核取方塊和商店檢視選取器](./assets/newsletter-customer-multi-site.png){width="500" zoomable="yes"}

1. 按一下&#x200B;**[!UICONTROL Save Customer]**。

## 從訂閱者清單取消訂閱

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Subscribers]**。

   針對部分客戶有多個網站訂閱的多網站設定，每個訂閱都會顯示為格線中的條列專案。

1. 在網格中尋找訂戶，並選取第一欄中的核取方塊。

   >[!NOTE]
   >
   >若要大量取消訂閱，請選取您要取消之每個訂閱者的核取方塊。

1. 將&#x200B;_[!UICONTROL Action]_&#x200B;控制項設為&#x200B;**[!UICONTROL Unsubscribe]**&#x200B;並按一下&#x200B;**[!UICONTROL Submit]**。

   ![取消訂閱電子報](./assets/newsletter-unsubscribe.png){width="600" zoomable="yes"}

   記錄的狀態變更為`Unsubscribed`。

## 匯出訂閱者清單

1. 從&#x200B;_[!UICONTROL Newsletter Subscribers]_&#x200B;清單中，使用篩選器控制項僅包含具有_&#x200B;狀態&#x200B;_（共`Subscribed`個）的記錄，並用於適當的網站、商店或商店檢視。

1. 將&#x200B;**[!UICONTROL Export to]**&#x200B;控制項設定為下列其中一項：

   - `CSV`
   - `XML`

1. 按一下&#x200B;**[!UICONTROL Export]**，然後在熒幕底部尋找提示並儲存檔案。

   ![匯出Newsletter訂閱者](./assets/newsletter-subscribers-export.png){width="600" zoomable="yes"}

## 從訂閱者清單中刪除訂閱者

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Subscribers]**。

1. 在網格中尋找訂戶，並選取第一欄中的核取方塊。

1. 將&#x200B;_[!UICONTROL Action]_&#x200B;控制項設為&#x200B;**[!UICONTROL Delete]**&#x200B;並按一下&#x200B;**[!UICONTROL Submit]**。

1. 提示確認時，按一下&#x200B;**[!UICONTROL OK]**。
