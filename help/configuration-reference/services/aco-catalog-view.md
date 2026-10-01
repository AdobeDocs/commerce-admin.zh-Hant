---
title: '[!UICONTROL Services] &gt； ACO目錄檢視'
description: 在Adobe Commerce Optimizer管理員的[!UICONTROL Services] &gt； [!UICONTROL ACO Catalog View]頁面上檢閱和更新Commerce組態設定。
feature: Configuration, Security
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hant/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案（Adobe管理的PaaS基礎結構）和內部部署專案的Adobe Commerce 。"
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: b32c28afffe75b3f684f0fef81bd61e9cdcb485a
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 3%
---
# [!UICONTROL Services] > [!UICONTROL ACO Catalog View]

使用這些設定來控制[!DNL Adobe Commerce Optimizer Connector for B2B]所核發的存取權杖。 店面會使用這些權杖，向填入了從管理員中設定的自訂共用目錄同步之資料的Commerce Optimizer私人目錄檢視進行驗證。

{{config}}

![Adobe Commerce管理員顯示ACO目錄檢視存取權杖設定，已啟用3,600秒TTL和權杖簽發。](./assets/aco-catalog-view-access-token-config.png)<!-- zoom -->

## [!UICONTROL Access Token Configuration]

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
| --- | --- | --- |
| [!UICONTROL Token TTL (seconds)] | 全域 | 存取Token在產生後仍保持有效的秒數。 此設定在預設範圍為唯讀。 在網站或商店檢視範圍內設定的值會被忽略。 預設為： 3600秒。 |
| [!UICONTROL Issue Access Tokens] | 存放區檢視 | 控制店面是否可以取得目錄檢視的存取權杖。 設定為`No`時，`Company.catalogViewContext`會傳回目錄檢視ID，但無存取Token，因此店面無法驗證以從Adobe Commerce同步的[!DNL Adobe Commerce Optimizer]私人目錄檢視讀取。 |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
> - [ACO目錄檢視同步處理](./aco-catalog-view-sync.md) — 設定目錄檢視同步處理至[!DNL Adobe Commerce Optimizer]的方式
> - [目錄檢視同步處理狀態監視](../../systems/catalog-view-sync-status.md) — 監視同步處理狀況與調解漂移
