---
title: 『[!UICONTROL General] &gt； [!UICONTROL B2B Features]『
description: 檢閱上的組態設定 [!UICONTROL General] &gt； [!UICONTROL B2B Features] 商務管理員頁面。
exl-id: fc07a067-b92a-49c7-8512-2dfcc1c6ba0c
feature: Configuration, B2B
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 4%

---

# [!UICONTROL General] > [!UICONTROL B2B Features]

{{b2b-feature}}

{{config}}

>[!TIP]
>
>安裝及啟用Adobe Commerce適用的B2B後，即可使用公司專屬的功能提供個人化的購買體驗。 Adobe Commerce適用的B2B是整合式解決方案，可支援B2B和B2C模型。 如需B2B功能的詳細資訊，請參閱 [_Adobe Commerce適用的B2B使用指南_](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).

## [!UICONTROL B2B Features]

![B2B功能](./assets/b2b-features.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [[!UICONTROL Enable Company]](../../b2b/account-companies.md) | 網站 | 啟用後，可讓客戶從其帳戶儀表板管理其公司指派，並依預設啟用「共用目錄」和「B2B報價」功能。 選項： `Yes` / `No` |
| [[!UICONTROL Enable Quick Order]](../../b2b/quick-order.md) | 網站 | 啟用後，可讓客戶和來賓根據SKU或產品名稱快速下訂單。 選項： `Yes` / `No` |
| [[!UICONTROL Enable Requisition List]](../../b2b/configure-requisition-lists.md) | 網站 | 啟用後，可讓客戶從其帳戶儀表板建立和管理請購單清單。 |

{:style=&quot;table-layout:auto&quot;}

![啟用公司和共用目錄的B2B功能](./assets/b2b-features-company-enabled.png)<!-- zoom -->

啟用「公司」功能時，其他欄位可用於「共用目錄」和「B2B報價」。

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--------------------------------------------------------------------|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [[!UICONTROL Enable Shared Catalog]](../../b2b/catalog-shared.md) | 網站 | 啟用後，即可使用自訂定價建立組織目錄，這些目錄可在全球範圍內使用，或僅限特定公司使用。 選項： `Yes` / `No` |
| [!UICONTROL Enable Shared Catalog direct products price assigning] | 網站 | 當 _[!UICONTROL Enable Shared Catalog]_欄位已設為 `Yes`，此選項可供使用。 啟用時，只有指派給共用目錄的產品才會儲存在價格索引中。 未指派給共用目錄的產品不會顯示在店面上。 選項： `Yes` / `No` |
| [[!UICONTROL Enable B2B Quote]](../../b2b/configure-quotes.md) | 網站 | 啟用後，可讓公司買家從購物車提交詢價。 選項： `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

### [!UICONTROL Default B2B Payment Methods]

![B2B設定 — 預設付款方式設定](./assets/b2b-features-default-payment-methods.png)<!-- zoom -->

|[!UICONTROL Applicable Payment Methods]|全域|決定B2B買家可用的付款方式選擇。 選項： `All Payment Methods` / `Specific Payment Methods`| |[!UICONTROL Payment Methods]|全域|指定B2B購買者可用的各種付款方式。|

{:style=&quot;table-layout:auto&quot;}

### [!UICONTROL Default B2B Shipping Methods]

![B2B設定 — 預設送貨方法](./assets/b2b-features-shipping-methods.png)<!-- zoom -->

|[!UICONTROL Applicable Shipping Methods]|全域|決定預設可供B2B購買者使用的送貨方式選項。 選項： `All Shipping Methods` / `Specific Shipping Methods`| |[!UICONTROL Shipping Methods]|全域|指定B2B購買者預設可用的各種送貨方法。 <br/>**_注意：_**您也可以限制特定產品的送貨方法 [公司帳戶](../../b2b/account-companies.md).|

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Order Approval Configuration]

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [[!UICONTROL Enable Purchase Orders]](../../stores-purchase/purchase-order.md) | 網站 | 啟用時，可讓公司建立採購單。 選項： `Yes` / `No` |

![B2B功能 — 訂單核准設定](./assets/b2b-features-order-approval.png)<!-- zoom -->

{:style=&quot;table-layout:auto&quot;}
