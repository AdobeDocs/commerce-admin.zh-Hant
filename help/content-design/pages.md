---
title: 頁面
description: 深入瞭解隨附的核心內容頁面 [!DNL Commerce] 示範儲存，並變更預設頁面設定。
exl-id: 4be7d3d6-ce36-42bc-9224-4804c3211f16
feature: Page Content, Configuration
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '908'
ht-degree: 0%

---

# 頁面

內容可以透過其儲存期來檢視，就像商店中的任何產品一樣。 您知道社群媒體內容的儲存期少於24小時嗎？ 您建立之內容的潛在儲存期限可協助您決定要將資源投入到何處。

保質期長的內容有時稱為 _長青內容_. 歷久不衰的內容範例包括客戶成功案例、 _操作說明_ 指示和常見問答(FAQ)。 相反地，容易腐爛的內容包括事件、產業新聞和新聞稿。

![範例Luma存放區中包含的關於我們頁面 ](./assets/storefront-about-us.png){width="700" zoomable="yes"}

## 核心內容頁面

此 [!DNL Commerce] 示範存放區提供核心內容頁面的範例，可協助您開始使用。 您可以修改所有這些頁面以符合您的需求。 檢視您商店中的下列頁面，並確定內容傳達您的訊息、語音和品牌。

### 首頁

示範 [首頁](../getting-started/storefront.md#home-page) 頁面包含橫幅、影像輪播、數個含連結的靜態區塊，以及新產品清單。

### 隱私權原則

商店 [隱私權原則](../getting-started/privacy-policy.md) 頁面應使用您自己的資訊進行更新。 依據最佳做法的要求，您的隱私權政策應向您的客戶說明貴公司收集的資訊型別及其使用方式。

### 404找不到

404 Page Not Found頁面的名稱為找不到頁面時傳回的回應代碼。 URL重新導向可減少此頁面出現的次數。 不過，在必要時您也可以利用這個機會，提供一些客戶可能感興趣的產品連結。

### 存取遭拒

{{b2b-feature}}

此 [存取遭拒](../b2b/account-company-roles-permissions.md) 當指派給公司使用者的許可權禁止存取頁面時，就會顯示頁面。

### 啟用Cookie

此 [啟用Cookie](../getting-started/compliance-cookie-law.md) 當您的網站訪客的瀏覽器未啟用Cookie時，畫面就會顯示。 此頁面提供逐步說明，說明如何為最熱門的瀏覽器啟用Cookie。

### 服務無法使用

此 [503服務無法使用](../configuration-reference/general/general.md) 頁面是以伺服器無法使用時傳回的回應代碼命名。

### 關於我們

「關於我們」頁面是從商店的頁尾連結。 您可以包括影像、影片、新聞稿與公告連結。 範例頁面右側有一個影像，以及一個裝飾性影像，用於指出頁面的結尾。

### 客戶服務

「客戶服務」頁面是頁面階層中的另一個節點。 頁面上的兩個標頭包含的內容，只有在客戶按一下標頭時才會顯示。

![店面的客戶服務頁面](./assets/storefront-customer-service.png){width="700" zoomable="yes"}

## 設定預設頁面

此 _預設頁面_ 設定會決定與關聯的登入頁面 [基礎URL](../stores-purchase/store-urls.md) 和對應的首頁。 它也會決定當頁面顯示 _找不到頁面_ 發生錯誤，並且 [階層連結路徑](../catalog/navigation-breadcrumb-trail.md) 會顯示在每個頁面的頂端。

1. 在 _管理員_ 側欄，前往  **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中的 _[!UICONTROL General]_，選擇&#x200B;**[!UICONTROL Web]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Default Pages]** 區段。

   ![預設頁面](./assets/web-default-pages.png){width="500" zoomable="yes"}

   | 欄位 | [範圍](../getting-started/websites-stores-views.md#scope-settings) | 說明 |
   |--- |--- |--- |
   | [!UICONTROL Default Web URL] | 存放區檢視 | 表示與基底URL關聯的登入頁面。 依預設，此欄位設為 `cms` 以指示頁面 [!DNL Commerce] 內容管理系統。 您也可以使用不同型別的登陸頁面，例如部落格。 例如，若在伺服器上安裝部落格，則位在 `magento/blog`，您可以輸入資料夾名稱 `blog` 作為選取頁面的相對路徑。 |
   | [!UICONTROL CMS Home Page] | 存放區檢視 | 若要選擇商店的首頁，只要從清單中選取CMS頁面即可。 依照預設，「CMS首頁」會列出商店可用的完整CMS頁面選項。 |
   | [!UICONTROL Default No-route URL] | 存放區檢視 | 包含您要在預設頁面URL `404 Page not Found` 發生錯誤。 預設值為 `cms/noroute/index`. |
   | [!UICONTROL CMS No Route Page] | 存放區檢視 | 識別您要在發生「404找不到頁面」錯誤時顯示的特定CMS頁面。 預設頁面為 `404 Not Found`. |
   | [!UICONTROL CMS No Cookies Page] | 存放區檢視 | 識別未針對瀏覽器啟用Cookie時所顯示的特定CMS頁面。 本頁面說明為何使用Cookie，以及如何為每個瀏覽器啟用。 預設頁面為 `Enable Cookies`. |
   | [!UICONTROL Show Breadcrumbs for CMS Pages] | 存放區檢視 | 決定階層連結軌跡是否出現在目錄中的所有CMS頁面上。 選項： `Yes` / `No` |

   {style="table-layout:auto"}

1. 的 **[!UICONTROL Default Web URL]**，請在以下位置輸入資料夾的相對路徑： [!DNL Commerce] 包含登入頁面的安裝。

   預設設定， `cms`，表示頁面來自 [!DNL Commerce] 內容管理系統。

   >[!NOTE]
   >
   >針對特定商店檢視，請清除 **[!UICONTROL Use Default]** 核取方塊旁的 _[!UICONTROL Default Web URL]_，以及任何其他要變更的預設設定。

1. 設定 **[!UICONTROL CMS Home Page]** CMS頁面做為首頁。 其他建立的頁面則可作為首頁使用，例如：

   - 歡迎使用專屬線上商店
   - 獎勵點數
   - 關於我們
   - 客戶服務
   - 啟用Cookie
   - 隱私權原則
   - 公司：存取遭拒

1. 的 **[!UICONTROL Default No-route URL]**，請在以下位置輸入資料夾的相對路徑： [!DNL Commerce] 安裝，頁面在下列情況下會重新導向： _404找不到頁面_ 發生錯誤。

   預設值為 `cms/index/noRoute`.

1. 設定 **[!UICONTROL CMS No Route Page]** 移至發生下列情況時顯示的CMS頁面： _404找不到頁面_ 發生錯誤。

1. 設定 **[!UICONTROL CMS No Cookies Page]** 移至瀏覽器中停用Cookie時顯示的CMS頁面。 本頁面說明為何使用Cookie，以及如何為每個瀏覽器啟用。 預設頁面為 `Enable Cookies`.

1. 如果您希望階層連結軌跡出現在所有CMS頁面的頂端，請設定 **[!UICONTROL Show Breadcrumbs for CMS Pages]** 至 `Yes`.

1. 完成後，按一下 **[!UICONTROL Save Config]**.
