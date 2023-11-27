---
title: Newsletter佇列
description: 瞭解如何管理新聞稿佇列，以傳送多個新聞稿批次。
exl-id: bf85b3ff-3093-49a1-8a9a-d3ea71fe3f09
feature: Customers, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---

# Newsletter佇列

為了管理伺服器上的負載，含有許多訂閱者的電子報會以多個批次的佇列傳送。 您可以定期檢查Newsletter佇列以檢查狀態，並檢視已處理的數量。 傳輸期間發生的任何問題都會顯示在 _Newsletter問題_ 報告。

## 傳送Newsletter

1. 在 _管理員_ 選單，前往 **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Template]**.

1. 在格線中，尋找 [電子報範本](newsletter-template.md) 即會傳送並設定 **[!UICONTROL Action]** 欄至 `Queue Newsletter`.

1. 的 **[!UICONTROL Queue Date Start]**，從行事曆選取傳輸開始的日期(![行事曆圖示](../assets/icon-calendar.png))。

1. 的 **[!UICONTROL Subscribers From]**，選取要納入電子郵件爆炸的每個商店檢視。

1. 填妥電子郵件標題資訊：

   - 輸入電子報的簡短說明 **[!UICONTROL Subject]** 電子郵件標頭的行。

   - 輸入 **[!UICONTROL Sender Name]**.

   - 的 **[!UICONTROL Sender Email]**，輸入寄件者的電子郵件地址。

     寄件者的預設名稱和電子郵件地址在設定中指定。

     ![Newsletter佇列資訊](./assets/newsletter-queue-information1.png){width="600" zoomable="yes"}

1. 如果適用，請在 **[!UICONTROL Message]** 方塊取消訂閱。

   >[!NOTE]
   >
   >請勿移除許多司法管轄區法律要求的指示。

1. 若要將自訂樣式套用至電子報，請將其新增至 **[!UICONTROL Newsletter Styles]** 欄位。

1. 完成後，按一下 **[!UICONTROL Save and Resume]**.

   Newsletter會出現在等待處理的佇列中。

## 檢查問題

在 _管理員_ 選單，前往 **[!UICONTROL Reports]** > _[!UICONTROL Marketing]_>**[!UICONTROL Newsletter Problem Reports]**.

## 按鈕列

| 按鈕 | 說明 |
|--- |--- |
| **[!UICONTROL Back]** | 返回「Newsletter範本」頁面而不儲存變更。 |
| **[!UICONTROL Reset]** | 將佇列資訊表單中未儲存的任何變更重設為先前的值。 |
| **[!UICONTROL Preview Template]** | 在個別標籤中開啟預覽頁面。 |
| **[!UICONTROL Save and Resume]** | 儲存所有所做的變更。 將Newsletter放入佇列。 |
| **[!UICONTROL Save Newsletter]** | 儲存所有所做的變更。 將Newsletter放入佇列。 |

{style="table-layout:auto"}

## 欄

| 欄 | 說明 |
|--- |--- |
| [!UICONTROL ID] | 指派給每個Newsletter範本的唯一數值識別碼。 |
| [!UICONTROL Queue Start] | 電子報的寄出日期。 |
| [!UICONTROL Queue End] | 電子報完成傳送的日期。 |
| [!UICONTROL Subject] | Newsletter範本的主題。 |
| [!UICONTROL Status] | 表示Newsletter郵件的狀態。 可能的值： `Sent`， `Canceled`， `Not Sent`， `Sending`，或 `Paused`. |
| [!UICONTROL Processed] | 表示已傳送多少電子報。 |
| [!UICONTROL Recipients] | 表示訂閱者已收到多少電子報。 |
| [!UICONTROL Actions] | **[!UICONTROL Preview]**：開啟個別視窗以預覽範本。 |

{style="table-layout:auto"}
