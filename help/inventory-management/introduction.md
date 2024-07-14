---
title: Inventory management簡介
description: 瞭解如何使用 [!DNL Inventory Management] 功能來管理多個位置的存貨，以便您的 [!DNL Commerce] 存放區能正確反映實際盤點。
exl-id: 6a7dd27e-248f-4c40-b2db-0d70529422a1
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---

# Inventory management簡介

[!DNL Commerce]的[!DNL Inventory Management]提供您管理產品詳細目錄的工具。 擁有單一商店到多個倉庫、商店、取貨地點、卸貨託運人等等的商家，可以使用這些功能來維護銷售數量，並處理出貨以完成訂單。 您可以追蹤存貨數量、為所有網站的客戶提供精確的可銷售存貨量，並根據距離或優先順序的建議出貨。 您也可以針對所有商店和產品，依來源及每項產品全域設定您偏好的產品組態。 這些功能會隨著您的企業成長，讓您只需使用幾個額外設定，就能從單一倉儲或複雜的運送網路工作。

[!DNL Inventory Management]功能包括：

- 不同設定，適用於存貨源自單一來源及多個來源的商家
- 用於透過指定的來源追蹤可用彙總數量的庫存
- 並行簽出保護
- 出貨比對演演算法

>[!NOTE]
>
>這些功能是透過Community Engineering Program開發為[Inventory management](https://github.com/magento/inventory) （原為MSI）專案的一部分。<br/>
>
>[!DNL Inventory Management]模組已隨Magento Open Source和Adobe Commerce一起安裝，預設會啟用所有功能。 如需模組發行中包含的變更資訊，請參閱[發行說明](release-notes.md)。

## 基本術語

使用[!DNL Inventory Management]時，請務必瞭解下列詞語：

[!UICONTROL **來源**]&#x200B;代表儲存及出貨可用產品的實體位置。 這些地點可包括倉庫、實體店、配送中心和卸貨託運人。 （任何位置都可指定為虛擬產品的來源。）

[!UICONTROL **庫存**]&#x200B;將銷售管道（目前僅限於網站）對應至來源地點與庫存量。 一個庫存可以對應到多個銷售管道，但一個銷售管道只能指派給一個庫存。

[!UICONTROL **Aggregate Salable Quantity**]&#x200B;是可透過銷售管道銷售的虛擬庫存總計。 金額會在所有指定給庫存的來源中計算。

[!UICONTROL **預留**]&#x200B;追蹤客戶將產品加入購物車並完成結帳時，可銷售數量中的扣除專案。 當訂單出貨時，預留會清除並扣除特定來源存貨數量中的出貨金額。
