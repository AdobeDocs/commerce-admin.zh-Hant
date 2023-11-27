---
title: 『[!DNL AR Viewer] (適用於Adobe Commerce設定)
description: 瞭解如何使用管理3D模型資產 [!DNL AR Viewer] 產品清單的擴充功能。
exl-id: e3f081ff-b994-4842-a1f3-613012d33a9c
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---

# 使用管理產品3D模型 [!DNL AR Viewer] 適用於Adobe Commerce

對於每個產品，您可以上傳 `.USDZ` 允許在產品清單中使用AR和3D模型的檔案。

此 [!DNL AR Viewer] 僅支援 `.USDZ` 檔案。

## 安裝擴充功能

[!DNL AR Viewer] 會作為擴充功能安裝，從 [Adobe Commerce Marketplace](https://commercemarketplace.adobe.com/magento-module-arviewer.html){target=_blank}.

請參閱 [_安裝指南_](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) 以取得擴充功能安裝程式的詳細資訊。

在 [!DNL AR Viewer] 已安裝並設定擴充功能，管理員使用者可以設定、自訂及管理產品清單，以包含3D模型。

## 新增3D模型

1. 在編輯模式中開啟產品。

1. 若要使用特定商店檢視，請設定 **[!UICONTROL Store View]** 選擇適用的檢視。

   >[!NOTE]
   >
   >新產品3D模型為 _一直_ 已上傳並顯示在中 _全部_ 商店檢視，即使 `All Store Views` 範圍未用於上傳。 <br/><br/>若要從特定商店檢視中隱藏任何產品3D模型，您必須切換到該「商店檢視」，選取 **[!UICONTROL Hide from Product Page]** 核取方塊，然後按一下 **[!UICONTROL Save]**.

1. 向下捲動並展開 _[!UICONTROL Product 3D Model]_區段。

   ![功能表快顯功能表](assets/ar-viewer-product-options.png){width="700" zoomable="yes"}

1. 新增3D模型(`.USDZ` 檔案)。

1. 按一下 **[!UICONTROL Save]**.

### 刪除3D模型

若要從產品詳細資料中移除3D模型：

1. 按一下 **[!UICONTROL Delete]**.

1. 按一下 **[!UICONTROL Save]**.

## 檢視產品3D模型

當使用3D模型更新產品詳細資料時：

1. 此 [!DNL AR Viewer] 在產品說明中產生QR碼，以編碼AR檔案。

1. 客戶可在產品頁面看到此QR碼。

1. 客戶使用行動裝置掃描二維碼時，行動裝置上會呈現AR體驗。

>[!NOTE]
>
> 如需使用者將3d模型新增至產品的一系列示範影片，請參閱 [Adobe Commerce的AR檢視器](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/catalog/augmented-reality.html) 頁面位置 _Commerce影片和Tutorials_.
