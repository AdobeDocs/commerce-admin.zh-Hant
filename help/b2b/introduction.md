---
title: 簡介 [!DNL B2B for Adobe Commerce]
description: 瞭解如何使用整合式B2B功能，滿足貴公司客戶的需求。
exl-id: fc7e8147-5fd5-4e4b-b16e-0b0d54c415da
feature: B2B
source-git-commit: fb075822e318073053cdf8cdd5cd9bb3a6343904
workflow-type: tm+mt
source-wordcount: '815'
ht-degree: 0%

---

# 簡介 [!DNL B2B for Adobe Commerce]

與標準的企業對消費者模式不同，整合式B2B （企業對企業）功能是專為符合擁有企業客戶的賣家(Adobe Commerce商家)需求而設計。 它可容納組織結構複雜的公司，以及擁有各種角色和購買許可權等級的多個使用者。 典型的B2B客戶可能是零售商店的經理，或代表公司進行購買的買家。 在這兩種情況下，交易都會在您的企業與其企業之間進行。 您也可以將產品直接銷售給消費者。 [!DNL B2B for Adobe Commerce] 是整合式解決方案，可支援B2B和B2C模型。

使用 [安裝](install.md) 和 [啟用](enable-basic-features.md) 在您的Adobe Commerce商店中使用B2B擴充功能，可以透過客戶特定的目錄和定價，以及目標式內容和促銷活動，提供個人化的購買體驗。

## 公司帳戶

Company帳戶元件是B2B內的主要實體，所有其他功能在某種程度上都與其相依。 它允許將屬於單一公司的多個買家加入單一公司帳戶（或公司帳戶）。 公司管理員可以建立公司結構（部門、子部門和使用者），以反映公司的運作模式，並為公司成員提供不同的使用者角色和許可權。 此結構可讓公司管理員控制公司帳戶的使用者活動：訂購、報價、購買、存取公司信用資訊或設定檔等。

從管理員那裡，Commerce網站管理員可以設定公司在網站上運作的方式。 組態決定可供公司使用者使用的B2B功能，包括付款方式、訂價層次、使用報價議價的能力、建立請購單清單的能力等等。

如需詳細資訊，請參閱 [公司帳戶](account-companies.md).

>[!NOTE]
>
>啟用後，您的商店可以為公司提供以下選項 _分期付款帳戶_，表示購買公司信用額度。 身為商家，您可以為公司帳戶配置銷退折讓並管理公司的銷退折讓設定以及銷退折讓補助。

## 公司管理

[!BADGE 1.5.0測試版]{type=Informative url="/help/b2b/release-notes.md" tooltip="僅供測試版計畫參與者使用"}

公司管理可協助商家管理員簡化具有複雜營運模型的B2B組織的行政管理。

具有適當許可權的使用者可以從管理員建立 **[!UICONTROL Company Hierarchy]** 這反映了由多家公司組成的企業組織結構。 此階層可以讓使用者以群組的形式檢視和管理公司。 例如，管理員可指定母公司，並指派所有作為母公司的子公司運作的公司。 然後，母公司管理員可以檢視和管理所有指定公司的公司帳戶。

如需詳細資訊，請參閱 [公司管理](manage-companies.md).

## Adobe Commerce 服務

Adobe Commerce服務是託管服務，可為Adobe Commerce和Magento Open Source提供延伸功能。 支援B2B工作流程的服務包括：

* [目錄服務](https://experienceleague.adobe.com/docs/commerce-merchant-services/catalog-service/guide-overview.html)
* [即時搜尋](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/guide-overview.html)
* [產品Recommendations](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html)

## 共用目錄

共用目錄是訂價層級，可在一或多個網站上為不同公司設定每個產品的自訂價格。 透過使用共用目錄，您可以針對不同的客戶群組套用不同的定價層級來銷售產品。 共用目錄支援僅適用於設定為支援公司帳戶的Commerce存放區。

如需詳細資訊，請參閱 [使用共用目錄](catalog-shared.md).

## 快速訂購

設定快速訂購，讓登入的客戶在知道要訂購的產品名稱或SKU時，減少訂單處理為幾次點按。

如需詳細資訊，請參閱 [快速訂購](quick-order.md).

## 可協商的報價

使用「報價單」功能，啟動公司買方與賣方之間的價格議價。

* 授權購買者可以從購物車中啟動報價。

* 賣家可以向Admin為買家啟動報價。

買方和賣方使用報價單來管理議價流程（例如新增料號、更新數量、要求及套用折扣），直到達成協定為止。 此 _引號_ 「管理員」中的網格會列出收到的每一份報價，並維護買賣雙方之間的通訊記錄。

只有設定為支援公司帳戶的Commerce商店才支援可協商的報價。

如需詳細資訊，請參閱 [可協商的報價](quotes.md).

## 採購單核准

為公司帳戶啟動採購單時，所有訂單都會自動建立為採購單(PO)。 具有必要許可權的公司使用者可以建立、編輯和刪除他們建立的採購單，以及下屬使用者建立的採購單。 根據其角色和順序，公司使用者可能需要遵守數個核准規則。

如需詳細資訊，請參閱 [公司的採購單](purchase-order-flow.md).

## 請購單清單

客戶可在購買經常訂購的產品時，使用請購單清單來節省時間，因為他們可以直接從清單新增專案至購物車。 他們可以維護多個清單，專注於來自不同廠商、購買者、團隊、行銷活動的產品，或簡化其工作流程的任何其他產品。

如需詳細資訊，請參閱 [請購單清單](requisition-lists.md).
