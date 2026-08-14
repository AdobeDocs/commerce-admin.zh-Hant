---
title: 庫存訊息情境
description: 設定出現在店面產品頁面和類別產品清單上的 [!DNL Inventory Management] 庫存可用性訊息。
exl-id: 63114305-e695-445b-91cd-9e0fb2729ec4
feature: Inventory, Configuration
TQID: https://experienceleague.adobe.com/9kPHtr75C7PkM9vD-2-AeG8JnAfKAao0GKEH9MhkBbU
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 047d1bdc0cbefa7618fb95713f08962c59c4da9e
workflow-type: tm+mt
source-wordcount: 338
ht-degree: 2%

---

# 庫存訊息情境

使用下列區段中的設定，設定庫存可用性訊息在產品頁面和目錄清單上的顯示方式。

![含有「無庫存」訊息的群組產品](assets/storefront-out-of-stock-message.png){width="600" zoomable="yes"}

## 產品頁面庫存訊息

視管理庫存和庫存可用性設定的組合而定，產品頁面提供數種可用的傳訊方式。

### 範例1：顯示可用性訊息

#### 案例1

此設定組合會根據每個產品的庫存可用性，使可用性訊息顯示在產品頁面上。

| 股票期權 | 設定 | 訊息 |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `Yes` | |
| [!UICONTROL Manage Stock] | `Yes` | |
| [!UICONTROL Stock Availability] | `In Stock` | _[!UICONTROL Availability: In Stock]_ |
| | `Out of Stock` | _[!UICONTROL Availability: Out of Stock]_ |

#### 案例2

當未管理產品的庫存時，此設定組合可用於在產品頁面上顯示可用性訊息。

| 股票期權 | 設定 | 訊息 |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `Yes` |  |
| [!UICONTROL Manage Stock] | `No` | _[!UICONTROL Availability: In Stock]_ |

### 範例2：隱藏可用性訊息

#### 案例1

此設定和產品設定的組合可防止可用性訊息出現在產品頁面上。

| 股票期權 | 設定 | 訊息 |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `No` |  |
| [!UICONTROL Manage Stock] | `Yes` |  |
| [!UICONTROL Stock Availability] | `In Stock` | 無 |
|  | `Out of Stock` | 無 |

#### 案例2

當未管理產品的庫存時，此設定和產品設定的組合會防止可用性訊息出現在產品頁面上。

| 股票期權 | 設定 | 訊息 |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `No` |  |
| [!UICONTROL Manage Stock] | `No` | 無 |

## 目錄頁面庫存訊息

視產品可用性和組態設定而定，類別和搜尋結果清單可能會出現下列顯示選項。

類別頁面](assets/storefront-out-of-stock-catalog-page.png){width="600" zoomable="yes"}上的![無庫存訊息

### 範例1：顯示帶有「無庫存」訊息的產品

組態設定的這個組合包括類別和搜尋結果清單中的無庫存產品，並顯示「無庫存」訊息。

| 股票期權 | 設定 | 訊息 |
|--|--|--|
| [!UICONTROL Display Out of Stock Products] | `Yes` |  |
| [!UICONTROL Display product availability in stock in the frontend] | `Yes` | _[!UICONTROL Out of stock]_ |
| [!UICONTROL Display Out of Stock Products] | `Yes` |  |
| [!UICONTROL Display product availability in stock in the frontend] | `No` | 無 |

### 範例2：顯示沒有「無庫存」訊息的產品

此組態設定組合包含類別和搜尋結果清單中的無庫存產品，但不顯示訊息。

| 股票期權 | 設定 | 訊息 |
|--|--|--|
| [!UICONTROL Display Out of Stock Products] | `Yes` | 無 |
| [!UICONTROL Display product availability in stock in the frontend] | `No` |  |

### 範例3：隱藏產品直到補貨為止

此組態設定會從類別和搜尋結果清單中完全省略無庫存的產品，直到這些產品重新補充庫存為止。

| 股票期權 | 設定 | 訊息 |
|--|--|--|
| [!UICONTROL Display Out of Stock Products] | `No` | 無 |
