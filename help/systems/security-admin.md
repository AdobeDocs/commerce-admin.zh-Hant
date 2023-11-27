---
title: 設定管理員安全性
description: 瞭解如何為商店管理員設定安全性。
exl-id: 931fd8ad-96b7-42e5-9c3e-4bb9ca85b1ba
role: Admin
feature: Admin Workspace, Configuration, Security
source-git-commit: e301cfaeec3a8427fff6138ba041bdbd7433c137
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 0%

---

# 設定管理員安全性

建議您採取多方面的方法來保護商店的安全。 您可從使用 [自訂管理員URL](../stores-purchase/store-urls.md#use-a-custom-admin-url) 這並不容易猜測，而不是顯而易見的「管理員」或「後端」。 根據預設，密碼用於 [登入](../getting-started/admin-signin.md) 管理員的長度必須是7個或更多字元，且包含字母和數字。 作為 [最佳實務](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html)，僅使用包含字母、數字和符號組合的增強式管理員密碼。 Adobe Commerce和Magento Open Source不允許重複使用最近四個指派給帳戶的密碼。

管理員安全性設定可讓您：

- 將秘密金鑰新增至URL
- 要求密碼區分大小寫
- 限制管理員工作階段的長度
- 限制密碼的存留期
- 在管理員使用者帳戶之前，限制可以嘗試登入的次數 [已鎖定](permissions-users-all.md#locked-users).

為了提高安全性，您可以設定目前工作階段到期之前鍵盤閒置的時間長度，並要求使用者名稱和密碼區分大小寫。

除了本節中的安全性設定外， [雙因素驗證](security-two-factor-authentication.md) 使用應用程式或裝置產生的一次性密碼來驗證使用者的身分時，需要(2FA)。 第一次登入管理員時，系統會提示您設定2FA。 為了提高安全性，管理員登入也可以設定為需要 [驗證碼](security-captcha.md).

>[!NOTE]
>
>已啟用的存放區 [!DNL Adobe Identity Management Services] (IMS)驗證已停用原生Adobe Commerce和Magento Open Source 2FA。 使用Adobe憑證登入其Commerce執行個體的管理員使用者不需要重新驗證許多管理員工作。 當管理員使用者登入目前的工作階段時，驗證會由Adobe IMS處理。 另請參閱 [[!DNL Adobe Identity Management Service] (IMS)整合概述](../getting-started/adobe-ims-integration-overview.md).

如需技術資訊，請參閱 [安全性概覽](https://developer.adobe.com/commerce/php/architecture/basics/security/)開發人員檔案中的{：target=&quot;_blank&quot;}。

![管理員安全性](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

## 設定管理員安全性

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中的 _[!UICONTROL Advanced]_，選擇&#x200B;**[!UICONTROL Admin]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Security]** 區段。

1. 若要防止管理員使用者從不同裝置上的相同帳戶登入，請設定 **[!UICONTROL Admin Account Sharing]** 至 `No`.

1. 若要確定用來管理密碼重設請求的方法，請設定 **[!UICONTROL Password Reset Protection Type]** 變更為下列其中一項：

   - `By IP and Email`  — 收到通知的回應後，可將密碼重設到與Admin帳戶關聯的電子郵件地址。
   - `By IP`  — 密碼可以線上上重設，不需要額外的確認。
   - `By Email`  — 只有透過電子郵件回應傳送至與管理員帳戶相關之電子郵件地址的通知才能重設密碼。
   - `None`  — 密碼只能由存放區管理員重設。

1. 設定登入安全性選項：

   - 的 **[!UICONTROL Recovery Link Expiration Period (hours)]**，輸入密碼復原連結保持有效的小時數。

   - 若要決定每小時可提交的最大密碼請求數，請輸入 **[!UICONTROL Max Number of Password Reset Requests]**.

   - 的 **[!UICONTROL Min Time Between Password Reset Requests]**，輸入密碼重設請求之間必須經過的最小分鐘數。

   - 若要將秘密金鑰附加至管理員URL以防範攻擊，請設定 **[!UICONTROL Add Secret Key to URLs]** 至 `Yes`. 此設定預設為啟用。

   - 若要要求在任何輸入的登入認證中使用大小寫字元，必須符合系統中儲存的內容，請設定 **[!UICONTROL Login is Case Sensitive]** 至 `Yes`.

   - 若要在逾時之前判斷管理員工作階段的時間長度，請以秒為單位輸入工作階段的持續時間 **[!UICONTROL Admin Session Lifetime (seconds)]** 欄位。 該值必須大於或等於60秒。

   - 的 **[!UICONTROL Maximum Login Failures to Lockout Account]**，輸入在帳戶鎖定前，使用者可以嘗試登入Admin的次數。 預設情況下，允許嘗試6次。 對於不限次數的登入嘗試，請將此欄位留空。

   - 的 **[!UICONTROL Lockout Time (minutes)]**，輸入當達到最大嘗試次數時，管理員帳戶鎖定的分鐘數。

1. 設定密碼選項：

   - 若要限制管理員密碼的存留期，請輸入密碼的有效天數 **[!UICONTROL Password Lifetime (days)]**. 對於無限期限，請將此欄位留空。

   - 設定 **[!UICONTROL Password Change]** 變更為下列其中一項：

      - `Forced`  — 要求管理員使用者在設定帳戶後變更密碼。
      - `Recommended`  — 建議管理員使用者在設定帳戶後變更密碼。

1. 完成後，按一下 **[!UICONTROL Save Config]**.

## 管理員密碼需求

依預設，管理員密碼的長度必須是7個或7個以上的字元，且包含字母和數字。
