---
title: 產品影像匯入
description: 瞭解如何使用每個影像的路徑和檔案名稱匯入產品影像。
exl-id: 991550e6-9ce2-4472-becb-3492bd4c9582
feature: Products, Data Import/Export, Media
source-git-commit: 53c3b6c9fa9c152e6619528a43580b0acc71a2a5
workflow-type: tm+mt
source-wordcount: '836'
ht-degree: 0%

---

# 產品影像匯入

每種型別的多個產品影像都可以匯入Adobe Commerce和Magento Open Source，並與特定產品建立關聯。 每個產品影像的路徑和檔案名稱都會輸入CSV檔案中，而要匯入的影像檔案會上傳至Commerce伺服器或外部伺服器上的對應路徑。

Commerce會針對按字母順序組織的產品影像建立專屬的目錄結構。 將含有現有影像的產品資料匯出至CSV檔案時，您可以在每個影像的檔案名稱前看到依字母順序排列的路徑。 不過，匯入新影像時，您不需要指定路徑，因為Commerce會自動管理目錄結構。 但請務必在要匯入之各影像的檔案名稱之前，輸入匯入目錄的相對路徑。

若要上傳影像，您必須擁有登入憑證和存取伺服器上Commerce資料夾的正確許可權。 使用正確的認證，您可以使用任何SFTP公用程式，將檔案從桌上型電腦上傳至伺服器。

在嘗試匯入許多影像之前，請先檢閱要使用的匯入方法中的步驟，並使用一些產品完成整個程式。 瞭解其運作方式後，您就可以放心地匯入大量影像。

>[!IMPORTANT]
>
>建議您使用支援UTF-8編碼的程式來編輯CSV檔案，例如Notepad++。 Microsoft® Excel會在CSV檔案的欄標題中插入其他字元，如此可防止將資料匯回Commerce。

## 方法1：從本機伺服器匯入影像

1. 在Commerce伺服器上，將影像檔案上傳至`var/import/images`資料夾或子資料夾，例如`var/import/images/product_images`。 這是匯入產品影像時的預設根資料夾。

   ```
   <Magento root folder>/var/import/images
   ```

   >[!NOTE]
   >
   >從Adobe Commerce和Magento Open Source`2.3.2`發行版本開始，**[!UICONTROL Images File Directory]**&#x200B;中指定的路徑會串連以匯入影像基底目錄 — `<Magento-root-folder>/var/import/images`。 若是舊版Adobe Commerce和Magento Open Source，只要在匯入程式期間指定了資料夾路徑，您就可以在Commerce伺服器上使用其他資料夾。

1. 在CSV資料中，輸入要匯入到正確資料列上的每個影像檔案的名稱，依`sku`輸入，並根據影像型別（`base_image`、`small_image`、`thumbnail_image`或`additional_images`）輸入到正確的資料欄中。

   >[!NOTE]
   >
   >對於預設匯入資料夾(`var/import/images`)中的影像，請勿在CSV資料中包含檔案名稱之前的路徑。

   CSV檔案只能包含`sku`欄及相關影像欄。

   ![範例 — CSV影像資料匯入](./assets/data-import-csv-image-files-default-local.png){width="600" zoomable="yes"}

1. 依照指示[匯入](data-import.md)資料。

1. 選取要匯入的檔案後，輸入相對路徑&#x200B;**[!UICONTROL Images File Directory]**。

   ```
   var/import/images
   ```

   ![資料匯入影像檔案目錄](./assets/data-import-file-to-import.png){width="600" zoomable="yes"}

   >[!TIP]
   >
   >保留&#x200B;_[!UICONTROL Images File Directory]_空白以使用`<Magento-root-folder>/var/import/images`目錄。 從Adobe Commerce和Magento Open Source版本2.3.2開始，這是預設的匯入影像基礎目錄。

   如果為單一`sku`匯入多個影像，請將影像插入名為`additional_images`的欄中（如果尚未新增，請新增該欄），並以逗號分隔。 範例： `image02.jpg,image03.jpg`

## 方法2：從外部伺服器匯入影像

1. 上傳要匯入至外部伺服器上指定資料夾的影像。

1. 在CSV資料中，依影像型別（`base_image`、`small_image`、`thumbnail_image`或`additional_images`）輸入正確欄中每個影像檔案的完整URL。

   ```
   https://example.com/images/image.jpg
   ```

1. 依照指示[匯入](data-import.md)資料。

## 方法3：使用遠端儲存匯入影像

1. 在遠端儲存模組中，將影像檔案上傳至`var/import/images`資料夾或子資料夾，例如`var/import/images/product_images`。 這是匯入產品影像時的預設根資料夾。

   ```bash
   <remote-storage-root-folder>/var/import/images
   ```

   >[!NOTE]
   >
   >從Adobe Commerce和Magento Open Source`2.3.2`發行版本開始，_[!UICONTROL Images File Directory]_中指定的路徑會串連以匯入影像基底目錄： `<remote-storage-root-folder>/var/import/images`。 對於舊版Adobe Commerce和Magento Open Source，只要在匯入過程中指定資料夾路徑，您就可以在Commerce伺服器上使用其他資料夾。

1. 在CSV資料中，輸入要匯入到正確資料列上的每個影像檔案的名稱，依`sku`輸入，並根據影像型別（`base_image`、`small_image`、`thumbnail_image`或`additional_images`）輸入到正確的資料欄中。

   >[!NOTE]
   >
   >對於預設匯入資料夾(`var/import/images`)中的影像，請勿在CSV資料中包含檔案名稱之前的路徑。

   CSV檔案只能包含`sku`欄及相關影像欄。

   ![範例 — CSV影像資料匯入](./assets/data-import-csv-image-files-default-local.png){width="600" zoomable="yes"}

1. 依照指示[匯入](data-import.md)資料。

1. 選取要匯入的檔案後，輸入相對路徑&#x200B;**[!UICONTROL Images File Directory]**。

   ```
   var/import/images/product_images
   ```

   >[!TIP]
   >
   >將&#x200B;_[!UICONTROL Images File Directory]_保留空白以使用`<Magento-root-folder>/var/import/images`目錄。 從Adobe Commerce和Magento Open Source版本2.3.2開始，這是預設的匯入影像基礎目錄。

   如果為單一`sku`匯入多個影像，請在名為`additional_images`的欄中插入影像（如果尚未新增，請新增該欄），並以逗號分隔： `image02.jpg,image03.jpg`

如需有關啟用及管理遠端儲存模組的詳細資訊，請參閱&#x200B;_設定指南_&#x200B;中的[設定遠端儲存](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage.html)。

>[!NOTE]
>
>匯入產品影像不會起始影像大小調整。 `pub/get.php`會在前端調整產品影像的大小。 請確定您的`pub/get.php`正常運作；否則，可能無法調整影像大小。
