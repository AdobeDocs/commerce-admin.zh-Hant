---
title: 轉移Adobe Commerce帳戶
description: 瞭解如何將Adobe Commerce帳戶轉讓給新的擁有者或電子郵件地址、選擇正確的轉讓型別、驗證電子郵件變更並聯絡支援人員。
exl-id: f6528931-dbf1-4702-8989-232c27969c4a
feature: User Account
TQID: https://experienceleague.adobe.com/CIyzus4f8WcBH-jW9R1nCL-gkl065DLTHbjNn0K6e7E
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: e01cba363eb149286479718e660f8cdf6526e826
workflow-type: tm+mt
source-wordcount: 1553
ht-degree: 0%

---

# 轉移Adobe Commerce帳戶

隨著業務責任變更，您可能需要將您的Adobe Commerce帳戶轉移給新所有者或其他電子郵件地址。 此轉移需要變更與帳戶相關聯的主要使用者電子郵件。

下列資訊說明Adobe Commerce帳戶(MAGEID)的轉移程式。 其中不包含雲端基礎結構專案所有權或[!DNL New Relic]所有權的變更Adobe Commerce。 如需有關雲端專案存取許可權的詳細資訊，請參閱&#x200B;_雲端基礎結構上的Commerce指南_&#x200B;中的[管理使用者存取許可權](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/project/user-access)。

>[!IMPORTANT]
>
>如果新帳戶擁有者使用「共用存取」購買擴充功能，帳戶轉移一開始，這些擴充功能的存取權就會遺失。
>
>在要求帳戶轉移之前，請確定新擁有者從[他們的 [!DNL Commerce Marketplace] 帳戶](https://commercemarketplace.adobe.com/sales/order/history/)擷取購買的訂單ID，並向[[!DNL Commerce Marketplace] 團隊](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case)要求退款。 擴充功能購買無法轉移到其他帳戶。

## 識別您的傳輸型別

適當的Adobe Commerce帳戶轉移程式取決於目前擁有者和新擁有者的帳戶狀態，以及目前擁有者的電子郵件地址是否仍可存取。 例如，如果目前擁有者已離開公司，您可能仍需要存取傳送至該地址的電子郵件。

下列案例會根據這些條件說明可用的傳輸選項。

| 傳輸型別 | 目前擁有者 | 新擁有者 |
| ------------- | ------------- | --------- |
| [新Adobe ID和電子郵件變更](#new-adobe-id-and-email-change) | 擁有尚未連線至Adobe ID的MAGEID | 沒有MAGEID，也沒有Adobe ID。 |
| [僅電子郵件變更](#email-change) | 擁有連線至Adobe ID的MAGEID。 | 具有Adobe ID，但未將MAGEID連線至帳戶。 |
| [Adobe ID帳戶開關](#adobe-id-account-switch) | 擁有連線至Adobe ID的MAGEID。 | 具有MAGEID且已連線至Adobe ID。 |

{style="table-layout:auto"}

>[!NOTE]
>
>由於Adobe Commerce持續與其他Adobe解決方案整合，因此Adobe Commerce帳戶(MAGEID)現在需要與Adobe ID建立關聯。 Adobe ID使用連線至您[Adobe Commerce帳戶](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account)的相同電子郵件地址。

## 驗證Adobe ID電子郵件變更

在[account.adobe.com](https://account.adobe.com/)上，有數個傳輸路徑使用相同的驗證工作流程。 輸入目標電子郵件地址並按一下&#x200B;**[!UICONTROL Change]**&#x200B;之後，請完成下列步驟：

1. 開啟傳送至您輸入之地址的驗證電子郵件，並尋找確認代碼。

1. 輸入確認代碼。

1. 按一下&#x200B;**[!UICONTROL Verify]**。

## 新的Adobe ID和電子郵件變更

>[!IMPORTANT]
>
>檢閱[傳輸型別](#identify-your-transfer-type)，並確認此路徑符合您的情況：
>
>- 目前擁有者仍在公司內。
>- 目前擁有者可能沒有Adobe ID，或其Adobe ID未連線至其[Adobe Commerce帳戶(MAGEID)](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account)。
>- 新所有者沒有Adobe ID且沒有Adobe Commerce帳戶。

當目前擁有者的MAGEID尚未連結至Adobe ID時，請使用此路徑。 目前擁有者先建立並連結Adobe ID，然後將Adobe ID電子郵件地址變更為新擁有者的電子郵件地址。

1. 移至[Adobe Commerce帳戶登入](https://account.magento.com/customer/account/login/)頁面。

1. 按一下&#x200B;**[!UICONTROL Sign in with Adobe ID]**。

1. 按一下&#x200B;**[!UICONTROL Create an account]**。

1. 輸入目前擁有者的電子郵件地址和密碼。

1. 按一下&#x200B;**[!UICONTROL Continue]**。

   此步驟會建立Adobe ID並將其連結至目前的Adobe Commerce帳戶(MAGEID)。 使用此帳戶連結，_[!UICONTROL Email]_欄位會遭到封鎖，無法進行任何變更。 相關電子郵件地址的設定是從Adobe ID帳戶進行管理。

1. 導覽至[account.adobe.com](https://account.adobe.com/)。

1. 按一下&#x200B;**[!UICONTROL Change Email]**。

1. 輸入新擁有者的電子郵件地址。

   如果新的電子郵件地址已經連結到系統中的另一個帳戶，則無法直接用於轉移。 請改為遵循[Adobe ID帳戶引數](#adobe-id-account-switch)路徑，並使用[臨時電子郵件地址](#change-to-a-temporary-account)。

1. 完成[電子郵件驗證步驟](#verify-an-adobe-id-email-change)。

新擁有者驗證電子郵件地址後，請繼續[最後步驟](#final-steps)，以便Adobe Commerce支援可以更新帳戶記錄，例如[[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/)設定檔。

>[!VIDEO](https://video.tv.adobe.com/v/3435325/?learn=on){transcript=true}

## 僅限電子郵件變更 {#email-change}

>[!IMPORTANT]
>
>檢閱[傳輸型別](#identify-your-transfer-type)，並確認此路徑符合您的情況：
>
>- 目前擁有者仍在公司內。
>- 目前擁有者的Adobe ID已連線至其[Adobe Commerce帳戶(MAGEID)](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account)。
>- 新擁有者的Adobe ID未連線至Adobe Commerce帳戶。

開始之前，請注意，此轉移型別會導致目前的帳戶擁有者無法存取與該Adobe ID相關聯的其他Adobe產品。

1. 導覽至[account.adobe.com](https://account.adobe.com/)並完成Adobe登入。

1. 在您的帳戶名稱和顯示圖片底下，按一下&#x200B;**[!UICONTROL Change Email]**。

1. 在對話方塊中，輸入新擁有者的電子郵件地址。

   如果新的電子郵件地址已經連結到系統中的另一個帳戶，則無法直接用於轉移。 請改為遵循[Adobe ID帳戶引數](#adobe-id-account-switch)路徑，並使用[臨時電子郵件地址](#change-to-a-temporary-account)。

1. 完成[電子郵件驗證步驟](#verify-an-adobe-id-email-change)。

新擁有者驗證電子郵件地址後，請繼續[最後步驟](#final-steps)，以便Adobe Commerce支援可以更新帳戶記錄，例如[[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/)設定檔。

## Adobe ID帳戶切換

>[!IMPORTANT]
>
>檢閱[傳輸型別](#identify-your-transfer-type)，並確認此路徑符合您的情況：
>
>- 目前擁有者已離開公司，但仍可存取傳送至目前擁有者公司電子郵件地址的電子郵件，或您的IT團隊可將這些電子郵件轉寄給授權連絡人。
>- 目前擁有者的Adobe ID已連線至其[Adobe Commerce帳戶(MAGEID)](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account)。
>- 新擁有者的Adobe ID已連線至其Adobe Commerce帳戶。

當目前擁有者和新擁有者都有現有的Adobe ID，而您想要保留這兩個Adobe ID時，此轉移型別會使用暫時電子郵件地址來切換帳戶擁有權。 若要完成所有權轉讓，您必須使用與Adobe ID無關聯的臨時電子郵件地址。

### 變更為臨時帳戶

完成這些步驟，將目前擁有者的Adobe ID與暫時電子郵件地址建立關聯。 您必須能存取該電子郵件地址，才能擷取確認代碼。

>[!NOTE]
>
>如果您無法存取目前所有者的電子郵件，請要求您的IT團隊為您公司電子郵件系統中的帳戶電子郵件地址設定電子郵件轉寄。 如果無法設定電子郵件轉寄，請確定新帳戶擁有者擁有Adobe ID，然後[提交支援要求](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case)，其中包含啟動帳戶轉送所需的全部詳細資料。

1. 導覽至[account.adobe.com](https://account.adobe.com/)並完成Adobe登入。

1. 在您的帳戶名稱和顯示圖片底下，按一下&#x200B;**[!UICONTROL Change Email]**。

1. 在對話方塊中，輸入Adobe ID未使用的有效暫時電子郵件地址。

1. 完成[電子郵件驗證步驟](#verify-an-adobe-id-email-change)。

1. 登出Adobe帳戶。

### 新所有者步驟

在目前擁有者完成轉送至臨時電子郵件地址後，新擁有者必須完成這些步驟，將其Adobe ID電子郵件地址變更為目前擁有者的原始電子郵件地址。

1. 導覽至[account.adobe.com](https://account.adobe.com/)並完成Adobe登入。

1. 在您的帳戶名稱和顯示圖片底下，按一下&#x200B;**[!UICONTROL Change Email]**。

1. 在對話方塊中，輸入目前擁有者的原始電子郵件地址。

1. 完成[電子郵件驗證步驟](#verify-an-adobe-id-email-change)。

1. 登出Adobe帳戶。

### 後續步驟

新擁有者使用目前擁有者的原始電子郵件地址成功設定其Adobe ID後，請完成這些步驟以將該電子郵件地址指派給新擁有者。

1. 導覽至[account.adobe.com](https://account.adobe.com/)，並使用[暫時帳戶](#change-to-a-temporary-account)的電子郵件地址完成Adobe登入。

1. 在帳戶名稱和顯示圖片底下，按一下&#x200B;**[!UICONTROL Change Email]**。

1. 在對話方塊中，輸入新擁有者的電子郵件地址。

1. 完成[電子郵件驗證步驟](#verify-an-adobe-id-email-change)。

新擁有者驗證電子郵件地址後，請繼續[最後步驟](#final-steps)，以便Adobe Commerce支援可以更新帳戶記錄，例如[[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/)設定檔。

## 最後步驟

完成[新Adobe ID和電子郵件變更](#new-adobe-id-and-email-change)、[僅電子郵件變更](#email-change)或[Adobe ID帳戶切換](#adobe-id-account-switch)程式後，請完成這些步驟。

1. 作為新擁有者，[提交支援要求](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide?lang=en#support-case)。

   包含下列詳細資料：

   - 前一個帳戶擁有者的電子郵件地址
   - 新所有者的電子郵件地址
   - 請注意，您已完成Adobe Commerce帳戶移轉並更新Adobe ID電子郵件地址

1. 等待Adobe Commerce支援確認更新。

   支援也會更新相關記錄，例如您[[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/)設定檔上的電子郵件地址。

在支援完成請求後，新擁有者可以使用其Adobe ID登入Adobe Commerce帳戶。 MAGEID仍然是帳戶的權利識別碼。
