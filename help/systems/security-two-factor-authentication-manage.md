---
title: 管理雙因素驗證
description: 瞭解如何為管理員使用者管理雙因素驗證及重設驗證者。
exl-id: 68256214-2d50-4c42-846f-306ffc305f25
role: Admin
feature: Configuration, Security, User Account
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 0%

---

# 管理雙因素驗證

無法登入的使用者 _管理員_ 使用雙因素驗證(2FA)可以嘗試同步或疑難排解問題。 您也可以重設與帳戶關聯的驗證者。 重設時，使用者必須再次登入並重新設定必要的驗證者。

如果您無法使用2FA登入，請考慮以下事項：

- 部分行動應用程式包含同步選項。 此選項會重新連線應用程式和伺服器，並同步裝置和伺服器上的時間設定。
- 撤銷裝置或重設驗證器可協助使用者連線。
- 清除Adobe Commerce或Magento Open Source安裝的Web Cache和Cookie也有所幫助。 Google等驗證者會使用產生的Cookie來儲存存取權和持續時間。 清除您特定瀏覽器和商店網域的Cookie。
- 封鎖Cookie會使某些驗證者無法正常運作，例如 [!DNL Google Authenticator]，完成驗證程式。 新增規則至瀏覽器，允許為Adobe Commerce安裝提供Cookie。

若要從命令列重設驗證者，以及更進階的疑難排解資訊，請參閱 [雙因素驗證](https://developer.adobe.com/commerce/testing/functional-testing-framework/two-factor-authentication/) 在開發人員檔案中。

**_若要重設使用者帳戶的驗證者：_**

>[!NOTE]
>
>若要為其他使用者重設2FA提供者，您必須是 _管理員_ 替換為 `All` 許可權，或具有 `Custom` 您角色的許可權，具有 [!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL Two Factor Auth] 和 [!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL All Users] 已選取。 若要深入瞭解，請參閱 [使用者角色](permissions-user-roles.md).

1. 在 _管理員_ 側欄，前往 **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. 選取使用者，並在編輯模式下開啟帳戶。

1. 向下捲動至 _[!UICONTROL Current User Identity Verification]_並輸入您的密碼。

1. 在左側面板中，按一下 **[!UICONTROL 2FA]**.

1. 在 _[!UICONTROL Configuration reset]_區段，按一下&#x200B;**[!UICONTROL Reset]**和&#x200B;**[!UICONTROL OK]**以確認。

   ![使用者帳戶 — 啟用2FA](./assets/admin-2fa-config-reset-providers.png){width="600" zoomable="yes"}

   如果使用者想要將必要的2FA方法還原至其帳戶，他們必須從 _登入_ 頁面。

1. 完成後，按一下 **[!UICONTROL Save User]**.
