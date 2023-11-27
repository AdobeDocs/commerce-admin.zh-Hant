---
title: 您的管理員使用者帳戶
description: 瞭解您的管理員帳戶以及如何使用雙因素驗證來登入管理員。
exl-id: ad576533-5914-49d1-8e73-3f59c55543a5
feature: Admin Workspace, User Account
source-git-commit: fff3464c9da50927bbe9773a17b0f6858360d788
workflow-type: tm+mt
source-wordcount: '964'
ht-degree: 0%

---

# 您的管理員帳戶

主要Admin帳戶最初是在安裝期間設定，可能包含初始預留位置資訊或範例資料資訊。 此帳戶的指定擁有者可以個人化使用者名稱和密碼，並隨時更新名字、姓氏和電子郵件地址。 此帳戶，a _超級使用者_ 依預設，會使用所有許可權建立業務所需的管理員使用者帳戶。

- 另請參閱 [建立使用者](../systems/permissions-users-all.md#create-a-user) 以取得新增或編輯使用者的相關資訊。

- 另請參閱 [許可權](../systems/permissions.md) 和 [使用者角色](../systems/permissions-user-roles.md) 有關管理員和使用者角色的資訊。

{{ims-admin-note}}

## 管理員登入

此 [!DNL Commerce] _管理員_ 受到多層安全措施的保護，以防止未經授權存取您的商店、訂單和客戶資料。 第一次登入 _管理員_，您必須輸入使用者名稱和密碼，並設定 [雙因素驗證](../systems/security-two-factor-authentication.md) (2FA)。

根據您的存放區設定，可能有 [驗證碼](../systems/security-google-recaptcha.md) 需要解決的難題，例如輸入一系列鍵盤字元、解決謎題，或按一下具有共同主題的一系列影像。 這些測試旨在將您識別為人類，而不是自動化機器人。

如需額外的安全性，您可以決定 _管理員_ 每個使用者都有 [許可權](../systems/permissions.md) 以存取，同時也可以限制 [登入嘗試](../configuration-reference/advanced/admin.md). 根據預設，帳戶在六次嘗試後會鎖定，使用者必須等候幾分鐘再重試。 [鎖定的帳戶](../systems/permissions-users-all.md#locked-users) 您也可以從重設 _管理員_.

>[!NOTE]
>
>第一次登入 _管理員_，系統會提示您輸入 _允許管理員使用資料收集_. 另請參閱 [使用資料集合](admin.md#usage-data-collection) 以取得詳細資訊。

![管理員登入](./assets/admin-login.png){width="400"}

### 步驟1：設定雙因素驗證

登入之前 _管理員_ 您必須設定好雙因素驗證解決方案，才能在商店中使用。 若要深入瞭解每個解決方案所使用的驗證程式，請參閱 [使用雙因素驗證](../systems/security-two-factor-authentication-use.md). 根據預設， [!DNL Commerce] 支援 [Google驗證器][1].

詢問您的 [!DNL Commerce] 商店支援哪些2FA解決方案的系統管理員。 接著，根據提供者的指示，完成您偏好的2FA解決方案設定。

### 步驟2：登入管理員

1. 輸入 _管理員_ 期間指定的URL [!DNL Commerce] 安裝。

   預設 _管理員_ URL類似於 `https://www.yourdomain.com/your-custom-admin-domain`.

   >[!NOTE]
   >
   >雖然本檔案使用 `admin` 作為大多數範例中的基礎URL，建議您選擇唯一且難以猜測的URL [自訂URL](../stores-purchase/store-urls.md) 針對 _管理員_ ，屬於您的商店。

   您可以為頁面新增書籤或在案頭上儲存捷徑以方便存取。

1. 輸入您的 _管理員_ **[!UICONTROL Username]** 和 **[!UICONTROL Password]**.

1. （選擇性）如果您的商店已啟用驗證碼，請依照熒幕上的指示解決挑戰。

   若要深入瞭解，請參閱 [驗證碼](../systems/security-captcha.md) 和 [reCAPTCHA](../systems/security-google-recaptcha.md).

1. 按一下 **[!UICONTROL Sign in]**.

   如果您是第一次登入 _管理員_ 您應該會從帳戶收到一封電子郵件，其中包含設定指示的連結。

### 步驟3：完成2FA設定

以下範例說明如何配對 _管理員_ 帳戶與Google Authenticator。

1. 當QR碼出現時，請使用下列其中一種方法來擷取碼，並將Google Authenticator與您的 _管理員_ 帳戶。

   ![設定Google驗證器](./assets/admin-login-google-auth-setup.png){width="400"}

   - 使用智慧型手機擷取QR碼

     在智慧型手機上啟動Google Authenticator。 點選 _加號_ (+)於應用程式右上角。 然後在畫面底部，點選 **[!UICONTROL Scan Barcode]** 並拍照QR碼。

   - 從瀏覽器擷取QR碼

     如果瀏覽器以擴充功能形式安裝了Google Authenticator，請按一下 **驗證者** 圖示並擷取頁面。

   - 手動輸入QR碼

     複製QR碼下方的文字字串。 使用您的智慧型手機或瀏覽器啟動Google Authenticator，然後按一下加號(+)。 然後，選擇 **[!UICONTROL Manual Entry]**. 在 **[!UICONTROL Account]**，輸入與您的網站相關聯的電子郵件地址 _管理員_ 將二維碼字串貼到 **[!UICONTROL Key]** 欄位。

1. 若要登入 _管理員_ 使用雙因素驗證，請將Google Authenticator產生的六位數代碼輸入到 **[!UICONTROL Authenticator code]** 欄位，然後按一下 **[!UICONTROL Confirm]**.

   ![輸入驗證程式代碼](./assets/admin-login-2fa-google.png){width="400"}

## 重設密碼

不允許重複使用指派給帳戶的最後四個密碼。

1. 輸入 **[!UICONTROL Email Address]** 與 _管理員_ 帳戶。

   ![忘記密碼](./assets/admin-sign-in-forgot-password.png){width="400"}

1. 按一下 **[!UICONTROL Retrieve Password]**.

   如果帳戶與電子郵件地址相關聯，則會傳送電子郵件以重設您的密碼。

   >[!NOTE]
   >
   >一個 _管理員_ 密碼長度必須是7個或7個以上的字元，且包含字母和數字。 另請參閱 [設定 _管理員_ 安全性](../systems/security-admin.md) 以取得有關密碼選項的資訊。

## 登出管理員

1. 在右上角，按一下 _帳戶_ (![帳戶](../assets/icon-admin-user.png))圖示。

1. 按一下 **[!UICONTROL Sign Out]**.

   ![登出](./assets/admin-sign-out.png){width="700" zoomable="yes"}

此 _[!UICONTROL Sign In]_頁面會顯示您已登出的訊息。 登出_&#x200B;管理員&#x200B;_無論何時離開電腦。

## 編輯帳戶資訊

1. 按一下 _帳戶_ (![帳戶圖示](../assets/icon-admin-user.png))圖示。

1. 按一下 **[!UICONTROL Account Setting]**.

   ![帳戶資訊](./assets/admin-account-information.png){width="700" zoomable="yes"}

1. 對您的帳戶資訊進行必要的變更。

   如果您變更登入認證，請務必將其儲存在安全位置。

1. 輸入您目前的帳戶密碼。

1. 按一下 **[!UICONTROL Save Account]**.

## 允許多重管理員登入

管理員提供存取權，以管理訂單、客戶、產品、配送和付款功能。 預設設定已設定為不允許管理員使用者帳戶多次登入為安全性最佳實務。 不過，您可以變更此設定，以允許管理員使用者從多部裝置登入，以配合您的業務工作流程。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側導覽面板中，展開 **[!UICONTROL Advanced]** 並選擇 **[!UICONTROL Admin]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Security]** 區段。

1. 的 **管理員帳戶共用**，選取 `Yes`.

   ![允許管理員帳戶共用](./assets/multiple-admin-login.png){width="700" zoomable="yes"}

1. 按一下 **[!UICONTROL Save Config]**.

## 將管理員使用者登入名稱設為區分大小寫

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側導覽面板中，展開 **[!UICONTROL Advanced]** 並選擇 **[!UICONTROL Admin]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Security]** 區段。

1. 設定 **[!UICONTROL Login is Case Sensitive]** 欄位至 `Yes`.

1. 按一下 **[!UICONTROL Save Config]**.

[1]: https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2&amp;hl=en_US
