---
title: Cookie法規遵循
description: 為了跟上許多國家/地區有關使用Cookie的法規，Adobe Commerce和Magento Open Source為商家提供多種取得客戶同意的方法。
exl-id: 42df20cd-50a7-4618-98fd-9ced936e305b
feature: Compliance
source-git-commit: ae43d97bb3031a06ce6a0211ee304aae53e4eb08
workflow-type: tm+mt
source-wordcount: '2105'
ht-degree: 0%

---

# Cookie法規遵循

Cookie是儲存在網站每位訪客的電腦中，並作為資訊的暫存地點的小檔案。 儲存在Cookie中的資訊可用來個人化購物體驗、將訪客連結至其購物車、測量流量模式，以及改善促銷活動的有效性。 為了跟上許多國家/地區有關使用Cookie的法規，Adobe Commerce和Magento Open Source為商家提供多種取得客戶同意的方法。 如需Adobe Commerce和Magento Open Source中的預設Cookie清單，[Cookie參考](#default-cookies)。

>[!NOTE]
>
>如果您修改預設的[Google隱私權設定](../merchandising-promotions/google-tools.md#google-privacy-settings)以符合[一般資料保護規範](compliance-gdpr.md)，則使用Google AnalyticsCookie時不需要取得使用者同意。

## 方法1：默示同意

默示同意表示您商店的訪客已清楚瞭解Cookie是作業的必要部分，而使用您的網站即間接授與使用這些內容的許可權。 取得隱含同意的關鍵是提供足夠的資訊讓訪客做出明智的決定。 許多商店會在所有標準頁面頂端顯示訊息，概要說明Cookie的使用方式，並附上商店隱私權政策的連結。 隱私權原則應說明您的商店收集到的資訊型別及其使用方式。

## 方法2：表示同意

在&#x200B;_Cookie限制模式_&#x200B;中操作您的商店時，訪客必須先表示同意，才能將任何Cookie儲存到其電腦。 除非獲得同意，否則您商店的許多功能都無法使用。 例如，如果Google Analytics可供您的商店使用，則只有在訪客授予使用Cookie的許可權後，才能叫用該量度。

## Cookie限制模式

啟用Cookie限制模式時，系統會通知您商店的訪客，要求使用Cookie才能進行完整功能的操作。 根據您的佈景主題，訊息可能會顯示在頁首上方、頁尾下方或頁面上的其他位置。 此訊息會連結至您的隱私權政策，以取得詳細資訊，並鼓勵訪客按一下「允許」按鈕來授予同意。 取得同意後，訊息會消失。

您的[隱私權原則](privacy-policy.md))應包含商店名稱和連絡資訊，並說明商店使用的每個Cookie的用途。 若要深入瞭解，請參閱[Cookie參考](#default-cookies)。

>[!NOTE]
>
>如果您變更隱私權原則的URL金鑰，您也必須建立自訂URL重寫，以將流量重新導向至新的URL金鑰。 否則，Cookie限制模式訊息中的連結會傳回`404 Page Not Found`。

![店面範例 — Cookie限制通知](./assets/storefront-cookie-restriction-message.png){width="600"}

### 步驟1：啟用Cookie限制模式

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側導覽面板的&#x200B;**[!UICONTROL General]**&#x200B;下，選擇&#x200B;**[!UICONTROL Web]**。

1. 展開&#x200B;**[!UICONTROL Default Cookie Settings]**&#x200B;區段並執行下列動作：

   ![網頁組態 — 預設Cookie設定](./assets/web-default-cookie-settings.png){width="600"}

   - 以秒為單位輸入&#x200B;**[!UICONTROL Cookie Lifetime]**。

   - 如果您要讓Cookie可供其他資料夾使用，請輸入&#x200B;**[!UICONTROL Cookie Path]**。 若要讓Cookie在網站的任何位置都可使用，請輸入正斜線(`/`)。 此值只能包含Cookie路徑，且&#x200B;**_不能_**&#x200B;包含任何其他Cookie引數。

   - 若要讓Cookie可用於子網域，請在&#x200B;**[!UICONTROL Cookie Domain]**&#x200B;欄位(`subdomain.yourdomain.com`)中輸入子網域名稱。 若要讓Cookie可用於所有子網域，請輸入開頭為句點(`.yourdomain.com`)的網域名稱。 此值只能包含Cookie網域，且&#x200B;**_不能_**&#x200B;包含任何其他Cookie引數。

   - 若要防止指令碼語言(例如JavaScript)存取Cookie，請確定&#x200B;**僅使用HTTP**&#x200B;設定為`Yes`。

   - 將&#x200B;**[!UICONTROL Cookie Restriction Mode]**&#x200B;設為`Yes`。

     如有必要，請清除核取方塊，然後按一下&#x200B;**[!UICONTROL OK]**&#x200B;以確認範圍切換。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

1. 當提示更新快取時，請按一下系統訊息中的&#x200B;**[!UICONTROL Cache Management]**&#x200B;連結。 接著，重新整理每個無效的快取。

### 步驟2：更新您的隱私權原則

更新您的[隱私權原則](privacy-policy.md)，以反映貴公司收集的資訊及使用方式。

## 預設Cookie

Adobe Commerce和Magento Open Source中的預設Cookie會分類為「劐免/不劐免」，以協助商家符合隱私權法規（例如[GDPR](compliance-gdpr.md)）的要求。 商戶應將此資訊作為指引，並諮詢法律顧問，以更新其隱私權和Cookie政策，作為全面隱私權法規遵循策略的一部分。

[!DNL Commerce]會將下列Cookie用於內部部署和雲端安裝，且此為立即可用。 客戶明確要求的功能可能會需要這些Cookie。 若要瞭解工作階段Cookie的期限，請參閱[工作階段期限](../customers/customer-online-options.md)。

其中一些Cookie可能會視需要提供設定選項，包括啟用/停用。

### 要求的功能Cookie （免費）


#### `add_to_cart`

![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)由Google Tag Manager使用。 擷取從購物車移除的產品SKU、名稱、價格和數量，並讓該資訊可供第三方指令碼未來整合。

#### `guest-view`

儲存訪客購物者用來擷取其訂單狀態的訂單ID。 訪客訂單檢視。 用於&#x200B;_[!DNL Orders and Returns]_Widget。

- 是否安全？ 否
- 僅限HTTP：是
- 到期原則：工作階段
- 模組： `Magento_Sales`

#### `login_redirect`

保留在導向客戶登入之前載入的目的地頁面。 如果[顯示迷你購物車](../stores-purchase/cart-configuration.md#mini-cart)組態選項設為`Yes`，則登入重新導向會與迷你購物車搭配使用。

- 是否安全？ 否
- 僅限HTTP：否
- 到期原則：工作階段
- 模組： `Magento_Customer`

#### `mage-banners-cache-storage`

![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)將橫幅內容儲存在本機，以改善效能。

#### `mage-messages`

追蹤顯示給使用者的錯誤訊息和其他通知，例如Cookie同意訊息和各種錯誤訊息。 訊息向購物者顯示後，就會從Cookie中刪除。

沒有選項可停用此Cookie。

- 是否安全？ 否
- 僅限HTTP：否
- 到期原則：持續時間1年。 對使用者顯示訊息時，已在前端清除。
- 模組： `Magento_Theme`

#### `mage-translation-storage` （本機儲存體）

當購物者要求時儲存翻譯的內容。 當[翻譯策略](../configuration-reference/advanced/developer.md)設定為「字典（店面翻譯）」時使用。

- 是否安全？ 否
- 僅限HTTP：否
- 到期原則：每個本機儲存體規則
- 模組： `Magento_Translation`

#### `mage-translation-file-version` （本機儲存體）

追蹤本機儲存體中的翻譯版本。 當[翻譯策略](../configuration-reference/advanced/developer.md)設定為`Dictionary (Translation on Storefront side)`時使用。

- 是否安全？ 否
- 僅限HTTP：否
- 到期原則：每個本機儲存體規則
- 模組： `Magento_Translation`

#### `product_data_storage` （本機儲存體）

儲存與最近檢視/比較的產品相關的產品資料設定。

- 是否安全？ 否
- 僅限HTTP：否
- 到期原則：每個本機儲存體規則
- 模組： `Magento_Catalog`

#### `recently_compared_product` （本機儲存體）

儲存最近比較產品的產品ID。

- 是否安全？ 否
- 僅限HTTP：否
- 到期原則：每個本機儲存體規則
- 模組： `Magento_Catalog`

#### `recently_compared_product_previous` （本機儲存體）

儲存先前比較產品的產品ID以方便瀏覽。

- 是否安全？ 否
- 僅限HTTP：否
- 到期原則：每個本機儲存體規則
- 模組： `Magento_Catalog`

#### `recently_viewed_product` （本機儲存體）

儲存最近檢視之產品的產品ID以方便瀏覽。

- 是否安全？ 否
- 僅限HTTP：否
- 到期原則：每個本機儲存體規則
- 模組： `Magento_Catalog`

#### `recently_viewed_product_previous` （本機儲存體）

儲存最近檢視過產品的產品ID，方便瀏覽。

- 是否安全？ 否
- 僅限HTTP：否
- 到期原則：每個本機儲存體規則
- 模組： `Magento_Catalog`

#### `remove_from_cart`

![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)由[Google Tag Manager](../merchandising-promotions/google-tag-manager.md)使用。 擷取新增到購物車的產品SKU、名稱、價格和數量，並讓該資訊可供第三方指令碼未來整合。

#### `stf`

記錄SendFriend （[傳送電子郵件給Friend](../stores-purchase/email-a-friend.md)）模組傳送訊息的時間。

- 是否安全？ 是
- 僅限HTTP：是
- 到期原則：工作階段
- 模組： `Magento_SendFriend`

#### `X-Magento-Vary`

組態設定可改善使用清漆靜態內容快取時的效能。

- 是否安全？ 是
- 僅限HTTP：是
- 到期原則：根據PHP設定session.cookie_lifetime
- 模組： `Magento_PageCache`

#### `form_key`

一種安全性措施，可在所有表單提交中附加隨機字串，以保護資料免受跨網站請求偽造(CSRF)的影響。

- 是否安全？ 否
- 僅限HTTP：否
- 到期原則：
   - PHP：根據PHP設定session.cookie_lifetime
   - JS：工作階段
- 模組：頁面快取

#### `mage-cache-sessid`

此Cookie的值會觸發本機快取存放區的清理。 當後端應用程式移除Cookie時，管理員會清理本機儲存空間，並將Cookie值設定為`true`。

- 是否安全？ 否
- 僅限HTTP：否
- 到期原則：工作階段
- 模組： `Magento_Customer`

#### `mage-cache-storage`

訪客特定內容的本機儲存，可啟用電子商務功能。

- 是否安全？ 否
- 僅限HTTP：否
- 到期原則：工作階段
- 模組： `Magento_Customer`，`Magento_Persistent`

#### `mage-cache-storage` （本機儲存體）

訪客特定內容的本機儲存，可啟用電子商務功能。

- 是否安全？ 否
- 僅限HTTP：否
- 到期原則：工作階段
- 模組： `Magento_Customer`，`Magento_Persistent`，`Magento_NegotiableQuote`

#### `mage-cache-storage-section-invalidation` （本機儲存體）

強制本機儲存應失效的特定內容區段。

- 是否安全？ 否
- 僅限HTTP：否
- 到期原則：每個本機儲存體
- 模組： `Magento_Customer`

#### `persistent_shopping_cart`

儲存永久性購物車的金鑰(ID)，以便能夠為匿名購物者還原購物車。

- 是否安全？ 是
- 僅限HTTP：是
- 到期原則：根據[持續性購物車](../stores-purchase/cart-persistent.md) — 持續性存留期（秒）設定
- 模組： `Magento_Persistent`

#### `private_content_version`

將隨機、唯一的數字和時間附加至包含客戶內容的頁面，以防止在伺服器上快取這些頁面。

它設定在多個位置：在PHP中、在JavaScript中作為Cookie，以及在JavaScript中設定為本機儲存。

若為HTTP Only=`Yes` （根據要求），這表示若在HTTPS要求期間設定Cookie是安全的，若在HTTP要求期間設定，則為不安全。

- 是否安全？ `Yes` （根據要求），`No`
- 僅限HTTP： `No`
- 到期原則：根據[持續性購物車](../stores-purchase/cart-persistent.md) — 持續性存留期（秒）設定
   - PHP： `1`年/ `315360000s` （十年）
   - JS： `1`天
   - JS本機儲存體：每個本機儲存體規則（永久）
- 模組： `Magento_PageCache`，`Magento_Customer`

#### `section_data_ids`

儲存與購物者啟動動作相關的客戶特定資訊，例如願望清單顯示和結帳資訊。

- 是否安全？`No`
- 僅限HTTP： `No`
- 到期原則： `Session`
- 模組： `Magento_Customer`

#### `store`

追蹤購物者選取的特定商店檢視/地區設定。

- 是否安全？`No`
- 僅限HTTP： `Yes`
- 到期原則： `1`年
- 模組： `Magento_Store`

#### `mage-banners-cache-storage` — 本機存放區

![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)橫幅功能的本機儲存。

- 是否安全？`No`
- 僅限HTTP： `No`
- 到期原則：每個本機儲存體規則
- 模組： `Magento_Banner`

## Google AnalyticsCookie

[Google Analytics](../merchandising-promotions/google-analytics.md)或Google Universal Analytics已完整啟用您的安裝時，會使用下列Cookie。 若要停用這些Cookie以符合隱私權法規，請參閱[Google隱私權設定](../merchandising-promotions/google-tools.md#google-privacy-settings)。 若要深入瞭解，請參閱網站上的[Google AnalyticsCookie使用情形][1]。

### Google Universal Analytics Cookie — 非劐免

![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce) JavaScript資料庫： `gtag.js`和`analytics.js`

- `_ga`：區分您網站的訪客。
- `_gid`：區分您網站的訪客。
- `gat`：用來節流要求速率。
- `dc_gtm_<property-id>`：使用[Google Tag Manager](../merchandising-promotions/google-tag-manager.md)部署Google Analytics時的節流要求速率。
- `AMP_TOKEN`：包含可用來從AMP使用者端ID服務擷取使用者端ID的權杖。 其他可能的值包括選擇退出、即時要求，或從AMP使用者端ID服務擷取使用者端ID時發生錯誤。
- `_gac_<property-id>`：包含使用者的行銷活動相關資訊。 如果Google Analytics連結至您的[AdWords][2]帳戶，則Google AdWords轉換標籤會讀取此Cookie。

### Google AnalyticsCookie — 非劐免

![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce) JavaScript資料庫： `ga.js`

- `__utma`：區分購物者和工作階段。 此Cookie是在JavaScript程式庫執行時建立，而且沒有現有的`__utma` Cookie。 每次將資料傳送至Google Analytics時，Cookie都會更新。
- `__utmt`：用來節流要求速率。
- `__utmb`：決定新的工作階段/造訪。 此Cookie是在JavaScript程式庫執行時建立，而且沒有現有的`__utmb` Cookie。 每次將資料傳送至Google Analytics時，Cookie都會更新。
- `_utmz`：儲存流量來源或行銷活動，說明購物者如何到達您的網站。 Cookie會在JavaScript程式庫執行時建立，並會在每次將資料傳送至Google Analytics時更新。
- `__utmv`：儲存訪客層級的自訂變數資料。 此Cookie是在開發人員搭配訪客層級自訂變數使用`_setCustomVar`方法時建立。 每次將資料傳送至Google Analytics時，都會更新此Cookie。

## 產品Recommendations Cookie

![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)產品Recommendations會為Adobe Commerce客戶使用下列Cookie。 這些Cookie與[DataServices模組](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure.html)一起安裝。

- `mg_dnt`：如果您有管理網站上之Cookie同意的自訂程式碼，可讓您[限制Adobe Commerce資料收集](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/developer/setting-cookie.html)。
- `user_allowed_save_cookie`：用於[Cookie限制模式](#cookie-restriction-mode)。
- `authentication_flag`：指出購物者是否已登入或登出。 此Cookie與`dataservices_customer_id` Cookie同時更新。
- `dataservices_customer_id`：指出購物者是否已登入或登出。 此Cookie包含系統中的客戶唯一ID。
- `dataservices_customer_group`：表示客戶的群組。 此Cookie儲存為客戶群組識別碼的[sha1](https://en.wikipedia.org/wiki/SHA-1)總和檢查碼。
- `dataservices_cart_id`：識別購物者的購物車動作。 此Cookie包含系統中客戶的唯一購物車ID。
- `dataservices_product_context`：識別購物者的產品互動。 此Cookie包含系統中客戶的唯一報價ID。

## 其他Cookie

![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)已為Adobe Commerce客戶設定下列Cookie。 這些Cookie與[DataServices模組](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure.html)一起安裝。

- `mg`：由Snowplow JavaScript追蹤器設定。 如需詳細資訊，請參閱[雪犁檔案](https://docs.snowplow.io/docs/collecting-data/collecting-from-own-applications/javascript-trackers/javascript-tracker/javascript-tracker-v3/tracker-setup/initialization-options)。
- `com.adobe.alloy.getTld`：根據目前網頁的主機名稱，這是不是如https://publicsuffix.org中所述「公用字尾」的最上層網域。 基本上，這是可以接受Cookie的最上層網域。 此Cookie是[Alloy Web SDK](https://github.com/adobe/alloy)的一部分。

[1]: https://developers.google.com/analytics/devguides/collection/analyticsjs/cookie-usage
[2]: https://support.google.com/adwords/answer/7521212
