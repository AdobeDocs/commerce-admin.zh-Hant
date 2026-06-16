---
title: '[!UICONTROL General] > [!UICONTROL Content Management]'
description: 檢閱Commerce管理員的[!UICONTROL General] &gt； [!UICONTROL Content Management]頁面上的組態設定。
exl-id: 67c5e89b-0a7c-4e4f-a5ad-10376c3ef6f9
feature: Configuration, Page Content
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案（Adobe管理的PaaS基礎結構）和內部部署專案的Adobe Commerce 。"
TQID: https://experienceleague.adobe.com/0xOspXoBYVeEE3ZvTlwkKNewR9YMAdbmch8RlRcE7S8
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 646
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL Content Management]

{{config}}

## [!UICONTROL WYSIWYG Options]

### [!UICONTROL TinyMCE 6]

![WYSIWYG選項](./assets/content-management-wysiwyg-options.png)<!-- zoom -->

<!-- [WYSIWYG Options](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/wysiwyg/editor) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable WYSIWYG Editor] | 存放區檢視 | 判斷是否已為存放區啟用編輯器。 選項：預設啟用/預設停用/完全停用 |
| [!UICONTROL WYSIWYG Editor] | 網站 | 決定用於WYSIWYG編輯器的TinyMCE編輯器版本。 選項： <br/>**`TinyMCE 6`**- （預設）使用TinyMCE版本6作為預設WYSIWYG編輯器。<br><br>_&#x200B;**&#x200B;注意：**&#x200B;_在Adobe Commerce和Magento Open Source 2.4.5中更新TinyMCE 5.10程式庫後，可解決在使用某些型別的URL更新影像或連結時，允許任意JavaScript執行的弱點。 TinyMCE 3在2.4.0版本中已過時，在2.4.3版本中已移除。 TinyMCE 4已在2.4.4版本中移除。 |
| [!UICONTROL Use Static URLs for Media Content in WYSIWYG] | 全域 | 決定是否要將[靜態URL](../../content-design/catalog-urls-dynamic-media.md)用於從WYSIWYG編輯器參考的媒體內容。 此設定會套用至WYSIWYG編輯器可用的所有位置，包括產品、類別、頁面和區塊。 選項： <br/>**`Yes`**— 針對以WYSIWYG編輯器插入的媒體內容使用靜態URL。 靜態URL是絕對的，如果存放區的[基底URL](../../stores-purchase/store-urls.md)變更，則會中斷。<br/>**`No`** （預設） — 根據`{{media url="..."}}`指示詞，對透過WYSIWYG編輯器插入的媒體內容使用動態URL。 動態URL是相對的，如果商店的基本URL有所變更，則不會中斷。 |

{style="table-layout:auto"}

>[!NOTE]
>
>TinyMCE已被Hugerte取代，成為Magento 2.4.6及更新版本中的預設WYSIWYG編輯器。

### [!UICONTROL HugeRTE]

![WYSIWYG選項](./assets/content-management-wysiwyg-options-hugerte.png)<!-- zoom -->

<!-- [WYSIWYG Options](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/wysiwyg/editor) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable WYSIWYG Editor] | 存放區檢視 | 判斷是否已為存放區啟用編輯器。 選項：預設啟用/預設停用/完全停用 |
| [!UICONTROL WYSIWYG Editor] | 網站 | 決定用於WYSIWYG編輯器的Hugerte編輯器版本。 |
| [!UICONTROL Use Static URLs for Media Content in WYSIWYG] | 全域 | 決定是否要將[靜態URL](../../content-design/catalog-urls-dynamic-media.md)用於從WYSIWYG編輯器參考的媒體內容。 此設定會套用至WYSIWYG編輯器可用的所有位置，包括產品、類別、頁面和區塊。 選項： <br/>**`Yes`**— 針對以WYSIWYG編輯器插入的媒體內容使用靜態URL。 靜態URL是絕對的，如果存放區的[基底URL](../../stores-purchase/store-urls.md)變更，則會中斷。<br/>**`No`** （預設） — 根據`{{media url="..."}}`指示詞，對透過WYSIWYG編輯器插入的媒體內容使用動態URL。 動態URL是相對的，如果商店的基本URL有所變更，則不會中斷。 |

{style="table-layout:auto"}

## [!UICONTROL CMS Page Hierarchy]

{{ee-feature}}

![CMS頁面階層](./assets/content-management-cms-page-hierarchy.png)<!-- zoom -->

<!--[CMS Page Hierarchy](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/pages/page-hierarchy) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable Hierarchy Functionality] | 全域 | 為您的內容頁面啟用頁面階層。 選項： `Yes` / `No` |
| [!UICONTROL Enable Hierarchy Metadata] | 全域 | 可讓您將中繼資料與階層中的頁面建立關聯。 選項： `Yes` / `No` |
| [!UICONTROL Default Layout for Hierarchy Menu] | 全域 | 決定預設選單樣式。 選項： `Content` / `Left Column` / `Right Column` |

{style="table-layout:auto"}

## [!UICONTROL Advanced Content Tools]

![進階內容工具](./assets/content-management-advanced-content-tools.png)<!-- zoom -->

<!-- [Advanced Content Tools](https://experienceleague.adobe.com/en/docs/commerce-admin/page-builder/walkthrough/3-catalog-content) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable Page Builder] | 全域 | 決定[!DNL Page Builder]進階內容工具是否可用。 選項： <br/>**`Yes`**- [!DNL Page Builder]工作區會顯示在頁面、區塊、產品和類別的「內容」區段中。<br/>**`No`** — 標準CMS編輯工具會出現在頁面、區塊、產品和類別的&#x200B;_[!UICONTROL Content]_&#x200B;區段中。 |
| [!UICONTROL Enable Page Builder Content Preview] | 全域 | 判斷是否針對產品和類別啟用[!DNL Page Builder]內容預覽。 選項： `Yes` / `No` <br/>**_Note:_**&#x200B;依預設會設為`Yes`，但關閉預覽可以防止在產品或類別表單中載入預覽而導致的任何效能問題。 |
| [!UICONTROL Google Maps API Key] | 全域 | 來自您Google帳戶的[!DNL Google Maps] API金鑰。 |
| [!UICONTROL Test Key] |  | 驗證[!DNL Google Maps] API金鑰。 |
| [!UICONTROL Google Maps Style] | 全域 | 在此處貼上[!DNL Google Maps]樣式JSON程式碼以變更Map內容型別的外觀。 |
| [!UICONTROL Default Column Grid Size] | 全域 | 決定[!DNL Page Builder]格線中的預設欄數。 |
| [!UICONTROL Maximum Column Grid Size] | 全域 | 決定[!DNL Page Builder]格線中的最大欄數。 |

{style="table-layout:auto"}

>[!TIP]
>
>Page Builder可讓您使用自訂版面輕鬆建立內容豐富的頁面，進而增強您的視覺storytelling並提高客戶參與度和忠誠度。 這些功能旨在改善品質，並縮短製作自訂頁面的時間和費用。 如需這些功能以及如何使用這些功能為您的Adobe Commerce或Magento Open Source商店建立吸引人的內容的詳細資訊，請參閱&#x200B;[_頁面產生器使用手冊_](../../page-builder/guide-overview.md)。
