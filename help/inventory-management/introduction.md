---
title: Inventory management簡介
description: 瞭解如何使用 [!DNL Inventory Management] 可在多個位置管理庫存的功能，讓您的 [!DNL Commerce] 存放區會正確反映實際盤點。
exl-id: 6a7dd27e-248f-4c40-b2db-0d70529422a1
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# Inventory management簡介

[!DNL Inventory Management] 的 [!DNL Commerce] 提供您管理產品詳細目錄的工具。 擁有單一商店到多個倉庫、商店、取貨地點、卸貨託運人等等的商家，可以使用這些功能來維護銷售數量，並處理出貨以完成訂單。 您可以追蹤存貨數量、為所有網站的客戶提供精確的可銷售存貨量，並根據距離或優先順序的建議出貨。 您也可以針對所有商店和產品，依來源及每項產品全域設定您偏好的產品組態。 這些功能會隨著您的企業成長，讓您只需使用幾個額外設定，就能從單一倉儲或複雜的運送網路工作。

[!DNL Inventory Management] 功能包括：

- 不同設定，適用於存貨源自單一來源及多個來源的商家
- 用於透過指定的來源追蹤可用彙總數量的庫存
- 並行簽出保護
- 出貨比對演演算法

>[!NOTE]
>
>這些功能是作為的一部分 [Inventory management](https://github.com/magento/inventory) （前身為MSI）專案。<br/>
>
>此 [!DNL Inventory Management] 模組會隨Magento Open Source和Adobe Commerce一起安裝，預設會啟用所有功能。 如需模組發行版本中所包含變更的相關資訊，請參閱 [發行說明](release-notes.md).

## 基本術語

使用時，請務必瞭解下列詞語 [!DNL Inventory Management]：

[!UICONTROL **來源**] 代表儲存和出貨可用產品的實體位置。 這些地點可包括倉庫、實體店、配送中心和卸貨託運人。 （任何位置都可指定為虛擬產品的來源。）

[!UICONTROL **庫存**] 將銷售管道（目前僅限於網站）對應至來源地點及庫存量。 一個庫存可以對應到多個銷售管道，但一個銷售管道只能指派給一個庫存。

[!UICONTROL **彙總可銷售數量**] 是可透過銷售管道銷售的虛擬庫存總數。 金額會在所有指定給庫存的來源中計算。

[!UICONTROL **預訂**] 當客戶新增產品至購物車並完成結帳時，追蹤從可銷售數量中扣除的專案。 當訂單出貨時，預留會清除並扣除特定來源存貨數量中的出貨金額。
