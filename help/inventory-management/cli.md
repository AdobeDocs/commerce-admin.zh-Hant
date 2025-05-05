---
title: '[!DNL Inventory Management] CLI參考'
description: 瞭解 [!DNL Inventory Management] 模組提供的管理清查資料和組態設定的命令。
exl-id: d92dffce-94a1-443c-8c72-98fecbbd5320
level: Experienced
feature: Inventory, Configuration
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hant/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%

---

# [!DNL Inventory Management] CLI參考

[!DNL Inventory Management]提供管理清查資料和組態設定的命令。

這些指令包括：

- 檢查並解決影響可銷售數量的預留不一致
- 新增距離優先順序演演算法的地理代碼

## 解決預留不一致

預留會針對各存貨的產品SKU保留可銷售數量。 當您出貨、新增產品、取消或退回訂單時，報酬預留會輸入以放置或清除這些保留。

[!DNL Inventory Management]提供兩個命令來檢查及解決保留不一致的問題：

- [&#39;詳細目錄:reservation:清單 — 不一致&#39;](#list-inconsistencies-command)
- [&#39;詳細目錄:reservation:建立補償&#39;](#create-compensations-command)

### 預訂不一致的原因

[!DNL Inventory Management]產生主要事件的保留：

- 訂購位置（初始預訂）
- 訂單出貨（補償預留）
- 退款訂單或發出銷退折讓單（薪酬預留）
- 訂單取消（補償預訂）

在下列情況下，可能會出現預訂不一致的情況：

- [!DNL Inventory Management]會遺失初始預訂，並輸入太多預訂補償（過度補償並導致數量不一致）
- [!DNL Inventory Management]正確放置初始預訂，但會遺失補償預訂。

您可以在`inventory_reservation`表格中手動檢閱及檢查預留。

以下設定和事件可能會導致預訂不一致：

- **升級至2.3.x，且訂單未處於最終狀態（完成、已取消或已關閉）。** [!DNL Inventory Management]會建立這些訂單的補償預留，但不會輸入或具有從可銷售數量扣除的初始預留。 建議在從2.1.x或2.2.x升級為Adobe Commerce或Magento Open Source v2.3.x之後使用這些命令。 如果您有暫緩訂單，這些指令會正確更新銷售與訂單履行的可銷售數量與預留。
- **您不管理Stock，稍後再變更此設定。**&#x200B;您可以在設定中將&#x200B;**[!UICONTROL Manage Stock]**&#x200B;設為`No`的情況下開始使用2.3.x。 [!DNL Commerce]不會在下單和出貨事件中預定時間。 如果您稍後啟用&#x200B;**[!UICONTROL Manage Stock]**&#x200B;設定並建立某些訂單，當您處理並履行該訂單時，可銷售數量將會因補償預留而損毀。
- **當訂單提交至網站時，您重新指派網站的庫存**。 初始預留會針對初始存貨輸入，而所有報酬預留則會輸入至新存貨。
- **所有保留的總數可能無法解析為`0`。**&#x200B;處於最終狀態（完成、已取消、已關閉）之訂單範圍中的所有預留應解析為`0`，並清除所有可銷售數量保留。

### 清單不一致性指令

`list-inconsistencies`命令會偵測並列出所有保留區不一致。 使用指令選項僅檢查已完成或不完整的訂單，或檢查全部。

```bash
bin/magento inventory:reservation:list-inconsistencies
```

命令選項：

- `-c`， `--complete-orders` — 傳回已完成訂單的不一致專案。 不正確的預留可能仍會保留已完成的訂單。
- `-i`， `--incomplete-orders` — 傳回未完成訂單（部分出貨、未出貨）的不一致情況。 不正確的預留可能會保留太多或沒有足夠的訂單可銷售數量。
- `-b`， `--bunch-size` — 定義要同時載入多少訂單。
- `-r`，`--raw` — 原始輸出。

使用`-r`的回應會以`<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>`格式傳回：

- 訂單ID表示不一致的範圍。
- SKU會指出產品不一致之處。
- 數量會設定要為預留補償輸入的金額。
- 存貨識別碼定義成存貨的範圍，使用預留來計算可銷售數量。

範例：

```bash
bin/magento inventory:reservation:list-inconsistencies

Inconsistencies found on following entries:
Order 172:
- Product bike-123 should be compensated by +2.000000 for stock 1
```

```bash
bin/magento inventory:reservation:list-inconsistencies -r

172:bike-123:+2.000000:1
```

如果找不到問題，則會傳回此訊息：找不到訂單不一致。

### 建立補償指令

`create-compensations`命令會建立補償預留。 視問題而定，系統會建立新的預留以放置或解除可銷售數量的保留。

若要建立保留，請使用格式`<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>`提供補償，例如`172:bike-123:+2.000000:1`。

```bash
bin/magento inventory:reservation:create-compensations
```

命令選項：

- `-r`， `--raw` — 傳回原始輸出。

如果請求的格式不正確，則會顯示以下訊息：

```
Error while parsing argument "your_incorrect_format_argument". Given argument does not match pattern "/(?P<increment_id>.*):(?P<sku>.*):(?P<quantity>.*):(?P<stock_id>.*)/".
```

當指令建立預留時，它會顯示訊息，指示SKU、訂單和庫存的更新。

```bash
bin/magento inventory:reservation:create-compensations 172:bike-123:+2.000000:1

Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
```

如果薪酬專案的SKU包含空格，請用引號將SKU括住。

```bash
bin/magento inventory:reservation:create-compensations 172:"bike 123":+2.000000:1
```

### 偵測不一致並建立補償

您可以使用管道同時執行`list-inconsistencies`和`create-compensations`，偵測不一致並立即建立補償。 使用`-r`命令選項產生原始資料並將其提交至`create-compensations`。

```bash
bin/magento inventory:reservation:list-inconsistencies -r | bin/magento inventory:reservation:create-compensations
```

範例回應：

```bash
bin/magento inventory:reservation:list-inconsistencies -r | bin/magento inventory:reservation:create-compensations
```

```
Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
- Product bikehat-456 was compensated by +1.000000 for stock 1
```

更新完成後，執行list命令以驗證：

```bash
bin/magento inventory:reservation:list-inconsistencies -r
```

```
No order inconsistencies were found.
```

您也可以傳送指令來偵測不一致，並為不完整(`-i`)或完整(`-c`)訂單建立補償。

```bash
bin/magento inventory:reservation:list-inconsistencies -r -i | bin/magento inventory:reservation:create-compensations
```

```bash
bin/magento inventory:reservation:list-inconsistencies -r -c | bin/magento inventory:reservation:create-compensations
```

## 匯入地理代碼

[!DNL Inventory Management]提供[距離優先順序演演算法](distance-priority-algorithm.md)，可協助您決定送出完整或部份訂單的最佳選項。 演演算法會使用GPS資訊或地理代碼，來計算訂單中每個料號的來源（倉儲或其他實體地點）與出貨地址之間的距離。 演演算法會根據這些結果，建議應使用哪個來源來依順序出貨每個專案。

商家會選取計算距離所需的GPS或地理碼資料提供者：

- **Google MAP**&#x200B;使用[Google Map Platform](https://mapsplatform.google.com/)服務來計算送貨目的地位址與來源位置之間的距離和時間。 此選項需要Google計費計畫，並可能透過Google產生費用。

- **離線計算**&#x200B;使用從[geonames.org](https://www.geonames.org/)下載的資料並使用命令匯入Commerce來計算距離。 這個選項是免費的。

若要匯入用於離線計算的地理代碼：

輸入下列命令，並包含以空格分隔的[ISO-3166 alpha2國碼](https://www.geonames.org/countries/)清單：

```bash
bin/magento inventory-geonames:import <country code> <country code> ...
```

例如：

```bash
bin/magento inventory-geonames:import us ca gb de
```

系統會下載地理編碼資料並匯入您的資料庫，然後顯示訊息`Importing <country code>: OK`。
