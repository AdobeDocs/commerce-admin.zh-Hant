---
title: 儲存URL
description: 瞭解商店URL以及如何設定基本URL和商店程式碼。
exl-id: dd7a6317-b0cf-4d0c-9b31-a963c467026b
feature: Site Management, System
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hant/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '1529'
ht-degree: 0%

---

# 儲存URL

Adobe Commerce或Magento Open Source安裝中的每個網站都有指派給店面的基底URL，以及指派給管理員的另一個URL。 Adobe會使用變數來定義與基底URL相關的內部連結，如此一來，您便可將整個商店從一個位置移至另一個位置，而不需更新連結。 標準基底URL以`http`開頭，安全基底URL以`https`開頭。

- **基底URL** — `http://www.yourdomain.com/magento/`
- **安全基底URL** — `https://www.yourdomain.com/magento/`
- **IP位址為**&#x200B;的URL — `http://###.###.###.###/magento/`或`https://###.###.###.###/magento/`

>[!IMPORTANT]
>
>請勿從預設的基本URL設定變更管理員URL。 若要變更管理員URL或路徑，請參閱[使用自訂管理員URL](#use-a-custom-admin-url)。

## 使用安全通訊協定

商店的基本URL最初是在Adobe Commerce安裝期間設定的。 如果當時有可用的安全性憑證，您可以指定要用於存放區、管理員或兩者的`HTTPS`個URL。 如果您的Adobe Commerce安裝包含多個商店，或您打算稍後新增更多商店，您可以在URL中包含商店程式碼。 所有Adobe資源和作業都可透過安全通訊協定使用。

如果在安裝時沒有可用於網域的安全性憑證，請確保在啟動存放區之前更新設定。 為您的網域建立安全性憑證後，您可以設定兩個或其中一個基本URL以使用加密的安全通訊端層(SSL)和[傳輸層安全性][1] (TLS)通訊協定來運作。

>[!IMPORTANT]
>
>Adobe強烈建議您使用安全通訊協定來傳輸生產網站的所有頁面，包括內容和產品頁面。

根據預設，Adobe Commerce和Magento Open Source可設定為傳送超過`HTTPS`的所有頁面。 如果您的存放區已使用標準通訊協定執行，您可以啟用[HTTP Strict Transport Security][2] (HSTS)並升級任何不安全的頁面要求，藉此提高安全性。 HSTS是一種選擇加入通訊協定，可防止瀏覽器針對指定的網域轉譯以不安全通訊協定傳輸的標準`HTTP`頁面。 因為搜尋引擎可能已使用標準`HTTP` URL索引您商店的每個頁面，您可以設定Commerce自動將任何不安全的頁面請求升級為`HTTPS`，這樣您就不會遺失任何流量。 當Commerce設定為對店面和管理員使用安全URL時，會出現兩個額外的欄位，可讓您啟用`HSTS`。

## 設定基底URL

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板的&#x200B;_一般_&#x200B;底下，選擇&#x200B;**[!UICONTROL Web]**。

1. 展開&#x200B;**[!UICONTROL Base URL]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   - **[!UICONTROL Base URL]** — 輸入商店的完整基底URL。 請務必以正斜線結束URL，以便使用商店中的其他URL金鑰進行擴充。 例如： `http://yourdomain.com/`

     >[!NOTE]
     >
     >請勿變更&#x200B;_[!UICONTROL Base Link URL]_&#x200B;欄位中的預留位置。 它是用來建立基本URL相對連結的預留位置。

   - **[!UICONTROL Base URL for Static View Files]** — （選擇性）輸入以下列預留位置開頭的路徑，為靜態檢視檔案的基本URL指定替代位置：

     \{\{unsecure_base_url}}

   - **[!UICONTROL Base URL for User Media Files]** — （選擇性）輸入以下列預留位置開頭的路徑，指定使用者媒體檔案基底URL的替代位置：

     \{\{unsecure_base_url}}

     對於一般安裝，不需要更新靜態檢視檔案或媒體檔案的路徑，因為它們是相對於基底URL的路徑。

   ![一般設定 — 網頁基底URL](../configuration-reference/general/assets/web-base-urls.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >以雙大括弧括住的預留位置是變數的標籤標籤。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

## 設定安全基底URL

如果您的網域具有有效的安全性憑證，您可以設定店面和管理員的URL，以透過安全(https)通道傳輸資料。 沒有有效的安全性憑證，您的存放區就無法使用安全(SSL/TLS)通訊協定運作。

1. 展開![擴充選擇器](../assets/icon-display-expand.png) _[!UICONTROL Base URLs (Secure]_&#x200B;區段，然後執行下列動作：

   ![一般設定 — 安全基底URL](../configuration-reference/general/assets/web-base-urls-secure.png){width="600" zoomable="yes"}

   - **[!UICONTROL Secure Base URL]** — 輸入完整的安全基底URL，後跟正斜線。 例如： `https://yourdomain.com/`

   - **[!UICONTROL Secure Base Link URL]** — 請勿變更安全基底連結URL欄位中的預留位置。 它可用來建立安全基底URL的相對連結。

   - **[!UICONTROL Secure Base URL for Static View Files]** — （選擇性）輸入以下列預留位置開頭的路徑，為靜態檢視檔案的安全基底URL指定替代位置：

     \{\{secure_base_url}}

   - **[!UICONTROL Secure Base URL for User Media Files]** — （選擇性）輸入以下列預留位置開頭的路徑，指定使用者媒體檔案的安全基底URL的替代位置：

     \{\{secure_base_url}}

1. 若要增強安全性，請將下列兩個選項設定為`Yes`。

   - **[!UICONTROL Use Secure URLs on Storefront]**
   - **[!UICONTROL Use Secure URLs in Admin]**

1. 針對&#x200B;_[!UICONTROL Enhanced Security Settings]_，請執行下列動作：

   - **[!UICONTROL Enable HTTP Strict Transport Security (HSTS)]** — 如果您希望商店只顯示安全的HTTPS頁面要求，請設為`Yes`。

   - **[!UICONTROL Upgrade Insecure Requests]** — 若要升級任何標準不安全HTTP頁面的要求以保護HTTPS，請設定為`Yes`。

1. 設定伺服器的&#x200B;**[!UICONTROL Offloader Header]**。

   大部分的Commerce安裝都使用預設的`X-Forward-Proto`來將通訊協定識別為`HTTP`或`HTTPS`。 如果您的伺服器設定使用不同的offloader_header，請在此處輸入它。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

## 在URL中包含商店代碼

>[!NOTE]
>
>當&#x200B;_將存放區代碼新增至URL_&#x200B;選項設為`Yes`時，您必須在瀏覽器URL中包含存放區代碼。 此設定可確保URL重寫正確對應，並且成功開啟所有頁面，沒有&#x200B;_「404找不到頁面」_&#x200B;錯誤。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板的&#x200B;_[!UICONTROL General]_&#x200B;下，選擇&#x200B;**[!UICONTROL Web]**。

1. 展開&#x200B;**[!UICONTROL URL Options]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

1. 將&#x200B;**[!UICONTROL Add Store Code]**&#x200B;設定為您的偏好設定：

   - **[!UICONTROL URL with Store Code]**： `http://www.yourdomain.com/magento/[store-code]/index.php/url-identifier`
   - **[!UICONTROL URL without Store Code]**： `http://www.yourdomain.com/magento/index.php/url-identifier`

   ![一般設定 — 網頁URL選項](../configuration-reference/general/assets/web-url-options.png){width="600" zoomable="yes"}

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

1. 按一下工作區頂端訊息中的&#x200B;**[!UICONTROL Cache Management]**&#x200B;連結。 然後，按照指示重新整理快取。

   ![快取管理訊息](./assets/msg-cache-management.png)

## url疑難排解

如果依照設定指示後，某些頁面仍會以不安全的URL (`http://`)提供服務，請執行下列動作：

- 將（不安全）基底URL變更為安全HTTPS URL。
- 在伺服器上編輯`.htaccess`檔案（或負載平衡器），以便將不安全URL重新導向至安全URL。

## 使用自訂管理員URL

根據[安全性最佳實務](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html?lang=zh-Hant)，Adobe建議您使用唯一的管理員URL，而非預設的&#x200B;_管理員_&#x200B;或常用辭彙（例如&#x200B;_後端_）。 雖然這不會直接保護您的網站不受確定性不良行為者的傷害，但可以減少嘗試獲得未經授權存取的指令碼暴露。

>[!NOTE]
>
>在實作自訂管理員URL之前，請洽詢您的託管提供者。 有些託管提供者會要求標準URL符合防火牆保護規則。

在典型的安裝中，管理員URL和路徑會緊接在基本URL後面。 管理路徑是根目錄下的一個目錄。

- **預設基底URL**： `http://yourdomain.com/magento/`
- **預設管理路徑**： `admin`
- **預設管理員URL和路徑**： `http://yourdomain.com/magento/admin`

雖然可以變更管理員URL和路徑至其他位置，但只要發生任何錯誤，系統就會移除對管理員的存取權，而必須從伺服器加以更正。

>[!NOTE]
>
>除非您知道如何編輯伺服器上的組態檔，否則請勿嘗試自行變更管理員URL，以防萬一。 針對部署在雲端基礎結構上的Adobe Commerce專案，請依照&#x200B;*雲端基礎結構上的Adobe Commerce指南*&#x200B;中的[指示](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/env/stage/variables-admin.html?lang=zh-Hant#admin-url)變更管理員URL。

### 方法1：從管理員變更

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Advanced]**&#x200B;並選擇&#x200B;**[!UICONTROL Admin]**。

1. 展開&#x200B;**[!UICONTROL Admin Base URL]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

1. 設定自訂URL的組態選項：

   ![進階設定 — Admin基底URL](../configuration-reference/advanced/assets/admin-admin-base-url.png){width="600" zoomable="yes"}

   如有需要，請清除&#x200B;**[!UICONTROL Use system value]**&#x200B;核取方塊以變更設定。

   - 將&#x200B;**[!UICONTROL Use Custom Admin URL]**&#x200B;設為`Yes`。

   - 輸入&#x200B;**[!UICONTROL Custom Admin URL]**： `http://yourdomain.com/magento/`

     >[!NOTE]
     >
     >管理員URL必須位於相同的Commerce安裝中，並與店面具有相同的檔案根目錄。

   - 將&#x200B;**[!UICONTROL Custom Admin Path]**&#x200B;設為`Yes`。

   - 針對&#x200B;**[!UICONTROL Custom Admin Path]**，輸入用來作為自訂管理資料夾名稱的路徑。

     範例： `sample_custom_admin`

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

1. 儲存變更後，請登出管理員，並使用新的管理員URL和路徑重新登入。

### 方法2：從伺服器命令列變更管理路徑

1. 在文字編輯器中開啟`app/etc/env.php`檔案，並變更`backend`區段的`frontName`引數值。 然後，儲存檔案。

   請務必只使用小寫字元。

   >[!NOTE]
   >
   >   此方法可讓您變更管理員路徑，但無法變更管理員URL。

   >[!TIP]
   >
   >針對雲端基礎結構上的Adobe Commerce，您可以使用Cloud UI中的`ADMIN_URL`變數來設定自訂管理路徑。 請參閱&#x200B;_雲端基礎結構上的Commerce指南_&#x200B;中的[管理員變數主題](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/env/stage/variables-admin.html?lang=zh-Hant)。

   - **預設管理路徑**

     ```php?start_inline=1
     'backend' => [
      'frontName' => 'admin'
     ],
     ```

   - **新管理員路徑**

     ```php?start_inline=1
     'backend' => [
         'frontName' => 'backend'
     ],
     ```

1. 使用下列其中一種方法來清除快取：

   - 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**。 然後，按一下&#x200B;**[!UICONTROL Flush Magento Cache]**。
   - 在伺服器上，執行下列動作：

     ```bash
     php bin/magento cache:flush
     ```

   >[!NOTE]
   >
   >使用方法1所做的變更優先於`app/etc/env.php`檔案中所做的變更。

### 方法3：使用Commerce CLI變更管理員路徑

您可以使用CLI `setup:config:set`命令來變更管理路徑。 下列範例使用`--backend-frontname`選項將路徑從Commerce根目錄變更為新的管理員路徑：

```bash
bin/magento setup:config:set --backend-frontname="backend_front_name"
```

此命令會更新`app/etc/env.php`檔案中的`backend` > `frontName`組態選項。

## 還原預設管理員URL和管理員路徑

如果您設定了無效的管理員URL或管理路徑，但失去對後端的存取權，則有辦法從命令列修正它。

1. 若要還原成預設的Admin URL，請執行此命令：

   ```bash
   php bin/magento config:set admin/url/use_custom 0
   ```

1. 若要還原為預設管理路徑（在`app/etc/env.php`中設定，如方法2所述），請執行此命令：

   ```bash
   php bin/magento config:set admin/url/use_custom_path 0
   ```

1. 使用下列其中一種方法來清除快取：

   - 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**。 然後，按一下&#x200B;**[!UICONTROL Flush Magento Cache]**。
   - 在伺服器上，執行下列動作：

     ```bash
     php bin/magento cache:flush
     ```


[1]: https://en.wikipedia.org/wiki/Transport_Layer_Security
[2]: https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security
