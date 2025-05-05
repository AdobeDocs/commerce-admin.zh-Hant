---
title: 新增贈品登入搜尋
description: 瞭解如何放置禮品註冊搜尋方塊，協助商店訪客從客戶註冊處購買產品。
exl-id: 8c5558d6-3641-4769-987e-8b217603d9fc
feature: Gift, Storefront, Search
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 0%

---

# 新增贈品登入搜尋

{{ee-feature}}

[Widget](../content-design/widgets.md)工具可用來將禮品註冊搜尋方塊放置在商店中的大部分位置。 您可以指定可供客戶使用的搜尋選項，例如名稱、電子郵件地址及禮品註冊識別碼。 當客戶按一下「搜尋」按鈕時，結果會顯示在「贈品註冊搜尋」頁面上。 如果搜尋未傳回任何結果，客戶可以使用其他引數重試。

![店面範例 — 禮品登入搜尋](./assets/storefront-gift-registry-search.png){width="700" zoomable="yes"}

## 設定禮品登入搜尋

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**。

1. 按一下右上角的&#x200B;**[!UICONTROL Add Widget]**。

1. 選擇&#x200B;**[!UICONTROL Settings]**&#x200B;索引標籤並執行下列動作：

   - 將&#x200B;**[!UICONTROL Type]**&#x200B;設為`Gift Registry Search`。

   - 將&#x200B;**[!UICONTROL Design Theme]**&#x200B;設定為商店使用的主題。

   - 按一下&#x200B;**[!UICONTROL Continue]**。

   ![禮品登入 — 搜尋設定](./assets/widget-gift-registry-search-settings.png){width="700" zoomable="yes"}

1. 在&#x200B;_[!UICONTROL Storefront Properties]_&#x200B;區段中，執行下列動作：

   - 輸入&#x200B;**[!UICONTROL Widget Title]**&#x200B;以供內部參考。

   - 將&#x200B;**[!UICONTROL Assign to Store Views]**&#x200B;設定為可供使用禮品登入搜尋的存放區檢視。

   - 設定&#x200B;**[!UICONTROL Sort Order]**&#x200B;以決定當頁面上有其他區塊指派給相同位置時，禮品登入搜尋區塊出現的順序。

   ![禮品登入 — 店面屬性](./assets/widget-gift-registry-search-storefront-properties.png){width="700" zoomable="yes"}

1. 在&#x200B;**[!UICONTROL Layout Updates]**&#x200B;區段中，按一下&#x200B;**[!UICONTROL Add Layout Update]**。

1. 若要判斷禮品註冊搜尋出現在商店中的位置，請執行下列步驟：

   - 將&#x200B;**[!UICONTROL Display On]**&#x200B;設定為您要在存放區中顯示禮品登入搜尋區塊的頁面。

   - 如果適用，請選擇要顯示它的&#x200B;**[!UICONTROL Categories]**。

   - 將&#x200B;**[!UICONTROL Container]**&#x200B;設定為頁面上放置禮品登入搜尋區塊的位置。

   ![贈品登入 — 配置更新](./assets/widget-gift-registry-search-layout-updates.png){width="500" zoomable="yes"}

1. 在左側面板中選擇&#x200B;**[!UICONTROL Widget Options]**。

1. 若要決定網站訪客搜尋禮品註冊的方式，請選取下列符合條件的專案：

   - [!UICONTROL All Forms]
   - [!UICONTROL Registrant Name Search]
   - [!UICONTROL Registrant Email Search]
   - [!UICONTROL Gift Registry ID Search]

   ![贈品登入 — Widget選項](./assets/widget-gift-registry-search-widget-options.png){width="700" zoomable="yes"}

1. 完成時，按一下&#x200B;**[!UICONTROL Save]**。

1. 當提示您重新整理頁面快取時，請按一下工作區頂端訊息中的連結，然後依照指示進行。

## 欄位說明

### [!UICONTROL Settings]

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Type] | 將`Gift Registry Search`識別為Widget的型別。 |
| [!UICONTROL Design Theme] | 禮品註冊搜尋所在商店使用的佈景主題。 |

{style="table-layout:auto"}

### [!UICONTROL Storefront Properties]

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Widget Title] | 內部參照的名稱。 |
| [!UICONTROL Assign to Store Views] | 識別可使用禮品註冊搜尋的存放區檢視。 |
| [!UICONTROL Sort Order] | 表示當有其他區塊指定出現在相同位置時，禮品註冊搜尋區塊出現的順序。 |

{style="table-layout:auto"}

### [!UICONTROL Layout Updates]

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Display On] | 指示出現禮品註冊搜尋區塊的特定頁面或頁面型別。 |
| [!UICONTROL Categories] | 如果適用，會識別「禮品註冊搜尋」出現的類別頁面。 |
| [!UICONTROL Container] | 表示放置贈品登入搜尋的頁面配置區塊。 選項會因範本和主題而異。 |

{style="table-layout:auto"}

### [!UICONTROL Widget Options]

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Quick Search Form Types] | 決定可用禮品註冊搜尋執行的搜尋型別。 選項： `All Forms` / `Registrant Name Search` /` Registrant Email Search` / `Gift Registry ID Search` |

{style="table-layout:auto"}
