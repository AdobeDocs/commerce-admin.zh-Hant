---
title: 店內傳遞
description: 瞭解如何為商店設定店內傳遞選項。
exl-id: bd64b110-5c39-41c6-8a0c-38561b2a5bf4
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 0%

---

# 店內傳遞

使用店內送貨方式時，客戶可選取在結帳期間作為取貨地點的來源。

![結帳時的店內傳遞方法](./assets/luma-in-store-example.png){width="700" zoomable="yes"}

在店面結帳期間：

1. 客戶點按 **[!UICONTROL Pick In Store]** 或選取 _[!UICONTROL In-Store Pickup Delivery]_送貨方法。
1. 此 _[!UICONTROL Pick In Store]_簽出索引標籤隨即開啟。

當客戶有地址，或先前在切換至 _[!UICONTROL Pick In Store]_標籤：

- 設定半徑內最接近客戶地址的來源會自動預先選取為取貨商店。
- 客戶點按時 **[!UICONTROL Select Other]**，則 _[!UICONTROL Select Store]_搜尋表單隨即開啟。 清單中只會顯示與預先選取的存放區之間設定距離（半徑）內的存放區。 清單中的所有存放區會依與預先選取之存放區的距離排序。
- 當客戶在搜尋欄位中輸入郵遞區號或城市名稱時，清單中只會顯示已設定距離搜尋地點（半徑）內的商店。 清單中的所有存放區會依搜尋位置的距離排序。
- 當客戶從搜尋欄位清除郵遞區號或城市名稱時，所有指派給購物車中產品的收取商店都會顯示給客戶。 清單中的所有存放區都會以原始程式碼的遞增順序排序，不受任何距離（半徑）限制。

如果客戶沒有地址，或先前未填寫送貨地址表單，則切換至 _[!UICONTROL Pick In Store]_標籤：

- 頁面會顯示 _我們無法根據可用資訊預先選取取車地點_ 訊息。
- 客戶點按時 **[!UICONTROL Select Store]**，則 _[!UICONTROL Select Store]_搜尋表單隨即開啟。
- 所有指定給購物車中產品的收取商店都會以原始程式碼的遞增順序顯示，沒有任何距離（半徑）限制。
- 當客戶在搜尋欄位中輸入郵遞區號或城市名稱時，清單中只會顯示已設定距離搜尋地點（半徑）內的商店。 清單中的所有存放區會依搜尋位置的距離排序。

## 設定前

- 確定您有非預設的庫存和來源。 如需如何將來源設定為取車地點的詳細資訊，請參閱 [新增來源](../inventory-management/sources-add.md).
- 請確定您已設定「距離優先順序演演算法」。 如需詳細資訊，請參閱 [設定距離優先順序演演算法](../inventory-management/distance-priority-algorithm.md).
- 確定您擁有 [下載和匯入](../inventory-management/cli.md#import-geocodes) 離線計算的所有必要地理代碼。
- 確定您已設定 [預設稅捐目的地計算](../configuration-reference/sales/tax.md#default-tax-destination-calculation) 設定。

>[!IMPORTANT]
>
>**在店面，搜尋結果會依距離（半徑）篩選以顯示相關結果：**<br><br>
>如果客戶有送貨地址，則計算距離（半徑）的基準地點會取自送貨地址。<br><br>
>如果客戶沒有送貨地址，則會從 [預設稅捐目的地計算](../configuration-reference/sales/tax.md#default-tax-destination-calculation) 設定。 這些設定是按商店檢視設定的，您必須設定「預設稅捐目的地計算」設定，以確保取貨商店搜尋正常運作。

## 設定店內傳遞

首先，檢查是否已啟用店內傳遞。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Sales]** 並選擇 **[!UICONTROL Delivery Methods]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL In-Store Delivery]** 區段。

   ![店內傳遞](../configuration-reference/sales/assets/delivery-methods-in-store-delivery.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Enabled]** 至 `Yes`.

   >[!NOTE]
   >
   >如有需要，請清除 **[!UICONTROL Use system value]** 核取方塊，以變更任何欄位的預設值。

1. 輸入 **[!UICONTROL Method Name]** 說明用於產生出貨估計值的計算方法。

   方法名稱會出現在購物車中經過計算的預估比率旁。

1. 輸入 **[!UICONTROL Title]** 您希望顯示的 _店內傳遞_ 區段進行結帳。

   預設標題為 `In-Store Pickup Delivery`.

1. 若要向客戶收取店內取貨服務的費用，請在 **[!UICONTROL Price]** 欄位。

1. 輸入 **[!UICONTROL Search Radius]** 以公里為單位，搜尋店面結帳處的商店取貨地點。

1. 的 **[!UICONTROL Displayed Error Message]**，輸入當店內傳遞無法使用時顯示的訊息。

   預設訊息為 `In-Store Delivery is not available. To use this delivery method, please contact us.`

1. 按一下 **[!UICONTROL Save Config]**.
