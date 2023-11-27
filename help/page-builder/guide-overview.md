---
title: '[!DNL Page Builder] 使用者指南'
description: 以下專案的完整資訊： [!DNL Page Builder] 適用於Adobe Commerce和Magento Open Source管理員。
seo-title: Adobe Commerce [!DNL Page Builder] User Guide
seo-description: Describes how to use the [!DNL Page Builder] module in Adobe Commerce or Magento Open Source.
exl-id: 983ef3a8-b803-40ff-a9f5-07eb895df31c
source-git-commit: fa4030d391fc9a3b21cf8fb6f681df9e9165157d
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 1%

---

# [!DNL Page Builder] 使用者指南

本指南適用於Adobe Commerce和Magento Open Source的管理員。 它提供以下專案的詳細資訊： [!DNL Page Builder] 功能，包括用於建立基本內容元件的三部分逐步解說。 它假定您對核心有基本的瞭解 [!DNL Commerce] 設定和功能。

[!DNL Page Builder] 有兩個區域可供存放區管理員使用：

- 管理員：使用此區域來存取設定UI及使用頁面產生器工具。
- 命令列介面：使用此工具來執行安裝和後端組態工作。

本指南涵蓋：

| 主旨 | 說明 |
| ------- | ----------- |
| [簡介](introduction.md) | 什麼是 [!DNL Page Builder]？ 它如何增強Adobe Commerce和Magento Open Source網站的內容建立？ |
| [發行說明](release-notes.md) | 檢閱每個報表套裝中提供的更新 [!DNL Page Builder] 模組發行。 |
| [設定](setup.md) | 若要更新預設設定，您可以變更預設版面配置並啟用更多進階 [!DNL Page Builder] 功能。 您也可以整合 [!DNL Google Maps] 以將位置內容併入頁面。 |
| [工作區](workspace.md) | 檢閱元件 [!DNL Page Builder] 工作區以及它們如何讓您為商店建立吸引人的內容。 |
| 逐步解說 | 如果您正開始使用 [!DNL Page Builder]，您可以完成逐步解說練習來快速上手：<br>[1 — 範例頁面](1-simple-page.md)<br>[2 — 可重複使用的內容區塊](2-blocks.md)<br>[3 — 產品清單的目錄頁面](3-catalog-content.md) |
| [工作區](workspace.md) | 探索中可用的工具 [!DNL Page Builder] 建立基本頁面、產品和目錄頁面、區塊及動態區塊時的Workspace。 |
| 版面配置 | 探索 _版面_ 的區段 [!DNL Page Builder] 面板，以及如何使用這些工具將版面元件新增至 [!DNL Page Builder] 階段： <br>[列](row.md)<br>[欄](column.md)<br>[索引標籤](tabs.md) |
| 元素 | 探索 _元素_ 的區段 [!DNL Page Builder] 面板，以及如何使用這些工具，將基本元素新增至 [!DNL Page Builder] 階段： <br>[文字](text.md)<br>[標題](heading.md)<br>[按鈕](buttons.md)<br>[分隔線](divider.md)<br>[HTML代碼](html-code.md) |
| 媒體 | 探索 _媒體_ 的區段 [!DNL Page Builder] 面板，以及如何使用這些工具將媒體專案新增到 [!DNL Page Builder] 階段： <br>[影像](image.md)<br>[視訊](video.md)<br>[橫幅](banner.md)<br>[滑桿](slider.md)<br>[[!DNL Google Maps]](map.md) |
| 新增內容 | 探索 _新增內容_ 的區段 [!DNL Page Builder] 面板，以及如何將內容元件新增至 [!DNL Page Builder] 階段： <br>[區塊](block.md)<br>[動態區塊](dynamic-block.md)<br>[產品](products.md)<br>[產品Recommendations](recommendations.md) (僅限Adobe Commerce) |
| [範本](templates.md) | 儲存您現有的 [!DNL Page Builder] 將內容當做範本，然後將該範本套用至另一個區域，以快速且一致地建立內容。 |

{style="table-layout:auto"}

其中並未涵蓋Adobe Commerce和Magento Open Source的核心功能。

## 其他檔案

{{docs-links}}

## [!DNL Page Builder] 開發人員資訊

[!DNL Page Builder] 會安裝Adobe Commerce 2.4.x及Magento Open Source 2.4.3和更新版本，預設會啟用所有功能。 如需模組發行版本中所包含變更的相關資訊，請參閱 [[!DNL Page Builder] 發行說明](release-notes.md). 此 [[!DNL Page Builder] 開發人員指南](https://developer.adobe.com/commerce/frontend-core/page-builder/) 提供有關模組架構和自訂的詳細資訊。

## 疑難排解資源

如需疑難排解的說明 [!DNL Page Builder] 問題，請參閱下列內容 [!DNL Commerce] 支援知識庫文章：

- [DotDigital時的空白頁面 [!DNL Page Builder] 表單已儲存](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/magento-2.4.1-empty-page-when-dotdigital-page-builder-form-saved.html)
- [[!DNL Page Builder] 未載入媒體集](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-12/mdva-32133-magento-patch-page-builder-doesn-t-load-media-gallery.html)
- [[!DNL Page Builder] 預覽折扣轉換產品價格會因網站而異](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-16/mdva-33453-page-builder-preview-breaks-product-price-differs-across-sites.html)
- [無法儲存字詞頁面](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-19/mdva-33614-magento-patch-can-t-save-terms-page.html)
