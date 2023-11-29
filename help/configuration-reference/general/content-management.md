---
title: 『[!UICONTROL General] &gt； [!UICONTROL Content Management]『
description: 檢閱上的組態設定 [!UICONTROL General] &gt； [!UICONTROL Content Management] 商務管理員頁面。
exl-id: 67c5e89b-0a7c-4e4f-a5ad-10376c3ef6f9
feature: Configuration, Page Content
source-git-commit: 5eef49c10680a47574afe3d3ecfa430dca7ad9ff
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL Content Management]

{{config}}

## [!UICONTROL WYSIWYG Options]

![WYSIWYG選項](./assets/content-management-wysiwyg-options.png)<!-- zoom -->

<!-- [WYSIWYG Options](https://docs.magento.com/user-guide/cms/editor.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable WYSIWYG Editor] | 存放區檢視 | 判斷是否已為存放區啟用編輯器。 選項：預設啟用/預設停用/完全停用 |
| [!UICONTROL WYSIWYG Editor] | 網站 | 決定用於WYSIWYG編輯器的TinyMCE編輯器版本。 選項： <br/>**`TinyMCE 5`**- （預設）使用TinyMCE版本5作為預設的WYSIWYG編輯器。<br><br>_**&#x200B;注意：**_在Adobe Commerce和Magento Open Source2.4.5中更新TinyMCE 5.10程式庫，解決了在使用某些型別URL更新影像或連結時允許任意JavaScript執行的弱點。 TinyMCE 3在2.4.0版本中已過時，在2.4.3版本中已移除。 TinyMCE 4已在2.4.4版本中移除。 |
| [!UICONTROL Use Static URLs for Media Content in WYSIWYG] | 全域 | 決定是否 [靜態URL](../../content-design/catalog-urls-dynamic-media.md) 用於從WYSIWYG編輯器引用的媒體內容。 此設定會套用至所有可使用WYSIWYG編輯器的位置，包括產品、類別、頁面和區塊。 選項： <br/>**`Yes`**— 針對以WYSIWYG編輯器插入的媒體內容使用靜態URL。 靜態URL為絕對URL，若為 [基礎URL](../../stores-purchase/store-urls.md) 的變更。<br/>**`No`** （預設） — 對於以WYSIWYG編輯器插入的媒體內容，根據  `{{media url="..."}}` 指令。 動態URL是相對的，如果商店的基本URL有所變更，則不會中斷。 |

{style="table-layout:auto"}

## [!UICONTROL CMS Page Hierarchy]

{{ee-feature}}

![CMS頁面階層](./assets/content-management-cms-page-hierarchy.png)<!-- zoom -->

<!--[CMS Page Hierarchy](https://docs.magento.com/user-guide/cms/page-hierarchy.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable Hierarchy Functionality] | 全域 | 為您的內容頁面啟用頁面階層。 選項： `Yes` / `No` |
| [!UICONTROL Enable Hierarchy Metadata] | 全域 | 可讓您將中繼資料與階層中的頁面建立關聯。 選項： `Yes` / `No` |
| [!UICONTROL Default Layout for Hierarchy Menu] | 全域 | 決定預設選單樣式。 選項： `Content` / `Left Column` / `Right Column` |

{style="table-layout:auto"}

## [!UICONTROL Advanced Content Tools]

![進階內容工具](./assets/content-management-advanced-content-tools.png)<!-- zoom -->

<!-- [Advanced Content Tools](https://docs.magento.com/user-guide/cms/page-builder-workspace.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable Page Builder] | 全域 | 決定 [!DNL Page Builder] 進階內容工具可供使用。 選項： <br/>**`Yes`**- [!DNL Page Builder] 工作區會顯示在頁面、區塊、產品和類別的「內容」區段中。<br/>**`No`**  — 標準CMS編輯工具會出現在 _[!UICONTROL Content]_頁面、區塊、產品和類別的區段。 |
| [!UICONTROL Enable Page Builder Content Preview] | 全域 | 決定 [!DNL Page Builder] 產品和類別已啟用內容預覽。 選項： `Yes` / `No` <br/>**_注意：_**此設定為 `Yes` 預設情況下，但關閉預覽可以防止在產品或類別表單中載入預覽而導致的任何效能問題。 |
| [!UICONTROL Google Maps API Key] | 全域 | 此 [!DNL Google Maps] 來自您的Google帳戶的API金鑰。 |
| [!UICONTROL Test Key] |  | 驗證 [!DNL Google Maps] API金鑰。 |
| [!UICONTROL Google Maps Style] | 全域 | 貼上 [!DNL Google Maps] 在此設定JSON程式碼樣式，以變更Map內容型別的外觀和風格。 |
| [!UICONTROL Default Column Grid Size] | 全域 | 決定預設欄數 [!DNL Page Builder] 格線。 |
| [!UICONTROL Maximum Column Grid Size] | 全域 | 決定 [!DNL Page Builder] 格線。 |

{style="table-layout:auto"}

>[!TIP]
>
>Page Builder可讓您使用自訂版面輕鬆建立內容豐富的頁面，進而增強您的視覺敘事能力，並提高客戶參與度和忠誠度。 這些功能旨在改善品質，並縮短製作自訂頁面的時間和費用。 如需這些功能以及如何使用這些功能為您的Adobe Commerce或Magento Open Source商店建立吸引人的內容的詳細資訊，請參閱 [_頁面產生器使用手冊_](../../page-builder/guide-overview.md).
