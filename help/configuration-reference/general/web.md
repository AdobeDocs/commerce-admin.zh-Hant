---
title: '[!UICONTROL General] &amp；gt； [!UICONTROL Web]'
description: 檢閱Commerce管理員的[!UICONTROL General] &amp；gt； [!UICONTROL Web]頁面上的組態設定。
exl-id: 1809b03a-a55c-41b4-947b-f66f4bd290a1
feature: Site Management, Configuration
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '1793'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL Web]

{{config}}

## [!UICONTROL URL Options]

![網頁>一般選項](./assets/web-url-options.png)<!-- zoom -->

<!-- [URL Options configuration settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/site-store/store-urls) -->

| 欄位 | 範圍 | 說明 |
|  ---  |  ---  |  ---  |
| [!UICONTROL Add Store Code to URLs] | 全域 | 如果啟用了「網頁伺服器重寫」，請在URL中插入目前檢視的「商店代碼」。 選項： `Yes` / `No`。 <br />當此欄位設為`Yes`時，您必須在瀏覽器URL中包含存放區代碼，以確保URL重寫正確對應且所有頁面都成功開啟。 這可避免&#x200B;_404找不到頁面_&#x200B;錯誤。 |
| [!UICONTROL Auto-redirect to Base URL] | 存放區檢視 | （針對單一商店設定）如果您的網站上有中斷的連結，會將流量重新導向至基本URL，而非具有「404找不到頁面」訊息的頁面。 選項：` No` / `Yes (302 Found)` / `Yes (301 Moved Permanently)` <br />**_重要：_**&#x200B;請勿在多存放區設定中使用自動重新導向至基底URL。 |
| [!UICONTROL Catalog media URL format] | 全域 | 定義指派給產品和類別的[URL格式](../../catalog/catalog-urls.md)。 選項：「每個影像變體的唯一雜湊」（舊版模式）會將轉換的檔案名稱定義為唯一的雜湊值。 根據查詢引數的影像最佳化會根據查詢引數定義[影像最佳化](../../content-design/media-gallery-image-optimization.md)程式。 |

{style="table-layout:auto"}

## [!UICONTROL Search Engine Optimization]

![網頁>搜尋引擎最佳化](./assets/web-search-engine-optimization.png)<!-- zoom -->

<!-- [Search Engine Optimization configuration settings](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/seo/url-rewrites/url-rewrite) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Use Web Server Rewrites] | 存放區檢視 | PHP系統通常在根資料夾中包含名為`index.php`的檔案。 依預設，檔案名稱會在URL中顯示在根資料夾名稱后面。 啟用後，系統會從URL中省略`index.php`。 此可用性最佳實務可讓每個URL更加簡潔，並且不會影響效能或網站排名。 選項： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Base URLs]

![網頁>基礎URL](./assets/web-base-urls.png)<!-- zoom -->

<!-- [Base URLS configuration settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/site-store/store-urls) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Base URL] | 存放區檢視 | 未透過加密(SSL)通道執行的Commerce根資料夾完整位址。 URL必須以正斜線結尾。 |
| [!UICONTROL Base Link URL] | 存放區檢視 | 用作基礎URL預留位置的標籤標籤。 |
| [!UICONTROL Base URL for Static View Files] | 存放區檢視 | 指向佈景主題所使用的靜態檔案(例如css、字型、影像和JavaScript)位置的路徑。 預留位置是用來表示基礎URL。 如果您的Commerce安裝有多個網站具有相同的資料夾結構，則每個網站可以有不同的資料夾。 在輸入靜態檢視檔案的基本URL之前，將設定範圍設定為正確的站台。 您也可以在Commerce安裝範圍外指定資料夾。 |
| [!UICONTROL Base URL for User Media Files] | 存放區檢視 | 指向目錄影像和其他媒體檔案位置的路徑。 預留位置是用來表示基礎URL。 如果您的Commerce安裝有多個網站具有相同的資料夾結構，則每個網站可以有不同的媒體資料夾。 如此一來，您就可以分別備份與復原每個媒體資料夾。 您也可以在Commerce安裝範圍外指定媒體資料夾。 |

{style="table-layout:auto"}

## [!UICONTROL Base URLs (Secure)]

![網頁>基礎URL （安全）](./assets/web-base-urls-secure.png)<!-- zoom -->

<!-- [Base URLs (Secure) configuration settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/site-store/store-urls) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Secure Base URL] | 存放區檢視 | 使用加密安全(SSL/TLS)通訊協定傳遞的Commerce根資料夾的完整位址。 URL必須以正斜線結尾。 |
| [!UICONTROL Secure Base Link URL] | 存放區檢視 | 標籤標籤，用來作為在安全通道上執行的基礎URL的預留位置。 |
| [!UICONTROL Secure Base URL for Static View Files] | 存放區檢視 | 指向靜態檔案(例如，佈景主題所使用的CSS、字型、影像和JavaScript)位置的標籤標籤。 檔案可能位於不安全或安全的通道。 如果您的Commerce安裝有多個網站具有相同的資料夾結構，則每個網站可以有不同的資料夾。 在輸入靜態檢視檔案的基本URL之前，將設定範圍設定為正確的站台。 您也可以在Commerce安裝範圍外指定資料夾。 |
| [!UICONTROL Secure Base URL for User Media Files] | 存放區檢視 | 指向目錄影像和其他媒體檔案位置的路徑。 檔案可能位於不安全或安全的通道。 預留位置是用來表示基礎URL。 如果您的Commerce安裝有多個網站具有相同的資料夾結構，則每個網站可以有不同的媒體資料夾。 如此一來，您就可以分別備份與復原每個媒體資料夾。 您也可以在Commerce安裝範圍外指定媒體資料夾。 |
| [!UICONTROL Use Secure URLs on Storefront] | 存放區檢視 | 如果您的網域有安全性憑證，您可以選擇執行店面（使用或不使用SSL加密）。 選項：<br />**`Yes`**— 儲存URL以`https`開頭，表示網頁是以加密的安全通訊協定傳遞。<br />**`No`** — 存放區URL以`http`開頭，表示頁面傳送時沒有安全通訊協定。 |
| [!UICONTROL Use Secure URLs in Admin] | 全域 | 如果您的網域有安全性憑證，您可以選擇執行存放區管理員，使用或不使用SSL加密。 選項： <br />**`Yes`**— 管理員URL以`https`開頭，表示網頁是以加密的安全通訊協定傳遞。<br />**`No`** — 管理員URL以`http`開頭，表示頁面傳送時沒有安全通訊協定。<br />當對存放區和管理員同時啟用安全URL時，會出現兩個額外的欄位以啟用和設定`HSTS`。 |
| [!UICONTROL Enable HTTP Strict Transport Security (HSTS)] | 存放區檢視 | 啟用時，[`HSTS`][1]會針對「中間人」攻擊提供安全性測量，並防止使用者覆寫「無效憑證」訊息。 選項： `Yes` / `No` |
| [!UICONTROL Upgrade Insecure Requests] | 存放區檢視 | 啟用時，將從瀏覽器接收的不安全(`HTTP`)要求轉換為安全(`HTTPS`)通訊協定。 選項： `Yes` / `No` |
| [!UICONTROL Offloader Header] | 全域 | 指定伺服器設定中的`offloader_header`值，以識別使用者端與負載平衡器之間的通訊協定。 大部分的Commerce安裝都使用預設值`X-Forwarded-Proto` (XFP)將通訊協定識別為`HTTP`或`HTTPS`。 |

{style="table-layout:auto"}

## [!UICONTROL Default Pages]

![網頁>預設頁面](./assets/web-default-pages.png)<!-- zoom -->

<!-- [Default Pages configuration settings](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/pages/pages#configure-default-pages) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Default Web URL] | 存放區檢視 | 表示與基底URL關聯的登入頁面。 預設會將此設為「cms」，表示來自Commerce內容管理系統(CMS)的頁面。 您也可以使用不同型別的登陸頁面，例如部落格。 例如，如果部落格安裝在位於`magento/blog`的伺服器上，您可以輸入「部落格」資料夾的名稱，作為選取頁面的相對路徑。 |
| [!UICONTROL CMS Home Page] | 存放區檢視 | 若要選擇商店的首頁，只要從清單中選取CMS頁面即可。 依預設，CMS首頁會列出商店可用的完整CMS頁面選項。 |
| [!UICONTROL Default No-route URL] | 存放區檢視 | 包含您要在發生`404 Page not Found`錯誤時顯示的預設頁面URL。 預設值為`cms/noroute/index`。 |
| [!UICONTROL CMS No Route Page] | 存放區檢視 | 識別發生「404找不到頁面」錯誤時，您想要顯示的特定CMS頁面。 預設頁面為404 Not Found。 |
| [!UICONTROL CMS No Cookies Page] | 存放區檢視 | 會識別未針對瀏覽器啟用Cookie時所顯示的特定CMS頁面。 本頁面說明為何使用Cookie，以及如何為每個瀏覽器啟用。 預設頁面為啟用Cookie。 |
| [!UICONTROL Show Breadcrumbs for CMS Pages] | 存放區檢視 | 判斷階層連結軌跡是否出現在目錄中的所有CMS頁面上。 選項： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Default Layouts]

![預設版面配置](./assets/web-default-layouts.png)<!-- zoom -->

<!--[Default Layouts](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/design/layout/page-layout) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Default Product Layout] | 全域 | 決定預設用於產品頁面的[配置](../../content-design/page-layout.md)。 選項： <br/>**`No layout updates`**— 依預設，產品頁面不提供配置更新。<br/>**`Empty`** — 依預設，產品頁面會使用空白版面配置。 <br/>**`1 column`**— 依預設，會使用產品頁面的單一欄配置。<br/>**`2 columns with left bar`** — 依預設，產品頁面會使用左側邊欄的雙欄版面配置。 <br/>**`2 columns with right bar`**— 預設情況下，對於產品頁面使用右側具側欄的雙欄配置。<br/>**`3 columns`** — 依預設，產品頁面會使用左右兩側有側欄的三欄式配置。<br/>**`Page -- Full Width`**- （需要[!DNL Page Builder]）依預設，會使用產品頁面的「頁面 — 全寬」配置。<br/>**`Category - Full Width`** - （需要[!DNL Page Builder]）依預設，會使用產品頁面的「類別 — 全寬」配置。 <br/>**`Product - Full Width`**- （需要[!DNL Page Builder]）依預設，會使用產品頁面的「產品 — 全寬」配置。 |
| [!UICONTROL Default Category Layout] | 全域 | 決定類別頁面預設使用的[配置](../../content-design/page-layout.md)。 選項： <br/>**`No layout updates`**— 依預設，配置更新不適用於類別頁面。<br/>**`Empty`** — 依預設，類別頁面使用空白版面配置。 <br/>**`1 column`**— 依預設，類別頁面會使用單一欄配置。<br/>**`2 columns with left bar`** — 預設情況下，類別頁面會使用左側邊欄的雙欄版面配置。 <br/>**`2 columns with right bar`**— 預設情況下，類別頁面使用右側具側欄的雙欄配置。<br/>**`3 columns`** — 依預設，類別頁面會使用左右兩側有側欄的三欄式配置。<br/>**`Page - Full Width`**- （需要[!DNL Page Builder]）依預設，會使用類別頁面的「頁面 — 全寬」配置。<br/>**`Category - Full Width`** - （需要[!DNL Page Builder]）依預設，會使用類別 — 完整寬度配置來處理類別頁面。 <br/>**`Product - Full Width`**- （需要[!DNL Page Builder]）依預設，會使用類別頁面的「產品 — 全寬」配置。 |
| 預設頁面配置 | 全域 | 決定預設用於CMS頁面的[配置](../../content-design/page-layout.md)。 選項： <br/>**`No layout updates`**— 依預設，CMS頁面不提供配置更新。<br/>**`Empty`** — 依預設，CMS頁面會使用空白版面配置。 <br/>**`1 column`**— 依預設，會針對CMS頁面使用單一欄配置。<br/>**`2 columns with left bar`** — 依預設，CMS頁面會使用左側邊欄的雙欄版面配置。<br/>**`2 columns with right bar`**— 依預設，CMS頁面會使用右側具側欄的雙欄版面配置。<br/>**`3 columns`** — 依預設，CMS頁面會使用左右兩側有側欄的三欄式配置。<br/>**`Page - Full Width`**- （需要[!UICONTROL Page Builder]）依預設，會使用CMS頁面的「頁面 — 全寬」配置。<br/>**`Category - Full Width`** - （需要[!UICONTROL Page Builder]）依預設，會使用CMS頁面的「類別 — 全寬」配置。 <br/>**`Product - Full Width`**- （需要[!DNL Page Builder]）依預設，會使用CMS頁面的「產品 — 全寬」配置。 |

{style="table-layout:auto"}

## [!UICONTROL Default Cookie Settings]

![網頁>預設Cookie設定](./assets/web-default-cookie-settings.png)<!-- zoom -->

<!-- [Default Cookie configuration settings](https://experienceleague.adobe.com/en/docs/commerce-admin/start/compliance/privacy/compliance-cookie-law) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Cookie Lifetime] | 存放區檢視 | 決定Cookie可以存在多久才會自動刪除。 預設值為3600秒（1小時） |
| [!UICONTROL Cookie Path] | 存放區檢視 | 指定伺服器上可使用Commerce Cookie的資料夾。 若要讓Commerce Cookie可在安裝中的各個位置使用，請將Cookie路徑設定為單一正斜線： `/`。 此值只能包含Cookie路徑，且&#x200B;**_不能_**&#x200B;包含任何其他Cookie引數。 |
| [!UICONTROL Cookie Domain] | 存放區檢視 | 決定Commerce Cookie是否可用於子網域。 例如，若要支援`mysubdomain`.domain.com，請輸入開頭有句號的網域名稱，例如`.domain.com`。 此值只能包含Cookie網域，且&#x200B;**_不能_**&#x200B;包含任何其他Cookie引數。 |
| [!UICONTROL Use HTTP Only] | 存放區檢視 | 決定Commerce Cookie是否只能透過不安全的通道(http)使用，或也可透過加密的通道(https)使用。 選項： `Yes` / `No` |
| [!UICONTROL Cookie Restriction Mode] | 網站 | 判斷是否已啟用Cookie限制模式。 選項： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Session Validation Settings]

![網頁>工作階段驗證](./assets/web-session-validation-settings.png)<!-- zoom -->

<!-- [Session Validation configuration settings](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/security/security-session-management#session-validation) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Validate REMOTE_ADDR] | 全域 | 驗證要求的IP位址是否符合`$_SESSION`資料。 如果偵測到不同的IP位址，工作階段就會終止。 選項： `Yes` / `No` |
| [!UICONTROL Validate HTTP_VIA] | 全域 | 驗證傳入的Proxy資料，並檢查要求的Proxy位址是否符合`$_SESSION`資料。 如果偵測到不同的Proxy位址，工作階段就會終止。 選項： `Yes` / `No` |
| [!UICONTROL Validate HTTP_x_FORWARDED_FOR] | 全域 | 驗證傳出的Proxy資料，並檢查要求的轉送位址是否符合`$_SESSION`資料。 如果偵測到不同的轉送地址，工作階段會終止。 選項： `Yes` / `No` |
| [!UICONTROL Validate HTTP_USER_AGENT] | 全域 | `USER_AGENT`是指用來存取網站的瀏覽器或裝置。 它驗證瀏覽器的名稱和版本以及作業系統是否符合`$_SESSION`資料。 如果在同一工作階段中從一個請求到另一個請求偵測到不同的使用者代理，工作階段會終止。 選項： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Browser Capabilities Detection]

![網頁>瀏覽器功能偵測](./assets/web-browser-capabilities-detection.png)<!-- zoom -->

<!-- [Browser Capabilities Detection configuration settings](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/security/security-browser-capabilities-detection) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Redirect to CMS-page if Cookies are Disabled] | 存放區檢視 | 如果瀏覽器停用Cookie，它會自動重新導向至CMS無Cookie頁面。 選項： `Yes` / `No` |
| [!UICONTROL Show Notice if JavaScript is Disabled] | 存放區檢視 | 如果瀏覽器停用JavaScript，它會顯示通知以提示使用者啟用JavaScript選項： `Yes` / `No` （停用） |
| [!UICONTROL Show Notice if Local Storage is Disabled] | 存放區檢視 | 如果本機快取已停用，則顯示訊息。 選項： `Yes` / `No` |

{style="table-layout:auto"}

[1]: https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html
