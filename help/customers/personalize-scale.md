---
title: 大規模建立引人入勝的個人化體驗
description: 瞭解Adobe [!DNL Commerce] 中的哪些功能可讓您為購物者建立個人化體驗。
feature: Customers, Storefront, Personalization
exl-id: 9546e1b8-796b-4694-8396-773a2b0e9c12
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '1808'
ht-degree: 0%

---

# 大規模建立引人入勝的個人化體驗

Adobe [!DNL Commerce]提供強大的工具組，可個人化每個客戶接觸點，進而提高購物者的參與度、轉換率和營收。

在本文章中，您將瞭解：

- 什麼是個人化？
- 我需要哪些資料才能實現個人化？
- Adobe [!DNL Commerce]如何解鎖個人化？
- 可用的個人化使用案例

## 什麼是個人化？

Personalization是指量身打造每位客戶購買體驗的各個層面，以符合其獨特的需求、情境和偏好設定。 Personalization不僅限於網站內容，或建議最適合的產品，而是涵蓋客戶歷程中的所有接觸點，包括：

- **行銷活動和通訊** — 透過行銷活動和通訊提供相關且一致的訊息
- **產品探索** — 在適當的時間向適當的客戶顯示適當的產品
- **促銷活動和優惠方案** — 鎖定目標促銷活動和優惠方案，以促使每位客戶轉換
- **內容體驗** — 量身打造網站內容，讓每位客戶及其歷程產生超相關感

![Personalization型別](assets/types-personalization.png){width="700" zoomable="yes"}

雖然這些型別的個人化體驗似乎對於一小部分客戶來說是可以實現的，但對於每個接觸點和管道中的數千或數百萬客戶來說，大規模個人化是無法做到的，所有即時體驗都讓人感覺是不可能的。 在以下章節中，您將瞭解Adobe [!DNL Commerce]和Adobe Experience Cloud如何提供協助。

## 我需要哪些資料才能實現個人化？

有效的個人化需要提供客戶相關資訊的內容或訊號，這些資訊可用於修改客戶體驗。 下表提供各種資料型別，以及Adobe [!DNL Commerce]在支援收集和啟用該資料方面所扮演的角色。

| 資料型別 | 店面資料（行為事件） | 後台資料（伺服器端事件） | 客戶設定檔和區段資料 |
|---|---|---|---|
| **定義** | 客戶在您網站上採取的點按或動作。 | 生命週期相關資訊和每個訂單（過去和目前）的詳細資訊。 | 您的購物者是誰，以及他們符合哪些區段的資格。 |
| 由Adobe Commerce擷取的&#x200B;**個事件** | [pageView](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#pageview)<br>[productPageView](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events)<br>[searchRequestSent](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#searchrequestsent)<br>[searchResponseReceived](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#searchresponsereceived)<br>[addToCart](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#addtocart)<br>[openCart](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#opencart)<br>[signIn](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#signin)<br>[登出](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#signout)<br>[startCheckout](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#startcheckout)<br>[completeCheckout](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#completecheckout)<br>[createRequisitionList](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#createrequisitionlist)<br>[AddList{addAddList toRequisitionList](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#addtorequisitionlist)<br>[removeFromRequisitionList](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#removefromrequisitionlist) | **訂單狀態**：<br>[訂單已訂購](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice#orderplaced)<br>[訂單專案已傳回起始專案](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice#orderitemsreturnedinitiated)<br>[訂單專案已出貨](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice#orderitemsshipped)<br>[訂單已取消](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice#ordercancelled)<br>[**訂單歷史記錄**](https://experienceleague.adobe.com/en/docs/commerce/data-connection/fundamentals/connect-data#send-historical-order-data)：<br>- SKU、名稱、價格數量、折扣<br> — 產品類別<br> — 付款金額、型別、貨幣<br> — 送貨方式與金額<br> — 退款識別碼、金額、金額、金額貨幣<br> — 返回原因、條件、解析度<br> — 地址<br> — 電子郵件 | [**個人資料記錄**](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-profilerecord)： （姓名、性別、地址、忠誠度狀態、電話號碼、電子郵件地址）<br>**帳戶狀態**：<br>[已建立帳戶](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice#accountcreated)<br>[已更新帳戶](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice#accountupdated)<br>[已刪除帳戶](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice#accountdeleted) |

有了這些豐富的第一方[!DNL Commerce]資料，您就可以鎖定目標並個人化每位購物者的體驗。 在下一節中，您將瞭解[!DNL Commerce]和Adobe Experience Cloud如何協助您建立個人化體驗，以及您可以啟用的使用案例。

## Adobe [!DNL Commerce]如何啟用個人化？

Adobe [!DNL Commerce]資料共用可讓您收集上表中的資料型別，並將其與其他Adobe Experience Cloud產品共用，以強化統一的客戶設定檔和對象、個人化行銷活動，以及豐富的分析和見解。

![資料如何流向Experience Platform Edge](assets/commerce-edge.png){width="700" zoomable="yes"}

Adobe [!DNL Commerce]資料共用包含兩個主要元件：

1. [資料連線](https://experienceleague.adobe.com/en/docs/commerce/data-connection/overview)：將店面、後台和客戶設定檔資料從Adobe [!DNL Commerce]共用至Adobe Experience Platform邊緣網路，以便在Adobe Experience Cloud應用程式中使用，包括：

   - [Adobe [!DNL Real-Time CDP]](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/intro/rtcdp-intro/overview)：將跨來源(ERP、CRM、POS)的客戶資料拼接至統一的設定檔，並建立規則型或AI型區段。
   - [Adobe [!DNL Journey Optimizer]](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/get-started)：啟動個人化的全頻道歷程，包括電子郵件行銷活動、簡訊、推播通知等。
   - [Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview)和[Adobe [!DNL Analytics]](https://experienceleague.adobe.com/en/docs/analytics/analyze/admin-overview/analytics-overview)：深入瞭解客戶和業務。
   - [Adobe [!DNL Target]](https://experienceleague.adobe.com/en/docs/target/using/introduction/intro)：測試並最佳化內容、建議的產品、優惠方案、導覽等。

1. [[!DNL Audience Activation]](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation)：使用[!DNL Real-Time CDP]對象個人化Adobe [!DNL Commerce]網站上的動態內容區塊、促銷活動及相關產品規則。

### 大規模個人化任何管道的店面體驗

Adobe [!DNL Commerce]可善用名為[Edge Delivery Services](https://experienceleague.adobe.com/developer/commerce/storefront/)的高效能店面，跨所有管道提供個人化體驗，以AI功能為核心，以速度為基礎。

透過Edge Delivery Services，您可以：

- **製作個人化內容**：使用檔案式製作、原生實驗以及Generative AI文字和影像變化，以大規模個人化體驗。 使用Assets和Generative AI內容建立可大規模產生產品和行銷影像。

- **產生變化**：允許內容作者使用Generative AI建立大量個人化AI驅動的[文字內容和影像變化](https://experienceleague.adobe.com/en/docs/experience-manager-learn/sites/generative-ai/generate-variations)與Adobe Firefly。

- **透過Edge Delivery Services Storefront部署**：Edge上的內容以及由插入式元件支援的Commerce功能，可為您的受眾建立客製化可購物體驗。

- **Commerce和Adobe Experience Manager Assets**： Generative AI產品資產建立和大規模變化。 建立、傳遞及監控任何通道的內容傳遞。

![下拉式清單：產品詳細資料頁面](assets/drop-in.png){width="700" zoomable="yes"}

### 現成可用的Personalization：開始使用原生Adobe [!DNL Commerce]功能

Adobe [!DNL Commerce]透過其原生現成可用的功能，提供強大的個人化功能。 下表說明您可以立即啟用的[!DNL Commerce]功能，以開始您的個人化歷程。

| 類別 | 功能 |
|---|---|
| 個人化產品探索 | [[!DNL Live Search]](https://experienceleague.adobe.com/en/docs/commerce/live-search/overview)：根據購物者的站上行為動作和與AI支援的搜尋的相似性來個人化和最佳化搜尋結果。<br>[智慧型類別銷售](https://experienceleague.adobe.com/en/docs/commerce/live-search/live-search-admin/category-merch)：根據購物者網站上的行為動作和相似性在類別頁面上進行AI驅動的產品排名。<br>[產品建議](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/guide-overview)：根據購物者的行為、趨勢和喜好性，提供AI支援的產品建議。<br>[相關產品規則](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules)：定義自訂規則，以顯示目錄中的產品，以推動交叉銷售和向上銷售。 |
| 個人化網站內容 | [動態內容區塊](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks)：根據Adobe Commerce中的客戶區段顯示個人化內容區塊，例如橫幅。 |
| 個人化優惠和促銷 | [購物車價格規則](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart)：根據一組條件(包括Adobe [!DNL Commerce]中的客戶區段)，將折扣套用至購物車中的專案。 |
| Insights and Measurement | [Adobe [!DNL Commerce] Intelligence](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started)：瞭解您的個人化策略如何隨著時間運作和改善。 |

## 熱門個人化使用案例

Adobe [!DNL Commerce]客戶正使用現成可用的功能，並將資料共用至Adobe Experience Cloud以用於各種使用案例。 以下章節重點說明最常用的使用案例，並說明如何使用Adobe [!DNL Commerce] Only或[!DNL Commerce]加上Experience Cloud應用程式來實作這些案例。

### 個人化的行銷活動和通訊

| 使用案例 | 解決方案 |
|---|---|
| **放棄的購物車和瀏覽** — 當客戶在展示高參與度後放棄購物車或瀏覽工作階段時，提供個人化的重新參與電子郵件或通知 | **僅Adobe [!DNL Commerce]**：<br>[電子郵件提醒](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/communications/email-reminders/email-reminder-rules)<br>**具有Adobe Journey Optimizer**：<br>[!DNL Commerce]資料的Adobe [!DNL Commerce]會作為全頻道放棄歷程的觸發因子。 根據客戶屬性、客戶放棄的專案、其他購物行為和過去的購買，個人化該歷程。<br>使用Adobe Journey Optimizer和Real-Time CDP的Commerce：根據統一的客戶設定檔和集中管理的對象量身打造放棄行銷活動，例如建立高放棄率的對象。 |
| **集中式對象建立** — 根據現場行為、過去購買、設定檔屬性、類別相關性、忠誠度狀態、客戶價值等，建立規則型或AI支援的對象 | **僅限Adobe [!DNL Commerce]**：<br>當[!DNL Commerce]客戶建立帳戶時，收集客戶設定檔資訊。 建立規則型[客戶區段](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/segments/customer-segments)和客戶群組，以個人化內容和促銷活動。<br>**Adobe [!DNL Commerce]搭配Adobe Real-Time CDP**：<br> 來自不同資料來源和管道的[統一設定檔](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/home)；規則型或AI支援的對象。 |
| **根據購物者行為的個人化電子郵件/簡訊優惠** — 根據過去的購買和購物者行為，透過目標電子郵件傳送個人化優惠給客戶，例如，傳送客戶已檢視或參與的產品或類別的優惠。 | **僅限Adobe [!DNL Commerce]**：<br>匯出資料以搭配行銷自動化解決方案使用。具有Adobe Journey Optimizer和Real-Time CDP的&#x200B;<br>**Adobe [!DNL Commerce]**：<br>[!DNL Commerce]資料會做為電子郵件或簡訊優惠方案的觸發條件，並提供訊號（購物者行為）以供根據進行個人化。 Real-Time CDP不是必要專案，但一般而言，這些優惠方案和行銷活動是圍繞對象建立的，且會在Real-Time CDP中建立和管理。 |
| **交叉或向上銷售相容的產品/品牌** — 如果客戶購買了一個相容的產品或品牌，或表示與其他產品或品牌高度相似，請傳送行銷活動（電子郵件/簡訊）以推動交叉銷售轉換。 | **僅限Adobe [!DNL Commerce]**：<br>使用Adobe [!DNL Commerce] [產品建議](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/guide-overview)來建議網站上的特定產品。 您也可以使用[相關產品規則](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules)來建議其他產品。具有&#x200B;[!DNL Target]**：<br>Adobe [!DNL Target]的<br>**[!DNL Commerce]也有內建的產品推薦引擎，具有強大的功能，例如類別相關性。 這可用於交叉或向上銷售。使用Adobe Journey Optimizer的<br>**[!DNL Commerce]**：<br>使用[!DNL Target]或[!DNL Commerce]決定要推薦的產品，然後透過Adobe Journey Optimizer傳遞。 |

### 個人化的網站體驗

| 使用案例 | 解決方案 |
|---|---|
| **個人化網站內容** — 根據購物者動作（例如產品瀏覽和類別相關性），個人化網站橫幅和其他頁面內容。 根據A/B測試的結果或業務目標部署最適合的內容。 | **僅限Adobe [!DNL Commerce]**：<br>部署區段特定的[動態內容區塊](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks)。使用Real-Time CDP的<br>**[!DNL Commerce]**：<br>使用[Audience Activation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation)來部署受眾特定的動態內容區塊，這些區塊會回應即時動作和統一的客戶設定檔資料，同時集中管理Real-Time CDP中的設定檔和受眾。使用[!DNL Target]**&#x200B;的<br>**[!DNL Commerce]：<br>在Adobe [!DNL Target]中使用Adobe [!DNL Commerce]資料來個人化網站體驗的每個部分，包括內容、導覽專案、完整版面配置等等。 A/B測試內容，自動為每個客戶選取和部署成功內容。使用AEM Assets的<br>**[!DNL Commerce]**：<br>在Adobe Experience Manager Assets中儲存您的所有內容。 從Adobe Commerce以原生方式存取該內容。 使用Generative AI建立內容變數，以針對不同區段或受眾進行個人化。 |
| **根據行為的個人化現場優惠方案** — 根據購物者動作（例如產品瀏覽和類別相關性）個人化促銷活動。 根據A/B測試的結果或業務目標部署下一個最佳優惠方案。 | **僅Adobe [!DNL Commerce]**：<br>部署區段特定的目錄和[購物車價格規則](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart)。<br>**Adobe [!DNL Commerce]搭配Real-Time CDP**：<br>使用[Audience Activation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation)來部署對象特定的選件，同時集中管理Real-Time CDP中的設定檔/對象。<br>**具有[!DNL Target]**&#x200B;的Commerce：使用Offer Decisioning來決定要部署哪個優惠方案、A/B測試或設定業務目標，以指導Adobe Commerce中部署的優惠方案。 |

### Analytics和深入分析

| 使用案例 | 解決方案 |
|---|---|
| **各管道的客戶行為** — 瞭解客戶參與每個管道（網頁、面對面、應用程式等）的細微差別，以影響每個管道的行銷策略；瞭解購物者漏斗和客戶體驗中的弱點。 | **Adobe [!DNL Commerce]僅**：<br>[Adobe [!DNL Commerce] Intelligence](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started)提供數位[!DNL Commerce]頻道上的豐富分析，但無法跨頻道或更廣泛的客戶歷程片段。<br>**Adobe [!DNL Commerce]搭配Customer Journey Analytics**：<br>[!DNL Commerce]資料摘要資料控制面板，取得客戶體驗所有階段（跨管道）的完整豐富詳細資訊。 瞭解每個接觸點和更廣泛的漏斗，以找出客戶歷程中可能流失的弱點。 |
| **購買趨勢** — 瞭解特定時間範圍內的購買行為（例如，購物籃分析、產品分析），以識別趨勢、季節性並根據歷史購買模式最佳化行銷。 | **Adobe [!DNL Commerce]僅**：<br>[Adobe [!DNL Commerce] Intelligence](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started)提供數位[!DNL Commerce]頻道上的豐富分析，但無法跨頻道或更廣泛的客戶歷程片段。<br>**Adobe [!DNL Commerce]搭配Customer Journey Analytics**：<br>[!DNL Commerce]資料摘要資料控制面板，取得客戶體驗所有階段（跨管道）的完整豐富詳細資訊。 瞭解每個接觸點和更廣泛的漏斗，以找出客戶歷程中可能流失的弱點。 |

## 範例使用案例

- 瞭解如何使用Adobe Journey Optimizer來[傳送捨棄的購物車電子郵件](https://experienceleague.adobe.com/en/docs/commerce/data-connection/use-cases/using-ajo)。
- 瞭解如何[在Real-Time CDP](https://experienceleague.adobe.com/en/docs/commerce/data-connection/use-cases/create-audience)中建立對象，以通知Adobe [!DNL Commerce]中的購物車價格規則。
