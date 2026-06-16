---
title: 定位內容區塊
description: 將區塊放置在頁面上的特定位置，甚至針對特定產品或類別進行定位，而不需編寫任何程式碼
exl-id: cfc9eb2c-19c8-43f1-937d-4162b5011b8a
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案（Adobe管理的PaaS基礎結構）和內部部署專案的Adobe Commerce 。"
TQID: https://experienceleague.adobe.com/BgZJJ9DGr8KD2-6XNf3yPTjo3ulGVdp0yyrJMXHWX-4
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 485
ht-degree: 0%

---

# 定位內容區塊

控制頁面配置與區塊位置的程式碼是以XML [介面工具集](widgets.md)寫入。 這些Widget可讓您輕鬆將區塊放置在頁面上的特定位置，甚至針對特定產品或類別也可以，而不需撰寫任何程式碼。 您可以從清單中選擇每個選項，而不是嘗試記住所有可能的組合。

下列清單說明通常會放置區塊的頁面型別所在的位置。 如需關於如何定義頁面上的區域的詳細資訊，請參閱[標準版面配置](page-layout.md#standard-page-layouts)。

## 類別和CMS頁面

| 區塊參考 | 位置 |
|----------|-------- |
| [!UICONTROL Breadcrumbs] | 許多頁面頂端的導覽輔助將您目前的位置顯示為連結。 如果顯示，置於階層連結參考中的任何其他內容都會浮動在階層連結的右側。 |
| [!UICONTROL Left Column] | 內容會新增至左欄。 |
| [!UICONTROL Main Content Area] | 內容會新增至主要內容區域。 |
| [!UICONTROL My Cart Extra Actions] | 當客戶按一下頁面頂端的購物車圖示時，內容會顯示在&#x200B;_購物車小計_&#x200B;下方。 |
| [!UICONTROL Navigation Bar] | 內容會顯示在主要導覽列下方。 |
| [!UICONTROL Page Bottom] | 內容會顯示在頁面底部。 |
| [!UICONTROL Page Footer] | 內容會顯示在頁面頁尾上方。 |
| [!UICONTROL Page Header] | 內容會顯示在頁面標頭下方。 |
| [!UICONTROL Page Top] | 內容會顯示在頁面頂端。 |
| [!UICONTROL Right Column] | 內容會顯示在右欄。 |
| [!UICONTROL Store Language] | 內容會顯示在標頭的左上角。 |

{style="table-layout:auto"}

## 產品頁面

| 區塊參考 | 位置 |
|----------|-------- |
| [!UICONTROL Alert URLs] | 內容會顯示在產品詳細資料頁面上的產品標題下方。 |
| [!UICONTROL Bottom Block Options Wrapper] | 如果新增自訂選項，內容會顯示在&#x200B;_「加入購物車」_&#x200B;按鈕下方。 |
| [!UICONTROL Breadcrumbs] | 內容會顯示在階層連結的右側，這是提供連結作為路徑的導覽輔助程式，顯示在導覽列下方。 |
| [!UICONTROL Info Column Options Wrapper] | 如果新增自訂選項，內容會顯示在右側。 相同的位置適用於可設定的選項。 |
| [!UICONTROL Left Column] | 內容會顯示在左側欄區塊下方。 |
| [!UICONTROL Main Content Area] | 內容會顯示在主要內容區域下方。 |
| [!UICONTROL My Cart Extra Actions] | 當客戶按一下頁面頂端的購物車圖示時，內容會顯示在&#x200B;_購物車小計_&#x200B;下方。 |
| [!UICONTROL Navigation Bar] | 內容會顯示在主要導覽列下方。 |
| [!UICONTROL Page Bottom] | 內容會顯示在頁面底部。 |
| [!UICONTROL Page Footer] | 內容會顯示在頁面頁尾上方。 |
| [!UICONTROL Page Header] | 內容會顯示在頁面標頭下方。 |
| [!UICONTROL Page Top] | 內容會顯示在頁面頂端。 |
| [!UICONTROL PayPal Express Checkout (Payflow Edition) Shortcut Wrapper] | 如果啟用PayPal付款方式，內容會顯示在&#x200B;_PayPal購買_&#x200B;按鈕下方。 |
| [!UICONTROL PayPal Express Checkout Shortcut Wrapper] | 如果啟用PayPal付款方式，內容會顯示在&#x200B;_PayPal購買_&#x200B;按鈕下方。 |
| [!UICONTROL Product Tags List] | 內容會顯示在產品標籤列下方。 |
| [!UICONTROL Product View Extra Hint] | 內容會顯示在產品主要最高價格下方。 |
| [!UICONTROL Right Column] | 內容會顯示在右側欄區塊下方。 |
| [!UICONTROL Store Language] | 內容會顯示在語言選擇器的右側。 |
| [!UICONTROL Tags List Before] | 內容出現在&#x200B;_[!UICONTROL Add Your Tags]_&#x200B;欄位上方。 |

{style="table-layout:auto"}
