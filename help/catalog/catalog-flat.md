---
title: 平面目錄
description: 瞭解如何建立平面型錄，每一列包含有關產品或類別的所有必要資料。
exl-id: f67bd2e0-3902-41eb-b26f-c772a7692cef
source-git-commit: f36925217230e558043078fdc274f5e69c096c1e
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 0%

---

# 平面目錄

>[!IMPORTANT]
>
>不再建議使用平面型錄作為最佳實務。 據悉，繼續使用此功能會導致效能降低和其他索引問題。 詳細說明和解決方案可參閱 [說明中心](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/slow-performance-slow-and-long-running-crons.html).<br/><br/>受影響的版本包括： <br/>- Adobe Commerce on cloud infrastructure、2.3.x和更新版本<br/>- Adobe Commerce （內部部署）、2.3.x及更高版本<br/>- Magento Open Source、2.3.x和更高版本 <br/><br/>在任何發行版本中，有些擴充功能只適用於平面表格，因此如果您停用平面表格，就會產生風險。 如果您知道您有一些使用一般目錄索引器的擴充功能，在將這些值設定為時，您必須注意這項風險 `No`.

Commerce通常會根據實體屬性值(EAV)模型，將目錄資料儲存在多個表格中。 由於產品屬性儲存在許多表格中，因此SQL查詢有時很長且複雜。

相對地，平面型錄會即時建立表格，其中每一列包含有關產品或類別的所有必要資料。 平面目錄會每分鐘自動更新，或根據您的cron工作更新。 平面目錄索引還可以加快目錄和購物車價格規則的處理。 擁有多達500,000個SKU的目錄可以快速索引為平面目錄。

>[!NOTE]
>
>在啟用即時存放區的平面目錄之前，請務必在開發環境中測試設定。

## 步驟1：啟用平面型錄

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Catalog]** 並選擇 **[!UICONTROL Catalog]** 底下。

1. 展開 _店面_ 並執行下列動作：

   - 設定 **[!UICONTROL Use Flat Catalog Category]** 至 `Yes`. (如有必要，請取消選取 **[!UICONTROL Use system value]** 核取方塊)。

   - 設定 **[!UICONTROL Use Flat Catalog Product]** 至 `Yes`.

   ![平面目錄組態](./assets/use-flat-catalog.png){width="700" zoomable="yes"}

1. 完成後，按一下 **[!UICONTROL Save Config]**.

1. 提示更新快取時，按一下 **[!UICONTROL Cache Management]** 並依照指示重新整理快取。

## 步驟2：驗證結果

您可以使用兩種方法驗證結果。

### 方法1：驗證單一產品的結果

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 在編輯模式中開啟產品。

1. 的 **[!UICONTROL Name]**，新增文字 `_TEST` 到產品名稱的結尾。

1. 按一下 **[!UICONTROL Save]**.

1. 在新瀏覽器標籤上，導覽至您的商店首頁，並執行下列動作：

   - 搜尋您編輯的產品。

   - 使用導覽來瀏覽至其指派類別下的產品。

     如有必要，請重新整理頁面以檢視結果。 變更會在分鐘內顯示，或根據 [Cron](../systems/cron.md) 排程。

   ![具平面型錄的店面](./assets/storefront-flat-catalog-enabled.png){width="700" zoomable="yes"}

### 方法2：驗證類別的結果

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. 在左上角，確認 **[!UICONTROL Store View]** 設為 `All Store Views`.

   如果出現提示，請按一下 **[!UICONTROL OK]** 以確認。

1. 在類別樹狀結構中，選取現有類別，按一下 **[!UICONTROL Add Subcategory]**，並執行下列動作：

   - 的 **[!UICONTROL Category Name]**，輸入 `Test Category`.

   - 完成後，按一下 **[!UICONTROL Save]**.

     ![測試子類別](./assets/catalog-flat-test-category.png){width="600" zoomable="yes"}

   - 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Products in Category]** 區段並按一下 **[!UICONTROL Reset Filter]** 以顯示所有產品。

   - 選取要新增至新類別的多個產品核取方塊。

   - 按一下 **[!UICONTROL Save]**.

   ![測試類別產品](./assets/catalog-flat-test-category-products.png){width="600" zoomable="yes"}

1. 在新瀏覽器標籤上，導覽至您商店的首頁，並使用商店導覽來瀏覽至您建立的類別。

   如有必要，請重新整理頁面以檢視結果。 變更會在分鐘內顯示或根據您的cron排程顯示。

## 步驟3：移除測試資料

執行下列操作以移除測試資料，並還原原始產品名稱和目錄設定。

### 移除測試類別

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. 在類別樹狀結構中，選取您建立的測試子類別。

1. 在右上角，按一下 **[!UICONTROL Delete]**.

1. 提示確認時，按一下 **[!UICONTROL OK]**.

   此類別移除不會移除指派給此類別的產品。

### 還原原始產品名稱

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. 在編輯模式中開啟測試產品。

1. 移除 `_TEST` 您新增至的文字 **[!UICONTROL Product Name]**.

1. 在右上角，按一下 **[!UICONTROL Save]**.

### 還原原始目錄設定

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Catalog]** 並選擇 **[!UICONTROL Catalog]** 底下。

1. 展開 _店面_ 並執行下列動作：

   - 設定 **[!UICONTROL Use Flat Catalog Category]** 至 `No`.

   - 設定 **[!UICONTROL Use Flat Catalog Product]** 至 `No`.

1. 完成後，按一下 **[!UICONTROL Save Config]**.

1. 出現提示時，請重新整理快取。
