---
title: 類別URL重寫
description: 瞭解如何使用類別URL重寫以將連結重新導向至Commerce商店中另一個類別的URL。
exl-id: fc18f472-4aa8-4203-ade9-7ca576689d61
feature: Categories, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 0%

---

# 類別URL重寫

如果從目錄中移除類別，您可以使用類別重寫將連結重新導向至商店中其他類別的URL。 思考角度 _目標_ / _原始請求_  或 _重新導向至_ / _重新導向來源_. 雖然使用者可能仍會從搜尋引擎或過時的連結導覽至先前的頁面，但重新導向會導致您的商店切換至新目標。

如果 [自動重新導向](url-redirect-product-automatic.md) 已為您的商店啟用，不需要在類別時建立重新寫入 [URL索引鍵](../catalog/catalog-urls.md) 已變更。

{{url-rewrite-skip}}

## 步驟1. 計畫重新寫入

若要避免錯誤，請寫下 _重新導向至_ 路徑和 _重新導向來源_ 路徑並包含URL金鑰和尾碼（若適用）。

如果您不確定，請開啟商店中的每個類別頁面，並從瀏覽器的位址列複製路徑。

**範例：**

重新導向至： `gear/backpacks-and-bags.html`

重新導向來源： `gear/bags.html`

## 步驟2. 建立重新寫入

{{url-rewrite-params}}

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**.

1. 在繼續之前，請執行以下操作以確認請求路徑可用：

   - 在頂端搜尋篩選條件中 **[!UICONTROL Request Path]** 欄中，輸入要重新導向之類別的URL索引鍵，然後按一下 **[!UICONTROL Search]**.

   - 如果頁面有多個重新導向記錄，請尋找符合適用商店檢視的記錄，然後在編輯模式中開啟重新導向記錄。

   - 在右上角，按一下 **[!UICONTROL Delete]**. 出現提示時，按一下 **[!UICONTROL OK]** 以確認。

1. 當您返回 _[!UICONTROL URL Rewrites]_頁面，按一下&#x200B;**[!UICONTROL Add URL Rewrite]**.

1. 設定 **[!UICONTROL Create URL Rewrite]** 至 `For category` 並在樹狀結構中選擇重新導向的目標類別。

   ![URL重寫 — 選擇類別](./assets/url-rewrite-category-choose.png){width="700" zoomable="yes"}

1. 在 _URL重寫_ 區段，請執行下列動作：

   - 如果您有多個商店，請選取 **[!UICONTROL Store]** 適用於重新寫入的位置。

   - 的 **[!UICONTROL Request Path]**，輸入客戶請求的類別的URL索引鍵。 這是 _重新導向來源_ 類別。

     >[!NOTE]
     >
     >對於指定的存放區而言，要求路徑必須是唯一的。 如果已經有使用相同請求路徑的重新導向，當您嘗試儲存重新導向時會收到錯誤。 必須先刪除先前的重新導向，才能建立重新導向。

   - 設定 **[!UICONTROL Redirect]** 變更為下列其中一項：

      - `Temporary (302)`
      - `Permanent (301)`

   - 如需參考，請輸入重寫的簡短說明。

   ![為類別新增URL重寫](./assets/url-rewrite-for-category.png){width="700" zoomable="yes"}

1. 儲存重新導向之前，請先檢閱下列內容：

   - 左上角的連結會顯示目標類別的名稱。
   - 請求路徑包含原始檔案的路徑 _重新導向來源_ 類別。

1. 完成後，按一下 **[!UICONTROL Save]** 按鈕。

   新的類別重寫會顯示在「URL重寫」格線的頂端。

## 步驟3. 測試結果

1. 前往商店的首頁。

1. 執行下列任一項作業：

   - 導覽至原始檔案 _重新導向來源_ 類別。
   - 在瀏覽器的位址列中，輸入原始檔案的路徑 _重新導向來源_ 類別，緊接在商店URL後面，然後按 **[!UICONTROL Enter]**.

   此時會出現新的目標類別，而非原始類別要求。

## 欄位說明

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | 指示重寫的型別。 建立重寫之後無法變更型別。 選項： `Custom` / `For category` / `For product` / `For CMS page` |
| [!UICONTROL Request Path] | 要重新導向的類別。 根據您的設定，請求路徑可能包含.html或.htm尾碼以及父類別。 請求路徑必須是唯一的，且不能由另一個重新導向使用。 如果您收到請求路徑存在的錯誤，請刪除現有的重新導向，然後再試一次。 |
| [!UICONTROL Target Path] | 系統用來指向重新導向目的地的內部路徑。 目標路徑會呈現灰色，且無法編輯。 |
| [!UICONTROL Redirect] | 決定重新導向的型別。 選項： <br/>**[!UICONTROL No]**— 未指定重新導向。 許多作業會建立此型別的重新導向要求。 例如，每次將產品新增至類別時， `No` 型別會在每個商店檢視中建立。<br/>**[!UICONTROL Temporary (302)]**  — 向搜尋引擎指出該重寫作業限時有效。 搜尋引擎通常不會保留頁面排名資訊以供暫時重寫。 <br/>**[!UICONTROL Permanent (301)]**— 向搜尋引擎指出此重新寫入是永久性的。 搜尋引擎通常會保留頁面排名資訊以供永久重寫。 |
| [!UICONTROL Description] | 說明重寫以供內部參考的用途。 |

{style="table-layout:auto"}
