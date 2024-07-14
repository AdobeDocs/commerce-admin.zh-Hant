---
title: '[!UICONTROL Customers] &amp；gt； [!UICONTROL Invitations]'
description: 檢閱Commerce管理員的[!UICONTROL Customers] &amp；gt； [!UICONTROL Invitations]頁面上的組態設定。
exl-id: edafeaed-9c4f-4d9f-b35c-381ae5f43b67
feature: Configuration, Promotions/Events
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Invitations]

{{ee-feature}}

{{config}}

## [!UICONTROL General]

![一般](./assets/invitations-general.png)<!-- zoom -->

<!-- [General](https://docs.magento.com/user-guide/marketing/invitations-configure.html) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable Invitations Functionality] | 全域 | 決定是否啟用邀請模組。 選項： `Yes` / `No` |
| [!UICONTROL Enable Invitations on Frontend] | 網站 | 決定是否可以從店面管理邀請。 選項： `Yes` / `No` |
| [!UICONTROL Referred Customer Group] | 存放區檢視 | 決定受邀者的客戶群組。 選項： <br/>**`Same as Inviter`**— 受邀者會自動指派給邀請他們的客戶群組。<br/>**`Default Customer Group from Configuration`** — 受邀者會自動擁有預設的[客戶群組](../../customers/customer-groups.md)。 |
| [!UICONTROL New Accounts Registration] | 存放區檢視 | 決定受邀者如何建立帳戶。 選項： <br/>**`By Invitation Only`**— 受邀者必須遵循邀請電子郵件中的連結來建立帳戶。<br/>**`Available to All`** — 受邀者可以使用商店中提供的帳戶登錄檔單。 |
| [!UICONTROL Allow Customers to Add Custom Message to Invitation Email] | 存放區檢視 | 決定邀請表單中是否有欄位邀請者可新增透過電子郵件傳送給邀請者的自訂訊息。 這不會影響管理員新增訊息至邀請的功能。 選項： `Yes` / `No`。 |
| [!UICONTROL Max Invitations Allowed to be Sent at One Time] | 存放區檢視 | 決定邀請者一次可傳送的最大邀請數量。 系統會傳送不同的邀請給邀請者在表單中包含的每個電子郵件地址。 這可以防止一次傳送大量邀請，並會降低邀請以垃圾訊息傳送的可能性，藉此保護伺服器資源。 |

{style="table-layout:auto"}

## [!UICONTROL Email]

![電子郵件](./assets/invitations-email.png)<!-- zoom -->

<!-- [Email](https://docs.magento.com/user-guide/marketing/invitations-configure.html) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Customer Invitation Email Sender] | 存放區檢視 | 決定受邀者在傳送邀請電子郵件時收到之電子郵件的寄件者。 預設值： `General Contact` |
| [!UICONTROL Customer Invitation Email Template] | 存放區檢視 | 決定受邀者在傳送邀請電子郵件時所收到電子郵件的範本。 預設範本： `Customer Invitation` |

{style="table-layout:auto"}
