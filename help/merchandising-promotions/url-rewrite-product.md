---
title: 產品URL
description: 瞭解如何使用產品URL重寫來將連結重新導向至Commerce商店中其他產品的URL。
exl-id: 42b28ff7-e148-44f2-b6b4-63a38458e752
feature: Products, Configuration
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hant/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '897'
ht-degree: 0%

---

# 產品URL

開始之前，請務必瞭解重新導向應該有哪些功用。 從&#x200B;_目標_ / _原始要求_&#x200B;或&#x200B;_重新導向至_ / _重新導向自_。 雖然使用者可能仍會從搜尋引擎或過時的連結導覽至先前的頁面，但重新導向會導致您的商店切換至新目標。

如果您的商店已啟用[自動重新導向](url-redirect-product-automatic.md)，當產品[URL金鑰](../catalog/catalog-urls.md)變更時，就不需要建立重新寫入。

{{url-rewrite-skip}}

## 步驟1. 計畫重新寫入

若要避免錯誤，請寫下&#x200B;_重新導向至_&#x200B;路徑，以及&#x200B;_重新導向自_&#x200B;路徑，並包含URL索引鍵與尾碼（如果適用）。

如果您不確定，請開啟商店中的每個產品頁面，並從瀏覽器的位址列複製路徑。 建立產品重新導向時，您可以包含或排除[類別路徑](../catalog/catalog-urls.md)。 在此範例中，我們會建立不含類別路徑的產品重新導向。

### 具有類別路徑的產品

重新導向至： `gear/bags/impulse-duffle.html`

重新導向來源： `gear/bags/overnight-duffle.html`

### 沒有類別路徑的產品

重新導向至： `impulse-duffle.html`

重新導向來源： `overnight-duffle.html`

## 步驟2. 建立重新寫入

{{url-rewrite-params}}

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**。

1. 在繼續之前，請執行以下操作以確認請求路徑可用。

   - 在&#x200B;**[!UICONTROL Request Path]**&#x200B;欄頂端的搜尋篩選中，輸入要重新導向之頁面的URL索引鍵，然後按一下&#x200B;**[!UICONTROL Search]**。

   - 如果頁面有多個重新導向記錄，請尋找符合適用商店檢視的記錄，並以編輯模式開啟。

   - 按一下右上角的&#x200B;**[!UICONTROL Delete]**。 出現提示時，按一下&#x200B;**[!UICONTROL OK]**&#x200B;確認。

1. 在「URL重寫」頁面的右上角，按一下「**新增URL重寫**」。

1. 將&#x200B;**[!UICONTROL Create URL Rewrite]**&#x200B;設為`For product`。

1. 在網格中，尋找作為重新導向目標（目的地）的產品，然後按一下列。

   ![URL重寫 — 產品](./assets/url-rewrite-product.png){width="700" zoomable="yes"}

1. 在類別樹狀結構下方，按一下&#x200B;**[!UICONTROL Skip Category Selection]**。

   在此範例中，重新導向不包含類別。

   ![產品URL重寫 — 略過類別選擇](./assets/url-rewrite-skip-category-selection.png){width="600" zoomable="yes"}

   「為產品新增URL重寫」頁面左上角顯示指向目標的連結，而「目標路徑」欄位則顯示無法變更的路徑系統版本。 「重新導向路徑」欄位一開始也會顯示目標路徑。

   - 如果您有多個存放區檢視，請將&#x200B;**[!UICONTROL Store]**&#x200B;設定為套用重新寫入的檢視。 否則，會為每個檢視建立一個重寫。

   - 針對&#x200B;**[!UICONTROL Request Path]**，請輸入原始產品請求的URL索引鍵與尾碼（如果適用）來取代預設值。 這是您在計畫步驟中識別的&#x200B;_產品的_&#x200B;重新導向。

     >[!NOTE]
     >
     >對於指定的存放區而言，要求路徑必須是唯一的。 如果已經有使用相同請求路徑的重新導向，當您嘗試儲存重新導向時會收到錯誤。 必須先刪除先前的重新導向，才能建立重新導向。

   - 將&#x200B;**[!UICONTROL Redirect Type]**&#x200B;設定為下列其中一項：

      - `Temporary (302)`
      - `Permanent (301)`

   - 如需您自己的參考，請輸入簡短的重新寫入&#x200B;**[!UICONTROL Description]**。

   ![產品URL重寫 — 資訊](./assets/url-rewrite-product-permanent-301.png){width="600" zoomable="yes"}

1. 儲存重新導向之前，請先檢閱下列內容：

   - 左上角的連結會顯示目標產品的名稱。
   - 要求路徑包含來自&#x200B;_產品的原始_&#x200B;重新導向的路徑。

1. 完成時，按一下&#x200B;**[!UICONTROL Save]**。

   新產品重寫現在會出現在URL重寫格線的頂端。

## 步驟3. 測試結果

1. 前往商店的首頁。

1. 執行下列任一項作業：

   - 從&#x200B;_產品請求頁面瀏覽至原始的_&#x200B;重新導向。
   - 在瀏覽器的位址列中，在商店URL後面緊接著輸入原始&#x200B;_重新導向_&#x200B;產品的路徑，然後按&#x200B;**Enter**。

   隨即顯示新的目標產品，而非原始產品請求。

## 欄位說明

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | 指示重寫的型別。 建立重寫之後無法變更型別。 選項： `Custom` / `For category` / `For product` / `For CMS page` |
| [!UICONTROL Request Path] | 要重新導向的產品。 根據您的設定，請求路徑可能包含`.html`或`.htm`尾碼和類別。 請求路徑必須是唯一的，且不能由另一個重新導向使用。 如果您收到要求路徑存在的錯誤，請刪除現有的重新導向，然後再試一次。 |
| [!UICONTROL Target Path] | 系統用來指向重新導向目的地的內部路徑。 目標路徑會呈現灰色，且無法編輯。 |
| [!UICONTROL Redirect] | 決定重新導向的型別。 選項： <br/>**[!UICONTROL No]**— 未指定重新導向。 許多作業會建立此型別的重新導向要求。 例如，每次您將產品新增至類別時，每個商店檢視都會建立`No`型別的重新導向。<br/>**[!UICONTROL Temporary (302)]** — 向搜尋引擎指出該重新寫入限時有效。 搜尋引擎通常不會保留頁面排名資訊以供暫時重寫。 <br/>**[!UICONTROL Permanent (301)]**— 向搜尋引擎指出此重新寫入是永久性的。 搜尋引擎通常會保留頁面排名資訊以供永久重寫。 |
| [!UICONTROL Description] | 說明重寫以供內部參考的用途。 |

{style="table-layout:auto"}

## 多個URL重寫

您可以使用以下步驟同時快速更新多個或所有產品的URL重寫。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Products]**。

1. 選取您要更新URL重寫的所有產品。

1. 在&#x200B;_[!UICONTROL Actions]_&#x200B;底下，選擇&#x200B;**[!UICONTROL Update attributes]**&#x200B;以更新多個或全部重寫。

1. 在&#x200B;_[!UICONTROL PRODUCTS INFORMATION]_&#x200B;下，按一下&#x200B;**[!UICONTROL Websites]**&#x200B;標籤。

1. 在&#x200B;_[!UICONTROL Add Product To Websites]_&#x200B;區段中，選取您要還原URL重寫的所有網站。

1. 準備更新時，請按一下&#x200B;**[!UICONTROL Save]**。

>[!NOTE]
>
>所有選取的產品都會重新導向至選取的網站，並重新產生URL重新寫入。

![更新屬性 — 更新多個URL重寫](./assets/url-rewrites-update.png){width="600" zoomable="yes"}
