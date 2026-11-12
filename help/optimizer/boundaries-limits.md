---
title: 銷售服務限制與界限
description: 瞭解Adobe Commerce Optimizer授許可權制和系統界限。 規劃容量、追蹤使用量，並在超過限制時避免延遲和節流。
role: Admin, Developer
hide: true
badgeSaas: label="僅限SaaS" type="Positive" url="https://experienceleague.adobe.com/zh-hant/docs/commerce/user-guides/product-solutions" tooltip="僅適用於以CCDM布建的Adobe Commerce as a Cloud Service執行個體（Adobe管理的SaaS基礎結構）。"
autotag-review: '2026-11-02T18:48:38.168Z'
TQID: 'https://experienceleague.adobe.com/KoRp--G2sMvv-Hr7KiHriZrFmtEm0BhGoGWVQQK-ofE'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
feature_v2:
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: 8d0b446f-5b16-5a10-b272-01143504a11c
    internal-label: System
  - id: d3b92bef-63fa-5031-a925-d04d9362d616
    internal-label: Saas
source-git-commit: 71df9ad673f2e7dff802e4b26d8e169c42d9c063
workflow-type: tm+mt
source-wordcount: '1006'
ht-degree: 1%
---

# 使用可撰寫目錄資料模型(CCDM)的銷售服務限制和邊界

搭配CDM的Adobe Commerce銷售服務會套用授許可權制和系統邊界，以定義專案可使用的容量：

- **授許可權制** — 根據您購買的容量；可以購買其他套件來擴充。
- **系統界限** — 已修正限制，可保護系統資源並確保所有使用者的可靠效能。

您的使用量必須維持在這些限制內。 超過上限可能會導致延遲增加並要求節流。

## 請求額外容量

透過購買[授許可權制和系統界限](#license-limits-and-system-boundaries)一節中所述的授權套件，或針對不重複的使用案例協商自訂授權，可增加授許可權制。 請聯絡您的Adobe客戶代表以討論您的需求。

若有關於系統界限的問題，請連絡[Adobe支援](https://experienceleague.adobe.com/home?lang=zh-Hant#support)。

## 避免效能問題

遵循這些最佳實務，以保持在限制內並避免營運問題：

- **檢閱您的限制** — 在啟動新店面或行銷活動之前，請先瞭解您的[容量限制](#license-limits-and-system-boundaries)。
- **追蹤您的使用情形** — 使用內建的量度儀表板或CDN記錄。

## 授許可權制和系統界限

下表按功能區域概述許可證限制和系統邊界，並包含新增額外許可證以擴大適用容量的相關資訊。


### 目錄

| **功能** | **描述** | **基底配置** | **可擴充？** |
| --- | --- | --- | --- |
| 產品擷取率 | 已建立或已更新的產品數 | 每分鐘1K更新<p>每天最多可更新100,000個</p> | 是<p>新增一個授權套件：</p><ul><li>每分鐘5K更新<br>每天最多可更新500K</li> <li>每分鐘10K更新<br>每天最多可更新1M</li></ul><p>資料擷取的最大容量為每天100萬次更新。</p> |
| 產品裝載大小 | 使用API建立、更新或擷取產品資訊時允許的最大資料量 | 200 KB | 否 |
| 目錄變數 | 店面使用者可用的目錄檢視次數。<p>計算為（*目錄檢視次數×價格簿數量*）</p> | 100個變數 | 是<p>新增100個目錄變化授權套件</p> |
| 單一目錄來源中的產品 | 目錄中支援的SKU | 25萬SKU | 是<p>新增100K SKU授權套件</p> |
| 各產品的變體 | 每個產品允許的產品變數（大小、顏色組合）數量 | 10K | 否 |
| 目錄來源 | 目錄資料內容（例如PIM和ERP等地區設定或資料來源）的數量 | 50 | 否 |

{style="table-layout:auto"}

### 價格簿

| **功能** | **描述** | **基底配置** | **可擴充？** |
| --- | --- | --- | --- |
| 價格簿 | 每個執行個體允許的價格簿數量 | 根據[目錄變數](#catalog)的數量 | 是<br>增加目錄變化 |
| 每筆價格記錄的折扣 | 單一價格簿中可套用至產品價格的折扣數 | 10 | 否 |

{style="table-layout:auto"}

### 目錄檢視與原則

| **功能** | **描述** | **基底配置** | **可擴充？** |
| --- | --- | --- | --- |
| 目錄檢視 | 主目錄的可設定子集數目 | 根據[目錄變數](#catalog)的數量 | 是<br>增加目錄變化 |
| 每個目錄檢視的原則 | 允許的資料篩選器數 | 10 | 否 |
| 原則中的屬性值 | 可設定為篩選的產品特性數 | 100 | 否 |
| [受限制的存取金鑰指派](setup/private-catalog-view.md) | 可指派給單一目錄檢視的受限制存取金鑰數目 | 3 | 否 |
| RSA金鑰大小（限制存取金鑰） | 受限制的存取金鑰可接受的最小和最大金鑰強度 | 最低2048位元，最高8192位元 | 否 |
| 受限制的存取金鑰 | 金鑰撤銷傳播延遲 | 由於快取，最多可達5分鐘。 延遲過後，系統會拒絕以移除的金鑰簽署的權杖。 | 不適用 |

{style="table-layout:auto"}

### 目錄店面

目錄店面功能的基本配置是根據GMV （毛商品價值）層級來決定。 此表格指出每項功能的最小配置。

| **功能** | **描述** | **基底配置** | **可擴充？** |
| --- | --- | --- | --- |
| 目錄擷取率 | 系統（店面、交易系統、ERP或其他）每月呼叫目錄API以從目錄中擷取資料的次數 | 根據GMV層級<p>最小配置：1000萬/月</p> | 是<p>每月新增100萬個授權套件要求</p> |
| 內容請求 | 要求店面提供HTML頁面檢視或JSON API呼叫。 計為1次頁面檢視或5次API呼叫。 | 根據GMV層級<p>最小配置：2M/月</p> | 是<p>每月新增100萬個授權套件</p> |
| 店面GenAI變數 | 允許產生文字式內容 | 根據GMV層級<p>最小配置：1K個變數/月</p> | 是<p>單獨購買Generative AI積分</p> |

{style="table-layout:auto"}

>[!NOTE]
>
>產生影像需要布建至與[!DNL Adobe Commerce Optimizer]相同的IMS組織的[!DNL Adobe Firefly]授權。


### 產品探索

下列限制適用於店面產品搜尋、清單和銷售設定。

| **功能** | **描述** | **基底配置** | **可擴充？** |
| --- | --- | --- | --- |
| 產品擷取 | 擷取具有`products`、`productSearch`、`refineProduct`和`variants`的產品資料時，每個[!DNL Catalog Service] GraphQL要求的最大SKU數。 將較大的請求分割為多個呼叫。 | 100 | 否 |
| 可篩選的屬性 | 可針對分層導覽和多面向啟用的產品特性（如顏色、大小、品牌或材質）數量 | 200 | 否 |
| 可搜尋的屬性 | 可針對目錄搜尋編制索引的產品特性數 | 200 | 否 |
| 可排序的屬性 | 搜尋和類別頁面上可作為排序選項的產品特性數。 | 50 | 否 |
| 搜尋分頁深度 | 透過搜尋分頁可存取的產品上限（例如，第100頁×100個產品/頁面） | 10K | 否 |
| Facet | 可篩選的產品屬性數量（例如品牌、顏色、大小、價格），可設定為協助購物者調整搜尋結果和瀏覽類別 | 100<p>必須是可篩選的屬性</p> | 否 |
| 各Facet選項 | 購物者可在Facet中選取的可篩選產品屬性值數量（例如「紅色」、「藍色」代表顏色；「小」、「Medium」代表大小） | 100 | 是<p>可透過支援要求提高</p> |

{style="table-layout:auto"}

### Recommendations

下列功能適用於產品建議。 [!DNL Adobe Commerce Optimizer]不支援其他Adobe Commerce產品中提供的部分功能。

| **功能** | **描述** | **基底配置** | **可擴充？** |
| --- | --- | --- | --- |
| 使用中的建議單位 | 店面上的即時建議元件數量（例如「已檢視客戶」或「您可能也喜歡」） | 50 | 否 |
| 類別或屬性包含/排除 | 將產品篩選為符合建議資格的特定集合 | 不支援 | — |

{style="table-layout:auto"}
