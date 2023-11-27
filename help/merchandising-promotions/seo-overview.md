---
title: 搜尋引擎最佳化
description: 瞭解Commerce網站的搜尋引擎最佳化(SEO)工具以及最佳化SEO的最佳實務。
exl-id: ba09159a-1b40-4592-8758-f7072dab4589
feature: Merchandising, Products, Search
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 0%

---

# SEO總覽

_搜尋引擎最佳化_ (SEO)是微調網站內容和呈現方式的作法，以改進搜尋引擎編制頁面索引的方式。 Commerce包含多種功能，可支援您持續的SEO工作。

## 中繼資料

進一步瞭解如何新增和增強關鍵字豐富 [中繼資料](meta-data.md) 用於您的網站和商店。

## 使用Sitemap

A [網站地圖](sitemap-xml.md) 改善搜尋引擎為存放區編制索引的方式，且設計用於尋找可能被網頁編目程式忽略的頁面。 網站地圖可設定為索引所有頁面和影像。

## URL重新寫入

此 [URL重寫](url-rewrite.md) 工具可讓您變更與產品、類別或CMS頁面相關聯的任何URL。

## 搜尋引擎自動機制

Commerce設定包含設定，可產生和管理為網站編制索引的網頁編目程式和機器人的指示。 如果對的要求 `robots.txt` 到達Commerce （而不是實體檔案），它會動態路由至robots控制器。 指示是大多數搜尋引擎識別並遵循的指示。

依預設，Commerce產生的robots.txt檔案包含網頁編目程式的指示，以避免為包含系統內部使用之檔案的網站特定部分建立索引。 您可以使用預設設定，或為全部或特定搜尋引擎定義您自己的自訂指示。 有許多線上文章詳細探索了主題。

### 自訂指示範例

**允許完整存取**

    使用者代理程式：*
    不允許：

**不允許存取所有資料夾**

    使用者代理程式：*
    不允許： /

**預設指示**

    使用者代理： *
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

### 設定 `robots.txt`

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. 尋找 **[!UICONTROL Global]** 格線第一列的組態，然後按一下 **[!UICONTROL Edit]**.

   ![全域設計設定](./assets/design-configuration-grid.png){width="700" zoomable="yes"}

1. 向下捲動並展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Search Engine Robots]** 並執行下列動作：

   ![設計組態 — 搜尋引擎自動機制](./assets/design-configuration-search-engine-robots.png){width="600" zoomable="yes"}

   - 設定 **[!UICONTROL Default Robots]** 變更為下列其中一項：

     | 選項 | 說明 |
     |------|------------|
     | `INDEX, FOLLOW` | 指示Web編目程式為網站建立索引，並於稍後檢查是否有變更。 |
     | `NOINDEX, FOLLOW` | 指示Web編目程式避免為網站編制索引，但稍後再檢查是否有變更。 |
     | `INDEX, NOFOLLOW` | 指示Web編目程式為網站建立一次索引，但稍後不要回來檢查變更。 |
     | `NOINDEX, NOFOLLOW` | 指示Web編目程式避免為網站編制索引，以及稍後不要回來檢查是否有變更。 |

     {style="table-layout:auto"}

   - 如有需要，請在中輸入自訂指示 **[!UICONTROL Edit Custom instruction of robots.txt file]** 方塊。 例如，當網站處於開發狀態時，您可能想要禁止存取所有資料夾。

   - 若要還原預設指示，請按一下 **[!UICONTROL Reset to Default]**.

1. 完成後，按一下 **[!UICONTROL Save Configuration]**.
