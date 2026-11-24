---
title: 建立目錄擴充品牌規則
description: 瞭解如何建立和管理目錄擴充的品牌治理規則、定義產品複製需求，以及將規則套用至目錄擴充工作。
role: Admin, User, Leader
source-git-commit: 9d7a4f4e98fe2d2d51261d96a2e072c28925babd
workflow-type: tm+mt
source-wordcount: '639'
ht-degree: 1%
---
# 建立目錄擴充品牌規則

品牌治理和品牌治理規則僅適用於目錄擴充。 它們不適用於PDP擴充。 這些規則定義了[!DNL Commerce Catalog Agent]產生的產品名稱和說明需求。 編輯或設定預設品牌標準的預設規則，然後建立特定行銷活動、產品類別或子品牌的自訂規則。 建立[目錄擴充](catalog-enrichment.md)工作時，使用Select規則。

## 開啟品牌控管

1. 在Admin中，移至&#x200B;**[!UICONTROL AI Product Discovery]** > **[!UICONTROL Catalog Enrichment]**。
1. 開啟&#x200B;**[!UICONTROL Brand Governance]**&#x200B;標籤。

**品牌控管**&#x200B;標籤包含預設規則和您已建立的任何自訂規則。 您可以搜尋規則或篩選規則表格。

每一列您會看到&#x200B;**規則名稱**、**欄位**、**色調**、**上次修改時間**&#x200B;以及&#x200B;**狀態**。 預設規則標示為&#x200B;**[!UICONTROL Default]**。

**[!UICONTROL Needs your attention]**&#x200B;區域會醒目顯示需要處理的規則，例如需要設定的草稿或存在衝突的規則。 檢閱規則詳細資料並使用可用的動作，例如&#x200B;**[!UICONTROL Finish setup]**&#x200B;或&#x200B;**[!UICONTROL Fix conflict]**。

## 瞭解規則型別

「目錄擴充」支援預設規則與自訂規則。

### 預設規則

每個[!DNL Adobe Commerce]執行個體只有一個預設規則。 [!DNL Adobe Commerce]會使用空白欄位建立此規則。 其名稱已固定為&#x200B;**[!UICONTROL Global]**。 您可以編輯規則，但無法刪除規則。

當您建立目錄擴充工作而不選取自訂規則時，[!DNL Adobe Commerce]預設會套用預設規則。 「預設規則」提供「目錄擴充」的基準管理。

### 自訂規則

您可以為行銷活動、產品類別或子品牌建立任意數量的自訂規則。 自訂規則不會自動套用。 在建立目錄擴充工作時Select它。

自訂規則不會繼承預設規則的值。 建立自訂規則時，您可以複製預設規則的目前值，作為一次性起點。 預設規則的後續變更不會更新自訂規則。

對於當使用者未選取自訂規則時應該套用的標準，使用預設規則。 為具有不同需求的行銷活動或類別建立自訂規則。 新增自訂規則也需要的任何全域需求，因為自訂規則不會繼承全域值。

## 建立自訂規則

在本節中，您將瞭解如何建立品牌治理規則。

![建立品牌治理規則](./assets/brand-gov-create-rule.png)

1. 在&#x200B;**品牌治理**&#x200B;索引標籤中，按一下&#x200B;**[!UICONTROL Create Rule]**。
1. 選擇啟動規則的方式：
   - **[!UICONTROL Blank]**：自行設定所有值。
   - **[!UICONTROL Copy Global enrichment]**：以目前的「預設規則」值作為一次性副本開始。
   - **[!UICONTROL Draft with AI]**： （**即將推出**）說明您的品牌語調，以取得建議的規則值。
1. 輸入識別其用途的&#x200B;**規則名稱**，例如行銷活動、類別或子品牌。
1. 在&#x200B;**要增強**&#x200B;的欄位底下，設定產品名稱和產品描述需求。

   分別設定產品名稱和說明。 每個欄位都有自己的啟用切換器和治理需求。

1. 設定&#x200B;**產品名稱長度**。

   設定擴充產品名稱的最小和最大名稱長度範圍。 例如，規則最少需要20個字元，最多需要200個字元。

1. 設定&#x200B;**大寫**&#x200B;選項：

   - **[!UICONTROL Sentence case]**: `Waterproof hiking boots`
   - **[!UICONTROL Title Case]**: `Waterproof Hiking Boots`
   - **[!UICONTROL As written]**：保留來源文字的大小寫。

1. 描述&#x200B;**品牌色調**。 請參閱[設定品牌色調](#set-brand-tone)以取得指引。
1. 設定必要和排除的片語

   新增&#x200B;**[!UICONTROL Must include]**片語。
   新增**[!UICONTROL Never use]**&#x200B;片語。

1. 按一下&#x200B;**[!UICONTROL Save as draft]**&#x200B;稍後完成，或按一下&#x200B;**[!UICONTROL Publish rule]**&#x200B;讓規則可在建立目錄擴充規則時供選取。 按一下&#x200B;**[!UICONTROL Cancel]**&#x200B;離開而不儲存。

1. 您現在可以將規則套用至[目錄擴充](catalog-enrichment.md)工作。

### 設定品牌色調

在多行&#x200B;**[!UICONTROL Brand tone]**&#x200B;欄位中輸入指引，說明擴充名稱的聲音和樣式。

以下是一些您可能會用於&#x200B;**描述**&#x200B;的語調範例：

- **B2B工業**： `Write for the operator and the buyer. Open with what the unit does and where it fits in the kitchen, then throughput, utility requirements, footprint, and certifications. Plain, technical language. Mention cleaning and maintenance, because total cost of ownership drives the decision. No lifestyle language.`
- **豪華時尚**： `Quiet confidence. Lead with craftsmanship and provenance (atelier, tannery, technique), then how the piece wears and ages. Short, measured sentences. Sensory detail is fine. Never compare to other brands or mention price or value.`
- **電子消費品**： `Clear and benefit-led. Turn every spec into what it does for the user. Scannable short paragraphs or bullets. Put compatibility and what's in the box up front. Don't make performance claims without a source, and don't use comparative claims like "fastest"`
- **特色食品及雜貨**： `Warm and appetizing, but honest. Describe taste, texture, and aroma in concrete terms, then origin and how it's made, then serving ideas. Plain, friendly language. Put allergens and dietary attributes in a consistent closing line. Don't make health claims.`
- **家用傢俱**： `Inviting and practical. Open with how the piece is used, then dimensions, materials, and care. Help the shopper picture it in their space without overselling. Always mention assembly, delivery, and weight, since those drive returns.`
