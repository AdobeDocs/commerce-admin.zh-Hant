---
title: Adobe Identity Management Service (IMS)整合概述
description: 介紹Adobe Commerce管理員登入與Adobe IMS的選擇性整合
exl-id: 106d731c-a541-4a19-a38c-221e80740508
feature: Identity Management
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"
source-git-commit: 484351d7db33139e3339ccea82e7a96f5ea7966e
workflow-type: tm+mt
source-wordcount: '817'
ht-degree: 0%

---

# Adobe Identity Management Service (IMS)整合概述

{{ee-feature}}

擁有Adobe Commerce帳戶的Adobe管理員使用者現在可以使用其Adobe ID登入Adobe Commerce。 Adobe Identity Management Service (IMS)是Adobe以OAuth 2.0為基礎的身分管理功能，可支援驗證。 將Commerce管理驗證整合至Adobe商務產品的IMS驗證工作流程，可簡化使用其他Adobe產品之使用者的驗證程式。 此整合為選用性，且會根據執行個體來啟用。 啟用此整合時，只有管理員使用者工作流程會受到影響。 

Commerce管理員IMS整合所需的模組會封裝在`adobe-ims-metapackage`中，此套件與Adobe Commerce核心發行版本搭配。

若要實作此整合，請參閱[使用IMS設定Commerce管理整合](./adobe-ims-config.md)。

## 與IMS整合後管理工作流程和介面的變更

啟用這項整合後，Commerce管理員使用者在管理員中執行需要重新驗證的例行工作時（例如建立管理員使用者），會體驗到預設Commerce管理員登入和驗證工作流程的變更。 啟用模組需要在Adobe組織層級執行雙因素驗證(2FA)。 預設的管理員登入和2FA已停用，且&#x200B;_[!UICONTROL Sign In with Adobe ID]_&#x200B;按鈕會取代預設的管理員登入表單。 許可權仍由管理員管理。

>
>
>AdobeIms整合會全域套用。 啟用後，所有使用者都必須透過AdobeIms進行驗證；此設定無法排除個別使用者。
>
>**只有在完全瞭解此整合的影響後，才可啟用此整合。**

## 管理員與IMS的整合如何影響Commerce密碼

已與Adobe IMS整合的Commerce部署需要Adobe ID帳戶，才能存取在IMS啟用程式中為Commerce應用程式設定的Adobe IMS組織。  IMS整合啟用時，管理員使用者會使用其Adobe憑證，透過Adobe登入頁面進行驗證。 只要啟用Adobe IMS整合，管理員使用者的Commerce密碼和使用者名稱就不會再用於驗證。

如果IMS整合已停用，管理員使用者必須使用其Commerce使用者名稱和密碼再次透過Adobe Commerce進行驗證。 管理員使用者在啟用這項整合之前，應儲存其Commerce管理員憑證（使用者名稱和密碼）和2FA憑證。

與使用者驗證有關的某些後端元件仍需要非Null密碼。 為了滿足此需求，Commerce會在`admin_user`表格中為新建立的管理員使用者建立隨機密碼。

Commerce應用程式的使用者帳戶和角色許可權仍由Commerce管理員管理。


## 使用IMS憑證產生網頁API權杖

在Commerce執行個體中啟用Adobe IMS的管理員驗證時，Commerce管理員API會受到影響。 管理員使用者無法再使用Commerce執行個體發行的認證。 這些是登入管理員和取得存取權杖所需的認證，服務可使用這些權杖來向管理員REST和SOAP API提出請求。

啟用Adobe IMS整合後，管理員使用者必須為需要驗證的Adobe Commerce API端點使用[Adobe IMS OAuth權杖](https://developer.adobe.com/developer-console/docs/guides/authentication/)。 使用者端解決方案會動態取得權杖以供網頁API使用。 在設定這項整合時，REST和SOAP Web API區域會啟用此驗證機制。

請參閱[權杖型驗證](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-token/)，以概略瞭解Web API如何使用Commerce存取權杖，包括IMS存取權杖。

## Commerce工作階段管理和Adobe IMS存取權杖

存取權杖中同時包含使用者認證和登入工作階段資訊。 使用者完成驗證且工作階段開始後，這兩個變數會新增至使用者的工作階段：

`token_last_check_time`。 識別目前時間，並由`\Magento\AdminAdobeIms\Plugin\BackendAuthSessionPlugin`外掛程式使用。

`adobe_access_token` — 識別在授權期間收到的`ACCESS_TOKEN`值。

`\Magento\AdminAdobeIms\Plugin\BackendAuthSessionPlugin`外掛程式會檢查`token_last_check_time`是否在10分鐘前更新。 如果`token_last_check_time`在十分鐘前已檢視，則驗證工作流程會對IMS進行API呼叫以驗證存取權杖，而工作階段會繼續進行。 如果存取權杖有效，則`token_last_check_time`值會更新為目前時間。 如果權杖無效，工作階段就會終止。

## 重要檔案

`adminAdobeIms` — 提供以`AdobeImsApi`模組為基礎的管理員登入實作。

`admin_adobe_ims_webapi` — 維護所有已驗證存取權杖的記錄。 當權杖通過驗證或失效時，其狀態的記錄將保留在此表格中。

`adobeIms` — 實作與Adobe IMS整合相關的所有商業邏輯（保留以防止回溯不相容）。

`adobeImsApi` — 宣告支援與Adobe IMS整合的介面。

`adminadobe-ims.log` — 錯誤記錄檔。

## 啟用整合

Adobe IMS中繼隨Adobe Commerce 2.4.5及更高版本安裝，但必須設定為可使用。 它會擴充`AdobeIms`模組以支援啟用驗證邏輯(`AdminAdobeIms`)的模組。

如需啟用整合的詳細資訊，請參閱[使用Adobe IMS設定Commerce管理整合](./adobe-ims-config.md)。
