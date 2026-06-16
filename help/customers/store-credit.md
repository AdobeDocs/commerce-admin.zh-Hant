---
title: 商店點數
description: 商店貸方是還原至客戶帳戶的金額，可用於支付購買或現金退款。
exl-id: 1fe627dd-5c49-4ff8-85e0-3c987285726d
feature: Customers, Storefront
TQID: https://experienceleague.adobe.com/kG-y-O2Yh-h1ct-oCwqylZFvS2FOCXFPD6qVIkKrpbg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 291
ht-degree: 0%

---

# 商店點數

{{ee-feature}}

商店貸方是還原至客戶帳戶的金額。 客戶可以使用商店積分支付購買費用，管理員可以使用商店積分支付現金退款。 禮品卡餘額可貸記至客戶帳戶，而非使用禮品卡代碼進行未來購買。

訂單付款並開立商業發票後，[簽發銷退折讓單](../stores-purchase/credit-memo-create.md)即可退款或部份訂單。 銷退折讓單與退款不同，因為銷退折讓的金額會還原至客戶帳戶，以便用於未來採購。 有時候，在發出銷退折讓單的同時，也會提供退款，並套用至客戶的商店銷退折讓餘額。 客戶帳戶中可用的商店貸方金額會在設定中指定。

>[!NOTE]
>
>必須啟用&#x200B;[_零小計結帳_](../stores-purchase/zero-subtotal-checkout.md)&#x200B;付款方式，以儲存點數涵蓋訂單總額。

## 儲存信用工作流程

1. **客戶登入** — 客戶在開始結帳程式之前登入帳戶。

1. **使用商店** — 信用在結帳程式的&#x200B;[!UICONTROL _檢閱與付款_]&#x200B;步驟中，客戶選取&#x200B;[!UICONTROL _使用商店信用額度_]&#x200B;作為付款選項。 可用餘額會顯示在括弧中。 如果可用餘額大於總計，則不再顯示其他付款方法。

1. **套用至訂單**&#x200B;的銷退折讓金額 — 套用至訂單的商店銷退折讓金額會與訂單總計一起顯示，並從總計中扣除。

1. **已調整客戶餘額** — 在下單時調整客戶的可用餘額。
