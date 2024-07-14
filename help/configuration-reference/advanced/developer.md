---
title: '[!UICONTROL Advanced] &amp；gt； [!UICONTROL Developer]'
description: 檢閱Commerce管理員的[!UICONTROL Advanced] &amp；gt； [!UICONTROL Developer]頁面上的組態設定。
exl-id: 2ef4ba6a-b5a5-419d-8d61-e535e3366370
role: Admin, Developer
feature: Site Management, Configuration, System
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '798'
ht-degree: 1%

---

# [!UICONTROL Advanced] > [!UICONTROL Developer]

{{config}}

>[!NOTE]
>
>這些組態設定僅適用於[開發人員模式](../../systems/developer-tools.md#operation-modes)。

## [!UICONTROL Frontend Development Workflow]

![前端開發工作流程](./assets/developer-frontend-development-workflow.png)<!-- zoom -->

如需有關變更這些設定的詳細資訊，請參閱&#x200B;_系統管理系統指南_&#x200B;中的[前端開發工作流程](../../systems/developer-tools.md#frontend-development-workflow)。

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Workflow Type] | 全域 | 決定開發期間在使用者端或伺服器端是否發生較少編譯。 選項： <br/>**`Client side less compilation`**— 使用原生less.js程式庫在瀏覽器中進行編譯。<br/>**`Server side less compilation`** — 使用Less PHP程式庫在伺服器上進行編譯。 這是生產的預設模式。 |

{style="table-layout:auto"}

## [!UICONTROL Developer Client Restrictions]

![開發人員使用者端限制](./assets/developer-developer-client-restrictions.png)<!-- zoom -->

如需有關變更此設定的詳細資訊，請參閱&#x200B;_系統管理系統指南_&#x200B;中的[使用者端限制](../../systems/developer-tools.md#client-restrictions)。

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Allow IPs (comma separated)] | 存放區檢視 | 建立IP位址允許清單，這些IP位址可以在即時網站上使用開發人員工具，而不會干擾商店中的客戶。 使用開發人員工具（例如&#x200B;_內嵌轉譯_）時，對網站所做的任何變更只會從允許清單上的IP位址中顯示。 |

{style="table-layout:auto"}

## [!UICONTROL Template Settings]

![範本設定](./assets/developer-template-settings.png)<!-- zoom -->

如需有關變更這些設定的詳細資訊，請參閱&#x200B;_管理系統指南_&#x200B;中的[最佳化資源檔案](../../systems/developer-tools.md#optimizing-resource-files)。

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Allow Symlinks] | 存放區檢視 | 啟用[符號連結](https://en.wikipedia.org/wiki/Symbolic_link)可能會讓您的網站面臨安全性風險，不建議用於生產存放區。 |
| [!UICONTROL Minify Html] | 存放區檢視 | 決定是否將存放區範本的HTML最小化。 選項： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Debug]

![偵錯](./assets/developer-debug.png)<!-- zoom -->

如需有關變更這些設定的詳細資訊，請參閱&#x200B;_系統管理系統指南_&#x200B;中的[範本路徑提示](../../systems/developer-tools.md#template-path-hints)。

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable Template Path Hints for Storefront] | 存放區檢視 | 在店面新增表示法，表示頁面上使用的每個範本的路徑。 選項： `Yes` / `No` |
| [!UICONTROL Enable Template Path Hints for Admin] | 全域 | 將標籤法新增至管理員，指出頁面上使用之每個範本的路徑。 選項： `Yes` / `No` |
| [!UICONTROL Add Block Class Type to Hints] | 存放區檢視 | 包括範本路徑提示中的區塊名稱。 選項： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Translate Inline]

![翻譯內嵌](./assets/developer-translate-inline.png)<!-- zoom -->

如需有關變更這些設定的詳細資訊，請參閱&#x200B;_系統管理系統指南_&#x200B;中的[翻譯內嵌](../../systems/developer-tools.md#translate-inline)。

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable for Storefront] | 存放區檢視 | 啟動店面的內嵌轉譯器。 可以針對每個存放區檢視編輯介面文字。 若要使用內嵌轉譯器而不干擾即時商店，請將您的IP位址新增至開發人員使用者端限制允許清單。 |
| [!UICONTROL Enable for Admin] | 全域 | 為管理員啟用內嵌翻譯工具。 不像店面，管理員無法翻譯成多種語言。 不過，介面中的欄位標籤和其他文字可以變更。 |

{style="table-layout:auto"}

## [!UICONTROL JavaScript Settings]

![JavaScript設定](./assets/developer-javascript-settings.png)<!-- zoom -->

如需有關變更這些設定的詳細資訊，請參閱&#x200B;_管理系統指南_&#x200B;中的[最佳化資源檔案](../../systems/developer-tools.md#optimizing-resource-files)。

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Merge JavaScript Files] | 存放區檢視 | 將多個JavaScript檔案合併為單一檔案以縮短頁面載入時間。 |
| [!UICONTROL Enable JavaScript Bundling] | 存放區檢視 | 判斷多個JavaScript檔案是否可整合為一個檔案。 選項： `Yes` / `No` |
| [!UICONTROL Minify JavaScript Files] | 存放區檢視 | 移除不必要的字元、空格和縮排，以縮小程式碼。 |
| [!UICONTROL Move JS code to the bottom of the page] | 全域 | 如果啟用，會將JS程式碼移至頁面底部。 選項： `Yes` / `No` |
| [!UICONTROL Translation Strategy] | 全域 | 決定系統使用的翻譯方法。 選項： <br/>**`Dictionary`**— 店面翻譯。<br/>**`Embedded`** — 管理員端翻譯。 |
| [!UICONTROL Log JS Errors to Session Storage] | 全域 | 如果啟用，則可供功能測試用於報表。 選項： `Yes` / `No` |
| [!UICONTROL Log JS Errors to Session Storage Key] | 全域 | 識別用於擷取所收集js錯誤的金鑰。 |

{style="table-layout:auto"}

## [!UICONTROL CSS Settings]

![CSS設定](./assets/developer-css-settings.png)<!-- zoom -->

如需有關變更這些設定的詳細資訊，請參閱&#x200B;_管理系統指南_&#x200B;中的[最佳化資源檔案](../../systems/developer-tools.md#optimizing-resource-files)。

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Merge CSS Files] | 存放區檢視 | 將多個CSS檔案合併為單一檔案以縮短頁面載入時間。 選項： `Yes` / `No` |
| [!UICONTROL Minify CSS Files] | 存放區檢視 | 移除不必要的字元、空格和縮排，以縮小程式碼。 選項： `Yes` / `No` |
| [!UICONTROL Use CSS critical path] | 全域 | _CSS重要路徑_&#x200B;在`<head>`中提供縮制的重要CSS內嵌，並遞延非同步載入的所有非重要樣式。 選項： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Image Processing Settings]

![影像處理設定](./assets/developer-image-processing-settings.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Image Adapter] | 全域 | 指定用來呈現影像的介面卡。 變更介面卡設定後，排清目錄影像快取。 選項： `PHP GD2` / `ImageMagick` <br/><br/>**_注意：_**只有ImageMagik介面卡支援ICO檔案型別。 |

{style="table-layout:auto"}

## [!UICONTROL Caching Settings]

![快取設定](./assets/developer-cache-settings.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Cache User Defined Attributes] | 全域 | 啟用時，會快取使用者定義及系統實體屬性值(EAV)屬性。 此選項可能會提高效能，但也需要額外的空間來快取。 選項： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Static Files Settings]

![靜態檔案設定](./assets/developer-static-files-settings.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Sign Static Files] | 全域 | 啟用時，會將數位簽章新增至靜態檔案的URL，讓瀏覽器能夠偵測較新版本的檔案何時可用。 如果檔案的簽章與瀏覽器快取中儲存的簽章不同，則會使用較新版本的檔案。 可簽署的靜態檔案包括JavaScript、CSS、影像和字型。 選項： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Grid Settings]

![格線設定](./assets/developer-grid-settings.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Asynchronous Indexing|Global] | 決定訂單、商業發票、出貨及銷退折讓單等訂單處理系統實體何時加入網格並重新編制索引。 非同步索引可用於避免在儲存操作期間鎖定資料，並縮短處理時間。 選項： <br/>**`Disable`**- （預設）與訂單相關的實體會在不同時間新增至網格。 在儲存時顯示。<br/>**`Enable`** — 訂單相關實體只會在排程的cron工作期間新增至網格。 Cron應設定為每分鐘執行一次。 |

{style="table-layout:auto"}
