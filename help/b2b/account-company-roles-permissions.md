---
title: 公司角色和許可權
description: 瞭解公司管理員可套用至公司使用者的角色和許可權，允許各種層級存取訂單資訊和資源。
exl-id: 9fe20d6a-2c9c-4618-a395-805d64dcf0de
feature: B2B, Companies, Roles/Permissions
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 0%

---

# 公司角色和許可權

公司使用者的角色設定為具有存取銷售資訊和資源的各種許可權層級。 依預設，公司管理員是具有完整許可權的&#x200B;_超級使用者_。 如果使用者沒有存取頁面的許可權，就會顯示[拒絕存取](../content-design/pages.md#access-denied)頁面。

具有預設角色的![角色和許可權頁面](./assets/company-roles-permissions.png){width="700" zoomable="yes"}

系統有一個預先定義的預設使用者角色，您可以以&#x200B;_形式使用_&#x200B;或進行修改以符合您的需求。 您可以視需要建立儘可能多的角色，以符合您的公司結構和組織責任，例如：

- **預設使用者** — 預設使用者擁有與銷售和報價相關的活動的完整存取權，以及公司設定檔和信用資訊的僅檢視存取權。

- **資深購買者** — 資深購買者可能擁有所有「銷售」和「報價」資源的存取權，以及公司設定檔、使用者和團隊、付款資訊和公司信用額的僅限檢視許可權。

- **助理購買者** — 助理購買者可能有權使用&#x200B;_使用報價結帳_&#x200B;下訂單，並可在公司設定檔中檢視訂單、報價和資訊。

## 管理角色和許可權

1. 公司管理員登入其商店帳戶。

1. 在左側面板中選擇&#x200B;**[!UICONTROL Roles and Permissions]**。

1. 完成下列任一作業。

### 建立角色

1. 按一下&#x200B;**[!UICONTROL Add New Role]**。

   ![新增角色](./assets/company-roles-permissions-add-storefront.png){width="600" zoomable="yes"}

1. 輸入描述性&#x200B;**[!UICONTROL Role Name]**。

1. 在&#x200B;_[!UICONTROL Role Permissions]_底下，執行下列其中一項作業：

   - 選取被指派角色的使用者有權存取之每個資源或活動的核取方塊。

   - 選取&#x200B;**[!UICONTROL All]**&#x200B;核取方塊，並清除指派給角色的使用者無權存取之每個資源或活動的核取方塊。

1. 按一下&#x200B;**[!UICONTROL Save Role]**。

1. 重複這些步驟，視需要建立多個角色。

### 修改角色

1. 對於要修改的角色，公司管理員按一下&#x200B;_[!UICONTROL Actions]_欄中的&#x200B;**[!UICONTROL Edit]**。

1. 對名稱和許可權設定進行必要的變更。

1. 完成後，按一下&#x200B;**[!UICONTROL Save Role]**。

### 複製角色

1. 對於要複製的角色，公司管理員按一下&#x200B;_[!UICONTROL Actions]_欄中的&#x200B;**[!UICONTROL Duplicate]**。

1. 對名稱和許可權設定進行必要的變更。

1. 完成後，按一下&#x200B;**[!UICONTROL Save Role]**。

### 刪除角色

1. 公司管理員在角色清單中找到要刪除的角色。

   只能刪除未指派使用者的角色。

1. 在&#x200B;_[!UICONTROL Actions]_欄中按一下&#x200B;**[!UICONTROL Delete]**。

1. 提示確認時，按一下&#x200B;**[!UICONTROL OK]**。

## 動作

| 動作 | 說明 |
|-----------| ----------- |
| [!UICONTROL Duplicate] | 建立所選角色的復本。 重複角色的名稱已新增`- Duplicated`到結尾。 |
| [!UICONTROL Edit] | 變更名稱和/或許可權集。 |
| [!UICONTROL Delete] | 刪除角色。 只能刪除未指派使用者的角色。 |

{style="table-layout:auto"}

## 角色許可權

- 全部
   - 銷售
      - 允許結帳（下單）
         - 使用分期付款方式
      - 檢視訂單
         - 檢視下屬使用者的訂單
- 引號
   - 檢視
      - 請求，編輯，刪除
      - 使用引號結帳
      - 檢視從屬使用者的報價單
- 訂單核准
   - 檢視我的採購單
      - 下屬的檢視
      - 檢視所有公司
   - 自動核准在此角色中建立的採購單
   - 核准採購單，而不需要其他核准
   - 檢視核准規則
      - 建立、編輯和刪除
- 公司設定檔
   - 帳戶資訊（檢視）
      - 編輯
   - 合法地址
      - 編輯
   - 連絡人（檢視）
   - 付款資訊（檢視）
   - 送貨資訊（檢視）
- 公司使用者管理
   - 檢視角色和許可權
      - 管理角色和許可權
   - 檢視使用者和團隊
      - 管理使用者和團隊
- 公司評價
   - 檢視

## 指派角色給公司使用者

定義所需的角色後，公司管理員會為每個公司使用者指派角色。

1. 以公司管理員的身分登入其公司帳戶。

1. 在左側面板中選擇&#x200B;**[!UICONTROL Company Users]**。

   ![公司使用者](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

1. 在清單中尋找使用者並按一下&#x200B;**[!UICONTROL Edit]**。

1. 為使用者選擇適當的&#x200B;**[!UICONTROL User Role]**。

   ![編輯使用者 — 選擇使用者角色](./assets/company-user-assign-role.png){width="700" zoomable="yes"}

1. 按一下&#x200B;**[!UICONTROL Save]**。
