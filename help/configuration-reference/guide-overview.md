---
title: 設定參考指南
description: 檢閱按設定索引標籤、頁面和區段整理的所有Commerce管理員商店設定之描述性資訊。
exl-id: b0359ba4-3643-4355-9154-adfedb369ec3
source-git-commit: 323ea635286fcb9a2bcc7f4f56b32c1518a7beef
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# 設定參考指南

本指南適用於在Adobe Commerce或Magento Open Source中工作的商家和系統管理員。 它提供所有存放區組態設定的參考資訊，這些設定可從&#x200B;_Admin_&#x200B;側邊欄（位於&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**）存取。

它不涵蓋Adobe Commerce功能的詳細資訊以及存放區設定的Magento Open Source或程式。

本指南是根據設定左側導覽來整理：

| 設定索引標籤 | 子索引標籤 |
| ----------------- | ---------- |
| **[!UICONTROL General]** <br/><br/> _[!UICONTROL General]_組態區段決定存放區引數、URL、主題、貨幣、電子郵件地址、存放區連絡人、編輯器和儀表板報告。 | - [[!UICONTROL General]](./general/general.md)<br>- [[!UICONTROL B2B Features]](./general/b2b-features.md)<br>- [[!UICONTROL Web]](./general/web.md)<br>- [[!UICONTROL Currency Setup]](./general/currency-setup.md)<br>- [[!UICONTROL Store Email Addresses]](./general/store-email-addresses.md)<br>- [[!UICONTROL Contacts]](./general/contacts.md)<br>- [[!UICONTROL Reports]](./general/reports.md)<br>- [[!UICONTROL Content Management]](./general/content-management.md)<br>- [[!UICONTROL New Relic Reporting]](./general/new-relic-reporting.md)<br>- [[!UICONTROL Advanced Reporting]](./general/advanced-reporting.md) |
| **[!UICONTROL Catalog]** <br/><br/> _[!UICONTROL Catalog]_組態設定會決定產品與詳細目錄設定、控制Sitemap與RSS摘要的產生，並指定用來與朋友共用產品的電子郵件範本。 | - [[!UICONTROL Catalog]](./catalog/catalog.md)<br>- [[!UICONTROL Visual Merchandiser]](./catalog/visual-merchandiser.md)<br>- [[!UICONTROL Inventory]](./catalog/inventory.md)<br>- [[!UICONTROL XML Sitemap]](./catalog/xml-sitemap.md)<br>- [[!UICONTROL RSS Feeds]](./catalog/rss-feeds.md)<br>- [[!UICONTROL Email to a Friend]](./catalog/email-to-a-friend.md) |
| **[!UICONTROL Security]** <br/><br/> _[!UICONTROL Security]_組態設定會控制存放區安全性、雙因素驗證，以及Google reCAPTCHA功能。 | - [[!UICONTROL 2FA]](./security/2fa.md)<br>- [[!UICONTROL Google reCAPTCHA Admin Panel]](./security/google-recaptcha-admin.md)<br>- [[!UICONTROL Google reCAPTCHA Storefront]](./security/google-recaptcha-storefront.md)<br>- [[!UICONTROL Security.txt]](./security/security-txt.md) |
| **[!UICONTROL Customers]** <br/><br/> _[!UICONTROL Customers]_組態設定會建立基本客戶帳戶與登入選項、電子報設定、希望清單，以及自動產生優惠券代碼的格式。 | - [[!UICONTROL Login as Customer]](./customers/login-as-customer.md)<br>- [[!UICONTROL Newsletter]](./customers/newsletter.md)<br>- [[!UICONTROL Company Configuration]](./customers/company-configuration.md)<br>- [[!UICONTROL Customer Configuration]](./customers/customer-configuration.md)<br>- [[!UICONTROL Requisition Lists]](./customers/requisition-lists.md)<br>- [[!UICONTROL Wish List]](./customers/wishlist.md)<br>- [[!UICONTROL Invitations]](./customers/invitations.md)<br>- [[!UICONTROL Reward Points]](./customers/reward-points.md)<br>- [[!UICONTROL Promotions]](./customers/promotions.md)<br>- [[!UICONTROL Gift Registry]](./customers/gift-registry.md)<br>- [[!UICONTROL Persistent Shopping Cart]](./customers/persistent-shopping-cart.md) |
| **[!UICONTROL Sales]** <br/><br/> _[!UICONTROL Sales]_組態設定決定結帳與稅務設定、付款與運送選項、銷售電子郵件與PDF列印輸出，以及Google API設定。 | - [[!UICONTROL Sales]](./sales/sales.md)<br>- [[!UICONTROL Sales Emails]](./sales/sales-emails.md)<br>- [[!UICONTROL Quotes]](./sales/quotes.md)<br>- [[!UICONTROL PDF Print-outs]](./sales/pdf-print-outs.md)<br>- [[!UICONTROL Tax]](./sales/tax.md)<br>- [[!UICONTROL Checkout]](./sales/checkout.md)<br>- [[!UICONTROL Shipping Settings]](./sales/shipping-settings.md)<br>- [[!UICONTROL Multishipping Settings]](./sales/multishipping-settings.md)<br>- [[!UICONTROL Delivery Methods]](./sales/delivery-methods.md)<br>- [[!UICONTROL Google API]](./sales/google-api.md)<br>- [[!UICONTROL 3D Secure]](./sales/3d-secure.md)<br>- [[!UICONTROL Gift Cards]](./sales/gift-cards.md)<br>- [[!UICONTROL Payment Methods]](./sales/payment-methods.md) |
| **[!UICONTROL Sales Channels]** <br/><br/>安裝[!DNL Amazon Sales Channel]擴充功能時，_[!UICONTROL Sales Channels]_設定會控制與Amazon市集的自動化整合作業。 | - [[!UICONTROL Global Settings]](sales-channels.md) |
| **[!UICONTROL Services]** <br/><br/> _[!UICONTROL Services]_組態設定決定Commerce API整合設定，包括SOAP和OAuth。 | - [[!UICONTROL Web API]](./services/magento-web-api.md)<br>- [[!UICONTROL Commerce Services]](./services/saas.md)<br>- [[!UICONTROL OAuth]](./services/oauth.md) |
| **[!UICONTROL Advanced]** <br/><br/> _[!UICONTROL Advanced]_組態設定決定預設管理員設定、各種系統組態設定、進階模組控制項以及開發人員工具。 | - [[!UICONTROL Admin]](./advanced/admin.md)<br>- [[!UICONTROL System]](./advanced/system.md)<br>- [[!UICONTROL Developer]](./advanced/developer.md) |

{style="table-layout:auto"}

它不涵蓋Adobe Commerce功能的詳細資訊以及存放區設定的Magento Open Source或程式。

## 可用檔案

{{docs-links}}
