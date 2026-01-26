---
title: '[!DNL Page Builder]設定'
description: 瞭解Adobe Commerce和Magento Open Source管理員中的 [!DNL Page Builder] 功能設定。
exl-id: 48396045-0fef-4f4f-8138-e6d969560e42
feature: Page Builder, Configuration
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# [!DNL Page Builder]設定

在設定中啟用時，[!DNL Page Builder]是CMS頁面、區塊和動態區塊的預設內容建立工具。 此外，_[!UICONTROL Enable Advanced CMS]_&#x200B;按鈕提供[!DNL Page Builder]作為類別和產品的選項。 您也可以選擇要用於產品、類別和CMS頁面的預設[頁面配置](../content-design/page-layout.md)。 [!DNL Page Builder]不適用於使用WYSIWYG [編輯器](../content-design/editor.md)的新聞稿內容。

>[!NOTE]
>
>安裝時，[!DNL Page Builder]會覆寫[!UICONTROL Mask for Meta Description]組態欄位的預設設定。 值已從`{{name}} {{description}}`變更為`{{name}}`。
><br>
>當您前往「[!UICONTROL Stores] > _[!UICONTROL Settings]_> [!UICONTROL Configuration]」，展開「[!UICONTROL Catalog]」，然後選擇下方的「[!UICONTROL Catalog]」時，可以存取此設定。 [!UICONTROL Mask for Meta Description]欄位在[!UICONTROL Product Fields Auto-generation]區段中。

>[!NOTE]
>
>管理員使用者必須擁有其[!UICONTROL Content]角色範圍[的](../systems/permissions-user-roles.md)許可權，才能看到[!UICONTROL Edit with Page Builder]按鈕並能夠使用頁面產生器。

如需有關內容管理進階工具組態選項的詳細資訊，請參閱&#x200B;[_組態參考指南_](../configuration-reference/general/content-management.md)。

## 設定[!DNL Page Builder]

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板的&#x200B;_[!UICONTROL General]_&#x200B;下，選擇&#x200B;**[!UICONTROL Content Management]**。

1. 展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**&#x200B;並驗證&#x200B;**[!UICONTROL Enable Page Builder]**&#x200B;是否設定為`Yes`。

   ![進階內容工具](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

1. 如果您已準備好設定[!DNL Google Maps]，請執行下列動作：

   - 如有必要，請依照[取得API金鑰](https://developers.google.com/maps/documentation/javascript/get-api-key)指示進行，然後複製並貼上您的&#x200B;**[!UICONTROL Google Maps API Key]**。

   - 若要變更&#x200B;**[!UICONTROL Google Maps Style]**，請貼上[[!DNL Google Maps] API樣式精靈](https://mapstyle.withgoogle.com/)產生的JSON程式碼。

   >[!NOTE]
   >
   >請參閱[媒體 — 地圖](map.md)，以取得有關在您的[!DNL Google Maps]內容中使用[!DNL Page Builder]的詳細資訊。

1. 若要設定[!DNL Page Builder]欄格線中的准則數目，請執行下列動作：

   - 針對&#x200B;**[!UICONTROL Default Column Grid Size]**，輸入您要顯示在格線中的預設欄數。

   - 針對&#x200B;**[!UICONTROL Maximum Column Grid Size]**，輸入您希望格線中可用的最大欄數。

   >[!NOTE]
   >
   >請參閱[配置 — 資料行](column.md)，以取得使用[!DNL Page Builder]內容時使用資料行格線的詳細資訊。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

## 設定預設版面

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板的&#x200B;_[!UICONTROL General]_&#x200B;下，選擇&#x200B;**[!UICONTROL Web]**。

1. 展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Default Layouts]**&#x200B;並執行下列動作：

   ![預設版面配置](../configuration-reference/general/assets/web-default-layouts.png){width="600" zoomable="yes"}

   如需有關Web組態選項的詳細資訊，請參閱&#x200B;[_組態參考指南_](../configuration-reference/general/web.md#default-layouts)。

   - 選擇您要用於產品頁面的&#x200B;**[!UICONTROL Default Product Layout]**。

   - 選擇您要用於類別頁面的&#x200B;**[!UICONTROL Default Category Layout]**。

   - 選擇您要用於CMS頁面的&#x200B;**[!UICONTROL Default Page Layout]**。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

## 停用[!DNL Page Builder]

>[!NOTE]
>
>停用[!DNL Page Builder]會以WYSIWYG [編輯器](../content-design/editor.md)取代進階內容工具，並可能導致店面顯示錯誤。 您先前使用[!DNL Page Builder]建立的內容可能無法從Admin編輯。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板的&#x200B;_[!UICONTROL General]_&#x200B;下，選擇&#x200B;**[!UICONTROL Content Management]**。

1. 展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**&#x200B;並將&#x200B;**[!UICONTROL Enable Page Builder]**&#x200B;設為`No`。

1. 提示確認時，按一下&#x200B;**[!UICONTROL Turn Off]**。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

1. 出現提示時，[重新整理](../systems/cache-management.md)任何無效的快取。
