---
title: 贈品登入設定
description: 瞭解如何為商店客戶設定禮品登入型別。
exl-id: d618c769-10be-4881-a799-42484d35c57b
feature: Gift, Storefront
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '1084'
ht-degree: 0%

---

# 贈品登入設定

{{ee-feature}}

任何型別的活動，例如婚禮、生日、週年紀念日、新生嬰兒或其他任何特殊場合，都可以建立禮物登記簿。 依預設，Adobe Commerce包含下列特殊事件：

- 嬰兒
- 生日
- 婚禮

當您建立登入時，它就會成為客戶帳戶中禮品登入型別清單中的一個選項。

您可以使用三個準備好的禮品註冊之一，或建立您自己的自訂註冊。 每個禮品登入型態都包含數個屬性，這些屬性是客戶建立禮品登入時所完成的資料輸入欄位。 屬性會提供關於事件、時間和位置的額外資訊，或需要的任何其他資訊。 視輸入型別而定，某些屬性有多個選項。 例如， `Wedding` 贈品登入型別具有屬性 `Role`，使用 `Bride`， `Groom`、和 `Partner` 選項。 若要深入瞭解屬性和輸入型別，請參閱 [屬性](../customers/attribute-properties.md).

![贈品登入型別](./assets/gift-registry-types.png){width="700" zoomable="yes"}

## 使用準備好的禮品登入

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Gift Registry]**.

   生日、婚禮和嬰兒登記處已可供客戶從他們的帳戶中使用。

1. 請務必完成 [電子郵件範本設定](../systems/email-templates.md#configure-email-templates)，因此可反映您的品牌。

## 建立自訂贈品登入

1. 在管理員側邊欄上，前往 **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Gift Registry]**.

1. 在右上角，按一下 **[!UICONTROL Add Gift Registry Type]**.

1. 在 **[!UICONTROL General Information]**，請完成下列操作：

   - 輸入唯一值 **[!UICONTROL Code]** 在內部識別贈品登入。

     程式碼必須以小寫字母開頭。 程式碼的其餘部分可以是小寫字母(a-z)、數字(0-9)和底線(`_`)。

   - 的 **[!UICONTROL Label]**，輸入贈品登入的名稱，使其顯示在商店中。

     此標籤是客戶可用的禮品登入型別清單中的一個選項。

   - 的 **[!UICONTROL Sort Order]**，請輸入數字，以決定此贈品登入與其他型別一起列出時的顯示順序。

   - 若要啟動贈品登入，請設定 **[!UICONTROL Is Listed]** 至 `Yes`.

     ![禮品登入 — 一般資訊](./assets/gift-registry-new-general-information.png){width="600" zoomable="yes"}

1. 檢查贈品登入的每個區段，以決定您要包含的資訊型別。

1. 在左側面板中，選擇 **[!UICONTROL Attributes]** 並按一下 **[!UICONTROL Add Attribute]**.

   ![贈品登入 — 新屬性](./assets/gift-registry-type-new-attribute.png){width="600" zoomable="yes"}

1. 針對每個屬性，執行下列動作：

   - 指派唯一 **[!UICONTROL Code]** 以在內部識別屬性。 程式碼的長度最多可為15個字元，且必須以小寫字母開頭。 其餘的程式碼可包含小寫字母(`a`-`z`)，數字(`0`-`9`)和底線(`_`)字元分隔單字。

   - 選擇 **[!UICONTROL Input Type]** 用於資料輸入。 您可以使用其中一個自訂或靜態型別。

   - 如果輸入型別有多個選項，請按一下 **[!UICONTROL Add New Option]** 並填入每個選項的資訊。

     有些輸入型別具有其他屬性。 例如，「事件位置」有其他屬性可讓事件可供搜尋，並包含在商店的禮品註冊公開清單中。

      - 設定 **[!UICONTROL Attribute Group]** 到贈品登入中您想要顯示屬性的區段。

      - 的 **[!UICONTROL Label]**，輸入名稱以識別登入中的資料輸入欄位。

      - 如果客戶必須選取或在欄位中輸入值，請設定 **[!UICONTROL Is Required]** 至 `Yes`.

      - 的 **[!UICONTROL Sort Order]**，請輸入數字，以決定此禮品註冊與其他可能在商店中提供的禮品註冊一起列出時的顯示順序。

1. 若要新增其他選項，請按一下 **新增選項**.

   每個新增的選項都會顯示在頂端的新區段中。 對新屬性重複此程式。

1. 完成後，按一下 **[!UICONTROL Save]**.

## 欄位說明

### [!UICONTROL General Information]

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Code] | 可在內部識別贈品登入型別的唯一名稱。 程式碼的第一個字元必須是小寫字母。 其餘的程式碼可以是小寫字母(a-z)、數字(0-9)和底線字元(`_`)。 |
| [!UICONTROL Label] | 出現在商店中的贈品登入型別名稱。 |
| [!UICONTROL Sort Order] | 與其他型別一起列出時，決定此贈品登入型別的顯示順序。 |
| [!UICONTROL Is Listed] | 決定商店中的客戶是否可以使用贈品登入型別。 選項： `Yes` / `No`. |

{style="table-layout:auto"}

### [!UICONTROL Attributes]

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Code] | 可在內部識別屬性的唯一名稱。 程式碼可包含小寫字母(a-z)、數字(0-9)和底線字元(`_`)。 |
| [!UICONTROL Input Type] | 根據型別決定與屬性關聯的資料型別和輸入控制項。 |
| [!UICONTROL Attribute Group] | 選取屬性列在禮品登入中的群組。 |
| [!UICONTROL Label] | 在客戶的帳戶儀表板中識別屬性的名稱。 |
| [!UICONTROL Is Required] | 指示屬性是否為必要專案。 在完成所有必要屬性之前，無法儲存贈品登入。 選項： `Yes` / `No`. |
| [!UICONTROL Sort Order] | 決定與其他屬性一起列出時，屬性出現的順序。 |

{style="table-layout:auto"}

#### [!UICONTROL Input Type Options]

選取與屬性關聯的資料型別和輸入控制項。

**_[!UICONTROL Custom Types]_**

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Text] | 將屬性顯示為文字欄位。 |
| [!UICONTROL Select] | 以下拉式清單顯示屬性。 按一下 **[!UICONTROL Add New Option]** 若要將更多條件新增至下拉式清單：<br/>**[!UICONTROL Code]**— 可在內部識別屬性的唯一名稱。<br/>**[!UICONTROL Label]**  — 在客戶的帳戶儀表板中識別屬性的名稱。<br/>**[!UICONTROL Is Default]**— 設定此引數以選取預設條件。<br/>**[!UICONTROL Delete Option]**  — 按一下以刪除選項。 |
| [!UICONTROL Date] | 將屬性顯示為日期欄位。 選項： `Short (3/23/2014)` / `Medium (Mar 23, 1914)` / `Long (March 23, 1914)` / `Full (Sunday, March 23, 2014)` |
| [!UICONTROL Country] | 將屬性顯示為國家/地區的下拉式清單。 設定 **[!UICONTROL Show Region]** 至： `Yes` / `No`. |

{style="table-layout:auto"}

**_[!UICONTROL Static Types]_**

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Event Date] | 決定如何在存放區中使用日期屬性。 選項： <br/>**[!UICONTROL Searchable]**— 決定該屬性是否可用於進階搜尋。 選項： `Yes` / `No`.<br/>**[!UICONTROL Is Listed]**  — 決定事件是否包含在存放區中可用的事件清單中。 選項： `Yes` / `No`. <br/>**[!UICONTROL Date Format]**— 決定事件日期的格式。 選項： `Short (3/23/2014)` / `Medium (Mar 23, 1914)` / `Long (March 23, 1914)` / `Full (Sunday, March 23, 2014)` |
| [!UICONTROL Event Country] | 將屬性顯示為國家/地區清單。 選項： <br/>**[!UICONTROL Searchable]**— 決定該屬性是否可用於進階搜尋。 選項： `Yes` / `No`.<br/>**[!UICONTROL Is Listed]**  — 決定事件是否包含在存放區中可用的事件清單中。 選項： `Yes` / `No`. <br/>**[!UICONTROL Show Region]**— 決定事件的地區。 |
| [!UICONTROL Event Location] | 與贈品登入相關的事件位置。 <br/>設定 **[!UICONTROL Is Searcheable]** 至： `Yes` / `No` <br/>設定 **[!UICONTROL Is Listed]** 至： `Yes` / `No` |
| [!UICONTROL Role] | 識別贈品收件者的角色。 例如， `Bride`， `Groom`，或 `Partner`.<br/>**[!UICONTROL Is Searcheable]**— 設為 `Yes`/ `No`<br/>**&#x200B;已列出&#x200B;**— 設為 `Yes` / `No`<br/>**[!UICONTROL Add New Option]**  — 按一下以新增更多條件至下拉式功能表：<br/>**程式碼**  — 可在內部識別屬性的唯一名稱。<br/>**[!UICONTROL Label]**— 在客戶的帳戶儀表板中識別屬性的名稱。<br/>**[!UICONTROL Is Default]**  — 設定此引數以選取預設條件。<br/>**[!UICONTROL Delete Option]**— 按一下以刪除選項。 |

{style="table-layout:auto"}

#### [!UICONTROL Attribute Group Options]

選取屬性列在禮品登入中的群組。

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Event Information] | 將所有加入贈品登入事件、時間、地點等資訊的贈品登入屬性分組。 |
| [!UICONTROL Gift Registry Properties] | 結合所有屬性，這些屬性會直接新增贈品登入的相關資訊。 |
| [!UICONTROL Privacy Settings] | 列出新增禮品登入事件隱私權相關資訊的屬性。 |
| [!UICONTROL Recipients Information] | 將屬性分組，以提供建立贈品登入之人員的相關資訊。 |
| [!UICONTROL Shipping Address] | 結合可新增贈品註冊事件出貨地址相關資訊的屬性。 |

{style="table-layout:auto"}
