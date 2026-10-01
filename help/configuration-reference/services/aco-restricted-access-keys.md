---
title: '[!UICONTROL Services] > [!UICONTROL ACO Restricted Access Keys]'
description: 檢閱Commerce管理員的[!UICONTROL Services] &gt； [!UICONTROL ACO Restricted Access Keys]頁面上的組態設定。
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
source-wordcount: '182'
ht-degree: 4%
---
# [!UICONTROL Services] > [!UICONTROL ACO Restricted Access Keys]

使用此設定可控制[!DNL Adobe Commerce Optimizer Connector for B2B]套用至其為B2B共用目錄檢視所設定的受限制存取金鑰的預設到期期間。 若要建立、指派和刪除這些金鑰，請參閱[限制存取金鑰管理](../../systems/restricted-access-keys.md)。

{{config}}

## [!UICONTROL Provisioning]

![布建](./assets/optimizer-restricted-access-key-config.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
| --- | --- | --- |
| [!UICONTROL Default key expiry (days)] | 全域 | 新布建的限制存取金鑰的有效期。 [!DNL Adobe Commerce Optimizer]要求每個金鑰的到期日至少在未來一分鐘，並從閘道讀取中排除過期的金鑰，因此一律會套用至少一天的值。 預設值： `36500` |

{style="table-layout:auto"}

>[!NOTE]
>
>由於尚未提供自動金鑰輪換功能，因此預設到期時間設定為較長的到期期間。 請參閱[鍵選取與輪換](../../systems/restricted-access-keys.md#key-selection-and-rotation)。

>[!MORELIKETHIS]
>
> - [ACO目錄檢視](./aco-catalog-view.md) — 設定目錄檢視的店面存取權杖
> - [受限存取金鑰管理](../../systems/restricted-access-keys.md) — 建立、指派和刪除受限存取金鑰
> - [目錄檢視同步處理狀態監視](../../systems/catalog-view-sync-status.md) — 監視金鑰即將到期
