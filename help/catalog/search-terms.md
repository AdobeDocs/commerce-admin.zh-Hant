---
title: 管理搜尋詞
description: 瞭解如何管理商店的搜尋字詞，以使用拼寫錯誤或替代字詞重新導向客戶。
exl-id: e21ece58-2bc2-49ef-96d3-3be930e09f94
feature: Catalog Management, Search
source-git-commit: 6126943f20f33d52085018ca634159918833efc9
workflow-type: tm+mt
source-wordcount: '1158'
ht-degree: 0%

---

# 管理搜尋詞

此 [登陸頁面](../content-design/pages.md) 搜尋字詞可以是內容頁面、類別頁面、產品詳細資料頁面，甚至不同網站上的頁面。

使用搜尋字詞來擷取常見的拼寫錯誤並將它們重新導向到適當的頁面。 例如，如果您銷售鍛鐵露台傢俱，您知道許多人會誤將這個辭彙拼寫為 _鐵桿_、甚至 _腐鐵_. 您可以輸入每個拼錯的字詞作為搜尋字詞，並將它們設為同義詞 _鍛鐵_. 即使字詞拼寫有誤，搜尋仍會被導向到鍛鐵的頁面。

您也可以透過檢查客戶在您商店中尋找產品時所使用的搜尋詞來瞭解他們想要什麼。 如果有足夠的人尋找不在您目錄中的產品，則可能表示有銷售機會。 同時，與其讓這些變數空手而歸，您可以將其重新導向至目錄中的其他產品。

## 新增搜尋詞

當您瞭解人們使用新字詞在您的商店中進行搜尋時，可以將這些字詞新增到您的搜尋字詞清單中，以將人們導向目錄中最相符的產品。

![搜尋字詞格線](./assets/search-terms.png){width="700" zoomable="yes"}

| 欄 | 說明 |
|--- |--- |
| [!UICONTROL Search Query] | 用來執行搜尋的查詢。 |
| [!UICONTROL Store] | 套用搜尋查詢的存放區。 |
| [!UICONTROL Results] | 查詢找到的結果數。 |
| [!UICONTROL Uses] | 使用次數。 |
| [!UICONTROL Redirect URL] | 執行搜尋後重新導向使用者的目標頁面URL。 |
| [!UICONTROL Suggested Terms] | 決定查詢結果是否顯示建議的詞語。 |
| [!UICONTROL Actions] | 以編輯模式開啟產品。 |

{style="table-layout:auto"}

>[!NOTE]
>
>每次購物者使用此搜尋查詢執行搜尋時，結果數都會更新。 若有任何產品變更或移除，則不會更新。

### 新增搜尋字詞

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Search Terms]**.

1. 按一下 **[!UICONTROL Add New Search Term]**.

   ![搜尋詞一般資訊](./assets/search-terms-information.png){width="600" zoomable="yes"}

1. 在 _[!UICONTROL General Information]_在&#x200B;**[!UICONTROL Search Query]**方塊中，輸入要新增為新搜尋字詞的字詞或片語。

1. 如果您的商店提供多種語言版本，請選擇適用的 **[!UICONTROL Store]** 檢視。

1. 若要將搜尋結果重新導向至您商店中的其他頁面或其他網站，請在中輸入目標頁面的完整URL **[!UICONTROL Redirect URL]** 欄位。

1. 如果您希望每當搜尋未傳回任何結果時，此辭彙都可用作建議，請設定 **[!UICONTROL Display in Suggested Terms]** 至 `Yes`.

1. 完成後，按一下 **[!UICONTROL Save Search]**.

## 編輯搜尋字詞

1. 在 _[!UICONTROL Search Terms]_格線中，按一下任何記錄的列，以編輯模式開啟搜尋字詞。

1. 進行必要的變更。

1. 完成後，按一下 **[!UICONTROL Save Search]**.

## 刪除搜尋字詞

刪除搜尋字詞的方法有兩種 — 從網格和編輯頁面上。

**方法1：** 在 _[!UICONTROL Search Terms]_格線

1. 在清單中，選取要刪除之字詞的核取方塊。

1. 在清單的左上角，設定 **[!UICONTROL Actions]** 至 `Delete`.

1. 完成後，按一下 **[!UICONTROL Submit]**.

**方法2：** 在 _[!UICONTROL Edit a Search Term]_頁面

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Search Terms]**.

1. 尋找要刪除的搜尋字詞，並在編輯模式中開啟。

1. 按一下 **[!UICONTROL Delete Search]**.

1. 若要確認動作，請按一下 **[!UICONTROL OK]**.

## 熱門搜尋詞

此 _搜尋字詞_ 商店頁尾的連結會顯示商店訪客所使用的搜尋辭彙，依人氣排名。 搜尋詞會出現在 _標籤雲_ 格式，其中文字的大小表示辭彙的人氣程度。

依預設，「熱門搜尋詞」已啟用作為搜尋引擎最佳化工具，但沒有與目錄搜尋程式的直接連線。 由於「搜尋辭彙」頁面是由搜尋引擎編制索引，因此頁面上的任何詞語都可以協助改善搜尋引擎排名，以及商店的可見度。 「熱門搜尋詞」頁面的URL為： `mystore.com/search/term/popular/`

![店面範例 — 熱門搜尋詞](./assets/store-front-search-terms-yoga-pants.png){width="600" zoomable="yes"}

**_若要設定熱門搜尋詞：_**

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Catalog]** 並選擇 **[!UICONTROL Catalog]** 底下。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Search Engine Optimization]** 區段。

   ![目錄設定 — 搜尋引擎最佳化](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

   如需這些選項的詳細清單，請參閱 [搜尋引擎最佳化](../configuration-reference/catalog/catalog.md#search-engine-optimization) 在 _設定參考_.

1. 設定 **[!UICONTROL Popular Search Terms]** 視需要。

   如有需要，請清除 **[!UICONTROL Use system value]** 核取方塊以變更此設定。

1. 完成後，按一下 **[!UICONTROL Save Config]**.

>[!NOTE]
>
>您可以進一步設定常用的 [目錄搜尋](search-configuration.md).

## 搜尋同義字

改善下列專案效益的一種方式 [目錄搜尋](search-configuration.md) 包括人們可用來描述相同專案的不同術語。 您不想因為某人正在尋找 _沙發_，而您的產品會列為 _沙發_. 您可以透過輸入 _沙發_， _達文波特_、和 _愛吃_ 做為的同義字 _沙發_，並將它們導向相同的登陸頁面。

Adobe Commerce支援兩種不同的同義字管理解決方案：

- 即時搜尋 [同義字](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-admin/synonyms/synonyms.html) 功能適用於已安裝Live Search的Adobe Commerce安裝。
- 所有Adobe Commerce安裝都能立即使用標準的搜尋同義字功能（如本頁所述）。

>[!NOTE]
>
>標準的搜尋同義字功能可立即支援 `name` 和 `sku` 產品屬性 **_僅限_**.

![店面範例 — 具有同義字的搜尋結果](./assets/storefront-search-results-synonyms.png){width="700" zoomable="yes"}

### 建立同義字群組

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Search Synonyms]**.

   此 _[!UICONTROL Search Synonyms]_格點隨即顯示。 如果這是您第一次使用搜尋同義字，則格線是空的。

   ![搜尋同義字方格](./assets/search-synonyms-grid-empty.png){width="700" zoomable="yes"}

1. 按一下 **[!UICONTROL New Synonym Group]**.

   ![新增搜尋同義字群組](./assets/search-synonym-group-new.png){width="700" zoomable="yes"}

1. 設定 **[!UICONTROL Scope]** 至同義字套用的存放區檢視。

1. 輸入群組中的每個同義字，以逗號分隔。 選擇人們可能用作搜尋條件的字詞。 例如：

   - `sweatshirt, sweat shirt, hoodie, fleece`
   - `cell phone, mobile phone, smart phone`
   - `couch, sofa, davenport`
   - `wrought iron, rot iron, rod iron`

1. 若要將這些同義字合併成群組，並與具有相同範圍的其他同義字合併，請選取 **[!UICONTROL Merge existing synonyms]** 核取方塊。

1. 完成後，按一下 **[!UICONTROL Save Synonym Group]**.

### 編輯同義字群組

1. 在 _[!UICONTROL Search Synonyms]_格線中，按一下任何記錄的列，在編輯模式中開啟同義字群組。

1. 進行必要的變更。

1. 完成後，按一下 **[!UICONTROL Save Synonym Group]**.

### 刪除同義字群組

刪除同義字群組的方法有兩種：從格線及編輯頁面上。

**方法1：** 在搜尋同義字格線中

1. 在 _[!UICONTROL Search Synonyms]_方格中，選取要刪除之群組的核取方塊。

1. 在清單的左上角，設定 **[!UICONTROL Actions]** 至 `Delete`.

1. 完成後，按一下 **[!UICONTROL Submit]**.

**方法2：** 在編輯同義字群組頁面

1. 在「搜尋同義字」網格中，按一下任何記錄的列，以編輯模式開啟同義字群組。

1. 按一下 **[!UICONTROL Delete Synonym Group]**.

1. 出現提示時，確認移除群組。

## 搜尋詞報表

「搜尋詞」報表會顯示每個詞語的結果數量，以及該詞語被使用的次數（點選）。 您可依辭彙、存放區、結果和點選來篩選報表資料，並匯出以供進一步分析。

### 檢視報告

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Reports]** > _[!UICONTROL Marketing]_>**[!UICONTROL Search Terms]**.

1. 視需要使用控制項來篩選報表。

   ![搜尋詞報表](./assets/search-terms-report.png){width="700" zoomable="yes"}

## 匯出報告

1. 的 **[!UICONTROL Export to]**，選擇匯出格式：

   - `CSV`  — 包含純文字資料的逗號分隔值檔案
   - `Excel XML`  — 以XML為基礎的試算表資料格式

1. 按一下 **[!UICONTROL Export]**.

   產生的檔案會自動儲存到您指定的資料夾以供下載。

### 報表欄

| 欄 | 說明 |
|--- |--- |
| [!UICONTROL ID] | 為搜尋字詞專案產生的唯一數值ID |
| [!UICONTROL Search Query] | 用來執行搜尋的查詢 |
| [!UICONTROL Store] | 套用搜尋查詢的存放區 |
| [!UICONTROL Results] | 結果數量 |
| [!UICONTROL Hits] | 使用次數 |

{style="table-layout:auto"}
