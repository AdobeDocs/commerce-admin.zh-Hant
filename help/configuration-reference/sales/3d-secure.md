---
title: 『[!UICONTROL Sales] &gt； [!UICONTROL 3D Secure]『
description: 檢閱上的組態設定 [!UICONTROL Sales] &gt； [!UICONTROL 3D Secure] 商務管理員頁面。
exl-id: 38eb3ee6-8b80-4ba3-afce-8ab82baa76a9
feature: Configuration, Security, Payments
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 3%

---

# [!UICONTROL Sales] > [!UICONTROL 3D Secure]

[!DNL 3-D Secure] 開發人員 [!DNL Visa] 提升安全的線上交易。 範例 [!DNL 3-D Secure] 由卡網路建立的解決方案需由驗證 [!DNL Visa]， [!DNL Mastercard SecureCode]， [!DNL American Express SafeKey]、和 [!DNL CardinalCommerce Consumer Authentication]. [!DNL CardinalCommerce] 是數位交易驗證的全球領先業者，也是本集團全資擁有的子公司， [!DNL Visa].

[!DNL 3-D Secure] 2.0版支援許多增強功能，包括進階驗證方法和驗證流程，以及改善商家和簽發者之間的資料共用。

>[!NOTE]
>
>此 [Braintree](../../stores-purchase/braintree.md) 付款閘道也支援 [!DNL 3-D Secure] 驗證。

{{config}}

## [!UICONTROL CardinalCommerce]

![Cardinalcommerce](./assets/3d-secure-cardinalcommerce.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Environment] | 網站 | 指示的作業模式 [!DNL CardinalCommerce] 帳戶。 如果您在測試環境中執行，請選擇「沙箱」。 選項：沙箱/生產（預設） |
| [!UICONTROL Org Unit ID] | 網站 | 來自貴機構的組織單位ID [!DNL CardinalCommerce] 商家帳戶。 |
| [!UICONTROL API Key] | 網站 | 來自您的 [!DNL CardinalCommerce] 商家帳戶。 |
| [!UICONTROL API Identifier] | 網站 | 來自您的 [!DNL CardinalCommerce] 商家帳戶。 |
| [!UICONTROL Debug] | 網站 | 選項： `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}
