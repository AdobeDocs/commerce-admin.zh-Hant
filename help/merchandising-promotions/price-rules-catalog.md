---
title: 目錄價格規則
description: 瞭解目錄價格規則，這些規則可用於根據一組已定義的條件，以折扣價格向買家提供產品。
exl-id: 8da95076-d724-41f6-b3ca-e61ff1906b72
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: f8254db7d69e58c8e9a78948ee6e40f5ea88cea0
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# 目錄價格規則

目錄價格規則可用來根據一組已定義的條件，以折扣價格提供產品給買家。 目錄價格規則不使用[優惠券代碼](price-rules-cart-coupon.md)，因為它們會在產品放入購物車之前觸發。

例如，您可以定義並設定價格規則的條件，當價格規則符合時，會自動顯示具有特殊或促銷價格的產品。 定義的規則屬性可能包括客戶群組、產品類別、折扣金額或百分比、產品顏色、產品大小，或是在您的商店中設定的幾乎任何產品屬性。 您可以設定價格規則的開始與結束日期，該價格規則會在您於規則中定義的日期自動開始與停止促銷。 已儲存規則的屬性可視需要更新或修改。

- ![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)您也可以將已定義的規則連結至[動態區塊](../content-design/dynamic-blocks.md)，以協助促銷商店中的事件或產品。

- ![Magento Open Source](../assets/open-source.svg) (僅限Magento Open Source)對於週期性促銷活動，您可以在每次想要執行促銷活動時，手動將儲存的規則設定為&#x200B;_作用中_&#x200B;或&#x200B;_非作用中_&#x200B;狀態。

## 存取型錄價格規則

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Catalog Price Rules]**。

   ![目錄價格規則](./assets/price-rule-catalog.png){width="700" zoomable="yes"}

1. 更新規則的屬性：

   - ![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)按一下「**[!UICONTROL Edit]**」以顯示&#x200B;_規則資訊_&#x200B;頁面。

   - ![Magento Open Source](../assets/open-source.svg) (僅限Magento Open Source)按一下清單中的規則以顯示[規則資訊]頁面。

   您可以在此變更規則的設定（類似[建立規則](price-rules-catalog-create.md)）。

## 篩選器選項

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL ID] | 輸入文字以篩選特定規則識別碼編號的清單。 |
| [!UICONTROL Rule] | 輸入文字，以根據建立規則時定義的規則名稱來篩選清單。 |
| [!UICONTROL Priority] | ![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)在此欄位中輸入文字，以根據為規則定義的優先順序來篩選清單。 |
| [!UICONTROL Web Site] | ![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)使用此選項以根據針對規則定義的網站來篩選清單。 |
| [!UICONTROL Action] | ![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)按一下&#x200B;**[!UICONTROL Edit]**&#x200B;以顯示規則資訊並更新規則設定（類似於建立規則）。 |
| [!UICONTROL Start] | ![Magento Open Source](../assets/open-source.svg) (僅限Magento Open Source)使用動態行事曆欄位（收件者：和寄件者：）根據建立規則時定義的規則開始日期來篩選清單。 |
| [!UICONTROL End] | ![Magento Open Source](../assets/open-source.svg) (僅限Magento Open Source)使用動態行事曆欄位（收件者：和寄件者：），依據建立規則時定義的規則結束日期來篩選清單。 |
| [!UICONTROL Status] | ![Magento Open Source](../assets/open-source.svg) (僅限Magento Open Source)使用此選項以根據規則狀態（`Active`或`Inactive`）來篩選清單。 |

{style="table-layout:auto"}
