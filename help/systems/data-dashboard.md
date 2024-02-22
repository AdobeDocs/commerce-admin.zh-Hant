---
title: 資料管理控制面板
description: 瞭解如何存取有關目錄服務、即時搜尋、產品Recommendations的資料串流的深入分析。
feature: Products, Customers, Data Import/Export
source-git-commit: eed80afd8755d416d979c362f8c21fe97ce2d2ba
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---


# 資料管理控制面板

「資料管理控制面板」能提供Adobe Commerce SaaS產品資料串流的深入分析。 使用者 [!DNL Live Search]， [!DNL Product Recommendations]、和 [!DNL Catalog Service] 可以從單一儀表板檢視產品同步狀態並重新同步資料。

資料管理儀表板位於 *系統* >資料傳輸> *資料管理控制面板*.

![資料管理控制面板](assets/data-management-dashboard.png)

## 設定

此 **[!UICONTROL Settings]** 頁面右側的按鈕會開啟對話方塊，您可以在其中重新同步目錄資料。

重新同步目錄資料會強制服務從Commerce資料庫重新擷取資料。 當目錄同步處理已有數小時未執行時，此動作通常用於首次上線期間。

## 同步狀態

此 _[!UICONTROL Sync]_狀態面板會報告過去三小時內已同步的產品數量。 如果您不經常更新目錄，此值通常為零。 按一下&#x200B;**[!UICONTROL Refresh]**以重新整理計數。

## 產品計數

產品計數面板會反映服務可用的目錄產品總數。

此 [!DNL Product Recommendations] 和 [!DNL Live Search] 儀表板顯示總數 _可顯示_ 產品。 [!DNL Catalog Service] 不會依可顯示內容來篩選產品，因此如果您同時擁有兩者 [!DNL Catalog Service] 和 [!DNL Live Search] 或 [!DNL Product Recommendations] 安裝後，兩個控制面板可能會顯示產品計數的兩個不同值。

## 同步的產品

「同步的產品」表格提供索引中產品的詳細資訊。 根據預設，此表格會依「上次更新」排序。

若要尋找特定產品，請使用 **[!UICONTROL Search by SKU]** 欄位。
若要控制要顯示的欄，請按一下 **[!UICONTROL Customize Table]** 在表格的右側。
