---
title: 重設客戶密碼
description: 客戶通常會從店面重設密碼，但店面管理員可以從管理員起始密碼重設或強制登入。
exl-id: bca1ef3e-2bc6-4146-ac86-d6c58c8995e4
feature: Customers, Configuration, Security
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# 重設客戶密碼

客戶通常按一下&#x200B;_[!UICONTROL Forgot Your Password?]_從店面重設密碼。 不過，存放區管理員可以從管理員起始密碼重設或強制登入。

| 函式 | 說明 |
| --- | --- |
| 重設密碼 | 密碼重設電子郵件會直接傳送至客戶的電子郵件帳戶。 存放區管理員無法取得客戶密碼的存取權。 |
| 強制登入 | 撤銷與客戶帳戶相關聯的OAuth存取權杖。 這只能用於已指派OAuth權杖的客戶帳戶，做為網頁API [整合](../systems/integrations.md)的一部分。 若要深入瞭解，請參閱開發人員檔案中的[OAuth驗證](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/)。 <br/><br/>從店面或管理員建立的標準客戶帳戶沒有OAuth權杖。 |

{style="table-layout:auto"}

## 從店面重設密碼

1. 客戶在登入頁面上按一下&#x200B;**[!UICONTROL Forgot Your Password?]**。

1. 出現提示時，輸入與其帳戶相關聯的&#x200B;**[!UICONTROL Email Address]**，然後按一下&#x200B;**[!UICONTROL Reset My Password]**。

   ![忘記密碼](assets/forgot-password.png){width="600" zoomable="yes"}

   >[!INFO]
   >
   >如果輸入的電子郵件地址與帳戶相關聯的地址相符，則客戶會收到「密碼重設確認」電子郵件，其中包含重設密碼的連結。

1. 當電子郵件到達時，客戶按一下&#x200B;_重設密碼_&#x200B;連結，然後在提示時輸入其&#x200B;**[!UICONTROL New Password]**。

1. 再次輸入以進行確認並按一下&#x200B;**[!UICONTROL Reset Password]**。

   >[!IMPORTANT]
   >
   >新密碼的長度必須是6個或6個以上的字元，不含空格。 當他們收到密碼已更新的確認時，他們可以使用新密碼登入他們的帳戶。 依預設，_重設密碼_&#x200B;連結的有效期間為24小時。

## 從管理員重設密碼

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL All Customers]**。

1. 在網格中尋找客戶帳戶，然後按一下&#x200B;_動作_&#x200B;欄中的&#x200B;**[!UICONTROL Edit]**。

1. 在頁面頂端的選項組中，按一下&#x200B;**[!UICONTROL Reset Password]**。

   在[組態](../configuration-reference/customers/customer-configuration.md)主題中設定了一小時內允許的密碼重設要求數目。

## 撤銷客戶的OAuth權杖

>[!IMPORTANT]
>
>除非您完全瞭解API驗證，否則請勿繼續。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL All Customers]**。

1. 在網格中尋找客戶帳戶，然後按一下&#x200B;_動作_&#x200B;欄中的&#x200B;**[!UICONTROL Edit]**。

1. 在頁面頂端的選項組中，按一下&#x200B;**[!UICONTROL Force Sign In]**。

1. 提示確認時，按一下&#x200B;**確定**。
