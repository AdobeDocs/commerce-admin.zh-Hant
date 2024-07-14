---
title: 標籤標籤
description: 瞭解包含程式碼片段的標籤標籤，這些片段會參照您商店中的物件。
exl-id: 0d6f5a9b-983d-473e-b641-0dceba40974f
feature: Page Content, Communications, Variables
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 0%

---

# 標籤標籤

標籤標籤是包含程式碼片段的指令，與存放區中物件的相對參照，例如變數、URL、影像或區塊。 標籤標籤標籤可用於任何有編輯器可用的地方，並可合併到[電子郵件](email-templates.md)和[電子報](../merchandising-promotions/newsletter-template.md)範本以及其他型別的[內容](../content-design/introduction.md#content)的HTML中。

標籤標籤會以雙大括弧括住，並可由Widget工具產生，或直接在HTML內容中輸入。 例如，與其將頁面的完整路徑硬式編碼，您可以使用標籤標籤來表示商店URL。 以下範例中的標籤標籤包括：

{{$include /help/_includes/directives-caution.md}}

## 自訂變數

變數標籤標籤可用來將[自訂變數](variables-custom.md)插入電子郵件範本、區塊、電子報和內容頁面。

\{\{CustomVar code= &quot;my_custom_variable&quot;}}

## 商店URL

「商店URL」標籤代表您網站的基底URL，可用來取代完整URL的第一部分，包括網域名稱。 此標籤標籤有兩個版本：一個直接前往您的商店，另一個在結尾使用正斜線(`/`)，用於新增路徑。

\{\{商店url=&#39;服飾/鞋子/女士&#39;}}

## 媒體URL

Dynamic Media URL標籤代表儲存在內容傳遞網路(CDN)上之影像的位置和檔案名稱。 標籤可用來將影像放置在頁面、區塊、橫幅或電子郵件範本上。

\{\{media url=&#39;shoe-sale.jpg&#39;}}

## 區塊ID

「區塊ID」標籤是最容易使用的標籤之一，可用來將區塊直接放置在CMS頁面上，或甚至巢狀放置在其他區塊內。 您可以使用此技巧來修改不同促銷活動或語言的區塊。 區塊ID標籤標籤會透過區塊的識別碼來參考區塊。

\{\{區塊id=&#39;block-id&#39;}}

## 範本標籤

範本標籤會參照PHTML範本檔案，並可用來在CMS頁面上或靜態區塊上顯示區塊。 可將下列範例中的程式碼新增至頁面或區塊，以顯示「聯絡我們」表單。

\{\{block class=&quot;Magento\Contact\Block\ContactForm&quot; name=&quot;contactForm&quot; template=&quot;Magento_連絡人：：form.phtml&quot;}}

可將下一個範例中的程式碼新增至頁面或區塊，依類別ID顯示特定類別中的產品清單。

\{\{block type=&quot;catalog/product_list&quot; category_id=&quot;22&quot; template=&quot;catalog/product/list.phtml&quot;}}

## Widget程式碼

Widget工具可用來根據產品ID顯示產品清單，或插入複雜的連結，例如前往特定產品頁面的連結。 產生的程式碼包括區塊參考、程式碼模組的位置和對應的PHTML範本。 產生程式碼後，您可以將其從一個位置複製並貼到另一個位置。

可將下列範例中的程式碼新增至頁面或區塊，以顯示新產品清單。

\{\{widget type=&quot;catalog/product_widget_new&quot; display_type=&quot;new_products&quot; products_count=&quot;10&quot; template=&quot;catalog/product/widget/new/content/new_grid.phtml&quot;}}

下一個範例中的程式碼可新增至頁面或區塊，依產品ID顯示特定產品的連結。

\{\{widget type=&quot;catalog/product_widget_link&quot; anchor_text=&quot;我的產品連結&quot; title=&quot;我的產品連結&quot; template=&quot;catalog/product/widgetlink/link_block.phtml&quot; id_path=&quot;product/31&quot;}}

## 在連結中使用標籤標籤

您可以將標籤標籤與HTML錨點標籤搭配使用，並直接連結至商店中的任何頁面。 此連結可合併至內容頁面、區塊或電子郵件與電子報範本中。 您也可以使用此技巧將影像連結至特定頁面。

### 步驟1. 識別目的地URL

如果可能的話，請導覽至您要連結的頁面，並從瀏覽器的位址列複製完整的URL。 您需要的部分URL出現在`.com/`之後。 否則，請從您要作為連結目的地的CMS頁面複製URL金鑰。

#### 類別頁面的完整URL

`https://mystore.com/apparel/shoes/womens`
`https://mystore.com/apparel/shoes/womens.html`

#### 產品頁面的完整URL

`https://mystore.com/apparel/shoes/womens/nine-west-pump`
`https://mystore.com/apparel/shoes/womens/nine-west-pump.html`

#### CMS頁面的完整URL

`https://mystore.com/about-us`

### 步驟2. 將標籤新增至URL

商店URL標籤代表您網站的基本URL，可用來取代商店URL的HTTP位址部分，包括網域名稱和`.com`。 根據您要達到的結果，您可以使用標籤的兩個版本。

`store direct_url` — 直接連結至頁面。

`store url` — 在結尾處加上正斜線，以便附加其他參照作為路徑。

在下列範例中，URL索引鍵會以單引號括住，而整個標籤標籤會以雙大括弧括住。 搭配錨點標籤使用時，標籤標籤會放置在錨點的雙引號內。 為避免混淆，您可以對每個巢狀引號集使用單引號與雙引號。

如果您以完整URL開頭，請刪除URL的HTTP位址（`http://`或`https://`）部分，一直到並包括`.com/`。 在其位置，透過開頭單引號輸入Store URL標籤標籤。

#### 儲存URL標籤標籤

`https://mystore.com/apparel/shoes/womens`

`{{store url='apparel/shoes/womens'}}`

否則，請輸入「商店URL」標籤的第一部分，並貼上您先前複製的URL金鑰或路徑。

### 使用URL金鑰儲存URL標籤標籤

`{{store url=`

若要完成標示標籤，請輸入右雙引號和雙大括弧。

`{{store url='apparel/shoes/womens'}}`

### 步驟3. 完成錨點標籤

使用標籤標籤（而非目標URL），將完成的標籤標籤包裝在錨點標籤內。 然後，新增連結文字並關閉錨點標籤。

#### 錨點標籤中的標籤

\&lt;a href=&quot;\{\{標籤移至此處}}&quot;>連結文字\&lt;/a>

將完成的錨點標籤貼到您要顯示連結的任何CMS頁面、區塊、橫幅或電子郵件範本的程式碼中。

### 使用標籤完成連結

\&lt;a href=&quot;\{\{商店url=&#39;apparel/shoes&#39;}}&quot;>鞋類促銷\&lt;/a>
