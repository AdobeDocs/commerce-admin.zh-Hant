---
title: '[!UICONTROL Services] > [!UICONTROL Commerce Services Connector]'
description: 檢閱Commerce管理員的[!UICONTROL Services] &gt； [!UICONTROL Commerce Services Connector]頁面上的組態設定。
exl-id: 3570e846-c8ab-4a36-b020-1b536bbd377d
feature: Configuration, Saas
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案（Adobe管理的PaaS基礎結構）和內部部署專案的Adobe Commerce 。"
TQID: https://experienceleague.adobe.com/50XCqY8JMjvf9G-wcHLxvlskSd5noIAB0LIX6xMarL0
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 238
ht-degree: 2%

---

# [!UICONTROL Services] > [!UICONTROL Commerce Services Connector]

若要瞭解如何將您的商店連結至Adobe Commerce服務，請參閱[Commerce服務](https://experienceleague.adobe.com/docs/commerce/user-guides/integration-services/saas.html)。

{{config}}

## [!UICONTROL Sandbox API Keys]

![沙箱API金鑰](./assets/sandbox-key-saas-configuration.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Sandbox public API key] | 全域 | 識別作者及其權益（若有）的API金鑰。 |
| [!UICONTROL Sandbox private API key] | 全域 | 與API金鑰相關聯的私密金鑰。 |

{style="table-layout:auto"}

## [!UICONTROL Production Keys]

![生產API金鑰](./assets/prod-key-saas-configuration.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Production public API key] | 全域 | 識別作者及其權益（若有）的API金鑰。 |
| [!UICONTROL Production private API key] | 全域 | 與API金鑰相關聯的私密金鑰。 |

{style="table-layout:auto"}

## [!UICONTROL SaaS Identifier]

![SaaS識別碼](./assets/saas-identifier.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Project] | 全域 | 將所有SaaS資料空間分組的SaaS專案名稱。 如果沒有任何SaaS專案，則會顯示&#x200B;_建立專案_&#x200B;按鈕。 |
| [!UICONTROL Data Space] | 全域 | 列出指定SaaS專案中的SaaS資料空間。 SaaS資料空間的數目取決於您的[Commerce授權](https://experienceleague.adobe.com/docs/commerce/user-guides/integration-services/saas.html)：<br />Adobe Commerce — 一個生產資料空間；兩個測試資料空間；<br />Magento Open Source — 一個生產資料空間；無測試資料空間 |

{style="table-layout:auto"}

## [!UICONTROL IMS Organization]

![IMS組織](./assets/ims-organization.png)<!-- zoom -->

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Sign in using Adobe ID] | 您的Adobe ID通常是您開始成為會員或購買Adobe應用程式或服務時第一次使用的電子郵件地址。 您的Adobe ID是存取Adobe帳戶所需的金鑰。 |

{style="table-layout:auto"}
