---
title: 『[!UICONTROL Security] &gt； [!UICONTROL 2FA]『
description: 檢閱上的組態設定 [!UICONTROL Security] &gt； [!UICONTROL 2FA] 商務管理員頁面。
exl-id: d3f6e16b-6eba-47db-a9dd-cb3268d1a13f
feature: Configuration, Security
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 1%

---

# [!UICONTROL Security] > [!UICONTROL 2FA]

>[!NOTE]
>
>已啟用Adobe Identity Management Services (IMS)驗證的商店已停用原生Adobe Commerce和Magento Open Source雙因素驗證(2FA)。 使用Adobe憑證登入其Adobe Commerce執行個體的管理員使用者不需要重新驗證許多管理員工作。 當管理員使用者登入目前的工作階段時，驗證會由Adobe IMS處理。 另請參閱 [將Adobe Commerce與Adobe IMS整合概覽](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

{{config}}

如需有關變更這些設定的詳細資訊，請參閱 [雙因素驗證(2FA)](../../systems/security-two-factor-authentication.md) 在 _Admin System指南_.

## [!UICONTROL General]

![一般](./assets/2fa-general.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Providers to use] | 全域 | 指示您需要的雙因素驗證方法。 如果您選取多個提供者，則每個使用者在下次登入時都必須設定每個2FA方法。 |
| [!UICONTROL Configuration Email URL for Web API] | 全域 | 對於自訂實施，為傳送至的備用電子郵件設定連結提供URL _管理員_ 初次登入的使用者。 在電子郵件範本中，使用預留位置 `:tfat` 以指出代號插入的位置。 |

{style="table-layout:auto"}

## [!UICONTROL Google]

![Google](./assets/2fa-google.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL OTP Window] | 全域 | Google Authenticator產生的每個一次性密碼(OTP)的期限（以秒為單位）。 預設： `30` |

{style="table-layout:auto"}

## [!UICONTROL Duo Security]

![Duo安全性](./assets/2fa-duo-security.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Integration Key] | 全域 | 您電腦的整合金鑰 [!DNL Duo Security] 帳戶。 |
| [!UICONTROL Secret Key] | 全域 | 您電腦中的秘密金鑰 [!DNL Duo Security] 帳戶。 |
| [!UICONTROL API Hostname] | 全域 | 來自您的 [!DNL Duo Security] 帳戶。 |

{style="table-layout:auto"}

## [!UICONTROL Authy]

![Authy](./assets/2fa-authy.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL API Key] | 全域 | 來自您的 [!DNL Authy] 帳戶。 |
| [!UICONTROL OneTouch Message] | 全域 | 顯示在「 」中的 [!DNL Authy] 登入時驗證者。 預設： `Login request to your Magento Admin` |

{style="table-layout:auto"}

## [!UICONTROL U2F Key]

![U2F金鑰](./assets/2fa-u2f-key.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL WebApi Challenge Domain] | 全域 | 用來發出和處理內容的網域 [!DNL WebAuthn] 自訂WebAPI實作的挑戰。 |

{style="table-layout:auto"}
