---
title: 翻譯內容頁面
description: 瞭解如何建立特定商店檢視中可用的每個頁面的翻譯版本。
exl-id: e8743ea5-0c8e-4970-987d-c9ac7c1e2a66
feature: Page Content
topic: Commerce, Localization
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---

# 翻譯內容頁面

如果您的存放區有多個使用不同[語言](../stores-purchase/store-localize.md)的檢視，而且您已將每個檢視的區域設定設定為不同的語言，則結果為部分翻譯的網站。 下一步是建立可從特定存放區檢視取得的每個頁面的翻譯版本。 _[!UICONTROL Manage Pages]_&#x200B;清單的[!UICONTROL Store View]欄會顯示每個具有頁面轉譯版本的檢視。

若要翻譯內容頁面，您必須建立另一個頁面，該頁面具有與原始頁面相同的URL索引鍵，但已指派給特定商店檢視。 然後，使用翻譯的文字更新特定檢視的頁面。 下列範例說明如何為西班牙商店檢視建立&#x200B;_About Us_&#x200B;頁面的翻譯版本。

## 步驟1：複製要翻譯之頁面的URL金鑰

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**。

1. 在格線中，找到要翻譯的頁面，並以&#x200B;_編輯_&#x200B;模式開啟。

1. 展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Search Engine Optimization]**&#x200B;區段，並將&#x200B;**[!UICONTROL URL Key]**&#x200B;複製到剪貼簿。

1. 若要返回&#x200B;_[!UICONTROL Pages]_&#x200B;格線，請按一下頂端按鈕列中的&#x200B;**[!UICONTROL Back]**。

## 步驟2：為翻譯內容新增頁面

1. 按一下&#x200B;**[!UICONTROL Add New Page]**。

1. 輸入翻譯的&#x200B;**[!UICONTROL Page Title]**。

1. 展開![展開選取器](../assets/icon-display-expand.png) **[!UICONTROL Content]**&#x200B;區段，並完成頁面的翻譯文字。

1. 展開![展開選取器](../assets/icon-display-expand.png) **[!UICONTROL Search Engine Optimization]**&#x200B;區段，然後執行下列動作：

   - 貼上您從原始頁面複製的&#x200B;**[!UICONTROL URL Key]**。

   - 輸入&#x200B;**[!UICONTROL Meta Title]**、**[!UICONTROL Meta Keywords]**&#x200B;和&#x200B;**[!UICONTROL Meta Description]**&#x200B;的翻譯文字。

1. 展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Page in Websites]**&#x200B;區段，並將&#x200B;**[!UICONTROL Store View]**&#x200B;設定為頁面可用的存放區檢視。

1. 展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Design]**&#x200B;區段並設定頁面的欄&#x200B;**[!UICONTROL Layout]**。

1. 按一下&#x200B;**[!UICONTROL Save]**。

1. 出現提示時，請重新整理任何無效的[快取](../systems/cache-management.md)。

## 步驟3：驗證翻譯

若要驗證翻譯，請前往店面並使用語言選擇器變更店面檢視。

請注意，頁面上仍有一些元素需要翻譯，包括公司頁尾連結[區塊](block-add.md)、[歡迎訊息](../getting-started/storefront-branding.md#change-the-welcome-message)和[產品資訊](../stores-purchase/store-localize.md#localize-products)。
