---
title: PSD2合規性
description: 瞭解可能影響商店的支付服務指示(PSD2)的要求。
exl-id: efe94cac-a170-48df-88cf-36019ca52951
feature: Compliance
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# PSD2合規性

自2019年9月14日起，歐盟要求歐盟和英國的所有商戶遵守支付服務指示(PSD2)的[強式客戶驗證](https://www.cardinalcommerce.com/content-hub/mandates/psd2-sca/understanding-psd2-sca) (SCA)要求。 我們鼓勵其他國家的商戶遵循PSD2作為最佳實務。

>[!NOTE]
>
>本主題僅供參考，不應理解為法律建議。 若要確定您的企業是否及如何遵守任何法律義務，請諮詢您的法律顧問。

強大的客戶驗證是PSD2的關鍵元件，而且需要下列兩項作業：

- 只有客戶才有的東西（密碼或PIN）
- 只有客戶才知道的事情（由電話或金鑰庫產生的唯一安全性權杖）
- 只有客戶才有的功能（生物測定驗證，例如指紋或臉部辨識）

歐洲銀行可能會拒絕不符合要求的付款。 不過，系統仍可能接受低風險和低價值交易，以及循環訂閱中的後續付款。

由於這項重大變更，並且為了確保客戶付款不會被拒絕，Adobe針對原生[!DNL Commerce]付款整合引進了下列變更和建議。

| 付款方法 | 合規性要求 |
|--- |--- |
| [PayPal](../stores-purchase/paypal.md) | 對於大多數PayPal解決方案，因為需求是由PayPal處理，所以不需要採取任何動作來遵守PSD2。 如需特定解決方案的相關資訊，請參閱每個PayPal主題頂端的注意事項。 |
| [Braintree](../stores-purchase/braintree.md) | 從2.4.0中轉換至已安裝的擴充功能開始，需求會在隨附的「Braintree付款」模組內處理，且無需採取任何動作即可遵守PSD2。 <br /><br />**_注意：_**若要在舊版中使用核心整合來遵守PSD2，請執行下列其中一個動作：<br/>- （建議）從[[!DNL Adobe Commerce Marketplace]](https://marketplace.magento.com/catalogsearch/result/?q=braintree#q=braintree&amp;idx=m2_cloud_prod_default_products&amp;p=0&amp;nR%5Bvisibility_search%5D%5B%3D%5D%5B0%5D=1)安裝正式Braintree付款整合延伸模組{：target=&quot;_blank&quot;}。<br/> — 在[!DNL Commerce]設定中啟用並設定Braintree付款方法。<br/><br/>這些舊版核心整合支援3D Secure 2.0驗證。 不過，在JavaScript SDK v2上執行的Braintree實作不支援3D Secure 2.0。 |
| 其他 | 若為所有其他的付款整合，請檢查[[!DNL Commerce Marketplace]](https://marketplace.magento.com/extensions/payments-security/payment-integration.html?_ga=2.108129217.2105547619.1564067043-238341041.1564067043){：target=&quot;_blank&quot;}上可用的副檔名。 請要求您的付款提供者推薦支援PSD2需求的解決方案。 |

{style="table-layout:auto"}
