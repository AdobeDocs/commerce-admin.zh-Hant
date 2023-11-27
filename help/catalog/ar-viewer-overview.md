---
title: 『[!DNL AR Viewer] 適用於Adobe Commerce'
description: 瞭解如何 [!DNL AR Viewer] 可讓您的Adobe Commerce執行個體受益，並瞭解如何成功入門和設定擴充功能。
exl-id: 9f9f3ff3-2402-4f70-9fc7-031dd2bb3916
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---

# [!DNL AR Viewer] 適用於Adobe Commerce

增強現實(AR)描述使用者體驗，這些體驗會以讓裝置相機將2D或3D元素加入即時檢視，看起來像是存在於真實世界。

此 [!DNL AR Viewer] 適用於Adobe Commerce的擴充功能提供流暢的體驗，專為使用者顯示已轉譯的3D圖形所設計。

本指南中的資訊提供入門體驗的概述。 [!DNL AR Viewer] 和Adobe Commerce的 [!DNL AR Viewer] 造福使用者，並提供該歷程中遵循的最佳實務。

由Pixar開發， [通用場景描述(USD)](https://www.pixar.com/usd){target=_blank} 是第一個開放原始碼軟體，可以強有力且可縮放地交換3D場景（可能由許多不同的資產、來源和動畫組成），同時促進高度合作的工作流程。 此美元使用於 `.USDZ` 檔案。 這個 `.USDZ` 檔案會將AR和3D內容傳送至使用者的裝置。

>[!NOTE]
>
> 此 [!DNL AR Viewer] 僅支援 `.USDZ` 檔案。

## [!DNL AR Viewer] 需求

此 [!DNL AR Viewer] 與兩者都相容 [!DNL Magento Open Source] 和Adobe Commerce。 另請參閱 [生命週期原則](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/lifecycle-policy.html){target=_blank} 以取得有關支援版本的詳細資訊。

另請參閱 [安裝 [!DNL AR Viewer] 副檔名](../catalog/ar-viewer-setup.md) 以取得詳細資訊。

為了使用 [!DNL AR Viewer]，您的執行個體必須具備下列可用專案：

* PHP 8.1.0
* Adobe Commerce 2.4.4版及更新版本
* Magento Open Source (CE) 2.4.x版

## 相容性限制

[!DNL AR Viewer] 現有的相容性限制：

* `.USDZ` 僅限：此功能僅支援 `.USDZ` 檔案。
* `qr-code`：需要 `endroid/qr-code` 版本4.5。
* `Catalog module`：需要 `magento/module-catalog` 104.0.0版。
