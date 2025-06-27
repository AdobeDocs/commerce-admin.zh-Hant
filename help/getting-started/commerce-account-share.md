---
title: 共用 [!DNL Commerce] 帳戶
description: 瞭解如何授予其他 [!DNL Commerce] 帳戶持有人對您 [!DNL Commerce] 帳戶的有限存取權。
exl-id: adc4fed4-89f4-4b0c-811c-fcf6f94dbc22
feature: User Account
source-git-commit: 6aa0ed78e668aa09170cbd47284dd2d559f1319b
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 0%

---

# 共用[!DNL Commerce]帳戶

您的[!DNL Commerce]帳戶包含您可以提供給受信任員工和協助管理您網站的服務提供者的資訊。 作為主要帳戶持有者，您有權授予其他[!DNL Commerce]帳戶持有者的有限存取權。 共用的存取權可以撤銷，但無法從一個使用者轉讓給另一個使用者。

[!DNL Commerce]支援團隊沒有該帳戶的存取權，因此無法為您設定共用存取權。 只有具有適當許可權的主要帳戶持有人才能設定共用存取權。 當您共用帳戶存取權時，所有敏感資訊（例如您的帳單歷史記錄或信用卡資訊）都會受到保護，不會提供給其他使用者。

>[!NOTE]
>
>具有共用存取許可權的使用者所採取的所有動作，都是主要帳戶持有者的全權責任。 對於已共用您帳戶存取許可權的使用者所執行的任何動作，Adobe概不負責。

![共用存取設定](./assets/shared-access.png){width="600" zoomable="yes"}

## 設定共用帳戶

1. 開始之前，請先從&#x200B;**新共用存取權受權者**&#x200B;的[!DNL Commerce]帳戶取得下列資訊：

   - 使用者必須已在account.adobe.com註冊帳戶，並透過account.magento.com登入。 如需詳細資訊，請參閱[建立Commerce帳戶](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create#create-a-commerce-account)。
   - `MAGE ID/Account ID (MAG00XXXXXXX)`會顯示在&#x200B;_[!UICONTROL Magento]_標籤的左上角，**登出**連結的正上方。
   - 與帳戶相關聯的`Email`位址。

1. 登入您的[[!DNL Commerce] 帳戶](commerce-account-create.md)。

1. 在左側導覽面板中，按一下&#x200B;**[!UICONTROL Shared Access]**。

1. 按一下&#x200B;**[!UICONTROL Add New User]**。

   ![新增使用者](./assets/shared-access-add.png){width="600" zoomable="yes"}

1. 在[!UICONTROL _New User Information]_底下，執行下列動作：

   - 輸入新使用者的[!DNL Commerce]帳戶中的&#x200B;**[!UICONTROL Account ID]**。
   - 輸入與新使用者的[!DNL Commerce]帳戶相關聯的&#x200B;**[!UICONTROL Email]**&#x200B;位址。

   ![新使用者資訊](./assets/shared-new-user.png){width="600"}

1. 在&#x200B;_[!UICONTROL Shared Information]_底下，執行下列動作：

   - 若要識別共用帳戶，請輸入&#x200B;**[!UICONTROL Share Name]**。 此名稱僅供內部參考，僅供您及共用您帳戶的人檢視。

     最佳實務是使用您的組織名稱做為[!UICONTROL Share Name]。 請勿使用以`CLOUD SHARED ACCESS FROM MAG XYX`開頭的名稱。
   - 如果您想要與新使用者共用您的個人聯絡資訊，請輸入&#x200B;**[!UICONTROL Your Email]**&#x200B;和&#x200B;**[!UICONTROL Your Phone]**。

1. 在&#x200B;_[!UICONTROL Grant Account Permissions]_底下，選取您要共用的每個[!DNL Commerce]產品與服務的核取方塊。

   ![授與帳戶許可權](./assets/shared-permissions.png){width="600"}

1. 按一下&#x200B;**[!UICONTROL Create Shared Access]**。

   新使用者資訊會出現在[共用存取]頁面的&#x200B;_[!UICONTROL Manage Permissions]_區段中，並傳送電子郵件邀請給新使用者，其中包含存取共用帳戶的指示。

   ![管理共用存取許可權](./assets/shared-manage-permissions.png){width="600" zoomable="yes"}

>[!NOTE]
>
>不需要共用對&#x200B;_[!UICONTROL Security Tool]_的存取權 — 任何具有MAGE ID的使用者都可以使用自己的帳戶設定安全性掃描工具。 他們只需要必要的許可權，就能變更網站，並使用[必要的方法](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/security/security-scan)之一來驗證網域的所有權。

## 存取共用帳戶

下列指示是從收到共用帳戶邀請的共用使用者的角度編寫的。

1. 當您收到共用帳戶的邀請時，請依照電子郵件中的指示，登入您自己的[!DNL Commerce]帳戶。

   您帳戶的左側導覽面板有新的&#x200B;_[!UICONTROL Shared with me]_標籤。 右上角的_[!UICONTROL Switch Accounts]_&#x200B;控制項具有`My Account`的選項以及共用帳戶的名稱。

   ![與我共用](./assets/shared-with-me.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >   如果您沒有看到&#x200B;_[!UICONTROL Switch Accounts]_控制項，請連絡主要帳戶持有者，並確認他們已輸入正確的[帳戶資訊](#set-up-a-shared-account)。


1. 若要存取共用帳戶，請將&#x200B;**[!UICONTROL Switch Accounts]**&#x200B;設為共用帳戶的名稱。

   ![切換到共用帳戶](./assets/shared-switch.png){width="600" zoomable="yes"}

   共用帳戶會顯示歡迎訊息和連絡資訊。 左側導覽面板僅包含您有權使用的專案。

1. 若要將共用帳戶連線到說明中心，請按一下共用帳戶左側導覽面板中的&#x200B;**[!UICONTROL Support]**。

   ![支援](./assets/shared-support.png){width="600" zoomable="yes"}

   您可以使用共用帳戶中的[Adobe Commerce說明中心](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/overview)來搜尋文章和疑難排解資訊、尋找已知問題的修補程式，以及建立支援票證。

   >[!NOTE]
   >
   >收到共用存取許可權後，使用者必須登入其[[!DNL Commerce] 帳戶](https://account.magento.com/customer/account/login)，瀏覽至&#x200B;_共用存取許可權_，然後按一下&#x200B;**[!UICONTROL Support]**&#x200B;索引標籤。 第一次需要此動作時，只是為了確保[Adobe Commerce支援知識庫](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/overview)已透過`SSO`呼叫正確設定。

1. 若要返回您自己的帳戶，請在瀏覽器控制項中按一下&#x200B;**上一步**，並將&#x200B;**[!UICONTROL Switch Accounts]**&#x200B;設為`My Account`。

## 撤銷共用存取權

1. 登入您的Commerce帳戶。

1. 在左側導覽面板中，按一下&#x200B;**[!UICONTROL Shared Access]**。

1. 尋找要在&#x200B;_[!UICONTROL Managing Users & Permissions]_下撤銷的帳戶，然後按一下&#x200B;**[!UICONTROL Delete]**。

   >[!NOTE]
   >
   > 如果未顯示&#x200B;**[!UICONTROL Delete]**，請檢查&#x200B;**[!UICONTROL Share Name]**&#x200B;是否以`Cloud Shared Access from MAG XYZ`開頭。 您無法刪除具有該[命名模式](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#remove-cloud-shared-access-users)的帳號。
   > 
   > 若是如此，請要求帳戶擁有者修改共用存取帳戶，以清除帳戶許可權。 更新後，使用者無法存取任何帳戶資源。
   >
   > 此外，請確定已將使用者從專案移除，這樣他們就不會再收到電子郵件通知： [前團隊成員會收到Adobe Commerce雲端通知電子郵件](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/former-teammembers-receive-cloud-notification-emails)


1. 提示確認時，按一下&#x200B;**[!UICONTROL Delete User]**。

>[!NOTE]
>
>您無法在此介面中從MAG[XYZ ]_刪除共用名稱為_&#x200B;雲端共用存取的使用者。 請參閱[如何刪除透過雲端專案被授予共用存取許可權的使用者？](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/shared-access-troubleshooting)。

## 相關閱讀

[共用存取疑難排解](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/shared-access-troubleshooting)
