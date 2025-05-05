---
title: '[!UICONTROL Customers] &amp；gt； [!UICONTROL Company Configuration]'
description: 檢閱Commerce管理員的[!UICONTROL Customers] &amp；gt； [!UICONTROL Company Configuration]頁面上的組態設定。
exl-id: 330eabeb-edab-4a9f-968e-37d0b95cdedb
feature: Configuration, Companies
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Company Configuration]

{{b2b-feature}}

{{config}}

>[!TIP]
>
>在安裝及啟用Adobe Commerce B2B後，即可使用公司專屬的功能個人化購買體驗。 Adobe Commerce B2B是整合式解決方案，可支援B2B和B2C模型。 如需B2B功能的詳細資訊，請參閱[Adobe Commerce B2B使用手冊](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=zh-Hant)。

>[!NOTE]
>
>B2B功能的這些組態選項存取權是由[角色資源](../../systems/permissions-user-roles.md#role-resources)所控制。 必須為指派給管理員使用者的使用者角色設定這些角色資源。

如需有關設定這些設定的詳細資訊，請參閱&#x200B;_Adobe Commerce B2B使用手冊_&#x200B;中的[啟用基本B2B功能](../../b2b/enable-basic-features.md)。

## [!UICONTROL General]

![一般](./assets/company-general.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Allow Company Registration from the Storefront] | 網站 | 決定您商店的訪客是否可以選擇為公司帳戶或個人帳戶[註冊](../../customers/customer-sign-in.md)。 選項： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Email Options - Company Registration]

![電子郵件選項 — 公司註冊](./assets/company-email-options-company-registration.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Company Registration Email Recipient] | 存放區檢視 | 從店面提交公司註冊請求時通知的店舖聯絡人。 選項： `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Send Company Registration Email Copy To] | 存放區檢視 | 每個將收到註冊通知副本的人的電子郵件地址。 請使用逗號分隔多個電子郵件地址。 |
| [!UICONTROL Send Email Copy Method] | 存放區檢視 | 用來傳送註冊電子郵件副本的電子郵件方法。 選項： `Bcc` / `Separate Email` |
| [!UICONTROL Default Company Registration Email] | 存放區檢視 | 預設用於公司註冊通知的電子郵件範本。 預設範本： `Company Registration Request` |

{style="table-layout:auto"}

## [!UICONTROL Customer-Related Emails]

![客戶相關電子郵件](./assets/company-email-options-customer-related-emails.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Default 'Sales Rep Assigned' Email] | 存放區檢視 | 將銷售代表指派給公司帳戶時，預設會使用的電子郵件範本。 此電子郵件會傳送給銷售代表及公司管理員。 預設範本： `Sales Representative Assigned to Company` |
| [!UICONTROL Default 'Assign Company to Customer' Email] | 存放區檢視 | 將個別客戶帳戶指派給公司帳戶時，預設會使用的電子郵件範本。 此電子郵件僅傳送給客戶。 預設範本： `Assign Company to Customer` |
| [!UICONTROL Default 'Assign Company Admin' Email] | 存放區檢視 | 將公司管理員指派給公司時使用的電子郵件範本。 此電子郵件會傳送給銷售代表及公司管理員。 預設範本： `Assign Company Admin` |
| [!UICONTROL Default 'Company Admin Inactive' Email] | 存放區檢視 | 作為公司管理員的人員狀態變更為「非使用中」時，預設使用的電子郵件範本。 系統會將變更的電子郵件通知傳送給新的和以前的公司管理員。 預設範本： `Company Admin Set Inactive` |
| [!UICONTROL Default 'Company Admin Changed to Member' Email] | 存放區檢視 | 當前公司管理員成為公司成員時，預設會使用的電子郵件範本。 電子郵件只會傳送給公司成員。 預設範本： `Company Admin Changed to Member` |
| [!UICONTROL Default 'Customer Status Active' Email] | 存放區檢視 | 客戶的狀態變為使用中時，預設會使用的電子郵件範本。 此電子郵件僅傳送給客戶。 預設範本： `Customer Status Active` |
| [!UICONTROL Default 'Customer Status Inactive' Email] | 存放區檢視 | 當客戶的狀態變為非使用中時，預設會使用的電子郵件範本。 此電子郵件僅傳送給客戶。 預設範本： `Customer Status Inactive` |

{style="table-layout:auto"}

## [!UICONTROL Company Status Change]

![公司狀態變更](./assets/company-email-options-company-status-change.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Company Status Change Email Recipient] | 存放區檢視 | 公司狀態變更時收到通知的商店聯絡人。 選項： `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Send Company Status Change Email Copy To] | 存放區檢視 | 每個將收到公司狀態變更通知副本的人員的電子郵件地址。 請使用逗號分隔多個電子郵件地址。 |
| [!UICONTROL Send Email Copy Method] | 存放區檢視 | 用來傳送狀態變更通知復本的電子郵件方法。 選項： `Bcc` / `Separate Email` |
| [!UICONTROL Default "Company Status Change to Active 1' Email] | 存放區檢視 | 當公司狀態從&#x200B;_未決核准_&#x200B;變更為&#x200B;_作用中_&#x200B;時所使用的電子郵件範本。 預設範本： `Company Status Active 1` |
| [!UICONTROL Default 'Company Status Change to Active 2' Email] | 存放區檢視 | 當公司的狀態從&#x200B;_已拒絕_&#x200B;或&#x200B;_已封鎖_&#x200B;變更為&#x200B;_使用中_&#x200B;時，預設會使用的電子郵件範本。 預設範本： `Company Status Active 2` |
| [!UICONTROL Default 'Company Status Change to Rejected' Email] | 存放區檢視 | 公司狀態變更為&#x200B;_已拒絕_&#x200B;時，預設使用的電子郵件範本。 預設範本： `Company Status Rejected` |
| [!UICONTROL Default 'Company Status Change to Blocked' Email] | 存放區檢視 | 公司狀態變更為&#x200B;_已封鎖_&#x200B;時，預設使用的電子郵件範本。 預設範本： `Company Status Blocked` |
| [!UICONTROL Default 'Company Status Change to Pending Approval' Email] | 存放區檢視 | 當公司的狀態變更為&#x200B;_未決核准_&#x200B;時，預設會使用的電子郵件範本。 預設範本： `Company Status Pending Approval` |

{style="table-layout:auto"}

## [!UICONTROL Company Credit]

![公司點數](./assets/company-email-options-company-credit.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Company Credit Change Email Sender] | 存放區檢視 | 公司信用發生變更時收到通知的商店聯絡人。 選項： `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Send Company Credit Change Email Copy To] | 存放區檢視 | 每一位將收到公司信用變更通知副本的人員電子郵件地址。 請使用逗號分隔多個電子郵件地址。 |
| [!UICONTROL Send Email Copy Method] | 存放區檢視 | 用來傳送信用變更通知復本的電子郵件方法。 選項： `Bcc` / `Separate Email` |
| [!UICONTROL Allocated Email Template] | 存放區檢視 | 分配公司業績時預設使用的電子郵件範本。 此電子郵件會傳送給公司管理員。 預設範本： `Credit Limit Allocated` |
| [!UICONTROL Updated Email Template] | 存放區檢視 | 更新公司的信用額度時，預設會使用的電子郵件範本。 此電子郵件會傳送給公司管理員。 預設範本： `Credit Limit Updated` |
| [!UICONTROL Reimbursed Email Template] | 存放區檢視 | 當公司獲得[退款](../../b2b/credit-company.md#apply-a-payment-to-a-company-account)時，預設會使用的電子郵件範本。 此電子郵件會傳送給公司管理員。 預設範本： `Credit Reimbursed` |
| [!UICONTROL Refunded Email Template] | 存放區檢視 | 將訂單中的金額退款給公司銷退折讓時，預設會使用的電子郵件範本。 此電子郵件會傳送給公司管理員。 預設範本： `Order Refunded to Company Credit` |
| [!UICONTROL Reverted Email Template] | 存放區檢視 | 將訂單恢復為公司信用時預設使用的電子郵件範本。 此電子郵件會傳送給公司管理員。 預設範本： `Order Reverted to Company Credit` |

{style="table-layout:auto"}
