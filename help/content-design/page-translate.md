---
title: 翻譯內容頁面
description: 瞭解如何建立特定商店檢視中可用的每個頁面的翻譯版本。
exl-id: e8743ea5-0c8e-4970-987d-c9ac7c1e2a66
feature: Page Content
topic: Commerce, Localization
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---

# 翻譯內容頁面

如果您的存放區在不同中有多個檢視 [語言](../stores-purchase/store-localize.md)，而且您已將每個檢視的地區設定設為不同的語言，結果會得到部分翻譯的網站。 下一步是建立可從特定存放區檢視取得的每個頁面的翻譯版本。 此 [!UICONTROL Store View] 的欄 _[!UICONTROL Manage Pages]_清單會顯示每個具有頁面翻譯版本的檢視。

若要翻譯內容頁面，您必須建立另一個頁面，該頁面具有與原始頁面相同的URL索引鍵，但已指派給特定商店檢視。 然後，使用翻譯的文字更新特定檢視的頁面。 下列範例說明如何建立 _關於我們_ 西班牙商店檢視頁面。

## 步驟1：複製要翻譯之頁面的URL金鑰

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. 在格線中，尋找要翻譯的頁面，並在中開啟 _編輯_ 模式。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Search Engine Optimization]** 區段並複製 **[!UICONTROL URL Key]** 到剪貼簿。

1. 若要返回 _[!UICONTROL Pages]_格點，按一下&#x200B;**[!UICONTROL Back]**頂端按鈕列中的。

## 步驟2：為翻譯內容新增頁面

1. 按一下 **[!UICONTROL Add New Page]**.

1. 輸入已翻譯的 **[!UICONTROL Page Title]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Content]** 並填入頁面的已翻譯文字。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Search Engine Optimization]** 並執行下列動作：

   - 貼上 **[!UICONTROL URL Key]** 從原始頁面複製而來的專案。

   - 輸入已翻譯文字 **[!UICONTROL Meta Title]**， **[!UICONTROL Meta Keywords]**、和 **[!UICONTROL Meta Description]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Page in Websites]** 部分與集合 **[!UICONTROL Store View]** 前往頁面可用的商店檢視。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Design]** 並設定欄 **[!UICONTROL Layout]** 頁面的「 」。

1. 按一下 **[!UICONTROL Save]**.

1. 出現提示時，請重新整理任何無效的 [快取](../systems/cache-management.md).

## 步驟3：驗證翻譯

若要驗證翻譯，請前往店面並使用語言選擇器變更店面檢視。

請注意，頁面上仍有一些需要翻譯的元素，包括公司頁尾連結 [區塊](block-add.md)，則 [歡迎訊息](../getting-started/storefront-branding.md#change-the-welcome-message)、和 [產品資訊](../stores-purchase/store-localize.md#localize-products).
