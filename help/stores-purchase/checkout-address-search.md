---
title: 結帳時的地址搜尋
description: 瞭解如何在商店結帳時包含地址搜尋。
exl-id: 8153c456-0848-4bb4-8deb-8219323344ed
feature: Checkout
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 0%

---

# 結帳時的地址搜尋

{{ee-feature}}

您的客戶在通訊錄中可能有許多已儲存的地址和資訊，尤其是定期回頭的客戶或輸入多個訂單和出貨地點的公司。 顯示許多位址可能會大幅減慢結帳載入與程式的速度，並導致購物體驗不佳。 為協助提高結帳的回應速度，建議您啟用並設定網站的位址搜尋。

>[!NOTE]
>
>預設不會啟用地址搜尋。 您可以設定此功能以包含您網站上的功能。

當啟用此功能且客戶的儲存地址數目符合或超過設定的限制時，_送貨_&#x200B;和&#x200B;_檢閱與付款_&#x200B;步驟只會顯示一個地址（預設）。 客戶可以按一下&#x200B;**變更地址**，然後依城市、州、街道或郵遞區號搜尋正確的地址，以變更選取的地址。 此功能也支援贈品註冊結帳的地址選擇。

![顯示已儲存送貨地址的簽出](./assets/storefront-checkout-address-search.png){width="700" zoomable="yes"}

如果客戶沒有預設送貨地址，_送貨_&#x200B;頁面會顯示&#x200B;_未選取地址_。 在這種情況下，客戶必須按一下&#x200B;**變更地址**&#x200B;以選取儲存的地址，或按一下&#x200B;**新增地址**&#x200B;以新增並選取地址，然後再繼續結帳。 如果客戶沒有預設帳單地址，則&#x200B;_檢閱與付款_&#x200B;頁面會顯示選取要送貨的地址以及&#x200B;_變更地址_&#x200B;選項。

![未選取任何地址的結帳](./assets/storefront-checkout-address-search-no-default.png){width="600" zoomable="yes"}

## 引號的鎖定位址搜尋

![Adobe Commerce B2B](../assets/b2b.svg) (僅適用於Adobe Commerce B2B)

啟用地址搜尋也會影響從報價建立的訂單結帳，其中客戶的儲存地址數目符合或超過設定的限制。 當報價單完成且客戶進行結帳時，只會顯示選取的送貨地址。 此頁面也會顯示訊息，指出送貨地址已鎖定，且只能在報價單中變更。

![已鎖定報價的送貨地址](./assets/quote-checkout-shipping-address-locked.png){width="600" zoomable="yes"}

## 啟用地址搜尋

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Sales]**&#x200B;並選擇&#x200B;**[!UICONTROL Checkout]**。

1. 展開&#x200B;**[!UICONTROL Checkout Options]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![組態 — 簽出選項](./assets/checkout-checkout-options.png){width="700" zoomable="yes"}

   如需這些組態設定的詳細說明，請參閱&#x200B;_組態參考指南_&#x200B;中的[簽出選項](../configuration-reference/sales/checkout.md#checkout-options)。

1. 將&#x200B;**[!UICONTROL Enable Address Search]**&#x200B;設為`Yes`。

1. 若要指定包含位址搜尋功能的臨界值，請設定&#x200B;**[!UICONTROL Number of Customer Addresses Limit]**&#x200B;選項。

   如有必要，請清除&#x200B;**[!UICONTROL Use system value]**&#x200B;核取方塊以進行此變更。

   當客戶的儲存地址數目達到或超過此限制時，頁面會顯示預設地址（如果客戶有預設地址）或使用&#x200B;_變更地址_&#x200B;選項的&#x200B;_未選取地址_。 預設限製為`10`。

1. 按一下&#x200B;**[!UICONTROL Save Config]**。
