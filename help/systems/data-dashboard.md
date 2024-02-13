---
title: 資料管理控制面板
description: 瞭解資料管理控制面板
feature: Products, Customers, Data Import/Export
source-git-commit: 925af4d3841f2972dfffcd52125a41c4a4b28815
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---

# 資料管理控制面板

「資料管理控制面板」能提供Adobe Commerce SaaS產品資料串流的深入分析。 使用者 [!DNL Live Search]， [!DNL Product Recommendations]、和 [!DNL Catalog Service] 可以從單一儀表板檢視產品同步狀態並重新同步資料。

資料管理儀表板位於 *系統* >資料傳輸> *資料管理控制面板*.

![資料管理控制面板](assets/data-management-dashboard.png)

## 設定

頁面右側的「設定」按鈕會開啟 [[!DNL Catalog Sync]](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/data-services/catalog-sync.html) 設定對話方塊。

通常情況下， [!DNL Catalog Sync] 程式會每小時自動執行一次。

重新同步目錄資料會強制服務從Commerce資料庫重新擷取資料，確保最新的變更會反映在服務和您的網站上。 如果您進行了幾項產品變更，且需要在正常自動同步程式之前更新這些變更，請使用此按鈕。

## 同步狀態

此 _[!UICONTROL Sync]_狀態面板會報告過去三小時內已同步的產品數量。 如果您不經常更新目錄，此值通常為零。 按一下&#x200B;**[!UICONTROL Refresh]**以重新整理計數。

## 產品計數

產品計數面板會反映服務可用的目錄產品總數。

此 [!DNL Catalog Service] 儀表板會反映目錄中可供服務使用的產品總數。 這通常是Commerce資料庫中的所有產品。

產品Recommendations和Live Search儀表板會顯示總數量的 [_可搜尋_](https://experienceleague.adobe.com/docs/commerce-admin/catalog/catalog/search/search.html) 產品。 如果部分產品未設定為可搜尋，這會解釋兩者之間的產品總數差異。 [!DNL Product Recommendations] 和 [!DNL Live Search]、和 [!DNL Catalog Service].

## 同步的產品

「同步的目錄產品」表格提供索引中產品的詳細資訊。 根據預設，此表格會依「上次更新」排序。

若要尋找特定產品，請使用**[!UICONTROL Search by SKU]**欄位。
若要控制要顯示的欄，請按一下 **[!UICONTROL Customize Table]** 在表格的右側。
