---
title: 設定公司電子郵件
description: 瞭解用於為公司帳戶傳送通訊的電子郵件選項和範本。
exl-id: fd61c0c6-0887-4ff2-8002-906ff615bad9
feature: B2B, Companies, Configuration
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '676'
ht-degree: 0%

---

# 設定公司電子郵件選項

此 [銷售代表](account-company-manage.md) 根據預設，該帳戶會設定為公司的主要聯絡人，以作為許多傳送給公司的自動化電子郵件訊息的寄件者。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Customers]** 並選擇 **[!UICONTROL Company Configuration]**.

1. 如有必要，請設定 **[!UICONTROL Store View]** 至商店檢視以定義 [範圍](../getting-started/websites-stores-views.md#scope-settings) 設定的。

1. 完成 **[!UICONTROL Company Registration]** 區段：

   >[!NOTE]
   >
   >清除 **[!UICONTROL Use system value]** 核取方塊，讓欄位可編輯。

   - 設定 **[!UICONTROL Company Registration Email Recipient]** 至 [商店聯絡人](../getting-started/store-details.md#store-email-addresses) 當收到新的公司註冊要求時，會通知誰。

   - 在 **[!UICONTROL Send Company Registration Email Copy To]** 欄位中，輸入每個要接收註冊通知副本之人員的電子郵件地址。 請使用逗號分隔多個電子郵件地址。

   - 若要確定通知副本的傳送方式，請設定 **[!UICONTROL Send Email Copy Method]** 變更為下列其中一項：

      - `Bcc`  — 傳送 _盲文提供_ 在傳送給客戶的相同電子郵件的標題中包含收件者。 客戶看不到密件副本收件者。
      - `Separate Email`  — 以個別電子郵件的形式傳送副本。

   - 如果您已準備要使用的電子郵件範本，而非預設值，請設定 **[!UICONTROL Default Company Registration Email]** 至範本的名稱。 根據預設， `Company Registration Request` 範本已使用。

     ![客戶組態 — 公司註冊](./assets/company-email-options-company-registration.png){width="600" zoomable="yes"}

1. 完成 **[!UICONTROL Customer-Related Emails]** 區段：

   如果您已準備要使用的替代電子郵件範本而非預設值，請選擇您要在下列各專案中使用的範本：

   - **[!UICONTROL Default 'Sales Rep Assigned' Email]**
   - **[!UICONTROL Default 'Assign Company to Customer' Email]**
   - **[!UICONTROL Default 'Assign Company Admin' Email]**
   - **[!UICONTROL Default 'Company Admin Inactive' Email]**
   - **[!UICONTROL Default 'Company Admin Changed to Member' Email]**
   - **[!UICONTROL Default 'Customer Status Active' Email]**
   - **[!UICONTROL Default 'Customer Status Inactive' Email]**

   ![客戶設定 — 客戶相關電子郵件](./assets/company-email-options-customer-related-emails.png){width="600" zoomable="yes"}

1. 完成 **[!UICONTROL Company Status Change]** 區段：

   - 設定 **[!UICONTROL Company Status Change for Email Recipient]** 至 [商店聯絡人](../getting-started/store-details.md#store-email-addresses) 當公司狀態變更時，會通知誰。

   - 在 **[!UICONTROL Send Company Status Change Email Copy To]** 欄位中，輸入每個要接收狀態變更通知復本之人員的電子郵件地址。 請使用逗號分隔多個電子郵件地址。

   - 若要確定通知副本的傳送方式，請設定 **[!UICONTROL Send Email Copy Method]** 變更為下列其中一項：

      - `Bcc`  — 傳送 _盲文提供_ 在傳送給客戶的相同電子郵件的標題中包含收件者。 客戶看不到密件副本收件者。
      - `Separate Email`  — 以個別電子郵件的形式傳送副本。

   - 如果您有準備好的電子郵件範本，則在公司狀態從變更時，會使用這個範本而非預設值 `Pending Approval` 至 `Active`，設定 **[!UICONTROL Default 'Company Status Change to Active 1' Email]** 至該範本。 根據預設， `Company Status Active 1` 範本已使用。

   - 如果您有準備好的電子郵件範本，則在公司狀態從變更時，會使用這個範本而非預設值 `Rejected` 或 `Blocked` 至 `Active`，設定 **[!UICONTROL Default 'Company Status Change to Active 2' Email]** 至該範本。 根據預設， `Company Status Active 2` 範本已使用。

   - 如果您有準備好的電子郵件範本，將會在公司狀態變更為時使用，而非預設值 `Rejected`，設定 **[!UICONTROL Default 'Company Status Change to Rejected' Email]** 至該範本。 根據預設， `Company Status Rejected` 範本已使用。

   - 如果您有準備好的電子郵件範本，將會在公司狀態變更為時使用，而非預設值 `Blocked`，設定 **[!UICONTROL Default 'Company Status Change to Blocked' Email]** 至該範本。 根據預設， `Company Status Blocked` 範本已使用。

   - 如果您有準備好的電子郵件範本，將會在公司狀態變更為時使用，而非預設值 `Pending Approval`，設定 **[!UICONTROL Default 'Company Status Change to Pending Approval' Email]** 至該範本。 根據預設， `Company Status Pending Approval` 範本已使用。

     ![客戶組態 — 公司狀態變更](./assets/company-email-options-company-status-change.png){width="600" zoomable="yes"}

1. 完成 **[!UICONTROL Company Credit Emails]** 區段：

   - 設定 **[!UICONTROL Company Credit Change Email Sender]** 至 [商店聯絡人](../getting-started/store-details.md#store-email-addresses) 當指定給公司的信用額度發生變更時，會通知誰。 依預設，通知會傳送至 _銷售代表_.

   - 在 **[!UICONTROL Send Company Credit Change Email Copy To]** 欄位，輸入每個要接收信用變更通知復本之人員的電子郵件地址。 請使用逗號分隔多個電子郵件地址。

   - 若要確定通知副本的傳送方式，請設定 **[!UICONTROL Send Email Copy Method]** 變更為下列其中一項：

      - `Bcc`  — 傳送 _盲文提供_ 在傳送給客戶的相同電子郵件的標題中包含收件者。 客戶看不到密件副本收件者。
      - `Separate Email`  — 以個別電子郵件的形式傳送副本。

   - 如果您已準備要使用的電子郵件範本而非預設值，請為傳送給公司管理員的下列每個通知選擇範本。

      - **[!UICONTROL Allocated Email Template]**
      - **[!UICONTROL Updated Email Template]**
      - **[!UICONTROL Reimbursed Email Template]**
      - **[!UICONTROL Refunded Email Template]**
      - **[!UICONTROL Reverted Email Template]**

   ![客戶設定 — 公司信用電子郵件](./assets/company-email-options-company-credit.png){width="600" zoomable="yes"}

1. 完成後，按一下 **[!UICONTROL Save Config]**.
