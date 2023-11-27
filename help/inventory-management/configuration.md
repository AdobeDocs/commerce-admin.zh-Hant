---
title: "設定 [!DNL Inventory Management]"
description: 瞭解的設定 [!DNL Inventory Management] 決定來源可用性、店面產品和訂單出貨的選項。
exl-id: 1696999e-77b1-45c7-9b0b-dd1512427cff
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '739'
ht-degree: 0%

---

# 設定 [!DNL Inventory Management]

此 [!DNL Inventory Management] 模組支援產品及全域層級的存貨組態設定，並提供會影響來源可用性、店面產品及訂單出貨的其他設定。 組態設定套用至：

- 整個目錄：前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**. 然後，展開&#x200B;**[!UICONTROL Catalog]**在左側面板中並選取「 」**[!UICONTROL Inventory]**.

- 特定產品：前往 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**. 然後，在編輯模式中開啟產品並按一下 **[!UICONTROL Advanced Inventory]** 在 _[!UICONTROL Sources]_區段。

您可以將目錄設定為在店面中顯示詳細目錄資料、管理使用中的購物車等。 將每個專案的可用性顯示為 _有貨_ 或 _無庫存_ 以及庫存不足時的可用存貨。

缺貨臨界值表示產品何時應重新訂購、從庫存的「可銷售數量」中減去數量，並可設定為支援啟用或停用的延期交貨。 允許您的商店延期交貨，設定所有或特定產品的訂單數量上限。

您可以使用庫存可用性臨界值的另一種方式是管理需求高的產品。 如果您想要抓取新客戶，而不是銷售給大量採購員，您可以設定最大數量，以防止單一採購員取出您的全部存貨。

![有庫存的範例，只剩下1個](assets/storefront-stock-options-1-left.png)

## 設定選項

[!DNL Commerce] 存放區和產品支援以下管理產品、詳細目錄、通知等的設定。 [!DNL Commerce] 提供大量動作和「距離優先順序」演演算法的其他組態設定。

| 選項 | 說明 |
|--|--|
| [!UICONTROL Manage Stock] | 啟用 [!DNL Commerce] 以管理所有詳細目錄。 若此產品或此專案中的所有產品都使用存貨控制，則請設定 [!DNL Commerce]. 設定為時顯示更多選項 `Yes`. |
| [!UICONTROL Only X left Threshold] | 設定特定金額可購買時通知的數量。 此金額會在庫存層級進行追蹤。 |
| [!UICONTROL Out-of-Stock Threshold] | 您的安全存量、觸發缺貨通知並減輕缺貨風險的數量。 此值會影響延期交貨。 選項：<br />**[!UICONTROL No Backorders]**：當產品無庫存時，不接受延期交貨。<br />**[!UICONTROL Allow Qty Below 0]**：當數量低於零時，接受延期交貨。<br />**[!UICONTROL Allow Qty Below 0 and Notify Customer]**：當數量低於零時接受延期交貨，但通知客戶仍可下訂單。<br /><br />**[!UICONTROL Backorders disabled]**：建議輸入大於0的正值，例如5或25。 <br/>**[!UICONTROL Backorders enabled]**：輸入允許延期交貨數量上限的負數臨界值，例如–5或–25。 0的值會做為無限庫存。 系統會忽略正值，並將其視為0。 |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | 設定單一訂單可購買之產品的最小數量。 |
| [!UICONTROL Maximum Qty Allowed in Shopping Cart] | 設定單一訂單可購買之產品的最大數量。 |
| [!UICONTROL Qty Uses Decimals] | 允許產品數量的小數金額，而不是整數。 此設定對依重量、體積或長度銷售的產品很有幫助。 在來源層級指定，根據指定的來源在庫存層級上計算。 |
| [!UICONTROL Allow Multiple Boxes for Shipping] | 決定產品的零件是否可以單獨出貨。 出現以下情況時可看見此選項： **[!UICONTROL Qty Uses Decimals]** = `Yes`. |
| [!UICONTROL Backorders] | 顯示是否允許延期交貨。 在來源層級指定，根據指定的來源在庫存層級上計算。 如果已啟用允許延期交貨，請為「缺貨臨界值」設定負值(請參閱 [設定延期交貨](backorders.md))。 選項：<br />**[!UICONTROL No Backorders]**：當產品無庫存時，不接受延期交貨。<br />**[!UICONTROL Allow Qty Below 0]**：當數量低於零時，接受延期交貨。<br />**[!UICONTROL Allow Qty Below 0 and Notify Customer]**：當數量低於零時接受延期交貨，但通知客戶仍可下訂單。 |
| [!UICONTROL Notify for Quantity Below] | 設定觸發「低於數量」通知的數量，警告庫存不足。 此金額是從「可銷售數量」扣除，而非從「存貨數量」扣除。 |
| [!UICONTROL Enable Qty Increments] | 決定產品是否可以數量遞增方式銷售。 如果啟用，請輸入必須以累加步驟購買的產品數量。 |
| [!UICONTROL Automatically Return Credit Memo Item to Stock] | [!DNL Inventory Management] 不會使用此值。 當您完成退貨或銷退折讓單時，產品數量會自動退回至受影響的來源數量。 另請參閱 [設定產品選項](product-options.md). |

## 設定回覆和繼承

設定會覆寫或套用至下列繼承路徑：產品 _[!UICONTROL Sources]_區段會覆寫產品_[!UICONTROL Advanced Options]_ 覆寫全域 _[!UICONTROL Inventory]_存放區設定。

時間 [!DNL Commerce] 檢查要套用的自訂設定，其順序如下：

1. 檢查中的產品層級自訂設定 _[!UICONTROL Sources]_區段。 有一些設定可供使用。

1. 檢查產品 _[!UICONTROL Advanced Inventory]_設定。

1. 如果 `Use Config Settings` ，則會檢查全域中的值 _詳細目錄_ 存放區設定頁面。

例如，您可以使用類似下列的設定，以不同方式設定商店中的延期交貨：

- _全域：_ 啟用商店的延期交貨，將「無庫存臨界值」設定為 `-50`

- _產品：_ 停用特定產品的延期交貨，將「缺貨臨界值」設定為 `10`
