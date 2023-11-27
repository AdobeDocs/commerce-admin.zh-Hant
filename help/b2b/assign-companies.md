---
title: 管理公司階層
description: 建立並管理公司階層，以支援具有複雜營運模型的B2B組織。
feature: B2B, Companies
role: Admin
hide: false
hidefromtoc: false
exl-id: a277ed95-7935-4d27-adb2-35116972732b
source-git-commit: 10b01db562777ef2fcc224177d7a83c0a6fc90e7
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# 管理 [!UICONTROL Company Hierarchy]

[!BADGE 1.5.0測試版]{type=Informative url="/help/b2b/release-notes.md" tooltip="僅供測試版計畫參與者使用"}

管理員可以建立 [!UICONTROL Company Hierarchy] 藉由將相關公司指派給指定的母公司（位於組織階層頂端的公司）。

編輯尚未指派給現有公司的公司，以建立母公司 [!UICONTROL Company Hierarchy]，並指派相關公司。

![公司階層格線](./assets/company-detail-view.png){width="700"}

將公司指派至階層後， [!UICONTROL Company type] 中的欄 **公司** 格線將公司識別為 `Parent` 或  `Child` 公司。  如果 [!UICONTROL Company Type] 是 `Company`，該公司不屬於公司階層，並有資格成為母公司，或指派給現有的母公司。

>[!NOTE]
>
>有關詳細資訊 [!UICONTROL Company Hierarchy] 格線，請參閱 [公司階層](account-company-create.md#company-hierarchy) 欄位說明。

在「管理員」中，您可以編輯公司，然後使用 [!UICONTROL Company Hierarchy] 的區段 [!UICONTROL Company] 指派或取消指派公司的頁面。

## 將公司指派給母公司

1. 在 _管理員_ 側欄，瀏覽至 **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![公司格線](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. 在「公司」網格中，開啟公司詳細資訊頁面以建立指派。

   - 若要將其他公司指派至現有的母公司，請選取 **[!UICONTROL Edit]** 適用於母公司的動作。
   - 若要建立新的母公司，請選取 **[!UICONTROL Edit]** 針對指定為母公司的公司的動作。

     您無法從現有的母公司或子公司建立新的母公司。

   ![建立公司](./assets/company-update.png){width="700" zoomable="yes"}

1. 在公司詳細資訊頁面上，展開 **[!UICONTROL Company Hierarchy]** 下拉式清單，然後選取 **[!UICONTROL Assign Companies]**.

   ![建立公司](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

   展開此檢視時，您可以看到現有的公司指派（如果有的話）。 母公司一律顯示在 _[!UICONTROL Company Hierarchy]_格線帶有 `current company indicator` 顯示在正在編輯的公司明細中。

1. 可指派的公司會列在格線中。 選取要指派的公司，然後選取 **[!UICONTROL Assign Selected Companies]**.

1. 您可以 **選取此頁面上的所有專案** 或一個特定公司條列專案，然後按一下 **[!UICONTROL Assign Selected Companies]**.

   ![建立公司](./assets/assign-selected-companies.png){width="700" zoomable="yes"}

1. 出現提示時，選取「 」，完成公司指派 **[!UICONTROL Assign]**.

## 從母公司解除指派公司

1. 在 _管理員_ 側欄，瀏覽至 **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![公司格線](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. 在「公司」頁面上，選取「 」以開啟母公司的公司詳細資料頁面。 **[!UICONTROL Edit]** 動作。

   ![建立公司](./assets/company-update.png){width="700" zoomable="yes"}

1. 展開以檢視指派的公司清單 **[!UICONTROL Company Hierarchy]** 下拉式清單。

1. 在公司階層網格中，選取下列專案以取消指定公司 **[!UICONTROL Select]** 針對公司採取的動作，然後選擇 **[!UICONTROL Unassign from parent]**.

   ![建立公司](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

1. 出現提示時，透過選取「 」，從階層中移除指派的公司 **[!UICONTROL Unassign]**.
