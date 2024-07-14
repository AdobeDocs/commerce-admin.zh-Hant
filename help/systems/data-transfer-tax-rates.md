---
title: 更新稅率資料
description: 瞭解如何使用匯出和匯入作業來更新商店的稅率。
exl-id: a3ef718d-b296-41d7-a1b8-ae8274da71b6
feature: Taxes, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 0%

---

# 更新稅率資料

如果您在數個州經營業務，並出貨大量產品，則手動輸入稅率會非常耗時。 透過郵遞區號下載稅率並將其匯入Commerce會更快更有效率。 下列範例顯示如何匯入從信任來源下載的一組特定州稅率。 Avalara提供您免費下載的[稅率表](https://www.avalara.com/taxrates/en/download-tax-tables.html)，適用於美國的每個郵遞區號。

>[!NOTE]
>
>如果您有興趣自動化銷售及使用稅捐法規遵循與申報功能，可在[Commerce合作夥伴](https://solutionpartners.adobe.com/s/directory/?solution=commerce)網站上找到Commerce信任的選項。

## 步驟1：匯出Commerce稅率資料

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import/Export Tax Rates]**。

1. 按一下&#x200B;**[!UICONTROL Export Tax Rates]**。

1. 在網頁瀏覽器的下載位置中尋找檔案。

1. 儲存並在試算表中開啟檔案。

   此範例使用[!DNL OpenOffice Calc]。

   匯出的Commerce稅率資料包含下列欄位：
   - 程式碼
   - 國家
   - 狀態
   - Zip/Post代碼
   - 評等
   - 範圍從
   - 範圍至
   - 每個商店檢視的欄

   ![匯出的資料 — 稅率](./assets/data-exported-tax-rates.png){width="500" zoomable="yes"}

1. 在試算表的第二個例項中開啟新的稅率資料，以便您並排檢視。

1. 在新稅率資料中，請記下在匯入資料之前，您可能需要在存放區中設定的任何其他稅率資料。

   例如，加州的稅率資料也包含：

   - `TaxRegionName`
   - `CombinedRate`
   - `StateRate`
   - `CountyRate`
   - `CityRate`
   - `SpecialRate`

   如果您需要匯入其他[稅捐區域和稅率](../stores-purchase/tax-zones-rates.md)，您必須先從商店的管理員定義它們，並視需要更新[稅捐規則](../stores-purchase/tax-rules.md)。 然後，匯出資料並在文字編輯器中開啟檔案，以便用作參考。 不過，為了簡化此範例，我們只匯入標準稅率欄。

## 步驟2：準備匯入資料

您有兩個並排開啟的試算表。 一個包含Commerce匯出檔案結構，另一個包含您要匯入的新稅率資料。

1. 若要在試算表中建立使用新稅率資料的位置，請視需要在最右側插入任意數量的空白欄，以便從Commerce匯出檔案新增資料。 使用剪下並貼上來新增資料，然後重新排列欄，使其與Commerce匯出資料檔案的順序相符。

1. 重新命名欄標題以符合Commerce匯出資料。

1. 刪除任何沒有資料的欄。

   否則，匯入檔案的結構應該與原始Commerce匯出資料相符。

1. 儲存檔案之前，請向下捲動並確保稅率欄只包含數值資料。

   在「稅率」欄中找到的任何文字，都會阻止匯入資料。

1. 將準備好的資料儲存為.CSV檔案。

   出現提示時，請確認逗號是做為欄位分隔符號，而雙引號是做為文字分隔符號。 然後按一下&#x200B;**[!UICONTROL OK]**。

## 步驟3：匯入稅率

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import/Export Tax Rates]**。

1. 按一下&#x200B;**[!UICONTROL Choose File]**，然後選擇您準備匯入的CSV稅率檔案。

1. 按一下&#x200B;**[!UICONTROL Import Tax Rates]**。

   匯入資料可能需要幾分鐘的時間。 當程式完成時，會顯示`The tax rate has been imported`訊息。 如果您收到錯誤訊息，請更正資料中的問題並重試。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**。

   匯入的費率會顯示在清單中。

1. 使用頁面控制項來檢視新的稅率。

   ![資料匯入稅率](../stores-purchase/assets/tax-zones-rates.png){width="600" zoomable="yes"}

1. 在您的商店中與不同郵遞區號的客戶進行一些測試交易，以確保新稅率正確運作。
