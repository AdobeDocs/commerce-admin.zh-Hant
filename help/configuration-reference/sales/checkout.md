---
title: '[!UICONTROL Sales] &amp；gt； [!UICONTROL Checkout]'
description: 檢閱Commerce管理員的[!UICONTROL Sales] &amp；gt； [!UICONTROL Checkout]頁面上的組態設定。
exl-id: a912beb0-37a9-407b-83bd-dc6cd0554dc4
feature: Configuration, Checkout
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Checkout]

{{config}}

## [!UICONTROL Checkout Options]

![簽出選項](./assets/checkout-checkout-options.png)<!-- zoom -->

<!--[Checkout Options](https://docs.magento.com/user-guide/sales/checkout-options.html) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|------------------------------------------------------------------|--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Guest Checkout Login] | 存放區檢視 | 啟用此設定可允許未驗證的使用者（店面和API）查詢電子郵件地址是否已與客戶帳戶相關聯。 如果輸入的電子郵件地址已註冊到客戶帳戶，則可以顯示登入提示，藉此增強來賓的結帳工作流程，但代價是需要向未經驗證的使用者公開資訊。  選項： `Yes` / `No` |
| [!UICONTROL Enable Onepage Checkout] | 存放區檢視 | 決定[單頁簽出](../../stores-purchase/checkout-process.md#checkout-options)是否為預設簽出格式。 選項： `Yes` / `No` |
| [!UICONTROL Allow Guest Checkout] | 存放區檢視 | 決定來賓是否可以在未註冊商店帳戶的情況下進行[簽出](../../stores-purchase/checkout-guest.md)。 選項： `Yes` / `No` |
| [!UICONTROL Enable Terms and Conditions] | 存放區檢視 | 決定是否要求客戶在購買前同意銷售的[條款及條件](../../stores-purchase/terms-and-conditions.md)。 選項： `Yes` / `No` |
| [!UICONTROL Display Billing Address On] | 存放區檢視 | 決定結帳時帳單地址的位置。 選項： `Payment Method` / `Payment Page` |
| [!UICONTROL Maximum Number of Items to Display in Order Summary] | 存放區檢視 | 決定結帳期間可出現在&#x200B;_訂單摘要_&#x200B;中的專案數目上限。 預設值為`10`。 |
| [!UICONTROL Enable Address Search] | 網站 | ![Adobe Commerce](../../assets/adobe-logo.svg) (僅限Adobe Commerce)決定客戶是否可以使用[地址搜尋](../../stores-purchase/checkout-address-search.md)功能進行送貨及檢閱和付款步驟。 啟用後，請使用「客戶地址數限制」來設定在結帳期間啟用此功能所需的儲存地址數。 選項： `Yes` / `No` |
| 客戶地址數量限制 | 網站 | ![Adobe Commerce](../../assets/adobe-logo.svg) (僅限Adobe Commerce)啟用位址搜尋時，會決定結帳期間啟用此功能所需的儲存位址數量。 當客戶的儲存地址數目符合或超過此數目時，僅會在&#x200B;_送貨_&#x200B;和&#x200B;_檢閱與付款_&#x200B;步驟中轉譯預設地址。 客戶可使用搜尋功能來變更選取的地址。 預設值為`10`。 |

{style="table-layout:auto"}

## [!UICONTROL Shopping Cart]

![購物車](./assets/checkout-shopping-cart.png)<!-- zoom -->

<!--[Shopping Cart](https://docs.magento.com/user-guide/sales/cart-configuration.html) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Quote Lifetime (days)] | 網站 | 決定報價價格](../../stores-purchase/cart-configuration.md#quote-lifetime)的[期限（天）。 |
| [!UICONTROL After Adding a Product Redirect to Shopping Cart] | 存放區檢視 | 決定產品加入購物車後，[購物車頁面是否立即顯示](../../stores-purchase/cart-configuration.md#redirect-to-cart)。 選項： `Yes` / `No` |
| [!UICONTROL Number of Items to Display Pager] | 存放區檢視 | 決定觸發呼叫前購物車中的專案數。 預設值： `20` |
| [!UICONTROL Show Cross-sell Items in the Shopping Cart] | 存放區檢視 | 表示購物車中是否顯示[交叉銷售專案](../../catalog/related-products-up-sells-cross-sells.md#cross-sells)，提供額外的銷售選項給客戶。 選項： `Yes` （預設） / `No` |
| [!UICONTROL Grouped Product Image] | 存放區檢視 | 決定針對購物車中[群組產品](../../catalog/product-create-grouped.md)顯示的[縮圖](../../stores-purchase/cart-configuration.md#cart-thumbnails)影像。 選項： `Product Thumbnail Itself` / `Parent Product Thumbnail` |
| [!UICONTROL Configurable Product Image] | 存放區檢視 | 決定針對購物車中可設定產品顯示的[縮圖](../../stores-purchase/cart-configuration.md#cart-thumbnails)影像。 選項： `Product Thumbnail Itself` / `Parent Product Thumbnail` |
| [!UICONTROL Preview Quote Lifetime (minutes)] | 存放區檢視 | 決定從購物車預覽報價時最長使用時間（分鐘）。 |
| [!UICONTROL Enable Clear Shopping Cart] | 網站 | 決定購物車是否顯示選項，讓使用者在單一動作中清除購物車內容。 選項： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL My Cart Link]

![我的購物車連結](./assets/checkout-my-cart-link.png)<!-- zoom -->

<!-- [*My Cart Link*](https://docs.magento.com/user-guide/sales/mini-cart.html) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Display Cart Summary] | 網站 | 決定出現在「我的購物車」連結後方括弧中的值。 選項： `Display number of items in cart` / `Display item quantities` |

{style="table-layout:auto"}

## 迷你購物車

![迷你購物車](./assets/checkout-mini-cart.png)<!-- zoom -->

<!-- [*Mini Cart*](https://docs.magento.com/user-guide/sales/mini-cart.html) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Display Mini Cart] | 存放區檢視 | 決定當標題中的購物車圖示被點按時，迷你購物車是否出現在商店頁面上。 迷你購物車的顯示取決於主題。 選項： `Yes` / `No` |
| [!UICONTROL Number of Items to Display Scrollbar] | 存放區檢視 | 決定觸發卷軸之前可以出現在迷你購物車中的專案數量。 預設： `5` |
| [!UICONTROL Maximum Number of Items to Display] | 存放區檢視 | 決定迷你購物車中可顯示的專案最大數量。 預設： `10` |

{style="table-layout:auto"}

## [!UICONTROL Payment Failed Emails]

![付款失敗的電子郵件](./assets/checkout-payment-failed-emails.png)<!-- zoom -->

<!-- [*Payment Failed Emails*](https://docs.magento.com/user-guide/sales/checkout-payment-failed-emails.html) -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Payment Failed Email Receiver] | 存放區檢視 | 識別接收「付款失敗」電子郵件的商店聯絡人。 預設接收器： `General Contact` |
| [!UICONTROL Payment Failed Email Sender] | 存放區檢視 | 識別顯示為「付款失敗」電子郵件訊息寄件者的商店聯絡人。 預設寄件者： `General Contact` |
| [!UICONTROL Payment Failed Template] | 存放區檢視 | 識別用於付款失敗電子郵件的範本。 預設範本： `Payment Failed` |
| [!UICONTROL Send Payment Failed Copy To] | 存放區檢視 | 提供任何人收到「付款失敗」電子郵件復本的電子郵件地址。 請使用逗號分隔多個地址。 |
| [!UICONTROL Send Payment Failed Copy Method] | 存放區檢視 | 表示用於傳送副本的電子郵件方法。 選項： <br />**`Bcc`**— 在傳送給客戶的同一封電子郵件的標題中包含收件者，以傳送不公開的禮貌復本。 客戶看不到密件副本收件者。<br />**`Separate Email`** — 以個別電子郵件的形式傳送復本。 |

{style="table-layout:auto"}
