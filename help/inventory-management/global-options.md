---
title: 設定 [!DNL Inventory Management] 全域選項
description: 瞭解如何為網站的產品和庫存設定預設 [!DNL Inventory Management] 設定選項。
exl-id: 1a8c9605-ae61-4d45-b549-64911b329203
feature: Inventory, Configuration
source-git-commit: 7384481d1a4a2a04882d4c99448cca75abc9be31
workflow-type: tm+mt
source-wordcount: '639'
ht-degree: 0%

---

# 設定[!DNL Inventory Management]全域選項

設定您網站產品與庫存的預設設定選項。 透過[設定產品選項](product-options.md)，可以覆寫每個產品的部分設定。 若要設定距離優先順序設定，請參閱[設定距離優先順序演演算法](distance-priority-algorithm.md)。

## 全域設定產品和庫存選項

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Catalog]**&#x200B;並選擇&#x200B;**[!UICONTROL Inventory]**。

1. 展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Stock Options]**&#x200B;區段並設定選項：

   ![股票期權](assets/config-catalog-inventory-stock-options.png){width="600" zoomable="yes"}

   - 若要在下訂單時調整庫存量，請將&#x200B;**[!UICONTROL Decrease Stock When Order is Placed]**&#x200B;設為`Yes`。

   - 若要在訂單取消時退回料號至庫存，請&#x200B;**[!UICONTROL Set Items' Status to be in Stock When Order in Cancelled]**&#x200B;至`Yes`。

   - 若要繼續顯示目錄中不再有庫存的產品，請將&#x200B;**[!UICONTROL Display Out of Stock Products]**&#x200B;設為`Yes`。

   - 如果已啟用[價格警示](alert-setup.md)，客戶可以註冊在產品有存貨時收到通知。

   - 若要設定在產品頁面上顯示最後剩餘存貨金額的開始時間，請輸入&#x200B;**[!UICONTROL Only X left Threshold]**&#x200B;的金額。

     當庫存量達到臨界值時，訊息就會開始出現。 例如，如果設為`3`，當庫存數量達到三時會顯示訊息`Only 3 left`。 訊息會調整以反映庫存中的數量，直到數量達到零為止。

   - 若要在產品頁面上顯示「有庫存」或「無庫存」訊息，請將&#x200B;**[!UICONTROL Display Products Availability In Stock on Storefront]**&#x200B;設為`Yes`。

   - 若要在載入購物車中的產品時檢查詳細目錄，請將&#x200B;**[!UICONTROL Enable Inventory Check On Cart Load]**&#x200B;設定為`Yes`。 停用此選項時，會略過詳細目錄檢查。 停用此選項會加快結帳速度，尤其是當購物車中有許多專案時。 不過，如果您略過預先驗證，客戶稍後在結帳程式中可能會看到「無庫存」錯誤。

   - 若要保持詳細目錄和目錄之間的一致性，請將&#x200B;**[!UICONTROL Synchronize with Catalog]**&#x200B;設定為`Yes`。 啟用此選項後，庫存資料會根據目錄變更進行調整（例如已移除產品、已變更產品SKU以及已變更產品型別）。

1. 展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Product Stock Options]**&#x200B;區段並設定選項：

   - 若要啟用目錄的[庫存控制](enable.md)，請將&#x200B;**[!UICONTROL Manage Stock]**&#x200B;設為`Yes`。

     ![產品庫存選項](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - 將&#x200B;**[!UICONTROL Backorders]**&#x200B;設定為下列其中一項：

     | 選項 | 說明 |
     | ----- | ----- |
     | `No Backorders` | 產品無庫存時，不接受[延期交貨](backorders.md)。 |
     | `Allow Qty Below 0` | 當數量低於零時，接受延期交貨。 |
     | `Allow Qty Below 0 and Notify Customer` | 當數量低於零時，系統會接受延期交貨，並通知客戶仍可下訂單。 |

   - 輸入&#x200B;**[!UICONTROL Maximum Qty Allowed in Shopping Cart]**。

   - 輸入&#x200B;**[!UICONTROL Out-of-Stock Threshold]**&#x200B;的金額：

     | 值 | 說明 |
     | ----- |-----|
     | 正數 | 如果停用「延期交貨」，請輸入正金額。 |
     | 零 | 啟用延期交貨訂單後，輸入`0`可允許無限延期交貨。 |
     | 負數金額 | 若已啟用「延期交貨」，則建議輸入負金額。 此金額會新增至「可銷售數量」。 例如，輸入`-50`以允許此金額以下的訂單。 |

   - 為選取的群組和金額輸入&#x200B;**[!UICONTROL Minimum Qty Allowed in Shopping Cart]**。

   - 針對&#x200B;**[!UICONTROL Notify for Quantity Below]**，輸入庫存等級，以觸發專案無庫存的通知。

   - 若要啟用產品的數量增加，請將&#x200B;**[!UICONTROL Enable Qty Increments]**&#x200B;設為`Yes`。 然後，針對&#x200B;**[!UICONTROL Qty Increments]**，輸入必須符合需求的專案數。

     例如，以6為增量銷售的專案，可以以`6`、`12`、`18`等數量購買。

   - 針對[!DNL Inventory Management]，**[!UICONTROL Automatically Return Credit Memo Item to Stock]**&#x200B;設定為`No`。 在提交銷退折讓單時，您可以輸入並選取將存貨退回給來源。

1. 展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Admin bulk operations]**&#x200B;區段並設定選項：

   ![管理員大量作業](assets/config-catalog-inventory-admin-bulk-operations.png){width="600" zoomable="yes"}

   - 設定&#x200B;**[!UICONTROL Run asynchronously]**&#x200B;以非同步方式執行大量產品動作的大量作業

     這些作業包括大量[指派和取消指派來源](bulk-assignment.md)，以及[將存貨轉移到來源](inventory-transfer.md)。 它會收集大量動作，直到達到非同步批次大小為止，然後執行這些動作。 此選項預設為停用。 建議您在啟用之前先透過大量動作檢閱您的效能。

     >[!NOTE]
     >
     >若要設定並支援&#x200B;_非同步佇列管理員_，您必須使用命令列發出命令。 此步驟可能需要開發人員協助。 請參閱&#x200B;_設定指南_&#x200B;中的[開始訊息佇列消費者](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html?lang=zh-Hant)。

   - 如果已啟用，請設定&#x200B;**[!UICONTROL Asynchronous batch size]**。 預設批次大小為100。 當大量程式達到此數量時，系統會觸發此事件。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。
