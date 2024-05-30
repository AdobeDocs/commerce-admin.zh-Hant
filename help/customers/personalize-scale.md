---
title: 大規模建立引人入勝的個人化體驗
description: 瞭解Adobe中的哪些功能 [!DNL Commerce] 可讓您為購物者建立個人化體驗。
feature: Customers, Storefront, Personalization
exl-id: 9546e1b8-796b-4694-8396-773a2b0e9c12
source-git-commit: 9884d0991cceda7c2917f723467230d3702b2d0f
workflow-type: tm+mt
source-wordcount: '1648'
ht-degree: 0%

---

# 大規模建立引人入勝的個人化體驗

Adobe [!DNL Commerce] 提供強大的工具組，將每個客戶接觸點個人化，進而提高購物者的參與度、轉換率和營收。

在本文章中，您將瞭解：

- 什麼是個人化？
- 我需要哪些資料才能實現個人化？
- 如何Adobe [!DNL Commerce] 解鎖個人化？
- 可用的個人化使用案例

## 什麼是個人化？

個人化是指量身打造每位客戶購買體驗的各個層面，以符合其獨特的需求、情境和偏好設定。 個人化不僅限於網站內容，或推薦最適合的產品，而是涵蓋客戶歷程中的所有接觸點，包括：

- **行銷活動和通訊**  — 透過行銷活動和通訊提供相關且一致的訊息
- **產品探索**  — 在適當的時間向適當的客戶顯示適當的產品
- **促銷活動和優惠方案**  — 目標定位促銷活動和優惠方案以促使每位客戶轉換
- **內容體驗**  — 量身打造網站內容，以提供與客戶及其歷程高度相關的感覺

![個人化型別](assets/types-personalization.png){width="700" zoomable="yes"}

雖然這些型別的個人化體驗似乎對於一小部分客戶來說是可以實現的，但對於每個接觸點和管道中的數千或數百萬客戶來說，大規模個人化是無法做到的，所有即時體驗都讓人感覺是不可能的。 在以下小節中，您將瞭解如何Adobe [!DNL Commerce] Adobe Experience Cloud會有所幫助。

## 我需要哪些資料才能實現個人化？

有效的個人化需要提供客戶相關資訊的內容或訊號，這些資訊可用於修改客戶體驗。 下表提供各種資料型別以及Adobe的角色 [!DNL Commerce] 支援收集和啟用該資料。

| 資料型別 | 店面資料（行為事件） | 後台資料（伺服器端事件） | 客戶設定檔和區段資料 |
|---|---|---|---|
| **定義** | 客戶在您網站上採取的點按或動作。 | 生命週期相關資訊和每個訂單（過去和目前）的詳細資訊。 | 您的購物者是誰，以及他們符合哪些區段的資格。 |
| **Adobe Commerce擷取的事件** | [pageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#pageview)<br>[productPageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)<br>[searchRequestSent](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#searchrequestsent)<br>[searchResponseReceived](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#searchresponsereceived)<br>[addToCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#addtocart)<br>[openCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#opencart)<br>[登入](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#signin)<br>[登出](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#signout)<br>[startCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#startcheckout)<br>[completeCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#completecheckout)<br>[createRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#createrequisitionlist)<br>[addToRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#addtorequisitionlist)<br>[removeFromRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#removefromrequisitionlist) | **訂單狀態**：<br>[orderPlaced](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#orderplaced)<br>[orderItemsReturnedInitiated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#orderitemsreturnedinitiated)<br>[orderItemsShipped](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#orderitemsshipped)<br>[orderCanceled](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#ordercancelled)<br>[**訂單歷史記錄**](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/fundamentals/connect-data#send-historical-order-data)：<br>- SKU、名稱、價格數量、折扣<br> — 產品類別<br> — 付款金額、型態、幣別<br> — 送貨方式與金額<br> — 退款識別碼、金額、幣別<br> — 退貨原因、條件、解決方式<br> — 地址<br> — 電子郵件 | [**設定檔記錄**](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-profilerecord)：（姓名、性別、地址、忠誠度狀態、電話號碼、電子郵件地址）<br>**帳戶狀態**：<br>[accountCreated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#accountcreated)<br>[帳戶已更新](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#accountupdated)<br>[accountDeleted](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#accountdeleted) |

擁有這些豐富的第一方 [!DNL Commerce] 資料，您已準備好鎖定每個購物者的目標並加以個人化。 在下一節中，您將瞭解如何 [!DNL Commerce] 和Adobe Experience Cloud可協助您建立個人化體驗，以及您可以啟用的使用案例。

## 如何Adobe [!DNL Commerce] 是否提供個人化功能？

Adobe [!DNL Commerce] 資料共用可讓您收集上表中資料型別，並將其與其他Adobe Experience Cloud產品共用，以強化統一的客戶設定檔和對象、個人化行銷活動，以及豐富的分析和見解。

![資料如何流向Experience Platform邊緣](assets/commerce-edge.png){width="700" zoomable="yes"}

Adobe [!DNL Commerce] 資料共用包含兩個主要元件：

1. [資料連線](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview)：共用Adobe的店面、後端辦公室和客戶設定檔資料 [!DNL Commerce] 到Adobe Experience Platform edge network，以便在Adobe Experience Cloud應用程式中使用，包括：

   - [Adobe [!DNL Real-Time CDP]](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/intro/rtcdp-intro/overview)：將跨來源(ERP、CRM、POS)的客戶資料拼接至統一的設定檔，並建立規則型或AI型區段。
   - [Adobe [!DNL Journey Optimizer]](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/get-started)：啟動個人化的全頻道歷程，包括電子郵件行銷活動、簡訊、推播通知等。
   - [Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview) 和 [Adobe [!DNL Analytics]](https://experienceleague.adobe.com/en/docs/analytics/analyze/admin-overview/analytics-overview)：獲得對客戶和業務的深入分析。
   - [Adobe [!DNL Target]](https://experienceleague.adobe.com/en/docs/target/using/introduction/intro)：測試並最佳化內容、建議的產品、選件、導覽等。

1. [[!DNL Audience Activation]](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation)：使用 [!DNL Real-Time CDP] 可將您Adobe上的動態內容區塊、促銷活動和相關產品規則個人化的對象 [!DNL Commerce] 網站。

### 開箱即用的個人化：開始使用原生Adobe [!DNL Commerce] 功能

Adobe [!DNL Commerce] 透過其原生現成可用的功能，提供強大的個人化功能。 下表說明 [!DNL Commerce] 您可以立即啟動功能，以開始您的個人化歷程。

| 類別 | 功能 |
|---|---|
| 個人化產品探索 | [[!DNL Live Search]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/overview)：透過AI支援的搜尋，根據購物者的站上行為動作和相似性來個人化和最佳化搜尋結果。<br>[智慧型類別銷售](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-admin/category-merch)：根據購物者的現場行為動作和相關性，在類別頁面上進行AI驅動的產品排名。<br>[產品Recommendations](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview)：根據購物者行為、趨勢和相似性進行AI支援的產品推薦。<br>[相關產品規則](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules)：定義自訂規則，以顯示目錄中的產品，推動交叉銷售和向上銷售。 |
| 個人化網站內容 | [動態內容區塊](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks)：根據Adobe Commerce中的客戶區段顯示個人化內容區塊，例如橫幅。 |
| 個人化優惠和促銷 | [購物車價格規則](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart)：根據一組條件(包括Adobe中的客戶區段)，將折扣套用至購物車中的專案 [!DNL Commerce]. |
| Insights and Measurement | [Adobe [!DNL Commerce] 情報](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started)：瞭解您的個人化策略如何運作，並隨著時間改善。 |

## 熱門個人化使用案例

Adobe [!DNL Commerce] 客戶正使用現成可用的功能，並針對各種使用案例將資料分享至Adobe Experience Cloud。 以下章節重點說明主要使用案例，並說明如何使用Adobe來實作這些案例 [!DNL Commerce] 僅限或 [!DNL Commerce] 加上Experience Cloud應用程式。

### 個人化的行銷活動和通訊

| 使用案例 | 解決方案 |
|---|---|
| **捨棄的購物車和瀏覽**  — 當客戶在展示高參與度後放棄購物車或瀏覽工作階段時，提供個人化重新參與電子郵件或通知 | **Adobe [!DNL Commerce] 僅限**：<br>[電子郵件提醒](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/communications/email-reminders/email-reminder-rules)<br>**Adobe [!DNL Commerce] 使用Adobe Journey Optimizer**：<br>[!DNL Commerce] 資料會作為全頻道放棄歷程的觸發條件。 根據客戶屬性、客戶放棄的專案、其他購物行為和過去的購買，個人化該歷程。<br>Commerce與Adobe Journey Optimizer和Real-Time CDP：根據統一的客戶設定檔和集中管理的對象（例如建立高放棄率的對象）量身打造放棄行銷活動。 |
| **集中式受眾建立**  — 根據現場行為、過去購買、設定檔屬性、類別相關性、忠誠度狀態、客戶價值等，建立規則型或AI支援的對象 | **Adobe [!DNL Commerce] 僅限**：<br>收集客戶設定檔資訊的時機 [!DNL Commerce] 客戶建立帳戶。 建立規則型 [客戶區段](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/segments/customer-segments) 與客戶群組，以個人化內容與促銷活動。<br>**Adobe [!DNL Commerce] 使用Adobe Real-Time CDP**：<br> [整合式設定檔](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/home) 來自不同資料來源和管道；規則型或AI支援的對象。 |
| **根據購物者行為提供的個人化電子郵件/簡訊優惠方案**  — 根據過去的購買和購物者行為，透過目標電子郵件將個人化優惠傳送給客戶，例如，傳送客戶已檢視或參與的產品或類別的優惠。 | **Adobe [!DNL Commerce] 僅限**：<br>匯出資料以搭配行銷自動化解決方案使用。<br>**Adobe [!DNL Commerce] 使用Adobe Journey Optimizer和Real-Time CDP**：<br>[!DNL Commerce] 資料會作為電子郵件或簡訊優惠方案的觸發器，並提供訊號（購物者行為）以供根據進行個人化。 Real-Time CDP不是必要專案，但一般而言，這些優惠方案和行銷活動是圍繞對象建立的，且會在Real-Time CDP中建立和管理。 |
| **交叉或向上銷售相容的產品/品牌**  — 如果客戶購買了一個相容的產品或品牌，或表示與另一個產品或品牌高度相關，請傳送行銷活動（電子郵件/簡訊）以促進交叉銷售轉換。 | **Adobe [!DNL Commerce] 僅限**：<br>使用Adobe [!DNL Commerce] [產品Recommendations](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview) 以建議網站上的特定產品。 您也可以使用 [相關產品規則](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules) 以建議其他產品。<br>**[!DNL Commerce] 替換為 [!DNL Target]**：<br>Adobe [!DNL Target] 也有內建的產品推薦引擎，具有強大的功能，例如類別相關性。 這可用於交叉或向上銷售。<br>**[!DNL Commerce] 使用Adobe Journey Optimizer**：<br>使用 [!DNL Target] 或 [!DNL Commerce] 以決定要推薦的產品，然後透過Adobe Journey Optimizer傳遞。 |

### 個人化的網站體驗

| 使用案例 | 解決方案 |
|---|---|
| **個人化網站內容**  — 根據購物者動作（例如產品瀏覽和類別相關性），個人化網站橫幅和其他頁面內容。 根據A/B測試的結果或業務目標部署最適合的內容。 | **Adobe [!DNL Commerce] 僅限**：<br>部署區段專用 [動態內容區塊](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks).<br>**[!DNL Commerce] 使用Real-Time CDP **：<br>使用 [Audience Activation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation) 部署對象特定的動態內容區塊，以回應即時動作和統一的客戶設定檔資料，同時集中管理Real-Time CDP中的設定檔和對象。<br>**[!DNL Commerce] 替換為[!DNL Target]**：<br>使用Adobe將網站體驗的每個部分個人化，包括內容、導覽專案、完整頁面佈局等 [!DNL Commerce] Adobe中的資料 [!DNL Target]. A/B測試內容，自動為每個客戶選取和部署成功內容。<br>**[!DNL Commerce] 使用AEM Assets **：<br>將所有內容儲存在Adobe Experience Manager Assets中。 從Adobe Commerce以原生方式存取該內容。 使用GenAI建立內容變數，以針對不同的區段或對象進行個人化。 |
| **根據行為提供個人化的現場優惠方案**  — 根據購物者動作來個人化促銷活動，例如產品瀏覽和類別相關性。 根據A/B測試的結果或業務目標部署下一個最佳優惠方案。 | **Adobe [!DNL Commerce] 僅限**：<br>部署區段特定的目錄和 [購物車價格規則](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart).<br>**Adobe [!DNL Commerce] 使用Real-Time CDP**：<br>使用 [Audience Activation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation) 以部署對象特定的選件，同時集中管理Real-Time CDP中的設定檔/對象。<br>**Commerce與[!DNL Target]**：使用offer decisioning來決定要部署哪個優惠方案、A/B測試或設定業務目標，以指導Adobe Commerce中部署的優惠方案。 |

### Analytics和深入分析

| 使用案例 | 解決方案 |
|---|---|
| **各管道的客戶行為**  — 瞭解客戶參與每個管道（網頁、面對面、應用程式等）的細微差別，以影響每個管道的行銷策略；瞭解購物者漏斗和客戶體驗中的弱點。 | **Adobe [!DNL Commerce] 僅限**：<br>[Adobe [!DNL Commerce] 情報](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) 提供豐富的數位分析 [!DNL Commerce] 管道，但不會跨管道或客戶歷程的更廣泛片段。<br>**Adobe [!DNL Commerce] 具有Customer Journey Analytics**：<br>[!DNL Commerce] 資料摘要資料控制面板，以取得客戶體驗所有階段（跨管道）的完整豐富詳細資訊。 瞭解每個接觸點和更廣泛的漏斗，以找出客戶歷程中可能流失的弱點。 |
| **購買趨勢**  — 瞭解特定時間範圍內的購買行為（例如購物籃分析、產品分析），以識別趨勢、季節性並根據歷史購買模式最佳化行銷。 | **Adobe [!DNL Commerce] 僅限**：<br>[Adobe [!DNL Commerce] 情報](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) 提供豐富的數位分析 [!DNL Commerce] 管道，但不會跨管道或客戶歷程的更廣泛片段。<br>**Adobe [!DNL Commerce] 具有Customer Journey Analytics**：<br>[!DNL Commerce] 資料摘要資料控制面板，以取得客戶體驗所有階段（跨管道）的完整豐富詳細資訊。 瞭解每個接觸點和更廣泛的漏斗，以找出客戶歷程中可能流失的弱點。 |

## 範例使用案例

- 瞭解如何使用Adobe Journey Optimizer來 [傳送捨棄的購物車電子郵件](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/use-cases/using-ajo).
- 瞭解如何 [在Real-Time CDP中建立受眾](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/use-cases/create-audience) 通知Adobe中的購物車價格規則 [!DNL Commerce].
