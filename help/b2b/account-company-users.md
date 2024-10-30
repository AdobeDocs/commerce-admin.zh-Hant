---
title: 管理公司使用者帳戶
description: 了解公司 用戶 帳戶及其在相關聯公司帳戶中的運作方式。
exl-id: 36b55f61-e579-4eb8-8f67-0156221d378e
feature: B2B, Companies, User Account, Storefront
role: Admin, User
source-git-commit: fec72b792cf3149c05803874795c45f9f4e28673
workflow-type: tm+mt
source-wordcount: '679'
ht-degree: 0%

---

# 管理公司用戶帳戶

在店面上，公司使用者由公司管理員分配，並且在頁面中 _[!UICONTROL Company Users]_可見。 這些人通常是購買者，在訪問商店服務和資源方面具有不同程度的權限。

公司管理員先設定[公司結構](account-company-structure.md)，然後視需要完成下列工作：

- 建立公司使用者並將使用者指派給團隊

- 定義角色和許可權，並將使用者指派給角色

公司使用者只能由公司管理員新增、編輯、停用或刪除。

- 移除使用者後，帳戶狀態會變更為&#x200B;*非使用中*，且客戶無法再登入公司。 管理員仍可存取與使用者相關聯的所有內容。 帳戶管理員可以從[!UICONTROL Company Users]頁面將帳戶狀態變更為&#x200B;*[!UICONTROL Active]*&#x200B;來還原存取權。

- When a user account is deleted, the account and any associated content is deleted from the storefront. This action cannot be reverted.

## Add company users

1. From the storefront, the company administrator signs in to their account.

1. **[!UICONTROL Company Users]**

   ![](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

1. 按下 **[!UICONTROL Add New User]** 並執行以下操作：

   - 輸入 **[!UICONTROL Job Title]** 新用戶。

   - 如果定義了角色和許可權，則選擇適當的 **[!UICONTROL User Role]** 角色。 否則，他們可以稍後返回以分配角色。

     ![](./assets/company-structure-users-add.png){width="700" zoomable="yes"}

   - Adds the user information in the remaining fields:
      - **[!UICONTROL First Name]**&#x200B;和&#x200B;**[!UICONTROL Last Name]**
      - **[!UICONTROL Email]**
      - **[!UICONTROL Phone Number]**

   預設情況下，帳戶的&#x200B;**[!UICONTROL Status]**&#x200B;為`Active`。

1. 完成後，按一下&#x200B;**[!UICONTROL Save]**。

1. 重複此程序，視需要建立任意數量的公司使用者。

   新使用者和公司管理員一起出現在「公司使用者」清單中。

為了節省第一筆訂單的時間，公司管理員可以提醒每個公司使用者將預設的公司帳單和送貨地址新增到他們的[通訊錄](../customers/account-dashboard-address-book.md)。

## 從[!UICONTROL Company structure]移除使用者

公司管理員可從[!UICONTROL Company Structure]移除使用者。

移除帳戶後，使用者帳戶狀態會變更為&#x200B;*非使用中*，且使用者無法再登入店面。
管理員可以從「公司使用者」頁面編輯使用者帳戶資訊，以重新啟用帳戶。

1. 公司管理員從店面登入其帳戶。

1. **[!UICONTROL Company Structure]**

1. Selects the company user in the company structure.

1. **[!UICONTROL Remove from Structure]**

   ![](./assets/company-structure-delete-user.png){width="600" zoomable="yes"}

1. **[!UICONTROL Remove]**

   [](../customers/customers-all.md)`Inactive`

## 檢視和管理公司用戶帳戶

[!UICONTROL Company Users]

![](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

- **[!UICONTROL Show Inactive Users]**
- **[!UICONTROL Show Active Users]**
- 選取&#x200B;**[!UICONTROL Show All Users]**&#x200B;以檢視所有使用者。

公司管理員可以使用條列項目 *[!UICONTROL Actions]* 管理單個帳戶，以编辑帳戶信息、管理帳戶狀態或刪除帳戶。

### 編輯公司用戶帳戶信息

公司管理員可以更新用戶帳戶設定檔信息并變更帳戶狀態。

1. 在 [!UICONTROL Company Users] 頁面上，找到要更新的用戶帳戶。 按兩下 **[!UICONTROL Edit]**。

1. 對使用者帳戶資訊進行任何必要的變更，包括變更帳戶狀態。

1. **[!UICONTROL Save]**

>[!NOTE]
>
>If you edit a company user account and notice that the profile is missing required account information such as job title and phone number, it indicates that the account was added by a Commerce site administrator. These accounts cannot be edited from the storefront. To update information or change the account status, contact your site administrator.

### Deactivate or delete an active account

1. [!UICONTROL Company Users]按兩下 **[!UICONTROL Manage]**。

   ![管理來自公司用戶的用戶 頁面](./assets/company-users-manage-storefront.png){width="600" zoomable="yes"}

1. 出現提示時，根據需要停用或刪除用戶帳戶。

>[!IMPORTANT]
>
>刪除公司用戶帳戶會從系統中刪除帳戶和所有相關內容。 此動作無法還原。

## Company user account profile field descriptions

| 欄位 | 說明 |
|--------------|---------------|
| [!UICONTROL Job Title] | 公司用戶的職稱。 |
| [!UICONTROL User Role] | 指派給 [公司角色](account-company-roles-permissions.md) 用戶。 選項： `Default User` / （其他角色） |
| [!UICONTROL First Name] | 公司用戶的名字。 |
| [!UICONTROL Last Name] | 公司使用者的姓氏。 |
| [!UICONTROL Email] | 公司使用者的電子郵件地址。 |
| [!UICONTROL Phone Number] | 公司使用者的電話號碼。 |
| [!UICONTROL Status] | 公司使用者帳戶的狀態。 選項： `Active` / `Inactive` |

{style="table-layout:auto"}
