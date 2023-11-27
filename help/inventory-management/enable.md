---
title: "啟用 [!DNL Inventory Management]"
description: 瞭解如何啟用 [!DNL Inventory Management] 全球商店或產品等級。
exl-id: 89bd2f8b-b9e4-4b9a-b729-f7bd71f764c9
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# 啟用 [!DNL Inventory Management]

若要管理您的產品詳細目錄，請啟用 [!DNL Inventory Management] 全球商店或產品等級。 當 _管理庫存_ 選項已啟用， [!DNL Inventory Management] 透過設定的庫存和來源，自動追蹤網站可用的產品數量。 每個功能和選項都可在啟用後開始追蹤和報告，無需額外設定。

您的企業會以銷售速度執行及庫存更新。 當客戶購物時，您會收到每個銷售管道和來源之可用庫存的確切、更新資訊。 當客戶將產品加入購物車並完成採購時，以及當您管理訂單、建立出貨及發放退款時，可用可銷售數量會更新每筆存貨。 新存貨或轉移存貨的到貨更新到您的來源，可立即用於線上銷售。 延交訂單最多可完成指定的臨界值，且無無限訂單或其他組態。 此外，您可以輸入並完成一或多個來源的部分或完整出貨與建議，讓您完全控制訂單履行與庫存量。

>[!NOTE]
>
>根據預設， [!DNL Inventory Management] 安裝或升級時啟用 [!DNL Commerce]. 根據您的業務需求，您可能需要啟用或停用追蹤的 [!DNL Inventory Management] 範圍 [!DNL Commerce].

此設定在單一來源與多重來源清查中的運作方式：

- 使用 [!DNL Inventory Management]，啟用 _[!UICONTROL Manage Stock]_.

- [!UICONTROL Manage Stock] 產品層級組態設定會覆寫商店組態。

- 若要使用「訂單管理系統」或協力廠商服務（例如ERP），請停用 [!UICONTROL Manage Stock].

- 如果產品層級設定使用系統預設值，則存放區設定會覆寫。

替換為 [!DNL Inventory Management] 已啟用，請參閱下列內容以設定所有設定：

- [設定全域選項](global-options.md)  — 影響整個目錄的設定，視為系統預設設定。

- [設定產品選項](product-options.md)  — 覆寫全域選項之特定產品的設定。

## 啟用或停用 [!DNL Inventory Management]

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Catalog]** 並選擇 **[!UICONTROL Inventory]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) _產品庫存選項_ 並設定：

   ![產品庫存選項](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - 若要管理詳細目錄並使用全部 [!DNL Commerce] 功能，設定 **[!UICONTROL Manage Stock]** 至 `Yes` （預設）。

   - 若要停用 [!DNL Inventory Management]，取消選取 **[!UICONTROL Use system value]** 核取方塊並設定 **[!UICONTROL Manage Stock]** 至 `No`.

1. 完成後，按一下 **[!UICONTROL Save Config]**.

## 管理商店的庫存

另請參閱 [設定全域選項](global-options.md).

## 管理產品的庫存

另請參閱 [設定產品選項](product-options.md).
