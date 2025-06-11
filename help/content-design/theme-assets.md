---
title: 佈景主題資產
description: 瞭解如何管理您的主題資產，例如CSS、字型、影像和JavaScript檔案。
exl-id: 326c648e-eace-45a0-b53d-bbc8702fee05
feature: Page Content, Themes
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hant/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"
source-git-commit: e50b85311f4512fb54c7cb29faf6136eaf07eae6
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 0%

---

# 佈景主題資產

_靜態檔案_&#x200B;是資產集合，例如主題所使用的CSS、字型、影像和JavaScript。 靜態檔案的位置是在[基底URL](../stores-purchase/store-urls.md)組態中指定的。 您可以將數位簽章新增至每個靜態檔案的URL，讓瀏覽器能在較新版本可用時偵測到。 如果簽章與瀏覽器快取中儲存的簽章不同，則會使用較新版本的檔案。

對於標準安裝，與主題關聯的資產會整理在[!DNL Commerce]根目錄下以下位置的`web`資料夾中。

`[commerce_root]/app/design/frontend/Magento/[theme_name]/web`

## 將數位簽章新增至靜態檔案URL

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Advanced]**&#x200B;並選擇&#x200B;**[!UICONTROL Developer]**。

1. 展開&#x200B;**[!UICONTROL Static Files Settings]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![靜態檔案設定](./assets/developer-static-files-settings.png){width="500" zoomable="yes"}

1. 將&#x200B;**[!UICONTROL Sign Static Files]**&#x200B;設為`Yes`。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

| 檔案型別 | 說明 |
|--- |--- |
| CSS | 控制與外觀關聯的視覺樣式。 伺服器上的位置範例： `[commerce]/app/design/frontend/Magento/[theme]/web/css` |
| 字型 | 提供主題可用的字型。 伺服器上的位置： `[commerce]/app/design/frontend/Magento/[theme]/web/fonts` |
| 影像 | 提供主題使用的圖形資產，包括按鈕、背景紋理等。 伺服器上的位置範例： `[commerce]/app/design/frontend/Magento/[theme]/web/images` |
| JS | 主題特定的JavaScript常式和可呼叫函式。 伺服器上的位置範例： `[commerce]/app/design/frontend/Magento/[theme]/web/js` |

{style="table-layout:auto"}

## 合併CSS檔案

為了將網站最佳化並減少頁面載入時間，您可以將CSS檔案合併成單一壓縮檔案，以減少個別CSS檔案的數量。 如果您開啟合併的CSS檔案，您會看到一個連續的文字串流，其中已移除分行符號。 您無法編輯合併的檔案，因此最好等到您退出開發模式且不再頻繁變更CSS為止。

>[!NOTE]
>
>只有在[開發人員模式](../systems/developer-tools.md#operation-modes)中工作時，才能從&#x200B;_Admin_&#x200B;面板合併CSS檔案。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板&#x200B;**[!UICONTROL Advanced]**&#x200B;中選擇&#x200B;**[!UICONTROL Developer]**。

1. 展開&#x200B;**[!UICONTROL CSS Settings]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![CSS設定](./assets/developer-css-settings.png){width="500" zoomable="yes"}

   如需這些組態選項的詳細說明，請參閱&#x200B;_組態參考_&#x200B;中的[CSS設定](../configuration-reference/advanced/developer.md#css-settings)。

1. 將&#x200B;**[!UICONTROL Merge CSS Files]**&#x200B;設為`Yes`。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

## 合併JavaScript檔案

您可以將多個JavaScript檔案合併為單一壓縮檔案，以縮短頁面載入時間。 如果您開啟合併的JavaScript檔案，您會看到一個連續的文字串流，其中刪除了分行符號。 如果您已完成開發程式，且程式碼不含任何錯誤，則可考慮合併檔案。

>[!NOTE]
>
>只有在[開發人員模式](../systems/developer-tools.md#operation-modes)中工作時，才能從&#x200B;_管理員_&#x200B;面板合併JavaScript檔案。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板&#x200B;**[!UICONTROL Advanced]**&#x200B;中選擇&#x200B;**[!UICONTROL Developer]**。

1. 展開&#x200B;**[!UICONTROL JavaScript Settings]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![JavaScript設定](./assets/developer-javascript-settings.png){width="600" zoomable="yes"}

   如需這些組態選項的詳細說明，請參閱&#x200B;_組態參考_&#x200B;中的[JavaScript設定](../configuration-reference/advanced/developer.md#javascript-settings)。

1. 將&#x200B;**[!UICONTROL Merge JavaScript Files]**&#x200B;設為`Yes`。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。
