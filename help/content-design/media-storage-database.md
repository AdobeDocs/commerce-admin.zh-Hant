---
title: 使用媒體資料庫
description: 瞭解如何使用媒體資料庫來儲存 [!DNL Commerce] 媒體檔案。
exl-id: b59349fb-0cb6-4812-a126-6e0d8d37564f
feature: Page Content, Media, Configuration
level: Experienced
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# 使用媒體資料庫

>[!IMPORTANT]
>
>自Adobe Commerce和Magento Open Source2.4.3起，資料庫媒體儲存方法已過時。

依預設，所有影像、編譯的CSS檔案和編譯的JavaScript檔案 [!DNL Commerce] 執行個體儲存在網頁伺服器的檔案系統中。 您可以選擇將這些檔案儲存在資料庫伺服器上的資料庫中。 此方法的一個優點是在網頁伺服器檔案系統與資料庫之間自動同步和反向同步選項。 您可以使用預設資料庫來儲存媒體或建立資料庫。 若要能夠使用新建立的資料庫做為媒體儲存體，您必須將其相關資訊及其存取認證新增至 `env.php` 檔案。

## 資料庫工作流程

1. **瀏覽器要求媒體**  — 商店中的頁面會在客戶的瀏覽器中開啟，瀏覽器會要求HTML中指定的媒體。

1. **系統在檔案系統中尋找媒體**  — 系統會搜尋檔案系統中的媒體，如果找到，會將它傳遞給瀏覽器。

1. **系統在資料庫中尋找媒體**  — 如果在檔案系統中找不到媒體，則會傳送對媒體的要求至設定中指定的資料庫。

1. **系統在資料庫中尋找媒體** - PHP指令碼會將檔案從資料庫傳輸到檔案系統，並傳送給客戶的瀏覽器。 瀏覽器的媒體要求會觸發指令碼執行，如下所示：

   - 如果網頁伺服器 [重寫](../merchandising-promotions/url-rewrite.md) 已啟用 [!DNL Commerce] 而且伺服器支援的PHP指令碼只有在檔案系統中找不到要求的媒體時才執行。
   - 如果停用網頁伺服器重寫 [!DNL Commerce]或者伺服器不支援，PHP指令碼仍會執行，即使檔案系統中有所需的媒體可用。

## 使用資料庫儲存媒體

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Advanced]** 並選擇 **[!UICONTROL System]**.

1. 在左上角，設定 **[!UICONTROL Store View]** 至 `Default Config` 在全域層級套用組態。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Storage Configuration for Media]** 並執行下列動作：

   ![進階設定 — 媒體的儲存設定](./assets/database-storage-deprecated.png){width="600" zoomable="yes"}

   - 設定 **[!UICONTROL Media Storage]** 至 `Database`.

   - 設定 **[!UICONTROL Select Media Database]** 到您要使用的資料庫。

   - 若要將現有媒體傳輸至新選取的資料庫，請按一下 **[!UICONTROL Synchronize]**.

   - 輸入 **[!UICONTROL Environment Update Time]** 以秒為單位。

1. 完成後，按一下 **[!UICONTROL Save Config]**.
