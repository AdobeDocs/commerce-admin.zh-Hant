---
title: 瀏覽器功能偵測
description: 瞭解如何設定瀏覽器功能偵測，以及在需要變更客戶的瀏覽器設定時顯示通知。
exl-id: 16caab8b-3ba5-43a1-a6f0-7c1e921be132
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 0%

---

# 瀏覽器功能偵測

和網際網路上的大多數網站和應用程式一樣，Adobe Commerce和Magento Open Source要求訪客的瀏覽器允許Cookie和JavaScript進行完整操作。 不過，使用者的瀏覽器偶爾會設為最高隱私權設定，以防止Cookie和JavaScript同時存取。 您的商店可以設定為測試每位訪客瀏覽器的功能，並在需要變更設定時顯示通知。

- 如果瀏覽器的隱私權設定不允許Cookie，您可以設定系統自動將其重新導向至 [啟用Cookie](../content-design/pages.md#enable-cookies) 頁面，說明如何使用大多數瀏覽器進行建議的設定。
- 如果瀏覽器的隱私權設定不允許JavaScript，您可以設定系統以在每個頁面的標頭上方顯示以下訊息。

如需技術資訊，請參閱 [支援的瀏覽器](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/system-requirements.html#supported-browsers) 在 _安裝指南_.

## 設定瀏覽器功能偵測

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側的面板中，在 _[!UICONTROL General]_，選擇&#x200B;**[!UICONTROL Web]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Browser Capabilities Detection]** 並執行下列動作：

   - 若要顯示說明如何設定瀏覽器以允許Cookie的指示，請設定 **[!UICONTROL Redirect to CMS-page if Cookies are Disabled]** 至 `Yes`.

   - 若要在使用者的瀏覽器中停用JavaScript時，在標題上方顯示橫幅，請設定 **[!UICONTROL Show Notice if JavaScript is Disabled]** 至 `Yes`.

   - 若要在使用者的瀏覽器中停用本機儲存時，在標題上方顯示橫幅，請設定 **[!UICONTROL Show Notice if Local Storage is Disabled]** 至 `Yes`.

   ![一般設定 — 偵測網頁瀏覽器功能](../configuration-reference/general/assets/web-browser-capabilities-detection.png){width="600" zoomable="yes"}

1. 完成後，按一下 **[!UICONTROL Save Config]**.
