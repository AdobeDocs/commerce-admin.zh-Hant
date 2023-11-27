---
title: 『[!UICONTROL Sales] &gt； [!UICONTROL Payment Methods] &gt； [!UICONTROL Braintree]『
description: 檢閱的組態設定 [!UICONTROL Braintree] 區段於 [!UICONTROL Sales] &gt； [!UICONTROL Payment Methods] 商務管理員頁面。
exl-id: cf08bc4d-8d88-45e7-af71-f1ff90023766
feature: Configuration, Payments
source-git-commit: 1f84bf9ab20aeccacf56eab396b2778140964d17
workflow-type: tm+mt
source-wordcount: '2330'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL Braintree]

>[!IMPORTANT]
>
>**Commerce 2.4移轉：**<br/>
>若是2.4.0之前的Adobe Commerce和Magento Open Source版本，建議商家從以下網址安裝並設定官方Braintree支付整合擴充功能： [Commerce Marketplace](https://marketplace.magento.com/catalogsearch/result/?q=braintree) 以取代核心整合。 截至2.4.0，擴充功能現已納入核心發行版本。
><br/><br/>
>移轉至Commerce 2.4時，商家需要解除安裝在Marketplace上散佈的擴充功能(`paypal/module-braintree` 或 `gene/module-braintree`)並更新任何程式碼自訂，以使用 `PayPal_Braintree` 名稱空間而非 `Magento_Braintree`. 來自Commerce套件擴充功能的組態設定和發佈至Commerce Marketplace的擴充功能持續存在。 系統會正常擷取、作廢或退款的付款，連同這些版本的擴充功能一併放置。
><br/><br/>
>如果您升級至Commerce 2.4.0，且未使用先前2.3.x版中建議的Commerce Marketplace擴充功能，則Braintree 2.4.0版無法運用多位址功能。 當購物者選取 _傳遞至多個地址_ ，Braintree付款方式不會出現。 先前建議用於2.3.x的Commerce Marketplace擴充功能有多個位址問題。

{{config}}

{{beta2-updates}}

## [!UICONTROL Basic Braintree Settings]

![基本Braintree設定](./assets/payment-methods-braintree-basic-config.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Title] | 存放區檢視 | 預設值： `Credit Card` (Braintree) |
| [!UICONTROL Environment] | 存放區檢視 | 選項： `Sandbox` / `Production` |
| [!UICONTROL Payment Action] | 存放區檢視 | 決定Braintree在處理付款時所採取的動作。 選項： <br/>**`Authorize`**— 客戶信用卡上的資金已獲授權，但並未從帳戶轉帳。 系統會在您的商店管理員中建立訂單。 您稍後可以擷取銷售，並建立發票。<br/>**`Intent Sale`** (先前版本 `Authorize and Capture` 在舊版中) — 客戶信用卡上的資金由Braintree授權並擷取，而訂單與商業發票則建立於您的商店管理員中。 |
| [!UICONTROL Sandbox Merchant ID] | 存放區檢視 | 這是您整個沙箱閘道帳戶的唯一識別碼。 也稱為 _公開ID_ 或 _生產ID_，您的商家ID和生產沙箱閘道不同。 此欄位出現於 _[!UICONTROL Environment]_欄位已設為 `Sandbox`. |
| [!UICONTROL Sandbox Public Key] | 存放區檢視 | 這是您的使用者專屬公用識別碼，可限制對加密資料的存取。 與您的沙箱Braintree閘道關聯的每個使用者都有各自的沙箱公開金鑰。 此欄位出現於 _[!UICONTROL Environment]_欄位已設為 `Sandbox`. |
| [!UICONTROL Sandbox Private Key] | 存放區檢視 | 這是您的使用者專屬私人識別碼，可限制對加密資料的存取。 與您的沙箱Braintree閘道關聯的每個使用者都有各自的沙箱私密金鑰。 此欄位出現於 _[!UICONTROL Environment]_欄位已設為 `Sandbox`. |
| [!UICONTROL Merchant ID] | 存放區檢視 | 這是您整個閘道帳戶的唯一識別碼，包括閘道中可能存在的多個商家帳戶。 也稱為 _公開ID_ 或 _生產ID_，您的商家ID和生產沙箱閘道不同。 此欄位出現於 _[!UICONTROL Environment]_欄位已設為 `Production`. |
| [!UICONTROL Public Key] | 存放區檢視 | 這是您的使用者專屬公用識別碼，可限制對加密資料的存取。 與您的Braintree閘道關聯的每個使用者都有自己的公開金鑰。 此欄位出現於 _[!UICONTROL Environment]_欄位已設為 `Production`. |
| [!UICONTROL Private Key] | 存放區檢視 | 這是您的使用者專屬私人識別碼，可限制對加密資料的存取。 與您的Braintree閘道關聯的每個使用者都有各自的私密金鑰。 此欄位出現於 _[!UICONTROL Environment]_欄位已設為 `Production`. |
| [!UICONTROL Enable Card Payments] | 網站 | 決定Braintree信用卡付款方式是否可供您的客戶作為付款方式使用。 選項： `Yes` / `No` |
| [!UICONTROL Enable Vault for Card Payments] | 網站 | 啟用後，可為客戶付款資訊提供安全的儲存空間，因此客戶不必在每次購買時都重新輸入信用卡資訊。 選項： `Yes` / `No` |
| [!UICONTROL Enable Vault CVV Reverification] | 網站 | 啟用後，將會對您的Braintree帳戶中的CVV規則設定進行驗證。 選項： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Advanced Braintree Settings]

![Braintree進階設定](./assets/payment-methods-braintree-advanced-config.png){width="550" zoomable="yes"}

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Vault Title] | 網站 | 描述性標題供您參考，可識別儲存客戶卡資訊的儲存庫。 |
| [!UICONTROL Merchant Account ID] | 網站 | 與此網站的Braintree交易相關聯的商家帳戶ID。 如果保留為空白，則會使用您Braintree帳戶的預設商家帳戶。 |
| [!UICONTROL Skip Fraud Checks on Admin Orders] | 網站 | 防止將交易當作的一部分傳送以進行評估 [!DNL Advanced Fraud Tools] 核取，僅在透過管理員下單的訂單上設定為 `Yes`.<br/>選項： `Yes` / `No` |
| [!UICONTROL Bypass Fraud Protection Threshold] | 網站 | `Advanced Fraud Protection` 當達到或超過臨界值時，會略過檢查。 將此欄位保留空白會停用此選項。 |
| [!UICONTROL Debug] | 網站 | 決定Braintree系統與存放區之間的通訊是否記錄在記錄檔中。 選項： `Yes` / `No` |
| [!UICONTROL CVV Verification] | 網站 | 決定是否要求客戶從信用卡背面提供三位數安全碼。 選項： `Yes` / `No` |
| [!UICONTROL Send Card Line Items] | 網站 | 傳送所有付款方式的購物車明細專案。 選項： `Yes` / `No` |
| [!UICONTROL Credit Card Types] | 網站 | 指定您接受以透過Braintree付款的每一張信用卡。 按住不放 `Ctrl` (或 `Command` (在Mac上)以選取卡片組合。 選項： `American Express` / `Visa` / `MasterCard` / `Discover` / `JCB` / `Diners` / `Maestro International` |
| [!UICONTROL Sort Order] | 網站 | 決定結帳期間Braintree與其他付款方法一起列出的順序。 |

## [!UICONTROL Braintree Webhooks Settings]

![BraintreeWebhook設定](./assets/payment-methods-braintree-webhooks-config.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable Webhook] | 網站 | 啟用webhook功能以防範詐騙、ACH付款及本機付款方法。 選項： `Yes` / `No` |
| [!UICONTROL Fraud Protection URL] | 網站 | 將此URL新增至您的Braintree帳戶，做為 [!UICONTROL Webhook Destination URL]. **此URL必須是安全的並可公開存取。** |
| [!UICONTROL Fraud Protection Approve Order Status] | 網站 | 當Braintree核准防詐騙功能時，系統會將選取的訂單狀態指派給商務訂單。 此狀態是用來更新使用ACH付款方式的訂單狀態以及訂單移至 `SETTLED` 在Braintree中。 |
| [!UICONTROL Fraud Protection Reject Order Status] | 網站 | 當Braintree拒絕詐騙保護時，會將選取的訂單狀態指派給商務訂單。 此狀態是用來更新使用ACH付款方式的訂單狀態，以及當 `SETTLEMENT` 是 `DECLINED` 在Braintree中。 |

{style="table-layout:auto"}

## [!UICONTROL Country Specific Settings]

![國家/地區特定設定](./assets/payment-methods-braintree-country-specific-config.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Payment from Applicable Countries] | 網站 | 決定您是接受所有國家/地區Braintree處理的付款，還是僅接受特定國家/地區的付款。 選項： `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | 網站 | 如果適用，會識別您接受Braintree所處理付款的特定國家/地區。 |
| [!UICONTROL Country Specific Credit Card Types] | 網站 | 識別每個國家/地區接受Braintree所處理之付款的信用卡。 系統會為每個國家/地區儲存記錄。 選項： <br/>**`Country`**— 選擇國家。<br/>**`Allowed Card Types`**  — 選取從國家/地區接受以透過Braintree付款的每一張信用卡。 <br/>**`Add`**— 新增線路以允許不同國家的信用卡。<br/>**`Action`**  — 刪除國家/地區允許的信用卡記錄。 |

{style="table-layout:auto"}

## [!UICONTROL ACH through Braintree]

![ACH透過Braintree](./assets/payment-methods-braintree-ach-config.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enabled ACH Direct Debit] | 網站 | 決定是否 [!DNL ACH Direct Debit] 是透過Braintree以付款方式納入。 選項： `Yes` / `No` |
| [!UICONTROL Sort Order] | 網站 | 決定順序 [!DNL ACH Direct Debit] 在結帳期間與其他付款方法一起列出。 |

{style="table-layout:auto"}

## [!UICONTROL Apple Pay through Braintree]

![Apple透過Braintree支付](./assets/payment-methods-braintree-applepay-config.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable ApplePay through Braintree] | 網站 | 決定是否透過Braintree將Apple Pay納入付款方式。 選項： `Yes` / `No` <br/><br/> 網域必須 [先在Braintree帳戶中驗證](https://developer.paypal.com/braintree/docs/guides/apple-pay/configuration/javascript/v3). |
| [!UICONTROL Payment Action] | 網站 | 決定Braintree在處理付款時所採取的動作。 選項： <br/>**`Authorize`**— 客戶卡上的資金已獲授權，但並未從客戶帳戶轉帳。 系統會在您的商店管理員中建立訂單。 您稍後可以擷取銷售，並建立發票。<br/>**`Intent Sale`**  — 客戶卡上的資金由Braintree授權並擷取，而訂單與商業發票則建立於您的商店管理員中。 **_注意：_** 這是 `Authorize and Capture` （在2.3.x及舊版中）。 |
| [!UICONTROL Merchant Name] | 存放區檢視 | 顯示在ApplePay快顯視窗中的標籤給客戶。 |
| [!UICONTROL Sort Order] | 網站 | 決定結帳期間Apple Pay與其他付款方法一起列出的順序。 |

{style="table-layout:auto"}

## [!UICONTROL Local Payment Methods]

![本地付款方法](./assets/payment-methods-braintree-local-payment-config.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enabled Local Payment Methods] | 網站 | 決定是否透過Braintree將「當地付款方式」納入為付款方式。 選項： `Yes` / `No` |
| [!UICONTROL Title] | 網站 | 顯示在結帳付款方式區段上的標籤。 預設值： `Local Payments` |
| [!UICONTROL Allowed Payment Method] | 網站 | 選取要啟用的本機「付款」方式。 選項： `Bancontact` / `EPS` / `giropay` / `iDeal` / `Klarna Pay Now` / `SOFORT` / `MyBank` / `P24` / `SEPA/ELV Direct Debit` （尚未支援） |
| [!UICONTROL Sort Order] | 網站 | 決定結帳期間本機付款方式與其他付款方式一起列出的順序。 |

{style="table-layout:auto"}

>[!NOTE]
>
>套件式Braintree擴充功能不支援 [Braintree開發人員檔案](https://developer.paypal.com/braintree/docs/guides/local-payment-methods/overview). 正在開發其他本機付款方法，未來版本將支援這些方法。

## [!UICONTROL GooglePay through Braintree]

![透過Braintree的GooglePay](./assets/payment-methods-braintree-googlepay-config.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enabled GooglePay through Braintree] | 網站 | 決定是否 [!DNL Google Pay] 透過Braintree以付款方式包含付款。 選項： `Yes` / `No` |
| [!UICONTROL Payment Action] | 網站 | 決定Braintree在處理付款時所採取的動作。 選項： <br/>**`Authorize`**— 客戶卡上的資金已獲授權，但並未從客戶帳戶轉帳。 系統會在您的商店管理員中建立訂單。 您稍後可以擷取銷售，並建立發票。<br/>**`Intent Sale`**  — 客戶卡上的資金由Braintree授權並擷取，而訂單與商業發票則建立於您的商店管理員中。 **_注意：_** 這是 `Authorize and Capture` （在2.3.x及舊版中）。 |
| [!UICONTROL Button Color] | 網站 | 決定 [!DNL Google Pay] 按鈕。 選項： `White` / `Black` |
| [!UICONTROL Merchant ID] | 存放區檢視 | 必須在這裡輸入Google提供的ID。 |
| [!UICONTROL Accepted Cards] | 網站 | 選擇客戶可使用以下方式下訂單的卡片型別 [!DNL Google Pay]. |
| [!UICONTROL Sort Order] | 網站 | 決定結帳期間Google Pay與其他付款方法一起列出的順序。 |

{style="table-layout:auto"}

## [!UICONTROL Venmo through Braintree]

![Venmo透過Braintree](./assets/payment-methods-braintree-venmo-config.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable Venmo through Braintree] | 網站 | 決定是否 [!DNL Venmo] 是透過Braintree以付款方式納入。 選項： `Yes` / `No` |
| [!UICONTROL Payment Action] | 網站 | 決定Braintree在處理付款時所採取的動作。 選項： <br/>**`Authorize`**— 客戶卡上的資金已獲授權，但並未從客戶帳戶轉帳。 系統會在您的商店管理員中建立訂單。 您稍後可以擷取銷售，並建立發票。<br/>**`Intent Sale`**  — 客戶卡上的資金由Braintree授權並擷取，而訂單與商業發票則建立於您的商店管理員中。 **_注意：_** 這是  _授權與擷取_ （在2.3.x及舊版中）。 |
| [!UICONTROL Sort Order] | 網站 | 決定結帳期間Venmo與其他付款方法一起列出的順序。 |

{style="table-layout:auto"}

## [!UICONTROL PayPal through Braintree]

![透過Braintree提供PayPal](./assets/payment-methods-braintree-paypal-config.png){width="550" zoomable="yes"}

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable PayPal through Braintree] | 網站 | 決定是否透過Braintree將PayPal納入付款方式。 選項： `Yes` / `No` |
| [!UICONTROL Enable PayPal Credit through Braintree] | 網站 | 決定是否要透過Braintree將PayPal點數納入為付款方式。 選項： `Yes` / `No`. 此欄位出現於 `Enable PayPal through Braintree` 設為 `Yes` |
| [!UICONTROL Enable PayPal PayLater through Braintree] | 網站 | 決定是否透過Braintree將PayPal PayLater納入為付款方式。 選項： `Yes` / `No`. 此欄位出現於 `Enable PayPal through Braintree` 設為 `Yes` |
| [!UICONTROL Title] | 存放區檢視 | 透過結帳期間對客戶的Braintree識別PayPal的標籤。 預設值： `PayPal` |
| [!UICONTROL Vault Enabled] | 網站 | 啟用後，可為客戶付款資訊提供安全的儲存，因此客戶不必在每次購買時都重新輸入其PayPal資訊。 選項： `Yes` / `No` |
| [!UICONTROL Sort Order] | 網站 | 決定PayPal透過Braintree在結帳期間與其他付款方式一起列出之順序的數字。 |
| [!UICONTROL Override Merchant Name] | 存放區檢視 | 可用來針對每個商店檢視識別商家的其他名稱。 |
| [!UICONTROL Payment Action] | 網站 | 決定PayPal在處理付款時透過Braintree採取的動作。 選項： <br/>**`Authorize`**— 客戶卡上的資金已獲授權，但並未從客戶帳戶轉帳。 系統會在您的商店管理員中建立訂單。 您稍後可以擷取銷售，並建立發票。<br/>**`Authorize and Capture`**  — 客戶卡上的資金由PayPal透過Braintree授權並擷取，而訂單與發票則建立於您的商店管理員中。 |
| [!UICONTROL Payment from Applicable Countries] | 網站 | 決定您是接受PayPal透過所有國家/地區Braintree處理的付款，還是僅接受特定國家/地區的付款。 選項： `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | 網站 | 如果適用，會識別您接受Braintree所處理付款的特定國家/地區。 |
| [!UICONTROL Require Customer's Billing Address] | 網站 | 決定是否需要客戶的帳單地址才能提交訂單。 選項： `Yes` / `No` |
| [!UICONTROL Debug] | 網站 | 判斷PayPal透過Braintree系統與您的商店之間的通訊是否記錄在記錄檔中。 選項： `Yes` / `No` |
| [!UICONTROL Display on Shopping Cart] | 網站 | 決定PayPal按鈕是否出現在 [迷你購物車](../../stores-purchase/cart-configuration.md#mini-cart) 並在 [購物車](../../stores-purchase/cart.md) 頁面。 選項： `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Styling]

![PayPal樣式](./assets/payment-methods-braintree-paypal-styling.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Location] | 網站 | 決定PayPal按鈕和訊息在店面上的呈現位置。 選項： `Mini-Cart and Cart Page` / `Checkout Page` / `Product Page` |

{style="table-layout:auto"}

**[!UICONTROL Mini-Cart and Cart Page]**

本節中的選項和設定會因 _[!UICONTROL Location]_欄位。

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL PayPal Button Type] | 網站 | 將按鈕設為下列三種型別之一： `PayPal Button` / `PayPal Pay Later Button` / `PayPal Credit Button` |

**[!UICONTROL PayPal Button]**

本節中的選項和設定會因在中選取的按鈕型別而異。 _[!UICONTROL PayPal Button Type]_欄位。

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Show PayPal Button] | 網站 | 決定PayPal按鈕在選取位置上的位置。 選項： `Yes` / `No` |
| [!UICONTROL Button Label] | 網站 | 決定PayPal按鈕的標籤。 選項： `Paypal` / `Checkout` / `Buy Now` / `Pay` |
| [!UICONTROL Color] | 網站 | 決定PayPal按鈕的色彩。 選項： `Blue` / `Black` / `Gold` / `Silver` |
| [!UICONTROL Shape] | 網站 | 決定PayPal按鈕的形狀。 選項： `Pill` / `Rectangle` |
| [!UICONTROL Size] | 網站 | 決定PayPal按鈕的大小。 選項： `Medium` / `Large` / `Responsive` |

{style="table-layout:auto"}

**[!UICONTROL PayLater Messaging]**

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Show PayLater Messaging] | 網站 | 在選取的位置啟用PayLater訊息。 選項： `Yes` / `No`. 啟用時，會顯示可用優惠的PayLater訊息([限制套用](https://developer.paypal.com/docs/checkout/pay-later/us/))。 |
| [!UICONTROL Message Layout] | 網站 | 決定PayLater訊息配置。 選項： `Text` / `Flex` |
| [!UICONTROL Logo] | 網站 | 決定用於PayPal按鈕的標誌型別。 選項： `Inline` / `Primary` / `Alternative` / `None` |
| [!UICONTROL Logo Position] | 網站 | 決定PayPal按鈕的標誌位置。 選項： `Left` / `Right` / `Top` |
| [!UICONTROL Text Color] | 網站 | 決定PayPal按鈕的文字色彩。 選項： `Black` / `White` / `Monochrome` / `Grayscale` |

{style="table-layout:auto"}

設定這些選項後，您可以看到PayPal按鈕和PayLater訊息的預覽。 有些控制項可用來套用設定或重設值：

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Apply] | 網站 | 儲存按鈕和PayLater訊息的選取樣式設定，並將它們套用至目前位置和目前的按鈕型別。 |
| [!UICONTROL Apply to All Buttons] | 網站 | 儲存按鈕和PayLater訊息值的所選樣式設定，並將它們套用至所有按鈕型別和位置。 |
| [!UICONTROL Reset to Recommended Defaults] | 網站 | 將樣式設定傳回至按鈕和PayLater訊息的建議預設值，並將其套用至所有按鈕型別和位置。 |

{style="table-layout:auto"}

## 3d安全驗證設定

![3D安全驗證設定](./assets/payment-methods-braintree-3d-secure-verify-config.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL 3D Secure Verification] | 網站 | 決定當客戶註冊方案時，交易是否必須通過額外的驗證處理，例如 _由VISA驗證_. 選項： `Yes` / `No` |
| [!UICONTROL Always request 3DS] | 網站 | 始終對所有交易挑戰3D Secure要求。 選項： `Yes` / `No` |
| [!UICONTROL Threshold Amount] | 網站 | 決定單一訂單上授權處理的最大訂單金額。 如果訂單金額超過此臨界值，Braintree會拒絕授權。 |
| [!UICONTROL Verify for Applicable Countries] | 網站 | 決定必須驗證付款的國家/地區。 選項： `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Verify for Specific Countries] | 網站 | 如果適用，會識別必須驗證透過Braintree付款的特定國家/地區。 |

{style="table-layout:auto"}

## [!UICONTROL Dynamic Descriptors]

![動態描述元](./assets/payment-methods-braintree-dynamic-config.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Name] | 存放區檢視 | 名稱描述項分為兩部分，以星號(*)分隔。 描述項的第一部分會識別公司或DBA，而第二部分則會識別產品。 例如： `company*myproduct`  <br/><br/>描述項的公司和產品部分長度可透過以下方式分配，合併長度最多為22個字元： <br/>**`Option 1`**— 公司必須為三個字元/產品最多可為18個字元<br/>**`Option 2`**  — 公司必須包含7個字元/產品最多可包含14個字元 <br/>**`Option 3`**— 公司必須是12個字元/產品最多可以是9個字元 |
| [!UICONTROL Phone] | 存放區檢視 | 電話描述元的長度必須是10到14個字元，而且只能包含數字、破折號、括弧和句點。 例如： `9999999999` `(999) 999-9999` `999.999.9999` |
| [!UICONTROL URL] | 存放區檢視 | URL描述項代表您的網域名稱，長度最多可達13個字元。 例如： `company.com` |

{style="table-layout:auto"}
