---
title: 購物車價格規則的排程變更
description: 瞭解如何在行銷活動中依排程套用購物車價格規則，並搭配其他內容變更分組。
exl-id: 4c9caa04-1e11-440d-b3db-7cc5fc83a08f
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: 0ceb61e6f1629a3bef16c550362c1db25b4aefa5
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 0%

---

# 購物車價格規則的排程變更

{{ee-feature}}

購物車價格規則可作為行銷活動的一部分依排程套用，並與其他內容變更一起分組。 您可以根據價格規則的排程變更來建立行銷活動，或將變更套用至現有行銷活動。

>[!NOTE]
>
>[!UICONTROL From]和[!UICONTROL To]欄位已在![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce中移除，無法直接在購物車價格規則上修改。 您必須為這些啟用建立排定的更新。

![購物車價格規則 — 排程變更](./assets/content-staging-price-rules-cart-scheduled-changes.png){width="700" zoomable="yes"}

>[!NOTE]
>
>所有排定的更新都會連續套用。 這表示任何實體在某個時間點只能有一個排程更新。 任何排定的更新都會套用至其時間範圍內的所有存放區檢視。 因此，一個實體無法同時擁有不同存放區檢視的不同排程更新。 所有存放區檢視中的所有實體屬性值（不受目前排程更新影響）都是從預設值取得，而不是從先前的排程更新取得。

如果在相同促銷活動中執行多個價格規則，則價格規則的&#x200B;_[!UICONTROL Priority]_設定會決定哪一個規則優先。 若要深入瞭解，請參閱[內容暫存](../content-design/content-staging.md)。

>[!NOTE]
>
>如果最初建立的有效行銷活動沒有結束日期，則無法在稍後編輯行銷活動以包含結束日期。 在這種情況下，必須建立重複的行銷活動並輸入所需的結束日期。

>[!NOTE]
>
>如果行銷活動連結到多個購物車價格規則，則只能從[內容測試儀表板](../content-design/content-staging-dashboard.md)編輯行銷活動。

請記住下列警告：

- 如果包含價格規則的促銷活動最初建立時沒有結束日期，則之後無法編輯促銷活動以包含結束日期。 建議您在建立行銷活動時新增結束日期，或建立現有行銷活動的重複版本，並根據需要新增結束日期至重複。
- 使用已排程的更新來啟用具有結束日期的購物車價格規則時，請務必將此規則設為最初停用。 已啟用的規則不會遵循結束日期。
- 優惠券未與購物車價格規則連結。 排定的更新未提供&#x200B;_[!UICONTROL Rule Information]_索引標籤上_[!UICONTROL Coupon]_、_[!UICONTROL Coupon Code]_、_[!UICONTROL Uses per Coupon]_&#x200B;和&#x200B;_[!UICONTROL Uses per Customer]_欄位的存取權。 此外，_[!UICONTROL Manage Coupon Codes]_&#x200B;標籤中的所有設定都無法使用。

>[!IMPORTANT]
>
>行銷活動&#x200B;**[!UICONTROL Start Date]**&#x200B;和&#x200B;**[!UICONTROL End Date]**&#x200B;必須使用從每個網站的當地時區轉換而來的&#x200B;**_預設_**&#x200B;管理時區來定義。 請考量下列範例：您有多個網站位在不同時區，但您想要根據美國時區啟動Campaign。 在此情況下，您需要為每個當地時區排程個別的更新，並將&#x200B;**[!UICONTROL Start Date]**&#x200B;和&#x200B;**[!UICONTROL End Date]**&#x200B;從每個當地網站時區轉換為預設管理時區。
