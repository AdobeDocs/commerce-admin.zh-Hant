---
title: 類別URL重寫
description: 瞭解如何使用類別URL重寫來將連結重新導向至Commerce商店中另一個類別的URL。
exl-id: fc18f472-4aa8-4203-ade9-7ca576689d61
feature: Categories, Configuration
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 0%

---

# 類別URL重寫

如果從目錄中移除類別，您可以使用類別重寫將連結重新導向至商店中其他類別的URL。 從&#x200B;_目標_ / _原始要求_&#x200B;或&#x200B;_重新導向至_ / _重新導向自_。 雖然使用者可能仍會從搜尋引擎或過時的連結導覽至先前的頁面，但重新導向會導致您的商店切換至新目標。

如果您的商店已啟用[自動重新導向](url-redirect-product-automatic.md)，則類別[URL索引鍵](../catalog/catalog-urls.md)變更時，不需要建立重新寫入。

{{url-rewrite-skip}}

## 步驟1. 計畫重新寫入

若要避免錯誤，請寫下&#x200B;_重新導向至_&#x200B;路徑，以及&#x200B;_重新導向自_&#x200B;路徑，並包含URL索引鍵與尾碼（如果適用）。

如果您不確定，請開啟商店中的每個類別頁面，並從瀏覽器的位址列複製路徑。

**範例：**

重新導向至： `gear/backpacks-and-bags.html`

重新導向來源： `gear/bags.html`

## 步驟2. 建立重新寫入

{{url-rewrite-params}}

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**。

1. 在繼續之前，請執行以下操作以確認請求路徑可用：

   - 在&#x200B;**[!UICONTROL Request Path]**&#x200B;欄頂端的搜尋篩選中，輸入要重新導向之類別的URL索引鍵，然後按一下&#x200B;**[!UICONTROL Search]**。

   - 如果頁面有多個重新導向記錄，請尋找符合適用商店檢視的記錄，然後在編輯模式中開啟重新導向記錄。

   - 按一下右上角的&#x200B;**[!UICONTROL Delete]**。 出現提示時，按一下&#x200B;**[!UICONTROL OK]**&#x200B;確認。

1. 當您返回&#x200B;_[!UICONTROL URL Rewrites]_頁面時，請按一下&#x200B;**[!UICONTROL Add URL Rewrite]**。

1. 將&#x200B;**[!UICONTROL Create URL Rewrite]**&#x200B;設為`For category`，然後在樹狀結構中選擇重新導向目的地的目標類別。

   ![URL重寫 — 選擇類別](./assets/url-rewrite-category-choose.png){width="700" zoomable="yes"}

1. 在&#x200B;_URL重寫_&#x200B;區段中，執行下列動作：

   - 如果您有多個存放區，請選取套用重寫的&#x200B;**[!UICONTROL Store]**。

   - 針對&#x200B;**[!UICONTROL Request Path]**，輸入客戶要求的類別URL索引鍵。 這是來自&#x200B;_類別的_&#x200B;重新導向。

     >[!NOTE]
     >
     >對於指定的存放區而言，要求路徑必須是唯一的。 如果已經有使用相同請求路徑的重新導向，當您嘗試儲存重新導向時會收到錯誤。 必須先刪除先前的重新導向，才能建立重新導向。

   - 將&#x200B;**[!UICONTROL Redirect]**&#x200B;設定為下列其中一項：

      - `Temporary (302)`
      - `Permanent (301)`

   - 如需參考，請輸入重寫的簡短說明。

   ![新增類別](./assets/url-rewrite-for-category.png){width="700" zoomable="yes"}的URL重寫

1. 儲存重新導向之前，請先檢閱下列內容：

   - 左上角的連結會顯示目標類別的名稱。
   - 要求路徑包含來自&#x200B;_類別的原始_&#x200B;重新導向路徑。

1. 完成時，按一下&#x200B;**[!UICONTROL Save]**&#x200B;按鈕。

   新的類別重寫會顯示在「URL重寫」格線的頂端。

## 步驟3. 測試結果

1. 前往商店的首頁。

1. 執行下列任一項作業：

   - 導覽至原始的&#x200B;_重新導向（從_&#x200B;類別）。
   - 在瀏覽器的位址列中，在商店URL後面緊接著輸入原始&#x200B;_重新導向_&#x200B;類別的路徑，然後按&#x200B;**[!UICONTROL Enter]**。

   此時會出現新的目標類別，而非原始類別要求。

## 欄位說明

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | 指示重寫的型別。 建立重寫之後無法變更型別。 選項： `Custom` / `For category` / `For product` / `For CMS page` |
| [!UICONTROL Request Path] | 要重新導向的類別。 根據您的設定，請求路徑可能包含.html或.htm尾碼以及父類別。 請求路徑必須是唯一的，且不能由另一個重新導向使用。 如果您收到請求路徑存在的錯誤，請刪除現有的重新導向，然後再試一次。 |
| [!UICONTROL Target Path] | 系統用來指向重新導向目的地的內部路徑。 目標路徑會呈現灰色，且無法編輯。 |
| [!UICONTROL Redirect] | 決定重新導向的型別。 選項： <br/>**[!UICONTROL No]**— 未指定重新導向。 許多作業會建立此型別的重新導向要求。 例如，每次您將產品新增至類別時，每個商店檢視都會建立`No`型別的重新導向。<br/>**[!UICONTROL Temporary (302)]** — 向搜尋引擎指出該重新寫入限時有效。 搜尋引擎通常不會保留頁面排名資訊以供暫時重寫。 <br/>**[!UICONTROL Permanent (301)]**— 向搜尋引擎指出此重新寫入是永久性的。 搜尋引擎通常會保留頁面排名資訊以供永久重寫。 |
| [!UICONTROL Description] | 說明重寫以供內部參考的用途。 |

{style="table-layout:auto"}
