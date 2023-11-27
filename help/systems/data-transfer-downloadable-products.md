---
title: 匯入可下載的產品
description: 檢閱針對可下載產品匯入產品資料的範例。
exl-id: e0b45ef5-dff1-4ee4-aa7e-2407162669fd
feature: Products, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---

# 匯入可下載的產品

匯入可下載產品的流程與的相同 [套件組合產品](data-transfer-bundle-products.md) 或 [可設定的產品](data-transfer-configurable-products.md). 其差異在於可下載的產品具有 [可下載的連結](../catalog/product-create-downloadable.md) 和 [可下載的範例](../catalog/product-create-downloadable.md) 及其影像。

可下載連結和範例的預設根目錄為 `<Magento-root-folder>/pub/media/import`. 如果已啟用遠端儲存模組，可下載連結和範例的預設根目錄為 `<remote-storage-root-folder>/media/import` 目錄。

CSV檔案有單獨的欄 `downloadable_links` 和 `downloadable_samples`.

- **可下載的連結影像**  — 在以下範例中，可下載的連結影像(`red.jpg` 和 `black.jpg`)在 `<Magento-root-folder>/pub/media/import/test` 資料夾。 如果已啟用遠端儲存，這些影像會位於 `<remote-storage-root-folder>/media/import/test` 資料夾。

  ![範例資料 — 可下載的產品與可下載的連結](./assets/data-import-downloadable-links.png){width="600" zoomable="yes"}

- **可下載的範例影像**  — 在以下範例中，可下載的範例影像(`white.jpg`)在 `<Magento-root-folder>/pub/media/import/test` 資料夾。 如果已啟用遠端儲存，此影像會位於 `<remote-storage-root-folder>/media/import/test` 資料夾。

  ![範例資料 — 可下載的產品，包含可下載的範例](./assets/data-import-downloadable-samples.png){width="400" zoomable="yes"}

如需啟用及管理遠端儲存模組的詳細資訊，請參閱 [設定遠端儲存裝置](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage.html) 在 _設定指南_.
