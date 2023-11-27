---
title: 客戶工作階段存留期
description: 客戶工作階段期限會決定客戶購物工作階段的期限。
exl-id: 7180631a-3233-40f3-92bf-b329fc260cf9
feature: Customers, Configuration, Security
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---

# 客戶工作階段存留期

客戶購物工作階段的期限是由數個因素決定，包括伺服器工作階段的長度、使用 [永續性購物車](../stores-purchase/cart-persistent.md)和儲存在瀏覽器中的資訊存留期。 雖然這些和相同的客戶體驗有關，但它們是具有不同到期事件和生命週期的不同程式。

| 程式 | 說明 |
| --- | --- |
| 工作階段 | 儲存在伺服器上的資訊，例如購物車的內容。 如果伺服器工作階段在Cookie過期之前過期，客戶可能會遺失購物車內容，並降低安全性風險。 |
| 工作階段Cookie | 以數字或字串形式儲存在瀏覽器中的資訊。 如果工作階段Cookie在伺服器工作階段之前過期，則客戶會登出。 當客戶關閉瀏覽器視窗時，會刪除工作階段Cookie。 Cookie期限預設為3600秒或一小時。 如果在這段期間沒有鍵盤活動，目前的工作階段就會結束，客戶必須登回他們的帳戶才能繼續購物。 |

{style="table-layout:auto"}

如果 [永久購物車](../stores-purchase/cart-persistent.md) 已啟用，購物車內容會儲存以供客戶下次登入其帳戶時使用。 使用永續性購物車時，建議您將伺服器工作階段和工作階段Cookie的存留期設定為較長的一段時間。

在伺服器上，作業階段的長度是由 `php.ini` 檔案和多個變數。 目前Adobe Commerce沒有控制伺服器工作階段長度的管理員組態設定。

## 設定Cookie期限

1. 在 _管理員_ 側欄，前往 [!UICONTROL **商店**] > _[!UICONTROL Settings]_>[!UICONTROL **設定**].

1. 如果您有多個商店，請將 **[!UICONTROL Store View]** 選擇器位於設定適用的存放區右上角。

1. 在左側面板中的 **[!UICONTROL General]**，選擇 **[!UICONTROL Web]**.

1. 展開 **[!UICONTROL Default Cookie Settings]** 區段。

   ![預設Cookie設定](../configuration-reference/general/assets/web-default-cookie-settings.png){width="600" zoomable="yes"}

1. 若要變更預設值，請清除 **[!UICONTROL Use system value]** 核取方塊，並輸入新值（以秒為單位）。

1. 完成後，按一下 **[!UICONTROL Save Config]**.

## 設定 _記住我_ 功能

為了讓您更輕鬆登入， **[!UICONTROL Remember Me]** 函式可讓使用者帳戶持有人避免在每次進入店面時都輸入其認證。 基於安全考量，預設會停用持續性功能。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Customers]** 並選擇 **[!UICONTROL Persistent Shopping Cart]**.

1. 展開 **[!UICONTROL General Options]** 區段。

1. 的 **[!UICONTROL Enable Persistence]**，設定為 `Yes`. (清除 **[!UICONTROL Use system value]** 核取方塊，以允許變更預設設定。)

1. 的 **[!UICONTROL Enable "Remember Me"]**，設定為 `Yes` 或 `No` 根據您的需求。

1. 完成後，按一下 **[!UICONTROL Save Config]**.
