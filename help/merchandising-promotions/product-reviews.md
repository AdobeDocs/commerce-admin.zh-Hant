---
title: 產品評論
description: 瞭解產品評論如何增強您的商店，並為您的產品帶來更多可信度。
exl-id: 82f96b24-626f-4b2d-be42-3d655d08dfda
feature: Merchandising, Products
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 0%

---

# 產品評論

產品評論有助於建立社群意識，而且被認為比任何廣告收入都更可信。 事實上，有些搜尋引擎會對有產品評論的網站給予比沒有產品評論的網站更高的排名。 對於透過搜尋特定產品來尋找您網站的人，產品評論基本上是您商店的登陸頁面。 產品評論有助於人們找到您的商店、讓他們持續參與，並且經常帶來銷售。

Commerce包含原生產品評論功能，您可以從「管理員」管理該功能。 您也可以使用擴充功能，從 [Commerce Marketplace](../getting-started/commerce-marketplace.md) 使用主控的稽核管理系統。

>[!NOTE]
>
>Adobe Commerce和Magento Open Source版本2.4.0到2.4.3包含Yotpo廠商開發的擴充功能。 從2.4.4版開始，此擴充功能不再與核心版本搭配，必須從Commerce Marketplace安裝和更新。 此Marketplace也可讓您存取擴充功能開發人員提供的目前檔案。
><br><br>
>如果您已啟用並設定隨附的擴充功能，則必須在2.4.4升級程式中更新composer.json檔案，並管理後續的擴充功能更新。 另請參閱 [升級模組](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) 在 _升級指南_ 以取得詳細資訊。

## 店面的產品評論

啟用原生產品評論功能時，客戶可以為目錄中的任何產品撰寫評論。 您可以按一下，從產品頁面撰寫評論：

- **新增您的評論** 適用於具有現有稽核的產品。

- **成為第一個檢閱此產品的使用者** 適用於沒有現有稽核的產品。

此 [!UICONTROL Reviews] 索引標籤會列出所有目前的稽核，以及用於提交稽核的表單。

您的設定會決定客戶在撰寫產品評論之前是否必須在您的商店開立帳戶，或者他們是否能以訪客身份提交評論。 要求稽核者開立帳戶，可防止匿名提交並改善稽核品質。

![範例店面 — 新增您的評論](./assets/storefront-review-this-product.png){width="700" zoomable="yes"}

星級數表示產品的滿意度評等。 訪客可以按一下連結，閱讀評論並撰寫自己的評論。 作為獎勵，客戶可以因提交評論而獲得獎勵積分。 提交稽核時，稽核會傳送給管理員進行稽核。 核准後，該評論就會發佈在您的商店中。

![店面範例 — 評論標籤](./assets/storefront-reviews-tab.png){width="700" zoomable="yes"}

### [!UICONTROL My Product Reviews]

此 _[!UICONTROL My Product Reviews]_客戶帳戶控制面板的區段會列出客戶提交並核准發佈的所有稽核。 每個稽核摘要都包含提交稽核的日期、產品頁面的連結和稽核詳細資訊。

![我的產品評論](./assets/account-dashboard-my-product-reviews.png){width="700" zoomable="yes"}

1. 在其帳戶的側邊欄中，客戶選擇 **[!UICONTROL My Product Reviews]**.

1. 若要檢視完整檢視，請按一下 **[!UICONTROL See Details]**.

   ![檢閱詳細資訊](./assets/account-dashboard-my-product-reviews-details.png){width="700" zoomable="yes"}

## 啟用產品評論功能

預設會啟用「商業產品評論」功能。

>[!NOTE]
>
>若要將這些欄位設為 `No` 並停用Commerce產品評論，您必須清除 **使用系統值** 核取方塊。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Catalog]** 並選取 **[!UICONTROL Catalog]** 底下。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Product Reviews]** 區段。

   ![目錄設定 — Commerce產品評論](../configuration-reference/catalog/assets/catalog-product-reviews.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Enabled]** 至 `Yes`.

   這是啟用產品評論的預設設定。

1. 設定 **[!UICONTROL Allow Guests to Write Reviews]** 至 `Yes`.

   此預設設定可判斷客戶是否必須在您的商店開立帳戶才能撰寫產品評論。

1. 完成後，按一下 **[!UICONTROL Save Config]**.

## 建立自訂評等

使用Commerce產品評論，客戶可以在提交產品評論時指派評分。 預設評等為品質、價格和值。 除了這些以外，您也可以新增自己的自訂評分。 目錄頁面上顯示的五星級評等是每個產品的平均值。

![店面範例 — 自訂評分](./assets/attribute-custom-ratings-review.png){width="700" zoomable="yes"}

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Rating]**.

1. 在右上角，按一下 **[!UICONTROL Add New Rating]**.

   ![管理員 — 評等](./assets/product-reviews-rating.png){width="700" zoomable="yes"}

1. 在 _[!UICONTROL Rating Title]_區段，輸入&#x200B;**[!UICONTROL Default Value]**新評等。

   如果適用，也請輸入每個商店檢視的翻譯。

   ![評等標題設定](./assets/product-rating-title.png){width="600" zoomable="yes"}

1. 在 _評等可見度_ 部分，設定 **[!UICONTROL Visibility In]** 至使用評等的商店檢視。

   若要選取多個存放區檢視，請按住Ctrl鍵(PC)或Command鍵(Mac)並按一下每個專案。

   >[!NOTE]
   >
   >除非指派給商店檢視，否則不會顯示評等。

1. 的 **[!UICONTROL Sort Order]**，輸入數字，與其他人一起列出時決定此評等的順序。

1. 如果要在店面顯示您的評等，請選取 **[!UICONTROL Is Active]** 核取方塊。

   ![評等可見度設定](./assets/product-rating-visibility.png){width="600" zoomable="yes"}

1. 完成後，按一下 **[!UICONTROL Save Rating]**.

   目錄產品格線頁面上會顯示每個產品的所有評論平均評分。

   ![目錄頁面](./assets/catalog-rating-page.png){width="700" zoomable="yes"}
