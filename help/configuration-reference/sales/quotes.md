---
title: 『[!UICONTROL Sales] &gt； [!UICONTROL Quotes]『
description: 檢閱上的組態設定 [!UICONTROL Sales] &gt； [!UICONTROL Quotes] Commerce管理員的頁面。
exl-id: 9382552d-1be5-47f2-b0e3-931e5c6298d4
feature: Configuration, Quotes
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Quotes]

{{b2b-feature}}

>[!TIP]
>
>在安裝及啟用Adobe Commerce B2B後，即可使用公司專屬的功能個人化購買體驗。 Adobe Commerce B2B是整合式解決方案，可支援B2B和B2C模型。 如需B2B功能的詳細資訊，請參閱 [Adobe Commerce B2B使用手冊](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).

{{config}}

<!-- [Quotes](https://docs.magento.com/user-guide/sales/quotes.html) -->

## [!UICONTROL General]

![一般](./assets/quotes-general.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Minimum Amount] | 網站 | 客戶提交報價請求前，扣除任何折扣後所需的購物車小計最小金額。 預設值： `0` |
| [!UICONTROL Minimum Amount Message] | 存放區檢視 | 當客戶嘗試提交報價請求，但未達到所需的最小金額時，顯示在購物車中的訊息。 |
| [!UICONTROL Default Expiration Period] | 網站 | 決定a的預設生命週期 [引用](../../b2b/quote-price-negotiation.md) 作為提交報價請求日期起的時間期間。 選項： `Days` / `Weeks` / `Months` |

{style="table-layout:auto"}

## [!UICONTROL Attached Files]

![附加的檔案](./assets/quotes-attached-files.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL File formats for upload] | 全域 | 決定可附加至報價的檔案格式。 支援的預設值： `doc`， `docx`， `xls`， `xlsx`， `pdf`， `txt`， `jpg`， `png`、和 `jpeg` |
| [!UICONTROL Maximum file size] | 全域 | 決定附加至引號的檔案大小上限。 伺服器組態可以覆寫此設定。 |

{style="table-layout:auto"}
