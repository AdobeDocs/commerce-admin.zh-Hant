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

啟用後，客戶可以從店面提交RMA請求。 只有在訂單中有可退貨的專案時，才能產生RMA。 傳回個別專案的要求是由每個產品記錄中的&#x200B;_啟用RMA_&#x200B;屬性所管理。 依照預設，組態設定會套用至產品（已選取&#x200B;_[!UICONTROL Use Config Settings]_）。 如果_[!UICONTROL Enable RMA]_&#x200B;設為`No`，產品不會出現在可傳回的專案清單中。 若您變更&#x200B;_啟用RMA_&#x200B;設定，該設定會同時套用至新訂單與現有訂單。

## 啟用商店的RMA

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Sales]**&#x200B;並在下方選擇&#x200B;**[!UICONTROL Sales]**。

1. 展開&#x200B;**[!UICONTROL RMA Settings]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![RMA設定](../configuration-reference/sales/assets/sales-rma-settings.png){width="600" zoomable="yes"}

1. 將&#x200B;**[!UICONTROL Enable RMA on Storefront]**&#x200B;設為`Yes`。

   此設定決定客戶是否可以從店面建立和檢視RMA請求。 RMA可同時套用至新訂單與現有訂單。

1. 將&#x200B;**[!UICONTROL Enable RMA on Product Level]**&#x200B;設為`Yes`。

   此設定決定店面個別產品的&#x200B;_啟用RMA_&#x200B;屬性的行為：

   - 當[!UICONTROL Enable RMA on Product Level]設定為`Yes`時，店面上的客戶可以傳回所有個別產品。 它包含&#x200B;_[!UICONTROL Enable RMA]_= `Yes`和_[!UICONTROL Enable RMA]_ = `No`產品屬性值。
   - 當[!UICONTROL Enable RMA on Product Level]設定為`No`時，店面的客戶只能傳回具有&#x200B;_[!UICONTROL Enable RMA]_= `Yes`產品屬性值的產品。

1. 將&#x200B;**[!UICONTROL Use Store Address]**&#x200B;設定為下列其中一個值：

   - `Yes` — 將傳回的產品傳送至商店地址。
   - `No` — 輸入產品退貨的替代地址。

   ![使用備用地址的RMA設定](../configuration-reference/sales/assets/sales-rma-settings.png){width="600" zoomable="yes"}

1. 按一下&#x200B;**[!UICONTROL Save Config]**。

## 設定退貨的送貨方法

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Sales]**&#x200B;並選擇&#x200B;**[!UICONTROL Delivery Methods]**。

1. 展開您要用於退貨服務的電信業者區段，例如&#x200B;**[!UICONTROL UPS]**。

   ![啟用電信業者的RMA服務](./assets/rma-delivery-method.png){width="600" zoomable="yes"}

1. 將&#x200B;**[!UICONTROL Enabled for RMA]**&#x200B;設為`Yes`。

1. 按一下&#x200B;**[!UICONTROL Save Config]**。

## 變更產品層級允許的RMA

如果您啟用商店的RMA，且您的目錄包含某些不允許退貨的產品，則您可以在產品層級修改設定。

1. 在編輯模式中開啟產品。

1. 向下捲動並展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Autosettings]**&#x200B;區段。

1. 視需要清除&#x200B;**[!UICONTROL Use Config Setting]**&#x200B;核取方塊。

1. 將&#x200B;**[!UICONTROL Enable RMA]**&#x200B;設定切換為`No`。

   ![停用產品的RMA](./assets/product-advanced-autosettings-enable-rma.png){width="600" zoomable="yes"}

1. 按一下&#x200B;**[!UICONTROL Save]**。
