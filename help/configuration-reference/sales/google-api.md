---
title: 『[!UICONTROL Sales] &gt； [!UICONTROL Google API]『
description: 檢閱上的組態設定 [!UICONTROL Sales] &gt； [!UICONTROL Google API] 商務管理員頁面。
exl-id: 5031ad3d-1c9a-4bc6-9bfa-683414dca979
feature: Configuration, Marketing Tools
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '996'
ht-degree: 2%

---

# [!UICONTROL Sales] > [!UICONTROL Google API]

{{config}}

## [!UICONTROL Google Analytics]

![Google Analytics](./assets/google-api-analytics-ee.png)<!-- zoom -->

<!-- [Google Analytics](https://docs.magento.com/user-guide/marketing/google-universal-analytics.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | 存放區檢視 | 啟用 [!DNL Google Analytics] 以取得您的商店。 選項： `Yes` / `No` |
| [!UICONTROL Account Type] | 存放區檢視 | ![Adobe Commerce](../../assets/adobe-logo.svg) (僅限Adobe Commerce)根據您的Google Analytics帳戶型別決定設定選項。 選項： Universal Analytics （預設） / Google標籤管理員 |
| [!UICONTROL Account Number] | 存放區檢視 | 建立時指派的帳號或追蹤代碼 [!DNL Google Analytics] 帳戶。 |
| [!UICONTROL Anonymize IP] | 存放區檢視 | 決定是否從出現的IP位址中移除識別資訊 [!DNL Google Analytics] 個結果。 |
| [!UICONTROL Enable Content Experiments] | 存放區檢視 | 啟用 [Google內容實驗](https://support.google.com/analytics/answer/9366791?hl=en&amp;ref_topic=1745207)，可用來測試相同頁面最多十個不同版本。 選項： `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Google Analytics - Google Tag Manager]

{{ee-feature}}

![Google Analytics- Google Tag Manager帳戶型別](./assets/google-api-analytics-tag-manager.png)<!-- zoom -->

時間 **[!UICONTROL Account Type]** 設為 `Google Tag Manager`，則會顯示其他欄位。

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Container ID] | 存放區檢視 | 的唯一識別碼 [!DNL Google Tag Manager] 容器。 此值通常開頭為 `GTM-`. 此ID位於您的 [!DNL Google Tag Manager] 帳戶。 如果 [!DNL Google Tag Manager] 已經為您的商店安裝和設定，容器ID會自動出現在此欄位中。 |
| [!UICONTROL List property for the catalog page] | 存放區檢視 | 識別 [!DNL Google Tag Manager] 與目錄頁面關聯的屬性。 預設值： `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | 存放區檢視 | 識別 [!DNL Google Tag Manager] 與交叉銷售區塊相關聯的屬性。 預設值： `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | 存放區檢視 | 識別 [!DNL Google Tag Manager] 與向上銷售區塊關聯的屬性。 預設值： `Up-sell` |
| [!UICONTROL List property for the related products block] | 存放區檢視 | 識別 [!DNL Google Tag Manager] 與相關產品區塊相關聯的屬性。 預設值： `Related Products` |
| [!UICONTROL List property for the search results page] | 存放區檢視 | 識別 [!DNL Google Tag Manager] 與搜尋結果頁面關聯的屬性。 預設值： `Search Results` |
| [!UICONTROL 'Internal Promotions' for promotions field "Label"] | 存放區檢視 | 識別 [!DNL Google Tag Manager] 與內部促銷活動標籤關聯的屬性。 預設值： `Label` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Google AdWords]

![Google AdWords](./assets/google-api-google-adwords.png)<!-- zoom -->

<!-- [Google AdWords](https://docs.magento.com/user-guide/marketing/google-adwords.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | 存放區檢視 | 啟用商店的Google AdWords。 選項： `Yes` / `No` |
| [!UICONTROL Conversion ID] | 存放區檢視 | 來自您Google AdWords帳戶的ID。 |
| [!UICONTROL Conversion Language] | 存放區檢視 | 用於AdWords轉換的語言。 選項： `All available languages` |
| [!UICONTROL Conversion Format] | 存放區檢視 | 決定 [!DNL Google Site Stats] 顯示在轉換頁面上的通知。 通知連結至通知訪客有關用於追蹤其瀏覽的Cookie的頁面。 此數值會指派給 `google_conversion_format` 變數來識別。 若要深入瞭解，請參閱 [關於轉換追蹤](https://support.google.com/google-ads/answer/1722022?hl=en) ，網址為： Google。 選項： <br/>**`1`**— 顯示單行通知。<br/>**`2`** - （預設）顯示兩行通知。 <br/>**`3`**— 不顯示客戶通知。 |
| [!UICONTROL Conversion Color] | 存放區檢視 | 決定轉換標籤的顏色。 使用 [檢色器](https://www.w3schools.com/colors/colors_picker.asp) 以選取十六進位值。 這個十六進位值會指派給 `google_conversion_color` 變數來識別。 例如： ffffff  `var google_conversion_color = "ffffff";` |
| [!UICONTROL Conversion Label] | 存放區檢視 | 文字標籤，會以 [!DNL Google Site Stats] 通知。 此文字字串會指派給 `~` 變數來識別。 例如：「感謝您的選購！」 |
| [!UICONTROL Conversion Value Type] | 存放區檢視 | 指定用來判斷轉換發生時間的值型別。 選項： <br/>**`Dynamic`**— 根據動態訂單金額判斷已發生轉換。<br/>**`Constant`**  — 根據輸入的值判斷已發生轉換。 |
| [!UICONTROL Conversion Value] | 存放區檢視 | 指定用於 _[!UICONTROL Constant]_轉換值型別。 |
| [!UICONTROL Send Order Currency] | 存放區檢視 | 啟用AdWords中的交易特定貨幣轉換值（適用於使用不同基本貨幣的網站）。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Google GTag]

{{gtag-api-note}}

### [!UICONTROL Google Analytics4]

![GOOGLE ANALYTICS4](./assets/google-api-gtag-google-analytics4.png)<!-- zoom -->

<!-- [Google Analytics4](https://docs.magento.com/user-guide/marketing/google-universal-analytics.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | 存放區檢視 | 為您的商店啟用Google Analytics4。 選項： `Yes` / `No` |
| [!UICONTROL Account Type] | 存放區檢視 | ![Adobe Commerce](../../assets/adobe-logo.svg) (僅限Adobe Commerce)根據您的Google Analytics帳戶型別決定設定選項。 選項： `Google Analytics4` （預設） / `Google Tag Manager` |
| [!UICONTROL Measurement ID] | 存放區檢視 | 建立Google Analytics帳戶時所指派的帳號或追蹤代碼。 |
| [!UICONTROL Anonymize IP] | 存放區檢視 | 決定是否從Google Analytics結果中顯示的IP位址中移除識別資訊。 |
| [!UICONTROL Enable Content Experiments] | 存放區檢視 | 啟用 [Google內容實驗](https://support.google.com/analytics/answer/9366791?hl=en&amp;ref_topic=1745207)，可用來測試相同頁面最多十個不同版本。 選項： `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

### [!UICONTROL Google Analytics4 - Google Tag Manager]

{{ee-feature}}

![Google Analytics4 - Google Tag Manager帳戶型別](./assets/google-api-gtag-google-analytics4-gtm.png)<!-- zoom -->

時間 **[!UICONTROL Account Type]** 設為 `Google Tag Manager`，則會顯示其他欄位。

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Container Id] | 存放區檢視 | 的唯一識別碼 [!DNL Google Tag Manager] 容器。 此值通常開頭為 `GTM-`. 此ID位於您的Google標籤管理員帳戶中。 如果 [!DNL Google Tag Manager] 已經為您的商店安裝和設定，容器ID會自動出現在此欄位中。 |
| [!UICONTROL List property for the catalog page] | 存放區檢視 | 識別 [!DNL Google Tag Manager] 與目錄頁面關聯的屬性。 預設值： `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | 存放區檢視 | 識別 [!DNL Google Tag Manager] 與交叉銷售區塊相關聯的屬性。 預設值： `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | 存放區檢視 | 識別 [!DNL Google Tag Manager] 與向上銷售區塊關聯的屬性。 預設值： `Up-sell` |
| [!UICONTROL List property for the related products block] | 存放區檢視 | 識別 [!DNL Google Tag Manager] 與相關產品區塊相關聯的屬性。 預設值： `Related Products` |
| [!UICONTROL List property for the search results page] | 存放區檢視 | 識別 [!DNL Google Tag Manager] 與搜尋結果頁面關聯的屬性。 預設值： `Search Results` |
| [!UICONTROL 'Internal Promotions' for promotions field "Label"] | 存放區檢視 | 識別 [!DNL Google Tag Manager] 與內部促銷活動標籤關聯的屬性。 預設值： `Label` |

{:style=&quot;table-layout:auto&quot;}

### [!UICONTROL Google AdWords]

![Google AdWords](./assets/google-api-gtag-google-adwords.png)<!-- zoom -->

<!-- -- Google AdWords](https://docs.magento.com/user-guide/marketing/google-adwords.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | 存放區檢視 | 啟用商店的Google AdWords。 選項： `Yes` / `No` |
| [!UICONTROL Conversion ID] | 存放區檢視 | 來自您Google AdWords帳戶的ID。 |
| [!UICONTROL Conversion Language] | 存放區檢視 | 用於AdWords轉換的語言。 選項：所有可用語言 |
| [!UICONTROL Conversion Format] | 存放區檢視 | 決定轉換頁面上顯示的Google網站統計資料通知格式。 通知連結至通知訪客有關用於追蹤其瀏覽的Cookie的頁面。 此數值會指派給 `google_conversion_format` 變數來識別。 若要深入瞭解，請參閱 [關於轉換追蹤](https://support.google.com/google-ads/answer/1722022?hl=en) ，網址為： Google。 選項： <br/>**`1`**— 顯示單行通知。<br/>**`2`** - （預設）顯示兩行通知。 <br/>**`3`**— 不顯示客戶通知。 |
| [!UICONTROL Conversion Color] | 存放區檢視 | 決定轉換標籤的顏色。 使用 [檢色器](https://www.w3schools.com/colors/colors_picker.asp) 以選取十六進位值。 這個十六進位值會指派給 `google_conversion_color` 變數來識別。 例如： ffffff  `var google_conversion_color = "ffffff";` |
| [!UICONTROL Conversion Label] | 存放區檢視 | 與Google網站統計資料通知一起顯示的文字標籤。 此文字字串會指派給 `~` 變數來識別。 例如：「感謝您的選購！」 |
| [!UICONTROL Conversion Value Type] | 存放區檢視 | 指定用來判斷轉換發生時間的值型別。 選項： <br/>**`Dynamic`**— 根據動態訂單金額判斷已發生轉換。<br/>**`Constant`**  — 根據輸入的值判斷已發生轉換。 |
| [!UICONTROL Conversion Value] | 存放區檢視 | 指定用於 _[!UICONTROL Constant]_轉換值型別。 |
| [!UICONTROL Send Order Currency] | 存放區檢視 | 啟用AdWords中的交易特定貨幣轉換值（適用於使用不同基本貨幣的網站）。 |

{:style=&quot;table-layout:auto&quot;}
