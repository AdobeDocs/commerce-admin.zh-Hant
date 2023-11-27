---
title: 排定存貨存貨來源的優先順序
description: 瞭解如何依優先順序從上到下排列來源，這可用於決定出貨及存貨扣減。
exl-id: 16db3ee3-ce99-40dd-b1a3-fcb145b1298f
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---

# 排定存貨來源的優先順序

新增之後 [來源](sources-manage.md) 至 [stock](stocks-manage.md)，以履行訂單的優先順序，從上到下排列這些來源。 「來源選取演演算法」(SSA)會在決定出貨與存貨扣除額時，使用此訂單提供演演算法「優先順序」。

編輯產品存貨時，存貨的來源優先順序不會影響指定的來源。

在此範例中，UK Stock已將來源指定給倫敦的一個商店和兩個倉庫，以及柏林的一個倉庫。

![優先順序之前的來源順序](assets/inventory-priority-before.png){width="350" zoomable="yes"}

商戶偏好從較大的柏林倉儲，然後是倫敦倉儲，最後是倫敦的店面，排定出貨優先順序。 若要變更順序，會將專案拖放至所需的順序。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Stocks]**.

1. 在中開啟庫存 _編輯_ 模式。

1. 展開 _[!UICONTROL Sources]_標籤（如有需要）。

1. 使用 ![排序圖示](assets/icon-sort.png) 將原始程式碼拖放至優先順序，順序為上（第一個）到下（最後一個）。

   此訂單在出貨訂單時很重要。 SSA會根據來源順序建議出貨

1. 按一下 **[!UICONTROL Save & Continue]** 以儲存變更。

![優先順序之後的來源順序](assets/inventory-stock-priority-after.png){width="350" zoomable="yes"}
