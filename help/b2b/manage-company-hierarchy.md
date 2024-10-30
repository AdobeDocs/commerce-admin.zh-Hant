---
title: 管理公司階層
description: 建立並管理公司階層，以支援具有複雜營運模型的B2B組織。
feature: B2B, Companies
role: Admin
hide: false
hidefromtoc: false
exl-id: a277ed95-7935-4d27-adb2-35116972732b
source-git-commit: 6b06f52eb4ee8ca136a1c60fd6dc04a9ac96bbfa
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 0%

---

# 管理[!UICONTROL Company Hierarchy]

管理員可以將相關公司指派給指定的母公司（位於組織階層頂端的公司），藉此建立[!UICONTROL Company Hierarchy]。

從Admin，編輯個別公司(`[!UICONTROL Company Type] = Company`)並在[!UICONTROL Company Hierarchy]設定中指派相關公司，以建立父公司。

![公司階層網格](./assets/company-hierarchy-grid.png){width="700"}


>[!NOTE]
>
>如需[!UICONTROL Company Hierarchy]格線的詳細資訊，請參閱[公司階層](account-company-create.md#company-hierarchy)欄位說明。

編輯母公司並使用&#x200B;*[!UICONTROL Company Hierarchy]*&#x200B;格線新增或移除公司，以管理公司指派。 使用&#x200B;*[!UICONTROL Actions]*&#x200B;控制項來管理組織中公司的[進階設定組態](#change-company-settings)。

## 將公司指派給母公司

1. 在&#x200B;_管理員_&#x200B;側邊欄上，瀏覽至&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL Companies]**。

   ![公司格線](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. 從[!UICONTROL Companies]格線中，開啟公司詳細資料頁面以建立指派。

   - 若要將其他公司指派給現有的母公司，請選取該母公司的&#x200B;**[!UICONTROL Edit]**&#x200B;動作。
   - 若要建立母公司，請為指定為母公司的公司選取&#x200B;**[!UICONTROL Edit]**&#x200B;動作。

     您無法從現有的母公司或子公司建立新的母公司。

1. 在公司詳細資訊頁面上，展開&#x200B;**[!UICONTROL Company Hierarchy]**，然後選取&#x200B;**[!UICONTROL Assign Companies]**。

   ![建立母公司](./assets/company-hierarchy-grid.png){width="675" zoomable="yes"}

1. 從可用公司清單中，選擇要指派的公司，然後選取&#x200B;**[!UICONTROL Assign Selected Companies]**。

   ![選取要指派的公司](./assets/company-hierarchy-select-companies-assign.png){width="675" zoomable="yes"}

1. 出現提示時，選取&#x200B;**[!UICONTROL Assign]**&#x200B;以完成公司指派。

## 從母公司解除指派公司

1. 在「公司」頁面上，選取&#x200B;**[!UICONTROL Edit]**&#x200B;動作，以開啟母公司之公司詳細資料頁面。

   ![母公司詳細資料頁面](./assets/company-update.png){width="700" zoomable="yes"}

1. 展開&#x200B;**[!UICONTROL Company Hierarchy]**&#x200B;以檢視指派的公司清單。

1. 從組織移除公司。

   - 在公司要移除的[!UICONTROL Action]欄中，**[!UICONTROL Select]** > **[!UICONTROL Unassign from parent]**。

     ![從組織移除公司](./assets/company-hierarchy-grid-unassign.png){width="640" zoomable="yes"}

   - 出現提示時，選取&#x200B;**[!UICONTROL Unassign]**，從階層中移除指派的公司。

## 管理組織的公司設定

更新組織的[進階設定](account-company-create.md#advanced-settings)設定，以將父組態套用至所有子公司，或將相同的設定套用至組織中選取的公司。

在更新程式期間，初始設定值會預設為目前為父公司設定的值。 您必須至少變更一個設定，才能更新所選公司的組態。

**變更多家公司的進階設定組態**

1. 在&#x200B;_管理員_&#x200B;側邊欄上，瀏覽至&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL Companies]**。

1. 從[!UICONTROL Companies]格線中，選取&#x200B;**[!UICONTROL Action]**&#x200B;欄中的&#x200B;**[!UICONTROL Edit]**&#x200B;以編輯父公司。

1. 在上層公司詳細資訊頁面上，展開&#x200B;**[!UICONTROL Company Hierarchy]**&#x200B;區段以檢視組織中包含的公司。

1. 選取要設定的公司。

   ![從公司階層中選取公司](assets/company-hierarchy-select-companies.png){width="675" zoomable="yes"}

1. 從格線上方的&#x200B;**[!UICONTROL Actions]**&#x200B;控制項選取&#x200B;**[!UICONTROL Change company settings]**。

   ![變更公司階層的公司設定](assets/company-hierarchy-change-company-settings-action.png){width="675" zoomable="yes"}

1. 變更設定組態。

   - 在[!UICONTROL Change company settings]頁面上，尋找要修改的組態設定。

   - 選取&#x200B;**[!UICONTROL Change]**&#x200B;核取方塊以啟用設定。

   - 視需要更新值。

     ![變更多個公司的公司設定](assets/company-hierarchy-change-settings-config.png){width="575" zoomable="yes"}

1. 更新組態之後，請選取&#x200B;**[!UICONTROL Apply Changes]**。

1. 出現提示時，請選取&#x200B;**[!UICONTROL Change settings]**&#x200B;以更新所選公司的組態。

>[!TIP]
>
>編輯公司條列專案，管理單一公司的進階設定組態。
