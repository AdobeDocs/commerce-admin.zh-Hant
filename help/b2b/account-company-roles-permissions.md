---
title: 公司角色和許可權
description: 瞭解公司管理員可套用至公司使用者的角色和許可權，允許各種層級存取訂單資訊和資源。
exl-id: 9fe20d6a-2c9c-4618-a395-805d64dcf0de
feature: B2B, Companies, Roles/Permissions
role: Admin
source-git-commit: bad59798a1a6d97826dc421fe8614ef511e067bd
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 0%

---

# 公司角色和許可權

公司使用者的角色設定為具有存取銷售資訊和資源的各種許可權層級。 依預設，公司管理員是具有完整許可權的&#x200B;_超級使用者_。 [如果用戶沒有權限來存取頁面，則會顯示「拒絕存取」](../content-design/pages.md#access-denied)頁面。

具有預設角色的![角色和許可權頁面](./assets/company-roles-permissions.png){width="700" zoomable="yes"}

系統有一個預先定義的預設使用者角色，您可以以&#x200B;_形式使用_&#x200B;或進行修改以符合您的需求。 您可以視需要建立儘可能多的角色，以符合您的公司結構和組織責任，例如：

- **預設使用者** — 預設使用者擁有與銷售和報價相關的活動的完整存取權，以及公司設定檔和信用資訊的僅檢視存取權。

- **資深購買者** — 資深購買者可能擁有所有「銷售」和「報價」資源的存取權，以及公司設定檔、使用者和團隊、付款資訊和公司信用額的僅限檢視許可權。

- **助理購買者** — 助理購買者可能有權使用&#x200B;_使用報價結帳_&#x200B;下訂單，並可在公司設定檔中檢視訂單、報價和資訊。

## 管理角色和許可權

1. 公司管理員登錄其商店帳戶。

1. 在左側面板中，選擇 **[!UICONTROL Roles and Permissions]**。

1. 完成以下任一項任務。

### 建立角色

1. 點擊 **[!UICONTROL Add New Role]**.

   ![新增新角色](./assets/company-roles-permissions-add-storefront.png){width="600" zoomable="yes"}

1. 輸入描述性 **[!UICONTROL Role Name]**。

1. 在 下 _[!UICONTROL Role Permissions]_&#x200B;執行下列操作之一..

   - 選中分配了角色權限有權訪問的每個資源或活動的複選框。

   - 選中 **[!UICONTROL All]** 該複選框並清除分配給角色的用戶無權限訪問的每個資源或活動的複選框。

1. 按一下&#x200B;**[!UICONTROL Save Role]**。

1. 重複這些步驟，視需要建立多個角色。

### 修改角色

1. 對於要修改的角色，公司管理員按一下&#x200B;_[!UICONTROL Actions]_&#x200B;欄中的&#x200B;**[!UICONTROL Edit]**。

1. 對名稱和權限設置進行必要的更改。

1. 完成後，按一下&#x200B;**[!UICONTROL Save Role]**。

### 複製角色

1. 對於要複製的角色，公司管理員按一下&#x200B;_[!UICONTROL Actions]_&#x200B;欄中的&#x200B;**[!UICONTROL Duplicate]**。

1. 對名稱和許可權設定進行必要的變更。

1. 完成後，按一下&#x200B;**[!UICONTROL Save Role]**。

### 刪除角色

1. 公司管理員在角色清單中找到要刪除的角色。

   只能刪除沒有指派使用者的角色。

1. 在&#x200B;_[!UICONTROL Actions]_&#x200B;欄中按一下&#x200B;**[!UICONTROL Delete]**。

1. 提示確認時，按一下&#x200B;**[!UICONTROL OK]**。

## 動作

| 行動 | 說明 |
|-----------| ----------- |
| [!UICONTROL Duplicate] | 建立所選角色的複本。 角色 `- Duplicated` 已添加到末尾的重複的名稱。 |
| [!UICONTROL Edit] | 變更名稱和/或許可權集。 |
| [!UICONTROL Delete] | 刪除角色。 只能刪除沒有指派使用者的角色。 |

{style="table-layout:auto"}

## 角色許可權

公司管理員可以選取[!UICONTROL Edit action]，然後在&#x200B;**角色許可權**&#x200B;清單中選取或移除許可權，來更新角色的許可權設定。

![角色和許可權清單](./assets/role-permissions-list.png){width="700" zoomable="yes"}

## 將角色指派給公司用戶

定義所需的角色后，公司管理員為每個公司用戶分配一個角色。

1. 以公司管理員的身分登入其公司帳戶。

1. 在左側面板中，選擇 **[!UICONTROL Company Users]**。

   ![公司使用者](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

1. 在清單中尋找使用者並按一下&#x200B;**[!UICONTROL Edit]**。

1. 為使用者選擇適當的&#x200B;**[!UICONTROL User Role]**。

   ![編輯使用者 — 選擇使用者角色](./assets/company-user-assign-role.png){width="700" zoomable="yes"}

1. 點擊 **[!UICONTROL Save]**.
