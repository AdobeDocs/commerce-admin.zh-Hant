---
title: 內容分段
description: 內容測試讓您的業務團隊能夠直接從管理員輕鬆建立、預覽和排程您商店的各種內容更新。
exl-id: 929cd020-cbc7-40bf-a22c-02df35212ecf
feature: Page Content, Staging
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"
source-git-commit: 07d7ca7e7f6af42fe8e06dc3c49c2df5f50d1425
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 0%

---

# 內容分段

{{ee-feature}}

內容測試讓您的業務團隊能夠直接從&#x200B;_管理員_&#x200B;輕鬆建立、預覽和排程您商店的各種內容更新。 例如，不要以靜態頁面來思考，而應將頁面視為不同元素的集合，可根據排程&#x200B;_開啟_&#x200B;或&#x200B;_關閉_。 您可以使用內容測試來建立頁面，此頁面會在一年中依排程自動變更。

術語&#x200B;_行銷活動_&#x200B;指的是排程變更的記錄，或是從測試儀表板管理的變更集合。 您可在行事曆或時間軸上檢視變更。 術語&#x200B;_排程變更_&#x200B;和&#x200B;_排程更新_&#x200B;可互換，且是指單一變更。

當您排程特定時段內的內容變更時，排程的變更過期時內容會回復到先前的版本。 您可以建立相同基準內容的多個版本，以供日後更新使用。 您也可以在時間軸中後退以檢視內容的舊版本。 若要儲存草稿版本，只需在時間軸上指派太遠，以至於永遠不會投入生產的日期。

## 內容暫存物件與行銷活動

與「開始日期」和「結束日期」相關的欄位已從Adobe Commerce中移除，且無法直接在購物車價格規則、目錄價格規則、產品、類別和CMS頁面上修改。 您必須為這些啟用建立排定的更新。

所有排定的更新都會連續套用，這表示任何實體一次只能有一個排定的更新。 任何排定的更新都會套用至其時間範圍內的所有存放區檢視。 因此，實體無法同時針對不同的存放區檢視有不同的排程更新。 所有存放區檢視中的所有實體屬性值（不受目前排程更新影響）都是從預設值取得，而不是從先前的排程更新取得。

為下列任何物件建立新的排程更新時，會建立對應的促銷活動作為預留位置，_[!UICONTROL Scheduled Changes]_&#x200B;方塊會出現在頁面頂端。 預留位置行銷活動具有開始日期，但無結束日期。 您可以將內容更新排程為行銷活動的一部分，然後依日期、時間或存放區檢視來預覽和共用變更。 為一個物件建立新行銷活動後，您可以將其指派為其他物件的排程更新。

- [產品](../catalog/product-scheduled-changes.md)
- [類別](../catalog/category-scheduled-changes.md)
- [目錄價格規則](../merchandising-promotions/price-rule-catalog-scheduled-changes.md)
- [購物車價格規則](../merchandising-promotions/price-rule-cart-scheduled-changes.md)
- [CMS頁面](pages-workspace.md#scheduled-changes)
- [CMS區塊](blocks.md)

## 內容測試工作流程

1. **建立基準線內容**

   基線是沒有行銷活動的資產內容，且包含頁面頂端&#x200B;_[!UICONTROL Scheduled Changes]_&#x200B;區段以下的所有內容。 一律會使用基準線內容，除非有在時間軸上該位置排程變更的作用中行銷活動。

1. **建立第一個行銷活動**

   視需要使用開始和結束日期來建立您的第一個行銷活動。 若要讓行銷活動成為開放式，請將結束日期保留空白。 第一個行銷活動結束時，會還原原始基準線內容。

   行銷活動開始日期和結束日期必須使用&#x200B;**_預設值_**&#x200B;管理時區來定義，該時區會從每個網站的當地時區轉換。 請考量下列範例：您有多個網站位在不同時區，但您想要根據美國時區啟動行銷活動。 在此情況下，您必須為每個當地時區排程個別的更新，並將&#x200B;**[!UICONTROL Start Date]**&#x200B;和&#x200B;**[!UICONTROL End Date]**&#x200B;從每個當地網站時區轉換為預設的管理時區。

1. **新增第二個行銷活動**

   建立第二個行銷活動，視需要提供開始和結束日期。 第二個行銷活動可指派給完全不同的時段。 為相同資產建立多個行銷活動時，行銷活動不能重疊。 您可以視需要建立儘可能多的行銷活動。

   可將多個資產指派給尚未開始的現有行銷活動。 例如，可以在相同行銷活動的範圍中，以未來的開始日期更新兩個不同的產品價格。

   >[!NOTE]
   >
   >如果行銷活動連結到多個實體，則只能從[內容測試儀表板](content-staging-dashboard.md)編輯行銷活動。

1. **還原基準線內容**

   如果所有行銷活動都有結束日期，則當所有作用中行銷活動結束時，會還原基準內容。

   >[!NOTE]
   >
   >如果最初建立的有效行銷活動沒有結束日期，則無法在稍後編輯行銷活動以包含結束日期。 在這種情況下，必須建立重複的行銷活動並輸入所需的結束日期。

>[!NOTE]
>
>當實體的中繼更新作用中時，編輯實體即會編輯目前作用中的中繼更新。 這不會影響基準內容，基準內容會在預備更新結束時還原。

## [!UICONTROL Content Staging]儀表板

[!UICONTROL Content Staging] [儀表板](content-staging-dashboard.md)提供所有計畫網站變更和更新的可見度。 您可以預覽行銷活動的任何一天、日期範圍或時段，並與他人共用。

![中繼儀表板](./assets/content-staging-dashboard-grid.png){width="600" zoomable="yes"}

## 內容測試示範

若要瞭解內容測試，請觀看此影片：

>[!VIDEO](https://video.tv.adobe.com/v/343784?quality=12&learn=on)

## 疑難排解資源

如需疑難排解內容測試問題的說明，請參閱下列[!DNL Commerce]支援知識庫文章：

- [由於內容暫存問題，所有頁面都出現404錯誤](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/site-down-or-unresponsive/error-404-on-all-pages-due-to-content-staging-issue.html)
- [已排程的內容暫存更新未以過時的Fastly快取顯示](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/scheduled-content-staging-updates-not-displayed-with-stale-fastly-cache.html)
- [我可以針對共用目錄中的價格排程內容測試更新嗎？](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/faq/can-i-schedule-content-staging-updates-for-prices-in-a-shared-catalog.html)
