---
title: '[!UICONTROL Catalog] &amp；gt； [!UICONTROL Email to a Friend]'
description: 檢閱Commerce管理員的[!UICONTROL Catalog] &amp；gt； [!UICONTROL Email to a Friend]頁面上的組態設定。
exl-id: cd1e3a8d-14ce-47e9-a3bc-c1b1dcbe0d8c
feature: Configuration, Communications
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---

# [!UICONTROL Catalog] > [!UICONTROL Email to a Friend]

{{config}}

## [!UICONTROL Email Templates]

![電子郵件範本](./assets/email-to-a-friend-email-templates.png)<!-- zoom -->

<!-- [Email Templates](https://docs.magento.com/user-guide/marketing/email-template-configuration.html) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 存放區檢視 | 啟用程式，讓客戶能夠傳送電子郵件給朋友，瞭解您商店中的產品。 選項： `Yes` / `No` |
| [!UICONTROL Select Email Template] | 存放區檢視 | 識別由&#x200B;_傳送電子郵件給Friend_&#x200B;函式產生的郵件所使用的電子郵件範本。 預設範本： `Send Product to Friend` |
| [!UICONTROL Allow for Guests] | 存放區檢視 | 判斷寄件者是否必須是註冊客戶，才能傳送產品相關電子郵件給朋友。 選項： `Yes` / `No` |
| [!UICONTROL Max Recipients] | 存放區檢視 | 限制單一電子郵件通訊群組清單中的人數。 |
| [!UICONTROL Max Products Sent in 1  Hour] | 存放區檢視 | 限制單一使用者在一小時期間內可共用的產品數量。 |
| [!UICONTROL Limit Sending By] | 存放區檢視 | 決定用來識別傳送者的方法。 選項包括： <br/>**`IP Address`**- （建議）依據用來傳送產品電子郵件之電腦的IP位址識別寄件者。<br/>**`Cookie (unsafe)`** — 透過瀏覽器Cookie識別寄件者。 此方法不安全，因為使用者可以刪除Cookie以避免限制。 |

{style="table-layout:auto"}
