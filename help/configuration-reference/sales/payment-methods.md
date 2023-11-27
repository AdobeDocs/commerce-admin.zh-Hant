---
title: 『[!UICONTROL Sales] &gt； [!UICONTROL Payment Methods]『
description: 檢閱上的組態設定 [!UICONTROL Sales] &gt； [!UICONTROL Payment Methods] 商務管理員頁面。
exl-id: 6545b980-c8ef-460a-a884-d5315f5ad513
feature: Configuration, Payments
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '1691'
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods]

>[!TIP]
>
>Adobe Commerce和Magento Open Source的支付服務提供全包式自助服務解決方案，包括沙箱測試和簡單的設定，提供穩定且安全的支付處理作業。 若要深入瞭解此強大的工具集，以及此工具集如何提供您所需的深入分析和控制力，讓購買者獲得最佳體驗，請參閱 [_Payment Services使用手冊_](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html).

{{config}}

## [!UICONTROL Merchant Location]

![商家地點](./assets/payment-methods-merchant-location.png)<!-- zoom -->

<!-- [Merchant Location](https://docs.magento.com/user-guide/payment/merchant-location.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Merchant Country] | 網站 | 識別商家註冊以從事業務的國家/地區。 |

{:style=&quot;table-layout:auto&quot;}

## 建議的解決方案

對於剛開始接受PayPal帳戶或信用卡線上付款的商家，建議使用下列付款解決方案，以利他們使用。 隨著您的業務成長，您可以將這些與其他的PayPal支付解決方案結合。

- [PayPal Express簽出](paypal-express-checkout.md)
- [Braintree](braintree.md)
- [付款服務](payment-services.md)

>[!NOTE]
>
>2.4.x版移除了部分付款整合和隨附的擴充功能，並移至Commerce Marketplace。 您可在以下網址找到最新正式的付款整合延伸模組： [Commerce Marketplace](https://marketplace.magento.com/extensions/payments-security.html){：target=&quot;_blank&quot;}。
><br/>
>**Amazon Pay** 和 **卡拉納**：Adobe Commerce和Magento Open Source版本2.4.0到2.4.3包含這些廠商開發的擴充功能。 從2.4.4版開始，這些擴充功能不再與核心版本搭配，必須從Commerce Marketplace安裝和更新。 此Marketplace也可讓您存取擴充功能開發人員提供的目前檔案。
><br/>
>如果您已啟用並設定這些套件擴充功能之一，則必須更新 `composer.json` 檔案，作為2.4.4升級程式的一部分，並管理日後的擴充功能更新。 另請參閱 [升級模組](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) 在 _升級指南_ 以取得詳細資訊。<br/>
><br/>
>**Worldpay**， **Eway**， **網路來源**、和 **Authorize.Net**：如需從這些付款整合進行安全轉換的詳細資訊，請參閱 [DevBlog](https://community.magento.com/t5/Magento-DevBlog/Deprecation-of-Magento-core-payment-integrations/ba-p/426445){：target=&quot;_blank&quot;}。

## 其他PayPal方法

PayPal提供各種支付解決方案，滿足各種規模的企業需求，並參與全球各地的業務。 PayPal可讓您接受所有主要借記卡與信用卡的付款。 PayPal提供額外的便利性，無需額外付費，因為即使沒有PayPal帳戶的客戶也可以使用PayPal支付購買費用。

### PayPal多合一方法

- [PayPal付款進階](paypal-payments-advanced.md)
- [PayPal Payments Pro](paypal-payments-pro.md)
- [PayPal支付標準](paypal-payments-standard.md)

### PayPal付款閘道

- [PayPal Payflow Pro](paypal-payflow-pro.md) （包括Express結帳）
- [PayPal Payflow連結](paypal-payflow-link.md) （包括Express結帳）

## 基本付款方法

下列支付方法內建在Commerce中，不使用第三方支付提供者來處理交易。 許多基本付款方式是離線管理，而非線上管理。

### [!UICONTROL Check / Money Order]

![支票/匯票](./assets/payment-methods-check-money-order.png)<!-- zoom -->

<!-- [Check / Money Order](https://docs.magento.com/user-guide/payment/check-money-order.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 網站 | 決定客戶是否可用支票或匯票付款。 選項： `Yes` / `No` |
| [!UICONTROL Title] | 存放區檢視 | 客戶在結帳時看到的付款方式名稱。 |
| [!UICONTROL New Order Status] | 網站 | 決定初始 [訂單狀態](../../stores-purchase/order-status.md) 指派給支票或貨幣訂單支付的訂單。 預設值： `Pending` |
| [!UICONTROL Payment from Applicable Countries] | 網站 | 決定您接受支票或匯票付款的國家/地區。 選項： `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | 網站 | 識別您接受支票或匯票付款的特定國家/地區。 |
| [!UICONTROL Make Check Payable to] | 存放區檢視 | 應向其支付支票和匯票的實體名稱。 |
| [!UICONTROL Send Check to] | 存放區檢視 | 寄送支票和匯票的街道地址或郵政信箱。 |
| [!UICONTROL Minimum Order Total] | 網站 | 可透過支票或匯票支付的最小訂單金額。 |
| [!UICONTROL Maximum Order Total] | 網站 | 支票或匯票可支付的最大訂單金額。 <br/><br/>**_注意：_**訂單符合總計在最小或最大訂單總計之間，或是符合訂單總計的最大值。 |
| [!UICONTROL Sort Order] | 網站 | 一個數字，當在結帳期間與其他付款方式一起列出時，此數字可決定以支票或匯票付款的順序。 輸入 `0` 以將其放在清單頂端。 |

{:style=&quot;table-layout:auto&quot;}

### [!UICONTROL Bank Transfer Payment]

![銀行轉帳付款](./assets/payment-methods-bank-transfer-payment.png)<!-- zoom -->

<!-- [Bank Transfer Payment](https://docs.magento.com/user-guide/payment/bank-transfer.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 網站 | 決定客戶是否可從銀行直接將付款轉帳至您的商家帳戶，以支付款項。 選項： `Yes` / `No` |
| [!UICONTROL Title] | 存放區檢視 | 客戶在結帳時看到的付款方式名稱。 |
| [!UICONTROL New Order Status] | 網站 | 決定指定給銀行轉帳所付訂單的初始訂單狀態。 預設值： `Pending` |
| [!UICONTROL Payment from Applicable Countries] | 網站 | 決定您接受銀行轉帳付款的國家/地區。 選項： `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | 網站 | 識別您接受銀行轉帳付款的特定國家/地區。 |
| [!UICONTROL Minimum Order Total] | 網站 | 銀行轉帳可支付的最小訂單金額。 |
| [!UICONTROL Maximum Order Total] | 網站 | 銀行轉帳可支付的最大訂單金額。 <br/><br/>**_注意：_**訂單符合總計在最小或最大訂單總計之間，或是符合訂單總計的最大值。 |
| [!UICONTROL Sort Order] | 網站 | 此編號可決定結帳期間與其他付款方式一起列出時，銀行轉帳付款的順序。 輸入 `0` 以將其放在清單頂端。 |

{:style=&quot;table-layout:auto&quot;}

### [!UICONTROL Payment on Account]

{{b2b-feature}}

![分期付款](./assets/payment-methods-payment-on-account.png)<!-- zoom -->

<!-- [Payment on Account](https://docs.magento.com/user-guide/payment/payment-on-account.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 網站 | 決定公司是否可使用公司信用進行購買。 選項： `Yes` / `No` |
| [!UICONTROL Title] | 存放區檢視 | 客戶在結帳時看到的付款方式名稱。 |
| [!UICONTROL New Order Status] | 網站 | 決定記入公司帳戶的新訂單狀態。 選項： `Pending (default)` / `Processing` / `Suspected Fraud` |
| [!UICONTROL Payment from Applicable Countries] | 網站 | 決定允許公司將購買費用計入其帳戶的國家/地區。 選項： `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | 網站 | 識別公司可將購買費用計入其帳戶的特定國家/地區。 |
| [!UICONTROL Minimum Order Total] | 網站 | 指定可計入公司帳戶的最小訂單金額。 |
| [!UICONTROL Maximum Order Total] | 網站 | 可借記至公司帳戶的最大訂單金額。 <br/><br/>**_注意：_**訂單符合總計在最小或最大訂單總計之間，或是符合訂單總計的最大值。 |
| [!UICONTROL Sort Order] | 網站 | 一個數字，可決定結帳期間與其他付款方式一起列出時顯示的分期付款順序。 輸入 `0` 以將其放在清單頂端。 |

{:style=&quot;table-layout:auto&quot;}

>[!NOTE]
>
>下列訂單不支援以帳戶付款： [多個送貨地址](../../stores-purchase/shipping-settings.md#multiple-addresses) 和未出現在付款選項中。

### [!UICONTROL Cash On Delivery Payment]

![貨到付款](./assets/payment-methods-cash-on-delivery-payment.png)<!-- zoom -->

<!-- [Cash On Delivery Payment](../../stores-purchase/cash-on-delivery.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 網站 | 決定客戶是否可從銀行直接將付款轉帳至您的商家帳戶，以支付款項。 選項： `Yes` / `No` |
| [!UICONTROL Title] | 存放區檢視 | 客戶在結帳時看到的付款方式名稱。 |
| [!UICONTROL New Order Status] | 網站 | 決定指定給銀行轉帳所付訂單的初始訂單狀態。 預設值： `Pending` |
| [!UICONTROL Payment from Applicable Countries] | 網站 | 決定您接受銀行轉帳付款的國家/地區。 選項： `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | 網站 | 識別您接受銀行轉帳付款的特定國家/地區。 |
| [!UICONTROL Minimum Order Total] | 網站 | 指定銀行轉帳可支付的最小訂單金額。 |
| [!UICONTROL Maximum Order Total] | 網站 | 銀行轉帳可支付的最大訂單金額。 <br/><br/>**_注意：_**訂單符合總計在最小或最大訂單總計之間，或是符合訂單總計的最大值。 |
| [!UICONTROL Sort Order] | 網站 | 此編號可決定結帳期間與其他付款方式一起列出時，銀行轉帳付款的順序。 輸入 `0` 以將其放在清單頂端。 |

{:style=&quot;table-layout:auto&quot;}

### [!UICONTROL Zero Subtotal Checkout]

![零小計簽出](./assets/payment-methods-zero-subtotal-checkout.png)<!-- zoom -->

<!-- [Zero Subtotal Checkout](../../stores-purchase/zero-subtotal-checkout.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Title] | 存放區檢視 | 結帳時用於此付款方法的名稱。 預設值：不需要付款資訊 |
| [!UICONTROL Enabled] | 網站 | 決定零小計結帳是否可供店舖管理員用來管理小計為零的訂單，例如已徵稅的訂單，但折扣已將金額減少至零。 選項： `Yes` / `No` |
| [!UICONTROL New Order Status] | 網站 | 決定指定給已處理為「零小計結帳」之訂單的初始訂單狀態。 預設值： `Pending` |
| [!UICONTROL Payment from Applicable Countries] | 網站 | 決定可套用「零小計結帳」的國家/地區。 選項： `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | 網站 | 識別可套用「零小計結帳」的特定國家/地區。 |
| [!UICONTROL Sort Order] | 網站 | 在結帳期間與其他付款方式一起列出時，決定標題（例如「不需要付款資訊」）順序的數字。 輸入 `0` 以將其放在清單頂端。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Payment actions]

付款動作已設定 _依付款方式_. 付款作業會決定何時抓取資金，以及何時為銷售訂單建立商業發票。

如需個別設定選項的完整清單，請參閱每個個別付款方法主題的基本設定區段。

| 付款動作 | 說明 |
|--- |---|
| [!UICONTROL Authorization] | 核准購買，但保留資金。 此金額必須等到商戶擷取後才會提取。 |
| [!UICONTROL Authorize] | 授權採購員帳戶處理訂單總計，但不抓取付款。 藉由建立商業發票來擷取付款。 授權訂單可以作廢或取消。 |
| [!UICONTROL Authorize and Capture] | 授權採購員帳戶以取得訂單總計，並擷取付款。 系統會自動建立發票。 您可以透過銷退折讓單來退回抓取的資金。 抓取付款後，即無法取消訂單。 |
| [!UICONTROL Charge on shipment] | 在Commerce中建立發票時，Amazon會收到擷取請求並向客戶收費。 |
| [!UICONTROL Charge on order] | Amazon會建立發票，並在下訂單時向客戶收費。 |
| [!UICONTROL Not Capture] | 提交商業發票時，系統不會擷取付款。 假設您稍後透過Commerce擷取付款。 已完成的商業發票中有[擷取]按鈕。 擷取之前，您可以取消商業發票。 擷取之後，您可以建立銷退折讓單並作廢商業發票。 |
| [!UICONTROL Order] | 代表與PayPal的合約，可讓商家在定義的時間期間（最長29天）內，從客戶的買方帳戶擷取一或多項最高至訂單總金額的金額。 |
| [!UICONTROL Sale] | 已授權並立即從客戶帳戶中提取的購買金額。 |

{:style=&quot;table-layout:auto&quot;}

>[!NOTE]
>
>不要選取 _[!UICONTROL Not Capture]_選項，除非您確定稍後會透過Commerce擷取付款。 您必須先使用「擷取」按鈕擷取付款，才能建立銷退折讓單。

## [!UICONTROL Purchase Order]

![採購單](./assets/payment-methods-purchase-order.png)<!-- zoom -->

<!-- [Purchase Order](../../stores-purchase/purchase-order.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 網站 | 決定客戶是否可依採購單(PO)付款。 選項： `Yes` / `No` |
| [!UICONTROL Title] | 存放區檢視 | 客戶在結帳時看到的付款方式名稱。 |
| [!UICONTROL New Order Status] | 網站 | 決定初始 [訂單狀態](../../stores-purchase/order-status.md) 指定給採購單支付的訂單。 預設值：擱置中 |
| [!UICONTROL Payment from Applicable Countries] | 網站 | 決定您接受採購單付款的國家/地區。 選項： `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | 網站 | 識別您接受採購單付款的特定國家/地區。 |
| [!UICONTROL Minimum Order Total] | 網站 | 採購單可支付的最小訂單金額。 |
| [!UICONTROL Maximum Order Total] | 網站 | 採購單可支付的最大訂單金額。 <br/><br/>**_注意：_**訂單符合總計在最小或最大訂單總計之間，或是符合訂單總計的最大值。 |
| [!UICONTROL Sort Order] | 網站 | 此編號可決定結帳期間與其他付款方式一起列出時，依採購單付款的順序。 輸入 `0` 以將其放在清單頂端。 |

{:style=&quot;table-layout:auto&quot;}
