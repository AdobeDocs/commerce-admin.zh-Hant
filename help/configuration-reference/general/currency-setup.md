---
title: 『[!UICONTROL General] &gt； [!UICONTROL Currency Setup]『
description: 檢閱上的組態設定 [!UICONTROL General] &gt； [!UICONTROL Currency Setup] 商務管理員頁面。
exl-id: a84be30f-f2eb-4c86-942c-2d49e5cf23af
role: Admin
feature: Currency, Configuration, Data Import/Export
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 3%

---

# [!UICONTROL General] > [!UICONTROL Currency Setup]

{{config}}

>[!NOTE]
>
>另請參閱 [貨幣設定](../../stores-purchase/currency-configuration.md) 以取得這些設定的詳細資訊。

## [!UICONTROL Currency Options]

![幣別設定>幣別選項](./assets/currency-setup-currency-options.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Base Currency] | 網站 | 用於所有線上付款交易的主要幣別。 若為多個商店檢視，價格範圍必須在 [目錄](../catalog/catalog.md) 設定。 |
| [!UICONTROL Default Display Currency] | 存放區檢視 | 用來顯示價格的主要貨幣。 |
| [!UICONTROL Allowed Currencies] | 存放區檢視 | 商店接受的付款貨幣。 |

{style="table-layout:auto"}

## [!UICONTROL Fixer.io (legacy)]

>[!IMPORTANT]
>
>從2.4.6版開始， [[!DNL Fixer.io]](https://fixer.io/) 服務已棄用，並由 [[!DNL Fixer API] （愛彼亞）](https://apilayer.com/marketplace/fixer-api) 服務。 強烈建議您使用APILayer帳戶，而非過時的帳戶 [!DNL Fixer.io] 帳戶。

![貨幣設定> Fixer.io](./assets/currency-setup-fixer.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL API key] | 全域 | 用於透過您的網站存取轉換服務的金鑰 [!DNL fixer.io] 帳戶。 如需詳細資訊，請參閱 [[!DNL fixer.io]](https://fixer.io/). |
| [!UICONTROL Connection Timeout in Seconds] | 全域 | 決定Fixer.io工作階段逾時前的閒置秒數。 預設值： `100` |

{style="table-layout:auto"}

## [!UICONTROL Fixer Api (APILayer)]

![貨幣設定>修正程式Api (APILayer)](./assets/currency-setup-fixer-api.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL API key] | 全域 | 用於透過您的網站存取轉換服務的金鑰 [!DNL APILayer] 帳戶。 如需詳細資訊，請參閱 [[!DNL APILayer]](https://apilayer.com/). |
| [!UICONTROL Connection Timeout in Seconds] | 全域 | 決定閒置的秒數，超過此秒數後 [!DNL APILayer] 工作階段逾時。 預設值為 `100`. |

{style="table-layout:auto"}

## [!UICONTROL Currency Converter API]

![貨幣設定>貨幣轉換工具API](./assets/currency-setup-converter.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL API key] | 全域 | 用來存取轉換服務的金鑰。 如需詳細資訊，請參閱 [[!DNL Currency Convertor] API](https://free.currencyconverterapi.com/). |
| [!UICONTROL Connection Timeout in Seconds] | 全域 | 決定閒置的秒數(在 [!DNL Currency Converter] 工作階段逾時。 預設值：`100` |

{style="table-layout:auto"}

## [!UICONTROL Scheduled Import Settings]

![貨幣設定>排程匯入設定](./assets/currency-setup-scheduled-import-settings.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 存放區檢視 | 決定是否已針對幣別匯率啟用排程匯入。 選項： `Yes` / `No` |
| [!UICONTROL Service] | 存放區檢視 | 指定為排程匯入提供資料的服務。 預設值為 `fixer.io` |
| [!UICONTROL Start Time] | 存放區檢視 | 以24小時製為基礎，以小時、分鐘和秒表示開始時間。 |
| [!UICONTROL Frequency] | 存放區檢視 | 決定排程匯入發生的頻率。 選項： `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Error Email Recipient] | 存放區檢視 | 識別透過電子郵件通知排程匯入錯誤之每個人的電子郵件地址。 如果有多個收件者，請以逗號分隔每個專案。 |
| [!UICONTROL Error Email Sender] | 網站 | 識別顯示為錯誤電子郵件通知寄件者的商店聯絡人。 預設寄件者： `General Contact` |
| [!UICONTROL Error Email Template] | 網站 | 指定作為錯誤電子郵件通知基礎的範本。 預設範本： `Currency Update Warnings` |

{style="table-layout:auto"}
