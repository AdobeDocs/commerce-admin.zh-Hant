---
title: 排定存貨存貨來源的優先順序
description: 瞭解如何依優先順序從上到下排列來源，這可用於決定出貨及存貨扣減。
exl-id: 16db3ee3-ce99-40dd-b1a3-fcb145b1298f
feature: Inventory, Configuration
TQID: https://experienceleague.adobe.com/oPgeuN3-Il-yf3zpG2r4PNAmNbf-4gmz5-GFngM3-Ng
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 210
ht-degree: 0%

---

# 排定存貨來源的優先順序

將[來源](sources-manage.md)新增至[庫存](stocks-manage.md)後，請以由上到下的優先順序排列這些來源，以履行訂單。 Source選擇演演算法(SSA)在決定出貨與存貨扣除額時，會使用此訂單提供演演算法「優先順序」。

編輯產品存貨時，存貨的來源優先順序不會影響指定的來源。

在此範例中，UK Stock已將來源指定給倫敦的一個商店和兩個倉庫，以及柏林的一個倉庫。

優先順序設定前![Source訂單](assets/inventory-priority-before.png){width="350" zoomable="yes"}

商戶偏好從較大的柏林倉儲，然後是倫敦倉儲，最後是倫敦的店面，排定出貨優先順序。 若要變更順序，會將專案拖放至所需的順序。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Stocks]**。

1. 以&#x200B;_編輯_&#x200B;模式開啟庫存。

1. 如有需要，請展開&#x200B;_[!UICONTROL Sources]_標籤。

1. 使用![排序圖示](assets/icon-sort.png)將來源拖放至優先順序(從上（第一個）到下（最後一個）。

   此訂單在出貨訂單時很重要。 SSA會根據來源順序建議出貨

1. 按一下&#x200B;**[!UICONTROL Save & Continue]**&#x200B;以儲存變更。

優先順序設定後的![Source訂單](assets/inventory-stock-priority-after.png){width="350" zoomable="yes"}
