---
title: '[!UICONTROL Sales] > [!UICONTROL 3D Secure]'
description: 檢閱Commerce管理員的[!UICONTROL Sales] &gt； [!UICONTROL 3D Secure]頁面上的組態設定。
exl-id: 38eb3ee6-8b80-4ba3-afce-8ab82baa76a9
feature: Configuration, Security, Payments
TQID: https://experienceleague.adobe.com/WzxM9ZYbobbC1fWSIph0jv89uXLte6Wzjs5be27eMyU
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 126
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL 3D Secure]

[!DNL 3-D Secure]由[!DNL Visa]開發，以提升安全的線上交易。 由卡片網路建立的[!DNL 3-D Secure]解決方案範例已由[!DNL Visa]、[!DNL Mastercard SecureCode]、[!DNL American Express SafeKey]和[!DNL CardinalCommerce Consumer Authentication]驗證。 [!DNL CardinalCommerce]是數位交易驗證的全球領先者，也是[!DNL Visa]的全資子公司。

[!DNL 3-D Secure] 2.0版支援許多增強功能，包括進階的驗證方法和驗證流程，以及改善商家與簽發者之間的資料共用。

>[!NOTE]
>
>[Braintree](../../stores-purchase/braintree.md)付款閘道也支援[!DNL 3-D Secure]驗證。

{{config}}

## [!UICONTROL CardinalCommerce]

![CardinalCommerce](./assets/3d-secure-cardinalcommerce.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Environment] | 網站 | 指示您[!DNL CardinalCommerce]帳戶的作業模式。 如果您在測試環境中執行，請選擇「沙箱」。 選項：沙箱/生產（預設） |
| [!UICONTROL Org Unit ID] | 網站 | 來自您[!DNL CardinalCommerce]商家帳戶的組織單位ID。 |
| [!UICONTROL API Key] | 網站 | [!DNL CardinalCommerce]商家帳戶的API金鑰。 |
| [!UICONTROL API Identifier] | 網站 | 來自您[!DNL CardinalCommerce]商家帳戶的API識別碼。 |
| [!UICONTROL Debug] | 網站 | 選項： `Yes` / `No` |

{style="table-layout:auto"}
