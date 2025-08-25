---
title: 管理公司階層
description: 建立並管理公司階層，以支援具有複雜營運模型的B2B組織。
feature: B2B, Companies
role: Admin
hide: false
hidefromtoc: false
exl-id: a277ed95-7935-4d27-adb2-35116972732b
source-git-commit: 1fc1e07f20e2c22ac430f384e9e2b278edae405c
workflow-type: tm+mt
source-wordcount: '827'
ht-degree: 0%

---

# 管理公司階層

[!UICONTROL Company Hierarchy]功能可讓您在單一母公司結構下組織多個相關公司。 這非常適合擁有子公司、特許經營權、多個地點或複雜組織結構的企業，這些企業需要集中管理，同時維護個別公司的身分。

## 使用案例

* **集中管理** — 將設定和組態套用至單一母公司的多家公司
* **維護結構** — 以邏輯階層組織公司，以反映您的企業組織
* **簡化作業** — 管理整個組織的報價單、採購單、付款方式及送貨設定
* **保留Autonomy** — 個別公司保留其身分，同時受益於共用組態

## 先決條件

在建立公司階層之前，請確定：

* 您的Commerce安裝已啟用B2B功能
* 您具有管理公司的管理員存取權
* 父公司和子公司已建立為個別公司
* 您瞭解套用父設定將會覆寫現有的子公司設定

## 運作方式

管理員可以將相關公司指派給指定的母公司（位於組織階層頂端的公司），藉此建立公司階層。

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

   * 若要將其他公司指派給現有的母公司，請選取該母公司的&#x200B;**[!UICONTROL Edit]**&#x200B;動作。
   * 若要建立母公司，請為指定為母公司的公司選取&#x200B;**[!UICONTROL Edit]**&#x200B;動作。

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

   * 在公司要移除的[!UICONTROL Action]欄中，**[!UICONTROL Select]** > **[!UICONTROL Unassign from parent]**。

     ![從組織移除公司](./assets/company-hierarchy-grid-unassign.png){width="640" zoomable="yes"}

   * 出現提示時，選取&#x200B;**[!UICONTROL Unassign]**，從階層中移除指派的公司。

## 管理組織的公司設定

更新組織的[進階設定](account-company-create.md#advanced-settings)組態。 您可以：

* 將父組態設定套用至所有子公司
* 將相同的設定套用至組織中選取的公司

您可以套用下列任何設定：

* **報價管理** — 啟用或停用公司要求和管理報價的功能
* **採購單** — 控制公司是否可以建立和管理採購單
* **付款方式設定** — 定義公司可用的付款方式
* **付款方式設定** — 設定特定的付款方式引數和限制
* **送貨方法可用性** — 設定公司可以使用哪些送貨方法
* **送貨方法組態** — 定義送貨方法設定與限制

在更新過程中，初始設定值會預設為目前為父公司設定的值。 您必須選取至少一個設定的變更核取方塊，才能將設定套用至選取的公司。 您也可以在套用變更之前，更新每個設定的預設值。

>[!WARNING]
>
>套用母公司設定會取代現有的子公司設定，包括信用限制、付款方法、送貨設定和自訂限制。 套用設定後，您仍然可以透過編輯公司條列專案來管理和自訂個別母公司與子公司的進階設定。

### 最佳實務

將母公司設定套用至子公司時，請考量下列最佳實務：

* 在套用上層設定之前，先檢閱現有的下層公司設定
* 先在單一子公司上變更測試設定
* 向可能受影響的公司管理員傳達變更

### 套用父組態設定至子公司

1. 在&#x200B;_管理員_&#x200B;側邊欄上，瀏覽至&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL Companies]**。

1. 從[!UICONTROL Companies]格線中，選取&#x200B;**[!UICONTROL Edit]**&#x200B;欄中的&#x200B;**[!UICONTROL Action]**&#x200B;以編輯父公司。

1. 在上層公司詳細資訊頁面上，展開&#x200B;**[!UICONTROL Company Hierarchy]**&#x200B;區段以檢視組織中包含的公司。

1. 選取要設定的公司。

   ![從公司階層中選取公司](assets/company-hierarchy-select-companies.png){width="675" zoomable="yes"}

1. 從格線上方的&#x200B;**[!UICONTROL Actions]**&#x200B;控制項選取&#x200B;**[!UICONTROL Change company settings]**。

   ![變更公司階層的公司設定](assets/company-hierarchy-change-company-settings-action.png){width="675" zoomable="yes"}

1. 變更設定組態。

   * 在[!UICONTROL Change company settings]頁面上，尋找要修改的組態設定。

   * 選取&#x200B;**[!UICONTROL Change]**&#x200B;核取方塊以啟用設定。

   * 如有需要，請更新值。

     ![變更多個公司的公司設定](assets/company-hierarchy-change-settings-config.png){width="575" zoomable="yes"}

1. 更新組態之後，請選取&#x200B;**[!UICONTROL Apply Changes]**。

1. 出現提示時，請選取&#x200B;**[!UICONTROL Change settings]**&#x200B;以更新所選公司的組態。

>[!MORELIKETHIS]
>
>* [建立公司帳戶](account-company-create.md) — 瞭解如何在建立階層之前建立個別公司
>* [公司角色和許可權](account-company-roles-permissions.md) — 瞭解公司結構內的使用者存取權
>* [公司信用管理](credit-company.md) — 設定公司的信用額度與付款條件
>* [管理公司](manage-companies.md) — 公司管理功能概觀
>* [啟用B2B功能](enable-basic-features.md) — 啟用並設定B2B功能
