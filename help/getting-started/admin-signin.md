---
title: 您的管理員使用者帳戶
description: 瞭解您的管理員帳戶以及如何使用雙因素驗證來登入管理員。
exl-id: ad576533-5914-49d1-8e73-3f59c55543a5
feature: Admin Workspace, User Account
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '1160'
ht-degree: 0%

---

# 您的管理員帳戶

主要Admin帳戶最初是在安裝期間設定，可能包含初始預留位置資訊或範例資料資訊。 此帳戶的指定擁有者可以個人化使用者名稱和密碼，並隨時更新名字、姓氏和電子郵件地址。 此帳戶預設為擁有所有許可權的&#x200B;_超級使用者_，通常會建立業務所需的管理員使用者帳戶。

- 如需新增或編輯使用者的資訊，請參閱[建立使用者](../systems/permissions-users-all.md#create-a-user)。

- 如需有關管理員和使用者角色的資訊，請參閱[許可權](../systems/permissions.md)和[使用者角色](../systems/permissions-user-roles.md)。

{{ims-admin-note}}

## 管理員登入

[!DNL Commerce] _Admin_&#x200B;受到多層安全性措施的保護，以防止未經授權存取您的商店、訂單和客戶資料。 第一次登入&#x200B;_管理員_&#x200B;時，您必須輸入使用者名稱和密碼，並設定[雙因素驗證](../systems/security-two-factor-authentication.md) (2FA)。

根據您商店的設定，可能會有[驗證碼](../systems/security-google-recaptcha.md)難題需要解決，例如輸入一系列鍵盤字元、解決謎題，或按一下具有共同主題的影像系列。 這些測試旨在將您識別為人類，而不是自動化機器人。

為了增加安全性，您可以決定每個使用者在&#x200B;_Admin_&#x200B;中擁有[存取許可權](../systems/permissions.md)的哪些部分，也可以限制[登入嘗試](../configuration-reference/advanced/admin.md)的次數。 根據預設，帳戶在六次嘗試後會鎖定，使用者必須等候幾分鐘再重試。 也可以從[Admin](../systems/permissions-users-all.md#locked-users)重設&#x200B;_鎖定的帳戶_。

>[!NOTE]
>
>第一次登入&#x200B;_Admin_&#x200B;時，系統會提示您&#x200B;_允許管理員使用資料收集_。 如需詳細資訊，請參閱[使用狀況資料集合](admin.md#usage-data-collection)。

![管理員登入](./assets/admin-login.png){width="400"}

### 步驟1：設定雙因素驗證

您必須先設定雙因素驗證解決方案，並準備好使用，才能登入商店的&#x200B;_管理員_。 若要進一步瞭解每個解決方案所使用的驗證程式，請參閱[使用雙因素驗證](../systems/security-two-factor-authentication-use.md)。 依預設，[!DNL Commerce]支援[Google驗證器](https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2&hl=en_US)。

請向您的[!DNL Commerce]系統管理員詢問市集支援哪些2FA解決方案。 接著，根據提供者的指示，完成您偏好的2FA解決方案設定。

### 步驟2：登入管理員

1. 輸入在&#x200B;_安裝期間指定的_&#x200B;管理員[!DNL Commerce] URL。

   預設&#x200B;_Admin_ URL類似於`https://www.yourdomain.com/your-custom-admin-domain`。

   >[!NOTE]
   >
   >雖然此檔案在大多數範例中都使用`admin`作為基底URL，但建議您為商店的[管理員](../stores-purchase/store-urls.md)選擇唯一且難以猜測的&#x200B;_自訂URL_。

   您可以為頁面新增書籤或在案頭上儲存捷徑以方便存取。

1. 輸入您的&#x200B;_管理員_ **[!UICONTROL Username]**&#x200B;和&#x200B;**[!UICONTROL Password]**。

1. （選擇性）如果您的商店已啟用驗證碼，請依照熒幕上的指示解決挑戰。

   若要深入瞭解，請參閱[驗證碼](../systems/security-captcha.md)和[reCAPTCHA](../systems/security-google-recaptcha.md)。

1. 按一下&#x200B;**[!UICONTROL Sign in]**。

   如果這是您第一次從帳戶登入&#x200B;_Admin_，您應該會收到一封包含設定指示連結的電子郵件。

### 步驟3：完成2FA設定

下列範例說明如何將您的&#x200B;_Admin_&#x200B;帳戶與Google Authenticator配對。

1. 當QR代碼出現時，請使用下列其中一種方法來擷取代碼，並將Google Authenticator與您的&#x200B;_Admin_&#x200B;帳戶配對。

   ![設定Google Authenticator](./assets/admin-login-google-auth-setup.png){width="400"}

   - 使用智慧型手機擷取QR碼

     在智慧型手機上啟動Google Authenticator。 點選應用程式右上角的&#x200B;_加號_ (+)。 然後在畫面底部，點選&#x200B;**[!UICONTROL Scan Barcode]**&#x200B;並拍攝QR碼的圖片。

   - 從瀏覽器擷取QR碼

     如果Google Authenticator是以擴充功能安裝在瀏覽器中，請按一下工具列中的&#x200B;**Authenticator**&#x200B;圖示並擷取頁面。

   - 手動輸入QR碼

     複製QR碼下方的文字字串。 使用您的智慧型手機或瀏覽器啟動Google Authenticator，然後按一下加號(+)。 然後選擇&#x200B;**[!UICONTROL Manual Entry]**。 在&#x200B;**[!UICONTROL Account]**&#x200B;下方，輸入與您的&#x200B;_Admin_&#x200B;帳戶相關聯的電子郵件地址，並將QR字串貼到&#x200B;**[!UICONTROL Key]**&#x200B;欄位中。

1. 若要以雙因素驗證登入&#x200B;_管理員_，請在&#x200B;**[!UICONTROL Authenticator code]**&#x200B;欄位中輸入Google驗證程式產生的六位數代碼，然後按一下&#x200B;**[!UICONTROL Confirm]**。

   ![輸入驗證程式碼](./assets/admin-login-2fa-google.png){width="400"}

## 重設密碼

不允許重複使用指派給帳戶的最後四個密碼。

1. 輸入與&#x200B;**[!UICONTROL Email Address]** Admin _帳戶相關聯的_。

   ![忘記密碼](./assets/admin-sign-in-forgot-password.png){width="400"}

1. 按一下&#x200B;**[!UICONTROL Retrieve Password]**。

   如果帳戶與電子郵件地址相關聯，則會傳送電子郵件以重設您的密碼。

   >[!NOTE]
   >
   >_Admin_&#x200B;密碼長度必須是7個或7個以上的字元，且包含字母和數字。 如需密碼選項的詳細資訊，請參閱[設定&#x200B;_管理員_&#x200B;安全性](../systems/security-admin.md)。

## 登出管理員

1. 按一下右上角的&#x200B;_帳戶_ （![帳戶](../assets/icon-admin-user.png)）圖示。

1. 按一下&#x200B;**[!UICONTROL Sign Out]**。

   ![登出](./assets/admin-sign-out.png){width="700" zoomable="yes"}

_[!UICONTROL Sign In]_頁面會顯示您已登出的訊息。 每當您離開電腦時，請登出_ Admin _。

## 編輯帳戶資訊

1. 按一下&#x200B;_帳戶_ （![帳戶圖示](../assets/icon-admin-user.png)）圖示。

1. 按一下&#x200B;**[!UICONTROL Account Setting]**。

   ![帳戶資訊](./assets/admin-account-information.png){width="700" zoomable="yes"}

1. 對您的帳戶資訊進行必要的變更。

   如果您變更登入認證，請務必將其儲存在安全位置。

1. 輸入您目前的帳戶密碼。

1. 按一下&#x200B;**[!UICONTROL Save Account]**。

## 允許多重管理員登入

管理員提供存取權，以管理訂單、客戶、產品、配送和付款功能。 預設設定已設定為不允許管理員使用者帳戶多次登入為安全性最佳實務。 不過，您可以變更此設定，以允許管理員使用者從多部裝置登入，以配合您的業務工作流程。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側導覽面板中，展開&#x200B;**[!UICONTROL Advanced]**&#x200B;並選擇&#x200B;**[!UICONTROL Admin]**。

1. 展開![區段的](../assets/icon-display-expand.png)擴充選擇器&#x200B;**[!UICONTROL Security]**。

1. 針對&#x200B;**管理員帳戶共用**，請選取`Yes`。

   ![允許系統管理員帳戶共用](./assets/multiple-admin-login.png){width="700" zoomable="yes"}

1. 按一下&#x200B;**[!UICONTROL Save Config]**。

## 將管理員使用者登入名稱設為區分大小寫

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側導覽面板中，展開&#x200B;**[!UICONTROL Advanced]**&#x200B;並選擇&#x200B;**[!UICONTROL Admin]**。

1. 展開![區段的](../assets/icon-display-expand.png)擴充選擇器&#x200B;**[!UICONTROL Security]**。

1. 將&#x200B;**[!UICONTROL Login is Case Sensitive]**&#x200B;欄位設為`Yes`。

1. 按一下&#x200B;**[!UICONTROL Save Config]**。


## 維護對管理員的安全存取

為確保管理員的安全，請以管理員存取權定期稽核使用者和角色。

此外，請考慮[更新Admin Base URL設定](https://experienceleague.adobe.com/en/docs/commerce-admin/config/advanced/admin#admin-base-url)以將預設`/admin`端點變更為自訂路徑。 設定自訂路徑可提供下列安全性優點：

**增強式安全性**：預設的「管理員」路徑是眾所周知的，且經常是惡意行為者嘗試暴力攻擊的目標。 將其變更為唯一的自訂值，可大幅降低未經授權存取嘗試的風險。

**減少漏洞**：自動化機器人經常掃描類似「管理員」等常見路徑，以利用漏洞。 自訂路徑會讓這些機器人更難找到您的管理員登入頁面，進而降低受到攻擊的可能性。

**已改善隱私權**：自訂管理路徑新增了額外的遮蔽層，讓潛在攻擊者更難識別並鎖定您的管理登入頁面。

**遵循最佳實務**：遵循安全性最佳實務（例如自訂您的管理員路徑），示範保護電子商務網站和客戶資料的主動方法。

>[!NOTE]
>
>如果懷疑發生入侵，請務必移除所有未知的管理員使用者，並重設所有管理員密碼，並檢閱[安全性行動計畫](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/security/security)以取得進一步的步驟。
