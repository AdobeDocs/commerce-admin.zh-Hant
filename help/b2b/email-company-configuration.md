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

依預設，指派為公司主要連絡人的[銷售代表](account-company-manage.md)會設定為許多傳送給公司的自動化電子郵件訊息的寄件者。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Customers]**&#x200B;並選擇&#x200B;**[!UICONTROL Company Configuration]**。

1. 如有必要，請將&#x200B;**[!UICONTROL Store View]**&#x200B;設定為存放區檢視以定義設定的[範圍](../getting-started/websites-stores-views.md#scope-settings)。

1. 完成&#x200B;**[!UICONTROL Company Registration]**&#x200B;區段：

   >[!NOTE]
   >
   >清除&#x200B;**[!UICONTROL Use system value]**&#x200B;核取方塊，讓欄位可編輯。

   - 將&#x200B;**[!UICONTROL Company Registration Email Recipient]**&#x200B;設定為[商店連絡人](../getting-started/store-details.md#store-email-addresses)，當收到新的公司註冊要求時，會通知該連絡人。

   - 在&#x200B;**[!UICONTROL Send Company Registration Email Copy To]**&#x200B;欄位中，輸入每個要接收註冊通知副本的人的電子郵件地址。 請使用逗號分隔多個電子郵件地址。

   - 若要判斷通知復本的傳送方式，請將&#x200B;**[!UICONTROL Send Email Copy Method]**&#x200B;設定為下列其中一項：

      - `Bcc` — 在傳送給客戶的同一封電子郵件的標頭中包含收件者，以傳送&#x200B;_不公開的禮貌副本_。 客戶看不到密件副本收件者。
      - `Separate Email` — 以個別電子郵件的形式傳送復本。

   - 如果您已準備要使用的電子郵件範本而非預設值，請將&#x200B;**[!UICONTROL Default Company Registration Email]**&#x200B;設定為範本的名稱。 依預設，會使用`Company Registration Request`範本。

     ![客戶組態 — 公司註冊](./assets/company-email-options-company-registration.png){width="600" zoomable="yes"}

1. 完成&#x200B;**[!UICONTROL Customer-Related Emails]**&#x200B;區段：

   如果您已準備要使用的替代電子郵件範本而非預設值，請選擇您要在下列各專案中使用的範本：

   - **[!UICONTROL Default 'Sales Rep Assigned' Email]**
   - **[!UICONTROL Default 'Assign Company to Customer' Email]**
   - **[!UICONTROL Default 'Assign Company Admin' Email]**
   - **[!UICONTROL Default 'Company Admin Inactive' Email]**
   - **[!UICONTROL Default 'Company Admin Changed to Member' Email]**
   - **[!UICONTROL Default 'Customer Status Active' Email]**
   - **[!UICONTROL Default 'Customer Status Inactive' Email]**

   ![客戶組態 — 客戶相關電子郵件](./assets/company-email-options-customer-related-emails.png){width="600" zoomable="yes"}

1. 完成&#x200B;**[!UICONTROL Company Status Change]**&#x200B;區段：

   - 將&#x200B;**[!UICONTROL Company Status Change for Email Recipient]**&#x200B;設定為[商店連絡人](../getting-started/store-details.md#store-email-addresses)，當公司狀態變更時，會通知該連絡人。

   - 在&#x200B;**[!UICONTROL Send Company Status Change Email Copy To]**&#x200B;欄位中，輸入每個要接收狀態變更通知副本之人員的電子郵件地址。 請使用逗號分隔多個電子郵件地址。

   - 若要判斷通知復本的傳送方式，請將&#x200B;**[!UICONTROL Send Email Copy Method]**&#x200B;設定為下列其中一項：

      - `Bcc` — 在傳送給客戶的同一封電子郵件的標頭中包含收件者，以傳送&#x200B;_不公開的禮貌副本_。 客戶看不到密件副本收件者。
      - `Separate Email` — 以個別電子郵件的形式傳送復本。

   - 如果您有準備好的電子郵件範本，當公司狀態從`Pending Approval`變更為`Active`時，會使用這個範本，而非預設值，請將&#x200B;**[!UICONTROL Default 'Company Status Change to Active 1' Email]**&#x200B;設定為該範本。 依預設，會使用`Company Status Active 1`範本。

   - 如果您有準備好的電子郵件範本，當公司狀態從`Rejected`或`Blocked`變更為`Active`時，會使用這個範本，而非預設值，請將&#x200B;**[!UICONTROL Default 'Company Status Change to Active 2' Email]**&#x200B;設定為該範本。 依預設，會使用`Company Status Active 2`範本。

   - 如果您有準備好的電子郵件範本，當公司狀態變更為`Rejected`時，會使用這個範本，而非預設值，請將&#x200B;**[!UICONTROL Default 'Company Status Change to Rejected' Email]**&#x200B;設定為該範本。 依預設，會使用`Company Status Rejected`範本。

   - 如果您有準備好的電子郵件範本，當公司狀態變更為`Blocked`時，會使用這個範本，而非預設值，請將&#x200B;**[!UICONTROL Default 'Company Status Change to Blocked' Email]**&#x200B;設定為該範本。 依預設，會使用`Company Status Blocked`範本。

   - 如果您有準備好的電子郵件範本，當公司狀態變更為`Pending Approval`時，會使用這個範本，而非預設值，請將&#x200B;**[!UICONTROL Default 'Company Status Change to Pending Approval' Email]**&#x200B;設定為該範本。 依預設，會使用`Company Status Pending Approval`範本。

     ![客戶組態 — 公司狀態變更](./assets/company-email-options-company-status-change.png){width="600" zoomable="yes"}

1. 完成&#x200B;**[!UICONTROL Company Credit Emails]**&#x200B;區段：

   - 將&#x200B;**[!UICONTROL Company Credit Change Email Sender]**&#x200B;設定為[商店聯絡人](../getting-started/store-details.md#store-email-addresses)，當指派給公司的信用額度發生變更時，將會通知該聯絡人。 依預設，通知會傳送給&#x200B;_銷售代表_。

   - 在&#x200B;**[!UICONTROL Send Company Credit Change Email Copy To]**&#x200B;欄位中，輸入每個要接收信用變更通知復本之人員的電子郵件地址。 請使用逗號分隔多個電子郵件地址。

   - 若要判斷通知復本的傳送方式，請將&#x200B;**[!UICONTROL Send Email Copy Method]**&#x200B;設定為下列其中一項：

      - `Bcc` — 在傳送給客戶的同一封電子郵件的標頭中包含收件者，以傳送&#x200B;_不公開的禮貌副本_。 客戶看不到密件副本收件者。
      - `Separate Email` — 以個別電子郵件的形式傳送復本。

   - 如果您已準備要使用的電子郵件範本而非預設值，請為傳送給公司管理員的下列每個通知選擇範本。

      - **[!UICONTROL Allocated Email Template]**
      - **[!UICONTROL Updated Email Template]**
      - **[!UICONTROL Reimbursed Email Template]**
      - **[!UICONTROL Refunded Email Template]**
      - **[!UICONTROL Reverted Email Template]**

   ![客戶組態 — 公司信用電子郵件](./assets/company-email-options-company-credit.png){width="600" zoomable="yes"}

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。
