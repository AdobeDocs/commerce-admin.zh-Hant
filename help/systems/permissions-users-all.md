---
title: 管理管理員使用者帳戶
description: 瞭解如何建立管理員使用者帳戶及指派角色，以授予許可權給管理員功能。
exl-id: 65cca7a8-3d44-4c8c-a758-c0de03d53e11
role: Admin
feature: Admin Workspace, Roles/Permissions, User Account, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1025'
ht-degree: 0%

---

# 管理管理員使用者帳戶

第一次安裝您的存放區時，會使用可為您提供完整管理存取權的登入憑證建立預設的Admin帳戶。 作為最佳實務，您應該建立另一個具有完整管理員存取權的使用者帳戶。 如此一來，您就可以將一個帳戶用於日常管理活動，並將另一個帳戶保留為「超級管理員」帳戶。 如果您忘記了一般的認證，或是認證變得無法使用，這會很有幫助。

如果您的團隊中有其他人或服務提供者需要存取權，您可以為每個建立單獨的使用者帳戶，並根據他們的業務需要指派受限制的存取權。 若要限制使用者可在「管理員」中存取的網站或商店，您必須先 [建立角色](permissions-user-roles.md) 範圍有限，且僅選取必要的資源。 然後，您可以將角色指派給特定使用者帳戶。 管理員使用者若被指派受限角色，只能看見和變更與該角色相關聯之網站或商店的資料，但無法變更任何全域設定或資料。

>[!NOTE]
>
>擁有Adobe ID且想要簡化登入Adobe Commerce和Adobe業務產品的Adobe Commerce商家可整合Commerce驗證與Adobe IMS驗證工作流程。 為您的Commerce商店啟用此整合後，每個管理員使用者都必須使用其Adobe認證（而不是其Commerce認證）才能登入。 另請參閱 [AdobeIdentity Management服務(IMS)整合概述](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

對於暫時的使用者或角色，您也可以設定使用者帳戶的到期日。

<!--  update this to a better info-graphic ![User types for your Admin](./assets/merchant-admin-users.png) -->

## 建立使用者

1. 在 _管理員_ 側欄，前往 **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. 在右上角，按一下 **[!UICONTROL Add New User]**.

   若要編輯現有使用者，請按一下網格中的使用者名稱。 您可以修改 _[!UICONTROL User Info]_和_[!UICONTROL User Role]_ 區段。

1. 在 _[!UICONTROL Account Information]_區段，請執行下列動作：

   ![使用者帳戶資訊](./assets/permissions-user-new.png){width="600" zoomable="yes"}

   - 輸入 **[!UICONTROL User Name]** 帳戶。

     使用者名稱應該容易記憶。 不區分大小寫。 例如，如果使用者名稱為 `John`，他們也可以以下列身分登入 `john`.

   - 完成下列資訊：

      - **[!UICONTROL First Name]**
      - **[!UICONTROL Last Name]**
      - **[!UICONTROL Email address]**

     每個使用者帳戶都必須有唯一的電子郵件地址。

   - 輸入 **[!UICONTROL Password]** 用於帳戶。

     >[!NOTE]
     >
     >管理員密碼的長度必須是7個或7個以上的字元，且包含字母和數字。 如需其他密碼選項，請參閱 [設定管理員安全性](security-admin.md).

   - 的 **[!UICONTROL Password Confirmation]**，請重新輸入密碼以確保輸入正確。

   - 如果您的商店有多種語言，請設定 **[!UICONTROL Interface Locale]** 至管理員介面使用的語言。

1. 設定 **[!UICONTROL This Account is]** 至 `Active`.

1. 按一下行事曆圖示以設定 **[!UICONTROL Expiration Date]** 使用者帳戶的。

   若使用者或角色為暫時性，則定義到期日會很有幫助。 到期日後，使用者帳戶狀態會變更為 `Inactive` 如有需要，可更新和。

1. 在 _[!UICONTROL Current User Identity Verification]_，輸入您的使用者帳戶密碼。

>[!IMPORTANT]
>
>使用 _[!UICONTROL Account Information]_區段完成後，您可以儲存使用者。 新使用者會顯示在_[!UICONTROL Users]_ 但使用者名稱必須等到指派角色後才能登入。

## 指派使用者角色

1. 在左側面板中，按一下 **[!UICONTROL User Role]**.

   網格會列出所有現有的使用者角色。 若為新商店， _[!UICONTROL Administrators]_是唯一可用的角色。

   ![管理員 — 新增使用者角色](./assets/permissions-user-roles.png){width="600" zoomable="yes"}

1. 在 _[!UICONTROL Assigned]_欄中，選取使用者角色。

   您可以 [檢視現有或定義其他使用者角色](permissions-user-roles.md). 定義角色後，您必須編輯使用者帳戶以指派新角色。

## 驗證或重設2FA提供者

1. 開啟Admin使用者帳戶。

1. 在左側面板中，按一下 **[!UICONTROL 2FA]**.

   ![管理員 — 新增使用者角色](./assets/permissions-user-2fa.png){width="600" zoomable="yes"}

1. 驗證可用的2FA解決方案 _管理員_ 使用者並建議每個使用者在登入前安裝他們想要使用的解決方案。

   只需由一個2FA解決方案驗證，即可登入 _管理員_.

1. 如果使用者需要重新安裝2FA解決方案，您可以重設目前的2FA設定。

   使用者必須重複設定程式，才能再次登入。 例如，使用者可能有一部新的智慧型手機，需要重新安裝Google Authenticator。 若要清除使用者目前的2FA設定，請按一下 **[!UICONTROL Reset (Provider)]** 清除的每個解決方案。 出現提示時，按一下 **[!UICONTROL OK]** 以確認。

   使用者會收到含有連結的電子郵件 [設定2FA](security-two-factor-authentication.md). 此連結只能使用一次。 如果使用者嘗試登入多次，則會在每次嘗試後傳送新連結。

1. 按一下 **[!UICONTROL Save User]**.

1. 出現提示時，輸入您的密碼以確認您的身分，然後再次按一下 **[!UICONTROL Save User]**.

   此 _[!UICONTROL Users]_格線會開啟並列出所有使用者。

## 刪除管理員使用者

1. 在 _管理員_ 側欄，前往 **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. 使用格線上方的篩選器來找出使用者帳戶，然後按一下使用者名稱。

1. 出現提示時，請輸入您的密碼以確認您的身分。

1. 在右上角，按一下 **[!UICONTROL Delete User]**.

1. 若要確認動作，請按一下 **[!UICONTROL OK]**.

## 忘記密碼並重設電子郵件

管理員電子郵件範本設定可決定在使用者忘記並重設密碼時傳送的電子郵件。 此設定會指定顯示為訊息寄件者的商店連絡人，以及密碼復原連結保持有效的時間。

**_若要設定管理員電子郵件範本：_**

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Setting]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Advanced]** 並選擇 **[!UICONTROL Admin]**.

1. 展開 ![擴充切換器](../assets/icon-display-expand.png) 此 **[!UICONTROL Admin User Emails]** 區段。

   ![進階設定 — 管理員電子郵件範本設定](../configuration-reference/advanced/assets/admin-admin-user-emails.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Forgot Password Email Template]** 至在管理員使用者忘記密碼時傳送的範本。

1. 設定 **[!UICONTROL Forgot and Reset Email Sender]** 與顯示為訊息寄件者的商店連絡人。

1. 設定 **[!UICONTROL User Notification Template]** 預設為管理員通知的電子郵件範本。

1. 完成後，按一下 **[!UICONTROL Save Config]**.

## 鎖定的使用者

為了您企業的安全，使用者帳戶在六次嘗試失敗後預設為鎖定 [登入](../getting-started/admin-signin.md) 傳送給管理員。 目前鎖定的任何使用者帳戶都會顯示在「鎖定的使用者」網格中。 擁有完整管理員許可權的任何其他使用者都可以解除鎖定帳戶。

其他密碼安全措施可在 [進階管理員](../configuration-reference/advanced/admin.md#security) 設定。 另請參閱 [管理安全性](security-admin.md).

![登入畫面警示 — 帳戶暫時停用](./assets/admin-login-locked-out-message.png){width="300"}

**_若要解除鎖定Admin帳戶：_**

1. 在 _管理員_ 側欄，前往 **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL Locked Users]**.

1. 在網格中，選取鎖定帳戶的核取方塊。

   ![許可權 — 鎖定的使用者帳戶](./assets/permissions-locked-users-grid.png){width="600" zoomable="yes"}

1. 在左上角，設定 **[!UICONTROL Actions]** 至 `Unlock`.

1. 按一下 **[!UICONTROL Submit]** 以解除鎖定帳戶。
