---
title: '[!UICONTROL Security] > [!UICONTROL 2FA]'
description: 檢閱Commerce管理員的[!UICONTROL Security] &gt； [!UICONTROL 2FA]頁面上的組態設定。
exl-id: d3f6e16b-6eba-47db-a9dd-cb3268d1a13f
feature: Configuration, Security
TQID: https://experienceleague.adobe.com/-5t8bTj14iB---88TotUNefATWwE80LTswPO3xVWU70
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 338
ht-degree: 1%

---

# [!UICONTROL Security] > [!UICONTROL 2FA]

>[!NOTE]
>
>已啟用Adobe Identity Management Services (IMS)驗證的商店已停用原生Adobe Commerce和Magento Open Source雙因素驗證(2FA)。 使用其Adobe憑證登入其Adobe Commerce執行個體的管理員使用者，不需要重新驗證許多管理員工作。 當管理員使用者登入目前的工作階段時，驗證會由Adobe IMS處理。 請參閱[整合Adobe Commerce與Adobe IMS概述](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html)。

{{config}}

如需有關變更這些設定的詳細資訊，請參閱&#x200B;_系統管理系統指南_&#x200B;中的[雙因素驗證(2FA)](../../systems/security-two-factor-authentication.md)。

## [!UICONTROL General]

![一般](./assets/2fa-general.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Providers to use] | 全域 | 指示您需要的雙因素驗證方法。 如果您選取多個提供者，則每個使用者在下次登入時都必須設定每個2FA方法。 |
| [!UICONTROL Configuration Email URL for Web API] | 全域 | 對於自訂實作，在第一次登入時傳送給&#x200B;_管理員_&#x200B;使用者的備用電子郵件設定連結的URL。 在電子郵件範本中，使用預留位置`:tfat`來指示代號插入的位置。 |
| [!UICONTROL Retry attempt limit for Two-Factor Authentication] | 全域 | 決定在暫時停用帳戶之前，系統管理員可以輸入[!DNL one-time password (OTP)]的次數。 預設： `10` |
| [!UICONTROL Two-Factor Authentication lockout time (seconds)] | 全域 | 決定管理員在其帳戶暫時停用之前可以等待多久輸入[!DNL one-time password (OTP)] （以秒為單位）。 預設： `300` |

{style="table-layout:auto"}

## [!UICONTROL Google]

![Google](./assets/2fa-google.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL OTP Window] | 全域 | 決定系統接受管理員[!DNL one-time-password (OTP)]過期後的時間（秒）。 不能超過單一OTP的存留期（通常為30秒）。 預設： `29` |

{style="table-layout:auto"}

## [!UICONTROL Duo Security]

![Duo安全性](./assets/2fa-duo-security.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Client Id] | 全域 | 來自您[!DNL Duo Security]帳戶的使用者端ID。 |
| [!UICONTROL Client Secret] | 全域 | 您[!DNL Duo Security]帳戶的使用者端密碼。 |
| [!UICONTROL Integration Key] | 全域 | 來自您[!DNL Duo Security] API帳戶的整合金鑰。 |
| [!UICONTROL Secret Key] | 全域 | [!DNL Duo Security] API帳戶的秘密金鑰。 |
| [!UICONTROL API Hostname] | 全域 | [!DNL Duo Security]帳戶的API主機名稱。 |

{style="table-layout:auto"}

## [!UICONTROL Authy]

![授權](./assets/2fa-authy.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL API Key] | 全域 | [!DNL Authy]帳戶的API金鑰。 |
| [!UICONTROL OneTouch Message] | 全域 | 登入時[!DNL Authy]驗證者中顯示的訊息。 預設： `Login request to your Magento Admin` |

{style="table-layout:auto"}

## [!UICONTROL U2F Key]

![U2F金鑰](./assets/2fa-u2f-key.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL WebApi Challenge Domain] | 全域 | 用來為自訂WebAPI實作發出及處理[!DNL WebAuthn]挑戰的網域。 |

{style="table-layout:auto"}
