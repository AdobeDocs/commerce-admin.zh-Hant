---
title: 設計設定
description: 「設計組態」可在單一頁面上顯示設定，讓您輕鬆編輯與設計相關的規則和組態設定。
exl-id: 43fec57f-d76d-45a9-812b-ba1947cea46d
feature: Page Content, Configuration
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# 設計設定

設計組態可讓您透過在單一頁面上顯示設定，輕鬆編輯與設計相關的規則和組態設定。

![設計設定頁面](./assets/configuration.png){width="700" zoomable="yes"}

## 變更設計組態

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**。

1. 尋找您要設定的存放區檢視，然後按一下&#x200B;_[!UICONTROL Action]_欄中的&#x200B;**[!UICONTROL Edit]**。

   頁面會顯示商店檢視的目前設計設定。

1. 若要變更預設主題，請將&#x200B;**[!UICONTROL Applied Theme]**&#x200B;設定為您要套用至檢視的主題。

   如果未指定主題，則會使用系統預設主題。 有些協力廠商擴充功能會修改系統預設主題。

1. 如果主題僅用於特定裝置，請設定&#x200B;**[!UICONTROL User Agent Rules]**。

   ![使用者代理程式規則](./assets/configuration-user-agent-rules.png){width="400" zoomable="yes"}

   對於您想要指定主題的每種裝置型別：

   - 按一下&#x200B;**[!UICONTROL Add New User Agent Rule]**。

   - 針對&#x200B;**[!UICONTROL Search String]**，輸入特定裝置的瀏覽器識別碼。

     搜尋字串可以是一般運算式或Perl相容的規則運算式(PCRE) （如需詳細資訊，請參閱[使用者代理程式](https://en.wikipedia.org/wiki/User_agent)）。 下列搜尋字串可識別Firefox：

         /^mozilla/i
     
   - 針對&#x200B;**[!UICONTROL Theme Name]**，選擇要用於指定裝置的主題。

   >[!NOTE]
   >
   >您可以為要指定的裝置新增任意數量的規則。 搜尋字串會依照輸入順序進行比對。

1. 在&#x200B;_[!UICONTROL Other Settings]_底下，展開每個區段，然後依照連結主題中的指示，視需要編輯設定。

   - [[!UICONTROL Pagination]](../catalog/navigation-product-listings.md#pagination-controls)
   - [[!UICONTROL HTML Head]](page-setup.md#html-head)
   - [[!UICONTROL Header]](page-setup.md#header)
   - [[!UICONTROL Footer]](page-setup.md#footer)
   - [[!UICONTROL Search Engine Robots]](../merchandising-promotions/seo-overview.md#search-engine-robots)
   - [[!UICONTROL Product Image Watermarks]](../catalog/product-image.md#watermarks)
   - [[!UICONTROL Transactional Emails]](../systems/email-templates.md#configure-email-templates)

   ![影響設計的其他設定](./assets/configuration-other-settings.png){width="500" zoomable="yes"}

1. 完成時，按一下&#x200B;**[!UICONTROL Save Configuration]**。
