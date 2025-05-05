---
title: 工作階段管理
description: 瞭解如何設定工作階段管理，以保護管理員和店面。
exl-id: ad954218-aa3e-44e6-b23f-008de7fc7543
role: Admin
feature: Configuration, Security
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '786'
ht-degree: 0%

---

# 工作階段管理

[工作階段管理](https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html)是API安全性的反拒絕服務(DoS)最佳實務。 工作階段代表訪客在您網站上花費的時間，與管理員使用者或客戶登入其帳戶的時間長短無關。

工作階段是與相同使用者相關聯的網路HTTP要求與回應交易序列。 這是在使用者端（管理員）存取伺服器時，將使用者端與其資料建立關聯的方法。 工作階段用於建立變數，例如存取許可權和本地化設定，這些變數適用於使用者在工作階段期間與網頁應用程式進行的每次互動。

## 工作階段大小

使用下列組態設定來限制管理員使用者和店面訪客的工作階段大小上限：

- **[!UICONTROL Max Session Size in Admin]** — 限制工作階段大小上限（位元組）。 使用`0`來停用。
- **[!UICONTROL Max Session Size in Storefront]** — 限制工作階段大小上限（位元組）。 使用`0`來停用。

>[!TIP]
>
>這兩個設定都是以位元組來測量，預設值為`256000`位元組（或256 KB）。

**_若要設定工作階段大小上限：_**

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Advanced]**&#x200B;並選擇&#x200B;**[!UICONTROL System]**。

1. 展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Security]**&#x200B;區段以存取工作階段設定。

   ![工作階段設定](../configuration-reference/advanced/assets/system-security.png){width="600" zoomable="yes"}

1. 輸入新的工作階段大小（位元組）。

   >[!WARNING]
   >
   >將值設定得太低可能會造成問題。 如果您將其中一個選項設定在預設值256000位元組下方，您會看到警告訊息。 如果您按一下&#x200B;**[!UICONTROL No]**，系統會將值變更為`256000`。

1. 按一下&#x200B;**[!UICONTROL Save Config]**。

### 管理員工作階段

僅[!BADGE 個PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"}

如果超過工作階段大小上限，則會顯示錯誤訊息，且系統會將工作階段大小限制記錄到`var/log`目錄。

如果您在設定工作階段大小太低後失去管理員的存取權，請使用CLI重設設定：

```bash
bin/magento config:set system/security/max_session_size_admin 256000
```

### 店面工作階段

僅[!BADGE 個PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"}

如果超過工作階段大小上限，則不會顯示錯誤，但系統會將工作階段大小限制記錄到`var/log`目錄。

## 工作階段驗證

Adobe Commerce和Magento Open Source可讓您驗證工作階段變數，藉此防範可能的工作階段固定攻擊，或嘗試毒害或劫持使用者工作階段。 「工作階段驗證設定」會決定工作階段變數在每次商店造訪期間的驗證方式，以及工作階段ID是否包含在商店的URL中。

如需技術資訊，請參閱&#x200B;_組態指南_&#x200B;中的[使用工作階段存放區的Redis](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/redis/redis-session.html)。

![一般設定 — Web工作階段驗證](../configuration-reference/general/assets/web-session-validation-settings.png){width="600" zoomable="yes"}

驗證會比較驗證變數中的值與為使用者儲存在`$_SESSION`資料中的工作階段資料，以檢查訪客的真實身分。 如果資訊未如預期傳輸，且對應的變數為空白，則驗證會失敗。 根據工作階段驗證設定，如果工作階段變數在驗證程式失敗時，使用者端工作階段會立即終止。

啟用所有驗證變數有助於防止攻擊，但也可能影響伺服器的效能。 依預設，會停用所有工作階段變數驗證。 建議您嘗試設定，以找出適合安裝Adobe Commerce或Magento Open Source的最佳組合。 啟用所有驗證變數可能會過度限制，而且可能會讓客戶的網際網路連線無法通過Proxy伺服器或來自防火牆後的客戶無法存取。 若要深入瞭解工作階段變數及其使用，請參閱Linux®系統的系統管理檔案。

**_若要設定工作階段驗證：_**

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;_[!UICONTROL General]_並選擇&#x200B;**[!UICONTROL Web]**。

1. 展開&#x200B;**[!UICONTROL Session Validation Settings]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

1. 設定每個組態選項：

   - **[!UICONTROL Validate REMOTE_ADDR]** — 設定為`Yes`以確認要求的IP位址符合儲存在`$_SESSION`變數中的內容。

   - **[!UICONTROL Validate HTTP_VIA]** — 設定為`Yes`以驗證傳入要求的Proxy位址是否符合`$_SESSION`變數中儲存的內容。

   - **[!UICONTROL Validate HTTP_X_FORWARDED_FOR]** — 設為`Yes`，以確認要求的轉寄地址符合`$_SESSION`變數中儲存的內容。

   - **[!UICONTROL Validate HTTP_USER_AGENT]** — 設為`Yes`，驗證工作階段期間用來存取存放區的瀏覽器或裝置是否符合`$_SESSION`變數中儲存的內容。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

## 管理員工作階段存留期

做為安全性測量，_Admin_&#x200B;最初設定為在鍵盤閒置900秒（15分鐘）後逾時。 您可以調整工作階段的存留期，以符合您的工作風格。

**_若要調整管理員工作階段存留期：_**

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 向下捲動並展開左側面板中的&#x200B;**[!UICONTROL Advanced]**。

1. 按一下&#x200B;**[!UICONTROL Admin]**。

1. 展開&#x200B;**[!UICONTROL Security]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

1. 針對&#x200B;**[!UICONTROL Admin Session Lifetime (seconds)]**，輸入工作階段在逾時前保持作用中狀態的秒數。

   ![進階設定 — 系統管理員安全性設定](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。
