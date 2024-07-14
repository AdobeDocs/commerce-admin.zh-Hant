---
title: "啟用 [!DNL Inventory Management]"
description: 瞭解如何在全域商店或產品層級啟用 [!DNL Inventory Management] 。
exl-id: 89bd2f8b-b9e4-4b9a-b729-f7bd71f764c9
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# 啟用[!DNL Inventory Management]

若要管理您的產品詳細目錄，請在全域商店或產品層級啟用[!DNL Inventory Management]。 啟用&#x200B;_管理庫存_&#x200B;選項時，[!DNL Inventory Management]會透過設定的庫存和來源自動追蹤網站可用的產品數量。 每個功能和選項都可在啟用後開始追蹤和報告，無需額外設定。

您的企業會以銷售速度執行及庫存更新。 當客戶購物時，您會收到每個銷售管道和來源之可用庫存的確切、更新資訊。 當客戶將產品加入購物車並完成採購時，以及當您管理訂單、建立出貨及發放退款時，可用可銷售數量會更新每筆存貨。 新存貨或轉移存貨的到貨更新到您的來源，可立即用於線上銷售。 延交訂單最多可完成指定的臨界值，且無無限訂單或其他組態。 此外，您可以輸入並完成一或多個來源的部分或完整出貨與建議，讓您完全控制訂單履行與庫存量。

>[!NOTE]
>
>依預設，[!DNL Inventory Management]在安裝或升級[!DNL Commerce]時啟用。 根據您的業務需求，您可能想要在[!DNL Commerce]內啟用或停用追蹤的[!DNL Inventory Management]。

此設定在單一來源與多重來源清查中的運作方式：

- 若要使用[!DNL Inventory Management]，請啟用&#x200B;_[!UICONTROL Manage Stock]_。

- 產品層級組態中的[!UICONTROL Manage Stock]設定會覆寫商店組態。

- 若要使用Order Management或第三方服務（例如ERP），請停用[!UICONTROL Manage Stock]。

- 如果產品層級設定使用系統預設值，則存放區設定會覆寫。

啟用[!DNL Inventory Management]後，請參閱下列專案以設定所有設定：

- [設定全域選項](global-options.md) — 影響整個目錄的設定，視為系統預設設定。

- [設定產品選項](product-options.md) — 覆寫全域選項的特定產品設定。

## 啟用或停用[!DNL Inventory Management]

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Catalog]**&#x200B;並選擇&#x200B;**[!UICONTROL Inventory]**。

1. 展開![擴充選擇器](../assets/icon-display-expand.png) _產品庫存選項_&#x200B;並設定：

   ![產品庫存選項](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - 若要管理詳細目錄並使用所有[!DNL Commerce]功能，請將&#x200B;**[!UICONTROL Manage Stock]**&#x200B;設為`Yes` （預設）。

   - 若要停用[!DNL Inventory Management]，請取消選取&#x200B;**[!UICONTROL Use system value]**&#x200B;核取方塊並將&#x200B;**[!UICONTROL Manage Stock]**&#x200B;設為`No`。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

## 管理商店的庫存

請參閱[設定全域選項](global-options.md)。

## 管理產品的庫存

請參閱[設定產品選項](product-options.md)。
