---
title: 新增自訂變數
description: 瞭解如何建立自訂變數，並將其插入頁面、區塊和產品內容中。
exl-id: 8233518a-abcf-4889-b75b-4aa503c7cebb
role: Admin, User
feature: System, Variables, Page Content, Communications
TQID: https://experienceleague.adobe.com/zhgemfdr2g5sanaFuiF9l20figj9ZD-3codE97WWWg8
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 344
ht-degree: 1%

---

# 新增自訂變數

為了滿足您企業的特定需求，您可以建立自訂變數，並將其插入到[頁面](../content-design/pages.md)、[區塊](../content-design/blocks.md)和[電子郵件範本](email-templates.md)中。 按一下&#x200B;_插入變數_&#x200B;按鈕時出現的允許變數清單包含[預先定義的](variables-predefined.md)和自訂變數。 特定電子郵件範本的可用變數清單取決於與範本相關聯的資料。 請參閱[變數參考資料](variables-reference.md)，以取得常用電子郵件範本及其相關變數的清單。

![自訂變數](./assets/variables-custom.png){width="600" zoomable="yes"}

>[!NOTE]
>
>只有允許的預定義或自訂變數才能用於電子郵件和電子報範本。

## 步驟1：建立自訂變數

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Custom Variables]**。

1. 按一下&#x200B;**[!UICONTROL Add New Variable]**。

1. 輸入&#x200B;**[!UICONTROL Variable Code]**&#x200B;的識別碼，使用不含空格的所有小寫字元。

   如有需要，您可以使用底線字元或連字型大小來代表空格。 例如： `my_custom_variable`

1. 輸入用於內部參考的&#x200B;**[!UICONTROL Variable Name]**。 例如： `My Custom Variable`

1. 若要輸入與變數相關聯的值，請執行下列任一項作業：

   - 針對&#x200B;**[!UICONTROL Variable HTML Value]**，輸入使用簡單HTML標籤格式化的變數值。 例如：

     `<b>This formatted content appears in place of the variable.</b>`

   - 針對&#x200B;**[!UICONTROL Variable Plain Value]**，以純文字格式輸入變數值，但不設定格式。 例如：

     `This unformatted content appears in place of the variable.`

   >[!TIP]
   >
   >如果您需要更多空間，請拖曳文字方塊的右下角。

   ![新的自訂變數](./assets/variable-custom-add.png){width="600" zoomable="yes"}

1. 完成時，按一下&#x200B;**[!UICONTROL Save]**。

## 步驟2：在內容中插入自訂變數

使用[!DNL Page Builder]插入自訂變數。

1. 開啟您要新增變數至內容的頁面、區塊、類別或產品。

1. 展開&#x200B;**[!UICONTROL Content]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

1. 按一下&#x200B;**[!UICONTROL Edit with Page Builder]**。

1. 在左側面板中，按一下&#x200B;**[!UICONTROL Elements]**&#x200B;並執行下列任一項作業：

   - 在要插入變數的現有文字區域中按一下。

   - 將新的&#x200B;**[!UICONTROL Text]**&#x200B;物件拖曳到舞台。

1. 在編輯器工具列的最右側，按一下（![插入變數](./assets/editor-btn-insert-variable.png) ）以插入變數。

   ![[!DNL Page Builder]階段和面板](./assets/variable-custom-pagebuilder-stage.png){width="600" zoomable="yes"}

1. 在清單中，選取您要插入的自訂變數，然後按一下&#x200B;**[!UICONTROL Insert Variable]**。

   ![新的自訂變數](./assets/variable-custom-insert-select.png){width="600" zoomable="yes"}

   變數識別碼會在編輯器中顯示為預留位置。

   ![[!DNL Page Builder]階段 — 變數預留位置](./assets/pagebuilder-variable-inserted.png){width="600" zoomable="yes"}

1. 完成時，按一下&#x200B;**[!UICONTROL Save]**。
