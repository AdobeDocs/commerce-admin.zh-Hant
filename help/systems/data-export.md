---
title: 匯出資料
description: 瞭解資料匯出篩選器和屬性，以及如何從存放區匯出資料。
exl-id: 80e7a2fc-beaa-416e-a00f-a3cad5055975
feature: Products, Customers, Data Import/Export
source-git-commit: f8254db7d69e58c8e9a78948ee6e40f5ea88cea0
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 0%

---

# 匯出資料

熟悉資料庫結構的最佳方式是匯出資料，並在試算表中將其開啟。 熟悉此程式後，您就可以用它當作管理大量資訊的有效方式。

特殊字元（例如等號、大於和小於符號、單引號和雙引號、反斜線、垂直線和&amp;符號）可能會在資料傳輸期間造成問題。 為確保正確解譯這類特殊字元，可將其標示為&#x200B;_逸出序列_。 例如，如果資料包含文字字串，例如`code="str"`、`code="str2"`，將文字括在雙引號中可確保原始雙引號被理解為資料的一部分： `"code="str""`。 當系統遇到雙引號集合時，它知道雙引號外部集合正在封入實際資料。

資料匯出是非同步操作，會在背景執行，因此您可以在管理員中繼續工作，而不需要等候操作完成。 當工作完成時，系統會顯示訊息。

## 匯出條件

匯出篩選器用於根據屬性值指定您要在匯出檔案中的資料。 此外，您可以指定要將哪些屬性資料包括在匯出中或從中排除。

![資料匯出條件](./assets/data-export-entity-attributes-exclude.png){width="600" zoomable="yes"}

### 匯出篩選器

您可以使用篩選器來判斷匯出檔案中包含哪些SKU。 例如，如果您在「製造國家/地區」篩選器中輸入值，則匯出的CSV檔案只會包含在該國家/地區製造的產品。

篩選型別會對應至資料型別。 對於日期欄位，您可以從行事曆![行事曆圖示](../assets/icon-calendar.png)中選擇日期。 如需詳細資訊，請參閱[屬性輸入型別](../catalog/attributes-input-types.md)。

日期格式由[地區設定](../getting-started/store-details.md#locale-options)決定。

若要僅包含具有特定值（例如SKU）的記錄，請在「篩選」欄位中輸入值。 有些欄位（例如「價格」、「重量」及「將產品設為「新增」）具有起始/終止值範圍。

### 排除屬性

第一欄中的核取方塊用於從匯出檔案中排除屬性。 如果排除屬性，則會包含匯出資料中的關聯欄，但為空白。

| 排除 | 篩選 | 結果 |
|--- |--- |--- |
| ![已清除核取方塊](../assets/checkbox-clear.png) | 否 | 匯出的檔案包含所有現有記錄的每個屬性。 |
| ![已清除核取方塊](../assets/checkbox-clear.png) | 是 | 匯出檔案包含每個屬性，其中僅包含篩選允許的記錄。 |
| ![已選取核取方塊](../assets/checkbox-selected.png) | 否 | 匯出檔案不包含排除屬性的欄，但包含所有現有記錄。 |
| ![已選取核取方塊](../assets/checkbox-selected.png) | 是 | 匯出檔案不包含排除屬性的欄，僅包含篩選允許的記錄。 |

{style="table-layout:auto"}

## 匯出資料

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**。

1. 在&#x200B;_匯出設定_&#x200B;區段中，將&#x200B;**[!UICONTROL Entity Type]**&#x200B;設定為下列其中一項：

   - `Advanced Pricing`
   - `Products`
   - `Customer Finances`
   - `Customers Main File`
   - `Customer Addresses`
   - `Stock Sources`

   ![資料匯出設定](./assets/data-export-settings.png){width="600" zoomable="yes"}

1. 接受CSV的預設&#x200B;**[!UICONTROL Export File Format]**。

1. 如果要將資料中可能找到的任何特殊字元括為&#x200B;_逸出序列_，請選取&#x200B;**[!UICONTROL Fields Enclosure]**&#x200B;核取方塊。

1. 如有需要，請變更實體屬性的顯示。

   依預設，「實體屬性」段落會依字母順序列出所有可用的屬性。 您可以使用標準[清單控制項](../getting-started/admin-grid-controls.md)來搜尋特定屬性並排序清單。 「搜尋和重設篩選」控制清單的顯示，但不會影響要包含在匯出檔案中的屬性選擇。

   ![資料匯出篩選的實體屬性](./assets/data-export-filter-entity-attributes.png){width="600" zoomable="yes"}

1. 若要根據屬性值篩選匯出的資料，請執行下列動作：

   - 若要僅匯出具有特定屬性值的記錄，請在&#x200B;**[!UICONTROL Filter]**&#x200B;欄中輸入所需的值。 以下範例僅匯出特定SKU。

   - 若要在匯出中省略屬性，請選取該列開頭的&#x200B;**[!UICONTROL Exclude]**&#x200B;核取方塊。 例如，若要僅匯出`sku`和`image`欄，請選取其他所有屬性的核取方塊。 欄會顯示在匯出檔案中，但沒有任何值。

1. 向下捲動並按一下頁面右下角的&#x200B;**[!UICONTROL Continue]**。

   工作完成後，會透過訊息佇列處理檔案（確認cron工作正在執行）。 匯出的檔案儲存在`var/export/ folder`中。 如需訊息佇列的詳細資訊，請參閱&#x200B;_設定指南_&#x200B;中的[管理訊息佇列](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html?lang=zh-Hant)。

   您可以將匯出的CSV檔案儲存或開啟為試算表，接著編輯資料並將其匯入回您的存放區。

   >[!NOTE]
   >
   >依預設，所有匯出的檔案都在`<Magento-root-directory>/var/export`資料夾中。 如果已啟用遠端儲存模組，則所有匯出的檔案都在`<remote-storage-root-directory>/import_export/export`資料夾中。

## 疑難排解資源

如需疑難排解資料匯出問題的說明，請參閱下列Commerce支援知識庫文章：

- [匯出的產品.csv檔案未出現](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/exported-products-.csv-file-does-not-appear.html?lang=zh-Hant)
