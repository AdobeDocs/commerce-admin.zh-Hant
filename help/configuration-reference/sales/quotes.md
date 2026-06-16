---
title: '[!UICONTROL Sales] > [!UICONTROL Quotes]'
description: 檢閱Commerce管理員的[!UICONTROL Sales] &gt； [!UICONTROL Quotes]頁面上的組態設定。
exl-id: 9382552d-1be5-47f2-b0e3-931e5c6298d4
feature: Configuration, Quotes
TQID: https://experienceleague.adobe.com/puZjB2YCCyZXT0U6AdDBd-YjxopU637-yxgOaB6hkvM
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 193
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Quotes]

{{b2b-feature}}

>[!TIP]
>
>在安裝及啟用Adobe Commerce B2B後，即可使用公司專屬的功能個人化購買體驗。 Adobe Commerce B2B是整合式解決方案，可支援B2B和B2C模型。 如需B2B功能的詳細資訊，請參閱[Adobe Commerce B2B使用手冊](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html)。

{{config}}

<!-- [Quotes](https://experienceleague.adobe.com/en/docs/commerce-admin/b2b/quotes/quotes) -->

## [!UICONTROL General]

![一般](./assets/quotes-general.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Minimum Amount] | 網站 | 客戶提交報價請求前，扣除任何折扣後所需的購物車小計最小金額。 預設值： `0` |
| [!UICONTROL Minimum Amount Message] | 存放區檢視 | 當客戶嘗試提交報價請求，但未達到所需的最小金額時，顯示在購物車中的訊息。 |
| [!UICONTROL Default Expiration Period] | 網站 | 決定[報價單](../../b2b/quote-price-negotiation.md)的預設有效期限，為自提交報價單請求之日算起的時間期間。 選項： `Days` / `Weeks` / `Months` |

{style="table-layout:auto"}

## [!UICONTROL Attached Files]

![附加的檔案](./assets/quotes-attached-files.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL File formats for upload] | 全域 | 決定可附加至報價的檔案格式。 支援的預設值： `doc`、`docx`、`xls`、`xlsx`、`pdf`、`txt`、`jpg`、`png`和`jpeg` |
| [!UICONTROL Maximum file size] | 全域 | 決定附加至引號的檔案大小上限。 伺服器組態可以覆寫此設定。 |

{style="table-layout:auto"}
