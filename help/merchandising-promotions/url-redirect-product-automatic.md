---
title: 自動重新導向
description: 瞭解如何設定當產品或類別的URL索引鍵在您的Commerce商店中變更時，系統會產生自動重新導向。
exl-id: fbde09d3-a1a3-4bac-a850-4c74c99fe714
feature: Categories, Products, Configuration
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hant/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 0%

---

# 自動重新導向

您的商店可設定為每當產品或類別的URL金鑰變更時，自動產生永久重新導向。 在「搜尋引擎最佳化」區段中，URL索引鍵下方的核取方塊會指出是否啟用永久重新導向。 如果您的存放區已設定為自動重新導向目錄URL，重新導向是對URL金鑰的簡單更新。 產品和類別建立自動重新導向的程式相同。

>[!NOTE]
>
>當啟用自動重新導向且儲存類別時，所有產品和類別重寫都會即時產生，並依預設儲存在資料庫表格中。 這可能會對有許多指派產品的類別造成顯著的效能問題。 解決方案是變更此預設值，並在類別儲存時略過為產品產生類別/產品URL重寫。 在這種情況下，只會針對標準產品URL產生產品重寫。

## 設定自動重新導向

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Catalog]**&#x200B;並在下方選擇&#x200B;**[!UICONTROL Catalog]**。

1. 展開&#x200B;**[!UICONTROL Search Engine Optimization]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![目錄組態 — 搜尋引擎最佳化](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

1. 將&#x200B;**[!UICONTROL Create Permanent Redirect for URLs if URL Key Changed]**&#x200B;設為`Yes`。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。


>[!NOTE]
>
> 可以為商店檢視或網站範圍產生URL重寫。 從管理員設定URL重寫範圍： **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;**[!UICONTROL Catalog]**>**[!UICONTROL Catalog]**>**[!UICONTROL Search Engine Optimization]**。 在&#x200B;_[!UICONTROL Product URL Rewrite Scope]_&#x200B;欄位中選取範圍。

## 自動重新導向產品URL

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Products]**。

1. 在清單中找到產品，然後按一下以開啟記錄。

1. 展開![展開選擇器](../assets/icon-display-expand.png) **[!UICONTROL Search Engine Optimization]**&#x200B;區段。

   ![產品搜尋引擎最佳化 — 永久重新導向](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

1. 針對&#x200B;**[!UICONTROL URL Key]**，請執行下列動作：

   - 確定已選取&#x200B;**[!UICONTROL Create Permanent Redirect for old URL]**&#x200B;核取方塊。 如果沒有，請依照指示[啟用自動重新導向](url-rewrite.md#configure-url-rewrites)。

   - 視需要更新&#x200B;**[!UICONTROL URL Key]**，在這些字元之間使用所有小寫字元和非尾隨連字型大小，而非空格。

1. 完成時，按一下&#x200B;**[!UICONTROL Save]**。

1. 當提示重新整理快取時，請遵循工作區頂端訊息中的連結。

   永久重新導向現在對產品和任何相關的類別URL有效。

## 自動重新導向類別URL

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Categories]**。

1. 在樹狀結構中尋找類別，然後按一下以開啟記錄。

1. 展開&#x200B;**[!UICONTROL Search Engine Optimization]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

1. 針對&#x200B;**[!UICONTROL URL Key]**，請執行下列動作：

   - 確定已選取&#x200B;**[!UICONTROL Create Permanent Redirect for old URL]**&#x200B;核取方塊。 如果沒有，請依照指示[啟用自動重新導向](url-rewrite.md#configure-url-rewrites)。

   - 視需要更新&#x200B;**[!UICONTROL URL Key]**，在這些字元之間使用所有小寫字元和非尾隨連字型大小，而非空格。

1. 完成時，按一下&#x200B;**[!UICONTROL Save]**。

1. 當提示重新整理快取時，請遵循工作區頂端訊息中的連結。

   永久重新導向現在對類別及任何相關聯的產品URL有效。

## 略過產生產品URL重寫以進行類別儲存 {#skip-rewrite}

>[!WARNING]
>
>關閉類別/產品URL重寫的自動產生功能，會導致永久移除所有現有類別/產品型別URL重寫，且無法還原。 這可能會造成無法解析的類別/產品型別URL衝突，需要手動更新URL金鑰才能解決。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Catalog]**&#x200B;並在下方選擇&#x200B;**[!UICONTROL Catalog]**。

1. 展開&#x200B;**[!UICONTROL Search Engine Optimization]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

1. 將&#x200B;**[!UICONTROL Generate "category/product" URL Rewrites]**&#x200B;設為`No`。

1. 在確認對話方塊中，按一下&#x200B;**[!UICONTROL OK]**&#x200B;以確認變更及移除現有的URL重寫。

   ![關閉類別/產品URL重新寫入 — 確認](./assets/seo-rewrite-off.png){width="350"}

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。
