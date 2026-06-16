---
title: 快速訂購
description: 瞭解快速訂購功能並為您的客戶啟用。
exl-id: 7007e1b4-a64f-46fe-a235-3ca9f64e77e4
feature: B2B, Orders
TQID: https://experienceleague.adobe.com/iwH1JStasz7KM-ECeWAvP-x4niVm-QFg4-GMw8r3SoI
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 438
ht-degree: 0%

---

# 快速訂購

_快速訂購_&#x200B;功能可讓知道要訂購產品的產品名稱或SKU的客戶將訂購程式減少為幾次點按。 您可以手動輸入具有多個SKU的訂單，或將其匯入「快速訂購」表單。 快速訂購可供登入其帳戶的客戶及來賓使用。 啟用時，_快速訂購_&#x200B;連結會出現在頁面頂端的客戶名稱旁。

![快速訂購連結](./assets/quick-order-link.png){width="700" zoomable="yes"}

## 為您的商店啟用快速訂單

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板的&#x200B;_[!UICONTROL General]_&#x200B;區段中，選擇&#x200B;**[!UICONTROL B2B Features]**。

1. 將&#x200B;**[!UICONTROL Enable Quick Order]**&#x200B;設為`Yes`。

   ![啟用快速訂購](./assets/quick-orders-config.png){width="600" zoomable="yes"}

1. 按一下&#x200B;**[!UICONTROL Save Config]**。

1. 出現提示時，請按一下[快取管理](../systems/cache-management.md)並重新整理任何無效的快取。

## 快速訂購工作流程

客戶可使用下列其中一種方法來指定快速訂購的產品。

### 方法1：輸入個別產品

1. 客戶按一下&#x200B;**[!UICONTROL Quick Order]**&#x200B;連結。

1. 依SKU或產品名稱選取產品：

   若要透過SKU **下快速訂單**，客戶會執行下列動作：

   - 進入&#x200B;**[!UICONTROL SKU]**。

   - 按一下&#x200B;**[!UICONTROL Add to List]**。

     SKU會顯示在輸入行中，其產品詳細資料如下。

     ![快速訂購詳細資料](./assets/quick-order-product-detail.png){width="600" zoomable="yes"}

   若要依產品名稱&#x200B;**快速下單**，客戶會執行下列動作：

   - 輸入&#x200B;**[!UICONTROL Product Name]**&#x200B;的前幾個字元。

     >[!NOTE]
     >
     >請勿使用&#x200B;_Enter_&#x200B;金鑰來選擇產品名稱。

   - 當可能的相符專案清單出現時，客戶按一下要訂購的產品。

     ![按一下以選擇產品名稱](./assets/quick-order-product-name.png){width="700" zoomable="yes"}

1. 進入&#x200B;**[!UICONTROL Qty]**。

1. 使用下一個輸入行，視需要重複此程式。

1. 按一下&#x200B;**[!UICONTROL Add to Cart]**。

### 方法2：輸入多個產品

1. 在&#x200B;**[!UICONTROL Enter Multiple SKUs]**&#x200B;方塊中，客戶執行下列任一項作業：

   - 每行輸入一個SKU

   - 在同一行中輸入所有SKU （以逗號分隔，不含空格）。

     ![輸入多個SKU](./assets/quick-order-skus.png){width="600" zoomable="yes"}

1. 若要將產品加入清單，請按一下&#x200B;**[!UICONTROL Add to List]**。

1. 輸入清單中每個專案要排序的&#x200B;**[!UICONTROL Qty]**。

   ![快速訂購清單](./assets/quick-order-skus-detail.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >如果產品有必要的選項，系統會提示客戶選擇選項。 他們可以等到到達購物車再新增產品選項。

   ![選擇選項](./assets/quick-order-skus-product-options.png){width="600" zoomable="yes"}

### 方法3：上傳產品清單

1. 在&#x200B;_[!UICONTROL Add from File]_&#x200B;區段中，按一下&#x200B;**[!UICONTROL Download Sample]**&#x200B;以下載訂單範本。

   ![從檔案新增](./assets/quick-order-skus-add-from-file.png){width="600" zoomable="yes"}

1. 開啟已下載的檔案。

1. 使用範本新增產品SKU以上傳給快速訂購清單。

1. 完成後，按一下&#x200B;**[!UICONTROL Save]**。

   要上載的![SKU](./assets/quick-order-skus-add-from-file-sample.png){width="400" zoomable="yes"}

1. 若要上傳檔案，請按一下&#x200B;**[!UICONTROL Choose]**&#x200B;並從其系統選取檔案。

   專案會新增至「快速訂購」清單。

1. 準備就緒後，按一下&#x200B;**[!UICONTROL Add to Cart]**。

客戶建立快速訂單後，就可以照常進行結帳。

![快速訂購](./assets/quick-order-add-to-cart.png){width="700" zoomable="yes"}
