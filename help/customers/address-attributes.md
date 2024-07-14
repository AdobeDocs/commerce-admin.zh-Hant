---
title: 客戶地址屬性
description: 瞭解客戶地址屬性，以及如何設定這些屬性屬性。
exl-id: 637a0f81-4d8f-40cb-a1b6-537229b2ce5b
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '1495'
ht-degree: 0%

---

# 客戶地址屬性

{{ee-feature}}

「客戶地址」屬性集決定從客戶帳戶或在[結帳](../stores-purchase/checkout-process.md)期間輸入[通訊錄](account-dashboard-address-book.md)的街道地址屬性。

可設定自訂地址屬性以提供其他資訊，例如選用的電子郵件地址、Skype帳戶、備用電話號碼、建築物或縣。 然後可以將自訂屬性合併到用來產生銷售檔案的[地址範本](address-templates.md)中。 建立自訂地址屬性的程式幾乎與建立[客戶屬性](attribute-properties.md)相同。

客戶地址屬性用於以下表單：

- [客戶地址註冊](account-create.md)
- [客戶帳戶地址](account-dashboard-address-book.md)

![管理員 — 客戶地址屬性](./assets/attributes-customer-address.png){width="700" zoomable="yes"}

## 步驟1：完成屬性特性

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Customer Address]**。

1. 按一下右上角的&#x200B;**[!UICONTROL Add New Attribute]**。

   ![客戶屬性屬性](./assets/attribute-customer-address-new.png){width="600" zoomable="yes"}

1. 在&#x200B;**[!UICONTROL Attribute Properties]**&#x200B;區段中，執行下列動作：

   - 輸入在資料輸入期間識別屬性的&#x200B;**[!UICONTROL Default Label]**。

   - 輸入識別系統內屬性的&#x200B;**[!UICONTROL Attribute Code]**。

     屬性程式碼必須以字母開頭，可包含小寫字母(a-z)和數字(0-9)的任何組合。 程式碼的長度必須少於30個字元，而且不能包含特殊字元或空格。 底線字元(_)可用來表示空格。

     >[!TIP]
     >
     >**_捷徑：_**&#x200B;若要只完成必要欄位，請向下捲動至[!UICONTROL Storefront Properties]，輸入[!UICONTROL Sort Order]，然後儲存。

1. 若要判斷資料輸入所使用的輸入控制項型別，請將&#x200B;**[!UICONTROL Input Type]**&#x200B;設定為下列其中一項：

   - `Text Field` — 單行文字欄位。
   - `Text Area` — 多行文字區域。
   - `Multiple Line` — 為屬性建立多個文字行，類似於多行街道地址。 個別資料輸入行的數量可以是2到20。 使用`Default Value`指定欄位的初始值。
   - `Date` — 使用快顯行事曆顯示日期欄位。 其他屬性：使用`Default Value`指定欄位的初始值。 <br/>使用`Minimal Value`指定可以輸入的最早日期。  使用`Maximum Value`指定可以輸入的最新日期。
   - `Dropdown` — 僅接受選取一個值的下拉式清單。
   - `Multiple Select` — 接受多個選取值的下拉式清單。
   - `Yes/No` — 僅提供`Yes`或`No`個值選擇的欄位。
   - `File (attachment)` — 允許檔案上傳並將其與客戶屬性關聯為附件的欄位。
   - `Image File` — 允許將影像上傳到相簿並與客戶屬性關聯的欄位。

1. 如果客戶必須在欄位中輸入值，請將&#x200B;**[!UICONTROL Values Required]**&#x200B;設為`Yes`。

1. 若要指派初始值給欄位，請輸入&#x200B;**[!UICONTROL Default Value]**。

1. 若要在儲存記錄之前檢查輸入到欄位中的資料是否準確，請將&#x200B;**[!UICONTROL Input Validation]**&#x200B;設定為允許在該欄位中的資料型別。 可用的值視指定的&#x200B;_[!UICONTROL Input Type]_而定。

   - `None` — 欄位在資料輸入期間沒有輸入驗證。
   - `Alphanumeric` — 在資料輸入期間接受任何數字(0-9)和字母字元(a-z、A-Z)的組合。 若要包含特殊字元，請參閱下一個步驟中的[!UICONTROL Escape HTML Entities]。
   - `Alphanumeric with Space` — 在資料輸入期間接受數字(0-9)、字母字元(a-z、A-Z)和空格的任意組合。
   - `Numeric Only` — 在資料輸入期間只接受數字(0-9)。
   - `Alpha Only` — 在資料輸入期間僅接受字母字元(a-z、A-Z)。
   - `URL` — 在資料輸入期間只接受URL。
   - `Email` — 在資料輸入期間只接受電子郵件地址。
   - `Length Only` — 根據輸入欄位的資料長度來驗證輸入。

1. 若要將前置處理篩選套用至在文字欄位、文字區域或多行輸入型別中輸入的值，請將&#x200B;**[!UICONTROL Input/Output Filter]**&#x200B;設定為下列其中一項：

   - `None` — 不對輸入欄位的文字套用篩選。
   - `Strip HTML Tags` — 從文字中移除HTML標籤。 此篩選器可協助清除從包含HTML標籤的其他來源貼入欄位中的資料。
   - `Escape  HTML Entities` — 將文字中發現的特殊字元轉換為有效的HTML逸出順序，例如`&;`。 逸出序列會括在&amp;符號和分號之間，常用於印刷體的智慧型引號、版權和商標符號。 逸出序列也可用來識別小於(`<`)和大於(`>`)符號等字元，以及程式碼中也使用的&amp;字元。 此篩選器可協助清除有時從文書處理器貼到資料庫欄位的特殊字元。

1. 完成客戶格線和區段屬性：

   - 若要在客戶格線中包含欄，請將&#x200B;**[!UICONTROL Add to Column Options]**&#x200B;設為`Yes`。

   - 若要依此屬性篩選客戶網格，請將&#x200B;**[!UICONTROL Use in Filter Options]**&#x200B;設為`Yes`。

   - 若要依具有不同篩選比對條件的文字屬性來篩選「客戶」網格，請將&#x200B;**[!UICONTROL Grid Filter Condition Type]**&#x200B;設為`Partial Match`、`Prefix Match`或`Full Match`。 它不會影響格線的&#x200B;_依關鍵字搜尋_&#x200B;欄位。

   - 若要依此屬性搜尋「客戶」網格，請將&#x200B;**[!UICONTROL Use in Search Options]**&#x200B;設為`Yes`。

   - 若要將此屬性提供給[客戶區段](customer-segments.md)，請將&#x200B;**[!UICONTROL Use in Customer Segment]**&#x200B;設為`Yes`。

## 步驟2：完成店面屬性

1. 向下捲動至&#x200B;**[!UICONTROL Storefront Properties]**&#x200B;區段。

   ![客戶地址屬性 — Storefront屬性](./assets/attribute-customer-address-storefront-properties.png){width="600" zoomable="yes"}

1. 若要讓客戶看到屬性，請將&#x200B;**[!UICONTROL Show on Storefront]**&#x200B;設為`Yes`。

1. 在&#x200B;**[!UICONTROL Sort Order]**&#x200B;欄位中輸入數字，當與其他屬性一起列出時，這會決定其外觀順序。

1. 將&#x200B;**[!UICONTROL Forms to Use]**&#x200B;設定為要包含屬性的每個表單。

   若要選擇這兩個選項，請在按一下每個表單時按住Ctrl鍵(PC)或Command鍵(Mac)。

   - [客戶地址註冊](account-create.md)
   - [客戶帳戶地址](account-dashboard-address-book.md)

## 步驟3：完成標籤並儲存

1. 在左側的面板中，選擇&#x200B;**[!UICONTROL Manage Labels/Options]**。

1. 在&#x200B;**[!UICONTROL Manage Titles]**&#x200B;底下，輸入標籤以識別每個[存放區檢視](../getting-started/websites-stores-views.md)的屬性。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Attribute]**。

   ![客戶地址屬性 — 標籤/選項](./assets/attribute-customer-address-new-manage-label-options.png){width="600" zoomable="yes"}

## 欄位說明

### [!UICONTROL Attribute Properties]

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Default Label] | 在管理員和店面中識別屬性的預設標籤。 |
| [!UICONTROL Attribute Code] | 識別系統內屬性的唯一代碼。 程式碼的長度最多可為21個字元，且不可包含空格或特殊字元。 可以使用底線符號，而非空格。 |
| [!UICONTROL Input Type] | 決定用於資料輸入的[輸入控制項](../catalog/attributes-input-types.md)。 選項： <br/>**`Text Field`**— 單行文字欄位。<br/>**`Text Area`** — 多行文字區域。 <br/>**`Multiple Line`**— 為屬性建立多個文字行，類似於多行街道地址。 個別資料輸入行的數量可以是2到20。<br/>**`Date`** — 使用快顯行事曆顯示日期欄位。<br/>**`Dropdown`**— 僅接受選取一個值的下拉式清單。<br/>**`Multiple Select`** — 接受多個選取值的下拉式清單。 <br/>**`Yes/No`**— 僅提供`Yes`或`No`個值選擇的欄位。<br/>**`File (attachment)`** — 允許檔案上傳並將其與客戶屬性關聯為附件的欄位。 <br/>**`Image File`**— 允許將影像上傳到相簿並與客戶屬性關聯的欄位。 |
| [!UICONTROL Values Required] | 決定是否必須在欄位中輸入值。 選項： `Yes` / `No` |
| [!UICONTROL Default Value] | 指定屬性的初始值。 |
| [!UICONTROL Input Validation] | 選項的選取由輸入型別決定。 選項： <br/>**`None`**— 欄位在資料輸入期間沒有輸入驗證。<br/>**`Alphanumeric`** — 在資料輸入期間接受任何數字(0-9)和字母字元(a-z、A-Z)的組合。 <br/>**`Alphanumeric with Space`**— 允許街道位址中的空格符合電信業者的最大長度要求。 結帳時，客戶可在收件者和寄件者的街道地址中，輸入數字(0-9)、字母字元(a-z、A-Z)和空格的任意組合。 儲存地址時，會裁剪任何額外的空格。<br/>**`Numeric Only`** — 在資料輸入期間只接受數字(0-9)。 <br/>**`Alpha Only`**— 在資料輸入期間僅接受字母字元(a-z、A-Z)。<br/>** URL **— 在資料輸入期間只接受URL。<br/>**`Email`** — 在資料輸入期間只接受電子郵件地址。 <br/>**`Length Only`**— 根據輸入欄位的資料長度來驗證輸入。 |
| [!UICONTROL Input/Output Filter] | 在儲存記錄之前，將前置處理篩選套用至在文字欄位、文字區域或多行輸入型別中輸入的值。 選項： <br/>**`None`**— 不會將篩選器套用至輸入欄位的文字。<br/>**`Strip HTML Tags`** — 從文字中移除HTML標籤。 此篩選器可協助清除從包含HTML標籤的其他來源貼入欄位中的資料。 <br/>**`Escape HTML Entities`**— 將文字中發現的特殊字元轉換為有效的HTML逸出順序，例如`amp;`。 逸出序列會括在&amp;符號和分號之間，常用於印刷體製作者的智慧型引號、版權符號和商標符號。 逸出序列也可用來識別小於(`<`)和大於(`>`)符號等字元，以及程式碼中也使用的&amp;字元。 此篩選器可協助清除有時從文書處理器貼到資料庫欄位的特殊字元。 |
| [!UICONTROL Add to Column Options] | 指定屬性是否包含在[客戶](./customers-all.md)格線中。 選項： `Yes` / `No` |
| 在篩選選項中使用 | 指定屬性是否可用作網格搜尋作業的篩選。 選項： `Yes` / `No` |
| [!UICONTROL Grid Filter Condition Type] | 指定從格線搜尋作業中屬性的篩選比對條件。 它不會影響格線的&#x200B;_[!UICONTROL Search by keyword]_欄位。 選項： `Partial Match` / `Prefix Match` / `Full Match` |
| [!UICONTROL Use in Search Options] | 指定屬性值是否可以在搜尋作業中作為關鍵字。 選項： `Yes` / `No` |
| [!UICONTROL Use in Customer Segment] | 決定屬性是否包含在[客戶區段](./customer-segments.md)條件中。 選項： `Yes` / `No` |

### [!UICONTROL Storefront Properties]

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Show on Storefront] | 決定屬性是否顯示為店面客戶資訊中的欄位。 選項： `Yes` / `No` |
| [!UICONTROL Sort Order] | 指定此屬性與其他客戶屬性相關的排序順序。 排序順序決定了使用鍵盤導覽時，欄位在資料輸入期間接收焦點的順序。 |
| [!UICONTROL Forms to Use in] | 決定具有資料輸入表單的頁面，其中屬性會顯示。 選項： <br/>[`Customer Address Registration`](account-create.md) <br/>[`Customer Account Address`](account-dashboard-address-book.md) |
