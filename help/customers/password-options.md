---
title: 客戶密碼選項
description: 客戶密碼選項會決定商店中各種面向客戶的功能的安全性等級。
exl-id: 84dec8e8-3363-4133-bbcc-9e58467749c4
feature: Customers, Configuration, Security
source-git-commit: ea9eeea0fc5213de2787e0b7ea2aed825ca3a9de
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# 客戶密碼選項

客戶密碼選項決定用於密碼重設請求的安全性等級、用於客戶通知的電子郵件範本，以及密碼復原連結的存留期。 您可以允許客戶變更自己的密碼，或要求只有商店管理員才能這麼做。

## 設定客戶密碼選項

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Customers]** 並選擇 **[!UICONTROL Customer Configuration]**.

1. 展開 **[!UICONTROL Password Options]** 區段。

   ![密碼選項](../configuration-reference/customers/assets/customer-configuration-password-options.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Password Reset Protection Type]** 若要使用檢查密碼重設要求的方法：

   - `By IP and Email`  — 檢查先前是否嘗試重設特定電子郵件或特定IP的密碼。
   - `By IP`  — 檢查先前是否嘗試從特定IP重設密碼。
   - `By Email`  — 檢查先前是否嘗試重設特定電子郵件的密碼。
   - `None`  — 已停用保護（重設密碼沒有限制）。

   此 **[!UICONTROL Max Number of Password Reset Requests]** 和 **[!UICONTROL Min Time Between Password Reset Requests]** 會根據此設定進行計算。

1. 若要限制每小時傳送的密碼重設要求數目，請執行下列動作：

   - 的 **[!UICONTROL Max Number of Password Reset Requests]**，輸入每小時可傳送的密碼重設要求數上限。

   - 的 **[!UICONTROL Min Time Between Password Reset Requests]**，輸入兩次請求之間必須經過的最小分鐘數。

1. 若要設定密碼重設電子郵件通知，請執行下列動作：

   - 設定 **[!UICONTROL Forgot Email Template]** 用於傳送給忘記密碼之客戶的電子郵件的範本。

   - 設定 **[!UICONTROL Remind Email Template]** 重新設定為管理員使用者重設客戶密碼時使用的範本。

   - 設定 **[!UICONTROL Reset Password Template]** 變更為客戶變更密碼時所使用的範本。

   - 設定 **[!UICONTROL Password Template Email Sender]** 至 [商店聯絡人](../getting-started/store-details.md) 以密碼相關通知的寄件者身分顯示。

1. 完成下列密碼重設安全性選項：

   - 的 **[!UICONTROL Recovery Link Expiration Period (hours)]**，輸入密碼復原連結到期前的小時數。

   - 如果您希望客戶登入和忘記密碼表單中的欄位自動填寫先前輸入項，請設定 **[!UICONTROL Enable Autocomplete on login/forgot password forms]** 至 `Yes`.

   - 的 **[!UICONTROL Number of Required Character Classes]**，根據下列字元類別，輸入密碼中必須包含的不同字元型別數目：

      - `Lowercase`
      - `Uppercase`
      - `Numeric`
      - `Special Characters`

   - 的 **[!UICONTROL Maximum Login Failures to Lockout Account]**，輸入在鎖定客戶帳戶之前的失敗登入嘗試次數。 對於不限次數的嘗試，輸入零(`0`)。

   - 的 **[!UICONTROL Minimum Password Length]**，輸入密碼中可以使用的最少字元數。 數字必須大於零。

   - 的 **[!UICONTROL Lockout Time (minutes)]**，輸入客戶帳戶在登入失敗次數太多後遭到鎖定的分鐘數。

1. 完成後，按一下 **[!UICONTROL Save Config]**.
