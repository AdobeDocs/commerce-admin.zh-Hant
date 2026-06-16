---
title: '[!UICONTROL Catalog] > [!UICONTROL Email to a Friend]'
description: 檢閱Commerce管理員的[!UICONTROL Catalog] &gt； [!UICONTROL Email to a Friend]頁面上的組態設定。
exl-id: cd1e3a8d-14ce-47e9-a3bc-c1b1dcbe0d8c
feature: Configuration, Communications
TQID: https://experienceleague.adobe.com/TzkDDALdwE5MMIEuZBpBL4DnOgngN93-YEf4biNwYMI
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 172
ht-degree: 1%

---

# [!UICONTROL Catalog] > [!UICONTROL Email to a Friend]

{{config}}

## [!UICONTROL Email Templates]

![電子郵件範本](./assets/email-to-a-friend-email-templates.png)<!-- zoom -->

<!-- [Email Templates](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/communications/email-templates#configure-email-templates) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 存放區檢視 | 啟用程式，讓客戶能夠傳送電子郵件給朋友，瞭解您商店中的產品。 選項： `Yes` / `No` |
| [!UICONTROL Select Email Template] | 存放區檢視 | 識別由&#x200B;_傳送電子郵件給Friend_&#x200B;函式產生的郵件所使用的電子郵件範本。 預設範本： `Send Product to Friend` |
| [!UICONTROL Allow for Guests] | 存放區檢視 | 判斷寄件者是否必須是註冊客戶，才能傳送產品相關電子郵件給朋友。 選項： `Yes` / `No` |
| [!UICONTROL Max Recipients] | 存放區檢視 | 限制單一電子郵件通訊群組清單中的人數。 |
| [!UICONTROL Max Products Sent in 1  Hour] | 存放區檢視 | 限制單一使用者在一小時期間內可共用的產品數量。 |
| [!UICONTROL Limit Sending By] | 存放區檢視 | 決定用來識別傳送者的方法。 選項包括： <br/>**`IP Address`**- （建議）依據用來傳送產品電子郵件之電腦的IP位址識別寄件者。<br/>**`Cookie (unsafe)`** — 透過瀏覽器Cookie識別寄件者。 此方法不安全，因為使用者可以刪除Cookie以避免限制。 |

{style="table-layout:auto"}
