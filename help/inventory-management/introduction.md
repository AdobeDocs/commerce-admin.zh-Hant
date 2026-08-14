---
title: ' [!DNL Inventory Management]簡介'
description: 瞭解如何使用 [!DNL Inventory Management]  for [!DNL Commerce] 來管理各種來源與存貨的存貨、計算可銷售數量、追蹤預訂，以及支援訂單履行。 使用「管理員」來設定設定並產生報表，並使用命令列介面進行設定和背景變更。
exl-id: 6a7dd27e-248f-4c40-b2db-0d70529422a1
TQID: https://experienceleague.adobe.com/7v-G-DZEki7y-4HSmq-rJxsmu6vih26jRYYCRRUF-XY
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 125a49f740639bce0ced8063074ca43d627c0eac
workflow-type: tm+mt
source-wordcount: 371
ht-degree: 0%

---

# [!DNL Inventory Management]簡介

[!DNL Commerce]的[!DNL Inventory Management]可協助商戶管理一或多個網站以及實體或虛擬產品地點的詳細目錄。 它提供管理介面和命令列介面中的工具，以設定存貨、追蹤庫存量和彙總可銷售數量、在結帳期間保護存貨，以及支援訂單履行。 您可以將[!DNL Inventory Management]用於單一來源或多來源網路，其中包含倉儲、倉庫、取貨地點、卸貨託運人及其他履行地點。

## 使用[!DNL Inventory Management]的方式

- **管理員：**&#x200B;設定詳細目錄選項並產生詳細目錄報告。
- **命令列介面：**&#x200B;執行安裝程式命令，並在背景套用清查變更。
- **設定範圍：**&#x200B;全域、每個來源或每個產品設定詳細目錄設定。

## 主要功能

[!DNL Inventory Management]功能包括：

- 不同設定，適用於存貨源自單一來源或多個來源的商家
- 用於追蹤跨指定來源之彙總可銷售數量的存量
- 並行簽出保護
- 支援根據距離或優先順序的履行建議的出貨比對演演算法

>[!NOTE]
>
>這些功能是透過Community Engineering Program開發為[Inventory management](https://github.com/magento/inventory) （原為MSI）專案的一部分。<br/>
>
>[!DNL Inventory Management]模組已隨Magento Open Source和Adobe Commerce安裝，預設會啟用所有功能。 如需模組發行中包含的變更資訊，請參閱[發行說明](release-notes.md)。

## 基本術語

使用[!DNL Inventory Management]時，請務必瞭解下列詞語：

[!UICONTROL Sources]代表儲存和出貨可用產品的實體位置。 如需範例和圖表，請參閱[庫存和來源](sources-stocks.md)。 （任何位置都可指定為虛擬產品的來源。）

[!UICONTROL Stocks]將銷售管道（目前僅限於網站）對應至來源地點與庫存量。 一個庫存可以對應到多個銷售管道，但一個銷售管道只能指派給一個庫存。

[!UICONTROL Aggregate Salable Quantity]是可透過銷售管道銷售的虛擬庫存總數。 金額會在所有指定給庫存的來源中計算。

當客戶新增產品至購物車並完成結帳時，[!UICONTROL Reservations]追蹤從可銷售數量中扣除的專案。 當訂單出貨時，預留會清除並扣除特定來源存貨數量中的出貨金額。
