---
title: '[!UICONTROL Sales] > [!UICONTROL Gift Cards]'
description: 檢閱Commerce管理員的[!UICONTROL Sales] &gt； [!UICONTROL Gift Cards]頁面上的組態設定。
exl-id: 95bfdbde-633e-44d0-9d43-00dde671ab6d
feature: Configuration, Gift
TQID: https://experienceleague.adobe.com/J-VH-mdaM7HrMRHJMNmmbBPggm1hjtHHWTh3q-5en0w
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2: id: d9ced453-36f4-4eb5-b2f3-1d593e32476b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 333
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Gift Cards]

{{ee-feature}}

{{config}}

## [!UICONTROL Gift Card Email Settings]

![禮卡電子郵件設定](./assets/gift-cards-gift-card-email-settings.png)<!-- zoom -->

<!-- [Gift Card Email Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Gift Card Notification Email Sender] | 存放區檢視 | 識別顯示為禮品卡通知電子郵件寄件者的[商店連絡人](../../getting-started/store-details.md#store-email-addresses)。 預設值： `General Contact` |
| [!UICONTROL Gift Card Notification Email Template] | 存放區檢視 | 決定用於禮品卡通知電子郵件的[範本](../../systems/email-templates.md)。 |

{style="table-layout:auto"}

## [!UICONTROL Gift Card General Settings]

![禮卡一般設定](./assets/gift-cards-gift-card-general-settings.png)<!-- zoom -->

<!-- [Gift Card General Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Redeemable] | 全域 | 決定禮卡持有人是否可以兌換其現金價值。 選項： `Yes` / `No`。 |
| [!UICONTROL Lifetime (days)] | 全域 | 決定卡片有效的天數。 如果留空，卡片不會過期。 <br/><br/>**_重要:_**&#x200B;在某些地方，在禮品卡上設定到期資料是不合法的。 在設定禮品卡的期限之前，請先檢查當地法律。 |
| [!UICONTROL Allow Gift Message] | 存放區檢視 | 決定購買禮品卡的客戶是否可選擇加入禮品訊息。 選項： `Yes` / `No`。 |
| [!UICONTROL Gift Message Maximum Length] | 存放區檢視 | 決定禮卡訊息中允許的最大字元數。 預設值： 255 |
| [!UICONTROL Generate Gift Card Account when Order Item is] | 全域 | 決定客戶下訂單時或開立訂單商業發票時是否產生禮品卡帳戶。 選項： `Ordered` / `Invoiced` |

{style="table-layout:auto"}

## [!UICONTROL Email Sent from Gift Card Account Management]

![由禮卡帳戶管理傳送的電子郵件](./assets/gift-cards-email-sent-from-account.png)<!-- zoom -->

<!-- [Email Sent from Gift Card Account Management](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Gift Card Email Sender] | 存放區檢視 | 識別顯示為禮品卡電子郵件寄件者的[商店連絡人](../../getting-started/store-details.md#store-email-addresses)。 預設值： `General Contact` |
| [!UICONTROL Gift Card Template] | 存放區檢視 | 決定用於禮品卡電子郵件的[範本](../../systems/email-templates.md)。 |

{style="table-layout:auto"}

## [!UICONTROL Gift Card Account General Settings]

![禮卡帳戶一般設定](./assets/gift-cards-gift-card-account-general-settings.png)<!-- zoom -->

<!-- [Gift Card Account General Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Code Length] | 全域 | 決定禮卡代碼的長度。 |
| [!UICONTROL Code Format] | 全域 | 決定禮卡代碼的格式。 選項： `Alphanumeric` / `Numeric` |
| [!UICONTROL Code Prefix] | 全域 | 定義新增至程式碼開頭的任何前置詞。 |
| [!UICONTROL Code Suffix] | 全域 | 定義新增到程式碼結尾的任何尾碼。 |
| [!UICONTROL Dash Every X Characters] | 全域 | 如果要在程式碼中包含破折號，請決定每個破折號之間的字元數。 |
| [!UICONTROL New Pool Size] | 全域 | 決定要產生的新程式碼集區的大小。 |
| [!UICONTROL Low Code Pool Threshold] | 全域 | 決定程式碼集區中觸發需要補充集區之警示的記錄數。 |
| [!UICONTROL Generate] | 全域 | 按一下以產生禮品卡代碼清單。 |

{style="table-layout:auto"}
