---
title: Negotiate a quote
description: 瞭解報價議價工作流程，以及如何與購買者合作進行購買。
exl-id: 93efbc9d-da4d-4ff8-95c1-13848b68bc38
feature: B2B, Quotes
source-git-commit: ec00288f33af2abb785d1b37dd67aaf1ebe35c06
workflow-type: tm+mt
source-wordcount: '2271'
ht-degree: 0%

---

# 交涉報價

如果組態中啟用了[B2B報價單](configure-quotes.md)，則價格議價可由公司授權採購員或銷售代表啟動。

買家透過向購物車要求[報價單](quote-request.md)來啟動價格議價程式。 [&#128279;](sales-rep-initiates-quote.md)

[&#128279;](quotes.md)All negotiation between the buyer and seller takes place by email, and is initiated and tracked from the detail view of the quote.

During the negotiation process, the seller can do the following from the Admin:

- Add or remove products
- Change the quantity
- 將折扣套用至明細專案或整個報價單
- 新增或變更送貨方法
- 新增註解
- 將更新後的報價單傳送給採購員，或另存為草稿

買方使用[[!UICONTROL My Quotes]](account-dashboard-my-quotes.md)從店面管理報價議價程式。 當報價單處於未結複查狀態時，其在購買者帳戶中的狀態設定為`Pending`。 即使報價已遭拒絕或已過期，採購員仍可變更並重新提交報價。

## 步驟1：檢視請求

1. 在管理員側邊欄上，前往&#x200B;**[!UICONTROL Sales]** > **[!UICONTROL Quotes]**。

   新要求會出現在&#x200B;_[!UICONTROL Quotes]_&#x200B;格線中。

1. 在&#x200B;_動作_&#x200B;欄中按一下&#x200B;**[!UICONTROL View]**。

   ![新報價](./assets/quote-grid-new.png){width="700" zoomable="yes"}

## 步驟2：修改報價

1. 在&#x200B;_[!UICONTROL Quote & Account Information]_&#x200B;底下，按一下_&#x200B;行事曆&#x200B;_（![行事曆圖示](../assets/icon-calendar.png)）圖示。

   ![報價和帳戶資訊](./assets/quote-details-account-information.png){width="575" zoomable="yes"}

1. 選擇報價的&#x200B;**[!UICONTROL Expiration Date]**。

1. 向下捲動至&#x200B;_[!UICONTROL Quote Totals]_&#x200B;區段，並視需要更新&#x200B;**[!UICONTROL Negotiated Price]**。

   ![更新議價價格](./assets/quote-change-update-negotiated-price.png){width="600" zoomable="yes"}

   如果採購員變更報價單中任何料號的數量，則會在報價單頂端顯示通知，指出料號清單已變更，且議價價格必須更新。

   ![報價變更通知](./assets/quote-change-notice.png){width="600" zoomable="yes"}

### 新增產品至報價單

1. 按一下&#x200B;**[!UICONTROL Add Products by SKU]**。

1. 輸入要新增的&#x200B;**[!UICONTROL SKU]**&#x200B;和&#x200B;**[!UICONTROL Qty]**。

   ![由SKU新增至報價單](./assets/quote-details-add-by-sku.png){width="600" zoomable="yes"}

### 套用行專案更新

如有需要，在&#x200B;_[!UICONTROL Items Quoted]_&#x200B;區段中套用行專案變更。

![套用行專案更新](./assets/quote-apply-line-item-operations.png){width="600" zoomable="yes"}

- 變更必須以建議價格購買的&#x200B;**[!UICONTROL Quantity]**。

- **[!UICONTROL Configure]**

  [!UICONTROL Configure]選項僅適用於可設定產品的條列專案

- 在&#x200B;**[!UICONTROL Action]**&#x200B;功能表中，選取動作以更新專案：
   - **折扣專案**，以百分比、固定金額或偏好訂價的形式套用折扣。
您可以選擇鎖定折扣金額，以防止進一步折扣。 如果未鎖定折扣，
明細專案折扣與任何報價層次折扣都會套用至產品價格。
   - **給購買者留下備註**，為購買者提供專案的額外資訊
   - **&#x200B;**

### 套用變更和更新

- 若要套用變更，請按一下&#x200B;**[!UICONTROL Add to Quote]**。

- 若要更新報價單，請按一下&#x200B;**[!UICONTROL Recalculate the Quote]**。

- 若要套用變更並將報價更新至共用型錄與價格規則，請按一下&#x200B;**[!UICONTROL Update Prices]**，然後按一下&#x200B;**[!UICONTROL Proceed]**&#x200B;以確認更新。

  ![個專案被引用](./assets/quote-detail-items-quoted.png){width="600" zoomable="yes"}

### 更新送貨資訊

1. 如果買方在報價單中包含&#x200B;_送貨地址_，請按一下&#x200B;**[!UICONTROL Get shipping methods and rates]**。

1. 從可用選項中選擇送貨方法。

1. 輸入&#x200B;**[!UICONTROL Proposed Shipping Price]**。

   _[!UICONTROL Quote Totals]_&#x200B;已更新，以反映建議的運費。

### 附加支援檔案

1. 在&#x200B;_新增您的註解_&#x200B;方塊下，按一下&#x200B;**[!UICONTROL Attach file]**。

   根據預設，[附加檔案](../configuration-reference/sales/quotes.md)在下列任何檔案格式中最多可有2 MB：DOC、DOCX、XLS、XLSX、PDF、TXT、JPG或JPEG、PNG。

1. 從目錄中選擇檔案。

## 步驟3：更新報價層級資訊，並傳送您的回覆

1. 在&#x200B;_[!UICONTROL Comments]_&#x200B;標籤的&#x200B;_[!UICONTROL Negotiation]_&#x200B;區段中，於&#x200B;**[!UICONTROL Add your comment]**&#x200B;區段中輸入您的回覆。

1. **[!UICONTROL Attach file]**

   The maximum file size allowed for attachments is 2 MB.

1. 若要將折扣套用至報價單，請執行下列步驟：

   - 在&#x200B;_[!UICONTROL Negotiated Price]_&#x200B;區段的&#x200B;_[!UICONTROL Quote Totals]_&#x200B;底下，選擇下列其中一個折扣型別：

      - `Percentage Discount`：百分比折扣會以特定百分比降低原始價格。
      - `Amount Discount`
      - `Proposed Price`

   - Enter the amount as a percentage or flat price.

     ![](./assets/quote-detail-negotiation-comments.png){width="600" zoomable="yes"}

   - You can apply discounts to each line item or the quote as a whole:

      - **&#x200B;**&#x200B;折扣可以是`percentage`、特定`amount`或`proposed price`。
      - **購物車層級折扣**：購物車層級折扣套用至整個購物車。 折扣可以是`percentage`或特定的`amount`，並套用至購物車總值。
      - **購物車與明細專案折扣的組合**：在某些情況下，折扣可同時套用至購物車與明細專案層次。 先套用明細專案折扣，然後套用剩餘總計的購物車層級折扣。

1. 傳送或儲存報價：

   - 如果報價單已準備好要傳回給買家，請按一下&#x200B;**[!UICONTROL Send]**。

   - 若要稍後繼續處理報價，請按一下&#x200B;**[!UICONTROL Save as Draft]**。

>[!NOTE]
>
> 在報價議價期間，可以鎖定折扣，以防止進一步的變更。 鎖定報價之後，若未先解除鎖定報價，則無法變更折扣型別和金額。 此鎖定機制可確保銷售代表與買方之間達成一致的條款得以保留。

## 步驟4：追蹤報價

當您傳送報價時，系統會通知購買者和管理公司帳戶的銷售代表。 電子郵件會包含購買者帳戶中報價的連結，以及報價的到期日。 在議價的任何時候，採購員都可以執行下列任一作業：

- 接受議價的報價並完成購買。
- 傳送包含還價報價的回覆，並繼續交涉。
- 結束交涉。

若要監視其在工作流程中的位置，請檢查您的電子郵件以及報價在格線中的狀態。 您可以視需要繼續交涉程式。

## 按鈕列

| 按鈕 | 說明 |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Back] | 返回&#x200B;_[!UICONTROL Quotes]_&#x200B;頁面而不儲存變更。 |
| [!UICONTROL Print] | 將報價傳送至印表機或儲存為PDF檔案。 |
| [!UICONTROL Create Copy] | 建立並開啟目前報價的復本，在原始名稱后面附加`(copy)`。 編輯[!UICONTROL Name]欄位以重新命名新報價。 將新的報價單儲存為草稿，或傳送給客戶來處理它。 |
| 建立範本 | 根據目前的報價建立報價範本。 報價樣版可讓買方與賣家就可套用至多個報價的合約與訂價條款達成一致意見，藉此簡化報價議價。. 在協定上，採購員可以從範本產生預先核准的連結式報價供後續訂單使用，而不需重新啟動詢價流程。 |
| [!UICONTROL Save as Draft] | Save any changes made to the quote, but do not send it back to the buyer. |
| [!UICONTROL Decline] | 拒絕議價要求，無論是在初始詢問時還是在進行中的議價期間。 當報價被拒絕時，賣家應新增評論來解釋決定。 拒絕報價時，所有議價價格都會重設為原始值。 當賣家等待買家的回覆時，此按鈕會停用。 |
| [!UICONTROL Send] | 傳送更新後的報價作為買家查詢的回覆。 如果賣家正在等待買家的回覆，此按鈕會停用。 |

{style="table-layout:auto"}

## 欄位說明

「管理員」中的報價資訊和功能分為下列區段。

### [!UICONTROL Quote & Account Information]

| 欄位 | 說明 |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Name] | 由[購買者](account-company-roles-permissions.md)指派給報價請求的名稱。 |
| [!UICONTROL Status] | 表示報價的目前狀態。 報價的狀態只能由買方或賣方執行動作來變更。 另請參閱管理員和[購買者帳戶](account-dashboard-my-quotes.md)的[狀態設定](quotes.md)。 |
| [!UICONTROL Created] | 買方首次提交報價請求的日期與時間。 |
| [!UICONTROL Created By] | 提交報價請求的公司買方名字和姓氏。 |
| [!UICONTROL Expiration Date] | 表示目前報價有效的最後一天。 在組態中，預設到期日設定為在採購員提交報價請求後的30天。 <br/><br/>賣家可以輸入不同的日期(YYYY MM DD )或從行事曆中選擇日期，覆寫預設到期日。 若將欄位留白，報價單將永不過期。 <br/><br/>對於未結報價，賣家會在報價排定到期前48小時收到[電子郵件通知](../systems/email-templates.md)。 買家會在到期日前24小時收到通知。 <br/><br/>__&#x200B;報價中的建議價格會回復到目錄中的原始值。 <br/><br/>如果報價設定為到期時，賣家將開啟供檢閱的報價，則到期日會根據組態中設定的範圍重設。 <br/><br/>到期日是&#x200B;_報價與帳戶_&#x200B;區段中唯一可在稽核過程中編輯的欄位。 |
| [!UICONTROL Company] | 買家代表的[公司](account-companies.md)法定名稱。 |
| [!UICONTROL Company Admin Email] | [公司管理員](account-company-admin.md)的電子郵件地址。 |
| [!UICONTROL Sales Rep] | 為賣家工作的[銷售代表](account-company-manage.md)，是指派給公司帳戶的主要聯絡人。 |
| [!UICONTROL Shared Catalog (or Customer Group)] | 公司被指派的[共用目錄](catalog-shared.md)或[客戶群組](account-company-customer-group.md)。 The quote might include custom prices from the shared catalog that is assigned to the company. |

{style="table-layout:auto"}

### [!UICONTROL Add to Quote by SKU]

| Field | 說明 |
|---------------------------|-----------------------------------------------------------|
| [!UICONTROL Enter SKU] | 要新增至報價的產品的SKU。 |
| [!UICONTROL Qty] | 要新增至報價的此SKU的專案數。 |
| [!UICONTROL Add to Quote] | 新增指定到報價單的產品數量。 |

{style="table-layout:auto"}

### [!UICONTROL Items Quoted]

| Field | 說明 |
|-----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Name & SKU] | The linked product name and stock-keeping unit (SKU). |
| [!UICONTROL Stock] | The number of products under this SKU that are currently available for sale. |
| [!UICONTROL Cost] | The amount the seller paid to purchase the product. |
| [!UICONTROL Catalog Price] | 採購員型錄中的產品價格，根據指派給採購員公司的客戶群組或共用型錄。 |
| [!UICONTROL Cart Price] | 購物車中專案的原始價格，減去從購物車套用的任何折扣。 如果有適用於買家客戶群組的折扣或購物車規則，購物車價格可能會與目錄價格不同。 |
| [!UICONTROL Discount] | 套用至料號的明細專案折扣。 值可以是百分比、固定金額或建議價格。 |
| [!UICONTROL Qty] | 此SKU中作為報價基礎的單位數。 只能輸入大於零的正數。 如果您想要將數量變更為零，請從報價中刪除明細專案。 |
| [!UICONTROL Subtotal] | 建議的價格乘以訂購的料號數量。 |
| [!UICONTROL Estimated Tax] | 根據組態估計此明細專案的稅捐金額。 根據「稅捐計算設定」的不同，預估稅捐可依據下列任一專案：單價/資料列總計/總計 |
| [!UICONTROL Subtotal (Incl./Excl. Tax)] | 視組態而定，此欄位可顯示含或不含預估稅捐的小計。 |
| [!UICONTROL Action] | 可套用至行專案的作業選取功能表：<ul><li>**[!UICONTROL Discount item]**</li><li>**[!UICONTROL Leave a note to Buyer]**</li><li>**[!UICONTROL Remove an item from the quote]**</li></ul>. |
| [!UICONTROL Configure] | 可讓您變更可設定產品的產品選項。 |
| [!UICONTROL Update Prices] | 使用共用型錄與價格規則的最新變更來更新報價單。 |
| [!UICONTROL Recalculate Quote] | 重新計算所有報價價格、購物車價格規則及稅捐，以反映報價的變更。 |

{style="table-layout:auto"}

### [!UICONTROL Shipping Information]

| 欄位 | 說明 |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Shipping Address] | 顯示採購員帳戶中指定的出貨地址。 如果買方在提交請求之前未指定地址，則出貨地址為空白。 |
| [!UICONTROL Shipping Method & Price] | 如果買家在報價單中包含&#x200B;_送貨地點_&#x200B;地址，就會顯示[取得送貨方式與費率]連結。 |

{style="table-layout:auto"}

### [!UICONTROL Negotiation]

| 欄位 | 說明 |
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Comments] | 「議價」區段的「附註」頁標是用來輸入有關報價的訊息給採購員。 <br/>**[!UICONTROL Add your comment]**— 註解是用來在交涉程式期間與採購員通訊。 使用註解來說明報價中提供的任何折扣，或報價請求遭拒絕的原因。<br/>**[!UICONTROL Attach file]** - [附加檔案](configure-quotes.md)的最大檔案大小和支援的檔案型別由組態決定。 依預設，附加檔案最大可達2 MB，以及下列任何檔案型別：DOC、DOCX、XLS、XLSX、PDF、TXT、JPG或JPEG、PNG。 |
| [!UICONTROL History Log] | 此索引標籤會顯示報價的完整歷史記錄，內含日期、報價狀態及註解。 |

{style="table-layout:auto"}

### [!UICONTROL Quote Totals]

| 欄位 | 說明 |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Total Cost] | 報價中包含之專案的銷售者總成本。 |
| [!UICONTROL Catalog Total Price  (Incl./Excl. Tax)] | 根據共用型錄或主要型錄中作為報價基礎的價格，報價單中不含稅捐的專案總價。 根據組態中的[顯示小計](../configuration-reference/sales/tax.md)設定，展開區段以顯示計算中使用的值。 選項： <br/>**[!UICONTROL Subtotal (Excl. Tax)]**— 不含預估稅捐的目錄總價。<br/>**[!UICONTROL Subtotal (Incl. Tax)]** — 不含預估稅捐的目錄總價。 <br/>**[!UICONTROL Estimated Tax]**— 預估要套用至目錄總價的稅捐金額。 |
| 議定價格 | 提供給買家的折扣可以以下列任何一項為依據： <br/>**[!UICONTROL Percentage Discount]**— 以百分比表示的折扣。<br/>**[!UICONTROL Amount Discount]** — 固定金額的折扣。 <br/>**[!UICONTROL Proposed Price]**— 賣家建議的價格。<p>如果報價中的所有專案都有鎖定的專案折扣，則[!UICONTROL Negotiated Price]區段會停用，因為無法套用其他折扣。</p><p>如果產品具有未鎖定的明細專案折扣，則明細專案折扣與報價層次折扣都會套用至產品價格。</p> |
| [!UICONTROL Quote Subtotal (Incl./Excl. Tax)] | 報價單中每個明細專案的總建議價格（無論是否含稅），視組態中的[稅捐計算](../configuration-reference/sales/tax.md)設定而定。 |
| [!UICONTROL Shipping & Handling] | 賣家在報價單的「出貨資訊」區段的「建議出貨價格」欄位中輸入的金額。 如果該欄位為空，則金額會根據所選的送貨方法而定。 |
| [!UICONTROL Estimated Tax] | 依照組態[顯示設定](../configuration-reference/sales/tax.md)中的指定，預估到期的稅捐金額。 |
| [!UICONTROL Quote Grand Total (Incl. Tax)] | 報價底端的最終總計，包括議定價格、預估稅捐，以及提議的出貨與處理。 |

{style="table-layout:auto"}
