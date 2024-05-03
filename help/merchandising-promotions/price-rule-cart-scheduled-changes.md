---
title: 購物車價格規則的排程變更
description: 瞭解如何在行銷活動中依排程套用購物車價格規則，並搭配其他內容變更分組。
exl-id: 4c9caa04-1e11-440d-b3db-7cc5fc83a08f
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: 3d04e7213d90bb4c323acce69ac31c1dbcb7ca49
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 0%

---

# 購物車價格規則的排程變更

{{ee-feature}}

購物車價格規則可作為行銷活動的一部分依排程套用，並與其他內容變更一起分組。 您可以根據價格規則的排程變更來建立行銷活動，或將變更套用至現有行銷活動。

>[!NOTE]
>
>此 [!UICONTROL From] 和 [!UICONTROL To] 欄位已移除於 ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce ，且無法直接在購物車價格規則上修改。 您必須為這些啟用建立排定的更新。

![購物車價格規則 — 排程變更](./assets/content-staging-price-rules-cart-scheduled-changes.png){width="700" zoomable="yes"}

>[!NOTE]
>
>所有排定的更新都會連續套用。 這表示任何實體在某個時間點只能有一個排程更新。 任何排定的更新都會套用至其時間範圍內的所有存放區檢視。 因此，一個實體無法同時擁有不同存放區檢視的不同排程更新。 所有存放區檢視中的所有實體屬性值（不受目前排程更新影響）都是從預設值取得，而不是從先前的排程更新取得。

如果同一個促銷活動中有多個價格規則在執行中，則 _[!UICONTROL Priority]_價格規則的設定會決定哪一個規則優先。 若要深入瞭解，請參閱 [內容分段](../content-design/content-staging.md).

請記住下列警告：

- 如果包含價格規則的促銷活動最初建立時沒有結束日期，則之後無法編輯促銷活動以包含結束日期。 建議您在建立行銷活動時新增結束日期，或建立現有行銷活動的重複版本，並根據需要新增結束日期至重複。
- 使用已排程的更新來啟用具有結束日期的購物車價格規則時，請務必將此規則設為最初停用。 已啟用的規則不會遵循結束日期。
- 優惠券未與購物車價格規則連結。 排定的更新不提供對的存取權 _[!UICONTROL Coupon]_，_[!UICONTROL Coupon Code]_， _[!UICONTROL Uses per Coupon]_、和_[!UICONTROL Uses per Customer]_ 欄位位於 _[!UICONTROL Rule Information]_標籤。 此外，所有設定均來自_[!UICONTROL Manage Coupon Codes]_ 索引標籤無法使用。

>[!IMPORTANT]
>
>Campaign **[!UICONTROL Start Date]** 和 **[!UICONTROL End Date]** 必須透過以下方式定義： **_預設_** 管理時區，由每個網站的當地時區加以轉換。 請考量下列範例：您有多個網站位在不同時區，但您想要根據美國時區啟動Campaign。 在這種情況下，您需要為每個當地時區排程單獨的更新，並設定 **[!UICONTROL Start Date]** 和 **[!UICONTROL End Date]** 從每個當地網站時區轉換為預設管理時區。
