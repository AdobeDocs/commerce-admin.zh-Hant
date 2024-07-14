---
title: 什麼是店面？
description: 瞭解您的商店可以提供的頁面和功能元素，以支援客戶的購物體驗。
exl-id: 1c64888f-2bc0-4e2e-b7da-0e7182ea67e0
feature: Storefront
source-git-commit: 3b359ed43e81a2771a372c8e3c7557853b3eecad
workflow-type: tm+mt
source-wordcount: '816'
ht-degree: 0%

---

# 什麼是店面？

在您的Adobe Commerce或Magento Open Source實作中，店面是您存放區的對外公開部分。 它提供客戶用於購物和購買的內容和功能元件。

客戶進行銷售的路徑有時稱為&#x200B;_購買路徑_，您的店麵包含供客戶完成此路徑的元件。 以下章節提供提供提供策略價值的基本頁面型別概觀，即客戶在商店購物時通常會造訪的位置。 在檢閱時，請考慮可在客戶歷程的每個階段使用的不同商店功能。

## 首頁

您是否知道大部分人在決定留下或前往其他位置前，只會在頁面上停留幾秒鐘？ 留下印象並不久。 研究表明，人們也喜歡照片，尤其是其他人的照片。 無論您選擇何種設計，首頁上的所有內容都應推動訪客進行銷售流程的下一步。 我們的想法是從某一個興趣點到下一個興趣點，以有凝聚力的流程引導他們的注意力。

![店面首頁範例](./assets/storefront-homepage-full.png){width="700"}

## 目錄頁面

目錄頁面清單通常具有小型產品影像和簡短說明，並可格式化為清單或格線。 您可以新增區塊、影片和關鍵字豐富的說明，也能為促銷活動或季節建立特別設計。 您可以建立特殊類別，以包含由不同類別的產品所組成的精選系列的生活風格或品牌。

最初的產品說明通常能給予購物者足夠的資訊，值得仔細檢視。 知道自己想要什麼的人可以將產品新增到購物車中去。 登入帳戶期間購物的客戶可獲得個人化的購物體驗。

店面上的![集合頁面](./assets/storefront-collection-page.png){width="700"}

## 搜尋結果

您知道使用搜尋的人購買的可能性幾乎是僅依賴導覽的人的兩倍？ 您可能會將這些購物者視為&#x200B;_預先合格_。

### [!DNL Live Search]

使用Adobe Commerce的[[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html)，您的商店可提供快速、超級相關且直覺式的搜尋體驗，Adobe Commerce可免費使用。

![即時搜尋範例 — 在您輸入時進行搜尋](./assets/storefront-search-as-you-type.png){width="700"}

### 標準目錄搜尋

透過[標準目錄搜尋](../catalog/search.md)，您的商店在右上角包含「搜尋」方塊，並在頁尾包含「進階搜尋」連結。 系統會儲存購物者提交的所有搜尋字詞，方便您精確檢視他們想要尋找的內容。 您可以提供建議，並輸入同義字和常見拼字錯誤。 然後，在輸入搜尋字詞時顯示特定頁面。

![標準目錄搜尋結果範例](./assets/storefront-search-results-page-full.png){width="700"}

## 產品頁面

產品頁面有很多事情要做！ 在產品頁面上吸引您眼球的第一件事情，就是具有高解析度縮放與縮相簿的主要影像。 除了價格與可用性之外，還有索引標籤區段，其中包含更多資訊和相關產品的清單。

![店面產品頁面範例](./assets/storefront-product-page-full-m.png){width="700"}

## 購物車

購物車是決定訂購總計、折扣券、預估運費和稅金的地方，也是顯示信任徽章和印章的好地方。 這也是提供最後一個專案的理想機會。 進行交叉銷售時，只要有特定專案出現在購物車中，您就可以選取要提供的特定專案作為衝動購買。

![店面購物車頁面範例](./assets/storefront-cart-full.png){width="700"}

## 結帳頁面

結帳程式包含兩個步驟：

1. 送貨資訊

   結帳程式的第一個步驟是讓客戶完成送貨地址資訊，並選擇送貨方式。 如果客戶有帳戶，則系統會自動輸入送貨地址，但如有需要，也可以進行變更。
如果訪客客戶輸入的電子郵件地址被識別為先前已註冊，則當存放區組態中的[!UICONTROL Enable Guest Checkout Login]欄位設定為`Yes`時，會顯示登入提示（請參閱&#x200B;_組態參考指南_&#x200B;中的[[!UICONTROL Checkout Options]](../configuration-reference/sales/checkout.md#checkout-options)）。 不過，此設定可能會將客戶資訊公開給未經驗證的使用者。

   ![店面結帳頁面範例](./assets/storefront-checkout-shipping-full.png){width="700"}

1. 複查與付款資訊

   結帳處理的第二個步驟是讓客戶選擇付款方式，並選擇性地套用折扣代碼。

   >[!NOTE]
   >
   >雖然[!DNL Commerce]允許設定多個優惠券代碼，但客戶只能將一個優惠券代碼套用至購物車。 （如需詳細資訊，請參閱[優惠券代碼](../merchandising-promotions/price-rules-cart-coupon.md#coupon-codes)。）

   ![店面結帳頁面範例](./assets/storefront-checkout-payment-full.png){width="700"}

頁面頂端的進度列會依循結帳程式的每個步驟，而&#x200B;_訂單摘要_&#x200B;會顯示截至目前所輸入的資訊。

>[!NOTE]
>
>兩步驟結帳的例外情況適用於虛擬及/或可下載的產品。 如果購物車中只有這些型別的產品，則結帳會自動轉換為單步驟程式，因為不需要送貨資訊。
