---
title: 傳回屬性
description: 瞭解退貨屬性，以及如何建立處理商店退貨所需的屬性。
exl-id: 639c1e94-1211-4a4e-8599-e54ed99b2355
feature: Attributes, Returns
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# 傳回屬性

{{ee-feature}}

退貨屬性是用來儲存產品退貨程式期間所需的資訊。 預設屬性包括傳回產品的條件、傳回原因，以及指出如何解決傳回的欄位。 建立退貨屬性的程式與建立 [客戶屬性](../customers/attribute-properties.md).

![管理員 — 傳回屬性](./assets/attribute-returns.png){width="700" zoomable="yes"}

## 建立傳回屬性

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Returns]**.

1. 在右上角，按一下 **[!UICONTROL Add New Attribute]**.

   ![新傳回 — 屬性屬性](./assets/attribute-returns-new-properties.png){width="600" zoomable="yes"}

### 定義屬性

1. 若要在資料輸入期間識別屬性，請設定 **[!UICONTROL Default Label]**.

1. 的 **[!UICONTROL Attribute Code]**，輸入在系統中識別屬性的程式碼。

1. 若要判斷用於資料輸入的輸入控制項型別，請設定 **[!UICONTROL Input Type]** 變更為下列其中一項：

   - `Text Field`
   - `Text Area`
   - `Dropdown`
   - `Yes/No`
   - `File`
   - `Image File`

1. 若要讓欄位成為必要專案，請設定 **[!UICONTROL Values Required]** 至 `Yes`.

1. 若要指派初始值給欄位，請輸入 **[!UICONTROL Default Value]**.

1. 若要在儲存記錄之前驗證輸入到欄位中的資料是否準確，請設定 **[!UICONTROL Input Validation]** 變更為下列其中一項：

   - `None`
   - `Alphanumeric`
   - `Alphanumeric with Space`
   - `Numeric Only`
   - `Alpha Only`
   - `URL`
   - `Email`

1. 對於 `Text Field` 和 `Text Area` 輸入型別，輸入 **[!UICONTROL Minimum Text Length]** 和 **[!UICONTROL Maximum Text Length]**.

1. 若要套用前置處理篩選，請設定 **[!UICONTROL Input/Output Filter]** 變更為下列其中一項：

   - `None`
   - `Strip HTML Tags`
   - `Escape  HTML Entities`

1. 若要讓客戶看到屬性，請設定 **[!UICONTROL Show on Storefront]** 至 `Yes` 在 _[!UICONTROL Storefront Properties]_區段。

1. （選用） For **[!UICONTROL Sort Order]**，請輸入數字以決定此屬性在頁面同一部分中相對於其他屬性的顯示位置。 (`0` =第一個， `1` =秒， `2` =第三個，依此類推。)

### 管理標籤/選項

1. 在左側面板中，選擇 **[!UICONTROL Manage Labels/Options]**.

1. 在 **[!UICONTROL Manage Titles (Size, Color, etc.)]** 區段，輸入每個商店檢視的標籤。

   ![管理標籤](./assets/return-attributes.png){width="600" zoomable="yes"}

1. 如果 **[!UICONTROL Input Type]** 屬性為 `Dropdown`，管理中的選項 **[!UICONTROL Manage Options (Values of Your Attribute)]** 區段。

   - 若要新增選項，請按一下 **[!UICONTROL Add Option]** 並為管理員和每個商店檢視輸入標籤。
   - 若要將選項設為選取的預設，請選擇 **[!UICONTROL Is Default]**.
   - 若要移除選項，請按一下 **[!UICONTROL Delete]**.

1. 若要儲存變更，請按一下 **[!UICONTROL Save Attribute]**.
