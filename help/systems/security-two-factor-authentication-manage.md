---
title: 管理雙因素驗證
description: 瞭解如何為管理員使用者管理雙因素驗證及重設驗證者。
exl-id: 68256214-2d50-4c42-846f-306ffc305f25
role: Admin
feature: Configuration, Security, User Account
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---

# 管理雙因素驗證

無法以雙因素驗證(2FA)登入&#x200B;_Admin_&#x200B;的使用者可以嘗試同步處理或疑難排解問題。 您也可以重設與帳戶關聯的驗證者。 重設時，使用者必須再次登入並重新設定必要的驗證者。

如果您無法使用2FA登入，請考慮以下事項：

- 部分行動應用程式包含同步選項。 此選項會重新連線應用程式和伺服器，並同步裝置和伺服器上的時間設定。
- 撤銷裝置或重設驗證器可協助使用者連線。
- 清除Adobe Commerce或Magento Open Source安裝的Web Cache和Cookie也有所幫助。 Google等驗證者會使用產生的Cookie來儲存存取權和持續時間。 清除您特定瀏覽器和商店網域的Cookie。
- 封鎖Cookie會使某些驗證者（例如[!DNL Google Authenticator]）無法完成驗證程式。 新增規則至瀏覽器，允許為Adobe Commerce安裝提供Cookie。

若要從命令列重設驗證者，以及更進階的疑難排解資訊，請參閱開發人員檔案中的[雙因素驗證](https://developer.adobe.com/commerce/testing/functional-testing-framework/two-factor-authentication/)。

**_若要重設使用者帳戶的驗證者：_**

>[!NOTE]
>
>若要重設其他使用者的2FA提供者，您必須是具有`All`許可權的&#x200B;_系統管理員_，或針對已選取[!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL Two Factor Auth]和[!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL All Users]的角色擁有`Custom`許可權。 若要深入瞭解，請參閱[使用者角色](permissions-user-roles.md)。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**。

1. 選取使用者，並在編輯模式下開啟帳戶。

1. 向下捲動至&#x200B;_[!UICONTROL Current User Identity Verification]_區段並輸入您的密碼。

1. 在左側面板中，按一下&#x200B;**[!UICONTROL 2FA]**。

1. 在&#x200B;_[!UICONTROL Configuration reset]_區段中，按一下&#x200B;**[!UICONTROL Reset]**與&#x200B;**[!UICONTROL OK]**以確認。

   ![使用者帳戶 — 啟用2FA](./assets/admin-2fa-config-reset-providers.png){width="600" zoomable="yes"}

   如果使用者想要將必要的2FA方法還原到他們的帳戶，他們必須從&#x200B;_登入_&#x200B;頁面重新設定每個方法。

1. 完成時，按一下&#x200B;**[!UICONTROL Save User]**。
