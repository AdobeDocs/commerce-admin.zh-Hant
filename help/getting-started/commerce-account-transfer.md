---
title: 轉移Commerce帳戶
description: 瞭解如何將您的Commerce帳戶轉移給其他擁有者或電子郵件地址。
exl-id: f6528931-dbf1-4702-8989-232c27969c4a
feature: User Account
source-git-commit: e44ebfab5b9505098405b005051f110b689c3f4f
workflow-type: tm+mt
source-wordcount: '1035'
ht-degree: 0%

---

# 轉移Commerce帳戶

隨著業務責任變更，您可能需要將您的Commerce帳戶轉移給新所有者或其他電子郵件地址。 此轉移需要變更與帳戶相關聯的主要使用者電子郵件。

下列資訊說明Commerce (MAGEID)帳戶的轉移程式。 其中不包含雲端帳戶(雲端專案或New Relic)所有權的變更。 如需有關雲端專案存取許可權的詳細資訊，請參閱&#x200B;_雲端基礎結構上的Commerce指南_&#x200B;中的[管理使用者存取許可權](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html?lang=zh-Hant)。

>[!IMPORTANT]
>
>如果新帳戶擁有者已使用「共用存取」購買擴充功能，帳戶轉移程式一啟動，這些擴充功能的存取權就會遺失。 在要求帳戶轉移之前，請確定新擁有者從[他們的Marketplace帳戶](https://commercemarketplace.adobe.com/sales/order/history/)擷取購買的訂單ID，並向[Marketplace團隊](https://experienceleague.adobe.com/zh-hant/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case)要求這些擴充功能的退款。 無法將擴充功能購買轉移至其他帳戶。

## 識別您的傳輸型別

Commerce帳戶轉移的型別取決於目前擁有者和新擁有者可用的Commerce帳戶認證。 以下案例會根據這些認證說明不同的傳輸型別。

| 傳輸型別 | 目前擁有者 | 新擁有者 |
| ------------- | ------------- | --------- |
| [新Adobe ID和電子郵件變更](#new-adobe-id-and-email-change) | 具有&#x200B;**_未連線_**&#x200B;的MAGEID與Adobe登入帳戶。 | 沒有MAGEID且未連線至Adobe登入帳戶。 |
| [電子郵件變更](#email-change) | 具有&#x200B;**_已連線_**&#x200B;且Adobe登入帳戶的MAGEID。 | 沒有MAGEID且未連線至Adobe登入帳戶。 |
| [Adobe ID開關](#adobe-id-account-switch) | 具有&#x200B;**_已連線_**&#x200B;且Adobe登入帳戶的MAGEID。 | 具有MAGEID，且已連線至Adobe登入帳戶，但未關聯其他Adobe產品/服務。 |

{style="table-layout:auto"}

>[!NOTE]
>
>由於Adobe Commerce持續與其他Adobe解決方案整合，因此Commerce帳戶(MAGEID)現在需要與Adobe登入建立關聯。 此Adobe ID使用與您Commerce帳戶連線的相同電子郵件地址。

## 新的Adobe ID和電子郵件變更

>[!IMPORTANT]
>
>請檢閱[傳輸型別](#identify-your-transfer-type)，並確定您符合此步驟順序的先決條件。

此轉移型別需要您先建立關聯的Adobe ID，然後將該帳戶變更為新所有者的電子郵件地址。

1. 前往您的[Commerce帳戶](https://account.magento.com/customer/account/login/)。

1. 按一下&#x200B;**[!UICONTROL Sign in with Adobe ID]**。

1. 按一下&#x200B;**[!UICONTROL Create an account]**。

1. 輸入目前擁有者的電子郵件地址和密碼。

1. 按一下&#x200B;**[!UICONTROL Continue]**。

   此步驟會建立Adobe ID並將其連結至目前的Commerce帳戶(MAGEID)。 使用此帳戶連結，_[!UICONTROL Email]_&#x200B;欄位會遭到封鎖，無法進行任何變更。 相關電子郵件地址的設定是從Adobe ID帳戶進行管理。

1. 導覽至[account.adobe.com](https://account.adobe.com/)。

1. 按一下&#x200B;**[!UICONTROL Change Email]**。

1. 輸入新擁有者的電子郵件地址。

1. 按一下&#x200B;**[!UICONTROL Change]**。

   此步驟會產生驗證電子郵件，傳送至新的電子郵件地址。 電子郵件包含完成電子郵件地址變更所需的確認代碼。

1. 輸入傳送到新電子郵件地址的確認代碼。

1. 按一下&#x200B;**[!UICONTROL Verify]**。

>[!VIDEO](https://video.tv.adobe.com/v/3435325/?learn=on)

## 電子郵件變更

>[!IMPORTANT]
>
>請檢閱[傳輸型別](#identify-your-transfer-type)，並確定您符合此步驟順序的先決條件。

1. 導覽至[account.adobe.com](https://account.adobe.com/)並完成Adobe登入。

1. 在您的帳戶名稱和顯示圖片底下，按一下&#x200B;**[!UICONTROL Change Email]**。

1. 在對話方塊中，輸入新擁有者的電子郵件地址。

1. 按一下&#x200B;**[!UICONTROL Change]**。

   此步驟會產生驗證電子郵件，傳送至新的電子郵件地址。 電子郵件包含完成電子郵件地址變更所需的確認代碼。

1. 輸入傳送到新電子郵件地址的確認代碼。

1. 按一下&#x200B;**[!UICONTROL Verify]**。

## Adobe ID帳戶切換

>[!IMPORTANT]
>
>請檢閱[傳輸型別](#identify-your-transfer-type)，並確定您符合此步驟順序的先決條件。

如果目前擁有者和新擁有者擁有現有的Adobe ID，這兩個帳戶應該都會保留，但電子郵件地址需要在它們之間切換。 這需要使用有效的&#x200B;_暫時_&#x200B;電子郵件地址，但該電子郵件地址與Adobe ID無關。

### 變更為臨時帳戶

目前的擁有者完成這些步驟，將其Adobe ID與另一個臨時電子郵件地址建立關聯。

1. 導覽至[account.adobe.com](https://account.adobe.com/)並完成Adobe登入。

1. 在您的帳戶名稱和顯示圖片底下，按一下&#x200B;**[!UICONTROL Change Email]**。

1. 在對話方塊中，輸入Adobe ID未使用的有效暫時電子郵件地址。

   您必須具有電子郵件地址的存取權，才能擷取包含確認代碼的電子郵件。

1. 按一下&#x200B;**[!UICONTROL Change]**。

   此步驟會產生驗證電子郵件，傳送至暫存電子郵件地址。 電子郵件包含完成電子郵件地址變更所需的確認代碼。

1. 輸入傳送至臨時電子郵件地址的確認代碼。

1. 按一下&#x200B;**[!UICONTROL Verify]**。

1. 登出Adobe帳戶。

### 新所有者步驟

在目前擁有者完成傳輸至臨時電子郵件地址後，新擁有者必須完成這些步驟，變更其帳戶設定，以指向目前擁有者的原始電子郵件地址。

1. 導覽至[account.adobe.com](https://account.adobe.com/)並完成Adobe登入。

1. 在您的帳戶名稱和顯示圖片底下，按一下&#x200B;**[!UICONTROL Change Email]**。

1. 在對話方塊中，輸入目前擁有者的原始電子郵件地址。

1. 按一下&#x200B;**[!UICONTROL Change]**。

   此步驟會產生驗證電子郵件，傳送至目前擁有者的原始電子郵件地址。 電子郵件包含完成電子郵件地址變更所需的確認代碼。

1. 輸入傳送至目前擁有者原始電子郵件地址的確認代碼。

1. 按一下&#x200B;**[!UICONTROL Verify]**。

1. 登出Adobe帳戶。

### 後續步驟

新擁有者使用目前（現在為上一個）擁有者的原始電子郵件地址成功設定其Adobe帳戶後，請完成這些步驟以轉移擁有權。

1. 導覽至[account.adobe.com](https://account.adobe.com/)，並使用[暫時帳戶](#change-to-a-temporary-account)的電子郵件地址完成Adobe登入。

1. 在帳戶名稱和顯示圖片底下，按一下&#x200B;**[!UICONTROL Change Email]**。

1. 在對話方塊中，輸入新擁有者的電子郵件地址。

1. 按一下&#x200B;**[!UICONTROL Change]**。

   此步驟會產生驗證電子郵件，傳送至新所有者的電子郵件地址。 電子郵件包含完成電子郵件地址變更所需的確認代碼。

1. 輸入傳送至新擁有者電子郵件地址的確認代碼。

1. 按一下&#x200B;**[!UICONTROL Verify]**。

>[!IMPORTANT]
>
>提交支援請求，通知支援團隊您已更新帳戶所有者的電子郵件地址。 團隊必須執行其他步驟以完成更新，例如更新[Commerce Marketplace](https://commercemarketplace.adobe.com/)設定檔上的電子郵件地址。 在您的請求中包含先前的帳戶擁有者電子郵件地址。
