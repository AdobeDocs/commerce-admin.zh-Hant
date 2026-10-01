---
title: '[!UICONTROL Services] &gt； ACO目錄檢視同步'
description: 檢閱Commerce管理員的[!UICONTROL Services] &gt； [!UICONTROL ACO Catalog View Sync]頁面上的組態設定。
feature: Configuration, Security
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案（Adobe管理的PaaS基礎結構）和內部部署專案的Adobe Commerce 。"
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
source-git-commit: 9ec73be87dd329dc04e7b133885fcc156f4ffcb6
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 3%
---
# [!UICONTROL Services] > [!UICONTROL ACO Catalog View Sync]

使用這些設定來控制[!DNL Adobe Commerce Optimizer Connector for B2B]如何將B2B共用目錄組態（目錄檢視、原則、價格手冊和金鑰）同步至[!DNL Adobe Commerce Optimizer]，以及如何解決兩個系統之間的組態差異。 請參閱[目錄檢視同步狀態監視](../../systems/catalog-view-sync-status.md)以監視這些設定的結果。

{{config}}

## [!UICONTROL Deletion]

![刪除](./assets/aco-catalog-view-sync-configuration.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
| --- | --- | --- |
| [!UICONTROL Deletion Grace Period (days)] | 全域 | 共用目錄資料的保留期。 指定刪除的共用目錄目錄檢視、原則和中繼資料在被硬刪除之前要保留的天數。 此值預設為7天。 設定為`0`立即硬刪除。 |

{style="table-layout:auto"}

## [!UICONTROL Creation]

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
| --- | --- | --- |
| [!UICONTROL Creation Grace Period (days)] | 全域 | 新註冊的目錄檢視可等待[!DNL Adobe Commerce Optimizer Connector for B2B]完成其目錄檢視、原則、價格簿和主要設定的首次同步處理的天數，而其狀態會回報為[!UICONTROL Pending]。 如果寬限期沒有成功同步化就失效，則狀態會變更為[!UICONTROL Failed]。 預設值： `1` |

{style="table-layout:auto"}

## [!UICONTROL Drift Reconciler]

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
| --- | --- | --- |
| [!UICONTROL Enabled] | 全域 | 執行排程的漂移調解器，以偵測並報告從[!DNL Adobe Commerce]投影的目錄檢視與[!DNL Adobe Commerce Optimizer]中的目錄檢視組態之間的差異。 如果`automatically repair drift`已啟用，它也會嘗試修正任何可修復的差異。 |
| [!UICONTROL Automatically Repair Drift] | 全域 | 設定為`Yes`時，排程的漂移調解器會更新[!DNL Adobe Commerce Optimizer]設定以符合[!DNL Adobe Commerce]，並重新同步設定。 設定為`No`時，執行只會偵測並報告漂移。 孤立的[!DNL Adobe Commerce Optimizer]實體一律會回報，絕對不會自動移除。 |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
> - [ACO目錄檢視](./aco-catalog-view.md) — 設定目錄檢視的店面讀取存取權杖
> - [目錄檢視同步狀態監視](../../systems/catalog-view-sync-status.md) — 使用這些設定來監視同步狀況與調解漂移
> - [受限制的存取金鑰管理](../../systems/restricted-access-keys.md) — 管理指派給已同步化目錄檢視的存取金鑰
