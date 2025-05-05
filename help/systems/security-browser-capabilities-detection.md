---
title: 瀏覽器功能偵測
description: 瞭解如何設定瀏覽器功能偵測，以及在需要變更客戶的瀏覽器設定時顯示通知。
exl-id: 16caab8b-3ba5-43a1-a6f0-7c1e921be132
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# 瀏覽器功能偵測

和網際網路上的大多數網站和應用程式一樣，Adobe Commerce和Magento Open Source要求訪客的瀏覽器允許Cookie和JavaScript進行完整操作。 不過，使用者的瀏覽器偶爾會設為最高隱私權設定，以防止Cookie和JavaScript同時存取。 您的商店可以設定為測試每位訪客瀏覽器的功能，並在需要變更設定時顯示通知。

- 如果瀏覽器的隱私權設定不允許Cookie，您可以設定系統自動將其重新導向至[啟用Cookie](../content-design/pages.md#enable-cookies)頁面，該頁面說明如何在大部分的瀏覽器中進行建議的設定。
- 如果瀏覽器的隱私權設定不允許JavaScript，您可以設定系統在每個頁面的標頭上方顯示以下訊息。

如需技術資訊，請參閱&#x200B;_安裝指南_&#x200B;中的[支援的瀏覽器](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/system-requirements.html?lang=zh-Hant#supported-browsers)。

## 設定瀏覽器功能偵測

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側&#x200B;_[!UICONTROL General]_&#x200B;下方的面板中，選擇&#x200B;**[!UICONTROL Web]**。

1. 展開![展開選取器](../assets/icon-display-expand.png) **[!UICONTROL Browser Capabilities Detection]**&#x200B;區段，然後執行下列動作：

   - 若要顯示說明如何設定瀏覽器以允許Cookie的指示，請將&#x200B;**[!UICONTROL Redirect to CMS-page if Cookies are Disabled]**&#x200B;設為`Yes`。

   - 若要在使用者的瀏覽器中停用JavaScript時，在標題上方顯示橫幅，請將&#x200B;**[!UICONTROL Show Notice if JavaScript is Disabled]**&#x200B;設為`Yes`。

   - 若要在使用者的瀏覽器中停用本機儲存體時，在標題上方顯示橫幅，請將&#x200B;**[!UICONTROL Show Notice if Local Storage is Disabled]**&#x200B;設定為`Yes`。

   ![一般設定 — 網頁瀏覽器功能偵測](../configuration-reference/general/assets/web-browser-capabilities-detection.png){width="600" zoomable="yes"}

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。
