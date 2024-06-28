---
title: 『[!DNL Adobe Commerce B2B] 版本注意事項
description: 檢閱發行說明，瞭解中變更的相關資訊 [!DNL Adobe Commerce B2B] 發行版本。
exl-id: 77d8c20d-6667-41e3-8889-252f36e56fd8
feature: B2B, Release Notes
source-git-commit: 35402eda770e59cc2862b204e6e54b55190ded13
workflow-type: tm+mt
source-wordcount: '6867'
ht-degree: 0%

---

# [!DNL Adobe Commerce B2B] 發行說明

以下是B2B擴充功能發行說明，擷取Adobe在發行週期中新增的新增功能和修正，包括：

![新增](../assets/new.svg) 新功能
![已修正的問題](../assets/fix.svg) 修正和改良
![已知問題](../assets/bug.svg) 已知問題

>[!NOTE]
>
>另請參閱 [產品可用性](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) 瞭解現有Adobe Commerce發行版本支援的B2B Commerce擴充功能版本相關資訊。

## B2B 1.5.0-beta

{{$include /help/_includes/b2b-beta-note.md}}

*2023年11月13日*

[!BADGE 支援]{type=Informative tooltip="支援"}

B2B v1.5.0 Beta版包含新功能、品質改善和錯誤修正。

![新增](../assets/new.svg) 報價功能的改進可協助買家和賣家更有效地管理報價和報價議價。

- **將報價儲存為草稿**<!--B2B-2566--> — 建立 [報價請求](quote-request.md) 在購物車中，購買者現在可以透過選取 **[!UICONTROL Save as Draft]** 於 [!UICONTROL Request a Quote] 表單。

  草擬報價沒有到期日。 採購員可以從以下網站複查並更新草擬報價單： [!UICONTROL My Quotes] 區段建立關聯。

- **重新命名報價**<!--B2B-2596--> — 購買者現在可以從以下位置變更報價名稱： [報價詳細資料](account-dashboard-my-quotes.md#quote-actions) 頁面，選取 **[!UICONTROL Rename]** 選項。 授權購買者在編輯報價時，可使用此選項。 名稱變更事件會記錄在「報價記錄檔」中。

- **重複報價**<!--B2B-2701--> — 買家和賣家現在可以複製現有的報價來建立新的報價。 透過選取「 」，從「報價詳細資料」檢視中建立副本  **[!UICONTROL Create Copy]** 於 [報價詳細資料檢視](quote-price-negotiation.md#button-bar) 在管理員或 [店面](account-dashboard-my-quotes.md#quote-actions).

- **明細專案折扣鎖定**<!--B2B-2597--> — 在報價議價期間，賣家可使用明細專案折扣鎖定，以便在套用折扣時獲得更大的彈性。 例如，賣家可對專案套用特殊明細專案折扣，並鎖定專案以防止進一步折扣。 鎖定料號時，套用報價層級折扣時無法更新料號價格。 另請參閱 [啟動採購員的報價單](sales-rep-initiates-quote.md).

![新增&#x200B;](../assets/new.svg)**公司管理**<!--B2B-2901--> — 商戶現在可以將公司指派給指定的母公司，以階層式組織形式檢視和管理Adobe Commerce公司。 將公司指派給母公司後，母公司管理員可以管理公司帳戶。 只有授權管理員使用者可以新增和管理公司指派。 如需詳細資訊，請參閱 [管理公司階層](assign-companies.md).

- 在公司頁面上，新增了 **[!UICONTROL Company Type]** 欄位可識別上下階公司。 商家可以依公司型別篩選公司檢視，並使用條列專案或大量動作管理公司。

- 商戶可以從新新增和管理公司指派 **[!UICONTROL Company Hierarchy]** 區段於 [!UICONTROL Company Account] 頁面。

- API開發人員可以使用新的公司關係REST API端點 `/V1/company/{parentId}/relations` 以建立、檢視及移除公司指派。 另請參閱 [管理公司物件](https://developer.adobe.com/commerce/webapi/rest/b2b/company-object/) 在 *Web API開發人員指南*.

![已修正的問題](../assets/fix.svg)<!--ACP2E-1984-->商戶按一下 **[!UICONTROL Print]** 現在會提示在Admin的報價詳細資料檢視中，將報價儲存為PDF的按鈕。 以前，商家會被重新導向到包含報價詳細資料的頁面。

![已修正的問題](../assets/fix.svg) <!--ACP2E-1742-->先前，傳送百分比為0的客戶報價單並變更數量時，管理員會擲回例外狀況，但會儲存數量。 在此修正套用後，針對 `0 percentage` 將會擲回適當的例外狀況並出現訊息。

![已修正的問題](../assets/fix.svg) <!--ACP2E-1742-->在報價議價期間，賣家現在可以指定 `0%` 「議價報價折扣」欄位中的折扣，並將報價傳回給採購員。 之前，如果賣家輸入0%的折扣，並將報價傳回給買方，管理員會傳回 `Exception occurred during quote sending` 錯誤訊息。

![已修正的問題](../assets/fix.svg) <!--ACP2E-2097-->ReCaptcha V3已設定為店面結帳，現在，ReCaptcha驗證可正確在B2B報價的結帳程式中運作。 之前，驗證失敗的原因為 `recaptcha validation failed, please try again` 錯誤訊息。

![已修正的問題](../assets/fix.svg) <!--ACP2E-1825-->公司遭到封鎖後，與公司相關聯的使用者就無法再下採購單。 以前，與公司相關聯的使用者可以在公司遭到封鎖時下訂單。

![已修正的問題](../assets/fix.svg)<!--ACP2E-1933-->公司管理員現在可以從店面新增公司使用者。 以前，當管理員使用者嘗試新增使用者時，Commerce會記錄錯誤： `CRITICAL: Error: Call to a member function __toArray() on null in app/code/Magento/LoginAsCustomerLogging/Observer/LogSaveCustomerObserver.php:123`.

## B2B v1.4.2-p1

[!BADGE 支援]{type=Informative tooltip="支援"}

![新增](../assets/new.svg) 新增與Adobe Commerce 2.4.7-p1+和2.4.6-p6+安全性修補程式版本的相容性。


## B2B v1.4.2

*2023年10月10日*

[!BADGE 支援]{type=Informative tooltip="支援"}

B2B v1.4.2版本包含品質改良與錯誤修正

![已修正的問題](../assets/fix.svg) <!--B2B-2897-->如果賣方建立的買方報價包含在與買方公司關聯的共用目錄中不可用的產品SKU，則系統會顯示錯誤訊息 `The SKU you entered is not available in the shared catalog. Please check the SKU and try again`.  除非賣家移除無法使用的產品，否則無法儲存報價。 之前，報價是以未提供的SKU儲存，且報價無法載入店面。

## B2B v1.4.1

*2023年8月7日*

[!BADGE 支援]{type=Informative tooltip="支援"}[Adobe Commerce 2.4.6-p2](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html). 與Adobe Commerce 2.4.7-beta1相容。

B2B v1.4.1版本包含品質改良和錯誤修正。

![已修正的問題](../assets/fix.svg) <!--ACP2E-1825-->公司遭到封鎖後，與公司相關聯的使用者就無法再下採購單。 以前，與公司相關聯的使用者可以在公司遭到封鎖時下訂單。

![已修正的問題](../assets/fix.svg) <!--ACP2E-1943-->現在，店面可正確顯示產品延期交貨狀態。 以前，可供出貨的產品被錯誤地識別為延期交貨。

![已修正的問題](../assets/fix.svg) <!--ACP2E-1862-->如果公司登錄檔單包含客戶檔案型別屬性，則在公司建立後，註冊過程中上傳的檔案現在會包含在公司管理員的帳戶資訊中。 之前，附件遺失。

![已修正的問題](../assets/fix.svg) <!--ACP2E-1793-->可設定產品的色票選取器現在會如預期般顯示在請購單清單專案設定頁面中。 之前，色票選取器會在請購單清單專案設定頁面中顯示為下拉式欄位。

![已修正的問題](../assets/fix.svg) <!--ACP2E-1968-->使用時 [公司GraphQL查詢](https://developer.adobe.com/commerce/webapi/graphql/schema/b2b/company/queries/company/#return-the-company-structure) 若要傳回公司詳細資料，結果現在可順利傳回，而不會發生錯誤。

## B2B v1.4.0

*2023年6月13日*

[!BADGE 支援]{type=Informative tooltip="支援"}[Adobe Commerce 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html). 與Adobe Commerce 2.4.7-beta1相容

此發行版本包含B2B議價報價和多個錯誤修正的新功能和增強功能。

![新增](../assets/new.svg) 新增與Adobe Commerce 2.4.7-beta1的相容性。

![新增](../assets/new.svg) **賣方起始的報價** — 賣家現在可以直接從Admin中的「報價單」與「客戶」網格為買家啟動報價單。 此功能可簡化報價流程，並降低客戶的複雜性。 如果客戶尚未啟動訂單，則賣家可以代表客戶快速建立報價單，並開始議價處理。 之前，報價只能由買方從店面建立，或由以客戶身分登入的賣方建立。

![新增](../assets/new.svg) **明細行料號折扣與議價**—<!--B2B-2440--> 在報價單中，B2B買方和賣方現在可以在明細專案層級進行交涉、套用折扣並交換附註，直到達成協定為止。 備註建立與更新會包含在明細專案與報價記錄中，以追蹤溝通。 以前，買家和賣家只能在報價層級交換備註和套用折扣。

![已修正的問題](../assets/fix.svg) 現在啟用「採購單」選項，且選取以PayPal付款選項建立的虛擬報價單時，Adobe Commerce會在付款期間顯示正確的詳細資料。 以前，在這些條件下，總計會顯示為零。

![已修正的問題](../assets/fix.svg) <!--ACP2E-1504--> 當您嘗試儲存信用額度超過999的公司時，不再發生驗證錯誤。 先前，對於大於999的公司信用限制，Adobe商務插入逗號分隔符號，這會導致驗證錯誤，阻止儲存更新。

![已修正的問題](../assets/fix.svg) <!--ACP2E-1474-->  現在，當您以可轉讓報價下訂單時，選取的送貨地址會維持不變。 之前，當您下訂單時，選取的送貨地址會變更為預設送貨地址。

![已修正的問題](../assets/fix.svg) <!--ACP2E-1429--> 在B2B功能的存放區組態設定中， **[!UICONTROL Enable Shared Catalog direct products price assigning]** 欄位現在會自動停用。 在店面，隱藏條件為 **[!UICONTROL Enable Company]** 設定或 **[!UICONTROL Enable Shared Catalog]** 設定已設為 **[!UICONTROL No]**.

![已修正的問題](../assets/fix.svg) <!--ACP2E-1683--> 從店面建立公司帳戶時，Commerce現在會在處理公司註冊之前驗證電子郵件地址。 如果電子郵件地址無效，則操作會失敗且不會處理任何帳戶更新。 以前，即使建立公司帳戶的請求由於電子郵件地址無效而失敗，也會建立客戶帳戶。

![已修正的問題](../assets/fix.svg) <!--ACP2E-1664--> 在「共用型錄」與訂價結構中包含雙引號的產品SKU不會再導致「管理員」發生錯誤。

![已修正的問題](../assets/fix.svg) <!--ACP2E-1498--> 更新Commerce應用程式的塗漆設定，以防止訪客使用者看到來自其他客戶群組的資料。

### 已知問題

如果您在上安裝或升級B2B 1.4.0 [Adobe Commerce 2.4.6版 — p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html)，會發生下列錯誤：

```terminal
Your requirements could not be resolved to an installable set of packages.

  Problem 1
    - Root composer.json requires magento/extension-b2b 1.4.0 -> satisfiable by magento/extension-b2b[1.4.0].
    - magento/extension-b2b 1.4.0 requires magento/security-package-b2b 1.0.4-beta1 -> found magento/security-package-b2b[1.0.4-beta1] but it does not match your minimum-stability.

Installation failed, reverting ./composer.json and ./composer.lock to their original content.
```

您可以為B2B安全性套件新增手動相依性，修正此問題，方法是為具有的B2B安全性套件新增手動相依性 [穩定性標籤](https://getcomposer.org/doc/04-schema.md#package-links). 如需指示，請參閱 [Adobe Commerce知識庫](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/installation-and-upgrade/b2b-1.4.0-installation-fails-on-adobe-commerce-2.4.6-p1-on-premises.html).

## B2B v1.3.5

*2023年3月14日*

[!BADGE 支援]{type=Informative tooltip="支援"}

![新增](../assets/new.svg) 已發行B2B 1.3.5-p2版，以支援與Adobe Commerce 2.4.6-p2的相容性。

![新增](../assets/new.svg) 已發行B2B 1.3.5-p1版，以支援與Adobe Commerce 2.4.6-p1的相容性。

>[!NOTE]
>
>將Commerce從2.4.6升級至 [最新版本](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html#2.4.6)，請務必更新至支援的B2B 1.3.5修補程式版本。 或者，請將B2B擴充功能從1.3.5版升級至1.4.0版或更新版本，以取得最新功能。

![新增](../assets/new.svg) 新增對Adobe Commerce 2.4.6的支援。

![已修正的問題](../assets/fix.svg) <!--- ACP2E-689--> 現在啟用「採購單」選項，且選取以PayPal付款選項建立的虛擬報價單時，Adobe Commerce會在付款期間顯示正確的詳細資料。 以前，在這些條件下，總計會顯示為零。

![已修正的問題](../assets/fix.svg) <!--- ACP2E-609--> 的客戶群組清單 **允許瀏覽類別** 設定不再包含與共用目錄相關的客戶群組。

![已修正的問題](../assets/fix.svg) <!--- ACP2E-1244--> 「稅捐/VAT編號」客戶屬性現在可如預期在「管理員」與「店面」上搭配公司管理員帳戶運作。 建立公司帳戶不再需要自訂稅捐/VAT屬性。 先前，當商家使用自訂Tax/VAT屬性建立公司帳戶時，Adobe Commerce會在店面和管理員上擲回驗證錯誤。

![已修正的問題](../assets/fix.svg) <!--- ACP2E-1236--> 停用特定範圍的共用目錄功能現在可以正常運作。 之前，當商家儲存共用目錄設定時，Adobe Commerce會設定無效的範圍。

![已修正的問題](../assets/fix.svg) <!--- ACP2E-1203--> 管理員使用者現在可以為公司使用者儲存客戶自訂屬性值。 以前無法儲存公司使用者的客戶自訂屬性。

![已修正的問題](../assets/fix.svg) <!--- ACP2E-1221--> 當已指派許多公司許可權時，透過GraphQL提供的公司許可權驗證即可解決效能問題。

![已修正的問題](../assets/fix.svg) <!--- ACP2E-1242--> 使用快速訂購新增數量超過可用存貨的產品時，Adobe Commerce不會再在購物車頁面上擲回錯誤。

![已修正的問題](../assets/fix.svg) <!--- ACP2E-1090--> 的效能 `SELECT` 公司許可權作業已改善。

![已修正的問題](../assets/fix.svg) <!--- ACP2E-2456--> 當查詢的類別沒有明確設定類別許可權時，類別查詢現在會根據商店組態設定傳回產品價格。

![已修正的問題](../assets/fix.svg) <!--- ACP2E-6829--> 此 **[!UICONTROL Place Order]** 使用核准的報價請求完成購買時，按鈕現在會如預期運作。 可轉讓報價的問題 `negotiableQuoteCheckoutSessionPlugin` 外掛程式已解決。

## B2B v1.3.4

*2022年8月9日*

[!BADGE 支援]{type=Informative tooltip="支援"}

![新增](../assets/new.svg) 新增對Adobe Commerce 2.4.5的支援。

![已修正的問題](../assets/fix.svg) <!--- ACP2E-453-->Adobe Commerce不再於每次API呼叫更新現有公司時傳送電子郵件通知。 現在，電子郵件只會在公司建立時傳送。

![已修正的問題](../assets/fix.svg) <!--- ACP2E-406-->Adobe Commerce現在會正確計算可轉讓報價的總計，當 **[!UICONTROL Enable Cross Border Trade]** 已啟用稅捐計算設定。

![已修正的問題](../assets/fix.svg) <!--- ACP2E-322-->現在，當庫存更新後，可設定的產品會移至產品清單中的最後一個位置， **[!UICONTROL Move out of stock to the bottom]** 設定已啟用。 已實作新的自訂資料庫查詢，以確保Elasticsearch索引排序順序現在遵循管理員啟用的排序順序。 先前，啟用此設定時，可設定的產品及其子產品不會移至清單底部。

![已修正的問題](../assets/fix.svg) <!--- ACP2E-308-->採購單電子郵件現在會遵循多網站部署中每個網站的電子郵件傳送設定。 檢查 **[!UICONTROL Disable Email Communications]** 此設定會新增至電子郵件佇列的自訂邏輯。 之前，Adobe Commerce沒有遵循次要網站的電子郵件傳送設定。

![已修正的問題](../assets/fix.svg) <!--- ACP2E-302-->為了清楚起見，快速訂購頁面的SKU欄位標題已變更。

![已修正的問題](../assets/fix.svg) <!--- ACP2E-543-->當購物者在「 」中輸入無效的SKU時，Adobe Commerce現在會顯示資訊更豐富的錯誤訊息。 **輸入SKU或產品名稱** 欄位。

![已修正的問題](../assets/fix.svg) <!--- ACP2E-1753-->此 **[!UICONTROL Account Created in]** 公司管理員的欄位現在會在您儲存公司後保留其預期值。

![已修正的問題](../assets/fix.svg) <!--- ACP2E-722 -->此 `customer` 查詢在擷取篩選依據的請購單清單時，不再傳回空白結果 `uid`.

![已修正的問題](../assets/fix.svg) <!--- ACP2E-210 -->在之前新增外掛程式 `collectQuoteTotals` 呼叫以確保商店積分僅套用一次。

![已修正的問題](../assets/fix.svg) <!--- ACP2E-665 -->現在，當管理員從管理員中刪除客戶的帳戶時，系統會將客戶重新導向至登入頁面。 之前，Adobe Commerce擲回錯誤。 外掛程式(`SessionPlugin`)程式碼區塊現在位於 `try…catch` 區塊。 之前，此程式碼不會包裝在一般例外狀況處理區塊中。

![已修正的問題](../assets/fix.svg) <!--- ACP2E-661 --> 在行動模式的「快速訂購」頁面上，按下 **輸入** 輸入有效的產品名稱或SKU後，購物者現在會如預期前往下一個欄位。

![已修正的問題](../assets/fix.svg) <!--- ACP2E-607 -->公司名稱現在會如預期顯示在結帳工作流程的帳單和送貨地址區段中。

![已修正的問題](../assets/fix.svg) <!--- ACP2E-375 -->現在，商店積分不可用於 **[!UICONTROL Zero Subtotal Checkout]** 付款方式已停用。 以前，在管理員下訂單時，「商店積分」核取方塊無法運作。 應用程式並未以商店信用下訂單，且顯示此錯誤： `The requested Payment Method is not available`.

## B2B v1.3.3

*2022年8月9日*

[!BADGE 支援]{type=Informative tooltip="支援"}

![新增](../assets/new.svg) 新增對Adobe Commerce 2.4.4的支援。

![已修正的問題](../assets/fix.svg) <!--- MC-41985--> 在擁有超過100,000個公司角色的部署中，從Adobe Commerce 2.3.x升級至Adobe Commerce 2.4.x所需的時間已大幅減少。

![已修正的問題](../assets/fix.svg) <!--- MC-42153--> POST `V1/order/:orderId/invoice` 現在，請求可支援在下列情況下建立部分商業發票： **[!UICONTROL Payment on Account]** 付款方式已啟用。 之前，Adobe Commerce擲回此錯誤： `An invoice for partial quantities cannot be issued for this order. To continue, change the specified quantity to the full quantity`. [GitHub-32428](https://github.com/magento/magento2/issues/32428)

![已修正的問題](../assets/fix.svg) <!--- MC-41975--> 當客戶的購物車包含其他產品時，PayPal Payflow Pro現在可與B2B可轉讓報價如期運作。 Adobe Commerce現在能成功處理訂單，並如預期傳送電子郵件給客戶。 之前，Adobe Commerce擲回嚴重錯誤，並傳送確認電子郵件給客戶，其中包含零值。

![已修正的問題](../assets/fix.svg) <!--- MC-41819--> 排除共用目錄中的部分產品後，目錄搜尋結果頁面上現在會正確顯示分頁。

![已修正的問題](../assets/fix.svg) <!--- MC-42886--> 在Admin中建立或儲存公司使用者時，客戶自訂屬性現在會如預期儲存。

![已修正的問題](../assets/fix.svg) <!--- MC-42927--> 此 **[!UICONTROL Submit]** 按一下後，「建立新公司」表單上的按鈕現在已停用，以防止提交多個表單。 以前，您可以多次提交此表單，只要反複按一下此按鈕就會產生錯誤。

![已修正的問題](../assets/fix.svg) <!--- MC-42787--> 當購物者登入已停用重新訂購的商店時，Adobe Commerce不再顯示店面上的重新訂購連結。

![已修正的問題](../assets/fix.svg) <!--- MC-43115--> 共用目錄啟用時，SKU的快速訂購搜尋現在會區分大小寫。

![已修正的問題](../assets/fix.svg) <!--- MC-42203--> 您現在可以在建立公司時更新客戶屬性的檔案。 先前，當您嘗試建立具有下列型別的附件的公司時 `File`，Adobe Commerce並未建立公司，並將此錯誤記錄於例外狀況記錄中： `Something went wrong while saving file`.

![已修正的問題](../assets/fix.svg) <!--- MC-42242--> 您現在可以使用客戶帳戶來建立公司，該客戶帳戶具有包含(`File`)或(`Image`)型別。 以前，如果帳戶具有其中一個可自訂的選項，公司編輯頁面載入器無法解析，這會阻止編輯公司詳細資訊。

![已修正的問題](../assets/fix.svg) <!--- MC-42268--> 此 `products` 查詢現在會傳回精確值 `total_count` 欄位（當啟用共用目錄時）。

![已修正的問題](../assets/fix.svg) <!--- MC-42203-->  您現在可以在建立公司時更新客戶屬性的檔案。 先前，當您嘗試建立具有下列型別的附件的公司時 `File`，Adobe Commerce並未建立公司，並將此錯誤記錄於例外狀況記錄中： `Something went wrong while saving file`.

![已修正的問題](../assets/fix.svg) <!--- MC-43178--> 此 _公司設定_ 和 _建立公司_ 停用線上送貨方法後，頁面現在會如預期般運作。 已新增驗證，以防止嘗試處理停用的送貨模組。 Adobe Commerce之前會顯示此錯誤： `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`.

![已修正的問題](../assets/fix.svg) <!--- MC-42214--> 此 _類別_ 部分索引期間產生許可權時，頁面現在會顯示一致的產品資料。 新的目錄許可權部分索引器已新增至此程式。 先前，索引器執行時顯示的資料不正確。

![已修正的問題](../assets/fix.svg) <!--- MC-42567--> 此 `categoryList` 現在，當使用目錄許可權並將產品指派給共用目錄時，query會傳回正確數量的產品。

![已修正的問題](../assets/fix.svg) <!--- MC-42528--> 此 `categoryList` 查詢現在會遵循類別許可權，並只傳回允許的類別。 之前，它會傳回所有指派和未指派的類別。

![已修正的問題](../assets/fix.svg) <!--- MC-42399--> 此 `rest/V1/company/{id}` 要求現在傳回 `is_purchase_order_enabled` 屬性值。

![已修正的問題](../assets/fix.svg) <!--- ACP2E-128--> 自訂客戶屬性現在會如預期顯示在中 _公司管理員_ 標籤。

![已修正的問題](../assets/fix.svg) <!--- ACP2E-130--> 「我的帳戶」頁面上的「我的願望清單」區塊現在會依預期顯示給公司管理員和公司使用者。

![已修正的問題](../assets/fix.svg) <!--- ACP2E-133--> 快速訂購錯誤不再顯示在購物車中。 之前，在目錄中找不到SKU時，Adobe Commerce會在購物車中顯示此錯誤：  `The SKU was not found in the catalog`.

![已修正的問題](../assets/fix.svg) <!--- ACP2E-194--> 已最佳化共用目錄儲存作業，以加快執行速度。 以前，儲存與許多客戶群組的共用目錄可能需要幾分鐘的時間。

![已修正的問題](../assets/fix.svg) <!--- MC-42240--> Adobe Commerce現在會刪除以下的所有子類別許可權： `sharedcatalog_category_permissions` 刪除父類別時顯示的表格。 之前，系統只會移除父類別資料。

## B2B v1.3.2

*2022年8月29日*

[!BADGE 支援]{type=Informative tooltip="支援"}

![新增](../assets/new.svg) 新增對Adobe Commerce 2.4.3的支援。

![已修正的問題](../assets/fix.svg) <!--- MC-39862--> Adobe Commerce現在已成功傳送有關過期可轉讓報價的更新電子郵件。 以往，當可轉讓報價過期時，Adobe Commerce不會傳送更新電子郵件。

![已修正的問題](../assets/fix.svg) <!--- MC-40682--> Adobe Commerce現在成功傳送有關即將到期的更新電子郵件，並在以下情況下過期的可協商報價： `cron` 工作遺失。

### 公司

![已修正的問題](../assets/fix.svg) <!--- MC-41542--> 「建立新公司帳戶」頁面的「國家/地區」下拉式欄位不再列出空白的選項值。 先前，前兩個選項值和國家/地區代碼 `AN` 空白。

![已修正的問題](../assets/fix.svg) <!--- MC-41260--> 按一下 **[!UICONTROL Return]** 公司使用者建立之訂單的按鈕，現在會如預期將管理使用者重新導向至「建立退貨」頁面。 之前，管理員會重新導向至「訂單歷史記錄」頁面。

![已修正的問題](../assets/fix.svg) <!--- MC-40798--> Adobe Commerce在執行時不再因記憶體不足錯誤而失敗。 `app/code/Magento/PurchaseOrder/Setup/Patch/Data/InitPermissions.php::apply` 期間的方法 `bin/magento setup:upgrade`. 以往，Adobe Commerce在初始化許可權時並未使用批次大小進行集合，而是載入所有公司角色的集合。

![已修正的問題](../assets/fix.svg) <!--- MC-40551--> 公司使用者現在可以編輯和更新客戶自訂屬性值。 以前，這些屬性無法與建立和編輯使用者表單正確繫結。 公司使用者可以輸入不同的屬性值，但Adobe Commerce未正確儲存這些值。

![已修正的問題](../assets/fix.svg) <!--- MC-32653--> 公司角色許可權的資源樹狀結構現在可以如預期般轉譯。 以前，即使存在有效的翻譯檔案，許可權樹狀結構也不會翻譯。

![已修正的問題](../assets/fix.svg) <!--- MC-40358--> Adobe Commerce現在會如預期為B2B使用者儲存自訂客戶屬性值。 之前，建立包含自訂客戶屬性的公司帳戶會觸發範本錯誤，且Adobe Commerce未成功載入表單。 將引數新增至的配置 `company_create_account` 已解決此問題。

![已修正的問題](../assets/fix.svg) <!--- MC-41721--> 公司使用者篩選器（例如「顯示所有使用者」、「顯示作用中使用者」和「顯示非作用中使用者」）現在可如預期運作。 先前，篩選公司使用者頁面上的動作會造成JavaScript錯誤。

### 公司評價

![已修正的問題](../assets/fix.svg) <!--- MC-41551--> 擁有僅包含網站層級許可權之受限制帳戶的管理員現在可以建立使用與網站不同貨幣的公司。

![已修正的問題](../assets/fix.svg) <!--- MC-41523--> Adobe Commerce現在會從正確的位置傳送公司電子郵件 `from` 電子郵件地址和範圍。 以往，在傳送公司信用指派或更新電子郵件時，Adobe Commerce不會考量網站範圍。

### 快速訂購

![已修正的問題](../assets/fix.svg) <!--- MC-42104--> 現在，從CSV檔案使用「快速訂購」來建立訂單，對不存在的SKU可如預期般運作。

![已修正的問題](../assets/fix.svg) <!--- MC-40268--> 使用「快速訂購」功能來搜尋多個SKU現在可如預期運作。 以前，結果包括重複的專案。

![已修正的問題](../assets/fix.svg) <!--- MC-40261--> 現在，當您在「快速訂購」期間使用SKU來選取多個產品時，「新增的產品」清單顯示會將輸入的小寫與大寫的SKU視為相同。

![已修正的問題](../assets/fix.svg) <!--- MC-40225--> 現在，使用「快速訂購」會以購物者指定的數量新增產品。 之前，即使購物者指定的數量超過一個，Adobe Commerce也只新增一個產品。

![已修正的問題](../assets/fix.svg) <!--- MC-41283--> 快速訂購自動完成功能現在可與部分SKU搭配使用。

![已修正的問題](../assets/fix.svg) <!--- MC-41299--> Adobe Commerce現在會顯示已設定為 **無法單獨顯示** 在快速訂購頁面的自動建議清單和搜尋結果上。

![已修正的問題](../assets/fix.svg) <!--- MC-42402--> 購物者現在可以使用「快速訂購」表單，依包含大寫字元的SKU來新增多個產品。 之前，僅新增第一個產品。

### 可轉讓報價

![已修正的問題](../assets/fix.svg) <!--- MC-41232--> 在URL欄位貼上可轉讓報價的連結並成功登入後，購物者現在會重新導向至可轉讓報價頁面。 之前，購物者會被重新導向至「我的帳戶」頁面。

![已修正的問題](../assets/fix.svg) <!--- MC-39317--> 對於在結帳期間建立的客戶帳戶，訂單中包含具有日期可自訂選項的產品，重新排序現在可如預期運作。 之前，Adobe Commerce不會處理重新排序，且會顯示此錯誤： `The product has required options. Enter the options and try again`.

![已修正的問題](../assets/fix.svg) <!--- MC-39063--> 當採購單模組停用時，可轉讓報價單的送貨地址在結帳期間不再可編輯。 此行為是先前進行下列修正所導致： `isQuoteAddressLocked` 已從可轉讓報价籤出轉譯器中移除。

![已修正的問題](../assets/fix.svg) <!--- MC-38967--> 商戶現在可以從管理員將產品新增至可轉讓的報價單。

### 採購單

![已修正的問題](../assets/fix.svg) <!--- MC-39983--> 現在，當您使用PayPal Express結帳功能下達採購單時，Adobe Commerce會如預期顯示資訊性錯誤訊息，當 **[!UICONTROL Name Prefix]** 屬性已設定為 `required`. 之前，Adobe Commerce不會下訂單或顯示錯誤訊息。

![已修正的問題](../assets/fix.svg) <!--- MC-39620--> 啟用Google Tag Manager時，採購訂單模組中帳單地址的UI元件現在會正確使用報價地址。 之前，付款頁面上發生JavaScript錯誤。

### 請購單清單

![已修正的問題](../assets/fix.svg) <!--- MC-40426--> 商家現在可以使用此POST `rest/all/V1/requisition_lists` 端點，為客戶建立請購單清單。 之前，當您嘗試建立請購單清單時，Adobe Commerce擲回這個400錯誤： `Could not save Requisition List`.

![已修正的問題](../assets/fix.svg) <!--- MC-41123--> 此 **[!UICONTROL Add to Requisition List]** 當購物車也包含無庫存產品時，購物車的庫存產品現在會顯示按鈕。 先前，如果購物車包含兩個產品，其中一個無庫存，則 _[!UICONTROL Add to Requisition List]_這兩個產品都沒有顯示按鈕。

![已修正的問題](../assets/fix.svg) <!--- MC-40877--> 您現在可以使用REST API將產品新增至請購單清單。

![已修正的問題](../assets/fix.svg) <!--- MC-40155--> 請購單清單 **[!UICONTROL Latest Activity Date]** 值現在遵循地區設定格式。

![已修正的問題](../assets/fix.svg) <!--- MC-39580--> 當您從請購單清單編輯套件組合產品時，Adobe Commerce不再擲回嚴重錯誤。

![已修正的問題](../assets/fix.svg) <!--- MC-40454--> 新增具可自訂選項的產品時，Adobe Commerce現在會顯示正確的產品價格 `(File)` 從請購單清單中選取希望清單。 上傳檔案的連結也會如預期般顯示。 之前，Adobe Commerce顯示錯誤的產品價格，且不顯示檔案連結。

![已修正的問題](../assets/fix.svg) <!--- MC-36383--> 具有可自訂選項的產品 `(File)` 現在可從請購單清單新增至購物車。

### 共用目錄

![已修正的問題](../assets/fix.svg) <!--- MC-40497--> 角色僅限於特定網站的管理員現在可以建立、檢視及編輯共用目錄。 之前，當角色有限的管理員嘗試建立共用目錄時，Adobe Commerce會擲回嚴重錯誤。

![已修正的問題](../assets/fix.svg) <!--- MC-41337--> 階層式導覽結果現在包含具有篩選屬性的精確產品計數，購物者現在可以套用多個篩選器。 之前，僅可套用一個篩選器，而Adobe Commerce在分層導覽中顯示不準確的產品計數。

![已修正的問題](../assets/fix.svg) <!--- MC-40779--> Adobe Commerce現在會在搜尋結果中的階層式導覽篩選器中正確顯示產品計數。 以前，「搜尋結果」頁面的外掛程式不會使用Elasticsearch，而是向資料庫發出新查詢。

![已修正的問題](../assets/fix.svg) <!--- MC-39978--> 當商家從預設共用目錄中刪除所有產品時，Adobe Commerce不再刪除層級價格。

![已修正的問題](../assets/fix.svg) <!--- MC-39802--> 篩選器現在會依目前類別篩選，且在啟用共用目錄時會在所有頁面上正確顯示。 之前，僅針對目前頁面錯誤地計算篩選器，且沒有按目前類別篩選。

![已修正的問題](../assets/fix.svg) <!--- MC-39522--> GraphQL `products` 若啟用共用目錄時，查詢不再傳回未指派至共用目錄之產品的價格範圍和類別。 以前，查詢會傳回產品的彙總，即使產品本身並未在 `items` 陣列。

## B2B v1.3.1

*2021年2月9日*

[!BADGE 支援]{type=Informative tooltip="支援"}

![新增](../assets/new.svg) 新增對Adobe Commerce 2.4.2的支援。

![新增](../assets/new.svg) 採購單現在支援線上付款方法。

![已修正的問題](../assets/fix.svg) 當此產品用於先前訂單時，直接從請購單清單將可設定產品新增到購物車中不再傳回系統錯誤。

![已修正的問題](../assets/fix.svg) Adobe Commerce現在會在部署分割資料庫組態時，正確顯示採購單的「需要我的核准」標籤。

![已修正的問題](../assets/fix.svg) 現在，當您檢視採購單時，Adobe Commerce會顯示有關套裝產品和禮品卡的詳細資料。

![已修正的問題](../assets/fix.svg) 在瀏覽商店時登入購物者的帳戶後，購物者現在會如預期重新導向 **[!UICONTROL Website Restriction]** 已啟用且 **[!UICONTROL Restriction Mode]** 設為 `Private Sales: Login Only`. 之前，購物者會被重新導向至商店首頁。 <!--- MC-38934-->

![已修正的問題](../assets/fix.svg) 在包含許多客戶(大於13000)的B2B公司階層部署中，訂單歷史記錄現在會如預期般載入公司管理員的帳戶控制面板頁面。 先前，訂單歷史記錄載入緩慢或完全沒有載入，且Adobe Commerce顯示503錯誤。 <!--- MC-38830-->

![已修正的問題](../assets/fix.svg) 當您從「類別」頁面將具有可自訂選項之未設定產品新增至「請購單清單」時，Adobe Commerce不再顯示多重相同的警告訊息。 <!--- MC-38342-->

![已修正的問題](../assets/fix.svg) 啟用B2B共用目錄時，新的和重複的產品現在會如預期般顯示在類別頁面上。 <!--- MC-38307-->

![已修正的問題](../assets/fix.svg) Adobe Commerce現在會維護正確的專案 `store_id` 在更新公司的客戶群組時，會與公司管理員建立關聯。 先前， `store_id` 已變更為預設存放區（當群組更新時）。 <!--- MC-38196-->

![已修正的問題](../assets/fix.svg) Adobe Commerce現在會將群組產品儲存至請購單清單，作為簡單產品清單，其方式與將群組產品新增至購物車相同。 先前，由於Adobe Commerce儲存群組產品的方式，請購單清單中群組產品的連結一律會重新導向至簡單產品，而非群組產品。 <!--- MC-38049-->

![已修正的問題](../assets/fix.svg) 您現在可以依據以下專案篩選訂單： **[!UICONTROL Company Name]** 以CSV格式匯出訂單資訊時的欄位。 Adobe Commerce先前在下列位置記錄錯誤： `var/export/{file-id}`. <!--- MC-37785-->

![已修正的問題](../assets/fix.svg) 當您在店面選取「建立新請購單清單」頁標時，Adobe Commerce現在會如預期顯示「建立請購單清單」快顯視窗。 <!--- MC-37915-->

![已修正的問題](../assets/fix.svg) 請購單清單現在包含已新增至清單的所有群組產品和數量。 先前，當商家從產品詳細資料頁面新增產品至請購單清單後，Adobe Commerce會顯示此錯誤： `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-37621-->

![已修正的問題](../assets/fix.svg) 現在，當您在多網站部署中建立公司時，正確的商店檢視會與相關網站相關聯。 之前，您無法建立公司，Adobe Commerce會顯示此錯誤： `The store view is not in the associated website`. <!--- MC-37488-->

![已修正的問題](../assets/fix.svg) SKU使用「快速訂購」來訂購產品不會再導致CSV檔案中的產品數量重複。 <!--- MC-37427-->

![已修正的問題](../assets/fix.svg) 此 **[!UICONTROL Add to Cart]** 按鈕不再封鎖 _[!UICONTROL Enter Multiple SKUs]_「快速訂購」頁面的區段包含一個空白值。 Adobe Commerce現在改為顯示訊息，提示您輸入有效的SKU。 <!--- MC-37387-->

![已修正的問題](../assets/fix.svg) 現在，當您從請購單清單提交產品稽核時，Adobe Commerce會在產品頁面上顯示此訊息： `You submitted your review for moderation`. 檢閱也會顯示在「擱置的檢閱」頁面上(Admin **[!UICONTROL Marketing]** > **[!UICONTROL Pending Reviews]**)。 之前，雖然Adobe Commerce已將評論新增至待處理評論的清單，但在產品頁面上擲回404錯誤。 <!--- MC-37119-->

![已修正的問題](../assets/fix.svg) 的效能 `sharedCatalogUpdateCategoryPermissions` 已改善消費者。 建立共用目錄後，目錄許可權索引器現在只會使用共用目錄中的客戶群組ID，而非所有客戶群組。 <!--- MC-36770-->

![已修正的問題](../assets/fix.svg) 與購物者的非預設地址相關聯的自訂客戶地址屬性欄位，現在會如預期般儲存在店面結帳工作流程中。 <!--- MC-36630-->

![已修正的問題](../assets/fix.svg) 現在，購物者可透過管理員REST API (`rest/V1/carts/{<CART_ID>/items`)依預期執行。 Adobe Commerce現在會先檢查產品是否已指派給公用目錄，然後再於進行共用目錄許可權驗證 `\Magento\SharedCatalog\Plugin\Quote\Api\ValidateAddProductToCartPlugin::beforeSave`. 之前，Adobe Commerce不會將產品新增至購物車的訊息，並擲回此錯誤： `No such shared catalog entity`. <!--- MC-36535-->

![已修正的問題](../assets/fix.svg) Adobe Commerce現在會從Adobe Commerce商店的地址傳送新的公司使用者註冊電子郵件。 之前，這封電子郵件是透過公司管理員的位址傳送的。 <!--- MC-36480-->

![已修正的問題](../assets/fix.svg) Adobe Commerce現在會先檢查自訂屬性，找出保留的公司屬性名稱的重複專案，再允許商家儲存新屬性。 <!--- MC-36282-->

![已修正的問題](../assets/fix.svg) 此 `credit_history` 查詢現在會傳回指定公司原始配置金額與購買金額的信用記錄。 之前，此查詢傳回錯誤。

![已修正的問題](../assets/fix.svg) 此 **[!UICONTROL Company]** 和  **[!UICONTROL Job Title]** [編輯帳戶資訊]頁面上的欄位不再可編輯。

### 已知問題

- B2B買家可以使用線上付款方式，略過一般的採購單流程。 如果購買者能將結帳總數減至0 （例如，透過促銷代碼或禮品卡），然後移除代碼或禮品卡，就可能發生這種情況。 即使在這些條件下，Adobe Commerce仍會根據所指派目錄中的專案價格，下正確金額的訂單。 **_因應措施_**：當啟用線上付款方式以進行採購單核準時，請停用禮品卡和優惠券代碼。 <!--- B2B-1603-->

- 當買家嘗試使用PayPal Express結帳功能從採購單下訂單時，系統會重新導向至購物車 **[!UICONTROL In-Context Mode]** 已停用。 <!--- B2B-1604-->

- 當採購員建立採購單，然後導覽至結帳頁面時，Adobe Commerce有時會顯示404錯誤。 當採購員先前使用線上付款方式建立不同的採購單，而未完成先前的採購就瀏覽至結帳頁面時，就會發生此錯誤。 採購員仍然可以下採購單。 **_解決方法_**：無。 <!--- B2B-1605-->

- 在採購單結帳期間，即使買方在最後結帳期間變更付款方式，特定付款方式的折扣仍會持續存在。 因此，客戶可獲得無權享有的折扣。 發生此問題是因為儘管付款方式有所變更，原始付款方式的購物車規則仍會套用。 **_解決方法_**：無。 請參閱 [Adobe Commerce 2.4.2 B2B已知問題：付款方式變更後，線上採購單的折扣仍會保留](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/magento-2.4.2-b2b-discount-remains-pay-method-change.html) _知識庫_ 文章。 <!-- B2B-1012 -->

- 此 `deleteRequisitionListOutput` 查詢會傳回已刪除的請購單清單（而非剩餘的請購單清單）的相關明細。 <!--- MC-39894-->

## B2B v1.3.0

*2020年10月15日*

[!BADGE 支援]{type=Informative tooltip="支援"}

此版本包括訂單核准、送貨方法、購物車及管理員動作記錄等的改善。

![新增](../assets/new.svg) 新增對Adobe Commerce 2.4.1的支援。

![新增](../assets/new.svg) 已增強B2B訂單核准，以改善可用性並允許對採購單執行大量動作。

![新增](../assets/new.svg) B2B商家現在可以控制提供給各公司的送貨方法。<!--- BUNDLE-160 161 162 -->

![新增](../assets/new.svg) 商戶現在可以允許使用者透過單一動作清除其購物車的內容，並可以在每個網站上獨立設定此功能 <!--- BUNDLE-108 -->

![新增](../assets/new.svg) B2B購買者現在可以直接將個別專案或其購物車的全部內容新增到請購單清單中。 <!--- BUNDLE-145 144-->

![新增](../assets/new.svg) B2B商家可使用「依帳戶付款」作為付款方式，代表客戶從管理員建立訂單。 <!--- BUNDLE-166 178-->

![新增](../assets/new.svg) 商戶現在可以從客戶的明細頁面，直接檢視與使用者相關的所有報價單。 <!--- BUNDLE-139 -->

![新增](../assets/new.svg) 商戶現在可以依公司篩選「立即線上客戶」方格。 <!--- BUNDLE-137 -->

![新增](../assets/new.svg) 管理員現在可以在Admin by Sales Rep中篩選客戶。 <!--- BUNDLE-110 -->

![新增](../assets/new.svg) 為了減少詐騙或垃圾郵件帳戶的建立，商家現在可以在店面的新公司申請表中啟用Google reCAPTCHA 。 <!--- BUNDLE-154 -->

![新增](../assets/new.svg) 在公司模組中採取的管理員動作現在記錄在「管理員動作記錄」中。 動作會從所有相關公司模組記錄： `Company`， `NegotiableQuote`， `CompanyCredit`， `SharedCatalog`.  <!--- BUNDLE-180 181 182 183 -->

![已修正的問題](../assets/fix.svg) Adobe Commerce不再顯示 **[!UICONTROL Delete customer]** 上的按鈕 **客戶** 此頁面代表登入管理員無權刪除已安裝B2B之部署中的客戶。 <!--- MC-35655-->

![已修正的問題](../assets/fix.svg) 當您在「客戶」方格上編輯客戶時，不再自動為指派至公司的客戶變更客戶群組。 <!--- MC-35254-->

![已修正的問題](../assets/fix.svg) 當商家建立共用目錄時，許可權現在會自動設定為 `Allow` 針對 **[!UICONTROL Display Product Prices]** 和 **[!UICONTROL Add to Cart]** 當客戶群組在目錄許可權設定中被指派此存取權時，類別中的功能。 之前，這些設定會自動設為 `Deny` 即使目錄許可權設定為 `Allow`.<!--- MC-34792-->

![已修正的問題](../assets/fix.svg) 從產品編輯頁面編輯產品時，不再覆寫共用目錄類別許可權。<!--- MC-34777-->

![已修正的問題](../assets/fix.svg) Adobe Commerce現在會傳送電子郵件通知，確認當商家啟用 **[!UICONTROL Allow To Exceed Credit Limit]** 設定。 以往，Adobe Commerce傳送的通知電子郵件指出客戶沒有許可權超過限制。 <!--- MC-34584-->

![已修正的問題](../assets/fix.svg) 針對套裝產品的子項，現在會正確呈現請購單清單上產品價格周圍的HTML容器。 <!--- MC-36331-->

![已修正的問題](../assets/fix.svg) 商戶現在可以指定在多語言部署中建立公司時，傳送公司使用者電子郵件所用的語言。 以前，商家可以使用的下拉式功能表選取適當的商店檢視和語言，但系統不會顯示。  <!--- MC-35777-->

![已修正的問題](../assets/fix.svg) 自訂客戶地址屬性欄位現在會如預期顯示在店面結帳工作流程中。 <!--- MC-35607-->

![已修正的問題](../assets/fix.svg) B2B功能設定索引標籤現在會正確開啟。 <!--- MC-35458-->來賓現在可以使用QuickOrder將產品新增至購物車，然後成功移除專案。 先前，當購物者使用QuickOrder將多個產品新增至購物車，然後移除產品時，產品未移除。 <!--- MC-35327-->

![已修正的問題](../assets/fix.svg) 現在可以使用REST APIPUT更新公司 `/V1/company/:companyId` 要求但不指定 `region_id` 當狀態設定為 **非必要**. 先前，即使 `region_id` 非必要，若未指定，Adobe Commerce會擲回錯誤。 <!--- MC-35304-->

![已修正的問題](../assets/fix.svg) 當您使用REST API建立或更新B2B公司時(`http://magento.local/rest/V1/company/2`，其中 `2` 代表公司ID)，回應現在包含 `applicable_payment_method` 或 `available_payment_methods` 如預期。 <!--- MC-35248-->

![已修正的問題](../assets/fix.svg) 商家使用「 」時，Adobe Commerce不再顯示404頁面 **輸入** 按鈕，而非按一下 **[!UICONTROL Save]** 按鈕。<!--- MC-35094-->

![已修正的問題](../assets/fix.svg) 當新產品指派至公用共用目錄時，類別許可權不再變更。 之前，類別許可權是重複的。 <!--- MC-34386-->

![已修正的問題](../assets/fix.svg) REST API端點PUT `rest/default/V1/company/{id}`用於更新公司電子郵件的，不再區分大小寫。 <!--- MC-34308-->

![已修正的問題](../assets/fix.svg) 停用獎勵模組不再影響客戶帳戶上的B2B功能。 先前，當獎勵模組停用時，不會顯示下列B2B相關標籤：公司設定檔、公司使用者以及角色和許可權。<!--- MC-34191-->

![已修正的問題](../assets/fix.svg) 現在，當對公司帳戶進行變更時，Adobe Commerce會在電子郵件通知中使用正確的寄件者名稱。 之前，Adobe Commerce使用所有電子郵件預設範圍中定義的一般聯絡人寄件者名稱。 <!--- MC-33917-->

![已修正的問題](../assets/fix.svg) 您現在可以針對同時包含實體與虛擬產品的訂單，成功實作多重出貨。 <!--- MC-33818-->

![已修正的問題](../assets/fix.svg) 商戶現在可以從以下網址建立公司使用者： _[!UICONTROL Company Users]_「我的帳戶」和「公司結構」頁面中的區段，當&#x200B;**[!UICONTROL Access Restriction]**已啟用且&#x200B;**[!UICONTROL Restriction Mode]**設為 `Sales: Login Only`. 之前，當商家嘗試建立使用者時，Adobe Commerce擲回此錯誤： `Can not register new customer due to restrictions are enabled`. <!--- MC-33608-->

![已修正的問題](../assets/fix.svg) 客戶儲存帳戶資訊時，Adobe Commerce不再將客戶的客戶群組重設為預設值。 <!--- MC-33554-->

![已修正的問題](../assets/fix.svg) 管理員將擁有有效購物車的客戶指派給客戶群組時，Adobe Commerce不再擲回嚴重錯誤。 <!--- MC-33313-->

![已修正的問題](../assets/fix.svg) Adobe Commerce現在提供 `addToCart` 「快速訂購」與「請購單」的DataLayer事件會列出頁面。  <!--- MC-33295-->

![已修正的問題](../assets/fix.svg) 傳送給指派給公司的銷售代表的通知電子郵件現在包含指派的公司標誌。 以前，通知電子郵件包含預設的LUMA標誌，而不是上傳的企業標誌。 <!--- MC-33232-->

![已修正的問題](../assets/fix.svg) 請購單清單現在包含已新增至清單的所有群組產品和數量。 先前，當商家從產品詳細資料頁面新增產品至請購單清單後，Adobe Commerce會顯示此錯誤： `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-32877-->

![已修正的問題](../assets/fix.svg) 此 `products` 查詢現在會傳回精確值 `total_count` 欄位（當啟用共用目錄時）。 <!--- MC-42268-->

![已修正的問題](../assets/fix.svg) 停用線上送貨方法後，「公司設定」和「建立公司」頁面現在會如預期般運作。 已新增驗證，以防止嘗試處理停用的送貨模組。 Adobe Commerce之前會顯示此錯誤： `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`. <!--- MC-43178-->

![已修正的問題](../assets/fix.svg) 整合測試記憶體耗用量已降低，可改善測試效能，並減少完成測試所需的時間。 <!--- AC-266-->

## B2B v1.2.0

*2020年7月28日*

[!BADGE 支援]{type=Informative tooltip="支援"}

![新增](../assets/new.svg) 新增對Adobe Commerce 2.4.0的支援。

![新增](../assets/new.svg) Storefront Order Search，在此感謝來自Marek Mularczyk的貢獻 [Divante](https://www.divante.com/) 和社群成員。

![新增](../assets/new.svg) 採購單已增強並重寫。 現在，預設情況下會包含在Adobe Commerce中。

![新增](../assets/new.svg) 已匯入採購單核准規則。 這些規則可讓使用者藉由建立訂單的採購規則來控制「採購單」工作流程。

![新增](../assets/new.svg) Adobe Commerce現在預設包含以客戶身分登入。 此功能可讓網站員工透過以客戶身分登入來協助客戶檢視他們看到的內容。

![已修正的問題](../assets/fix.svg) 屬性彙總現在可正確用於具有Elasticsearch的分層導覽

![已修正的問題](../assets/fix.svg) 依特殊字元搜尋順序現在可正常運作。

![已修正的問題](../assets/fix.svg) 按一下 **[!UICONTROL Clear All]** Button現在會展開所有篩選器，而不是將其收合。

![已修正的問題](../assets/fix.svg) 產品SKU/名稱現已納入「訂單歷史記錄」搜尋篩選條件摘要中。

![已修正的問題](../assets/fix.svg) 排序指標現在可在「我的採購單」格線中正確顯示。

![已修正的問題](../assets/fix.svg) 現在，您只能按一下「核准」、「取消」、「拒絕」及「採購單」按鈕一次。 之前，您可以按一下按鈕多次。

![已修正的問題](../assets/fix.svg) 採購單核准、拒絕、取消和驗證按鈕現在可在行動裝置上正確呈現。

![已修正的問題](../assets/fix.svg) 以前，核准具有已過期折扣的採購單時，會將訂單全額下單，而且不會更新採購單總計。 現在，採購單總計會更新以顯示正確的總計。

![已修正的問題](../assets/fix.svg) 2.3.4中引入了一個問題，其中自訂擴充功能屬性不會從客戶地址複製到報價地址。 此問題已修正。

![已修正的問題](../assets/fix.svg) 安裝B2B後，將類別指派給共用目錄時會出現SQL錯誤。 此問題已修正。

![已修正的問題](../assets/fix.svg) 由於不正確的變數型別值，管理員無法將可設定的產品新增至訂單。 選項下拉式清單不會填入。 此功能現在已正常運作。

![已修正的問題](../assets/fix.svg) 先前，編輯「未登入」群組的類別許可權時，儲存變更會發生錯誤。 此問題已修正。

![已修正的問題](../assets/fix.svg) 已新增修正，以允許商店管理員將產品新增至不在共用目錄中的訂單。 以前，新增不在目錄中的專案時，會出現錯誤訊息。

![已修正的問題](../assets/fix.svg) 先前，在執行指令之後 `php bin/magento indexer:set-dimensions-mode catalog_product_price website` 然後嘗試建立共用目錄時，會發生錯誤。 此問題已修正。

![已修正的問題](../assets/fix.svg) 新增公司並將公司管理員指派至非預設網站時，會傳送錯誤的網站ID，進而導致錯誤。 此問題已修正。

![已修正的問題](../assets/fix.svg) 之前，在將客戶移至另一個客戶群組後，使用以下專案將產品新增至訂單 _快速訂購_ 將失敗，並出現錯誤。 此問題已修正。

![已修正的問題](../assets/fix.svg) 先前，嘗試搭配B2B引號使用WebAPI來結帳時，系統會傳送不正確的值至API，進而導致發生錯誤。 此問題已修正。

![已修正的問題](../assets/fix.svg) 先前，透過API將公司設為「作用中」時，會發生錯誤。 此問題現已修正。

![已修正的問題](../assets/fix.svg) 由於不需要 `form` 標籤，當您在變更提議的運費後按下Enter鍵時，訂單頁面會自動重新整理。 此問題已修正。

![已修正的問題](../assets/fix.svg) 先前，在目錄頁面上設定產品顯示限制，且該限制小於產品總數時，會發生錯誤。 此功能現在可如預期運作。

![已修正的問題](../assets/fix.svg) 先前，變更公司的管理員時，會將原始的管理員地址複製到新的管理員，並為他們提供兩個地址。 現在，只會新增正確的地址。

![已修正的問題](../assets/fix.svg) 先前，當Git設為「允許並通知客戶」時，使用API儲存報價專案會失敗。 此API呼叫現在可如預期般運作。

![已修正的問題](../assets/fix.svg) 「固定產品稅捐」現在會顯示在「報價明細」頁面上。

![已修正的問題](../assets/fix.svg) 先前，在「我的報價」頁面的「註解」標籤中按一下附件時，檔案下載會失敗。 此行為現在會如預期般運作。

### 已知問題

- 在多網站部署中，Adobe Commerce在升級至B2B 1.2.0期間擲回例外狀況。 時間 `setup:upgrade` 執行，此錯誤發生於 `PurchaseOrder` 模組： `Module Magento_PurchaseOrder: Unable to apply data patch Magento\PurchaseOrder\Setup\Patch\Data\InitPurchaseOrderSalesSequence for moduleMagento_PurchaseOrder`. **因應措施**：安裝 `B2B-716 Add NonTransactionableInterface` 介面至 `InitPurchaseOrderSalesSequence` 資料修補程式hotfix現在可從 **我的帳戶** > **下載** 部分 `magento.com`.
- 如果折扣代碼在核准採購單(PO)之前過期，則PO會繼續顯示折扣金額，但是一旦核准了PO，訂單就會以非折扣總計下單。 **因應措施**：安裝 `B2B-709 Purchase Order Discount patch` 此問題的Hotfix，現在可從 **我的帳戶** > **下載** 部分 `magento.com`.
- 如果採購單中的料號無庫存，或採購單轉換為實際訂單時數量不足，則會發生錯誤。 如果啟用延期交貨，則會正常處理訂單。
