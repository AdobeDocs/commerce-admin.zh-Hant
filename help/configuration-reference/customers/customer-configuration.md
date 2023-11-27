---
title: 『[!UICONTROL Customers]  &gt； [!UICONTROL Customer Configuration]『
description: 檢閱上的組態設定 [!UICONTROL Customers] &gt； [!UICONTROL Customer Configuration] 商務管理員頁面。
exl-id: 596359d7-3891-4e0c-9604-3647032188fd
feature: Configuration, Customers
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '1898'
ht-degree: 2%

---

# [!UICONTROL Customers]  > [!UICONTROL Customer Configuration]

{{config}}

## [!UICONTROL Account Sharing Options]

![帳戶共用選項](./assets/customer-configuration-account-sharing-options.png)<!-- zoom -->

<!-- [Account Sharing Options](https://docs.magento.com/user-guide/customers/account-scope.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Share Customer Accounts] | 全域 | 決定商店階層中客戶帳戶的範圍。 選項： <br/>**`Global`**— 客戶帳戶資訊會與Commerce安裝中的每個網站和商店共用。<br/>**`Per Website`**  — 客戶帳戶資訊僅限於建立帳戶的網站。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Online Customers Options]

![線上客戶選項](./assets/customer-configuration-online-customers-options.png)<!-- zoom -->

<!-- [Online Customers Options](https://docs.magento.com/user-guide/customers/now-online.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Online Minutes Interval] | 全域 | 決定可從管理員存取客戶線上活動的時長。 留空則預設間隔為15分鐘。 |
| [!UICONTROL Customer Data Lifetime] | 全域 | 決定客戶輸入的未儲存資料過期前的分鐘數。 依預設，未儲存的資料會在60分鐘後到期。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Create New Account Options]

{{beta-updates}}

![建立新帳戶選項](./assets/customer-configuration-create-new-account-options.png)<!-- zoom -->

![建立新帳戶選項（VAT欄位）](./assets/customer-configuration-create-new-account-options-vat.png)<!-- zoom -->

<!-- [Create New Account Options (VAT Fields)](https://docs.magento.com/user-guide/customers/customer-account-configuration.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable Automatic Assignment to Customer Group] | 存放區檢視 | 決定是否自動將客戶指定至預設客戶群組。 若要在店面中顯示VAT編號，請設定「在店面中顯示VAT編號」，然後選取 `Yes`. 選項： <br/>**`Yes`**— 系統不會自動驗證客戶VAT ID，也不會變更客戶群組。<br/>**`No`**  — 系統行為如常執行，且預設客戶群組可在「預設群組」欄位中設定。 |
| [!UICONTROL Default Group] | 存放區檢視 | 識別建立帳戶時指派的初始客戶群組。 |
| [!UICONTROL Default Value for Disable Automatic Group Changes Based on VAT ID] | 全域 | (僅當目前的設定範圍設定為 `Default Group`.) 選擇預設是啟用還是停用根據VAT ID自動變更客戶群組。 可在產品層級上覆寫設定。 設定會影響下列情況中的系統行為： <br/>  — 客戶預設地址或整個預設地址的VAT ID會變更。 <br/>  — 對於先前沒有儲存地址的註冊客戶或在結帳期間註冊的客戶，在結帳期間模擬客戶群組變更。 <br/>如果啟用了自動群組變更，則在第一種情況下，客戶群組會自動變更，而在第二種情況下，臨時模擬的客戶群組會指派給客戶。 如果停用自動群組變更，則除非管理員手動變更，否則指派的客戶群組不會變更。 |
| [!UICONTROL Show VAT Number on Storefront] | 網站 | 決定商店中的客戶是否可看到VAT編號。 選項： `Yes` / `No` <br/> 僅影響一般非B2B客戶帳戶。 公司帳戶有自己的個別「VAT編號」欄位。 |
| [!UICONTROL Default Email Domain] | 存放區檢視 | 識別商店的預設電子郵件網域。 例如： `mystore.com` |
| [!UICONTROL Default Welcome Email] | 存放區檢視 | 識別用於預設的電子郵件範本 _歡迎_ 電子郵件。 |
| [!UICONTROL Default Welcome Email Without Password] | 存放區檢視 | 替代歡迎電子郵件範本，用於管理員建立但尚未指派密碼的新客戶帳戶。 |
| [!UICONTROL Email Sender] | 存放區檢視 | 識別顯示為歡迎電子郵件寄件者的商店聯絡人。 |
| [!UICONTROL Require Emails Confirmation] | 網站 | 決定建立帳戶的請求是否需要客戶的確認。 選項： `Yes` / `No` |
| [!UICONTROL Confirmation Link Email] | 存放區檢視 | 識別用於確認電子郵件的電子郵件範本。 預設範本： `New account confirmation key` |
| [!UICONTROL Welcome Email] | 存放區檢視 | 識別在帳戶確認後傳送之歡迎訊息所使用的電子郵件範本。 |
| [!UICONTROL Generate Human-Friendly Customer ID] | 全域 | 判斷是否可從店面看到用來輸入及儲存VAT ID號碼的欄位。 選項： `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Password Options]

![密碼選項](./assets/customer-configuration-password-options.png)<!-- zoom -->

<!-- [Password Options](https://docs.magento.com/user-guide/customers/password-options.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Password Reset Protection Type] | 存放區檢視 | 決定用來重設客戶帳戶密碼的方法。 選項： <br/>**`By IP and Email`**— 收到來自重設通知的回應後，可線上上重設密碼，該重設通知會傳送至與管理員帳戶相關聯的電子郵件地址。<br/>**`By IP`**  — 密碼可以線上上重設。 <br/>**`By Email`**— 密碼可以透過回應電子郵件通知來重設，該電子郵件通知會傳送到與管理員帳戶關聯的電子郵件地址。<br/>**`None`**  — 密碼只能由存放區管理員重設。 |
| [!UICONTROL Max Number of Password Reset Requests] | 存放區檢視 | 限制每小時的密碼重設要求數目。 對於無限制的請求，輸入零(0)。 |
| [!UICONTROL Min Time Between Password Reset Requests] | 存放區檢視 | 決定密碼重設要求之間的分鐘數。 若要求之間沒有延遲，請輸入零(0)。 |
| [!UICONTROL Forgot Email Template] | 存放區檢視 | 識別客戶忘記密碼時所使用的電子郵件範本。 預設範本： `Forgot Password` |
| [!UICONTROL Remind Email Template] | 存放區檢視 | 識別客戶收到密碼提醒或提示時所使用的電子郵件範本。 預設範本： `Remind Password` |
| [!UICONTROL Reset Password Template] | 存放區檢視 | 決定客戶重設密碼時使用的電子郵件範本。 |
| [!UICONTROL Password Template Email Sender] | 存放區檢視 | 決定要顯示為密碼相關電子郵件寄件者的商店聯絡人。 |
| [!UICONTROL Recovery Link Expiration Period (hours)] | 全域 | 指定密碼復原連結到期前的小時數。 |
| [!UICONTROL Enable Autocomplete on login/forgot password forms] | 網站 | 決定登入/忘記密碼表單上是否啟用自動完成。 選項： `Yes` / `No` |
| [!UICONTROL Number of Required Character Classes] | 全域 | 決定密碼中必須包含的不同字元類別（小寫、大寫、數字和特殊字元）數目。 |
| [!UICONTROL Maximum Login Failures to Lockout Account] | 全域 | 決定鎖定客戶帳戶前失敗的登入嘗試次數。 對於不限次數的嘗試，輸入零(`0`)。 |
| [!UICONTROL Minimum Password Length] | 全域 | 決定密碼中允許的最小字元數。 數字必須大於零(`0`)。 |
| [!UICONTROL Lockout Time (minutes)] | 全域 | 決定嘗試登入失敗太多後，客戶帳戶鎖定的分鐘數。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Account Information Options]

![帳戶資訊選項](./assets/customer-configuration-account-info-options.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Change Email Template] | 存放區檢視 | 識別客戶變更電子郵件地址時所使用的預設電子郵件範本。 |
| [!UICONTROL Change Email and Password Template] | 存放區檢視 | 識別客戶變更其電子郵件地址和密碼時使用的預設電子郵件範本。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Name and Address Options]

### Magento Open Source選項

{{ce-feature}}

![名稱和地址選項 — Open Source](./assets/customer-configuration-name-address-options-ce.png)<!-- zoom -->

<!-- [Name and Address Options - Open Source](https://docs.magento.com/user-guide/customers/name-address-options.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Number of Lines in a Street Address] | 網站 | 決定街道地址中的行數。 街道地址由以下地址組成： `1` 至 `4` 行。 如果欄位空白，預設街道地址為三(`3`)行。 |
| [!UICONTROL Show Prefix] | 網站 | 決定客戶名稱的開頭是否包含前置詞，例如Mr與Ms. Options： `No` / `Optional` / `Required` |
| [!UICONTROL Prefix Dropdown Options] | 網站 | 定義首碼選項的清單。 以分號分隔值。 在第一個值前放置分號，在清單頂端顯示空白值。 |
| [!UICONTROL Show Middle Name (initial)] | 網站 | 判斷客戶名稱中是否包含中間首字母。 若使用，中間初始字元是選用欄位。 選項： `Yes` / `No` |
| [!UICONTROL Show Suffix] | 網站 | 決定客戶名稱在結尾是否包含尾碼，例如Jr.、Sr.和III。 選項： `No` / `Optional` / `Required` |
| [!UICONTROL Suffix Dropdown Options] | 網站 | 定義字尾選項的清單。 以分號分隔值。 在第一個值前放置分號，在清單頂端顯示空白值。 |
| [!UICONTROL Show Date of Birth] | 網站 | 決定名稱和地址表單中是否包含客戶出生日期。 選項： `No` / `Optional` / `Required`  <br><br>**_重要：_**為了遵循目前的安全性和隱私權最佳實務，請注意任何與儲存客戶完整出生日期（月、日、年）和其他個人識別碼相關的潛在法律和安全風險。 建議您限制客戶完整出生日期的儲存量，並建議使用客戶出生年作為替代方法。 |
| [!UICONTROL Show Tax/VAT Number] | 網站 | 決定稅捐或 [VAT編號](../../stores-purchase/vat.md) 包含在名稱和地址表單中。 選項： `No` / `Optional` / `Required` |
| [!UICONTROL Show Gender] | 網站 | 決定名稱和地址表單中是否包含性別。 選項： `No` / `Optional` / `Required` |
| [!UICONTROL Show Telephone] | 網站 | 決定名稱與地址表單中是否包含客戶的電話號碼。 選項： `No` / `Optional` / `Required` |
| [!UICONTROL Show Company] | 網站 | 判斷名稱和地址表單中是否包含客戶的公司。 選項： `No` / `Optional` / `Required` |
| [!UICONTROL Show Fax] | 網站 | 決定名稱與地址表單中是否包含客戶的傳真號碼。 選項： `No` / `Optional` / `Required` |

{:style=&quot;table-layout:auto&quot;}

### Adobe Commerce選項

{{ee-feature}}

![名稱和地址選項 — 商務](./assets/customer-configuration-name-address-options-ee.png)<!-- zoom -->

<!-- [Name and Address Options - Commerce](https://docs.magento.com/user-guide/customers/name-address-options.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Prefix Dropdown Options] | 網站 | 定義首碼選項的清單。 以分號分隔值。 在第一個值前放置分號，在清單頂端顯示空白值。 |
| [!UICONTROL Suffix Dropdown Options] | 網站 | 定義字尾選項的清單。 以分號分隔值。 在第一個值前放置分號，在清單頂端顯示空白值。 |
| [!UICONTROL Show Telephone] | 網站 | 決定名稱與地址表單中是否包含客戶的電話號碼。 選項： `No` / `Optional` / `Required` |
| [!UICONTROL Show Company] | 網站 | 判斷名稱和地址表單中是否包含客戶的公司。 選項： `No` / `Optional` / `Required` |
| [!UICONTROL Show Fax] | 網站 | 決定名稱與地址表單中是否包含客戶的傳真號碼。 選項： `No` / `Optional` / `Required` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Store Credit Options]

{{ee-feature}}

![儲存點數選項](./assets/customer-configuration-store-credit-options.png)<!-- zoom -->

<!-- [Store Credit Options](https://docs.magento.com/user-guide/customers/credit-configure.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable Store Credit Functionality] | 全域 | 決定是否啟用「商店評價」。 停用此選項會從客戶帳戶和「管理員管理客戶」頁面移除「商店貸方」。 選項： `Yes` / `No`. |
| [!UICONTROL Show Store Credit History to Customers] | 網站 | 決定餘額歷史記錄是否顯示在客戶帳戶中。 選項： `Yes` / `No`. |
| [!UICONTROL Refund Store Credit Automatically] | 全域 | 決定是否自動核發商店退款。 選項： `Yes` / `No` |
| [!UICONTROL Store Credit Update Email Sender] | 存放區檢視 | 決定要顯示為傳送給客戶的信用更新通知寄件者的商店身分。 |
| [!UICONTROL Store Credit Update Email Template] | 存放區檢視 | 決定用於信用更新的電子郵件範本。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Login Options]

![登入選項](./assets/customer-configuration-login-options.png)<!-- zoom -->

<!-- [Login Options](https://docs.magento.com/user-guide/customers/login-landing-page.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Redirect Customer to Account Dashboard after Logging in] | 網站 | 決定客戶登入帳戶後會發生什麼事。 若要將客戶重新導向至其帳戶儀表板，請選取 `Yes`. 選項： <br/>**`Yes`**— 客戶登入帳戶時，帳戶儀表板會出現。<br/>**`No`**  — 客戶登入帳戶後，可繼續購物。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Address Templates]

![地址範本](./assets/customer-configuration-address-templates.png)<!-- zoom -->

<!-- [Address Templates](https://docs.magento.com/user-guide/customers/address-templates.html) -->

| 範本 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Text] | 存放區檢視 | 範本用於列印的所有地址。 |
| [!UICONTROL Text One Line] | 存放區檢視 | 此範本定義客戶購物車通訊錄清單中的地址實體順序。 結帳期間的進度。 |
| [!UICONTROL HTML] | 存放區檢視 | 此範本定義位於 _客戶地址_ 區域([!UICONTROL Customers] > [!UICONTROL Manage Customers])。 這也會影響以下專案的使用者： _新增地址_ 客戶在其帳戶頁面上建立帳單或送貨地址時的頁面。 |
| [!UICONTROL PDF] | 存放區檢視 | 樣版會定義在列印的商業發票、出貨及銷退折讓單中，帳單與出貨地址的顯示。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Customer Segments]

{{ee-feature}}

![客戶區段](./assets/customer-configuration-customer-segments.png)<!-- zoom -->

<!-- [Customer Segments](https://docs.magento.com/user-guide/marketing/customer-segments.html) -->

| 範本 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable Customer Segment Functionality] | 全域 | 判斷是否可使用客戶區段來建立目標促銷活動。 選項： `Yes` / `No` |
| [!UICONTROL Real-time Check if Customer is Matched by Segment] | 全域 | 決定是否即時驗證客戶區段。 選項： <br/>**[!UICONTROL Yes]**— 客戶區段會即時驗證（預設值）。<br/>**[!UICONTROL No]**  — 客戶區段會透過單一合併條件SQL查詢進行驗證。 如果系統中有許多客戶區段，這會改善區段驗證的效能。 但是，分割資料庫或沒有註冊客戶時，驗證無法運作。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL CAPTCHA]

![驗證碼](./assets/customer-configuration-captcha.png)<!-- zoom -->

<!-- [CAPTCHA](https://docs.magento.com/user-guide/stores/security-captcha.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable CAPTCHA on Storefront] | 網站 | 在與Commerce網站相關的商店中啟用驗證碼。 選項： `Yes` / `No` |
| [!UICONTROL Font] | 網站 | 決定用於顯示驗證碼的字型。 若要新增您自己的字型，請將字型檔案放在與Commerce安裝相同的目錄中，並將宣告新增至 `config.xml` 檔案位於 `app/code/Magento/Captcha/etc`. |
| [!UICONTROL Forms] | 網站 | 決定使用CAPTCHA的表單。 選項： <br />`Applying Coupon Code` <br />`Checkout/Placing Order`<br />`Create user` <br />`Login` <br />`Forgot password` <br />`Contact Us` <br />`Change password` <br />`Share Wishlist Form` <br />`Send to Friend Form` <br />`Payflow Pro` (請參閱 [安全性修補程式](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/paypal-payflow-pro-active-carding-activity.html)) <br />`Add Gift Card Code` ![Adobe Commerce](../../assets/adobe-logo.svg)  <br />`Create company` ![Adobe Commerce](../../assets/adobe-logo.svg)  <br /><br />_**注意：**_ 選取時，一律會啟用「建立使用者」、「忘記密碼」和「Payflow Pro」表單。 |
| [!UICONTROL Displaying Mode] | 網站 | 決定驗證碼何時出現。 選項： <br/>**`Always`**— 必須具備驗證碼才能登入。<br/>**`After number of attempts to login`**  — 此選項僅適用於「管理員登入」表單。 選取時， _[!UICONTROL Number of Unsuccessful Attempts to Login]_欄位隨即顯示。 輸入您要允許的登入嘗試次數。 值 `0` （零）與設定類似 [!UICONTROL Displaying Mode] 至 `Always`.<br/>_**注意：**_若要追蹤失敗的登入嘗試次數，每次嘗試以一個電子郵件地址登入，以及從一個IP位址登入都會計算在內。 允許來自相同IP位址的登入嘗試次數上限為1,000。 此限制僅在啟用驗證碼時適用。 |
| [!UICONTROL Number of Unsuccessful Attempts to Login] | 網站 | 指定帳戶鎖定前，客戶可嘗試登入的次數。 |
| [!UICONTROL CAPTCHA Timeout (minutes)] | 網站 | 決定目前驗證碼的存留期。 驗證碼過期時，使用者必須重新載入頁面。 |
| [!UICONTROL Number of Symbols] | 網站 | 決定驗證碼中顯示的符號數，最多為8個。 您也可以指定範圍，例如5-8。 |
| [!UICONTROL Symbols Used in CAPTCHA] | 網站 | 決定驗證碼中顯示的字母（a-z和A-Z）和數字(0-9)。 難以與其他符號區分的符號，例如 `i`， `l`，或 `1`的預設驗證碼符號集中不包含。 |
| [!UICONTROL Case Sensitive] | 網站 | 判斷驗證碼字元是否區分大小寫。 選項： `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}
