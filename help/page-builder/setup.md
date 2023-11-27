---
title: 『[!DNL Page Builder] 設定'
description: 瞭解 [!DNL Page Builder] Adobe Commerce和Magento Open Source管理員中的功能設定。
exl-id: 48396045-0fef-4f4f-8138-e6d969560e42
feature: Page Builder, Configuration
source-git-commit: 2299beb6c11af801076d3aff0b026d41b9dbd212
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# [!DNL Page Builder] 設定

在設定中啟用時， [!DNL Page Builder] 是CMS頁面、區塊和動態區塊的預設內容建立工具。 此外， _[!UICONTROL Enable Advanced CMS]_按鈕選件 [!DNL Page Builder] 作為「類別」和「產品」的選項。 您也可以選擇預設值 [頁面配置](../content-design/page-layout.md) 要用於產品、類別和CMS頁面的物件。 [!DNL Page Builder] 無法使用WYSIWYG的新聞稿內容 [編輯者](../content-design/editor.md).

>[!NOTE]
>
>安裝時， [!DNL Page Builder] 覆寫預設設定 [!UICONTROL Mask for Meta Description] 設定欄位。 此值已變更，從 `{{name}} {{description}}` 至 `{{name}}`.
><br>
>您可以前往以下位置存取此設定： [!UICONTROL Stores] > _[!UICONTROL Settings]_> [!UICONTROL Configuration]，展開 [!UICONTROL Catalog]，並選擇 [!UICONTROL Catalog] 底下。 此 [!UICONTROL Mask for Meta Description] 欄位位於 [!UICONTROL Product Fields Auto-generation] 區段。

>[!NOTE]
>
>管理員使用者必須具備 [!UICONTROL Content] 的許可權 [角色範圍](../systems/permissions-user-roles.md) 以檢視 [!UICONTROL Edit with Page Builder] 按鈕的下拉式選單，以及能夠使用頁面產生器的按鈕。

如需有關內容管理進階工具組態選項的詳細資訊，請參閱 [_設定參考指南_](../configuration-reference/general/content-management.md).

## 設定 [!DNL Page Builder]

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中的 _[!UICONTROL General]_，選擇&#x200B;**[!UICONTROL Content Management]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** 並確認 **[!UICONTROL Enable Page Builder]** 設為 `Yes`.

   ![進階內容工具](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

1. 如果您已準備好進行設定 [!DNL Google Maps]，請執行下列動作：

   - 如有需要，請遵循 [取得API金鑰][1] 指示，然後複製並貼上 **[!UICONTROL Google Maps API Key]**.

   - 若要變更 **[!UICONTROL Google Maps Style]**，貼上產生的JSON程式碼 [[!DNL Google Maps] API樣式精靈][2].

   >[!NOTE]
   >
   >另請參閱 [媒體 — 地圖](map.md) 如需關於使用的詳細資訊 [!DNL Google Maps] 在您的 [!DNL Page Builder] 內容。

1. 若要設定 [!DNL Page Builder] 欄格線，請執行下列動作：

   - 的 **[!UICONTROL Default Column Grid Size]**&#x200B;中，輸入要在格線中顯示的預設欄數。

   - 的 **[!UICONTROL Maximum Column Grid Size]**，輸入您希望格線中可用的最大欄數。

   >[!NOTE]
   >
   >另請參閱 [版面 — 欄](column.md) 以取得有關使用欄格線時之詳細資訊 [!DNL Page Builder] 內容。

1. 完成後，按一下 **[!UICONTROL Save Config]**.

## 設定預設版面

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中的 _[!UICONTROL General]_，選擇&#x200B;**[!UICONTROL Web]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) **[!UICONTROL Default Layouts]** 並執行下列動作：

   ![預設版面](../configuration-reference/general/assets/web-default-layouts.png){width="600" zoomable="yes"}

   如需有關Web組態選項的詳細資訊，請參閱 [_設定參考指南_](../configuration-reference/general/web.md#default-layouts).

   - 選擇 **[!UICONTROL Default Product Layout]** 要用於產品頁面的屬性。

   - 選擇 **[!UICONTROL Default Category Layout]** 要用於類別頁面的設定檔。

   - 選擇 **[!UICONTROL Default Page Layout]** 要用於CMS頁面的物件。

1. 完成後，按一下 **[!UICONTROL Save Config]**.

## 停用 [!DNL Page Builder]

>[!NOTE]
>
>正在停用 [!DNL Page Builder] 以WYSIWYG取代進階內容工具 [編輯者](../content-design/editor.md)、和，可能會導致店面顯示錯誤。 您先前建立的內容 [!DNL Page Builder] 可能無法從管理員進行編輯。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中的 _[!UICONTROL General]_，選擇&#x200B;**[!UICONTROL Content Management]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** 並設定 **[!UICONTROL Enable Page Builder]** 至 `No`.

1. 提示確認時，按一下 **[!UICONTROL Turn Off]**.

1. 完成後，按一下 **[!UICONTROL Save Config]**.

1. 出現提示時， [重新整理](../systems/cache-management.md) 任何無效的快取。

[1]: https://developers.google.com/maps/documentation/javascript/get-api-key
[2]: https://mapstyle.withgoogle.com/
