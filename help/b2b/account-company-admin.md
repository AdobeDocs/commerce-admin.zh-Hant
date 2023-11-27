---
title: 指派公司管理員
description: 瞭解如何將公司使用者帳戶指派為公司帳戶的指定公司管理員。
exl-id: 26f3a449-6f3a-4078-816d-6248ac6d1e46
feature: B2B, Companies
role: Admin, User
source-git-commit: fb075822e318073053cdf8cdd5cd9bb3a6343904
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# 指派公司管理員

公司管理員最初是在公司帳戶首次建立時指派的，且只能由管理員的商店管理員修改。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. 在清單中尋找公司並按一下 **[!UICONTROL Edit]**.

   ![公司](./assets/companies-grid.png){width="700" zoomable="yes"}

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Company Admin]** 區段。

   ![公司管理員](./assets/company-create-company-admin.png){width="700" zoomable="yes"}

1. 輸入 **[!UICONTROL Job Title]** ，然後按一下 **[!UICONTROL Proceed]** 以繼續。

   此動作會清除表單及必要的 _[!UICONTROL First Name]_和_[!UICONTROL Last Name]_ 欄位會醒目提示。

1. 輸入 **[!UICONTROL Email]** 新公司管理員的地址。

   如果系統在資料庫中找不到電子郵件地址，系統會提示您確認是否要取代公司管理員。

   - 如果新公司管理員的使用者帳戶不存在，則系統會建立 `Company Admin` 型別。

   - 如果使用者帳戶存在於系統中，則會將其移至公司結構中的公司管理員位置。

1. 輸入 **[!UICONTROL First Name]** 和 **[!UICONTROL Last Name]**，以及適用於新公司管理員的任何其他資訊。

1. 完成後，按一下 **[!UICONTROL Save]**.

   前公司管理員的個別帳戶會保留在系統中，作為公司結構中的作用中個別使用者帳戶，並指派給預設使用者角色。

   系統會將變更的電子郵件通知傳送給新的和以前的公司管理員。
