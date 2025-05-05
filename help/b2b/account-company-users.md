---
title: 管理公司使用者帳戶
description: 瞭解公司使用者帳戶及其在相關聯公司帳戶中的運作方式。
exl-id: 36b55f61-e579-4eb8-8f67-0156221d378e
feature: B2B, Companies, User Account, Storefront
role: Admin, User
source-git-commit: 9c16d7a3909598328cc42bbcbf39fc14ae6a9eb9
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 0%

---

# 管理公司使用者帳戶

在店面，公司使用者由公司管理員指派，並可從&#x200B;_[!UICONTROL Company Users]_&#x200B;頁面看到。 這些個人通常是買家，擁有存取商店服務和資源的不同許可權等級。

公司管理員先設定[公司結構](account-company-structure.md)，然後視需要完成下列工作：

- 建立公司使用者並將使用者指派給團隊

- 定義角色和許可權，並將使用者指派給角色

公司使用者只能由公司管理員新增、編輯、停用或刪除。

- 移除使用者後，帳戶狀態會變更為&#x200B;*非使用中*，且客戶無法再登入公司。 管理員仍可存取與使用者相關聯的所有內容。 帳戶管理員可以從[!UICONTROL Company Users]頁面將帳戶狀態變更為&#x200B;*[!UICONTROL Active]*&#x200B;來還原存取權。

- 刪除使用者帳戶時，該帳戶和任何關聯內容都會從店面中刪除。 此動作無法還原。

## 新增公司使用者

1. 公司管理員從店面登入其帳戶。

1. 在左側面板中選擇&#x200B;**[!UICONTROL Company Users]**。

   ![公司使用者](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

1. 按一下&#x200B;**[!UICONTROL Add New User]**&#x200B;並執行下列動作：

   - 輸入新使用者的&#x200B;**[!UICONTROL Job Title]**。

   - 如果已定義角色和許可權，請選擇適當的&#x200B;**[!UICONTROL User Role]**。 否則，他們稍後可以返回以指派角色。

     ![新增使用者](./assets/company-structure-users-add.png){width="700" zoomable="yes"}

   - 在剩餘欄位中新增使用者資訊：
      - **[!UICONTROL First Name]**&#x200B;和&#x200B;**[!UICONTROL Last Name]**
      - **[!UICONTROL Email]**
      - **[!UICONTROL Work Phone Number]**

   預設情況下，帳戶的&#x200B;**[!UICONTROL Status]**&#x200B;為`Active`。

1. 完成後，按一下&#x200B;**[!UICONTROL Save]**。

1. 重複此程式，視需要建立任意數目的公司使用者。

   新使用者會與「公司管理員」一起顯示在「公司使用者」清單中。

為了節省第一筆訂單的時間，公司管理員可以提醒每個公司使用者將預設的公司帳單和送貨地址新增到他們的[通訊錄](../customers/account-dashboard-address-book.md)。

## 從[!UICONTROL Company structure]移除使用者

公司管理員可從[!UICONTROL Company Structure]移除使用者。

移除帳戶後，使用者帳戶狀態會變更為&#x200B;*非使用中*，且使用者無法再登入店面。
管理員可以從「公司使用者」頁面編輯使用者帳戶資訊，以重新啟用帳戶。

1. 公司管理員從店面登入其帳戶。

1. 在左側面板中選擇&#x200B;**[!UICONTROL Company Structure]**。

1. 選取公司結構中的公司使用者。

1. 按一下&#x200B;**[!UICONTROL Remove from Structure]**。

   ![刪除使用者](./assets/company-structure-delete-user.png){width="600" zoomable="yes"}

1. 提示確認時，按一下&#x200B;**[!UICONTROL Remove]**。

   在Admin中，公司使用者仍列在[客戶](../customers/customers-all.md)方格中，但狀態為`Inactive`。

## 檢視和管理公司使用者帳戶

公司管理員可以使用[!UICONTROL Company Users]頁面上的檢視篩選器來檢視和管理公司使用者帳戶。

![公司使用者](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

- 選取&#x200B;**[!UICONTROL Show Inactive Users]**，只檢視非作用中的使用者。
- 選取&#x200B;**[!UICONTROL Show Active Users]**&#x200B;以僅檢視作用中的使用者。
- 選取&#x200B;**[!UICONTROL Show All Users]**&#x200B;以檢視所有使用者。

公司管理員可以使用條列專案&#x200B;*[!UICONTROL Actions]*&#x200B;管理個別帳戶，以編輯帳戶資訊、管理帳戶狀態或刪除帳戶。

### 編輯公司使用者帳戶資訊

公司管理員可以更新使用者帳戶設定檔資訊，並變更帳戶狀態。

1. 在[!UICONTROL Company Users]頁面上，尋找要更新的使用者帳戶。 按一下&#x200B;**[!UICONTROL Edit]**。

1. 對使用者帳戶資訊進行任何必要的變更，包括變更帳戶狀態。

1. 按一下&#x200B;**[!UICONTROL Save]**&#x200B;套用變更。

>[!NOTE]
>
>如果您編輯公司使用者帳戶，且注意到設定檔遺失必要的帳戶資訊（例如職稱和工作電話號碼），即表示該帳戶是由Commerce網站管理員新增。 無法從店面編輯這些帳戶。 若要更新資訊或變更帳戶狀態，請連絡您的網站管理員。

### 停用或刪除使用中的帳戶

1. 在[!UICONTROL Company Users]頁面上，尋找要更新的使用者帳戶。 按一下&#x200B;**[!UICONTROL Manage]**。

   ![從「公司使用者」頁面管理使用者](./assets/company-users-manage-storefront.png){width="600" zoomable="yes"}

1. 出現提示時，請視需要停用或刪除使用者帳戶。

>[!IMPORTANT]
>
>刪除公司使用者帳戶會從系統移除該帳戶和所有關聯內容。 此動作無法還原。

## 公司使用者帳戶設定檔欄位說明

| 欄位 | 說明 |
|--------------------------------|---------------|
| [!UICONTROL Job Title] | 公司使用者的職稱。 |
| [!UICONTROL User Role] | 指派給公司使用者的[角色](account-company-roles-permissions.md)。 選項： `Default User` / （其他角色） |
| [!UICONTROL First Name] | 公司使用者的名字。 |
| [!UICONTROL Last Name] | 公司使用者的姓氏。 |
| [!UICONTROL Email] | 公司使用者的電子郵件地址。 |
| [!UICONTROL Work Phone Number] | 公司使用者的工作電話號碼。 |
| [!UICONTROL Status] | 公司使用者帳戶的狀態。 選項： `Active` / `Inactive` |

{style="table-layout:auto"}
