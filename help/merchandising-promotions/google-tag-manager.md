---
title: '[!DNL Google Tag Manager]'
description: 瞭解如何使用 [!DNL Google Tag Manager] 管理在Adobe Commerce網站中與行銷活動相關的許多標籤（程式碼片段）。
exl-id: 9c24239b-9efd-42ee-9b99-5a194f3c4347
feature: Marketing Tools, Integration
source-git-commit: 7384481d1a4a2a04882d4c99448cca75abc9be31
workflow-type: tm+mt
source-wordcount: '1161'
ht-degree: 0%

---

# [!DNL Google Tag Manager]

{{ee-feature}}

[!DNL Google Tag Manager] 可協助您管理與行銷活動活動相關的許多標籤（程式碼片段）。 [!DNL Google Tag Manager] 可讓您將追蹤標籤新增至您的網站，以測量對象，或個人化、重新鎖定目標或執行搜尋引擎行銷計畫。

[!DNL Google Tag Manager] 直接將資料和事件傳輸至 [!DNL Google Analytics]、增強型電子商務和其他協力廠商分析解決方案，讓您清楚瞭解網站、產品和促銷活動的執行狀況。

您應該有一個 [!DNL Google Analytics] 和 [!DNL Tag Manager] 帳戶以繼續此程式。 下列指示會逐步引導您完成設定Google帳戶、設定Commerce商店及建立標籤的程式。

>[!NOTE]
>
>如果您的企業受到隱私權法規的約束，例如 [一般資料保護規範](../getting-started/compliance-gdpr.md) 和/或 [加州消費者隱私法](../getting-started/compliance-ccpa.md)，請參閱 [Google隱私權設定](google-tools.md#google-privacy-settings).

## 步驟1. 設定您的 [!DNL Google Analytics] 帳戶

另請參閱 [設定網站搜尋](https://support.google.com/analytics/answer/1012264) 如需開始使用所需的基本資訊，請參閱Google說明。 另請參閱Google指南 [Google Analytics](https://support.google.com/analytics/answer/9304153) 和 [Google Tag Manager](https://support.google.com/tagmanager/answer/6102821).

1. 登入您的 [!DNL Google Analytics] 帳戶。

1. 若要啟用 **[!UICONTROL Internal Site Search Tracking]**，請執行下列動作：

   - 瀏覽至 **[!UICONTROL Select View]** > **[!UICONTROL View Settings]**.

   - 設定 **[!UICONTROL Site Search Tracking]** 至 `On`.

   - 設定 **[!UICONTROL Query]** 引數至 `q`.

   - 完成時， **[!UICONTROL Save]** 設定。

1. 若要啟用顯示功能，請執行下列動作：

   - 選擇 **[!UICONTROL Property Settings]**.

   - 在 _[!UICONTROL Advertising Features]_，設定&#x200B;**[!UICONTROL Enable Demographics and Interest Reports]**至 `On`.

   - **[!UICONTROL Save]** 設定。

1. 若要啟用電子商務追蹤，請執行以下操作：

   - 瀏覽至 **[!UICONTROL Select View]** > **[!UICONTROL Ecommerce Settings]**.

   - 設定 **[!UICONTROL Enable Ecommerce]** 至 `On`.

   - 設定 **[!UICONTROL Enable Enhanced Ecommerce Reporting]** 至 `On`.

   - **[!UICONTROL Save]** 設定。

1. 重新載入頁面，並確認所有設定仍保留 `On`.

   >[!NOTE]
   >
   >如果不是所有設定 `On`，重複上述步驟，儲存並重新載入頁面。 重複此程式，直到所有設定皆設為 `On`.

## 步驟2. 設定您的 [!DNL Google Tag Manager] 帳戶

下列指示顯示如何使用基本設定來設定新容器。 範例 [作曲者](https://developer.adobe.com/commerce/php/development/composer/) 組態(.json)檔案可用來簡化程式，匯入可在新容器中產生標籤。 在此範例中，建議建立容器，而非修改現有容器。

>[!NOTE]
>
>如需詳細資訊，請參閱Google [容器匯出和匯入](https://support.google.com/tagmanager/answer/6106997). 這些指示會提供逐步解說，說明如何將JSON範例匯入新容器中。

1. 下載連結的檔案 [GTM_M2_Config_json.txt](./assets/GTM_M2_Config_json.txt)，在編輯器中開啟檔案，並將其儲存為 `GTM_M2_Config.json`.

   json檔案會直接上傳至 [!DNL Google Tag Manager].

1. 瀏覽至 **[!UICONTROL Admin]** > **[!UICONTROL Container]** > **[!UICONTROL Import Container]**.

1. 按一下 **[!UICONTROL Choose container file]** 並選取json檔案。

1. 在 **[!UICONTROL Choose workspace]**，按一下 **[!UICONTROL New]**.

1. 輸入標題和說明，然後按一下 **[!UICONTROL Save]**.

1. 若要匯入檔案，請選取下列動作之一：

   - 此 **[!UICONTROL Overwrite]** 應該為新容器選取選項。

   - 此 **[!UICONTROL Merge]** 如果您使用現有容器，則應選取選項。

1. 按一下 **[!UICONTROL Preview]** 以檢閱標籤、觸發器和變數。

1. 若要編輯 **[!UICONTROL Google Analytics ID]** ，請執行下列動作：

   - 瀏覽至 **[!UICONTROL Variables]** > **[!UICONTROL User-Defined Variables]**.

   - 選擇 **[!UICONTROL Google Analytics]** 並更新預留位置(`UA-xxxxxx-x`)，使用您自己的 **[!UICONTROL GA ID]**.

1. 依照Google的指示，將標籤、觸發器和變數新增至新容器。

   如果您在另一個要使用的容器中有設定，可將它們移至新容器。

1. 按一下 **[!UICONTROL Confirm]** 完成時。

1. 依照Google的指示發佈新容器。

## 步驟3. 設定您的商店

{{gtag-api-note}}

1. 登入您的Commerce商店的管理員。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Sales]** 並選擇 **[!UICONTROL Google API]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Google Analytics]** 並設定下列專案：

   ![銷售組態 — Google Analytics](../configuration-reference/sales/assets/google-api-analytics-tag-manager.png){width="600" zoomable="yes"}

   - 設定 **[!UICONTROL Enable]** 至 `Yes`.

   - 設定 **[!UICONTROL Account type]** 至 `Google Tag Manager`.

   - 在 **[!UICONTROL Container ID]** 欄位，輸入您的GTM ID (`GTM-xxxxxx`)。

   - 如果您也使用Google Analytics進行內容實驗，請設定 **啟用內容實驗** 至 `Yes`.

   - 對其餘欄位使用預設值。

1. 完成後，按一下 **[!UICONTROL Save Config]**.

1. 測試您的 [!DNL Google Tag Manager] 設定，並確認一切都正常運作。

>[!NOTE]
>
>每個容器都與一個網站相關聯，每個帳戶只需要一個容器。 如果您有多個網站的Commerce例項，則需要個別的容器。

## 步驟4. 將GTM程式碼新增至您的Adobe Commerce市集

1. 若要複製GTM程式碼，請前往 **[!UICONTROL Admin]** > **[!UICONTROL Install Google Tag Manager]**.

   有兩個要新增至Commerce網站的GTM程式碼片段：第一個 `<head>` 標籤與的第二 `<body>` 標籤之間。

1. 在Commerce管理員中，前往 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**並以編輯模式開啟商店檢視。

1. 在 _[!UICONTROL Other Settings]_，展開&#x200B;**[!UICONTROL HTML Head]**並貼上您從GTM複製的程式碼 `<head>` 標籤中的變數&#x200B;**[!UICONTROL Scripts and Style Sheets]**欄位。

   ![在HTML標題中插入程式碼](./assets/head-tag.png){width="600" zoomable="yes"}

1. 展開 **[!UICONTROL Footer]** 並貼上適用於的GTM程式碼 `<body>` 在 **[!UICONTROL Miscellaneous HTML]** 欄位。

   ![在頁尾中插入程式碼](./assets/footer-tag-section.png){width="600" zoomable="yes"}

1. 完成後，按一下 **[!UICONTROL Save Configuration]**.

## 欄位說明

| 欄位 | 範圍 | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable] | 存放區檢視 | 決定Google Analytics Enhanced E-commerce是否可用來分析商店中的活動。 選項： `Yes` / `No` |
| [!UICONTROL Account type] | 存放區檢視 | 決定用來監控商店活動和流量的Google追蹤代碼。 選項： `Google Analytics` / `Google Tag Manager` |
| [!UICONTROL Anonymize IP] | 存放區檢視 | 決定是否從Google Analytics結果中顯示的IP位址中移除識別資訊。 |
| [!UICONTROL Enable Content Experiments] | 存放區檢視 | 啟用Google內容實驗，此實驗可用來測試最多十個相同頁面的不同版本。 選項： `Yes` / `No` |
| [!UICONTROL Container Id] | 存放區檢視 | 如果 [!DNL Google Tag Manager] 已經為您的商店安裝和設定，容器ID會自動出現在此欄位中。 |
| [!UICONTROL List property for the catalog page] | 存放區檢視 | 識別與目錄頁面相關聯的Tag Manager屬性。 預設值： `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | 存放區檢視 | 識別與交叉銷售區塊相關聯的Tag Manager屬性。 預設值： `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | 存放區檢視 | 識別與向上銷售區塊相關聯的Tag Manager屬性。 預設值： `Up-sell` |
| [!UICONTROL List property for the related products block] | 存放區檢視 | 識別與相關產品區塊相關聯的Tag Manager屬性。 預設值： `Related Products` |
| [!UICONTROL List property for the search results page] | 存放區檢視 | 識別與搜尋結果頁面相關聯的Tag Manager屬性。 預設值： `Search Results` |
| [!UICONTROL "Internal Promotions" for promotions field "Label"] | 存放區檢視 | 識別與內部促銷活動標籤相關聯的Tag Manager屬性。 預設值： `Label` |

{style="table-layout:auto"}

## 建立標籤以追蹤轉換

如果您有Google AdWords帳戶，則可建立追蹤轉換的標籤。 以下範例說明如何使用兩者 [!DNL Google Tag Manager] 和 [!DNL Google Analytics] 建立會在存放區轉換時觸發的標籤 _成功_ 頁面。

### 步驟1. 建立標籤

1. 登入您的 [!DNL Google Tag Manager] 帳戶，然後按一下您為商店建立之容器的連結。

1. 在 **[!UICONTROL New Tag]** 方塊，按一下 **[!UICONTROL Add a new tag]**.

1. 從您的AdWords帳戶取得下列資訊：

   - 轉換ID
   - 轉換標籤

   如果您需要協助，請造訪Google的 [支援網站](https://support.google.com/tagmanager/answer/6105160).

1. 從 [!DNL Google Tag Manager] 儀表板，按一下 **[!UICONTROL Google AdWords]** 並執行下列動作：

   - 按一下標題預留位置，然後輸入新標籤的名稱。

   - 在 **[!UICONTROL Choose Product]**，選取 **[!UICONTROL Google AdWords]**.

   - 在 _[!UICONTROL Choose a Tag Type]_，選取&#x200B;**[!UICONTROL AdWords Conversion Tracking]**並按一下&#x200B;**[!UICONTROL Continue]**.

1. 輸入 **[!UICONTROL Conversion ID]** 和 **[!UICONTROL Conversion Label]** ，然後按一下 **[!UICONTROL Continue]**.

### 步驟2. 建立規則

繼續從 [!DNL Google Tag Manager] 儀表板，下一步是建立規則，以便在轉換頁面上觸發標籤。

1. 在 **[!UICONTROL Fire On]**，按一下 **[!UICONTROL Some Pages]**.

1. 在 _[!UICONTROL Choose Pages]_區段，完成下列設定：

   - **[!UICONTROL Name]**  — 輸入頁面說明的名稱。

   - **[!UICONTROL Variable]** `url`

   - **作業** - `matches RegEx`

     若要深入瞭解，請參閱 [規則運算式和CSS選取器運運算元](https://support.google.com/tagmanager/answer/7679109) Google Tag Manager說明中的。

   - **[!UICONTROL Value]** - `checkout/success.*`

1. 選取綠色核取方塊並按一下 **[!UICONTROL Save]**.

   您設定的觸發程式會在「引發於」區段中顯示為藍色按鈕。

1. 完成後，按一下 **[!UICONTROL Save Tag]**.

### 步驟3. 預覽和發佈

此程式的下一個步驟是預覽標籤。 每次預覽標籤時，都會儲存版本的快照。 對結果感到滿意時，請轉至要使用的版本，然後按一下 **[!UICONTROL Publish]**.
