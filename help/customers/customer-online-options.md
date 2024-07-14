---
title: 客戶工作階段存留期
description: 客戶工作階段期限會決定客戶購物工作階段的期限。
exl-id: 7180631a-3233-40f3-92bf-b329fc260cf9
feature: Customers, Configuration, Security
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# 客戶工作階段存留期

客戶購物工作階段的存留期是由數個因素所決定，包括伺服器工作階段的長度、[持續購物車](../stores-purchase/cart-persistent.md)的使用，以及儲存在瀏覽器中的資訊存留期。 雖然這些和相同的客戶體驗有關，但它們是具有不同到期事件和生命週期的不同程式。

| 程式 | 說明 |
| --- | --- |
| 工作階段 | 儲存在伺服器上的資訊，例如購物車的內容。 如果伺服器工作階段在Cookie過期之前過期，客戶可能會遺失購物車內容，並降低安全性風險。 |
| 工作階段Cookie | 以數字或字串形式儲存在瀏覽器中的資訊。 如果工作階段Cookie在伺服器工作階段之前過期，則客戶會登出。 當客戶關閉瀏覽器視窗時，會刪除工作階段Cookie。 Cookie期限預設為3600秒或一小時。 如果在這段期間沒有鍵盤活動，目前的工作階段就會結束，客戶必須登回他們的帳戶才能繼續購物。 |

{style="table-layout:auto"}

如果[永久購物車](../stores-purchase/cart-persistent.md)已啟用，購物車內容會儲存以供下次客戶登入帳戶時使用。 使用永續性購物車時，建議您將伺服器工作階段和工作階段Cookie的存留期設定為較長的一段時間。

在伺服器上，工作階段的長度是由`php.ini`檔案和數個變數所控制。 目前Adobe Commerce沒有控制伺服器工作階段長度的管理員組態設定。

## 設定Cookie期限

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;[!UICONTROL **商店**] > _[!UICONTROL Settings]_>[!UICONTROL **設定**]。

1. 如果您有多個商店，請將右上角的&#x200B;**[!UICONTROL Store View]**&#x200B;選擇器設定為套用設定的商店。

1. 在左側面板的&#x200B;**[!UICONTROL General]**&#x200B;下，選擇&#x200B;**[!UICONTROL Web]**。

1. 展開&#x200B;**[!UICONTROL Default Cookie Settings]**&#x200B;區段。

   ![預設Cookie設定](../configuration-reference/general/assets/web-default-cookie-settings.png){width="600" zoomable="yes"}

1. 若要變更預設值，請清除&#x200B;**[!UICONTROL Use system value]**&#x200B;核取方塊並輸入新值（以秒為單位）。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

## 設定&#x200B;_記住我_&#x200B;功能

為了更輕鬆登入，**[!UICONTROL Remember Me]**&#x200B;功能可讓使用者帳戶持有人避免在每次進入店面時輸入其認證。 基於安全考量，預設會停用持續性功能。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Customers]**&#x200B;並選擇&#x200B;**[!UICONTROL Persistent Shopping Cart]**。

1. 展開&#x200B;**[!UICONTROL General Options]**&#x200B;區段。

1. 針對&#x200B;**[!UICONTROL Enable Persistence]**，設定為`Yes`。 （清除&#x200B;**[!UICONTROL Use system value]**&#x200B;核取方塊以允許變更預設設定。）

1. 針對&#x200B;**[!UICONTROL Enable "Remember Me"]**，根據您的需求設定為`Yes`或`No`。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。
