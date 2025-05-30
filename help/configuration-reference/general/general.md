---
title: '[!UICONTROL General] &amp；gt； [!UICONTROL General]'
description: 檢閱Commerce管理員的[!UICONTROL General] &amp；gt； [!UICONTROL General]頁面上的組態設定。
exl-id: 67760d24-ad12-4c49-9649-0607c57f5cf0
feature: Configuration, System
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '999'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL General]

{{config}}

## [!UICONTROL Country Options]

如需這些設定欄位和選項的詳細資訊，請參閱[國家選項](../../getting-started/store-details.md#country-options)。

![一般>國家/地區選項](./assets/general-country-options.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Default Country] | 存放區檢視 | 您的商店所在的國家/地區。 |
| [!UICONTROL Allow Countries] | 網站 | 您接受訂單的國家/地區。 |
| [!UICONTROL Zip/Postal Code is Optional for] | 全域 | 運送地址中不需要郵遞區號的國家/地區。 |
| [!UICONTROL European Union Countries] | 全域 | 歐盟成員國家/地區。 |
| [!UICONTROL Top Destinations] | 存放區檢視 | 您鎖定銷售目標的主要國家/地區。 |

{style="table-layout:auto"}

## [!UICONTROL State Options]

請參閱[狀態選項](../../getting-started/store-details.md#state-options)，以取得有關這些設定欄位和選項的詳細資訊。

![一般>狀態選項](./assets/general-state-options.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL State is required for] | 全域 | 要求將地區或州納入郵寄地址的國家/地區（您經營業務的地方）。 |
| [!UICONTROL Allow to Choose State if It is Optional for Country] | 全域 | 若為非必要國家/地區，會判斷&#x200B;_地區/州_&#x200B;欄位是否包含在客戶的郵寄地址中。<br /> <br />**`Yes`**— 在客戶地址中包含&#x200B;_地區/州_欄位，即使該國家/地區不需要該欄位。<br />**`No`** — 若國家/地區不需要，則省略客戶地址中的地區/州欄位。 |

{style="table-layout:auto"}

## [!UICONTROL Locale Options]

請參閱[地區設定選項](../../getting-started/store-details.md#locale-options)，以取得有關這些設定欄位和選項的詳細資訊。

![一般>地區設定選項](./assets/general-locale-options.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Timezone] | 網站 | 網站服務的主要市場的時區。 通常時區與企業實際地點使用的時區相同。 |
| [!UICONTROL Locale] | 存放區檢視 | 商店檢視所提供的市場中所使用的語言、貨幣和測量系統。 |
| [!UICONTROL Weight Unit] | 存放區檢視 | 通常用於來自地區設定的出貨的測量單位。 選項： `lbs` / `kgs` |
| [!UICONTROL First Day of Week] | 存放區檢視 | 這天會被視為商店檢視所提供的市場一週中的第一天。 |
| [!UICONTROL Weekend Days] | 存放區檢視 | 週末在商店景點提供的市場中的日子。 |

{style="table-layout:auto"}

## [!UICONTROL Website Restrictions]

{{ee-feature}}

![一般>網站限制](./assets/general-website-restrictions.png)<!-- zoom -->

如需有關變更這些設定的詳細資訊，請參閱&#x200B;_銷售與促銷指南_&#x200B;中的[存取限制](../../merchandising-promotions/event-configure.md#access-restrictions)。

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Access Restriction] | 網站 | 判斷網站是否以限制模式運作。<br /> <br />**`Yes`**— 網站存取受到下列欄位中設定的方式限制。<br />**`No`** — 已停用限制，且下列設定無效。 |
| [!UICONTROL Restriction Mode] | 網站 | 決定適用於網站的存取限制型別。<br /> <br />**`Website Closed`**— 對店面的所有存取權皆已限制，且店面URL會暫時重新導向至登陸頁面。 此設定在網站維護期間或啟動之前相當實用。<br />**`Private Sales: Login Only`** — 只有註冊客戶才能登入存取店面。 所有店面URL會暫時重新導向至指定的登陸頁面或登入表單。 使用者無法在此模式中建立帳戶。<br />**`Private Sales: Login and Register`**— 使用者必須登入才能存取店面。 所有店面URL會暫時重新導向至登入表單，直到使用者登入為止。 網站處於此模式時，使用者可以註冊帳戶。 |
| [!UICONTROL Startup Page] | 存放區檢視 | 當網站處於「私人銷售」模式時，此設定會決定客戶登入之前顯示的頁面。<br />  <br />**`To login form`**— 系統會將使用者重新導向至登入表單，直到他們登入為止。<br />**`To landing page`** — 系統會將使用者重新導向至下方指定的靜態頁面，直到他們登入為止。<br /> <br />**_重要！_**&#x200B;請務必加入指定登陸頁面之登入頁面的連結，讓客戶可以登入以存取完整網站。 |
| [!UICONTROL Landing Page] | 存放區檢視 | 決定網站處於「私人銷售」模式時顯示的第一個頁面。 |
| [!UICONTROL HTTP Response] | 網站 | 決定當網站關閉且機器人、編目程式或爬蟲程式嘗試連線時傳送的HTTP回應。<br /> <br />**`503 Service unavailable`**— 頁面無法使用，但爬蟲程式不應更新索引。<br />**`200 OK`** — 登入頁面正確，爬蟲應該將其視為網站上的唯一頁面。 |
| [!UICONTROL Enable Autocomplete on login/forgot password forms] | 網站 | 決定&#x200B;_登入_&#x200B;與&#x200B;_忘記密碼_&#x200B;表單上的欄位是否自動填入先前專案。 選項： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Store Information]

![一般>存放區資訊](./assets/general-store-information.png)<!-- zoom -->

如需有關變更這些設定的詳細資訊，請參閱&#x200B;_快速入門手冊_&#x200B;中的[存放區資訊](../../getting-started/store-details.md)。

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Store Name] | 存放區檢視 | 與存放區檢視相關聯的存放區名稱。 |
| [!UICONTROL Store Phone Number] | 存放區檢視 | 商店的主要電話號碼（與商店檢視相關聯）已針對企業開放。 例如：週一 — 週五，9-5，週六9 — 中午PST |
| 國家 | 網站 | 經營網站的企業的國家/地區。 |
| [!UICONTROL Region/State] | 網站 | 經營網站的業務地區或州。 |
| [!UICONTROL ZIP/Postal Code] | 網站 | 經營網站之業務的郵遞區號。 |
| [!UICONTROL City] | 網站 | 經營網站之企業的城市位置。 |
| [!UICONTROL Street Address] | 網站 | 經營網站的企業的街道或郵寄地址。 |
| [!UICONTROL Street Address Line 2|]網站 | 商業街道地址的第二行（如有需要）。 |
| [!UICONTROL VAT Number] | 網站 | 擁有Commerce安裝之企業的「增值稅」編號（如適用）。 |
| [!UICONTROL Validate VAT Number] |  | 驗證增值稅識別碼。 |

{style="table-layout:auto"}

## [!UICONTROL Single-Store Mode]

![一般>單一存放區模式](./assets/general-single-store-mode.png)<!-- zoom -->

如需有關變更這些設定的詳細資訊，請參閱&#x200B;_快速入門手冊_&#x200B;中的[單一存放區模式](../../getting-started/websites-stores-views.md#single-store-mode)。

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable Single-Store Mode] | 全域 | 啟用單一存放區安裝時，會隱藏設定範圍方塊和相關欄位標籤選項： `Yes` / `No` <br/>**_注意：_**&#x200B;對於具有多個檢視的存放區，會忽略單一存放區模式。<br/>啟用單一存放區模式會將所有目錄和產品存放區特定資料，從預設存放區檢視複製到所有存放區檢視範圍。 如果商店僅有一個商店，它只會複製目錄和產品資料。 如果商店有一個停用的商店和一個啟用的商店，它將不會複製目錄和產品資料。<br/>啟用單一存放區模式會忽略內容特定資料的存放區檢閱特定組態設定。 而是使用全域層級範圍中定義的組態設定，以確保管理員UI和店面之間的一致性。 |

{style="table-layout:auto"}

## [!UICONTROL Data Services]

![一般>資料服務](./assets/general-data-services.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Commerce Events Enabled] | 全域 | 如果您是醫療保健客戶，且已安裝[資料服務HIPAA](https://experienceleague.adobe.com/zh-hant/docs/commerce/data-connection/hipaa-readiness)擴充功能，則此設定預設為關閉。 因此，即時搜尋和產品建議使用的店面活動資料將不再擷取。 這是因為店面事件資料是在使用者端產生。 若要繼續擷取和傳送店面事件資料以供[即時搜尋](https://experienceleague.adobe.com/zh-hant/docs/commerce/live-search/overview)和[產品推薦](https://experienceleague.adobe.com/zh-hant/docs/commerce/product-recommendations/guide-overview)服務使用，請將&#x200B;**已啟用Commerce事件**&#x200B;設定為`Yes`。 |

{style="table-layout:auto"}
