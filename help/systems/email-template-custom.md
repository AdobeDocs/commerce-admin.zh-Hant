---
title: 自訂電子郵件範本
description: 瞭解如何為每個網站、商店或商店檢視自訂電子郵件範本。
exl-id: d328b84d-fab7-4956-9071-2d8848f7c21e
feature: Communications, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1277'
ht-degree: 0%

---

# 自訂電子郵件範本

Commerce會針對系統所傳送的每則訊息，在正文區段加入預設電子郵件範本。 內文內容的範本會與頁首和頁尾範本結合，以建立完整的訊息。 內容使用HTML和CSS格式化，並可透過新增輕鬆編輯和自訂 [變數](variables-predefined.md) 和 [Widget](../content-design/widgets.md). 您可以為每個網站、商店或商店檢視自訂電子郵件範本。 如果使用自訂範本，請務必更新 [系統組態](email-templates.md#configure-email-templates) 以確保使用正確的範本。

![範例 — 歡迎電子郵件預覽](./assets/email-template-preview.png){width="500" zoomable="yes"}

預設範本包含您的標誌和商店資訊，且不需進一步自訂即可使用。 然而，最佳實務是檢視每個範本，並在傳送給客戶之前進行任何必要的變更。

- [頁首範本](email-template-custom.md#header-template)
- [頁尾範本](email-template-custom.md#footer-template)
- [訊息範本](email-template-custom.md#message-templates)

![電子郵件範本](./assets/email-templates.png){width="700" zoomable="yes"}

## 範本資訊

| 欄位 | 說明 |
| ----- | ----------- |
| [!UICONTROL Template Name] | 自訂範本的名稱。 |
| [!UICONTROL Insert Variable] | 在範本的游標位置插入變數。 |
| [!UICONTROL Template Subject] | 範本主旨會顯示在「主旨」欄中，可用來排序和篩選清單中的範本。 |
| [!UICONTROL Template Content] | HTML中的範本內容。 |
| [!UICONTROL Template Styles] | 任何格式化範本所需的CSS樣式宣告，都可以在 _[!UICONTROL Template Styles]_方塊。 |

{style="table-layout:auto"}

## 頁首範本

完成 [設定](email-templates.md#configure-email-templates)，電子郵件標題範本包含連結至商店的標誌。 如果您具備HTML的基本知識，便可輕鬆使用 [預先定義的變數](variables-predefined.md) 以新增商店聯絡資訊至標題。

### 步驟1. 載入預設範本

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. 按一下 **[!UICONTROL Add New Template]**.

1. 在 **[!UICONTROL Load default template]** 區段，按一下 **[!UICONTROL Template]** 選擇器並選擇 `Magento_Email` > `Header`.

   ![電子郵件範本標題 — 載入預設範本](./assets/email-template-select-default-header.png){width="600" zoomable="yes"}

1. 按一下 **[!UICONTROL Load Template]**.

   範本中的HTML程式碼和變數會顯示在表單中。

### 步驟2. 自訂範本

1. 輸入 **[!UICONTROL Template Name]** 用於自訂標頭。

1. 輸入 **[!UICONTROL Template Subject]** 協助組織範本。

   在格線中，範本清單可依 _[!UICONTROL Subject]_欄。

   ![電子郵件範本標題資訊](./assets/email-template-information.png){width="600" zoomable="yes"}

1. 在 **[!UICONTROL Template Content]** 方塊，視需要修改HTML。

   >[!NOTE]
   >
   >在範本程式碼中工作時，請注意不要覆寫任何以雙大括弧括住的內容。

1. 若要插入 [變數](variables-reference.md)，將游標置於程式碼中要放置變數的位置，然後按一下 **[!UICONTROL Insert Variable]**.

1. 選擇要插入的變數。

   ![頁首範本 — 插入變數](./assets/email-template-insert-variable.png){width="600" zoomable="yes"}

   選取變數時， [標籤標籤](markup-tags.md) ，會將適用的變數插入程式碼中。

   雖然商店電子郵件地址變數是最常包含在標題中的變數，但您可以輸入任何系統的程式碼，或 [自訂變數](variables-custom.md) 直接放入範本。

1. 如果您需要做任何CSS宣告，請在以下位置輸入樣式： **[!UICONTROL Template Styles]** 方塊。

1. 當您準備好要檢閱您的工作時，請按一下 **[!UICONTROL Preview Template]**.

   對範本進行任何必要的變更。

1. 完成後，按一下 **[!UICONTROL Save Template]**.

   您的自訂標題現在會顯示在可用電子郵件範本的清單中。

### 步驟3. 更新設定

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. 在格線中，尋找要設定的存放區檢視，然後按一下 **[!UICONTROL Edit]** 在 _[!UICONTROL Action]_欄。

1. 向下捲動並展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Transactional Emails]** 區段。

1. 選擇 **[!UICONTROL Header Template]** 會作為電子郵件通知的預設值。

1. 完成後，按一下 **[!UICONTROL Save Config]**.

![異動電子郵件設計設定 — 標題範本](./assets/design-configuration-transactional-emails.png){width="600" zoomable="yes"}

## 頁尾範本

電子郵件範本頁尾包含電子郵件訊息的結尾和簽名行。 您可以變更結案以符合您的風格，並新增其他資訊，例如公司名稱和地址在您的名稱下方。

### 步驟1. 載入預設範本

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. 按一下 **[!UICONTROL Add New Template]**.

1. 在 **[!UICONTROL Load default template]** 區段，按一下 **[!UICONTROL Template]** 選擇器並選擇 `Magento_Email` > `Footer`.

1. 按一下 **[!UICONTROL Load Template]**.

   範本中的HTML程式碼和變數會顯示在表單中。

### 步驟2. 自訂和預覽範本

1. 輸入 **[!UICONTROL Template Name]** 用於自訂頁尾。

1. 輸入 **[!UICONTROL Template Subject]** 協助組織範本。

   在格線中，範本可依下列方式排序和篩選 _[!UICONTROL Subject]_欄。

   ![電子郵件範本頁尾 — 資訊](./assets/email-template-footer-information.png){width="600" zoomable="yes"}

1. 在 **[!UICONTROL Template Content]** 方塊，視需要修改HTML。

   >[!NOTE]
   >
   >在範本程式碼中工作時，請注意不要覆寫任何以雙大括弧括住的內容。

1. 若要插入 [變數](variables-reference.md)，將游標置於程式碼中要放置變數的位置，然後按一下 **[!UICONTROL Insert Variable]**.

1. 選擇要插入的變數。

   選取變數時， [標籤標籤](markup-tags.md) ，會將適用的變數插入程式碼中。

   雖然商店聯絡人變數是最常包含在頁尾中的變數，但您可以輸入任何系統的程式碼，或 [自訂變數](variables-custom.md) 直接放入範本。

1. 如果您需要做任何CSS宣告，請在以下位置輸入樣式： **[!UICONTROL Template Styles]** 方塊。

### 步驟3. 更新設定

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. 在格線中，尋找要設定的存放區檢視，然後按一下 **[!UICONTROL Edit]** 在 _[!UICONTROL Action]_欄。

1. 向下捲動並展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Transactional Emails]** 區段。

1. 選擇 **[!UICONTROL Footer Template]** 會作為電子郵件通知中的預設頁尾。

1. 完成後，按一下 **[!UICONTROL Save Config]**.

![異動電子郵件設計設定 — 頁尾範本](./assets/design-configuration-transactional-emails.png){width="600" zoomable="yes"}

## 訊息範本

自訂每則訊息本文的程式與自訂頁首或頁尾的程式相同。 唯一的差異在於每個觸發通知的活動或事件的訊息範本。 您可以照原樣使用範本，或自訂範本以符合您的聲音和品牌。 除了範本文字之外，還允許進行多種選擇 [預先定義](variables-predefined.md) 變數和 [自訂](variables-custom.md) 您可以建立並整合至範本的變數。

### 步驟1. 載入預設範本

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. 按一下 **[!UICONTROL Add New Template]**.

   ![電子郵件範本 — 載入預設範本](./assets/email-templates-message-load-default.png){width="600" zoomable="yes"}

1. 執行下列動作：

   - 在 **[!UICONTROL Load default template]**，選擇 **[!UICONTROL Template]** 您想要自訂的專案。

   - 按一下 **[!UICONTROL Load Template]**.

### 步驟2. 自訂範本

1. 的 **[!UICONTROL Template Name]**，輸入自訂範本的名稱。

1. 如有需要，請變更 **[!UICONTROL Template Subject]**.

   這是訊息的第一行，預設為問候語。 您可以保持原樣，也可以輸入更清楚描述的內容。

1. 記下 **[!UICONTROL Currently Used For]** 範本的路徑，此路徑用於更新設定。

   ![電子郵件範本 — 範本資訊](./assets/email-template-message-information.png){width="600" zoomable="yes"}

1. 在 **[!UICONTROL Template Content]** 方塊，視需要修改HTML。

   內容包含HTML標籤、CSS指示、變數和文字的組合。

   >[!NOTE]
   >
   >在範本程式碼中工作時，請注意不要意外在程式碼中輸入雙大括弧。

1. 若要插入變數，請將游標置於您要該變數出現的程式碼中。

   變數的選取範圍會依範本而異，並包含允許的 [預先定義](variables-predefined.md) 和 [自訂](variables-custom.md) 變數（若有）。

1. 按一下 **[!UICONTROL Insert Variable]** 並選擇要插入的變數。

   插入變數的命令會以大括弧括住，並新增至游標位置的程式碼中。 例如：

   `customVar code=my_custom_variable`

1. 若要進行CSS宣告，請在下列位置輸入樣式： **[!UICONTROL Template Styles]**.

   ![電子郵件範本 — 新增自訂樣式](./assets/email-template-add-custom-styles-min.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >自訂樣式只有在以下情況下才會套用至電子郵件 `{{template config_path="design/email/header_template"}}` 中存在於 _[!UICONTROL Template Styles]_. 若要在沒有預設標頭範本的情況下使用自訂CSS，您必須在標題範本的以下位置提供它們： `<style>` HTML標籤。

### 步驟3. 更新設定

此 _[!UICONTROL Currently Used For]_階層連結軌跡會顯示範本的使用位置。 在此範例中，範本設定位於_[!UICONTROL Customer Configuration]_ 頁面，在 _[!UICONTROL Create New Account Options]_區段，以及_[!UICONTROL Default Welcome Email]_ 欄位。

- 頁面 - [!UICONTROL Customer Configuration]
- 區段 —  [!UICONTROL Create New Account Options]
- 欄位 —  [!UICONTROL Default Welcome Email]

1. 在 **[!UICONTROL Currently Used For]** 階層連結路徑，按一下連結以開啟範本設定頁面。

   ![目前的電子郵件範本](./assets/email-template-new-currently-used-for.png){width="600" zoomable="yes"}

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 區段，並尋找您自訂之電子郵件範本的欄位。

1. 清除 **[!UICONTROL Use system value]** 核取方塊，然後按一下自訂範本的名稱。

   ![客戶設定 — 預設歡迎電子郵件範本](./assets/email-template-message-configuration-default-template.png){width="600" zoomable="yes"}

1. 完成後，按一下 **[!UICONTROL Save Config]**.

1. 在工作區頂端的訊息中，按一下 **[!UICONTROL Cache Management]** 並清除任何無效的快取。

### 步驟4. 預覽並儲存範本

1. 當您準備好要檢閱您的工作時，請按一下 **[!UICONTROL Preview Template]**.

1. 視需要更新範本。

1. 完成後，按一下 **[!UICONTROL Save Template]**.

   您的自訂範本現在可在電子郵件範本清單中使用。
