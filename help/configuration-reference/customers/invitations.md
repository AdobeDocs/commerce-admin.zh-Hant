---
title: '[!UICONTROL Customers] > [!UICONTROL Invitations]'
description: 檢閱Commerce管理員的[!UICONTROL Customers] &gt； [!UICONTROL Invitations]頁面上的組態設定。
exl-id: edafeaed-9c4f-4d9f-b35c-381ae5f43b67
feature: Configuration, Promotions/Events
TQID: https://experienceleague.adobe.com/UOJF8r7CsXWK6qG7FjkJoJTIqnH2fPQhnRyZrJ7u4nE
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 250
ht-degree: 1%

---

# [!UICONTROL Customers] > [!UICONTROL Invitations]

{{ee-feature}}

{{config}}

## [!UICONTROL General]

![一般](./assets/invitations-general.png)<!-- zoom -->

<!-- [General](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/events/invitations#enable-invitations-for-your-store) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable Invitations Functionality] | 全域 | 決定是否啟用邀請模組。 選項： `Yes` / `No` |
| [!UICONTROL Enable Invitations on Frontend] | 網站 | 決定是否可以從店面管理邀請。 選項： `Yes` / `No` |
| [!UICONTROL Referred Customer Group] | 存放區檢視 | 決定受邀者的客戶群組。 選項： <br/>**`Same as Inviter`**— 受邀者會自動指派給邀請他們的客戶群組。<br/>**`Default Customer Group from Configuration`** — 受邀者會自動擁有預設的[客戶群組](../../customers/customer-groups.md)。 |
| [!UICONTROL New Accounts Registration] | 存放區檢視 | 決定受邀者如何建立帳戶。 選項： <br/>**`By Invitation Only`**— 受邀者必須遵循邀請電子郵件中的連結來建立帳戶。<br/>**`Available to All`** — 受邀者可以使用商店提供的帳戶登錄檔。 |
| [!UICONTROL Allow Customers to Add Custom Message to Invitation Email] | 存放區檢視 | 決定邀請表單中是否有欄位邀請者可新增透過電子郵件傳送給邀請者的自訂訊息。 這不會影響管理員新增訊息至邀請的功能。 選項： `Yes` / `No`。 |
| [!UICONTROL Max Invitations Allowed to be Sent at One Time] | 存放區檢視 | 決定邀請者一次可傳送的最大邀請數量。 系統會傳送不同的邀請給邀請者在表單中包含的每個電子郵件地址。 這可以防止一次傳送大量邀請，並會降低邀請以垃圾訊息傳送的可能性，藉此保護伺服器資源。 |

{style="table-layout:auto"}

## [!UICONTROL Email]

![電子郵件](./assets/invitations-email.png)<!-- zoom -->

<!-- [Email](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/events/invitations#enable-invitations-for-your-store) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Customer Invitation Email Sender] | 存放區檢視 | 決定受邀者在傳送邀請電子郵件時收到之電子郵件的寄件者。 預設值： `General Contact` |
| [!UICONTROL Customer Invitation Email Template] | 存放區檢視 | 決定受邀者在傳送邀請電子郵件時所收到電子郵件的範本。 預設範本： `Customer Invitation` |

{style="table-layout:auto"}
