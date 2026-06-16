---
title: PSD2合規性
description: 瞭解可能影響商店的支付服務指示(PSD2)的要求。
exl-id: efe94cac-a170-48df-88cf-36019ca52951
feature: Compliance
TQID: https://experienceleague.adobe.com/paVa-tpYYzrINAPRFs4TOzbp4b4CLJDlxqNlL1gzp2Q
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: b5f00040-57a0-4a6d-a39e-383b1936c2c9
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: c32adafa-ed01-4b31-997e-2413013911b0
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: f0ca7b10-ef6c-4ee4-b63f-030819bdd1f3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 396
ht-degree: 0%

---

# PSD2合規性

自2019年9月14日起，歐盟要求歐盟和英國的所有商戶遵守支付服務指示(PSD2)的[強式客戶驗證](https://www.cardinalcommerce.com/content-hub/mandates/psd2-sca/understanding-psd2-sca) (SCA)要求。 其他國家或地區的商戶建議遵循PSD2作為最佳實務。

>[!NOTE]
>
>本主題僅供參考，不應理解為法律建議。 若要確定您的企業是否及如何遵守任何法律義務，請諮詢您的法律顧問。

強大的客戶驗證是PSD2的關鍵元件，並需要下列兩項作業：

- 只有客戶才有的東西（密碼或PIN）
- 只有客戶才知道的事情（由電話或金鑰庫產生的唯一安全性權杖）
- 只有客戶才有的功能（生物測定驗證，例如指紋或臉部辨識）

歐洲銀行可能會拒絕不符合要求的付款。 不過，系統仍可能接受低風險和低價值交易，以及循環訂閱中的後續付款。

由於這項重大變更，並且為了確保不會拒絕客戶付款，Adobe針對原生[!DNL Commerce]付款整合推出了下列變更和建議。

| 付款方法 | 合規性要求 |
|--- |--- |
| [PayPal](../stores-purchase/paypal.md) | 大部分的PayPal解決方案不需採取任何動作即可遵守PSD2，因為需求是由PayPal處理。 如需特定解決方案的相關資訊，請參閱每個PayPal主題頂端的注意事項。 |
| [Braintree](../stores-purchase/braintree.md) | 從2.4.0版已安裝的擴充功能轉換開始，需求會在隨附的Braintree支付模組內處理，遵循PSD2無需任何動作。 <br /><br />**_Note:_**&#x200B;為了遵循PSD2，在舊版中使用核心整合，請執行下列其中一個動作：<br/>- （建議）從[[!DNL Adobe Commerce Marketplace]](https://marketplace.magento.com/catalogsearch/result/?q=braintree#q=braintree&idx=m2_cloud_prod_default_products&p=0&nR%5Bvisibility_search%5D%5B%3D%5D%5B0%5D=1){:target="_blank"}安裝正式的Braintree付款整合延伸模組。<br/> — 在[!DNL Commerce]設定中啟用並設定Braintree付款方法。<br/><br/>這些舊版核心整合支援3D Secure 2.0驗證。 不過，在JavaScript SDK v2上執行的Braintree實作不支援3D Secure 2.0。 |
| 其他 | 對於所有其他的付款整合，請檢查[[!DNL Commerce Marketplace]](https://marketplace.magento.com/extensions/payments-security/payment-integration.html?_ga=2.108129217.2105547619.1564067043-238341041.1564067043){:target="_blank"}上可用的副檔名。 請要求您的付款提供者推薦支援PSD2需求的解決方案。 |

{style="table-layout:auto"}
