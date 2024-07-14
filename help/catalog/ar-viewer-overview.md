---
title: Adobe Commerce的'[!DNL AR Viewer]'
description: 瞭解 [!DNL AR Viewer] 如何讓您的Adobe Commerce執行個體受益，以及如何成功上線和設定擴充功能。
exl-id: 9f9f3ff3-2402-4f70-9fc7-031dd2bb3916
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# 適用於Adobe Commerce的[!DNL AR Viewer]

增強現實(AR)描述使用者體驗，這些體驗會以讓裝置相機將2D或3D元素加入即時檢視，看起來像是存在於真實世界。

適用於Adobe Commerce的[!DNL AR Viewer]擴充功能提供流暢的體驗，專為使用者顯示已轉譯的3D圖形所設計。

本指南中的資訊提供Adobe Commerce中[!DNL AR Viewer]上線體驗的概觀，以及[!DNL AR Viewer]如何讓使用者受益，以及在歷程中要遵循的最佳實務。

由Pixar所開發，[Universal Scene Description (USD)](https://www.pixar.com/usd){target=_blank}是第一個開放原始碼軟體，可以強有力且可縮放地交換可能由許多不同資產、來源和動畫所組成的3D場景，同時促進高度合作的工作流程。 此USD用於`.USDZ`個檔案中。 此`.USDZ`檔案會將AR和3D內容傳送至使用者的裝置。

>[!NOTE]
>
> [!DNL AR Viewer]僅支援`.USDZ`個檔案。

## [!DNL AR Viewer]需求

[!DNL AR Viewer]與[!DNL Magento Open Source]和Adobe Commerce都相容。 請參閱[生命週期原則](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/lifecycle-policy.html){target=_blank}，以取得支援版本的詳細資訊。

如需詳細資訊，請參閱[安裝 [!DNL AR Viewer] 擴充功能](../catalog/ar-viewer-setup.md)。

若要使用[!DNL AR Viewer]，您的執行個體必須具備下列可用專案：

* PHP 8.1.0
* Adobe Commerce 2.4.4版及更新版本
* Magento Open Source (CE) 2.4.x版

## 相容性限制

[!DNL AR Viewer]現有的相容性限制：

* 僅限`.USDZ`：此功能僅支援`.USDZ`個檔案。
* `qr-code`：需要`endroid/qr-code` 4.5版。
* `Catalog module`：需要`magento/module-catalog` 104.0.0版。
