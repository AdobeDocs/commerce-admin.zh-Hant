---
title: 出貨訂單
description: 瞭解如何完成處理訂單的送貨資訊，並檢視送貨與追蹤資訊。
exl-id: 60b0e66a-8ee6-4091-94ce-179cc2fdf57a
feature: Orders, Shipping/Delivery
source-git-commit: abd125cc6e61850db55fb31dbcbd9dc38ac0fca5
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---

# 出貨訂單

已付款但正在等候出貨的訂單具有`Processing`狀態。 出貨記錄包含與訂單相關之履行處理的詳細歷史記錄。 在訂單完成之前，可以出貨一部分。

1. 在&#x200B;_管理員_&#x200B;側邊欄中，選取&#x200B;**[!UICONTROL Sales]** > **[!UICONTROL Orders]**。

1. 在&#x200B;_[!UICONTROL Orders]_&#x200B;清單中，找到要送出的訂單，然後按一下以開啟。

1. 按一下右上角的&#x200B;**[!UICONTROL Ship]**&#x200B;按鈕。

1. 如果您要更新帳單或送貨地址，請按一下區段右上角的&#x200B;**[!UICONTROL Edit]**&#x200B;連結。

   進行必要的變更，然後按一下&#x200B;**[!UICONTROL Save Order Address]**。

1. 若要讓承運商產生送貨標籤，請選取「**[!UICONTROL Create Shipping Label]**」核取方塊並設定選項：

   - 若要新增追蹤號碼，請向下捲動至&#x200B;_[!UICONTROL Shipping Information]_&#x200B;區段，然後按一下&#x200B;**[!UICONTROL Add Tracking Number]**。

   - 執行下列任一項作業：

      - 選取&#x200B;**[!UICONTROL Carrier]**&#x200B;並輸入追蹤&#x200B;**[!UICONTROL Number]**。

      - 將&#x200B;**[!UICONTROL Carrier]**&#x200B;設為`Custom Value`，輸入自訂電信業者的&#x200B;**[!UICONTROL Title]**，然後輸入追蹤&#x200B;**[!UICONTROL Number]**。

      - [檢視追蹤資訊](#track-the-shipment)。

1. 若要進行部份出貨，請向下捲動至「要出貨的料號」區段，然後為每個料號輸入&#x200B;**[!UICONTROL Qty to Ship]**。

1. 若要透過電子郵件通知客戶出貨，請執行下列步驟：

   - 輸入您要包含在&#x200B;**[!UICONTROL Shipment Comments]**&#x200B;方塊中的任何註解。

   - 若要在傳送給客戶的通知電子郵件中包含註解，請選取&#x200B;**[!UICONTROL Append Comments]**&#x200B;核取方塊。

   - 若要傳送出貨電子郵件的復本給您自己，請選取&#x200B;**[!UICONTROL Email Copy of Shipment]**&#x200B;核取方塊。

     商業發票電子郵件的狀態會顯示在已完成商業發票的商業發票號碼旁，表示已傳送或未傳送。

1. 完成時，按一下&#x200B;**[!UICONTROL Submit Shipment]**。

   訂單的狀態從`Processing`變更為`Complete`。

>[!NOTE]
>
>如果訂單是以「店內交貨」方式下單，則無法使用送貨選項。 按一下「**[!UICONTROL Notify Order is Ready for Pickup]**」以觸發傳送給客戶的電子郵件。 然後，訂單的狀態會變更為`Complete`。

## 檢視出貨明細

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Sales]** > **[!UICONTROL Shipments]**。

1. 在清單中尋找出貨，然後按一下以開啟記錄。

1. 如果您想要新增註解至訂單，請向下捲動至&#x200B;_[!UICONTROL Comments History]_&#x200B;區段，然後在方塊中輸入註解。

   - 若要透過電子郵件將註解傳送給客戶，請選取&#x200B;**[!UICONTROL Notify Customer by Email]**&#x200B;核取方塊。

   - 若要在客戶的帳戶中張貼註解，請選取&#x200B;**[!UICONTROL Visible on Frontend]**&#x200B;核取方塊。

1. 按一下&#x200B;**[!UICONTROL Update]**。

## 追蹤出貨

**方法1：**&#x200B;從訂單資訊索引標籤

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Sales]** > **[!UICONTROL Orders]**。

1. 在格線中尋找出貨訂單，然後按一下&#x200B;**[!UICONTROL View]**。

1. 向下捲動至&#x200B;_[!UICONTROL Shipping & Handling Information]_&#x200B;區段並按一下&#x200B;**[!UICONTROL Track Order]**。

   任何可用的追蹤資訊都會顯示在快顯視窗中。

1. 準備就緒後，按一下&#x200B;**[!UICONTROL Close Window]**。

**方法2：**&#x200B;從訂單出貨頁標

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Sales]** > **[!UICONTROL Shipments]**。

1. 在清單中尋找出貨，然後按一下以開啟記錄。

1. 按一下&#x200B;**[!UICONTROL Track this Shipment]**。

   任何可用的追蹤資訊都會顯示在快顯視窗中。

1. 準備就緒後，按一下&#x200B;**[!UICONTROL Close Window]**。
