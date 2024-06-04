---
title: 電子郵件範本
description: 瞭解電子郵件範本，以及如何使用這些範本支援與客戶溝通並強化您的品牌。
exl-id: dfe28c77-607e-41e4-b872-3a07bcd67962
feature: Communications, Configuration
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1151'
ht-degree: 0%

---

# 電子郵件範本

電子郵件範本定義從您的商店傳送之自動化訊息的配置、內容和格式。 這些電子郵件稱為交易式電子郵件，因為每個電子郵件都與特定型別的交易或事件相關聯。

Commerce包含一組回應式電子郵件範本，這些範本是由商店運作期間發生的各種事件所觸發。 每個範本皆已針對任何熒幕大小進行最佳化，且可從桌上型電腦、平板電腦及行動裝置檢視。 您可以準備各種與客戶活動、銷售、產品警示、管理員動作和系統訊息相關的電子郵件範本 [自訂](email-template-custom.md) 以反映您的品牌。

Commerce電子郵件可由HTML和純文字電子郵件使用者端轉譯。 使用者端之間呈現電子郵件的方式可能有一些差異。

## 準備您的電子郵件標誌

標誌可以儲存為下列任何檔案型別。 具有透明背景的標誌可以儲存為。GIF或.PNG檔案。

- JPG/JPEG
- GIF
- PNG

頁首範本中指定了維度。 不過，為確保您的標誌在高解析度裝置上呈現良好，上傳的影像大小應為此大小的三倍。 通常，原始標誌圖稿會建立為向量影像，因此可以放大而不失去解析度。 然後可以將影像儲存為支援的點陣圖影像格式之一。

<!-- ![Logo 3X display size](./assets/email-logo-third-size.png)-->

若要利用標頭有限的垂直空間，請務必裁切影像，以消除頂端或底部的任何浪費空間。 編輯影像時，請務必保留標誌的外觀比例，以按比例調整高度和寬度。

一般而言，您可以讓影像小於原始影像，但不會失去解析度。 拍攝小影像並在像片編輯器中放大會降低影像的解析度。 例如，如果標頭範本中標誌的顯示尺寸是寬168畫素、高48畫素，則上傳的影像應該寬504畫素、高144畫素。

| 標誌Dimension | 1 x （顯示大小） | 3 x （影像大小） |
|----------|----|----|
| 寬度： | 168畫素 | 504畫素 |
| 高度： | 48畫素 | 144畫素 |

{style="table-layout:auto"}

## 設定電子郵件範本

此設定會決定出現在預設頁首範本中的標誌，以及任何自訂的標誌 [頁首](email-template-custom.md#header-template) 和 [頁尾](email-template-custom.md#footer-template) 您要用於商店傳送之交易式電子郵件訊息的範本。

![異動電子郵件設計](./assets/design-configuration-transactional-emails.png){width="600" zoomable="yes"}

如需組態設定的詳細清單，請參閱 [_異動電子郵件_](../content-design/configuration.md) 在 _內容與設計手冊_.

## 步驟1. 上傳您的標誌

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. 尋找要設定的存放區檢視，然後按一下 **[!UICONTROL Edit]** 在 _[!UICONTROL Action]_欄。

1. 在 _[!UICONTROL Other Settings]_，展開 ![展開選擇器](../assets/icon-display-expand.png) 此&#x200B;**[!UICONTROL Transactional Emails]**區段。

1. 上傳您準備好的專案 **[!UICONTROL Logo Image]**，按一下 **[!UICONTROL Upload]** 並從系統中選取檔案。

1. 的 **[!UICONTROL Logo Image Alt]**，輸入替代文字以識別影像。

1. 輸入 **[!UICONTROL Logo Width]** 和 **[!UICONTROL Logo Height]** 以畫素為單位。

   將每個值輸入為數字，不使用 `px` 縮寫。 這些值是指標題中標誌的顯示尺寸，而不是影像的實際大小。

## 步驟2. 選擇頁首與頁尾範本

如果您有適用於商店或不同商店的自訂頁首與頁尾範本，您可根據 [範圍](../getting-started/websites-stores-views.md#scope-settings) 設定的。 否則，會使用預設範本。 若要深入瞭解，請參閱 [自訂電子郵件範本](email-template-custom.md).

1. 選擇 **[!UICONTROL Header Template]** 用於所有異動電子郵件訊息。

1. 選擇 **[!UICONTROL Footer Template]** 用於所有異動電子郵件訊息。

1. 完成後，按一下 **[!UICONTROL Save Config]**.

## 電子郵件範本清單

電子郵件範本清單會依模組以字母順序組織。

### [!DNL Amazon_Payment]

| 範本 | 設定路徑 |
|--- |--- |
| `Hard-declined Authorization` | 不適用 |
| `Soft-declined Authorization` | 不適用 |

{style="table-layout:auto"}

### [!DNL Magento_Checkout]

| 範本 | 設定路徑 |
|--- |--- |
| `Payment Failed` | **頁面：** [!UICONTROL Sales] > [[!UICONTROL Checkout]](../configuration-reference/sales/checkout.md)<br/>**區段：** [!UICONTROL Payment Failed Emails]<br/>**欄位：** [!UICONTROL Payment Failed Template] |

{style="table-layout:auto"}

### [!DNL Magento_Company]

![Adobe Commerce B2B](../assets/b2b.svg) (僅適用於Adobe Commerce B2B)

| 範本 | 設定路徑 |
|--- |--- |
| `Assign Company Admin` | **頁面：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**區段：** [!UICONTROL Customer-Related Emails]<br/>**欄位：** [!UICONTROL Default 'Assign Company Admin' Email] |
| `Assign Company to Customer` | **頁面：** [!UICONTROL Customers] > [公司設定&#x200B;](../configuration-reference/customers/company-configuration.md)<br/>**區段：** [!UICONTROL Customer-Related Emails] <br/>**欄位：** [!UICONTROL Default 'Assign Company to Customer' Email] |
| `Company Admin Changed to Member` | **頁面：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**區段：** [!UICONTROL Customer-Related Emails]<br/>**欄位：** [!UICONTROL Default 'Company Admin Changed To Member' Email] |
| `Company Admin Set Inactive` | **頁面：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**區段：** [!UICONTROL Customer-Related Emails]<br/>**欄位：** [!UICONTROL Default 'Customer Status Inactive' Email] |
| `Company Invite` | 不適用 |
| `Company Registration Request` | **頁面：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**區段：** [!UICONTROL Email Options - Company Registration]<br/>**欄位：** [!UICONTROL Default Company Registration Email] |
| `Company Status Active1` | **頁面：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**區段：** [!UICONTROL Company Status Change]<br/>**欄位：** [!UICONTROL Default 'Company Status Change To Active 1" Email] |
| `Company Status Active2` | **頁面：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**區段：** [!UICONTROL Company Status Change]<br/>**欄位：** [!UICONTROL Default 'Company Status Change To Active 2" Email] |
| `Company Status Blocked` | **頁面：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**區段：** [!UICONTROL Company Status Change]<br/>**欄位：** [!UICONTROL Default 'Company Status Change To Blocked" Email] |
| `Company Status Pending Approval` | **頁面：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**區段：** [!UICONTROL Company Status Change]<br/>**欄位：** [!UICONTROL Default 'Company Status Change To Pending Approval" Email] |
| `Company Status Rejected` | **頁面：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**區段：** [!UICONTROL Company Status Change]<br/>**欄位：** [!UICONTROL Default 'Company Status Change To Rejected" Email] |
| `Customer Status Active` | **頁面：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**區段：** [!UICONTROL Customer-Related Emails]<br/>**欄位：** [!UICONTROL Default 'Customer Status Active' Email] |
| `Customer Status Inactive` | **頁面：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**區段：** [!UICONTROL Customer-Related Emails]<br/>**欄位：** [!UICONTROL Default 'Company Admin Inactive' Email] |
| `Sales Representative Assigned to Company` | **頁面：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**區段：** [!UICONTROL Customer-Related Emails]<br/>**欄位：** [!UICONTROL Default 'Sales Rep Assigned' Email] |

{style="table-layout:auto"}

### [!DNL Magento_CompanyCredit]

![Adobe Commerce B2B](../assets/b2b.svg) (僅適用於Adobe Commerce B2B)

| 範本 | 設定路徑 |
|--- |--- |
| `Credit Limit Allocated` | **頁面：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**區段：** [!UICONTROL Company Credit]<br/>**欄位：** [!UICONTROL Allocated Email Template] |
| `Credit Limit Updated` | **頁面：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**區段：** [!UICONTROL Company Credit]<br/>**欄位：** [!UICONTROL Updated Email Template] |
| `Credit Reimbursed` | **頁面：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**區段：** [!UICONTROL Company Credit]<br/>**欄位：** [!UICONTROL Reimbursed Email Template] |
| `Order Refunded to Company Credit` | **頁面：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**區段：** [!UICONTROL Company Credit]<br/>**欄位：** [!UICONTROL Refunded Email Template] |
| `Order Reverted to Company Credit` | **頁面：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**區段：** [!UICONTROL Company Credit]<br/>**欄位：** [!UICONTROL Reverted Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_Contact]

| 範本 | 設定路徑 |
|--- |--- |
| `Contact Form` | **頁面：** [!UICONTROL General] > [[!UICONTROL Contacts]](../configuration-reference/general/contacts.md)<br/>**區段：** [!UICONTROL Email Options]<br/>**欄位：** [!UICONTROL Email Template] |

{style="table-layout:auto"}

### [!UICONTROL Magento_Customer]

| 範本 | 設定路徑 |
|--- |--- |
| `Change Email` | **頁面：** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**區段：** [!UICONTROL Account Information Options]<br/>**欄位：** [!UICONTROL Change Email Template] |
| 變更電子郵件和密碼 | **頁面：** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**區段：** [!UICONTROL Account Information Options]<br/>**欄位：** [!UICONTROL Change Email and Password Template] |
| `Forgot Password` | **頁面：** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**區段：** [!UICONTROL Password Options]<br/>**欄位：** 忘記電子郵件範本 |
| `New Account` | **頁面：** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**區段：** [!UICONTROL Create New Account Options]<br/>**欄位：** 預設歡迎電子郵件 |
| `New Account (Magento/luma)` | **頁面：** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**區段：** [!UICONTROL Create New Account Options]<br/>**欄位：** 預設歡迎電子郵件 |
| `New Account Confirmation Key` | **頁面：** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**區段：** [!UICONTROL Create New Account Options]<br/>**欄位：** 確認連結電子郵件 |
| `New Account Confirmed` | **頁面：** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**區段：** [!UICONTROL Create New Account Options]<br/>**欄位：** 歡迎電子郵件 |
| `New Account Without Password` | **頁面：** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**區段：** [!UICONTROL Create New Account Options]<br/>**欄位：** 預設的歡迎電子郵件（不含密碼） |
| `Remind Password` | **頁面：** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**區段：** [!UICONTROL Password Options]<br/>**欄位：** 提醒電子郵件範本 |
| `Reset Password` | **頁面：** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**區段：** [!UICONTROL Password Options] <br/>**欄位：** 重設密碼範本 |

{style="table-layout:auto"}

### [!DNL Magento_CustomerBalance]

![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)

| 範本 | 設定路徑 |
|--- |--- |
| `Store Credit Update` | **頁面：** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**區段：** [!UICONTROL Store Credit Options]<br/>**欄位：** [!UICONTROL Store Credit Update Email Template] |

{style="table-layout:auto"}

### [!UICONTROL Magento_Directory]

| 範本 | 設定路徑 |
|--- |--- |
| `Currency Update Warnings` | **頁面：** [!UICONTROL General] > [[!UICONTROL Currency Setup]](../configuration-reference/general/currency-setup.md)<br/>**區段：** [!UICONTROL Scheduled Import Settings]<br/>**欄位：** [!UICONTROL Error Email Template] |

{style="table-layout:auto"}

### [!UICONTROL Magento_Email]

| 範本 | 設定路徑 |
|--- |--- |
| `Footer` | 不適用 |
| `Footer (Magento/luma)` | 不適用 |
| `Header` | 不適用 |

{style="table-layout:auto"}

### [!UICONTROL Magento_GiftCard]

![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)

| 範本 | 設定路徑 |
|--- |--- |
| `Gift Card(s) Purchase` | **頁面：** [!UICONTROL Sales] > [[!UICONTROL Gift Cards]](../catalog/product-gift-card-create.md)<br/>**區段：** [!UICONTROL Gift Card Email Settings]<br/>**欄位：** [!UICONTROL Gift Card Notification Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_GiftCardAccount]

| 範本 | 設定路徑 |
|--- |--- |
| `Gift Card Code/Balance` | **頁面：** [!UICONTROL Sales] > [[!UICONTROL Gift Cards]](../catalog/product-gift-card-create.md)<br/>**區段：** [!UICONTROL Email Sent from Gift Card Account Management]<br/>**欄位：** [!UICONTROL Gift Card Template] |

{style="table-layout:auto"}

### [!DNL Magento_GiftRegistry]

| 範本 | 設定路徑 |
|--- |--- |
| `New Registry` | **頁面：** [!UICONTROL  Customers] > [[!UICONTROL  Gift Registry]](../configuration-reference/customers/gift-registry.md) <br/>**區段：** [!UICONTROL Owner Notification]<br/>**欄位：** [!UICONTROL Email Template] |
| `Registry Sharing` | **頁面：** [!UICONTROL  Customers] > [[!UICONTROL  Gift Registry]](../configuration-reference/customers/gift-registry.md) <br/>**區段：** [!UICONTROL Gift Registry Sharing]<br/>**欄位：** [!UICONTROL Email Template] |
| `Registry Update` | **頁面：** [!UICONTROL  Customers] > [[!UICONTROL  Gift Registry]](../configuration-reference/customers/gift-registry.md) <br/>**區段：** [!UICONTROL Gift Registry Update]<br/>**欄位：** [!UICONTROL Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_InventoryInStorePickupSales]

| 範本 | 設定路徑 |
|--- |--- |
| `Order is Ready for Pickup` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**區段：** [!UICONTROL Order Ready For Pickup in Store]<br/>**欄位：** [!UICONTROL Order Ready For Pickup Email Template] |
| `Order is Ready for Pickup For Guest` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**區段：** [!UICONTROL Order Ready For Pickup in Store]<br/>**欄位：** [!UICONTROL Order Ready For Pickup Email Template for Guest] |

{style="table-layout:auto"}

### [!DNL Magento_Invitation]

| 範本 | 設定路徑 |
|--- |--- |
| `Customer Invitation` | **頁面：** [!UICONTROL Customers] > [[!UICONTROL Invitation]](../configuration-reference/customers/invitations.md)<br/>**區段：** [!UICONTROL Email]<br/>**欄位：** [!UICONTROL Customer Invitation Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_NegotiableQuote]

![Adobe Commerce B2B](../assets/b2b.svg) (僅適用於Adobe Commerce B2B)

| 範本 | 設定路徑 |
|--- |--- |
| `Declined Quote` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**區段：** [!UICONTROL Quote]<br/>**欄位：** [!UICONTROL Declined Quote Template (to Buyer)] |
| `Expiration Date Reset` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**區段：** [!UICONTROL Quote]<br/>**欄位：** [!UICONTROL Expiration Date Reset] | **頁面：** [!UICONTROL Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**區段：** [!UICONTROL Quote]<br/>**欄位：** [!UICONTROL Order Ready For Pickup Email Template] |
| `Expiration Warning` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**區段：** [!UICONTROL Quote]<br/>**欄位：** [!UICONTROL Quote Expiration (in 48 hrs)] |
| `Expiration Warning1` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**區段：** [!UICONTROL Quote]<br/>**欄位：** [!UICONTROL Quote Expiration (in 24 hrs)] |
| `New Quote` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**區段：** [!UICONTROL Quote]<br/>**欄位：** [!UICONTROL New Quote Template (to Seller)] |
| `Updated Quote` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**區段：** [!UICONTROL Quote]<br/>**欄位：** [!UICONTROL Updated Quote Template (to Seller)] |

{style="table-layout:auto"}

### [!DNL Magento_Newsletter]

| 範本 | 設定路徑 |
|--- |--- |
| `Subscription Confirmation` | **頁面：** [!UICONTROL Customers] > [[!UICONTROL Newsletter]](../configuration-reference/customers/newsletter.md)<br/>**區段：** [!UICONTROL  Subscription Options]<br/>**欄位：** [!UICONTROL Confirmation Email Template] |
| `Subscription Success` | **頁面：** [!UICONTROL Customers] > [[!UICONTROL Newsletter]](../configuration-reference/customers/newsletter.md)<br/>**區段：** [!UICONTROL  Subscription Options]<br/>**欄位：** [!UICONTROL Success Email Template] |
| `Unsubscription Success` | **頁面：** [!UICONTROL Customers] > [[!UICONTROL Newsletter]](../configuration-reference/customers/newsletter.md)<br/>**區段：** [!UICONTROL  Subscription Options]<br/>**欄位：** [!UICONTROL Unsubscription Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_ProductAlert]

| 範本 | 設定路徑 |
|--- |--- |
| `Cron Error Warning` | **頁面：** [!UICONTROL Catalog] > [[!UICONTROL Catalog]](../configuration-reference/catalog/catalog.md)<br/>**區段：** [!UICONTROL Product Alerts Run Settings]<br/>**欄位：** [!UICONTROL Error Email Template] |
| `Price Alert` | **頁面：** [!UICONTROL Catalog] > [[!UICONTROL Catalog]](../configuration-reference/catalog/catalog.md)<br/>**區段：** [!UICONTROL Product Alerts]<br/>**欄位：** [!UICONTROL Price Alert Email Template] |
| `Stock Alert` | **頁面：** [!UICONTROL Catalog] > [[!UICONTROL Catalog]](../configuration-reference/catalog/catalog.md)<br/>**區段：** [!UICONTROL Product Alerts]<br/>**欄位：** [!UICONTROL Stock Alert Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_PurchaseOrder]

| 範本 | 設定路徑 |
|--- |--- |
| `Approved Purchase Order` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**區段：** [!UICONTROL Purchase Order Approval]<br/>**欄位：** [!UICONTROL Approved Purchase Order] |
| `Approved, requires payment` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**區段：** [!UICONTROL Purchase Order Approval]<br/>**欄位：** [!UICONTROL Approved, requires payment details (to Buyer)] |
| `Comment added to Purchase Order` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**區段：** [!UICONTROL Purchase Order Approval]<br/>**欄位：** [!UICONTROL Comment added to Purchase Order] |
| `Created and Auto-approved Purchase Order` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**區段：** [!UICONTROL Purchase Order Approval]<br/>**欄位：** [!UICONTROL Created and Automatically approved Purchase Order (to Buyer)] |
| `Created and automatically approved, requires payment details` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**區段：** [!UICONTROL Purchase Order Approval]<br/>**欄位：** [!UICONTROL Created and automatically approved, requires payment details (to Buyer)] |
| `Created and requires Approval Purchase Order` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**區段：** [!UICONTROL Purchase Order Approval]<br/>**欄位：** [!UICONTROL Created and requires Approval Purchase Order (to Buyer)] |
| `Error creating Order from Purchase Order` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**區段：** [!UICONTROL Purchase Order Approval]<br/>**欄位：** [!UICONTROL Error creating Order from Purchase Order (to Buyer)] |
| `Purchase Order requires Approval` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**區段：** [!UICONTROL Purchase Order Approval]<br/>**欄位：** [!UICONTROL Purchase Order requires Approval (to Approver)] |
| `Rejected Purchase Order` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**區段：** [!UICONTROL Purchase Order Approval]<br/>**欄位：** [!UICONTROL Rejected Purchase Order (to Buyer)] |

{style="table-layout:auto"}

### [!DNL Magento_Reminder]

![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)

| 範本 | 設定路徑 |
|--- |--- |
| `Promotion Notification/Reminder` | **頁面：** [!UICONTROL Customers] > [[!UICONTROL Promotions]](../configuration-reference/customers/promotions.md)<br/>**區段：** [!UICONTROL Automated Email Reminder Rules]<br/>**欄位：** [!UICONTROL Reminder Email Sender] |

{style="table-layout:auto"}

### [!DNL Magento_Reward]

![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)

| 範本 | 設定路徑 |
|--- |--- |
| `Balance Update` | **頁面：** [!UICONTROL Customers] > [[!UICONTROL Reward Points]](../configuration-reference/customers/reward-points.md)<br/>**區段：** [!UICONTROL Email Notification Settings]<br/>**欄位：** [!UICONTROL Balance Update Email] |
| `Points Expiry Warning` | **頁面：** [!UICONTROL Customers] > [[!UICONTROL Reward Points]](../configuration-reference/customers/reward-points.md)<br/>**區段：** [!UICONTROL Email Notification Settings]<br/>**欄位：** [!UICONTROL Reward Points Expiry Warning Email] |

{style="table-layout:auto"}

### [!DNL Magento_Rma]

![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)

| 範本 | 設定路徑 |
|--- |--- |
| `New RMA` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**區段：** [!UICONTROL  RMA]<br/>**欄位：** [!UICONTROL RMA Email Template] |
| `New RMA for Guest` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**區段：** [!UICONTROL  RMA]<br/>**欄位：** [!UICONTROL RMA Email Template for Guest] |
| `RMA Admin Comments` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**區段：** [!UICONTROL  RMA Admin Comments]<br/>**欄位：** [!UICONTROL RMA Comment Email Template] |
| `RMA Admin Comments for Guest` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**區段：** [!UICONTROL  RMA Admin Comments]<br/>**欄位：** [!UICONTROL RMA Comment Email Template for Guest] |
| `RMA Authorization` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**區段：** [!UICONTROL  RMA Authorization]<br/>**欄位：** [!UICONTROL RMA Authorization Email Template] |
| `RMA Authorization for Guest` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**區段：** [!UICONTROL  RMA Authorization]<br/>**欄位：** [!UICONTROL RMA Authorization Email Template for Guest] |
| `RMA Customer Comments` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**區段：** [!UICONTROL RMA Customer Comments]<br/>**欄位：** [!DNL RMA Comment Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_Sales]

| 範本 | 設定路徑 |
|--- |--- |
| `Credit Memo Update` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**區段：** [!UICONTROL Credit Memo Contents]<br/>**欄位：** [!UICONTROL Credit Memo Comment Email Template] |
| `Credit Memo Update (Magento/luma)` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**區段：** [!UICONTROL Credit Memo Comments]<br/>**欄位：** [!UICONTROL Credit Memo Comment Email Template] |
| `Credit Memo Update for Guest` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**區段：** [!UICONTROL Credit Memo Comments]<br/>**欄位：** [!UICONTROL Credit Memo Comment Email Template for Guest] |
| `Credit Memo Update for Guest (Magento/luma)` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**區段：** [!UICONTROL Credit Memo Comments]<br/>**欄位：** [!UICONTROL Credit Memo Comment Email Template for Guest] |
| `Invoice Update` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/../configuration-reference/sales/sales-emails.md)<br/>**區段：** [!UICONTROL Invoice Comments]<br/>**欄位：** [!UICONTROL Invoice Comment Email Template] |
| `Invoice Update (Magento/luma)` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**區段：** [!UICONTROL Invoice Comments]<br/>**欄位：** [!UICONTROL Invoice Comment Email Template] |
| `Invoice Update for Guest` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**區段：** [!UICONTROL Invoice Comments]<br/>**欄位：** [!UICONTROL Invoice Comment Email Template for Guest] |
| `Invoice Update for Guest (Magento/luma)` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**區段：** [!UICONTROL Invoice Comments]<br/>**欄位：** [!UICONTROL Invoice Comment Email Template for Guest] |
| `New Credit Memo` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**區段：** [!UICONTROL Credit Memo]<br/>**欄位：** [!UICONTROL Credit Memo Email Template] |
| `New Credit Memo (Magento/luma)` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]]../configuration-reference/sales/sales-emails.md)<br/>**區段：** [!UICONTROL Credit Memo]<br/>**欄位：** [!UICONTROL Credit Memo Email Template] |
| `New Credit Memo for Guest` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**區段：** [!UICONTROL Credit Memo]<br/>**欄位：** [!UICONTROL Credit Memo Email Template for Guest] |
| `New Credit Memo for Guest (Magento/luma)` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**區段：** [!UICONTROL Credit Memo]<br/>**欄位：** [!UICONTROL Credit Memo Email Template for Guest] |
| `New Invoice` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**區段：** [!UICONTROL Invoice]<br/>**欄位：** [!UICONTROL Invoice Email Template] |
| `New Invoice (Magento/luma)` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**區段：** [!UICONTROL Invoice]<br/>**欄位：** [!UICONTROL Invoice Email Template] |
| `New Invoice for Guest` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**區段：** [!UICONTROL Invoice]<br/>**欄位：** [!UICONTROL Invoice Email Template for Guest] |
| `New Invoice for Guest (Magento/luma)` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**區段：** [!UICONTROL Invoice]<br/>**欄位：** [!UICONTROL Invoice Email Template for Guest] |
| `New Order` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**區段：** [!UICONTROL Order]<br/>**欄位：** [!UICONTROL New Order Confirmation Template] |
| `New Order (Magento/luma)` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**區段：** [!UICONTROL Order]<br/>**欄位：** [!UICONTROL New Order Confirmation Template] |
| `New Order for Guest` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**區段：** [!UICONTROL Order]<br/>**欄位：** [!UICONTROL New Order Confirmation Template for Guest] |
| `New Order for Guest (Magento/luma)` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**區段：** [!UICONTROL Order]<br/>**欄位：** [!UICONTROL New Order Confirmation Template for Guest] |
| `New Shipment` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**區段：** [!UICONTROL Shipment]<br/>**欄位：** [!UICONTROL Shipment Email Template] |
| `New Shipment (Magento/luma)` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**區段：** [!UICONTROL Shipment]<br/>**欄位：** [!UICONTROL Shipment Email Template] |
| `New Shipment for Guest` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**區段：** [!UICONTROL Shipment]<br/>**欄位：** [!UICONTROL Shipment Email Template for Guest] |
| `New Shipment for Guest (Magento/luma)` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**區段：** [!UICONTROL Shipment]<br/>**欄位：** [!UICONTROL Shipment Email Template for Guest] |
| `Order Update` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**區段：** [!UICONTROL Order Comments]<br/>**欄位：** [!UICONTROL Order Comment Email Template] |
| `Order Update (Magento/luma)` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**區段：** [!UICONTROL Order Comments]<br/>**欄位：** [!UICONTROL Order Comment Email Template] |
| `Order Update for Guest` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**區段：** [!UICONTROL Order Comments]<br/>**欄位：** [!UICONTROL Order Comment Email Template for Guest] |
| `Order Update for Guest (Magento/luma)` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**區段：** [!UICONTROL Order Comments]<br/>**欄位：** [!UICONTROL Order Comment Email Template for Guest] |
| `Shipment Update` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**區段：** [!UICONTROL Shipment Comments]<br/>**欄位：** [!UICONTROL Shipment Comment Email Template] |
| `Shipment Update (Magento/luma)` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**區段：** [!UICONTROL Shipment Comments]<br/>**欄位：** [!UICONTROL Shipment Comment Email Template] |
| `Shipment Update for Guest` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**區段：** [!UICONTROL Shipment Comments]<br/>**欄位：** [!UICONTROL Shipment Comment Email Template for Guest] |
| `Shipment Update for Guest (Magento/luma)` | **頁面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**區段：** [!UICONTROL Shipment Comments]<br/>**欄位：** [!UICONTROL Shipment Comment Email Template for Guest] |

{style="table-layout:auto"}

### [!DNL Magento_ScheduledImportExport]

![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)

| 範本 | 設定路徑 |
|--- |--- |
| `Export Failed` | **頁面：** [!UICONTROL Advanced] > [[!UICONTROL System]](../configuration-reference/advanced/system.md)<br/>**區段：** [!UICONTROL Scheduled Import/Export File History Cleaning]<br/>**欄位：** [!UICONTROL Export Failed Template] |
| `File History Clean Failed` | **頁面：** [!UICONTROL Advanced] > [[!UICONTROL System]](../configuration-reference/advanced/system.md)<br/>**區段：** [!UICONTROL Scheduled Import/Export File History Cleaning]<br/>**欄位：** [!UICONTROL Error Email Template] |
| `Import Failed` | **頁面：** [!UICONTROL Advanced] > [[!UICONTROL System]](../configuration-reference/advanced/system.md)<br/>**區段：** [!UICONTROL Scheduled Import/Export File History Cleaning]<br/>**欄位：** [!UICONTROL Import Failed Template] |

{style="table-layout:auto"}

### [!DNL Magento_SendFriend]

| 範本 | 設定路徑 |
|--- |--- |
| `Send Product Link to Friend` | **頁面：** [!UICONTROL Catalog] > [[!UICONTROL Email to a Friend]](../configuration-reference/catalog/email-to-a-friend.md)<br/>**區段：** [!UICONTROL Email Templates]<br/>**欄位：** [!UICONTROL Select Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_Sitemap]

| 範本 | 設定路徑 |
|--- |--- |
| `Sitemap Generation Settings` | **頁面：** [!UICONTROL Catalog] > [[!UICONTROL XML Sitemap]](../configuration-reference/catalog/xml-sitemap.md)<br/>**區段：** [!UICONTROL Generation Settings]<br/>**欄位：** [!UICONTROL Error Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_TwoFactorAuth]

| 範本 | 設定路徑 |
|--- |--- |
| `2FA Configuration Required by User` | 不適用 |
| `2FA Configuration Required for the Application` | 不適用 |

{style="table-layout:auto"}

### [!DNL Magento_User]

| 範本 | 設定路徑 |
|--- |--- |
| `Forgot Admin Password` | **頁面：** [!UICONTROL Advanced] > [[!UICONTROL Admin]](../configuration-reference/advanced/admin.md)<br/>**區段：** [!UICONTROL Admin User Emails]<br/>**欄位：** 忘記密碼電子郵件範本 |
| `User Notification` | **頁面：** [!UICONTROL Advanced] > [[!UICONTROL Admin]](../configuration-reference/advanced/admin.md)<br/>**區段：** [!UICONTROL Admin User Emails]<br/>**欄位：** 使用者通知範本 |
| `New User Notification` | **頁面：** [!UICONTROL Advanced] > [[!UICONTROL Admin]](../configuration-reference/advanced/admin.md)<br/>**區段：** [!UICONTROL Admin User Emails]<br/>**欄位：** [!UICONTROL New User Notification Template] |

{style="table-layout:auto"}

### [!DNL Magento_Wishlist]

| 範本 | 設定路徑 |
|--- |--- |
| `Magento Wish List Sharing` | **頁面：** [!UICONTROL Customers] > [[!UICONTROL Wish List]](../configuration-reference/customers/wishlist.md)<br/>**區段：** [!UICONTROL Share Options]<br/>**欄位：** [!UICONTROL Email Template] |

{style="table-layout:auto"}
