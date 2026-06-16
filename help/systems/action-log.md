---
title: 動作記錄
description: 瞭解動作記錄檔以及如何設定記錄動作，協助您追蹤對存放區所做的所有變更。
exl-id: a482adfe-a63f-428b-b078-7542a1e2ecee
feature: Logs, Configuration
TQID: https://experienceleague.adobe.com/UtJhP452hJXDyEyjxrknuF4WPoLza-UcnuWxP6ILtq8
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 289
ht-degree: 0%

---

# 動作記錄

{{ee-feature}}

動作記錄檔功能會記錄（記錄）在您商店中工作的管理員使用者所進行的每次變更。 這可讓您追蹤對存放區進行的所有變更。 追蹤這些變更，以及為使用者設定[管理員許可權](permissions.md)，有助於保護您的存放區免受不必要的變更。

對於大多數Admin動作，記錄的資訊包括動作、使用者名稱、動作成功或失敗，以及受動作影響的物件ID。 也會記錄IP位址和日期。

依預設，會啟用並記錄所有管理動作。 若要設定管理員動作記錄，請檢閱選項並選取或清除每個動作型別的核取方塊。 Adobe Commerce僅記錄勾選型別。

檢視[動作記錄報告](action-log-report.md)，以檢閱記錄的管理動作和詳細資料。

![進階設定 — 管理員動作記錄](../configuration-reference/advanced/assets/admin-actions-logging.png){width="600" zoomable="yes"}

如需組態設定的詳細清單，請參閱&#x200B;_組態參考_&#x200B;中的[管理動作記錄檔封存](../configuration-reference/advanced/system.md)。

## 設定管理員記錄動作

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Advanced]**&#x200B;並選擇&#x200B;**[!UICONTROL Admin]**。

1. 展開![展開選取器](../assets/icon-display-expand.png) **[!UICONTROL Admin Actions Logging]**&#x200B;區段，並對每個動作執行下列動作：

   - 若要為動作啟用管理員記錄，請選取核取方塊。
   - 若要停用動作的「管理員記錄」，請清除核取方塊。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

## 封存管理動作記錄

管理員動作記錄檔可以封存任何天數。 指定期間後也可刪除封存。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Advanced]**&#x200B;並選擇&#x200B;**[!UICONTROL System]**。

1. 展開&#x200B;**[!UICONTROL Admin Action Log Archiving]**&#x200B;並設定選項：

   - **[!UICONTROL Logs Entry Lifetime, Days]** — 設定要保留封存記錄檔的天數。
   - **[!UICONTROL Log Archiving Frequency]** — 設定建立封存的頻率。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。
