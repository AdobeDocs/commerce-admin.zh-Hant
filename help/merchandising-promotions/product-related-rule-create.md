---
title: 建立相關的產品規則
description: 瞭解如何建立可觸發的相關產品規則，以顯示相關產品、向上銷售和交叉銷售。
exl-id: fbc059ec-d3e6-46ca-810a-a979a0631dd8
feature: Merchandising, Products, Storefront
source-git-commit: cea943cd7f4d148c885fbd113c3bc08bfdf63ea0
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 0%

---

# 建立相關的產品規則

{{ee-feature}}

建立相關產品規則的程式與設定價格規則類似。 首先，請定義相符條件，然後選擇要顯示的產品。 在任何指定時間，都可能會觸發數個作用中規則來顯示相關產品、向上銷售和交叉銷售。 每個規則的優先順序會決定產品區塊在頁面上出現的順序。

>[!NOTE]
>
>若要在目標規則中使用屬性，[_[!UICONTROL Use for Promo Rule Conditions]_](../catalog/product-attributes.md)屬性必須設定為`Yes`。

>[!NOTE]
>
>`All Store Views`範圍值一律用於所有產品屬性的[!UICONTROL Products to Match]和[!UICONTROL Products to Display]條件。 當產品屬性針對不同的商店檢視和網站具有不同值時，這也適用。

## 建立相關的產品規則

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Related Product Rules]**。

1. 按一下右上角的&#x200B;**[!UICONTROL Add Rule]**。

   ![相關產品規則 — 資訊](./assets/catalog-related-products-rule-information.png){width="600" zoomable="yes"}

1. 完成&#x200B;**[!UICONTROL Rule Information]**，如下所示：

   - 輸入&#x200B;**[!UICONTROL Rule Name]**&#x200B;以識別在Admin中工作時的規則。

   - 針對&#x200B;**[!UICONTROL Priority]**，輸入當其他規則的結果鎖定相同位置時，決定結果在頁面上出現順序的數字。 數字`1`是最高優先順序。

   - 若要啟用規則，請將&#x200B;**[!UICONTROL Status]**&#x200B;設為`Active`。

   - 將&#x200B;**[!UICONTROL Apply To]**&#x200B;設定為下列其中一項：

      - `Related Products`
      - `Up-sells`
      - `Cross-sells`

   - 如果規則在特定時間範圍內為使用中，請輸入&#x200B;**[!UICONTROL From]**&#x200B;和&#x200B;**[!UICONTROL To]**&#x200B;日期。

   - 針對&#x200B;**[!UICONTROL Result Limit]**，輸入要出現在結果清單中的記錄數。 最大數目為20。

   - 如果規則套用至特定的[客戶區段](../customers/customer-segments.md)，請將&#x200B;**[!UICONTROL Customer Segments]**&#x200B;設為`Specified`並從清單中選擇客戶區段。

   - 如果規則套用至特定的[Real-Time CDP對象](../customers/audience-activation.md)，請將&#x200B;**[!UICONTROL Real-Time CDP Audience]**&#x200B;設為`Specified`並從清單中選擇Real-Time CDP對象。 此功能為測試版。 如果您想要加入Beta版計畫，請傳送要求給[dataconnection@adobe.com](mailto:dataconnection@adobe.com)。

     ![相關產品規則 — Real-Time CDP對象](./assets/rtcdp-related-products.png){width="500"}

1. 在左側面板中，選擇&#x200B;**[!UICONTROL Products to Match]**&#x200B;並建置條件，就像您建置[目錄價格規則](price-rules-catalog.md)一樣。

   ![相關產品規則 — 符合的產品](./assets/catalog-related-products-match.png){width="500"}

1. 在左側面板中，選擇&#x200B;**[!UICONTROL Products to Display]**&#x200B;並建置結果條件，就像您建置[目錄價格規則](price-rules-catalog.md)一樣。

   ![相關產品規則 — 要顯示的產品](./assets/catalog-related-products-to-display.png){width="500"}

   完成條件以說明您要包含在顯示結果中的產品。

1. 完成時，按一下&#x200B;**[!UICONTROL Save]**。

## 刪除相關的產品規則

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Related Product Rules]**。

1. 尋找您要刪除的相關產品規則。

1. 按一下規則以開啟詳細資訊頁面。

1. 按一下右上角的&#x200B;**[!UICONTROL Delete]**。

1. 若要確認動作，請按一下&#x200B;**[!UICONTROL OK]**。

## 相關產品規則示範

觀看此影片以瞭解如何建立相關的產品規則：

>[!VIDEO](https://video.tv.adobe.com/v/343837?quality=12&learn=on)

## 欄位說明

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Rule Name] | 識別內部使用規則的名稱。 |
| [!UICONTROL Priority] | 決定規則的結果與針對頁面上相同位置的其他結果集一起顯示時的顯示順序。 此值可設為任何整數，最高優先順序為1。 例如，如果有多個適用的向上銷售規則，優先順序最高的規則會出現在其他規則之前。 每組結果中的產品排序順序是隨機的。 任何手動設定的向上銷售、交叉銷售及相關產品，一律會出現在任何規則型產品促銷活動之前的頁面上。 |
| [!UICONTROL Status] | 控制規則的作用中狀態。 選項： `Active` / `Inactive` |
| [!UICONTROL Apply To] | 識別與規則相關聯的產品關係型別。 選項： `Related Products` / `Up-sells` / `Cross-sells` |
| [!UICONTROL From Date] | 如果規則在一段時間內有效，此設定會決定規則生效的第一個日期。 |
| [!UICONTROL To Date] | 如果規則在一段時間內有效，此設定會決定規則最後有效的日期。 |
| [!UICONTROL Result Limit] | 決定一次出現在結果中的產品數量。 最大數目為20。 如果找到更多相符的結果，每次重新整理頁面時，產品都會在區塊中旋轉。 |
| [!UICONTROL Customer Segments] | 識別規則套用的客戶區段。 選項： `All` / `Specified` |

{style="table-layout:auto"}
