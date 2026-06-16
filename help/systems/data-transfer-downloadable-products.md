---
title: 匯入可下載的產品
description: 檢閱針對可下載產品匯入產品資料的範例。
exl-id: e0b45ef5-dff1-4ee4-aa7e-2407162669fd
feature: Products, Data Import/Export
TQID: https://experienceleague.adobe.com/a62y8GDLpN0PHxlm8EYHHMsHfzzkjB4mSNa-BV78Ra8
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 183
ht-degree: 0%

---

# 匯入可下載的產品

匯入可下載產品的流程與[套件組合產品](data-transfer-bundle-products.md)或[可配置產品](data-transfer-configurable-products.md)相同。 不同之處在於，可下載的產品有[個可下載連結](../catalog/product-create-downloadable.md)和[個可下載的範例](../catalog/product-create-downloadable.md)及其影像。

可下載連結和範例的預設根目錄為`<Magento-root-folder>/pub/media/import`。 如果已啟用遠端儲存模組，可下載連結和範例的預設根目錄為`<remote-storage-root-folder>/media/import`目錄。

CSV檔案有`downloadable_links`和`downloadable_samples`的個別資料行。

- **可下載的連結影像** — 在下列範例中，可下載的連結影像（`red.jpg`和`black.jpg`）位於`<Magento-root-folder>/pub/media/import/test`資料夾中。 如果已啟用遠端儲存，則這些影像位於`<remote-storage-root-folder>/media/import/test`資料夾中。

  ![範例資料 — 包含可下載連結的可下載產品](./assets/data-import-downloadable-links.png){width="600" zoomable="yes"}

- **可下載的範例影像** — 在下列範例中，可下載的範例影像(`white.jpg`)位於`<Magento-root-folder>/pub/media/import/test`資料夾中。 如果已啟用遠端儲存，則此影像在`<remote-storage-root-folder>/media/import/test`資料夾中。

  ![範例資料 — 可下載的產品，包含可下載的範例](./assets/data-import-downloadable-samples.png){width="400" zoomable="yes"}

如需有關啟用及管理遠端儲存模組的詳細資訊，請參閱&#x200B;_設定指南_&#x200B;中的[設定遠端儲存](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage.html?lang=zh-Hant)。
