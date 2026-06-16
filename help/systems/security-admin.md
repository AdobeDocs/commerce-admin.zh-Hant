---
title: 設定管理員安全性
description: 瞭解如何為商店管理員設定安全性。
exl-id: 931fd8ad-96b7-42e5-9c3e-4bb9ca85b1ba
role: Admin
feature: Admin Workspace, Configuration, Security
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hant/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案（Adobe管理的PaaS基礎結構）和內部部署專案的Adobe Commerce 。"
TQID: https://experienceleague.adobe.com/UFK-C-W5E0DngIy4VncIVRzM2f6tNS5RgNqaNVk9GJc
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
subfeature_v2:
  - id: b01a71b7-d17a-42b2-a9ac-af4b8d9d2ef5
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 864
ht-degree: 0%

---

# 設定管理員安全性

建議您採取多方面的方法來保護商店的安全。 您可以透過使用不容易猜測的[自訂管理員URL](../stores-purchase/store-urls.md#use-a-custom-admin-url)開始，而不是使用明顯的「管理員」或「後端」。 根據預設，用來[登入](../getting-started/admin-signin.md)管理員的密碼長度必須是7個或7個以上的字元，且包含字母和數字。 您可以設定最低密碼長度要求，以根據貴組織的需求增強安全性。 根據[最佳作法](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html?lang=zh-Hant)，請只使用包含字母、數字和符號組合的強式管理員密碼。 Adobe Commerce和Magento Open Source不允許重複使用最近四個指派給帳戶的密碼。

管理員安全性設定可讓您：

- 將秘密金鑰新增至URL
- 要求密碼區分大小寫
- 設定密碼長度下限要求
- 限制管理員工作階段的長度
- 限制密碼的存留期
- 限制在Admin使用者帳戶為[鎖定](permissions-users-all.md#locked-users)之前可以嘗試登入的次數。

為了提高安全性，您可以設定目前工作階段到期之前鍵盤閒置的時間長度，並要求使用者名稱和密碼區分大小寫。

除了本節中的安全性設定外，還需要[雙因素驗證](security-two-factor-authentication.md) (2FA)以應用程式或裝置產生的一次性密碼來驗證使用者的身分。 第一次登入管理員時，系統會提示您設定2FA。 為了增加安全性，管理員登入也可以設定為需要[驗證碼](security-captcha.md)。

>[!NOTE]
>
>已啟用[!DNL Adobe Identity Management Services] (IMS)驗證的存放區已停用原生Adobe Commerce和Magento Open Source 2FA。 使用其Adobe憑證登入其Commerce執行個體的管理員使用者，不需要重新驗證許多管理員工作。 當管理員使用者登入目前的工作階段時，驗證會由Adobe IMS處理。 請參閱[[!DNL Adobe Identity Management Service] (IMS)整合概述](../getting-started/adobe-ims-integration-overview.md)。

如需技術資訊，請參閱開發人員檔案中的[安全性概觀](https://developer.adobe.com/commerce/php/architecture/basics/security/){:target="_blank"}。

![管理安全性](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

## 設定管理員安全性

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板的&#x200B;_[!UICONTROL Advanced]_&#x200B;下，選擇&#x200B;**[!UICONTROL Admin]**。

1. 展開&#x200B;**[!UICONTROL Security]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

1. 若要防止管理員使用者從不同裝置上的相同帳戶登入，請將&#x200B;**[!UICONTROL Admin Account Sharing]**&#x200B;設為`No`。

1. 若要決定用來管理密碼重設要求的方法，請將&#x200B;**[!UICONTROL Password Reset Protection Type]**&#x200B;設定為下列其中一項：

   - `By IP and Email` — 在收到來自通知的回應後，可以將密碼重設到與Admin帳戶關聯的電子郵件地址。
   - `By IP` — 密碼可以線上上重設，不需要其他確認。
   - `By Email` — 只有透過電子郵件回應傳送至與管理員帳戶相關之電子郵件地址的通知才能重設密碼。
   - `None` — 密碼只能由存放區管理員重設。

1. 設定登入安全性選項：

   - 對於&#x200B;**[!UICONTROL Recovery Link Expiration Period (hours)]**，請輸入密碼復原連結保持有效的小時數。

   - 若要決定每小時可提交的最大密碼要求數目，請輸入&#x200B;**[!UICONTROL Max Number of Password Reset Requests]**&#x200B;的數字。

   - 對於&#x200B;**[!UICONTROL Min Time Between Password Reset Requests]**，請輸入密碼重設要求之間必須經過的最小分鐘數。

   - 若要將秘密金鑰附加至管理員URL以防範利用漏洞攻擊，請將&#x200B;**[!UICONTROL Add Secret Key to URLs]**&#x200B;設為`Yes`。 此設定預設為啟用。

   - 若要要求在任何輸入的登入認證中使用大寫和小寫字元，都必須符合系統中儲存的內容，請將&#x200B;**[!UICONTROL Login is Case Sensitive]**&#x200B;設為`Yes`。

   - 若要在管理員工作階段逾時之前判斷其長度，請在&#x200B;**[!UICONTROL Admin Session Lifetime (seconds)]**&#x200B;欄位中輸入工作階段持續時間（以秒為單位）。 該值必須大於或等於60秒。

   - 針對&#x200B;**[!UICONTROL Maximum Login Failures to Lockout Account]**，輸入在帳戶鎖定前，使用者可以嘗試登入Admin的次數。 預設情況下，允許嘗試6次。 對於不限次數的登入嘗試，請將此欄位留空。

   - 對於&#x200B;**[!UICONTROL Lockout Time (minutes)]**，輸入當達到最大嘗試次數時，Admin帳戶鎖定的分鐘數。

1. 設定密碼選項：

   - 針對&#x200B;**[!UICONTROL Minimum Admin Password Length]**，輸入管理員密碼所需的最小字元數。 預設值為7，允許的最小值為7。

     >[!WARNING]
     >
     >若將此值從預設值變更，可能會導致現有服務的回溯相容性問題。 此設定會影響管理員密碼變更、從管理員介面和CLI建立新的管理員使用者，以及從管理員重設密碼。

   - 若要限制管理員密碼的存留期，請輸入密碼對&#x200B;**[!UICONTROL Password Lifetime (days)]**&#x200B;有效的天數。 對於無限期限，請將此欄位留空。

   - 將&#x200B;**[!UICONTROL Password Change]**&#x200B;設定為下列其中一項：

      - `Forced` — 要求系統管理員使用者在設定帳戶之後變更密碼。
      - `Recommended` — 建議管理員使用者在設定帳戶後變更密碼。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

## 管理員密碼需求

依預設，管理員密碼的長度必須是7個或7個以上的字元，且包含字母和數字。 您可以使用&#x200B;**[!UICONTROL Minimum Admin Password Length]**&#x200B;設定來設定密碼長度下限要求，以符合貴組織的安全性標準。 不過，提高此值可能會影響與現有服務和整合的相容性。
