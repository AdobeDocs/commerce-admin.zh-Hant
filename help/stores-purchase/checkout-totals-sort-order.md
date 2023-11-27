---
title: 簽出總計排序順序
description: 瞭解顯示的結帳總計，以及如何設定訂單摘要上的結帳總計排序順序。
exl-id: 2b1345e3-6ad3-472a-af3e-3f7b24577b13
feature: Checkout, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

---

# 簽出總計排序順序

在訂單複查期間，總計會顯示在訂單底部，其中包含折扣、運費、商店退款及稅捐的任何調整。 每個料號的順序會決定計算順序，並在組態中依指定給每個料號的編號來設定。 例如，「小計」是區段中的第一個專案，且被指派值10。 「總量」會顯示於最後，且會指定值100。 在總計區段中的所有其他專案都會被指定這些值之間的值。

![「訂單摘要」會顯示結帳總計](./assets/storefront-checkout-totals.png){width="700" zoomable="yes"}

**_若要設定結帳總計排序順序：_**

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Sales]** 區段並選擇 **[!UICONTROL Sales]** 底下。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Checkout Totals Sort Order]** 區段。

   ![簽出總計選項以編號決定排序順序](../configuration-reference/sales/assets/sales-checkout-totals-sort-order.png){width="600" zoomable="yes"}

   如需這些組態設定的詳細說明，請參閱 [結帳總計排序順序](../configuration-reference/sales/sales.md#checkout-totals-sort-order) 在 _設定參考指南_.

1. 如果設定是針對特定商店檢視， [選擇商店檢視](../configuration-reference/scope-change.md#set-the-scope) 組態適用的位置。

   出現提示時，按一下 **[!UICONTROL OK]** 以繼續。

1. 若要確定 _總計_ 區段，變更指派給每個專案的編號。

   值越低，其在清單中的位置越早。 在預設設定中，`10`)是第一個和全部總計(`100`)是最後一個。

   如有必要，請清除 **[!UICONTROL Use system value]** 核取方塊以完成這些變更。

1. 按一下 **[!UICONTROL Save Config]**.
