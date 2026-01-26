---
title: 商店本地化
description: 瞭解如何將商店或商店檢視本地化。
exl-id: 64e1b431-f599-444c-9d39-207bb95f0400
topic: Commerce, Localization
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '725'
ht-degree: 0%

---

# 商店本地化

在您商店的所有頁面中，大多數看似以硬式編碼撰寫的文字，可以透過變更檢視的地區設定來立即變更為不同的語言。 變更地區設定實際上並不會逐字翻譯文字，而只是參照不同的翻譯表格，提供整個存放區使用的介面文字。 可變更的文字包含導覽標題、標籤、按鈕和連結，例如&#x200B;_我的購物車_&#x200B;和&#x200B;_我的帳戶_。 您也可以使用[內嵌翻譯](../configuration-reference/advanced/developer.md)工具來修改介面中的文字。

在Commerce Marketplace的[翻譯與本地化](https://marketplace.magento.com/extensions/content-customizations/translations-localization.html){:target="_blank"}下可找到語言套件。 Marketplace會持續新增新擴充功能，因此請經常回來檢視。

## 步驟1：安裝語言套件

請依照標準指示安裝語言套件擴充功能。 如需有關安裝擴充功能的詳細資訊，請參閱[擴充功能指南](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html)中的&#x200B;_一般CLI安裝_。

## 步驟2：建立該語言的存放區檢視

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**。

1. 按一下&#x200B;**[!UICONTROL Create Store View]**。

1. 設定新商店檢視的選項：

   - **[!UICONTROL Store]** — 選擇檢視的父級存放區。

   - **[!UICONTROL Name]** — 輸入存放區檢視的名稱。 例如：葡萄牙文。

     在存放區的標頭中，名稱出現在&#x200B;_語言選擇器_&#x200B;中。

   - **[!UICONTROL Code]** — 輸入小寫字元的程式碼以識別檢視。 例如： `portuguese`。

   - **[!UICONTROL Status]** — 若要啟用檢視，請設定為`Enabled`。

   - **[!UICONTROL Sort Order]** — （選擇性）輸入數字，以決定此檢視與其他檢視一起列出的順序。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Store View]**。

## 步驟3：變更存放區檢視的地區設定

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在&#x200B;**[!UICONTROL Scope]**&#x200B;下拉式清單中，選取要設定的存放區檢視，然後在提示時按一下&#x200B;**[!UICONTROL OK]**。

1. 在&#x200B;*[!UICONTROL General]*&#x200B;設定頁面上，展開![區段中的](../assets/icon-display-expand.png)擴充選取器&#x200B;**[!UICONTROL Locale Options]**。

1. 清除「**[!UICONTROL Use Website]**」核取方塊，並將&#x200B;**[!UICONTROL Locale]**&#x200B;設定為您要指派給檢視的語言。

   如果有多種語言可供使用，請務必選擇適合特定地區或方言的語言。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

   在您變更地區設定的語言之後，您建立的其餘內容，包括產品名稱和說明、類別、[CMS](../content-design/page-translate.md)頁面和區塊，必須針對每個商店檢視分別翻譯。

## 將產品本地化

如果您的商店有多種不同語言的檢視，則每種商店檢視都會提供相同的產品。 您可以使用相同的基本產品資訊，例如SKU、價格和存貨層次，無論語言為何。 然後，視需要只翻譯每種語言的產品名稱、說明欄位和中繼資料。

### 步驟1：翻譯產品欄位

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Products]**。

1. 在格線中，尋找要翻譯的產品，並以編輯模式開啟。

1. 在左上角，將&#x200B;**[!UICONTROL Store View]**&#x200B;設定為翻譯的檢視，並在提示確認時按一下&#x200B;**[!UICONTROL OK]**。

1. 針對要編輯的每個欄位，執行下列動作：

   - 取消選取欄位右側的&#x200B;**[!UICONTROL Use Default Value]**&#x200B;核取方塊。

   - 在欄位中貼上或輸入翻譯的文字。

   請確定翻譯所有文字欄位，包括[影像](../catalog/catalog-images-video.md)標籤和Alt文字、[搜尋引擎最佳化](../catalog/product-search-engine-optimization.md)欄位和任何[自訂選項](../catalog/settings-advanced-custom-options.md)資訊。

1. 完成時，按一下&#x200B;**[!UICONTROL Save]**。

### 步驟2：翻譯欄位標籤

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**。

1. 在清單中，找到要翻譯的屬性，並在編輯模式下開啟。

1. 在左側面板中選擇&#x200B;**[!UICONTROL Manage Labels]**。

1. 在&#x200B;_[!UICONTROL Manage Titles]_區段中，輸入每個商店檢視的轉譯標籤。

   ![輸入翻譯的標籤](./assets/product-attribute-labels-translate.png){width="600" zoomable="yes"}

1. 完成時，按一下&#x200B;**[!UICONTROL Save Attribute]**。

### 步驟3：翻譯所有類別

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Catalog]** > **類別**。

1. 在左上角，將&#x200B;**[!UICONTROL Store View]**&#x200B;設定為翻譯的檢視，並在提示確認時按一下&#x200B;**[!UICONTROL OK]**。

1. 在樹狀結構中，找到要轉譯的類別，並以編輯模式開啟。

1. 如需&#x200B;_基本資訊_，請翻譯&#x200B;**[!UICONTROL Category Name]**。

1. 展開![擴充選擇器](../assets/icon-display-expand.png) _[!UICONTROL Content]_區段並翻譯&#x200B;**[!UICONTROL Description]**。

1. 展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Search Engine Optimization Settings]**&#x200B;區段並翻譯下列欄位：

   - **[!UICONTROL Meta Title]**
   - **[!UICONTROL Meta Keywords]**
   - **[!UICONTROL Meta Description]**

1. 在&#x200B;_[!UICONTROL Search Engine Optimization Settings]_區段下，執行下列動作以翻譯&#x200B;**[!UICONTROL URL Key]**：

   - 清除欄位右側的&#x200B;**[!UICONTROL Use Default Value]**&#x200B;核取方塊。

   - 輸入翻譯的文字。

   - 確定已選取&#x200B;**[!UICONTROL Create Permanent Redirect for old URL]**&#x200B;核取方塊。

   ![翻譯URL索引鍵](./assets/category-translate-url-key.png)

1. 完成時，按一下&#x200B;**[!UICONTROL Save Category]**。

1. 對存放區中使用的所有類別重複此程式。

### 步驟4：翻譯產品屬性和屬性選項

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**。

1. 選取要翻譯的屬性。

1. 選擇左側的&#x200B;**[!UICONTROL Manage Labels]**&#x200B;並設定&#x200B;**[!UICONTROL Managed Titles]**&#x200B;選項以定義屬性標題轉換。

1. 選擇左側的&#x200B;**[!UICONTROL Properties]**，並在&#x200B;**[!UICONTROL Manage Options]**&#x200B;區段中輸入轉譯的屬性選項。

   ![管理選項](./assets/manage-option-tab.png){width="600" zoomable="yes"}

1. 完成時，按一下&#x200B;**[!UICONTROL Save Attribute]**。
