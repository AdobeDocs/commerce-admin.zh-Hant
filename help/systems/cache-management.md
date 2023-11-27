---
title: 快取管理
description: 瞭解如何使用快取管理工具，這些工具可讓您輕鬆改善網站效能。
exl-id: c87f85ca-81b9-4cbf-9817-3d779397eefd
feature: Cache, System
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1422'
ht-degree: 0%

---

# 快取管理

Adobe Commerce和Magento Open Source快取管理系統可讓您輕鬆改善網站的效能。 每當快取需要重新整理時，工作區頂端都會出現通知，引導您完成整個程式。 請依照「快取管理」的連結操作，重新整理無效的快取。

![儲存產品屬性 — 更新快取訊息](./assets/product-attribute-save-msg-update-cache.png){width="500"}

>[!NOTE]
>
>變更目錄實體時，可能會影響其他頁面，並同時讓多個快取失效。 當您檢閱快取管理頁面時，可能會看到需要重新整理的無效專案 _**未直接編輯**_. 例如，當您編輯目錄中的任何產品並將其指派給任何類別時，或當您變更任何相關的產品規則時，就會發生這種失效。

此 _[!UICONTROL Cache Management]_頁面會顯示每個主要快取的狀態及其關聯的標籤。 右上角的大按鈕可用來清除快取，或是包含所有快取儲存體。 在頁面底部，有其他按鈕可清除目錄產品影像快取和JavaScript/CSS快取。

清除快取後，請一律重新整理瀏覽器，以確保您可以看到最新的檔案。 清除Commerce快取不會清除您的網頁瀏覽器快取。 您可能需要清除瀏覽器快取才能檢視更新的內容。

如需其他技術資訊，請參閱 [快取概述](https://developer.adobe.com/commerce/frontend-core/guide/caching/){：target=&quot;_blank&quot;}於 _Commerce前端開發指南_.

存取 _[!UICONTROL Cache Management]_執行下列任一項作業來建立頁面：

- 按一下 **[!UICONTROL Cache Management]** 工作區上方訊息中的連結。
- 在 _管理員_ 側欄，前往 **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**.

![快取管理](./assets/cache-management-invalid.png){width="700" zoomable="yes"}

## 快取的最佳作法

在Commerce中，重新索引和快取具有不同的目的。 [索引](index-management.md) 追蹤資料庫資訊，以提升搜尋效能、加快儲存前端的資料擷取速度等等。 快取儲存已載入的資料、影像、格式等，以提高載入和存取店面的效能。

- 安裝擴充功能/模組後，請務必清除快取。 您可以安裝一或多個擴充功能，然後清除快取。
- 安裝Commerce後排清快取。 若是全新安裝，您也應該重新編列索引。
- 從開放原始碼或商務的一個版本升級至另一個版本後，請排清快取。
- 排清快取時，請考慮快取型別，並排程在非尖峰期進行排清。 例如，挑選有少數客戶可存取網站的時間，例如深夜或清晨。 在高峰期間清除某些快取型別會導致管理員負載過高，並可能使網站停止運作，直到完成為止。
- 時間 [重新索引](index-management.md)，您不需要同時執行排清快取。

## 快取管理角色資源

特定快取維護動作的存取權可依角色指派給使用者，包括檢視、切換和排清快取的選項。 Adobe建議僅對管理員層級的使用者啟用排清動作。 存取所有快取管理功能可能會影響店面的效能。

![角色資源 — 快取管理](./assets/permissions-role-resources-cache-management.png){width="600" zoomable="yes"}

如需有關指派資源以授予管理員使用者帳戶存取權的資訊，請參閱 [角色資源](permissions-user-roles.md#role-resources). 下列資源可控制對快取管理工具的存取：

- [!UICONTROL Clean Cache Actions]

   - [!UICONTROL Flush Cache Storage]
   - [!UICONTROL Flush Magento Cache]

- [!UICONTROL Cache Type Management]

   - [!UICONTROL Toggle Cache Type]
   - [!UICONTROL Refresh Cache Type]

- [!UICONTROL Additional Cache Management]

   - [!UICONTROL Catalog Images Cache]
   - [!UICONTROL Flush Js/Css]
   - [!UICONTROL Flush Static Files]

## 重新整理特定快取

1. 對於每個要重新整理的快取，請選取該列開頭的核取方塊。

1. 設定 **[!UICONTROL Actions]** 至 `Refresh` 並按一下 **[!UICONTROL Submit]**.

## 執行大量動作重新整理

1. 若要選取一組快取，請設定 **[!UICONTROL Mass Actions]** 變更為下列其中一項：

   - `Select All`
   - `Select Visible`

1. 選取動作要鎖定之每個快取的核取方塊。

1. 設定 **[!UICONTROL Actions]** 至 `Refresh` 並按一下 **[!UICONTROL Submit]**.

## 排清產品影像快取

1. 在 _[!UICONTROL Additional Cache Management]_，按一下&#x200B;**[!UICONTROL Flush Catalog Images Cache]**以清除預先產生的產品影像檔案。

   此 `Image cache was cleaned` 訊息會顯示在工作區頂端。

1. 清除瀏覽器的快取。

## 排清JavaScript/CSS快取

1. 在 _[!UICONTROL Additional Cache Management]_，按一下&#x200B;**[!UICONTROL Flush JavaScript/CSS Cache]**以清除已合併至單一檔案的任何JavaScript和CSS檔案。

   此 `The JavaScript/CSS cache has been cleaned` 訊息會顯示在工作區頂端。

1. 清除瀏覽器的快取。

## 使用命令列排清

Commerce使用命令列提供其他排清快取選項。 這些選項可能需要開發人員支援才能完成。 如需完整的詳細資訊和命令選項，請參閱 [管理快取](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/manage-cache.html){：target=&quot;_blank&quot;}於 _設定指南_.

## 控制項

| 控制 | 說明 |
|--- |--- |
| [!UICONTROL Mass Actions] | 選取多個快取的核取方塊。 選項： <br/>**[!UICONTROL Select All]**— 選取所有快取的核取方塊。<br/>**&#x200B;取消全選&#x200B;**— 清除所有快取的核取方塊。<br/>**[!UICONTROL Select Visible]**  — 選取所有可見快取的核取方塊。 <br/>**[!UICONTROL Unselect Visible]**— 清除所有可見快取的核取方塊。 |
| [!UICONTROL Actions] | 決定要套用至所有所選快取的動作。 選項： <br/>**[!UICONTROL Enable]**— 啟用所有選取的快取。<br/>**[!UICONTROL Disable]**  — 停用所有選取的快取。 <br/>**[!UICONTROL Refresh]**— 重新整理所有選取的快取。 |
| [!UICONTROL Submit] | 將動作套用至所有選取的快取。 |

{style="table-layout:auto"}

### 按鈕

| 按鈕 | 說明 |
|--- |--- |
| [!UICONTROL Flush Magento Cache] | 移除預設Commerce快取中的所有專案(`var/cache`)，根據他們相關聯的Commerce標籤。 |
| [!UICONTROL Flush Cache Storage] | 不論Commerce標籤為何，都會從快取中移除所有專案。 如果您的系統使用替代快取位置，則其他應用程式使用的任何快取檔案都會在程式中移除。 |
| [!UICONTROL Flush Catalog Images Cache] | 移除所有儲存在中的自動調整大小和加水印的目錄影像 `media/catalog/product/cache`. 如果最近上傳的影像未反映在目錄中，請嘗試清除目錄並重新整理瀏覽器。 |
| [!UICONTROL Flush JavaScript/CSS Cache] | 從快取中移除合併的JavaScript和CSS檔案復本。 如果樣式表或JavaScript的最近變更未反映在存放區中，請嘗試排清JavaScript/CSS快取並重新整理瀏覽器。 |
| [!UICONTROL Flush Static Files Cache] | 移除已預先處理的檢視檔案和靜態檔案。 |

{style="table-layout:auto"}

### 快取

| 快取 | 說明 | 關聯的標籤 |
| ----- | ----------- | -------------- |
| [!UICONTROL Configuration] | 跨模組收集並合併的各種XML設定。<br>**[!UICONTROL System]**-  `config.xml`，`local.xml`<br>**[!UICONTROL Module]** -  `config.xml` | `CONFIG` |
| [!UICONTROL Layouts] | 配置建置指示。 | `LAYOUT_GENERAL_CACHE_TAG` |
| [!UICONTROL Blocks HTML output] | 頁面區塊HTML。 | `BLOCK_HTML` |
| [!UICONTROL Collections Data] | 集合資料檔案。 | `COLLECTION_DATA` |
| [!UICONTROL Reflection Data] | 清除API介面反射資料，這些資料通常會在執行階段產生。 | `REFLECTION` |
| [!UICONTROL Database DDL operations] | DDL查詢的結果，例如描述表格或索引。 | `DB_DDL` |
| [!UICONTROL Compiled Config] | 程式碼編譯的結果。 | `COMPILED_CONFIG` |
| [!UICONTROL EAV types and attributes] | 實體型別宣告快取。 | `EAV` |
| [!UICONTROL Customer Notification] | 顯示在使用者介面中的臨時通知。 | `CUSTOMER_NOTIFICATION` |
| [!UICONTROL Integrations Configuration] | 整合設定檔。 | `INTEGRATION` |
| [!UICONTROL Integrations API Configuration] | 整合API設定檔。 | `INTEGRATION_API_CONFIG` |
| [!UICONTROL Page Cache] | 全頁快取。 | `FPC` |
| [!UICONTROL Translations] | 翻譯檔案。 | `TRANSLATE` |
| [!UICONTROL Web Services Configuration] | REST和SOAP組態，產生的WSDL檔案。 | `WEBSERVICE` |
| [!UICONTROL Target Rule] | 目標規則索引 | `TARGET_RULE` |

{style="table-layout:auto"}

## 全頁快取

Adobe Commerce和Magento Open Source會使用伺服器上的全頁快取，快速顯示類別、產品和CMS頁面。 全頁快取可改善回應時間並降低伺服器負載。 若沒有快取，每個頁面可能需要執行程式碼區塊，並從資料庫擷取資訊。 不過，啟用全頁快取後，可以直接從快取讀取完全產生的頁面。

>[!NOTE]
>
>建議您 [清漆快取](https://varnish-cache.org/){：target=&quot;_blank&quot;}僅用於生產環境。

快取內容可用於處理類似造訪型別的請求。 因此，向臨時訪客顯示的頁面可能與向客戶顯示的頁面不同。 就快取目的而言，每次造訪都是下列三種型別之一：

- `Non-sessioned`  — 在非工作階段瀏覽期間，購物者會檢視頁面，但不會與商店互動。 系統會快取每個已檢視頁面的內容，並將內容提供給其他無工作階段的購物者。
- `Sessioned`  — 在工作階段瀏覽期間，與商店互動的購物者（透過比較產品或新增產品至購物車等活動）會獲得一個工作階段ID。 在工作階段期間產生的快取頁面僅供該購物者在工作階段期間使用。
- `Customer`  — 系統會為登入帳戶並在商店和商店註冊帳戶的使用者建立客戶工作階段。 在會議期間，系統會根據指派的客戶群組，向客戶呈現特殊優惠、促銷和價格。

如需技術資訊，請參閱 [設定及使用清漆](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/varnish/config-varnish.html){：target=&quot;_blank&quot;}和 [Commerce頁面和預設快取使用Redis](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/redis/redis-pg-cache.html){：target=&quot;_blank&quot;}於 _設定指南_.

**_若要設定整頁快取：_**

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Advanced]** 並選擇 **[!UICONTROL System]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Full Page Cache]** 區段。

   ![進階設定 — 整頁快取](../configuration-reference/advanced/assets/system-full-page-cache.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Caching Application]** 變更為下列其中一項：

   - `Built-in Application`
   - `Varnish Caching`

1. 若要設定頁面快取的逾時，請輸入 **[!UICONTROL TTL for public content]**. (預設值為 `86400`)

1. 如果使用清漆，請完成 **[!UICONTROL Varnish Configuration]** 區段如下所示：

   - **[!UICONTROL Access list]**  — 輸入可以清除Varnish設定以產生設定檔的IP位址。 請使用逗號分隔多個專案。 預設值為 `localhost`.

   - **[!UICONTROL Backend host]**  — 輸入產生設定檔的後端主機的IP位址。 預設值為 `localhost`.

   - **[!UICONTROL Backend port]**  — 識別用來產生設定檔案的後端連線埠。 預設值為： `8080`.

   - **[!UICONTROL Grace period]**  — 指定用來作為產生設定檔之寬限期的秒數。 另請參閱 [進階清漆組態](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/config-varnish-advanced.html) 在 _設定指南_.

   - 將組態匯出為 `varnish.vcl` 檔案中，按一下您使用之清漆版本的按鈕。

   ![進階設定 — 整頁快取清漆](../configuration-reference/advanced/assets/system-full-page-cache-varnish.png){width="600" zoomable="yes"}

1. 完成後，按一下 **[!UICONTROL Save Config]**.
