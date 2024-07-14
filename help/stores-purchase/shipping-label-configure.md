---
title: 設定送貨標籤
description: 瞭解如何設定商店以產生配送標籤。
exl-id: 0693d74b-8b36-4a36-8739-c9fe5a934ff0
feature: Shipping/Delivery, Orders
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 0%

---

# 設定送貨標籤

下列設定必須在產品層級，以及在每個用於列印標籤之電信業者的組態中進行。 若要列印標籤，所有電信業者都要求您開立帳戶。 然後，針對您打算使用的每個電信業者，完成您商店中的設定。

## 電信業者需求

| [!UICONTROL Carrier] | 需求 |
|-------|--------|
| [USPS](usps.md) | 需要USPS帳戶。 自2018年2月23日起，USPS要求所有運送標籤皆須包含郵資。 |
| [UPS](ups.md) | 需要UPS帳戶。 出貨標籤僅適用於產自美國特定證明的出貨。美國以外的商店需要此證明資料。 |
| [FedEx](fedex.md) | 需要FedEx帳戶。 對於美國以外的商店，僅支援國際出貨的運送標籤。 FedEx不允許源自美國境外的國內出貨 |
| [DHL](dhl.md) | 需要DHL帳戶。 僅支援源自美國的出貨標籤。 |

{style="table-layout:auto"}

## 步驟1：確認製造國家

USPS和FedEx國際出貨的所有產品都需要有製造國家/地區。 如果您有許多產品需要更新，您可以[匯入](../systems/data-import.md)更新，或使用詳細目錄格線來更新多個記錄。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Products]**。

1. 使用下列其中一種方法更新送貨標籤記錄。

### 方法1：更新單一記錄

1. 在格線中，尋找要更新的產品，並以編輯模式開啟。

1. 視需要更新&#x200B;**製造國家**。

   ![製造國家/地區](./assets/product-country-of-manufacture.png){width="700" zoomable="yes"}

1. 按一下&#x200B;**[!UICONTROL Save]**。

### 方法2：更新多個記錄

1. 在格線中，選取每個要更新之產品的核取方塊。

   例如，在中國製造的所有產品。

1. 將&#x200B;**[!UICONTROL Actions]**&#x200B;控制項設為`Update Attributes`並按一下&#x200B;**[!UICONTROL Submit]**。

1. 在&#x200B;_更新屬性_&#x200B;表單中，尋找&#x200B;**製造國家**&#x200B;欄位，並選取&#x200B;**變更**&#x200B;核取方塊。

1. 選擇國家/地區。

1. 按一下&#x200B;**[!UICONTROL Save]**。

## 步驟2驗證商店資訊

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Sales]**&#x200B;並選擇&#x200B;**[!UICONTROL Shipping Settings]**。

1. 展開![展開選取器](../assets/icon-display-expand.png) **[!UICONTROL Origin]**&#x200B;區段，然後確認下列欄位是否已完成：

   - **[!UICONTROL Street Address]** — 出貨的寄件地街道地址。 例如，公司或倉儲的位置。 送貨標籤需要此欄位。
   - **[!UICONTROL Street Address Line 2]** — 任何其他地址資訊，例如樓層或入口。 建議使用此欄位。

   ![來源](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. 在左側面板的&#x200B;_銷售_&#x200B;區段中，選擇&#x200B;**[!UICONTROL Delivery Methods]**。

1. 展開![展開選取器](../assets/icon-display-expand.png) **[!UICONTROL USPS]**&#x200B;區段，然後確認下列欄位是否已完成：

   - **[!UICONTROL Secure Gateway URL]** — 系統會自動進入閘道URL。
   - **[!UICONTROL Password]** — 密碼由USPS提供，可讓您透過Web服務存取其系統。
   - **長度、寬度、高度、周長** — 封裝的預設尺寸。 若要顯示這些欄位，請將&#x200B;**[!UICONTROL Size]**&#x200B;設為`Large`。

1. 展開![擴充選擇器](../assets/icon-display-expand.png) **FedEx**&#x200B;區段，並確認下列欄位是否完整：

   - 計量器編號
   - 索引鍵
   - 密碼

   此資訊由電信業者提供，是透過Web服務存取其系統所需。

1. 在左側面板中，展開&#x200B;**[!UICONTROL General]**&#x200B;並在下方選擇&#x200B;**[!UICONTROL General]**。

1. 展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Store Information]**&#x200B;區段，並確認下列欄位是否已完成：

   - **[!UICONTROL Store Name]** — 存放區或存放區檢視的名稱。
   - **[!UICONTROL Store Contact Telephone]** — 商店或商店檢視的主要連絡人電話號碼。
   - **[!UICONTROL Country]** — 您的商店所在的國家/地區。
   - **[!UICONTROL VAT Number]** — 若適用的話，為您的商店加值稅編號。 （位於美國的商店不需要）
   - **[!UICONTROL Store Contact Address]** — 商店或商店檢視的主要連絡人的街道地址。

1. 如果您有多個商店，且連絡資訊與預設值不同，請為每個設定&#x200B;**[!UICONTROL Store View]**，並確認資訊是否完整。

   如果資訊遺失，當您嘗試列印標籤時會出現錯誤。

   ![存放區資訊](../configuration-reference/general/assets/general-store-information.png){width="600" zoomable="yes"}

1. 按一下&#x200B;**[!UICONTROL Save Config]**。
