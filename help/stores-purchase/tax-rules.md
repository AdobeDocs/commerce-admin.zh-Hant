---
title: 稅捐規則
description: 瞭解如何使用產品類別、客戶類別及稅率來定義稅捐規則。
exl-id: 38d65998-7769-49ce-9814-e65df9d77bba
feature: Taxes, Currency
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 0%

---

# 稅捐規則

稅捐規則整合了產品類別、客戶類別及稅率的組合。 每個客戶都會被指定至一個客戶類別，而每個產品都會被指定至一個產品類別。 Commerce會分析每個客戶的購物車，並根據客戶、產品類別及地區計算適當的稅捐。 區域以客戶的送貨地址、帳單地址或送貨來源為依據。

>[!NOTE]
>
>當必須定義許多稅率時，您可以透過匯入來簡化處理。

![稅捐規則](./assets/tax-rules.png){width="600" zoomable="yes"}

## 步驟1：完成稅捐規則資訊

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**.

1. 在右上角，按一下 **[!UICONTROL Add New Tax Rule]**.

1. 在 _稅捐規則資訊_，輸入 **[!UICONTROL Name]** 用於新規則。

   ![稅捐規則資訊](./assets/tax-rule-information.png){width="600" zoomable="yes"}

1. 選擇 **[!UICONTROL Tax Rate]** 適用於此規則的屬性。

   若要編輯現有稅率，請執行下列步驟：

   - 暫留在稅率上，然後按一下 _編輯_ ![鉛筆圖示](../assets/icon-edit-pencil.png) 圖示。

   - 視需要更新表單，然後按一下 **[!UICONTROL Save]**.

1. 若要輸入稅率，請使用下列其中一種方式：

### 方式1：手動輸入稅率

1. 按一下 **[!UICONTROL Add New Tax Rate]**.

1. 視需要填寫表單(請參閱 [稅捐區與稅率](tax-zones-rates.md))。

1. 完成後，按一下 **[!UICONTROL Save]**.

   ![新稅率](./assets/tax-rate-create-new.png){width="600" zoomable="yes"}

### 方法2：匯入稅率

1. 向下捲動至頁面底部的區段。

1. 若要匯入稅率，請執行下列步驟：

   - 按一下 **[!UICONTROL Choose File]** 並導覽至CSV檔案，其中包含要匯入的稅率。

   - 按一下 **[!UICONTROL Import Tax Rates]**.

1. 若要匯出稅率，請按一下 **[!UICONTROL Export Tax Rates]** (請參閱 [匯入/匯出稅率](../systems/data-transfer-tax-rates.md))。

![匯入/匯出稅率](./assets/tax-rule-new-import-export.png){width="600" zoomable="yes"}

## 步驟2：完成其他設定

1. 若要開啟區段，請按一下 **[!UICONTROL Additional Settings]**.

   ![稅捐規則的額外設定](./assets/tax-class-additional-settings.png){width="600" zoomable="yes"}

1. 選擇 **[!UICONTROL Customer Tax Class]** 要套用規則的。

   - 若要編輯客戶稅捐類別，請按一下 _編輯_ ![鉛筆圖示](../assets/icon-edit-pencil.png) 圖示，視需要更新表單，然後按一下 **[!UICONTROL Save]**.

   - 若要建立稅捐類別，請按一下 **[!UICONTROL Add New Tax Class]**，視需要填寫表單，然後按一下 **[!UICONTROL Save]**.

1. 選擇 **[!UICONTROL Product Tax Class]** 要套用規則的。

   - 若要編輯產品稅捐類別，請按一下 _編輯_ ![鉛筆圖示](../assets/icon-edit-pencil.png) 圖示，視需要更新表單，然後按一下 **[!UICONTROL Save]**.

   - 若要建立稅捐類別，請按一下 **[!UICONTROL Add New Tax Class]**，視需要填寫表單，然後按一下 **[!UICONTROL Save]**.

1. 如果套用多個稅捐，請輸入數字以表示此稅捐的優先順序 **[!UICONTROL Priority]**.

   如果套用具有相同優先順序的兩個稅捐規則，則會新增稅捐。 如果套用兩個具有不同優先順序設定的稅捐，這些稅捐就會複合。

1. 如果您希望稅捐是以訂單小計為基礎，請選取 **[!UICONTROL Calculate off Subtotal Only]** 核取方塊。

1. 的 **[!UICONTROL Sort Order]**，輸入數字，以表示此稅捐規則與其他稅捐規則一起列出的順序。

1. 完成後，按一下 **[!UICONTROL Save Rule]**.

## 幣別與稅捐規則示範

觀看此影片，瞭解如何管理貨幣和稅捐規則：

>[!VIDEO](https://video.tv.adobe.com/v/343657/?quality=12)
