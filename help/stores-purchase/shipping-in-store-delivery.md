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

1. 客戶按一下&#x200B;**[!UICONTROL Pick In Store]**&#x200B;或選取&#x200B;_[!UICONTROL In-Store Pickup Delivery]_&#x200B;送貨方法。
1. _[!UICONTROL Pick In Store]_&#x200B;簽出索引標籤隨即開啟。

當客戶有地址，或先前在切換至&#x200B;_[!UICONTROL Pick In Store]_&#x200B;索引標籤之前已填妥送貨地址表單時：

- 設定半徑內最接近客戶地址的來源會自動預先選取為取貨商店。
- 當客戶按一下&#x200B;**[!UICONTROL Select Other]**&#x200B;時，_[!UICONTROL Select Store]_&#x200B;搜尋表單會開啟。 清單中只會顯示與預先選取的存放區之間設定距離（半徑）內的存放區。 清單中的所有存放區會依與預先選取之存放區的距離排序。
- 當客戶在搜尋欄位中輸入郵遞區號或城市名稱時，清單中只會顯示已設定距離搜尋地點（半徑）內的商店。 清單中的所有存放區會依搜尋位置的距離排序。
- 當客戶從搜尋欄位清除郵遞區號或城市名稱時，所有指派給購物車中產品的收取商店都會顯示給客戶。 清單中的所有存放區都會以原始程式碼的遞增順序排序，不受任何距離（半徑）限制。

如果客戶沒有地址或之前未填寫送貨地址表單，則切換至&#x200B;_[!UICONTROL Pick In Store]_&#x200B;標籤：

- 頁面顯示&#x200B;_我們無法根據可用資訊預先選取取車地點_&#x200B;訊息。
- 當客戶按一下&#x200B;**[!UICONTROL Select Store]**&#x200B;時，_[!UICONTROL Select Store]_&#x200B;搜尋表單會開啟。
- 所有指定給購物車中產品的收取商店都會以原始程式碼的遞增順序顯示，沒有任何距離（半徑）限制。
- 當客戶在搜尋欄位中輸入郵遞區號或城市名稱時，清單中只會顯示已設定距離搜尋地點（半徑）內的商店。 清單中的所有存放區會依搜尋位置的距離排序。

## 設定前

- 確定您有非預設的庫存和來源。 如需如何將來源設定為取車地點的詳細資訊，請參閱[新增來源](../inventory-management/sources-add.md)。
- 請確定您已設定「距離優先順序演演算法」。 如需詳細資訊，請參閱[設定距離優先順序演演算法](../inventory-management/distance-priority-algorithm.md)。
- 請確定您已下載[並匯入](../inventory-management/cli.md#import-geocodes)離線計算所需的所有地理代碼。
- 確定您已設定[預設稅捐目的地計算](../configuration-reference/sales/tax.md#default-tax-destination-calculation)設定。

>[!IMPORTANT]
>
>**在店面，搜尋結果會依距離（半徑）篩選，以顯示相關結果：**<br><br>
>如果客戶有送貨地址，則會從送貨地址取得計算距離（半徑）的基準位置。<br><br>
>如果客戶沒有送貨地址，則計算距離的基準地點是從[預設稅捐目的地計算](../configuration-reference/sales/tax.md#default-tax-destination-calculation)設定中取得。 這些設定是按商店檢視設定的，您必須設定「預設稅捐目的地計算」設定，以確保取貨商店搜尋正常運作。

## 設定店內傳遞

首先，檢查是否已啟用店內傳遞。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Sales]**&#x200B;並選擇&#x200B;**[!UICONTROL Delivery Methods]**。

1. 展開&#x200B;**[!UICONTROL In-Store Delivery]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![店內傳遞](../configuration-reference/sales/assets/delivery-methods-in-store-delivery.png){width="600" zoomable="yes"}

1. 將&#x200B;**[!UICONTROL Enabled]**&#x200B;設為`Yes`。

   >[!NOTE]
   >
   >如有需要，請清除&#x200B;**[!UICONTROL Use system value]**&#x200B;核取方塊以變更任何欄位的預設值。

1. 輸入描述用來產生出貨估計的計算方法的&#x200B;**[!UICONTROL Method Name]**。

   方法名稱會出現在購物車中經過計算的預估比率旁。

1. 輸入您要在結帳期間針對&#x200B;_店內傳遞_&#x200B;區段顯示的&#x200B;**[!UICONTROL Title]**。

   預設標題為`In-Store Pickup Delivery`。

1. 若要向客戶收取店內取貨服務的費用，請在&#x200B;**[!UICONTROL Price]**&#x200B;欄位中輸入費用。

1. 輸入在店面結帳時搜尋商店取貨地點的&#x200B;**[!UICONTROL Search Radius]**&#x200B;公里。

1. 針對&#x200B;**[!UICONTROL Displayed Error Message]**，輸入當店內傳遞無法使用時所顯示的訊息。

   預設訊息為`In-Store Delivery is not available. To use this delivery method, please contact us.`

1. 按一下&#x200B;**[!UICONTROL Save Config]**。
