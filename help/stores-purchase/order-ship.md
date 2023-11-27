---
title: 出貨訂單
description: 瞭解如何完成處理訂單的送貨資訊，並檢視送貨與追蹤資訊。
exl-id: 60b0e66a-8ee6-4091-94ce-179cc2fdf57a
feature: Orders, Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%

---

# 出貨訂單

已付款但正在等待出貨的訂單具有 `Processing` 狀態。 出貨記錄包含與訂單相關之履行處理的詳細歷史記錄。 在訂單完成之前，可以出貨一部分。

1. 在 _管理員_ 側欄，選取 **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. 在 _[!UICONTROL Orders]_清單，尋找要出貨的訂單，然後按一下以開啟。

1. 在右上角，按一下 **[!UICONTROL Ship]** 按鈕。

1. 如果您要更新帳單或送貨地址，請按一下 **[!UICONTROL Edit]** 區段右上角的連結。

   進行必要的變更，然後按一下 **[!UICONTROL Save Order Address]**.

1. 若要讓承運商產生送貨標籤，請選取 **[!UICONTROL Create Shipping Label]** 核取方塊並設定選項：

   - 若要新增追蹤編號，請向下捲動至 _[!UICONTROL Shipping Information]_部分，然後按一下&#x200B;**[!UICONTROL Add Tracking Number]**.

   - 執行下列任一項作業：

      - 選取 **[!UICONTROL Carrier]** 並輸入追蹤 **[!UICONTROL Number]**.

      - 設定 **[!UICONTROL Carrier]** 至 `Custom Value`，輸入 **[!UICONTROL Title]** ，並輸入追蹤 **[!UICONTROL Number]**.

      - [檢視追蹤資訊](#track-the-shipment).

1. 若要進行部份出貨，請向下捲動至「要出貨的料號」區段，然後輸入 **[!UICONTROL Qty to Ship]** 每個專案。

1. 若要透過電子郵件通知客戶出貨，請執行下列步驟：

   - 輸入您要加入的任何註解 **[!UICONTROL Shipment Comments]** 方塊。

   - 若要在傳送給客戶的通知電子郵件中包含註解，請選取 **[!UICONTROL Append Comments]** 核取方塊。

   - 若要將出貨電子郵件復本傳送給您自己，請選取 **[!UICONTROL Email Copy of Shipment]** 核取方塊。

     商業發票電子郵件的狀態會顯示在已完成商業發票的商業發票號碼旁，表示已傳送或未傳送。

1. 完成後，按一下 **[!UICONTROL Submit Shipment]**.

   訂單狀態變更自 `Processing` 至 `Complete`.

>[!NOTE]
>
>如果訂單是以「店內交貨」方式下單，則無法使用送貨選項。 按一下 **[!UICONTROL Notify Order is Ready for Pickup]** 以觸發傳送給客戶的電子郵件。 訂單的狀態隨後會變更為 `Complete`.

## 檢視出貨明細

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. 在清單中尋找出貨，然後按一下以開啟記錄。

1. 如果您想要在訂單中新增註解，請向下捲動至 _[!UICONTROL Comments History]_部分，然後在方塊中輸入註解。

   - 若要透過電子郵件將註解傳送給客戶，請選取 **[!UICONTROL Notify Customer by Email]** 核取方塊。

   - 若要在客戶帳戶中張貼註解，請選取 **[!UICONTROL Visible on Frontend]** 核取方塊。

1. 按一下 **[!UICONTROL Submit Comment]**.

## 追蹤出貨

**方法1：** 從訂單資訊頁標

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. 在格線中尋找出貨訂單，然後按一下 **[!UICONTROL View]**.

1. 向下捲動至 _[!UICONTROL Shipping & Handling Information]_區段並按一下&#x200B;**[!UICONTROL Track Order]**.

   任何可用的追蹤資訊都會顯示在快顯視窗中。

1. 準備就緒後，按一下 **[!UICONTROL Close Window]**.

**方法2：** 從訂單出貨頁標

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. 在清單中尋找出貨，然後按一下以開啟記錄。

1. 按一下 **[!UICONTROL Track this Shipment]**.

   任何可用的追蹤資訊都會顯示在快顯視窗中。

1. 準備就緒後，按一下 **[!UICONTROL Close Window]**.
