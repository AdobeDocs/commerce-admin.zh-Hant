---
title: 管理詳細目錄來源
description: 瞭解來源，以及來源如何定義管理及出貨產品存貨以進行訂單履行或提供服務的實際位置。
exl-id: 1315a8c9-7791-4c4b-9463-3126b79793c2
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '689'
ht-degree: 0%

---

# 管理來源

來源是管理產品存貨並出貨以履行訂單或提供服務的實際地點。 這些地點可包括倉庫、實體店、配送中心、取貨地點及卸貨託運人。 您配置存貨數量給這些來源，[!DNL Commerce]會自動彙總存貨的可銷售產品總數。 對於大型公司，請為所有位置新增多個來源：在不同地理位置（依國家/地區和大陸）、在城市中的位置（根據存貨型別，甚至根據服務）。

建立來源時，建議您提供特定的實體地理位置。 這可讓&#x200B;_距離優先順序演演算法_&#x200B;比較出貨目的地地址的位置與可用的來源位置，以決定最接近完成出貨的來源。 您可以使用Google地圖或使用地理代碼的離線計算。 如需此&#x200B;_距離優先順序演演算法_&#x200B;的詳細資訊，請參閱[設定距離優先順序演演算法](distance-priority-algorithm.md)。

從您可以更新但不能停用的&#x200B;_預設Source_&#x200B;開始。 單一來源商家和產品移轉會使用此來源。 您一律需要預設來源。

- **地點資訊** — 每個來源都包含名稱、國家/地區、地點的實體地址以及聯絡點。
- **正在啟用資源** — 您可以視需要啟用和停用來源。 只有在來源接受並履行訂單與延期交貨訂單時，才啟用來源。
- **可用存貨** — 透過產品頁面指定及更新每個來源的存貨數量。 存貨數量會透過來源與存貨對應來計算、提供及預留。

下圖可協助說明銷售山地腳踏車的腳踏車商店商家的「來源」，可供存貨使用，且SSA可存取其出貨。

![範例來源圖表](assets/diagram-sources.png){width="600" zoomable="yes"}

所有商店的開頭皆採用必須保持啟用的預設Source：

- 所有匯入至[!DNL Commerce]的新產品都需要來源和庫存，並且會自動指派以立即存取[!DNL Inventory Management]。
- 單一來源商家使用預設Source作為其存貨地點與出貨的單一地點。

## 編輯來源

您可以更新名稱、地址、GPS位置和聯絡點資訊。 來源的程式碼是受保護的值，可作為將來源與您的產品數量和庫存相關聯的唯一ID。

如果編輯預設Source，您可以編輯所有設定，但名稱和程式碼除外。 建議單一來源商家新增與其位置相符的資訊。

_[!UICONTROL Manage Sources]_&#x200B;頁面列出所有可用的存貨地點和履行設施。 您可以新增存貨來源及編輯現有位置。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**。

1. 若要新增詳細目錄位置，請參閱[新增新的Source](sources-add.md)。

1. 尋找詳細目錄來源，並以&#x200B;_編輯_&#x200B;模式開啟。

1. 更新資訊並儲存變更。

   ![管理來源](assets/inventory-sources.png){width="600" zoomable="yes"}

## 按鈕列

| 按鈕 | 說明 |
|--|--|
| [!UICONTROL Add New Source] | 開啟「新Source」表單，用於輸入新的存貨來源、履行設施或地點。 |

## 管理來源欄說明

| 欄 | 說明 |
|--|--|
| [!UICONTROL Code] | 系統用來識別詳細目錄來源的唯一英數字元代碼。 |
| [!UICONTROL Name] | 可識別管理員使用者之詳細目錄來源的唯一名稱。 |
| [!UICONTROL Is Enabled] | 表示存貨來源是否有效且可供使用。 |
| [!UICONTROL Pickup Location] | 指出來源是否為[店內傳遞](../stores-purchase/shipping-in-store-delivery.md)的取貨地點。 |
| [!UICONTROL Action] | 按一下&#x200B;**[!UICONTROL Edit]**&#x200B;在編輯模式中開啟詳細目錄來源記錄。 |

## 其他欄

| 欄 | 說明 |
|--- |--- |
| [!UICONTROL Latitude] | 指定GPS詳細目錄來源的緯度座標。 以數字輸入值，視需要加上加號或減號。 不允許使用度符號和字母。 例如： `32.7555` |
| [!UICONTROL State/Province] | 來源所在的州或省。 |
| [!UICONTROL Postcode] | 來源的郵遞區號。 |
| [!UICONTROL Email] | 主要連絡人的電子郵件。 |
| [!UICONTROL Longitude] | 指定GPS詳細目錄來源的經度座標。 以數字輸入值，視需要加上加號或減號。 不允許使用度符號和字母。 例如：經度–97.3308 |
| [!UICONTROL City] | 來源所在的城市。 |
| [!UICONTROL Phone] | 主要連絡人的電話號碼。 |
| [!UICONTROL Country] | 來源所在的國家/地區。 |
| [!UICONTROL Street] | 來源的街道地址。 |
| [!UICONTROL Fax] | 主要連絡人的區碼和傳真號碼。 |
