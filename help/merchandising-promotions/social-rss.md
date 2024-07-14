---
title: 社群媒體和RSS摘要
description: 瞭解如何新增社群媒體和其他RSS摘要整合，以建立品牌和產品知名度。
exl-id: e4a48870-f53e-4848-8faa-8f2aedaf53b7
feature: Merchandising, Communications
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1162'
ht-degree: 0%

---

# 社群媒體和RSS摘要

許多商家使用社群媒體和其他數位工具來建立品牌和產品知名度。 您可以安裝Marketplace擴充功能或新增外掛程式至內容頁面，將商店與社交網路整合。 使用RSS摘要將您的產品資訊發佈到購物彙總網站，甚至將其包含在您的電子報中。 客戶可以訂閱您的RSS摘要，瞭解新產品和促銷活動。

## 社交網路

您可以安裝[Marketplace擴充功能](../getting-started/commerce-marketplace.md)，將您的商店連線至社交網路。 此外，您可以輕鬆地將社交外掛程式（例如&#x200B;_Like_&#x200B;按鈕）新增至CMS區塊，這些區塊可整合至您整個商店的頁面中。

社交網站有許多外掛程式，可以輕鬆新增到您的商店。 此外，Commerce Marketplace上有許多擴充功能可用來將您的商店與社群媒體整合。 下列範例說明如何將Facebook _Like_&#x200B;按鈕新增至您的商店。

>[!NOTE]
>
>Adobe Commerce已移除原生&#x200B;_Magento社交_ Facebook整合，不再支援此擴充功能。 前往[Commerce Marketplace](https://marketplace.magento.com/catalogsearch/result/?q=Facebook){：target=&quot;_blank&quot;}，尋找Facebook整合的替代擴充功能。

### 步驟1. 取得按鈕程式碼

1. 在中繼開發人員網站上，前往[按鈕設定](https://developers.facebook.com/docs/plugins/like-button)頁面。

1. 針對&#x200B;**[!UICONTROL URL to Like]**，輸入您商店中您希望人們&#x200B;_喜歡_&#x200B;之頁面的URL。

   例如，您可以輸入商店首頁的URL。

1. 選擇按鈕的&#x200B;**[!UICONTROL Layout]**。

1. 輸入您的網站上可用於按鈕及任何關聯文字訊息的&#x200B;**[!UICONTROL Width]**&#x200B;畫素。

1. 將&#x200B;**[!UICONTROL Action Type]**&#x200B;設定為下列其中一項：

   - `Like`
   - `Recommend`

1. 按一下&#x200B;**[!UICONTROL Get Code]**&#x200B;將產生的程式碼複製到剪貼簿。

### 步驟2. 建立內容區塊

1. 返回您的商店管理員。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**。

1. 按一下右上角的&#x200B;**[!UICONTROL Add New Block]**。

1. 輸入描述性&#x200B;**[!UICONTROL Block Title]**&#x200B;以供內部參考。

   例如： `Facebook Like Button`。

1. 使用所有小寫字元和底線而非空格將唯一&#x200B;**[!UICONTROL Identifier]**&#x200B;指派給區塊。

   例如： `facebook_like_button`。

1. 如果您的Commerce執行個體有多個存放區檢視，請選擇讓區塊可用的每個&#x200B;**[!UICONTROL Store View]**。

1. 視您的內容工具而定，將程式碼片段新增至區塊內容：

   - 使用[!DNL Page Builder]時，將[HTML程式碼](../page-builder/html-code.md)區塊新增至舞台，並貼上您從Facebook網站複製的程式碼片段。 否則，請將程式碼片段貼到&#x200B;**[!UICONTROL Content]**&#x200B;方塊中。

   - 使用編輯器將您從Facebook網站複製的程式碼片段貼到&#x200B;**[!UICONTROL Content]**&#x200B;方塊中。

1. 如果區塊尚未準備好上線，請將&#x200B;**[!UICONTROL Enable Block]**&#x200B;設定為`No`。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Block]**。

### 步驟3. 放置區塊

1. 根據您的內容工具新增區塊：

   - 使用[!UICONTROL Page Builder]時，請依照指示[將區塊](../page-builder/block.md)新增到階段。

   - 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**。

1. 按一下右上角的&#x200B;**[!UICONTROL Add Widget]**&#x200B;並執行下列動作：

   - 在&#x200B;_設定_&#x200B;區段中，![Adobe Commerce B2B](../assets/b2b.svg) (僅適用於Adobe Commerce B2B)，將&#x200B;**[!UICONTROL Type]**&#x200B;設為`CMS Static Block`，然後按一下&#x200B;**[!UICONTROL Continue]**。

   - 確認&#x200B;**[!UICONTROL Design Theme]**&#x200B;已設定為目前主題。

   - 按一下&#x200B;**[!UICONTROL Continue]**。

1. 在&#x200B;**[!UICONTROL Storefront Properties]**&#x200B;區段中，執行下列動作：

   - 針對&#x200B;**[!UICONTROL Widget Title]**，輸入內部參考的標題。

   - 將&#x200B;**[!UICONTROL Assign to Store Views]**&#x200B;設為`All Store Views`，或設為您想要讓應用程式可用的檢視。 若要選取多個檢視，請按住Ctrl鍵(PC)或Command鍵(Mac)並按一下每個選項。

   - 在&#x200B;**[!UICONTROL Sort Order]**&#x200B;欄位中輸入數字，以決定區塊順序（如果指派給該區塊，使其出現在頁面上與其他內容元素相同的位置）。 頂端位置是零。

1. 在&#x200B;_[!UICONTROL Layout Updates]_區段中，按一下&#x200B;**[!UICONTROL Add Layout Update]**並將&#x200B;**[!UICONTROL Display On]**設定為您要顯示區塊的類別、產品或頁面。

   例如，如果您選擇`All Pages`，並將區塊放置在頁首或頁尾中，區塊會出現在商店每個頁面的相同位置。

   若要將區塊放置在特定頁面上，請執行下列動作：

   - 將&#x200B;**[!UICONTROL Display On]**&#x200B;設為`Specified Page`，並選取您要區塊出現的&#x200B;**[!UICONTROL Page]**。

   - 選擇&#x200B;**[!UICONTROL Block Reference]**&#x200B;以識別頁面上要放置區塊的位置。

   - 接受&#x200B;**[!UICONTROL Template]**&#x200B;的預設設定，此設定設為`CMS Static Block Default Template`。

   - 按一下&#x200B;**[!UICONTROL Save and Continue Edit]**。

1. 在左側的面板中，選擇&#x200B;**[!UICONTROL Widget Options]**。

1. 按一下&#x200B;**[!UICONTROL Select Block…]**&#x200B;並選擇要放置的區塊。

1. 完成時，按一下&#x200B;**[!UICONTROL Save]**。

1. 出現提示時，請依照工作區頂端的指示，更新索引和頁面快取。

   Widget現在出現在&#x200B;_[!UICONTROL Widgets]_清單中。

### 步驟4. 驗證在存放區中的位置

返回您的店面，確認區塊位於正確位置。 若要移動區塊，您可以重新開啟Widget，嘗試不同的頁面或區塊參照。

## RSS摘要

RSS (Really Simple Syndication)是一種以XML為基礎的資料格式，用於線上散發資訊。 您的客戶可以訂閱您的RSS摘要，以瞭解有關新產品和促銷活動的資訊。 RSS摘要也可用來將您的產品資訊發佈到購物彙總網站，並包含在電子報中。

啟用RSS摘要時，產品、特殊優惠、類別和優惠券的任何新增內容都會自動傳送給每個摘要的訂閱者。 您發佈的所有RSS摘要連結位於商店頁尾。

![RSS摘要圖示](./assets/icon-rss.png){width="100"}<br/>

讀取RSS摘要所需的軟體稱為摘要讀取器，可讓使用者訂閱標題、部落格、播客等。 GoogleReader是眾多線上免費提供的摘要閱讀程式之一。

![店面範例 — RSS摘要](./assets/storefront-rss-feeds.png){width="700" zoomable="yes"}

### 設定RSS摘要的優點

- 從您的商店或部落格下載最新更新
- 淺色廣告
- 普通股
- 提升SEO
- 增加銷售額

### RSS摘要型別

| RSS摘要 | 說明 |
|--- |--- |
| [!UICONTROL Wish List] | 啟用時，RSS摘要連結會出現在客戶希望清單頁面的頂端。 此外，希望清單共用頁面包含一個核取方塊，可讓您包含共用希望清單之摘要的連結。 |
| [!UICONTROL New Products] | 發佈新增至目錄之新產品的通知。 |
| [!UICONTROL Special Products] | 發佈任何具有特殊定價之產品的通知。 |
| [!UICONTROL Coupons / Discounts] | 發佈商店內任何特殊優惠券或折扣的通知。 |
| [!UICONTROL Top Level Category] | 發佈目錄之最上層類別結構變更的通知，這會反映在主功能表中。 |
| [!UICONTROL Customer Order Status] | 讓客戶能透過RSS摘要追蹤其訂單狀態。 啟用時，訂單上會顯示RSS摘要連結。 |

{style="table-layout:auto"}

### 為您的商店設定RSS摘要

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在右上角，將&#x200B;**[!UICONTROL Store View]**&#x200B;設定為可使用摘要的檢視。

   如果提示您確認，請按一下&#x200B;**[!UICONTROL OK]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Catalog]**&#x200B;並選擇&#x200B;**[!UICONTROL RSS Feeds]**。

1. 展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Rss Config]**&#x200B;區段，並將&#x200B;**[!UICONTROL Enable RSS]**&#x200B;設為`Enable`。

   ![目錄組態 — RSS摘要](../configuration-reference/catalog/assets/rss-feeds-rss-config.png){width="600" zoomable="yes"}

   如有必要，請清除&#x200B;**[!UICONTROL Use Default]**&#x200B;核取方塊以變更預設值。

1. 展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Wish List]**&#x200B;區段，並將&#x200B;**[!UICONTROL Enable RSS]**&#x200B;設為`Enable`。

1. 展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Catalog]**&#x200B;區段，並視需要設定其他摘要為`Enable`。

   - **[!UICONTROL New Products]**
   - **[!UICONTROL Special Products]**
   - **[!UICONTROL Coupons/Discounts]**
   - **[!UICONTROL Top Level Category]**

   ![目錄 — RSS摘要設定](../configuration-reference/catalog/assets/rss-feeds-catalog.png){width="600" zoomable="yes"}

1. 展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Order]**&#x200B;區段，並將&#x200B;**[!UICONTROL Customer Order Status Notification]**&#x200B;設為`Enable`。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

1. 檢視店面上的結果，頁面URL結尾有`/rss`。

