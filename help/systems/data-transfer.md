---
title: 資料傳輸
description: 瞭解資料傳輸支援，包括資料驗證。
exl-id: 5057e398-c458-42e9-8ec0-bf116a667a3c
feature: System, Data Import/Export
source-git-commit: b89d6b08d0559dc769a8c51570696f033f23c7f3
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# 資料傳輸

使用匯入和匯出工具，在單一操作中管理多個記錄。 您可以匯入新專案以及更新、取代和刪除現有產品集。

例如，您可以將新產品新增至詳細目錄、更新產品資料和進階價格資料，以及用新產品取代一組現有產品。 匯入和匯出工具可協助您更有效率地管理大型產品目錄，因為您可以匯出資料、在試算表中編輯資料，以及將資料匯回您的存放區，而不必在「管理員」中執行多項作業。


>[!NOTE]
>
>Adobe Commerce也支援SaaS資料匯出，以將產品資料從Commerce伺服器傳輸至SaaS服務。 SaaS資料匯出已與Commerce SaaS服務整合，包括 [產品Recommendations](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/overview.html)， [即時搜尋](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/overview)、和 [目錄服務](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/catalog-service/guide-overview). 如需詳細資訊，請參閱 [SaaS資料匯出指南](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview).

## 資料驗證

所有資料都必須通過驗證，以確保值的品質、正確性和完整性，才能將其匯入存放區。 當您按一下「 」，驗證就會開始 **[!UICONTROL Check Data]**. 在程式進行期間，匯入檔案中的所有圖元都會被驗證為符合下列情況：

- **屬性**  — 驗證欄標題名稱，確保它們符合系統資料庫中對應的屬性。 每個屬性的值都會受到檢查，以確保其符合資料型別（小數、整數、varchar、文字和日期時間）的需求。
- **複雜資料**  — 驗證來自已定義集合的值（例如下拉式清單或多重選取輸入型別），以確保這些值存在於已定義集合中。
- **服務資料**  — 會驗證服務資料欄中的值，以確保屬性或複雜資料值與系統資料庫中已定義的值一致。
- **必要值**  — 對於新實體，會檢查檔案中是否存在必要的屬性值。 對於現有實體，不需要重新檢查必要屬性值的存在。
- **分隔符號**  — 雖然在試算表中檢視分隔符號時不會顯示，但CSV檔案中的資料值會以逗號分隔，且文字值會以雙引號括住。 在驗證程式中，會驗證分隔符號的格式以及包含字元字串的每一組引號。

驗證結果會顯示在「驗證結果」區段中，並包含下列資訊：

- 核取的實體數
- 無效列數
- 找到的錯誤數

如果資料有效，則 _匯入成功_ 訊息便會出現。

![系統訊息 — 檔案有效](./assets/data-import-validation-message.png){width="500" zoomable="yes"}

如果驗證失敗，請閱讀每個錯誤的說明，並在CSV檔案中更正問題。 例如，如果某列包含無效的SKU，則匯入程式會停止，而該列及所有後續列都不會匯入。 在正確解決問題後，再次匯入資料。 如果發生許多錯誤，則可能需要數次嘗試才能通過驗證。

### 資料驗證訊息

#### 驗證

- `Product with specified SKU not found in rows: 1`
- `URL key for specified store already exists`
- `'7z' file extension is not supported`
- `TXT file extension is not supported`

#### 錯誤次數

- `Wrong field type. Type in the imported file %decimal%, expected type is %text%.`
- `Value is not allowed. Attribute value does not exist in the system.`
- `Field %column name% is required.Wrong value separator is used.`
- `Wrong encoding used. Supported character encoding is UTF-8 and Windows-1252.`
- `Imported file does not contain SKU field.`
- `SKU does not exist in the system.`
- `Column name %column name% is invalid. Should start with a letter. Alphanumeric.`
- `Imported file does not contain a header.`
- `%website name% website does not exist in the system.`
- `%storeview name% storeview does not exist in the system.`
- `Imported attribute %attribute name% does not exist in the system.`
- `Imported resource (image) could not be downloaded from external resource due to timeout or access permissions.`
- `Imported resource (image) does not exist in the local media storage.`
- `Product creation error displayed to the user equal to the one seen during manual product save.`
- `Advanced Price creation error displayed to the user equal to the one seen during the manual product save.`
- `Customer creation error displayed to the user equal to the one seen during the manual customer save.`
