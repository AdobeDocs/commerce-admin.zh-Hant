---
title: 搜尋引擎最佳化
description: 瞭解適用於Commerce網站的搜尋引擎最佳化(SEO)工具，以及最佳化SEO的最佳實務。
exl-id: ba09159a-1b40-4592-8758-f7072dab4589
feature: Merchandising, Products, Search
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 0%

---

# SEO總覽

_搜尋引擎最佳化_ (SEO)是微調網站的內容與呈現方式，以改進搜尋引擎索引頁面的方式。 Commerce包含多種功能，可支援您持續的SEO作業。

## 中繼資料

進一步瞭解如何為您的網站和商店新增及增強關鍵字豐富的[中繼資料](meta-data.md)。

## 使用Sitemap

[網站地圖](sitemap-xml.md)改善了搜尋引擎為存放區編制索引的方式，並設計來尋找可能被網頁編目程式忽略的頁面。 網站地圖可設定為索引所有頁面和影像。

## URL重新寫入

[URL重寫](url-rewrite.md)工具可讓您變更與產品、類別或CMS頁面相關聯的任何URL。

## 搜尋引擎自動機制

Commerce組態包含設定，可產生和管理為網站編制索引的網頁編目程式和機器人的指示。 如果`robots.txt`的請求到達Commerce （而非實體檔案），則會動態路由至robots控制器。 指示是大多數搜尋引擎識別並遵循的指示。

依預設，Commerce產生的robots.txt檔案包含網頁編目程式的指示，以避免為包含系統內部使用之檔案的網站特定部分建立索引。 您可以使用預設設定，或為全部或特定搜尋引擎定義您自己的自訂指示。 有許多線上文章詳細探索了主題。

### 自訂指示範例

**允許完整存取**

    使用者代理程式：*
    不允許：

**不允許存取所有資料夾**

    使用者代理程式：*
    不允許： /

**預設指示**

    使用者代理程式： *
    不允許： /index.php/
    不允許： /*?
    不允許： /checkout/
    不允許： /app/
    不允許： /lib/
    不允許： /*.php$
    不允許： /pkginfo/
    不允許： /report/
    不允許： /var/
    不允許： /catalog/
    不允許： /customer/
    不允許： /sendfriend/
    不允許： /review/
    不允許： /*SID=

### 設定`robots.txt`

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**。

1. 在網格的第一列找到&#x200B;**[!UICONTROL Global]**&#x200B;設定，然後按一下&#x200B;**[!UICONTROL Edit]**。

   ![全域設計組態](./assets/design-configuration-grid.png){width="700" zoomable="yes"}

1. 向下捲動並展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Search Engine Robots]**&#x200B;區段，然後執行下列動作：

   ![設計組態 — 搜尋引擎自動機制](./assets/design-configuration-search-engine-robots.png){width="600" zoomable="yes"}

   - 將&#x200B;**[!UICONTROL Default Robots]**&#x200B;設定為下列其中一項：

     | 選項 | 說明 |
     |------|------------|
     | `INDEX, FOLLOW` | 指示Web編目程式為網站建立索引，並於稍後檢查是否有變更。 |
     | `NOINDEX, FOLLOW` | 指示Web編目程式避免為網站編制索引，但稍後再檢查是否有變更。 |
     | `INDEX, NOFOLLOW` | 指示Web編目程式為網站建立一次索引，但稍後不要回來檢查變更。 |
     | `NOINDEX, NOFOLLOW` | 指示Web編目程式避免為網站編制索引，以及稍後不要回來檢查是否有變更。 |

     {style="table-layout:auto"}

   - 如有需要，請在&#x200B;**[!UICONTROL Edit Custom instruction of robots.txt file]**&#x200B;方塊中輸入自訂指示。 例如，當網站處於開發狀態時，您可能想要禁止存取所有資料夾。

   - 若要還原預設指示，請按一下&#x200B;**[!UICONTROL Reset to Default]**。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Configuration]**。
