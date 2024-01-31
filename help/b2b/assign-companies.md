---
title: 管理公司階層
description: 瞭解如何透過建立公司階層來管理具有複雜營運模型的B2B組織
feature: B2B, Companies
role: Admin
hide: false
hidefromtoc: false
exl-id: a277ed95-7935-4d27-adb2-35116972732b
source-git-commit: 582f15c422e43af9acec6313c7b777b3126030f8
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 0%

---

# 管理 [!UICONTROL Company Hierarchy]

[!BADGE 1.5.0測試版]{type=Informative url="/help/b2b/release-notes.md" tooltip="僅供測試版計畫參與者使用"}

管理員可以建立 [!UICONTROL Company Hierarchy] 藉由將相關公司指派給指定的母公司，即位於組織頂端的公司。 如果 [!UICONTROL Company Type] 是 `Company`，該公司不是組織的一部分，並有資格成為母公司，或指派給現有的母公司。

在「管理員」中，您可以編輯公司，然後更新 [!UICONTROL Company Hierarchy] 用於指派或取消指派公司的設定。

![公司階層格線](./assets/company-detail-hierarchy-current-flag.png){width="700"}

>[!NOTE]
>
>有關詳細資訊 [!UICONTROL Company Hierarchy] 格線，請參閱 [公司階層](account-company-create.md#company-hierarchy) 欄位說明。

## 將公司指派至組織

1. 從 _管理員_ 側欄，瀏覽至 **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![公司格線](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. 在 [!UICONTROL Companies] 網格中，開啟公司詳細資訊頁面以建立指派。

   - 若要將其他公司指派至現有的母公司，請選取 **[!UICONTROL Edit]** 適用於母公司的動作。
   - 若要建立母公司，請選取 **[!UICONTROL Edit]** 公司要指定為母公司的動作。

     您無法從現有的母公司或子公司建立母公司。

1. 在公司詳細資訊頁面上，展開 **[!UICONTROL Company Hierarchy]**.

   ![公司階層格線](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}

   此網格會顯示現有的公司指派（如果有的話）。 母公司一律位於 [!UICONTROL Company Hierarchy] 格線。 此 `[!UICONTROL Current]` 旗標會指出正在編輯的公司。

1. 將公司新增至父級組織。

   - 從可用公司清單中選取 **[!UICONTROL Assign Companies]**.

   - **選取此頁面上的所有專案**，或選取一或多個特定公司條列專案。

   - 選取 **[!UICONTROL Assign Selected Companies]**.

   - 透過選取完成公司指派 **[!UICONTROL Assign]**.

     ![將公司指派至組織](./assets/assign-selected-companies-hierarchy.png){width="675" zoomable="yes"}

## 從母公司解除指派公司

1. 在 _管理員_ 側欄，瀏覽至 **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![公司格線](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. 在 [!UICONTROL Companies] 格線，選取以開啟父公司的公司詳細資訊頁面 **[!UICONTROL Edit]**.

1. 展開以檢視指派的公司清單 **[!UICONTROL Company Hierarchy]**.

1. 從 [!UICONTROL Company Hierarchy] 格線，使用取消指派公司 **[!UICONTROL Select]** 要選擇的動作控制項 **[!UICONTROL Unassign from parent]**.

   ![取消指定父級組織的公司](./assets/company-hierarchy-grid-unassign.png){width="700" zoomable="yes"}

1. 出現提示時，透過選取「 」，從階層中移除指派的公司 **[!UICONTROL Unassign]**.
