---
title: 稅金
description: 瞭解如何設定您的商店，以根據地區設定的要求計算稅捐。
exl-id: bf807132-416f-497a-82c4-b00dba4d3092
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1100'
ht-degree: 0%

---

# 稅金

設定您的商店，以根據地區設定的要求計算稅捐。 您可以為產品與客戶群組設定[稅捐類別](tax-class.md)，並建立結合產品與客戶類別、稅捐地區與稅率的[稅捐規則](tax-rules.md)。 Commerce也提供固定產品稅捐、複合稅捐的組態設定，以及跨國境價格的顯示。 如果您必須收取[增值稅](vat.md)，您可以將商店設定為自動計算適當金額並進行驗證。

>[!NOTE]
>
>Adobe Commerce和Magento Open Source版本2.4.0到2.4.3包含Vertex廠商開發的擴充功能，用於與Vertex Cloud整合，以提供稅務管理和位址清理。 從2.4.4版開始，此擴充功能不再與核心版本搭配，必須從Commerce Marketplace或直接從供應商安裝及更新。 [連絡頂點](https://marketplace.magento.com/partner/vertex_inc)以取得擴充功能與檔案的相關資訊。<br><br>
>
>如果您已啟用並設定隨附的擴充功能，則必須在2.4.4升級程式中更新composer.json檔案，並管理後續的擴充功能更新。 請參閱&#x200B;_升級指南_&#x200B;中的[升級模組](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html)。

## 快速參考

有些稅捐設定有選項可供選擇，以決定計算稅捐及向客戶呈現稅捐的方式。 如需詳細資訊，請參閱[國際稅務准則](international-tax-guidelines.md)。

設定稅捐計算設定時，請參考下清單格：

### 稅捐計算方法

稅捐計算方法選項包括[!UICONTROL Unit Price]、[!UICONTROL Row Total]和[!UICONTROL Total]。 下表說明如何針對不同的設定處理舍入（至兩位數）。

| 設定 | 計算與顯示 |
|--- |--- |
| [!UICONTROL Unit Price] | Commerce會計算每個專案的稅捐，並顯示含稅價格。 若要計算稅捐總計，它會舍入每個專案的稅捐，然後將它們相加。 |
| [!UICONTROL Row Total] | Commerce會計算各明細行的稅捐。 若要計算稅捐總計，它會舍入每個明細行專案的稅捐，然後將它們相加。 |
| [!UICONTROL Total] | Commerce會計算每個專案的稅捐，並加總這些稅捐值，以計算訂單的未舍入稅捐總額。 然後，它會將指定的舍入模式套用至稅捐總計，以決定訂單的稅捐總計。 |

{style="table-layout:auto"}

### 含稅或不含稅的型錄價格

可能的顯示欄位會依計算方法，以及型錄價格是否包含或排除稅捐而有所不同。 顯示欄位在一般計算中具有小數點兩位數的精確度。 某些價格設定組合會顯示包含與排除稅捐的價格。 當兩者出現在相同的條列專案上時，可能會讓客戶感到困惑，並觸發[警告](taxes.md#warning-messages)。

| 設定 | 計算與顯示 |
|--- |--- |
| [!UICONTROL Excluding Tax] | 使用此設定時，會使用輸入的基準料號價格，並套用稅捐計算方法。 |
| [!UICONTROL IncludingTax] | 使用此設定時，會先計算不含稅捐的基本料號價格。 此值會作為基本價格，並套用稅捐計算方法。 |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>對於在數個國家（地區）擁有多種商店檢視的歐盟商戶或其他加值稅商戶而言，其顯示價格（包括稅捐）與營運的較舊版本有所變更。 如果您以兩位數的精確度載入價格，Commerce會自動將所有價格四捨五入為兩位數，以確保向買家呈現一致的價格。

### 含稅或不含稅的運費

| 設定 | 顯示 | 計算 |
|--- |--- |--- |
| [!UICONTROL Excluding Tax] | 顯示時不含稅金。 | 正常計算。 送貨會新增至購物車總價，通常會顯示為個別專案。 |
| [!UICONTROL Including Tax] | 可含稅，或可個別顯示稅捐。 | 使用相同的計算，將送貨視為購物車中含稅的其他專案。 |

{style="table-layout:auto"}

### 明細行專案的稅捐金額

若要將兩個不同的稅捐金額顯示為個別的明細行專案，例如加拿大商店的GST與PST，您必須為相關稅捐規則設定不同的優先順序。 不過，在先前的稅捐計算中，不同優先順序的稅捐會自動進行複合。 若要正確顯示個別的稅捐金額，且稅捐金額的複合方式不正確，您可以設定不同的優先順序，也可以選取&#x200B;_僅計算小計_&#x200B;核取方塊。 此設定會產生正確計算的稅捐金額，顯示為個別的明細行專案。

## 警告訊息

某些稅捐相關選項的組合可能會讓客戶感到困惑，並觸發警告。 當稅捐計算方法設為`Row`或`Total`，且客戶收到不含稅和含稅的價格時，可能會發生這些狀況。 當購物車中有針對每個專案的稅捐時，也可能發生這種情況。 由於稅捐計算已四捨五入，因此出現在購物車中的金額可能會與客戶預期支付的金額不同。

如果您的稅捐計算是以有問題的組態為基礎，則會出現下列警告：

![驚歎號](../assets/icon-warning.png) **警告**。`Tax discount configuration might result in different discounts than a customer might expect for store(s); Europe Website (French), Europe Website (German). Please see source for more details.`

![驚歎號](../assets/icon-warning.png) **警告**。`Tax configuration can result in rounding errors for store(s): Europe Websites (French), Europe Websites (German).`

## 數位貨品的供應地點（歐盟）

歐盟(EU)商戶必須依季別向各成員國家/地區報告其數位商品的銷售情況。 數位商品會根據客戶的運送地址納稅。 法律要求商戶執行稅捐報表，並識別數位貨品（而非實體貨品）的相關稅額。

商戶必須每個季度向中央稅務管理部門報告歐盟成員國銷售的所有數位商品，連同期間所收稅款的應付帳款。

尚未達到臨界值（每年營業額50k/100k歐元）的商家，必須繼續報告已註冊VAT號碼的歐盟國家所銷售的實體商品。

針對數位商品所繳納的稅金進行稽核的商家，必須提供兩種支援資訊來建立客戶居住地。

- 客戶的送貨地址與成功付款交易的記錄，可用來建立客戶的居住地。 （只有在送貨地址符合付款提供者資訊時，才接受付款。）
- 您也可以直接從Commerce資料庫表格中的資料存放區擷取資訊。

_**若要收集數位貨品稅捐資訊：**_

1. 載入所有歐盟成員國的稅率。

1. 建立數位商品產品稅捐類別。

1. 將您的所有數位商品指派給數位商品產品稅捐類別。

1. 使用實體產品稅捐類別，為實體貨品建立[稅捐規則](tax-rules.md)，並將其與適當的稅率產生關聯。

1. 使用數位貨品的產品稅捐類別，建立數位貨品的稅捐規則，並將這些規則與歐盟成員國的適當稅率建立關聯。

1. 執行適當期間的稅捐報表，並收集所需的數位貨品資訊。

1. 匯出與數位貨品稅捐類別之稅率相關的稅捐金額。

其他資源：

- [歐洲委員會稅收與關稅同盟][1]
- [EU 1015供給地點變更][2]

[1]: https://europa.eu/youreurope/business/taxation/vat/vat-rules-rates/index_en.htm
[2]: https://www2.deloitte.com/global/en/services/tax.html
