---
title: 設定傳回
description: 瞭解如何啟用商店退貨，並設定支援的送貨方法。
exl-id: a1b508fc-7e42-4d37-bf7e-dea17a40d39b
feature: Returns, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 0%

---

# 設定傳回

{{ee-feature}}

啟用後，客戶可以從店面提交RMA請求。 只有在訂單中有可退貨的專案時，才能產生RMA。 傳回個別專案的請求由管理 _啟用RMA_ 屬性。 依預設，組態設定會套用至產品(_[!UICONTROL Use Config Settings]_已選取)。 如果_[!UICONTROL Enable RMA]_ 設為 `No`，產品不會出現在可回訪的專案清單中。 如果您變更 _啟用RMA_ 設定，則同時適用於新訂單和現有訂單。

## 啟用商店的RMA

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Sales]** 並選擇 **[!UICONTROL Sales]** 底下。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL RMA Settings]** 區段。

   ![RMA設定](../configuration-reference/sales/assets/sales-rma-settings.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Enable RMA on Storefront]** 至 `Yes`.

   此設定決定客戶是否可以從店面建立和檢視RMA請求。 RMA可同時套用至新訂單與現有訂單。

1. 設定 **[!UICONTROL Enable RMA on Product Level]** 至 `Yes`.

   此設定決定 _啟用RMA_ 店面中個別產品的屬性：

   - 時間 [!UICONTROL Enable RMA on Product Level] 設為 `Yes`，店面的客戶可退還所有個別產品。 它包含兩者 _[!UICONTROL Enable RMA]_= `Yes` 和_[!UICONTROL Enable RMA]_ = `No` 產品屬性值。
   - 時間 [!UICONTROL Enable RMA on Product Level] 設為 `No`，店面的客戶僅能傳回帶有 _[!UICONTROL Enable RMA]_= `Yes` 產品屬性值。

1. 設定 **[!UICONTROL Use Store Address]** 變更為下列其中一個值：

   - `Yes`  — 將傳回的產品傳送至商店地址。
   - `No`  — 輸入產品退貨的替代地址。

   ![含備用地址的RMA設定](../configuration-reference/sales/assets/sales-rma-settings.png){width="600" zoomable="yes"}

1. 按一下 **[!UICONTROL Save Config]**.

## 設定退貨的送貨方法

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Sales]** 並選擇 **[!UICONTROL Delivery Methods]**.

1. 展開您要用於退貨服務的承運商的區段，例如 **[!UICONTROL UPS]**.

   ![啟用電信業者的RMA服務](./assets/rma-delivery-method.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Enabled for RMA]** 至 `Yes`.

1. 按一下 **[!UICONTROL Save Config]**.

## 變更產品層級允許的RMA

如果您啟用商店的RMA，且您的目錄包含某些不允許退貨的產品，則您可以在產品層級修改設定。

1. 在編輯模式中開啟產品。

1. 向下捲動並展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Autosettings]** 區段。

1. 清除 **[!UICONTROL Use Config Setting]** 核取方塊（如有需要）。

1. 切換 **[!UICONTROL Enable RMA]** 將設為 `No`.

   ![停用產品的RMA](./assets/product-advanced-autosettings-enable-rma.png){width="600" zoomable="yes"}

1. 按一下 **[!UICONTROL Save]**.
