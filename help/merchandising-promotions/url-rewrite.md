---
title: URL重新寫入
description: 瞭解URL重寫並使用Commerce URL重寫工具來變更與產品、類別或CMS頁面相關聯的URL。
exl-id: 91e65f7f-7e33-4da5-b0a1-538ace56328a
feature: Categories, Products, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 0%

---

# URL重新寫入

URL重寫工具可讓您變更與產品、類別或CMS頁面相關聯的任何URL。 當重寫生效時，任何指向先前URL的連結都會重新導向到新位址。

>[!NOTE]
>
>若要同時更新多個或所有產品的URL重寫，請參考[多個URL重寫](url-rewrite-product.md#multiple-url-rewrites)。

術語&#x200B;_rewrite_&#x200B;和&#x200B;_重新導向_&#x200B;通常可互換使用，但參考的流程稍有不同。 URL重寫會變更URL在瀏覽器中的顯示方式。 URL重新導向會更新儲存在伺服器上的URL。 URL重新導向可以是暫時的或永久的。 您的商店會使用URL重寫和重新導向，讓您輕鬆變更產品、類別或頁面的URL金鑰，並保留現有連結。

預設會針對您的商店啟用[自動URL重新導向](url-redirect-product-automatic.md)，並且在每個產品的URL索引鍵欄位下會選取&#x200B;**為舊URL建立永久重新導向**&#x200B;核取方塊。

{{url-rewrite-skip}}

{{url-rewrite-params}}

![搜尋引擎最佳化 — 建立永久性URL重新導向](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

## 標準URL

出於SEO目的，建議您每個網頁都只有一個不同的URL。

如果您有多個URL可存取單一頁面，或內容相似的不同頁面，Google會將這些頁面視為相同頁面的重複版本。 Google會選擇一個URL作為規範版本並進行編目，而其他所有URL都會被視為重複URL，且編目頻率較低。

Google如果您未明確指出哪個URL是標準網址，系統會為您做出選擇，或可能會將兩者視為同等權重。 這可能會導致不必要的行為，並存在編目預算無效和分散式反向連結不足的風險。

根據您設定網站的方式，索引中可能會有您網站的多個版本，包括：

    https://www.example.com
    https://www.example.com/
    http://www.example.com
    https://example.com
    https://www.example.com/index.html

若要指定標準頁面，請參閱[Google Search Central檔案](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls)。

## 設定URL重寫

啟用Web伺服器Apache Rewrites是初始Commerce設定的一部分。 Commerce會定期使用URL重寫來移除通常出現在URL根資料夾之後的檔案名稱`index.php`。 啟用Web伺服器重寫時，系統會重寫每個URL以省略`index.php`。 重寫作業會移除對搜尋引擎或客戶毫無價值的字詞，對效能或網站排名沒有影響。

不重寫網頁伺服器的URL

    http://www.yourdomain.com/magento/index.php/storeview/url-identifier

網頁伺服器重寫的URL

    http://www.yourdomain.com/magento/storeview/url-identifier

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在展開&#x200B;**[!UICONTROL General]**&#x200B;的左側面板中，選擇&#x200B;**[!UICONTROL Web]**。

1. 展開&#x200B;**[!UICONTROL Search Engine Optimization]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![一般設定 — Web搜尋引擎最佳化](../configuration-reference/general/assets/web-search-engine-optimization.png){width="600" zoomable="yes"}

1. 將&#x200B;**[!UICONTROL Use Web Server Rewrites]**&#x200B;設定為您的偏好設定。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

## 建立URL重寫

您可以使用URL重寫工具來建立產品和類別重寫，以及商店中任何頁面的自訂重寫。 當重寫生效時，任何指向先前URL的現有連結都會順暢地重新導向至新位址。

URL重寫可用來新增高值關鍵字，以改善搜尋引擎為產品編制索引的方式。 您也可以使用重寫，針對暫時性季節性變更或永久性變更建立其他URL。 可以為任何有效路徑（包括CMS內容頁面）建立重寫。 在內部，系統會一律透過ID參考產品和類別。 不論URL多久變更一次，ID都會保持不變。 以下是您可以使用URL重寫的一些方法：

系統URL

    http://www.example.com/catalog/category/id/6

原始URL

    http://www.example.com/peripherals/keyboard.html

重新導向的產品URL

    http://www.example.com/ergonomic-keyboard.html

其他類別URL

    http://www.example.com/all-on-sale.html
    http://www.example.com/save-now/spring-sale

![URL重寫格線](./assets/url-rewrites.png){width="700" zoomable="yes"}

Commerce提供下列URL重寫型別：

* [產品重寫](url-rewrite-product.md)
* [類別重寫](url-rewrite-category.md)
* [CMS頁面重寫](url-rewrite-cms-page.md)
* [自訂重寫](url-rewrite-custom.md)

## URL重寫示範

觀看此影片，瞭解如何管理URL重寫：

>[!VIDEO](https://video.tv.adobe.com/v/343751?quality=12&learn=on)
