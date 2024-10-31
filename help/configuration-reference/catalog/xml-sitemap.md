---
title: '[!UICONTROL Catalog] &amp；gt； [!UICONTROL XML Sitemap]'
description: 檢閱Commerce管理員的[!UICONTROL Catalog] &amp；gt； [!UICONTROL XML Sitemap]頁面上的組態設定。
exl-id: 319c34e9-bd5f-46f8-810f-bc4d5228f9c9
feature: Configuration, Site Navigation
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 2%

---

# [!UICONTROL Catalog] > [!UICONTROL XML Sitemap]

{{config}}

## [!UICONTROL Categories Options]

![類別選項](./assets/xml-sitemap-categories-options.png)<!-- zoom -->

<!-- [Categories Options](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/seo/sitemap-xml) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Frequency] | 存放區檢視 | 決定Sitemap類別的更新頻率。 選項： `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | 存放區檢視 | 介於`0.0`和`1.0`之間的值，可決定類別Sitemap更新相對於其他內容的優先順序。 零(`0.0`)的優先順序最低。 |

{style="table-layout:auto"}

## [!UICONTROL Products Options]

![產品選項](./assets/xml-sitemap-products-options.png)<!-- zoom -->

<!-- [Products Options](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/seo/sitemap-xml) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Frequency] | 存放區檢視 | 決定Sitemap產品的更新頻率。 選項： `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | 存放區檢視 | 介於`0.0`和`1.0`之間的值，可決定產品Sitemap更新相對於其他內容的優先順序。 零(`0.0`)的優先順序最低。 |
| [!UICONTROL Add Images into Sitemap] | 存放區檢視 | 決定影像包含在網站地圖中的範圍。 選項： `None` / `Base Only` / `All` |

{style="table-layout:auto"}

## [!UICONTROL CMS Pages Options]

![CMS頁面選項](./assets/xml-sitemap-cms-pages-options.png)<!-- zoom -->

<!-- [CMS Pages Options](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/seo/sitemap-xml) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Frequency] | 存放區檢視 | 決定網站地圖CMS頁面的更新頻率。 選項： `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | 存放區檢視 | 介於`0.0`和`1.0`之間的值，可決定CMS頁面Sitemap更新相對於其他內容的優先順序。 零(`0.0`)的優先順序最低。 |

{style="table-layout:auto"}

## [!UICONTROL Store Url Options]

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Frequency] | 存放區檢視 | 決定儲存URL更新的頻率。 選項： `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | 存放區檢視 | 介於`0.0`和`1.0`之間的值，可決定存放區URL更新相對於其他內容的優先順序。 零(`0.0`)的優先順序最低。 |

{style="table-layout:auto"}

## [!UICONTROL Generation Settings]

![產生設定](./assets/xml-sitemap-generation-settings.png)<!-- zoom -->

<!-- [Generation Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/seo/sitemap-xml) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 存放區檢視 | 判斷是否有XML Sitemap可供存放區使用。 選項： `Yes` / `No` |
| [!UICONTROL Start Time] | 存放區檢視 | 指定網站地圖在一天中的小時、分鐘和秒進行更新。 |
| [!UICONTROL Frequency] | 存放區檢視 | 決定Sitemap更新的頻率。 選項： `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Error Email Recipient] | 存放區檢視 | 在Sitemap更新過程中發生錯誤時收到通知的人員的電子郵件地址。 如果有多個地址，請用逗號分隔每個地址。 |
| [!UICONTROL Error Email Sender] | 網站 | 識別顯示為錯誤通知寄件者的商店聯絡人。 選項： `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Error Email Template] | 網站 | 識別用於錯誤通知的電子郵件範本。 預設範本： `Sitemap generate Warnings` |

{style="table-layout:auto"}

## [!UICONTROL Sitemap File Limits]

![Sitemap檔案限制](./assets/xml-sitemap-sitemap-file-limits.png)<!-- zoom -->

<!-- [Sitemap File Limits](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/seo/sitemap-xml) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Maximum No of URLs Per File] | 存放區檢視 | 決定單一Sitemap可包含的URL數量上限。 |
| [!UICONTROL Maximum File Size] | 存放區檢視 | 決定產生的Sitemap大小上限（位元組）。 |

{style="table-layout:auto"}

## [!UICONTROL Search Engine Submission Settings]

![搜尋引擎提交設定](./assets/xml-sitemap-search-engine-submission-settings.png)<!-- zoom -->

<!-- [Search Engine Submission Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/seo/sitemap-xml) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable Submission to Robots.txt] | 存放區檢視 | 啟用為robots.txt檔案提交的指令。 選項： `Yes` / `No` |

{style="table-layout:auto"}
