---
title: 稅捐區與稅率
description: 瞭解如何針對您收稅和匯款的每個地理區域定義稅率。
exl-id: d8eb0743-d277-438d-91ed-fc711a6ba3ae
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 0%

---

# 稅捐區與稅率

稅率通常適用於在特定地理區域內發生的交易。 使用 _稅捐區與稅率_ 此工具可針對您徵收及匯出稅捐的每個地理區域指定稅率。 因為每個稅捐區和稅率都有唯一識別碼，所以您可以針對特定地理區域使用多種稅率（例如不徵收食物或藥品稅捐但會徵收其他專案稅捐的區域）。

根據商店地址計算商店稅金。 在客戶完成訂單資訊之後，計算訂單的實際客戶稅捐。 然後Commerce會根據商店的稅捐設定來計算稅捐。

![稅捐區與稅率](./assets/tax-zones-rates.png){width="600" zoomable="yes"}

## 定義新的稅率

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

1. 在右上角，按一下 **[!UICONTROL Add New Tax Rate]**.

   ![新稅率](./assets/tax-rate-new.png){width="600" zoomable="yes"}

1. 輸入 **[!UICONTROL Tax Identifier]**.

1. 若要將稅率套用至單一郵遞區號，請輸入 **[!UICONTROL Zip/Post Code]**.

   星號萬用字元(`*`)可用來比對程式碼中最多十個字元。 例如， `90*` 代表從90000到90999的所有郵遞區號。

1. 若要將稅率套用至某個郵遞區號範圍，請執行下列步驟：

   - 選取 **[!UICONTROL Zip/Post is Range]** 核取方塊，並輸入第一個和最後一個郵遞區號來定義範圍 **[!UICONTROL Range From]** 和 **[!UICONTROL Range To]**.

     ![ZIP/Post為範圍](./assets/tax-rate-new-zip-post-range.png){width="600" zoomable="yes"}

   - 選擇 **[!UICONTROL State]** 適用稅率的位置。

   - 選擇 **[!UICONTROL Country]** 適用稅率的位置。

   - 輸入 **[!UICONTROL Rate Percent]** 用於稅率計算。

1. 如果您有多個商店，您可以設定 **[!UICONTROL Tax Titles]** 適用於每個商店檢視。

   >[!NOTE]
   >
   >如果您要使用稅捐識別碼，請將此欄位留空。

1. 完成後，按一下 **[!UICONTROL Save Rate]**.

## 編輯現有稅率

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

1. 在「 」中尋找稅率 _[!UICONTROL Tax Zones and Rates]_格線，然後在編輯模式中開啟記錄。

   如果清單中有許多費率，請使用 [篩選控制項](../getting-started/admin-grid-controls.md) 以找出所需的費率。

1. 進行必要的變更 **[!UICONTROL Tax Rate Information]**.

1. 更新 **[!UICONTROL Tax Titles]** 視需要。

1. 完成後，按一下 **[!UICONTROL Save Rate]**.

## 刪除稅率

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

1. 尋找要刪除的稅率，並在編輯模式中開啟。

1. 在功能表列中，按一下 **[!UICONTROL Delete Rate]**.

1. 若要確認動作，請按一下 **[!UICONTROL OK]**.
