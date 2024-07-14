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

# 管理[!UICONTROL Company Hierarchy]

[!BADGE 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="僅適用於Beta計畫參與者"}

管理員可以將相關公司指派給指定的母公司（組織頂端的公司），以建置[!UICONTROL Company Hierarchy]。 如果[!UICONTROL Company Type]是`Company`，則該公司不是組織的一部份，且有資格成為母公司，或指派給現有的母公司。

在「管理員」中，您可以編輯公司，然後更新[!UICONTROL Company Hierarchy]設定以指派或取消指派公司，藉此管理公司指派。

![公司階層網格](./assets/company-detail-hierarchy-current-flag.png){width="700"}

>[!NOTE]
>
>如需[!UICONTROL Company Hierarchy]格線的詳細資訊，請參閱[公司階層](account-company-create.md#company-hierarchy)欄位說明。

## 將公司指派至組織

1. 從&#x200B;_管理員_&#x200B;側邊欄，瀏覽至&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL Companies]**。

   ![公司格線](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. 在[!UICONTROL Companies]格線中，開啟公司詳細資料頁面以建立指派。

   - 若要將其他公司指派給現有的母公司，請選取該母公司的&#x200B;**[!UICONTROL Edit]**&#x200B;動作。
   - 若要建立母公司，請選取要指定為母公司的公司的&#x200B;**[!UICONTROL Edit]**&#x200B;動作。

     您無法從現有的母公司或子公司建立母公司。

1. 在公司詳細資訊頁面上，展開&#x200B;**[!UICONTROL Company Hierarchy]**。

   ![公司階層網格](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}

   此網格會顯示現有的公司指派（如果有的話）。 母公司一律位於[!UICONTROL Company Hierarchy]格線的頂端。 `[!UICONTROL Current]`旗標表示正在編輯的公司。

1. 將公司新增至父級組織。

   - 選取&#x200B;**[!UICONTROL Assign Companies]**，從可用公司清單中選擇。

   - **在此頁面上選取[全部]**，或選取一或多個特定的公司條列專案。

   - 選取&#x200B;**[!UICONTROL Assign Selected Companies]**。

   - 選取&#x200B;**[!UICONTROL Assign]**&#x200B;以完成公司指派。

     ![將公司指派給組織](./assets/assign-selected-companies-hierarchy.png){width="675" zoomable="yes"}

## 從母公司解除指派公司

1. 在&#x200B;_管理員_&#x200B;側邊欄上，瀏覽至&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL Companies]**。

   ![公司格線](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. 在[!UICONTROL Companies]格線中，選取&#x200B;**[!UICONTROL Edit]**&#x200B;以開啟父公司的公司詳細資料頁面。

1. 展開&#x200B;**[!UICONTROL Company Hierarchy]**&#x200B;以檢視指派的公司清單。

1. 從[!UICONTROL Company Hierarchy]格線中，使用&#x200B;**[!UICONTROL Select]**&#x200B;動作控制項取消指派公司以選擇&#x200B;**[!UICONTROL Unassign from parent]**。

   ![從父級組織取消指派公司](./assets/company-hierarchy-grid-unassign.png){width="700" zoomable="yes"}

1. 出現提示時，選取&#x200B;**[!UICONTROL Unassign]**，從階層中移除指派的公司。
