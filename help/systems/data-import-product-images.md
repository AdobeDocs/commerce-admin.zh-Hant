---
title: 產品影像匯入
description: 瞭解如何使用每個影像的路徑和檔案名稱匯入產品影像。
exl-id: 991550e6-9ce2-4472-becb-3492bd4c9582
feature: Products, Data Import/Export, Media
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '835'
ht-degree: 0%

---

# 產品影像匯入

每種型別的多個產品影像都可以匯入Adobe Commerce和Magento Open Source，並與特定產品建立關聯。 每個產品影像的路徑和檔案名稱都會輸入CSV檔案中，而要匯入的影像檔案會上傳至Commerce伺服器或外部伺服器上的對應路徑。

Commerce會針對按字母順序組織的產品影像建立自己的目錄結構。 將含有現有影像的產品資料匯出至CSV檔案時，您可以在每個影像的檔案名稱前看到依字母順序排列的路徑。 不過，當您匯入新影像時，您不需要指定路徑，因為Commerce會自動管理目錄結構。 但請務必在要匯入之各影像的檔案名稱之前，輸入匯入目錄的相對路徑。

若要上傳影像，您必須擁有登入憑證和存取伺服器上Commerce資料夾的正確許可權。 使用正確的認證，您可以使用任何SFTP公用程式，將檔案從桌上型電腦上傳至伺服器。

在嘗試匯入許多影像之前，請先檢閱要使用的匯入方法中的步驟，並使用一些產品完成整個程式。 瞭解其運作方式後，您就可以放心地匯入大量影像。

>[!IMPORTANT]
>
>建議您使用支援UTF-8編碼的程式來編輯CSV檔案，例如Notepad++。 Microsoft® Excel會在CSV檔案的欄標題中插入其他字元，如此可防止將資料匯回Commerce。

## 方法1：從本機伺服器匯入影像

1. 在Commerce伺服器上，將影像檔案上傳至 `var/import/images` 資料夾或子資料夾，例如 `var/import/images/product_images`. 這是匯入產品影像時的預設根資料夾。

   ```terminal
   <Magento root folder>/var/import/images
   ```

   >[!NOTE]
   >
   開始使用Adobe Commerce和Magento Open Source `2.3.2` 發行版本，此版本指定的路徑 **[!UICONTROL Images File Directory]** 串連以匯入至影像基礎目錄 —  `<Magento-root-folder>/var/import/images`. 若是舊版Adobe Commerce和Magento Open Source，只要在匯入程式期間指定了資料夾路徑，您就可以在Commerce伺服器上使用其他資料夾。

1. 在CSV資料中，輸入要在正確列匯入的每個影像檔案的名稱，方法為 `sku`，並根據影像型別在正確的欄中(`base_image`， `small_image`， `thumbnail_image`，或 `additional_images`)。

   >[!NOTE]
   >
   對於預設匯入資料夾中的影像(`var/import/images`)，請勿在CSV資料中包含檔案名稱前的路徑。

   CSV檔案只能包含 `sku` 欄和相關影像欄。

   ![範例 — CSV影像資料匯入](./assets/data-import-csv-image-files-default-local.png){width="600" zoomable="yes"}

1. 依照指示進行 [匯入](data-import.md) 資料。

1. 選取要匯入的檔案後，輸入以下相對路徑 **[!UICONTROL Images File Directory]**.

   ```terminal
   var/import/images
   ```

   ![資料匯入影像檔案目錄](./assets/data-import-file-to-import.png){width="600" zoomable="yes"}

   >[!TIP]
   >
   離開 _[!UICONTROL Images File Directory]_空白以使用 `<Magento-root-folder>/var/import/images` 目錄。 從Adobe Commerce和Magento Open Source版本2.3.2開始，這是預設的匯入影像基礎目錄。

   如果為單一匯入多個影像 `sku`，將影像插入名為的欄中 `additional_images` （如果欄尚未新增，請新增該欄），並以逗號分隔。 範例： `image02.jpg,image03.jpg`

## 方法2：從外部伺服器匯入影像

1. 上傳要匯入至外部伺服器上指定資料夾的影像。

1. 在CSV資料中，依影像型別在正確的欄中輸入每個影像檔案的完整URL (`base_image`， `small_image`， `thumbnail_image`，或 `additional_images`)。

   ```terminal
   https://example.com/images/image.jpg
   ```

1. 依照指示進行 [匯入](data-import.md) 資料。

## 方法3：使用遠端儲存匯入影像

1. 在遠端儲存模組中，將影像檔案上傳至 `var/import/images` 資料夾或子資料夾，例如 `var/import/images/product_images`. 這是匯入產品影像時的預設根資料夾。

   ```terminal
   <remote-storage-root-folder>/var/import/images
   ```

   >[!NOTE]
   >
   開始使用Adobe Commerce和Magento Open Source `2.3.2` 發行版本，此版本指定的路徑 _[!UICONTROL Images File Directory]_串連以匯入至影像基礎目錄： `<remote-storage-root-folder>/var/import/images`. 對於舊版Adobe Commerce和Magento Open Source，只要在匯入過程中指定資料夾路徑，您就可以在Commerce伺服器上使用其他資料夾。

1. 在CSV資料中，輸入要在正確列匯入的每個影像檔案的名稱，方法為 `sku`，並根據影像型別在正確的欄中(`base_image`， `small_image`， `thumbnail_image`，或 `additional_images`)。

   >[!NOTE]
   >
   對於預設匯入資料夾中的影像(`var/import/images`)，請勿在CSV資料中包含檔案名稱前的路徑。

   CSV檔案只能包含 `sku` 欄和相關影像欄。

   ![範例 — CSV影像資料匯入](./assets/data-import-csv-image-files-default-local.png){width="600" zoomable="yes"}

1. 依照指示進行 [匯入](data-import.md) 資料。

1. 選取要匯入的檔案後，輸入以下相對路徑 **[!UICONTROL Images File Directory]**.

   ```terminal
   var/import/images/product_images
   ```

   >[!TIP]
   >
   離開 _[!UICONTROL Images File Directory]_空白以使用 `<Magento-root-folder>/var/import/images` 目錄。 從Adobe Commerce和Magento Open Source版本2.3.2開始，這是預設的匯入影像基礎目錄。

   如果為單一匯入多個影像 `sku`，將影像插入名為的欄中 `additional_images` （如果尚未新增欄，請新增欄），以逗號分隔： `image02.jpg,image03.jpg`

如需啟用及管理遠端儲存模組的詳細資訊，請參閱 [設定遠端儲存裝置](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage.html) 在 _設定指南_.

>[!NOTE]
>
匯入產品影像不會起始影像大小調整。 產品影像在前端會依下列方式調整大小： `pub/get.php`. 確定您的 `pub/get.php` 運作正常；否則，可能無法調整影像大小。
