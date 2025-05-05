---
title: 客戶名稱和地址選項
description: 客戶名稱與地址選項會決定名稱與地址表單中包含哪些欄位。
exl-id: 28949cfc-2c96-4d0a-a35b-b37b3aa2d1e9
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '806'
ht-degree: 0%

---

# 客戶名稱和地址選項

_名稱和地址選項_&#x200B;決定當客戶在您的商店建立[帳戶](../customers/account-create.md)時，哪些欄位會包含在名稱和地址表單中。

![客戶帳戶登錄檔單](assets/storefront-customer-account-address-book.png){width="500" zoomable="yes"}

Adobe Commerce和Magento Open Source的名稱和位址選項設定步驟不同。

## 設定Adobe Commerce的名稱和位址選項

您可以設定在店面向客戶建立帳戶時顯示的名稱和地址選項。

### 步驟1：設定設定的範圍

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Customers]**&#x200B;並選擇&#x200B;**[!UICONTROL Customer Configuration]**。

1. 展開&#x200B;**[!UICONTROL Name and Address Options]**&#x200B;區段。

   >[!INFO]
   >
   >請注意，名稱和位址選項的範圍套用在`website`層級。

1. 向上捲動至頁面頂端，並將設定的範圍設定為下列其中一項：

   - `Default Config`
   - `Main Website` （或多站台安裝的特定站台）

   >[!INFO]
   >
   >當範圍設定為`Default Store View`時，_[!UICONTROL Name and Address Options]_&#x200B;區段沒有出現。

   ![設定範圍](assets/customer-configuration-scope-ee.png){width="700" zoomable="yes"}

### 步驟2：設定名稱和位址選項

1. 返回「客戶設定」頁面的&#x200B;[!UICONTROL _名稱和地址選項_]&#x200B;區段。

   >[!INFO]
   >
   > 如果您未使用`Default config`範圍設定，則必須先清除每個欄位的`Use Default`核取方塊，才能變更值。

   ![名稱和地址選項](../configuration-reference/customers/assets/customer-configuration-name-address-options-ee.png){width="600" zoomable="yes"}

1. 針對&#x200B;**[!UICONTROL Prefix Dropdown Options]**，輸入您要在清單中顯示的每個首碼，以分號分隔。

   >[!IMPORTANT]
   >
   >在第一個值前放置分號，在清單頂端顯示空白值。

1. 針對&#x200B;**[!UICONTROL Suffix Dropdown Options]**，輸入您要在清單中顯示的每個尾碼，以分號分隔。

1. 若要在客戶表單中包含下列欄位，請視需要將每個欄位的值設為`Optional`或`Required`。

   - **[!UICONTROL Show Telephone]**
   - **[!UICONTROL Show Company]**
   - **[!UICONTROL Show Fax]**

### 步驟3：儲存並重新整理

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

1. 在頁面頂端的訊息中，按一下&#x200B;**[!UICONTROL Cache Management]**&#x200B;和[重新整理](../systems/cache-management.md)每個無效的快取。

## 設定Magento Open Source的名稱和位址選項

設定當客戶建立帳戶時，在店面向客戶顯示的名稱和地址選項。

![客戶帳戶登錄檔單](assets/storefront-customer-account-signup.png){width="500" zoomable="yes"}

### 步驟1：設定設定的範圍

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Customers]**&#x200B;並選擇&#x200B;**[!UICONTROL Customer Configuration]**。

1. 展開&#x200B;**[!UICONTROL Name and Address Options]**&#x200B;區段。

   >[!IMPORTANT]
   >
   > 請注意，名稱和位址選項的範圍套用在`website`層級。

   ![名稱和地址選項](../configuration-reference/customers/assets/customer-configuration-name-address-options-ce.png){width="600" zoomable="yes"}

1. 向上捲動至頁面頂端，並將設定的範圍設定為下列其中一項：

   - `Default Config`
   - `Main Website` （或多站台安裝的特定站台）

   >[!NOTE]
   >
   >範圍設定為`Default Store View`時，_名稱和位址選項_&#x200B;區段不會出現。

   ![設定範圍](assets/configuration-scope.png){width="600" zoomable="yes"}

### 步驟2：設定名稱和位址選項

1. 返回「客戶設定」頁面的&#x200B;[!UICONTROL _名稱和地址選項_]&#x200B;區段。

   >[!INFO]
   >
   >如果您未使用`Default config`範圍設定，則必須先清除每個欄位的`Use Default`核取方塊，才能變更值。

1. 若是街道地址&#x200B;**中的**&#x200B;行數，請輸入從1到4的數字。

   >[!WARNING]
   >
   >依預設，街道地址是三行。

1. 若要在名稱中包含前置詞（例如Mr或Ms.），請將&#x200B;**顯示前置詞**&#x200B;設定為`Yes`。

   ![客戶登錄檔單中的前置詞](assets/storefront-customer-account-prefix.png){width="600" zoomable="yes"}

   >[!INFO]
   >
   >在&#x200B;**首碼下拉式清單選項**&#x200B;中，輸入您要在清單中顯示的每個首碼，並以分號分隔。 您可以在第一個值前面加上分號，在清單頂端顯示空白值。

1. 若要在客戶中間名或初始名稱中加入選用欄位，請將&#x200B;**[!UICONTROL Show Middle Name (initial)]**&#x200B;設為`Yes`。

1. 包含尾碼(例如Jr. 或Sr.)在客戶名稱后，將&#x200B;**[!UICONTROL Show Suffix]**&#x200B;設定為下列其中一項：

   - `Optional`
   - `Required`

   >[!INFO]
   >
   >在&#x200B;**尾碼下拉式清單選項**&#x200B;中，輸入您要在清單中顯示的每個尾碼，並以分號分隔。 您可以在第一個值前面加上分號，在清單頂端顯示空白值。

1. 若要包含出生日期，請將&#x200B;**[!UICONTROL Show Date of Birth]**&#x200B;設為下列其中一項：

   - `Optional`
   - `Required`

   >[!INFO]
   >
   >為了遵循目前的安全性和隱私權最佳實務，請注意任何與儲存客戶完整出生日期（月、日、年）和其他個人識別碼相關的潛在法律和安全風險。 建議您限制客戶完整出生日期的儲存量，並建議使用客戶出生年作為替代方法。

   客戶可使用欄位後面的「行事曆」圖示，從快顯行事曆中選擇出生日期。

   ![客戶登錄檔單中的出生日期](assets/storefront-customer-account-date-of-birth.png){width="600" zoomable="yes"}

1. 若要允許客戶輸入稅捐或[VAT](../stores-purchase/vat.md)編號，請將&#x200B;**[!UICONTROL Show Tax/VAT Number]**&#x200B;設定為下列其中一項：

   - `Optional`
   - `Required`

1. 若要在客戶表單中包含性別欄位，請將&#x200B;**[!UICONTROL Show Gender]**&#x200B;設為下列其中一項：

   - `Optional`
   - `Required`

   ![客戶登錄檔單中的性別選項](assets/storefront-customer-account-gender.png){width="600" zoomable="yes"}

1. 若要在客戶表單中包含下列欄位，請視需要將每個欄位的值設為`Optional`或`Required`。

   - **[!UICONTROL Show Telephone]**
   - **[!UICONTROL Show Company]**
   - **[!UICONTROL Show Fax]**

### 步驟3：儲存並重新整理

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

1. 在頁面頂端的訊息中，按一下&#x200B;**[!UICONTROL Cache Management]**&#x200B;和[重新整理](../systems/cache-management.md)每個無效的快取。
