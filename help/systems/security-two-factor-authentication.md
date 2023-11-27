---
title: 雙因素驗證(2FA)
description: 瞭解雙因素驗證支援，以確保您的存放區和資料的安全。
exl-id: d9eb3dd6-4a7b-411a-ac08-0441803cd59a
role: Admin
feature: Configuration, Security, User Account
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '704'
ht-degree: 0%

---

# 雙因素驗證(2FA)

商務 _管理員_ 用於您的Adobe Commerce或Magento Open Source安裝，可讓您存取商店、訂單和客戶資料。 為避免未經授權存取您的資料，所有嘗試登入 _管理員_ 必須完成驗證程式以驗證其身分。

>[!NOTE]
>
>此雙因素驗證(2FA)的實作適用於 _管理員_ 僅限，且不適用於客戶帳戶。 保護您的Commerce帳戶的雙因素驗證具有單獨的設定。 若要進一步瞭解，請前往 [保護您的Commerce帳戶](../getting-started/commerce-account-secure.md).

雙因素驗證被廣泛使用，且通常會在相同應用程式上產生不同網站的存取代碼。 這樣可確保只有您才能登入使用者帳戶。 如果您遺失密碼或機器人猜到密碼，雙因素驗證會增加一層保護。 例如，您可以使用Google Authenticator產生商店、Commerce帳戶和Google帳戶管理員的代碼。

![安全性設定iphone - 2FA](./assets/google-authenticator-iphone.png){width="300"}

Adobe Commerce支援來自多個提供者的2FA方法。 有些要求安裝可產生一次性密碼(OTP)的應用程式，讓使用者在登入時輸入以驗證其身分。 通用次要因數(U2F)裝置類似金鑰組，並產生唯一金鑰以驗證身分。 其他裝置在插入USB連線埠時驗證身分。 身為商店管理員，您可以要求一或多個可用的2FA方法來驗證使用者身分。 您的2FA設定會套用至與Adobe Commerce安裝相關聯的所有網站和商店。

使用者第一次登入 _管理員_，他們必須設定 [2FA](../configuration-reference/security/2fa.md) 所需的方法，並使用相關聯的應用程式或裝置驗證其身分。 進行此初始設定後，使用者每次登入時都必須使用其中一個已設定方法進行驗證。 每個使用者的2FA資訊都會記錄在 _管理員_ 帳戶，可以是 [重設](security-two-factor-authentication-manage.md) 如有需要。 若要進一步瞭解登入程式，請前往 [_管理員_ 登入](../getting-started/admin-signin.md).

>[!NOTE]
>
>已啟用Adobe Identity Management Services (IMS)驗證的商店會停用原生Adobe Commerce和Magento Open Source 2FA。 使用Adobe憑證登入其Commerce執行個體的管理員使用者不需要重新驗證許多管理員工作。 當管理員使用者登入目前的工作階段時，驗證會由Adobe IMS處理。 另請參閱 [AdobeIdentity Management服務(IMS)整合概述](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

您可以觀看此節目 [影片示範](https://video.tv.adobe.com/v/339104?quality=12&learn=on) 有關「管理員」中雙因素驗證的概觀。

## 設定您所需的2FA提供者

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Security]** 並選擇 **[!UICONTROL 2FA]**.

1. 在 _[!UICONTROL General]_區段，選取每個&#x200B;**[!UICONTROL Provider to use]**.

   | 提供者 | 函式 |
   |--- |--- |
   | [!UICONTROL Google Authenticator] | 在應用程式中產生一次性密碼，以供使用者驗證。 |
   | [!UICONTROL Duo Security] | 提供簡訊和推播通知。 |
   | [!UICONTROL Authy] | 產生取決於時間的六位數代碼，並提供SMS或語音呼叫2FA保護或代號。 |
   | [!UICONTROL U2F Devices (Yubikey and others)] | 使用實體裝置進行驗證，例如 [[!DNL YubiKey]](https://www.yubico.com/). |

   若要選取多個方法，請按住Ctrl鍵(PC)或Command鍵(Mac)，然後按一下每個專案。

1. 完成每個必要2FA方法的設定。

   ![安全性設定 — 2FA](../configuration-reference/security/assets/2fa-general.png){width="600" zoomable="yes"}

1. 完成後，按一下 **[!UICONTROL Save Config]**.

   使用者第一次登入 _管理員_，則須設定每個必要的2FA方法。 進行此初始設定後，每次登入時都必須使用其中一個已設定方法進行驗證。

## 2FA提供者設定

完成您所需的每個2FA方法的設定。

### Google

若要變更一次性密碼(OTP)在登入期間可用的時間，請清除 **[!UICONTROL Use system value]** 核取方塊。 然後，輸入您想要的 **[!UICONTROL OTP Window]** 才有效。

![安全性設定 — Google](../configuration-reference/security/assets/2fa-google.png){width="600" zoomable="yes"}

### [!DNL Duo Security]

從您的Duo Security帳戶輸入下列認證：

- 整合索引鍵
- 秘密金鑰
- API主機名稱

![安全性組態 — Duo](../configuration-reference/security/assets/2fa-duo-security.png){width="600" zoomable="yes"}

### [!DNL Authy]

1. 輸入您電腦的 [!DNL Authy] 帳戶。

1. 若要變更驗證期間顯示的預設訊息，請清除 **[!UICONTROL Use system value]** 核取方塊。 然後，輸入 **[!UICONTROL OneTouch Message]** 您希望顯示的專案。

   ![安全性設定 — Authy](../configuration-reference/security/assets/2fa-authy.png){width="600" zoomable="yes"}

### U2F裝置([!DNL Yubikey] 和其他)

在驗證程式期間，預設會使用存放區網域。 若要使用自訂網域來解決驗證難題，請清除 **[!UICONTROL Use system value]** 核取方塊。 然後，輸入 **[!UICONTROL WebAPi Challenge Domain]**.

![安全性設定 — U2F裝置](../configuration-reference/security/assets/2fa-u2f-key.png){width="600" zoomable="yes"}
