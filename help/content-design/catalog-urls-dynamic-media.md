---
title: 動態媒體URL
description: 瞭解如何使用動態媒體URL作為影像或其他媒體資產的相對參照。
exl-id: 41aabde2-f6cc-4b83-8d56-9753a7aa93e9
feature: CMS, Media
source-git-commit: d3b9b4cd0d12f8d5feb2bad0bf601970f9ee1a36
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---

# 動態媒體URL

動態媒體URL是影像或其他媒體資產的相對參照。 啟用後，動態媒體URL可用於直接連結至伺服器上的資產，或連結至儲存在伺服器上的檔案。 [內容傳遞網路](media-storage-content-delivery-network.md). 使用Dynamic Media URL可能會影響目錄效能，以及 [編輯者](editor.md#configure-the-editor) 可設定為使用靜態或動態媒體URL。

與所有專案一樣 [標籤標籤](../systems/markup-tags.md)，指示詞會以雙大括弧括住。 動態媒體URL的格式如下所示：

`\{\{media url="path/to/image.jpg"}}`

頁面在店面轉譯時，系統會從儲存的HTML內容處理動態URL指示。 每次呈現頁面時，都會掃描內容 `\{\{media url="..."}}` 而每個指示詞都會取代為對應的媒體URL。

{{$include /help/_includes/directives-caution.md}}

## 設定靜態媒體URL

依預設，從WYSIWYG編輯器插入目錄中的影像會有相對的動態URL。 如果您偏好使用靜態URL，可以變更組態設定。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中的 _[!UICONTROL General]_，選擇&#x200B;**[!UICONTROL Content Management]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL WYSIWYG Options]** 區段。

   ![WYSIWYG選項](./assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Use Static URLs for Media Content in WYSIWYG]** 變更為下列其中一項：

   - `Yes`  — 針對以WYSIWYG編輯器插入的媒體內容使用靜態URL。 靜態URL為絕對URL，若為 [基礎URL](../stores-purchase/store-urls.md) 的變更。

   - `No` - （預設）對於以WYSIWYG編輯器插入的媒體內容，根據 `\{\{media url="..."}}` 指令。 動態URL是相對的，如果商店的基本URL有所變更，則不會中斷。

1. 完成後，按一下 **[!UICONTROL Save Config]**.
