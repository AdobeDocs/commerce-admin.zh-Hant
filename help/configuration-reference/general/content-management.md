---
title: '[!UICONTROL General] &amp；gt； [!UICONTROL Content Management]'
description: 檢閱Commerce管理員的[!UICONTROL General] &amp；gt； [!UICONTROL Content Management]頁面上的組態設定。
exl-id: 67c5e89b-0a7c-4e4f-a5ad-10376c3ef6f9
feature: Configuration, Page Content
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL Content Management]

{{config}}

## [!UICONTROL WYSIWYG Options]

![WYSIWYG選項](./assets/content-management-wysiwyg-options.png)<!-- zoom -->

<!-- [WYSIWYG Options](https://experienceleague.adobe.com/zh-hant/docs/commerce-admin/content-design/wysiwyg/editor) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable WYSIWYG Editor] | 存放區檢視 | 判斷是否已為存放區啟用編輯器。 選項：預設啟用/預設停用/完全停用 |
| [!UICONTROL WYSIWYG Editor] | 網站 | 決定用於WYSIWYG編輯器的TinyMCE編輯器版本。 選項： <br/>**`TinyMCE 5`**- （預設）使用TinyMCE版本5作為預設WYSIWYG編輯器。<br><br>_&#x200B;**&#x200B;注意：**&#x200B;_在Adobe Commerce和Magento Open Source2.4.5中更新TinyMCE 5.10程式庫時，解決了在使用某些型別的URL更新影像或連結時允許任意JavaScript執行的漏洞。 TinyMCE 3在2.4.0版本中已過時，在2.4.3版本中已移除。 TinyMCE 4已在2.4.4版本中移除。 |
| [!UICONTROL Use Static URLs for Media Content in WYSIWYG] | 全域 | 決定是否要將[靜態URL](../../content-design/catalog-urls-dynamic-media.md)用於從WYSIWYG編輯器參考的媒體內容。 此設定會套用至WYSIWYG編輯器可用的所有位置，包括產品、類別、頁面和區塊。 選項： <br/>**`Yes`**— 針對以WYSIWYG編輯器插入的媒體內容使用靜態URL。 靜態URL是絕對的，如果存放區的[基底URL](../../stores-purchase/store-urls.md)變更，則會中斷。<br/>**`No`** （預設） — 根據`{{media url="..."}}`指示詞，對透過WYSIWYG編輯器插入的媒體內容使用動態URL。 動態URL是相對的，如果商店的基本URL有所變更，則不會中斷。 |

{style="table-layout:auto"}

## [!UICONTROL CMS Page Hierarchy]

{{ee-feature}}

![CMS頁面階層](./assets/content-management-cms-page-hierarchy.png)<!-- zoom -->

<!--[CMS Page Hierarchy](https://experienceleague.adobe.com/zh-hant/docs/commerce-admin/content-design/elements/pages/page-hierarchy) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable Hierarchy Functionality] | 全域 | 為您的內容頁面啟用頁面階層。 選項： `Yes` / `No` |
| [!UICONTROL Enable Hierarchy Metadata] | 全域 | 可讓您將中繼資料與階層中的頁面建立關聯。 選項： `Yes` / `No` |
| [!UICONTROL Default Layout for Hierarchy Menu] | 全域 | 決定預設選單樣式。 選項： `Content` / `Left Column` / `Right Column` |

{style="table-layout:auto"}

## [!UICONTROL Advanced Content Tools]

![進階內容工具](./assets/content-management-advanced-content-tools.png)<!-- zoom -->

<!-- [Advanced Content Tools](https://experienceleague.adobe.com/zh-hant/docs/commerce-admin/page-builder/walkthrough/3-catalog-content) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable Page Builder] | 全域 | 決定[!DNL Page Builder]進階內容工具是否可用。 選項： <br/>**`Yes`**- [!DNL Page Builder]工作區會顯示在頁面、區塊、產品和類別的「內容」區段中。<br/>**`No`** — 標準CMS編輯工具會出現在頁面、區塊、產品和類別的&#x200B;_[!UICONTROL Content]_&#x200B;區段中。 |
| [!UICONTROL Enable Page Builder Content Preview] | 全域 | 判斷是否針對產品和類別啟用[!DNL Page Builder]內容預覽。 選項： `Yes` / `No` <br/>**_注意：_**&#x200B;這預設為`Yes`，但關閉預覽可以防止在產品或類別表單中載入預覽而導致的任何效能問題。 |
| [!UICONTROL Google Maps API Key] | 全域 | 來自您Google帳戶的[!DNL Google Maps] API金鑰。 |
| [!UICONTROL Test Key] |  | 驗證[!DNL Google Maps] API金鑰。 |
| [!UICONTROL Google Maps Style] | 全域 | 在此處貼上[!DNL Google Maps]樣式JSON程式碼以變更Map內容型別的外觀。 |
| [!UICONTROL Default Column Grid Size] | 全域 | 決定[!DNL Page Builder]格線中的預設欄數。 |
| [!UICONTROL Maximum Column Grid Size] | 全域 | 決定[!DNL Page Builder]格線中的最大欄數。 |

{style="table-layout:auto"}

>[!TIP]
>
>Page Builder可讓您使用自訂版面輕鬆建立內容豐富的頁面，進而增強您的視覺敘事能力，並提高客戶參與度和忠誠度。 這些功能旨在改善品質，並縮短製作自訂頁面的時間和費用。 如需這些功能以及如何使用這些功能為您的Adobe Commerce或Magento Open Source商店建立吸引人的內容的詳細資訊，請參閱&#x200B;[_頁面產生器使用手冊_](../../page-builder/guide-overview.md)。
