---
title: 排定的訂單作業
description: 瞭解支援此功能的排程訂單作業和訂單cron設定。
exl-id: 330fe75a-d901-4696-946e-fa7af9ea3d40
feature: Orders, Configuration
source-git-commit: db859c40cd6f052a8f1153e245c23d9f1ea97d33
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# 排定的訂單作業

使用[Cron](../systems/cron.md)工作來排程下列順序處理工作：

![訂單格線](./assets/orders-grid.png){width="700" zoomable="yes"}

## 設定暫緩付款訂單期限

含待處理付款的訂單的存留期由&#x200B;_訂單Cron設定_&#x200B;組態決定。 預設值設為480分鐘，即8小時。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Sales]**&#x200B;區段並在下方選擇&#x200B;**[!UICONTROL Sales]**。

1. 展開&#x200B;**[!UICONTROL Orders Cron Settings]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![訂單Cron設定](../configuration-reference/sales/assets/sales-orders-cron-settings.png){width="600" zoomable="yes"}

1. 針對&#x200B;**[!UICONTROL Pending Payment Order Lifetime (minutes)]**，輸入暫緩付款到期之前的分鐘數。

1. 按一下&#x200B;**[!UICONTROL Save Config]**。

## 啟用排定的網格更新並重新索引

「網格設定」組態會排定下列訂單管理網格的更新，並按照[Cron](../systems/cron.md)的排程重新索引資料：

- [訂購](orders.md#orders-workspace)
- [發票](invoices.md)
- [出貨](shipments.md)
- [銷退折讓單](credit-memos.md)

藉由排程這些工作，您可以避免在儲存資料時發生鎖定，並縮短處理時間。 啟用後，任何更新只會在排程的cron作業期間發生。 為了獲得最佳結果，應將Cron設定為每分鐘執行一次。

**_若要啟用更新並重新索引：_**

當[生產模式](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#production-mode) (在雲端基礎結構上的Adobe Commerce中使用的預設模式)啟用時，請執行以下命令：

``bin/magento config:set dev/grid/async_indexing 1``

啟用[預設模式](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#default-mode)時，請完成下列步驟：

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Advanced]**&#x200B;區段並選擇&#x200B;**[!UICONTROL Developer]**。

1. 展開&#x200B;**[!UICONTROL Grid Settings]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

1. 將&#x200B;**[!UICONTROL Asynchronous Indexing]**&#x200B;設為`Enable`。

   ![格線設定](../configuration-reference/advanced/assets/developer-grid-settings.png){width="600" zoomable="yes"}

1. 按一下&#x200B;**[!UICONTROL Save Config]**。
