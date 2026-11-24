---
title: 擴充設定
description: 設定傳遞、每月代理流量工作，以及由AI產品探索中的目錄擴充和PDP擴充共用的合格AI代理。
source-git-commit: ed404fb8515374a33116ccc811c96548fb14dd35
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%
---
# 擴充設定

使用AI產品探索工作區中的&#x200B;**[!UICONTROL Settings]**&#x200B;索引標籤來設定您的Adobe Commerce執行個體。 完成設定後，目錄和PDP擴充功能會在AI產品探索工作區中出現。

此索引標籤上的欄位會識別AI產品探索所連線的[!DNL Adobe Commerce]環境和存放區檢視。 如需IMS登入與組織需求，請參閱[AI產品探索必要條件](prerequisites.md)。

1. 在Admin中，移至&#x200B;**[!UICONTROL AI Product Discovery]** > **[!UICONTROL Catalog Enrichment]**&#x200B;或&#x200B;**[!UICONTROL Product Details Page Enrichment]**。
1. 在頁面頂端的&#x200B;**[!UICONTROL Scope]**&#x200B;清單中，選取您要設定的商店檢視，或保留&#x200B;**[!UICONTROL All Store Views]**&#x200B;以跨商店檢視管理設定。
1. 開啟&#x200B;**[!UICONTROL Settings]**&#x200B;標籤。
1. 在&#x200B;**[!UICONTROL Commerce Configuration]**&#x200B;中，展開標示其URL的存放區檢視面板。

   提供您的[!DNL Adobe Commerce]環境詳細資訊，以啟用AI產品探索服務和稽核工作流程。

   目錄擴充設定索引標籤上的![Commerce設定](./assets/catalog-enrichment-commerce-config.png){zoomable="yes"}

1. 輸入存放區檢視所需的連線詳細資料。

   - **[!UICONTROL Store View URL]**：對應至商店檢視的URL （例如，`https://brand.example.com/fr/`）。
   - **[!UICONTROL Environment ID]**：連線存取之[!DNL Adobe Commerce]環境的唯一識別碼。
   - **[!UICONTROL Website Code]**、**[!UICONTROL Store Code]**&#x200B;和&#x200B;**[!UICONTROL Store View Code]**： Commerce網站的網站、商店和商店檢視代碼。 這些值必須符合您Commerce管理員中的程式碼。
   - **[!UICONTROL Host Name]**： [!DNL Adobe Commerce]執行個體的主機名稱。
   - **（選擇性 — 僅供目錄擴充）**&#x200B;在&#x200B;**[!UICONTROL Catalog field limits]**&#x200B;底下，選取&#x200B;**[!UICONTROL Limit maximum characters for product name]**&#x200B;並指定任何產生之產品名稱的字元限制。 Select **[!UICONTROL Limit maximum characters for product description]**&#x200B;並指定任何產生的產品說明的字元限制。

1. 按一下&#x200B;**[!UICONTROL Save]**。

儲存後，請等待任何初始同步或驗證工作完成，然後再為該存放區檢視依賴目錄或稽核結果。 產品建議最多可能需要24小時的時間才會出現在&#x200B;**[!UICONTROL Catalog Enrichment]**&#x200B;頁面上。

若要移除存放區檢視設定，請展開該專案，然後按一下&#x200B;**[!UICONTROL Delete]**。

## 欄位說明 {#commerce-connection-fields}

在&#x200B;**[!UICONTROL Commerce Configuration]**&#x200B;表單上，必填欄位標有星號(*)。

| 欄位 | 必填 | 說明 |
| --- | --- | --- |
| 存放區檢視URL | 是 | 對應至商店檢視的URL （例如，`https://brand.example.com/fr/`）。 |
| 環境ID | 是 | 連線存取之[!DNL Adobe Commerce]環境的唯一識別碼。 |
| 網站程式碼 | 是 | Commerce網站的網站程式碼。 |
| 存放區代碼 | 是 | Commerce網站的商店代碼。 |
| 存放區檢視代碼 | 是 | Commerce網站的商店檢視。 |
| 主機名稱 | 是 | 您的[!DNL Adobe Commerce]執行個體的主機名稱。 |
| 目錄欄位限制（僅限目錄擴充） | 否 | 為任何產生的產品名稱和說明定義字元限制。 |
