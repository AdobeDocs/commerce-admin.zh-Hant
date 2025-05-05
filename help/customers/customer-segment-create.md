---
title: 建立和刪除客戶區段
description: 客戶可在其「客戶帳戶資料面板」中檢視與訂單相關的退款資訊。
exl-id: 8a13271d-d0b5-4fc6-a701-3edfae04bfca
feature: Customers, Configuration
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '897'
ht-degree: 0%

---

# 建立和刪除客戶區段

{{ee-feature}}

建立客戶區段類似於建立[購物車價格規則](../merchandising-promotions/price-rules-cart.md)，只是選項包含[客戶區段特定屬性](../customers/customer-segments.md)。

![客戶區段清單](assets/customer-segments.png){width="700" zoomable="yes"}

_&#x200B;**[!UICONTROL Customer Segments]格線&#x200B;**&#x200B;_

| 欄 | 說明 |
|--- |--- |
| **[!UICONTROL ID]** | 客戶區段的唯一ID。 |
| **[!UICONTROL Segment]** | 客戶區段的名稱。 |
| **[!UICONTROL Status]** | 指出客戶區段是&#x200B;_[!UICONTROL Active]_&#x200B;還是&#x200B;_[!UICONTROL Inactive]_。 |
| **[!UICONTROL Website]** | 指出客戶區段所屬的網站。 |

{style="table-layout:auto"}

## 先決條件：啟用客戶區段

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Customers]**&#x200B;並選擇&#x200B;**[!UICONTROL Customer Configuration]**。

1. 展開&#x200B;**[!UICONTROL Customer Segments]**&#x200B;區段。

1. 確認&#x200B;**[!UICONTROL Enable Customer Segment Functionality]**&#x200B;已設定為`Yes`。

   ![客戶組態 — 客戶區段](../configuration-reference/customers/assets/customer-configuration-customer-segments.png){width="600" zoomable="yes"}

1. （選用）若要停用客戶區段的即時驗證，請將&#x200B;**[!UICONTROL Real-time Check if Customer is Matched by Segment]**&#x200B;設為`No`。

   當您停用即時驗證時，客戶區段會由單一合併條件SQL查詢來驗證。 如果系統中有許多客戶區段，停用此函式可改善區段驗證的效能。 但是，分割資料庫或沒有註冊客戶時，驗證無法運作。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

## 建立區段

下列步驟以建立客戶區段的範例為例，其目標是洛杉磯的女性客戶。

### 步驟1：新增客戶區段

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL Segments]**。

1. 按一下右上角的&#x200B;**[!UICONTROL Add Segment]**。

1. 在Admin中工作時，輸入可識別客戶區段的&#x200B;**[!UICONTROL Segment Name]**。

1. 輸入說明區段用途的簡短&#x200B;**[!UICONTROL Description]**。

1. 將&#x200B;**[!UICONTROL Assigned to Website]**&#x200B;設定為可使用客戶區段的網站。

1. 將&#x200B;**[!UICONTROL Status]**&#x200B;設定為&#x200B;_作用中_&#x200B;或&#x200B;_非作用中_。

1. 若要識別您要用來套用區段的客戶型別，請將&#x200B;**[!UICONTROL Apply to]**&#x200B;設定為下列其中一項：

   - `Visitors and Registered Customers` — 包含所有購物者，無論他們是否已登入帳戶。
   - `Registered Customers` — 僅包含已登入帳戶的購物者。
   - `Visitors` — 僅包含未登入帳戶的購物者。

   >[!TIP]
   >
   >如果您是根據儲存在客戶帳戶中的客戶屬性來建立區段，最佳作法是僅將區段套用至註冊客戶。

   >[!NOTE]
   >
   > 如果區段套用至`Visitors and Registered Customers`，[!UICONTROL Matched Customers]只會顯示`Registered Customers`。 即使可依據適用於訪客的條件鎖定訪客，亦會如此。 僅`Visitors`區段不會顯示`Matched Customers`標籤。


1. 按一下&#x200B;**[!UICONTROL Save and Continue Edit]**。

   儲存區段&#x200B;_[!UICONTROL General Properties]_&#x200B;後，左側面板中會有其他選項可供使用。

   ![區段屬性](assets/customer-segment-saved.png){width="600" zoomable="yes"}

**_[!UICONTROL General Properties]_**

| 欄位 | 說明 |
|--- |---|
| **[!UICONTROL Segment Name]** | 可識別供內部參照之區段的名稱。 |
| **[!UICONTROL Description]** | 說明區段用途以供內部參考的簡短說明。 |
| **[!UICONTROL Assigned to Website]** | 可使用區段的單一網站。 |
| **[!UICONTROL Status]** | 啟用和停用區段。 區段停用時，所有相關的價格規則和橫幅都會停用。 選項： `Active` / `Inactive` |
| **[!UICONTROL Apply to]** | 定義套用區段的客戶型別。 選取範圍會影響可用於建立區段的條件集。 區段儲存後，便無法變更設定。 |

{style="table-layout:auto"}

### 步驟2：定義條件

>[!NOTE]
>
> 對於訪客，僅適用於下列條件：購物車條件（購物車小計金額、購物車明細專案和購物車產品數量）、產品規則（在購物車和產品歷史記錄中找到的產品）以及這些專案的組合。 如果區段應同時套用至訪客和註冊客戶，則只會根據列出的條件來追蹤訪客。


1. 在左窗格中，按一下&#x200B;**[!UICONTROL Conditions]**。

   預設條件在頁面上以&#x200B;_[!UICONTROL If ALL of these conditions are TRUE:]_&#x200B;開頭。

   ![條件](assets/customer-segment-conditions.png){width="600" zoomable="yes"}

1. 建立以女性客戶為目標的條件：

   - 按一下&#x200B;**[!UICONTROL Add]**&#x200B;圖示以顯示條件清單，並選取`Gender`。

   - 保留預設的&#x200B;**為**&#x200B;條件控制選項。

   - 按一下&#x200B;**...**&#x200B;並選取`female`。

   ![條件行1](assets/customer-segment-condition-line1.png){width="600" zoomable="yes"}

1. 建立另一個以洛杉磯居民為目標的條件：

   - 在下一行，按一下&#x200B;**[!UICONTROL Add]**&#x200B;圖示並選取`Customer Address`。

     此動作會建立父條件，您可在其中定義一或多個要比對的位址列位。

   - 按一下&#x200B;**[!UICONTROL Add]**&#x200B;圖示以顯示位址列位清單，並選取`City`。

   - 按一下&#x200B;**是**&#x200B;以顯示條件控制選項並選取`contains`。

   - 按一下&#x200B;**...**&#x200B;並輸入`Los Angeles`。

   - 在下一行，按一下&#x200B;**[!UICONTROL Add]**&#x200B;圖示並選取`State/Province`。

   - 保留預設的&#x200B;**為**&#x200B;條件控制選項。

   - 按一下&#x200B;**...**&#x200B;並選取`United States > California`。

   ![加州洛杉磯女性條件](assets/customer-segment-conditions-la-ladies.png){width="600" zoomable="yes"}

1. 按一下&#x200B;**[!UICONTROL Save and Continue Edit]**。

### 步驟3：檢閱相符客戶的清單

1. 在左窗格中，按一下&#x200B;**[!UICONTROL Matched Customers]**&#x200B;以顯示符合條件的所有客戶。

   ![個相符的客戶](assets/customer-segment-matched-customers.png){width="600" zoomable="yes"}

1. 如果客戶清單符合您的目標，請按一下「**[!UICONTROL Save]**」以完成客戶區段。

1. 客戶區段現在可用於目標定位促銷活動、內容和郵件。

_&#x200B;**[!UICONTROL Matched Customers]格線&#x200B;**&#x200B;_

| 欄 | 說明 |
|--- |--- |
| **[!UICONTROL ID]** | 註冊客戶的客戶ID。 |
| **[!UICONTROL Name]** | 註冊客戶的名稱。 |
| **[!UICONTROL Email]** | 註冊客戶的電子郵件地址。 |
| **[!UICONTROL Group]** | 客戶被指派到的客戶群組。 |
| **[!UICONTROL Phone]** | 客戶的電話號碼。 |
| **[!UICONTROL ZIP]** | 客戶的郵遞區號。 |
| **[!UICONTROL Country]** | 客戶所在的國家/地區。 |
| **[!UICONTROL State / Province]** | 客戶所在的州或省。 |
| **[!UICONTROL Customer Since]** | 建立客戶帳戶的日期和時間。 |

{style="table-layout:auto"}

## 移除客戶區段

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL Segments]**。

1. 找到要刪除的區段並加以選取。

1. 在功能表列中，按一下&#x200B;**[!UICONTROL Delete]**&#x200B;按鈕。

1. 若要確認動作，請按一下&#x200B;**[!UICONTROL OK]**。

## 按鈕列

| 按鈕 | 說明 |
|--- |--- |
| **[!UICONTROL Back]** | 返回&#x200B;_[!UICONTROL Customer Segments]_&#x200B;頁面而不儲存變更。 |
| **[!UICONTROL Delete]** | 刪除目前的客戶區段。 不會移除區段中與客戶相關聯的客戶或已完成的訂單。 |
| **[!UICONTROL Reset]** | 將客戶區段表單中未儲存的任何變更重設為先前的值。 |
| **[!UICONTROL Refresh Segment Data]** | 將區段資料重新整理為最近儲存的值。 如果任何區段資料無法使用或已過期，則為相關。 |
| **[!UICONTROL Save and Continue Edit]** | 儲存變更並保持客戶區段開啟。 |
| **[!UICONTROL Save]** | 儲存變更並關閉客戶區段。 |

{style="table-layout:auto"}

## 客戶區段示範

觀看此影片以示範如何建立客戶區段：

>[!VIDEO](https://video.tv.adobe.com/v/343659/?quality=12&learn=on)
