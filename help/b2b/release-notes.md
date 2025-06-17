---
title: '[!DNL Adobe Commerce B2B]發行說明'
description: 請檢閱發行說明，以瞭解 [!DNL Adobe Commerce B2B] 發行版本中的變更資訊。
exl-id: 77d8c20d-6667-41e3-8889-252f36e56fd8
feature: B2B, Release Notes
source-git-commit: 706b62170507da90934eeff1d894865b27713b55
workflow-type: tm+mt
source-wordcount: '8867'
ht-degree: 0%

---

# [!DNL Adobe Commerce B2B]發行說明

以下是B2B擴充功能發行說明，擷取Adobe在發行週期中新增的新增功能和修正，包括：

![新](../assets/new.svg)新功能
![已修正問題](../assets/fix.svg)修正和改良
![已知問題](../assets/bug.svg)已知問題

>[!NOTE]
>
>請參閱[產品可用性](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html)，以取得可用Adobe Commerce版本所支援B2B Commerce擴充功能版本的資訊。

## B2B v1.5.2-p1

*2025年6月10日*

[!BADGE 支援]{type=Informative tooltip="支援"} Adobe Commerce 2.4.8-p1、2.4.7-p6和2.4.6-p11安全性修補程式發行版本。
與Adobe Commerce版本2.4.7至2.4.7-p5、2.4.6至2.4.6-p10相容

![已修正問題](../assets/fix.svg)包含[安全性公告APSB25-50](https://helpx.adobe.com/security/products/magento/apsb25-50.html)中記錄的安全性修正。

## B2B 1.5.2

*2025年4月8日*

[!BADGE 支援]{type=Informative tooltip="支援"} Adobe Commerce 2.4.8、2.4.7-p5和2.4.6-p10安全性修補程式發行版本。
與Adobe Commerce版本2.4.7至2.4.7-p4、2.4.6至2.4.6-p9相容

B2B v1.5.2版本包含品質改良與錯誤修正。

### 公司管理

![新](../assets/new.svg)<!-- B2B-4123 -->管理員現在可以使用店面公司切換器，從單一帳戶管理多個公司。 主要優點包括：

- **簡化的多公司管理** — 管理員現在可以從單一使用者帳戶監督多個公司，不需要為每個公司建立和管理個別的登入。
- **高效的公司切換** — 直覺式介面可讓管理員快速切換公司並進行更新，在管理多個實體時提高生產力。
- **簡化營運** — 地區經理與業務負責人可以集中管理所有公司，讓決策更快速，業務運作更順暢。

此增強功能以B2B 1.5.0的多公司成員資格功能為基礎，該功能允許使用者屬於多個公司，但不支援跨公司的管理員存取權。 公司切換器不需要個別的管理員帳戶，同時維持適當的存取控制項和公司特定檢視。

### 公司

![已修正問題](../assets/fix.svg)<!-- B2B-4480 -->修正當來賓客戶以公司使用者身分登入，並在其購物車中放入產品時，會看到`No such entity with cartId = ?`錯誤訊息的問題。

### 可轉讓報價

![已修正問題](../assets/fix.svg) B2B v1.5.2版本包含下列可協商報價的修正：

- &#x200B;<!-- B2B-3252 -->[!UICONTROL Line Item Discount Amount]欄位現在會驗證輸入，以防止輸入負折扣值。
- &#x200B;<!-- B2B-3224 -->修正B2B客戶的長條列專案附註遭到截斷且難以閱讀的使用者體驗問題。
- &#x200B;<!-- B2B-2865 -->B2B客戶現在可以在建立報價時，使用小數值（例如1.5或2.75）指定產品數量。

### 報價範本

![新](../assets/new.svg)<!-- B2B-4104 --> B2B買家和賣家新增將外部檔案連結附加至報價範本的功能。 此功能允許直接從引號連結至在DocuSign和Adobe Sign等服務中託管的檔案，以補充現有的檔案附件功能。 主要優點包括：

- 透過直接存取重要合約與合約，簡化協同合作
- 透過即時存取最新檔案增強透明度
- 無需下載和上傳檔案，即可加快報價議價
- 使用外部檔案託管服務進行靈活的檔案管理

## B2B 1.5.1

*2025年2月11日*

[!BADGE 支援]{type=Informative tooltip="支援"} Adobe Commerce 2.4.7-p4+和2.4.6-p9+安全性修補程式發行版本。
與Adobe Commerce版本2.4.8-beta1至2.4.8-beta2、2.4.7至2.4.7-p3、2.4.6至2.4.6-p8相容

B2B v1.5.1版本包含品質改良和錯誤修正。

### 公司

![已修正問題](../assets/fix.svg)<!-- B2B-4422 -->如果客戶嘗試在「報價詳細資料」頁面上切換公司，系統現在會將客戶重新導向至&#x200B;*拒絕存取*&#x200B;頁面，以確保為一家公司建立的報價無法用來以另一家公司的價格下訂單。 以前，使用者可以使用一家公司的價格來建立報價，然後切換到另一家公司，以不同的價格下訂單。

### 明細專案折扣

![已修正問題](../assets/fix.svg)<!-- B2B-2938 -->解決報價重新計算案例中發現的效能降低問題，進而改善系統效率。 之前，在每個cart條列專案上新增兩個實體，導致資料庫要求明顯增加，導致效能降低。

### 可轉讓報價

![已修正問題](../assets/fix.svg)<!-- B2B-3820 -->系統現在會在JavaScript驗證套用至Luma Storefront報價範本頁面上的&#x200B;*[!UICONTROL min/max qty]*&#x200B;欄位時，保留UI元素的位置。 之前，套用JavaScript驗證至這些欄位會導致頁面上的其他UI元素發生位移。

### 購物車

![已修正問題](../assets/fix.svg)<!-- B2B-4222 -->推出新的購物車管理系統，專為管理多個公司帳戶的使用者簡化購物體驗所設計。 新系統將購物車與個別公司而非客戶帳戶建立關聯，以透過支援以下功能來簡化購物體驗並改善工作流程。

- **特定公司的購物車：** — 購物車現在已連結至個別公司，以支援特定公司的定價和產品選項。
- **順暢切換** — 使用者可以輕鬆地在不同公司帳戶之間切換，而不會影響每個公司的購物車內容。
- **內容完整性** — 所有購物車詳細資料都保留在個別公司的內容中，提供一致且可靠的購物體驗。

## B2B 1.5.0

*2024年10月30日*

[!BADGE 支援]{type=Informative tooltip="支援"} Adobe Commerce 2.4.7-p3+和2.4.6-p8+安全性修補程式發行版本。
與Adobe Commerce版本2.4.8-beta1、2.4.7至2.4.7-p2、2.4.6至2.4.6-p7相容。

Adobe Commerce B2B 1.5.0版也與PHP 8.3相容，並支援[GraphQL應用程式伺服器](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/concepts/application-server)。

B2B v1.5.0版本包含新功能、品質改善和錯誤修正。

>[!NOTE]
>
> 檢閱[回溯不相容變更](backward-incompatible-changes.md)主題中的重點和參考資訊，瞭解B2B 1.5.0版本中推出的回溯不相容變更(BIC)。

### 公司管理

![新](../assets/new.svg) **公司管理**<!--B2B-2901--> — 商戶現在可以將公司指派給指定的母公司，以階層式組織方式檢視和管理Adobe Commerce公司。 將公司指派給母公司後，母公司管理員可以管理公司帳戶。 只有授權管理員使用者可以新增和管理公司指派。 如需詳細資訊，請參閱[管理公司階層](manage-company-hierarchy.md)。

- 從管理員的&#x200B;*[!UICONTROL Company Account]*&#x200B;頁面上的新&#x200B;*[!UICONTROL Company Hierarchy]*&#x200B;區段新增及管理公司指派。

- 依新的&#x200B;*[!UICONTROL Company Type]*&#x200B;設定排序及篩選公司。 在公司網格中，*[!UICONTROL Company Type]*&#x200B;欄指出公司是個別公司或組織階層（父項或子項）的一部分。

![新的](../assets/new.svg) **大規模管理公司組態**<!--B2B-2849--> — 現在從&#x200B;*[!UICONTROL Companies]*&#x200B;或&#x200B;*[!UICONTROL Company Hierarchy]*&#x200B;網格管理公司時，可使用&#x200B;*[!UICONTROL Change company setting]*&#x200B;大量動作，快速變更所選公司的公司組態設定。 例如，如果您為一組公司建立新的共用目錄，您可以在單一動作中變更共用目錄組態，而非個別編輯每個公司。

![新](../assets/new.svg) API開發人員可以使用新的公司關係REST API端點`/V1/company/{parentId}/relations`來建立、檢視及移除公司指派。 請參閱&#x200B;*Web API開發人員指南*&#x200B;中的[管理公司物件](https://developer.adobe.com/commerce/webapi/rest/b2b/company-object/)。

### 公司帳戶

![新增](../assets/new.svg)<!--B2B-2828--> **多公司指派** — 將使用者指派給多個公司，簡化公司使用者的公司帳戶存取權。 例如，如果您的採購員從多個公司地點訂購，請建立單一帳戶，並將與採購員合作的所有公司指派給該帳戶。 然後，購買者可以登入一次，並從店面選擇公司，在公司帳戶之間切換。

>[!NOTE]
>
>一個公司使用者可以指派給多個公司，但他們只能是一個公司的公司管理員。

![新](../assets/new.svg) <!--B2B-2747--> **公司範圍選擇器** — 為指派給多個公司的公司使用者提供變更店面公司的功能。 範圍切換時，資料會更新以根據新的公司內容顯示資訊。 例如，如果新公司使用不同的共用目錄，則公司使用者會根據新共用目錄檢視產品、價格和其他資訊。 與訂單、報價單、報價範本相關的內容也會根據所選公司的內容更新。

>[!NOTE]
>購物車內容會反映目前客戶選取的專案。 如果客戶有作用中的購物車並選擇不同的公司，系統會提示他們更新購物車，以反映根據新公司內容的產品分類、定價和促銷折扣。 與新公司關聯的目錄中不可用的產品會從購物車中移除。 如果產品具有不同的價格或可用性，購物車會更新以反映所選公司內容中的可用資料。<!--B2B-4222-->

![已修正問題](../assets/fix.svg)<!--ACP2E-1933-->公司管理員現在可以從店面新增公司使用者。 以前，當管理員使用者嘗試新增使用者時，Commerce會記錄錯誤： `CRITICAL: Error: Call to a member function __toArray() on null in app/code/Magento/LoginAsCustomerLogging/Observer/LogSaveCustomerObserver.php:123`。

### 報價與報價範本

報價功能的改進可協助買家和賣家更有效地管理報價和報價議價。

![新的](../assets/new.svg) **報價範本**—<!--B2B-3367-->買家和賣家現在可以建立可重複使用且可自訂的報價範本，以簡化報價程式。 使用報價樣版時，報價議價處理可以完成一次，而採購員可以針對重複產生訂單產生預先核准的連結報價，而非針對每筆訂單執行報價議價處理。 報價範本藉由新增下列進階功能來擴充現有的報價功能：

- **訂單臨界值**&#x200B;可讓賣家設定最小與最大訂單承諾，確保買方遵守議定的採購量。
- **設定最小與最大料號訂購數量**&#x200B;可讓採購員彈性調整連結報價單上的訂購數量，而不需要新的樣版或進一步的議價。
- **追蹤已產生並成功完成訂單的連結報價數目**，以深入瞭解交涉合約的履行情況。
- **連結的報價單**&#x200B;是採購員從有效報價單範本產生的預先核准報價單，以根據報價單範本中議定的條款提交週期性訂單。

![新](../assets/new.svg) **現有報價功能改善**

- **已更新的Commerce存取控制清單(ACL)規則**&#x200B;允許B2B管理員和主管管理從屬使用者的報價和報價範本。 個別規則支援檢視、編輯和刪除存取權的精細設定。

- **將報價另存為草稿**<!--B2B-2566--> — 當從購物車建立[報價請求](quote-request.md)時，買家現在可以將報價另存為草稿，以便在與賣家開始報價議價程式之前，可以複查並更新報價。 草擬報價沒有到期日。 買家可以從其帳戶儀表板的[!UICONTROL My Quotes]區段檢閱和更新草稿報價。

- **重新命名報價**<!--B2B-2596--> — 購買者現在可以選取&#x200B;**[!UICONTROL Rename]**&#x200B;選項，從[報價詳細資料](account-dashboard-my-quotes.md#quote-actions)頁面變更報價名稱。 授權購買者在編輯報價時，可使用此選項。 名稱變更事件會記錄在「報價記錄檔」中。

- **重複報價**<!--B2B-2701--> — 買家和賣家現在可以複製現有的報價，建立新的報價。 在Admin或[店面](account-dashboard-my-quotes.md#quote-actions)的[報價詳細資料檢視](quote-price-negotiation.md#button-bar)中選取&#x200B;**[!UICONTROL Create Copy]**，以從報價詳細資料檢視建立副本。

- **將報價專案移至請購單清單**<!--B2B-2755--> — 如果採購員決定不將其納入報價議價程式，則他們現在可以彈性地移除報價中的產品，並將其儲存至請購單清單。

- **從報價移除多個產品**<!--B2B-2881--> — 在包含大量產品的報價上，購買者現在可以從報價移除多個產品，方法是選取這些產品，並使用報價詳細資料頁面上&#x200B;*[!UICONTROL Actions]*&#x200B;控制項中的&#x200B;*[!UICONTROL Remove]*&#x200B;選項。 在舊版中，購買者必須一次刪除一個產品。

- **明細專案折扣鎖定**<!--B2B-2597--> — 在報價議價期間，賣家可使用明細專案折扣鎖定，以在報價議價處理期間套用折扣時獲得更大的彈性。 例如，賣家可對專案套用特殊明細專案折扣，並鎖定專案以防止進一步折扣。 鎖定料號時，套用報價層級折扣時無法更新料號價格。 請參閱為購買者[&#128279;](sales-rep-initiates-quote.md)起始報價。

![已修正問題](../assets/fix.svg) **現有報價功能的修正**

- 現在系統會提示商戶在Admin中，按一下報價詳細資料檢視中的&#x200B;*[!UICONTROL Print]*&#x200B;按鈕，將報價儲存為PDF。 以前，商家會被重新導向到包含報價詳細資料的頁面。<!--ACP2E-1984-->

- 先前傳送具有`0`百分比的客戶報價並變更數量時，管理員會擲回例外狀況，但會儲存數量。 此修正套用後，將會擲回包含訊息的`0 percentage`適當例外狀況。<!--ACP2E-1742-->

- 在報價議價期間，賣家現在可以在「議價報價折扣」欄位中指定`0%`折扣，並將報價傳回給買方。 之前，如果賣家輸入0%的折扣，並將報價傳回給買方，管理員會傳回`Exception occurred during quote sending`錯誤訊息。<!--ACP2E-1742-->

- ReCaptcha V3已設定為店面結帳，現在，ReCaptcha驗證可正確在B2B報價的結帳程式中運作。 之前，驗證失敗並出現`recaptcha validation failed, please try again`錯誤訊息。 <!--ACP2E-2097-->

### 採購單

![已修正問題](../assets/fix.svg) <!--ACP2E-1825-->公司遭到封鎖後，與公司相關聯的使用者無法再下採購單。 以前，與公司相關聯的使用者可以在公司遭到封鎖時下訂單。

## B2B v1.4.2-p6

*2025年6月10日*

[!BADGE 支援]{type=Informative tooltip="支援"} Adobe Commerce 2.4.7-p6+和2.4.6-p11+安全性修補程式發行版本。

![已修正問題](../assets/fix.svg)包含[安全性公告APSB25-50](https://helpx.adobe.com/security/products/magento/apsb25-50.html)中記錄的安全性修正。

{{b2b-compatibility}}

## B2B v1.4.2-p5

*2025年4月8日*

[!BADGE 支援]{type=Informative tooltip="支援"} Adobe Commerce 2.4.7-p5+和2.4.6-p10+安全性修補程式發行版本。

![新](../assets/new.svg)已新增與Adobe Commerce 2.4.7-p5+和2.4.6-p10+安全性修補程式版本的相容性。

![已修正問題](../assets/fix.svg)包含[安全性公告APSB25-26](https://helpx.adobe.com/security/products/magento/apsb25-26.html)中記錄的安全性修正。

{{b2b-compatibility}}

## B2B v1.4.2-p4

*2025年2月11日*

[!BADGE 支援]{type=Informative tooltip="支援"} Adobe Commerce 2.4.7-p4+和2.4.6-p9+安全性修補程式發行版本。

![新](../assets/new.svg)已新增與Adobe Commerce 2.4.7-p4+和2.4.6-p9+安全性修補程式版本的相容性。

![已修正問題](../assets/fix.svg)包含[安全性公告APSB25-08](https://helpx.adobe.com/security/products/magento/apsb25-08.html)中記錄的安全性修正。

{{b2b-compatibility}}

## B2B v1.4.2-p3

*2024年10月8日*

[!BADGE 支援]{type=Informative tooltip="支援"} Adobe Commerce 2.4.7-p3+和2.4.6-p8+安全性修補程式發行版本。

![新](../assets/new.svg)已新增與Adobe Commerce 2.4.7-p3+和2.4.6-p8+安全性修補程式版本的相容性。

![已修正問題](../assets/fix.svg)包含[安全性公告APSB24-73](https://helpx.adobe.com/security/products/magento/apsb24-73.html)中記錄的安全性修正。

{{b2b-compatibility}}

## B2B v1.4.2-p2

[!BADGE 支援]{type=Informative tooltip="支援"} Adobe Commerce 2.4.7-p2+和2.4.6-p7+安全性修補程式發行版本。

![新](../assets/new.svg)已新增與Adobe Commerce 2.4.7-p2+和2.4.6-p7+安全性修補程式版本的相容性。

![已修正問題](../assets/fix.svg)包含安全性公告xxxx中記錄的安全性修正。

{{b2b-compatibility}}

## B2B v1.4.2-p1

*2024年8月9日*

[!BADGE 支援]{type=Informative tooltip="支援"} Adobe Commerce 2.4.7-p1+和2.4.6-p6+安全性修補程式發行版本。

![新](../assets/new.svg)已新增與Adobe Commerce 2.4.7-p1+和2.4.6-p6+安全性修補程式版本的相容性。

{{b2b-compatibility}}

## B2B v1.4.2

*2023年10月10日*

[!BADGE 支援]{type=Informative tooltip="支援"} Adobe Commerce 2.4.7版和從2.4.6到2.4.6-p5的版本。

B2B v1.4.2版本包含品質改良與錯誤修正。

![已修正問題](../assets/fix.svg) <!--B2B-2897-->如果賣方建立的買方報價包含在與買方公司關聯的共用目錄中不可用的產品SKU，則系統會顯示錯誤訊息`The SKU you entered is not available in the shared catalog. Please check the SKU and try again`。  除非賣家移除無法使用的產品，否則無法儲存報價。 之前，報價是以未提供的SKU儲存，且報價無法載入店面。

>[!IMPORTANT]
>
>Adobe Commerce B2B 1.4.2+版相容於PHP 8.2。如果您將Commerce執行個體升級至2.4.7+版，請確定執行個體使用PHP 8.2版，以保持與Adobe Commerce B2B版本的相容性。 此外，B2B 1.4.2+目前不支援[GraphQL應用程式伺服器](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/concepts/application-server)。

## B2B v1.4.1

*2023年8月7日*

[!BADGE 支援]{type=Informative tooltip="支援"} [Adobe Commerce 2.4.6-p2](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html)。 與Adobe Commerce 2.4.7-beta1相容。

B2B v1.4.1版本包含品質改良和錯誤修正。

![已修正問題](../assets/fix.svg) <!--ACP2E-1825-->公司遭到封鎖後，與公司相關聯的使用者無法再下採購單。 以前，與公司相關聯的使用者可以在公司遭到封鎖時下訂單。

![已修正問題](../assets/fix.svg) <!--ACP2E-1943-->店面現在已正確顯示產品延期交貨狀態。 以前，可供出貨的產品被錯誤地識別為延期交貨。

![已修正問題](../assets/fix.svg) <!--ACP2E-1862-->如果公司登錄檔單包含客戶檔案型別屬性，則公司建立後，註冊程式期間上傳的檔案現在會包含在公司管理員的帳戶資訊中。 之前，附件遺失。

![已修正問題](../assets/fix.svg) <!--ACP2E-1793-->可設定產品的色票選取器現在會如預期般顯示在請購單清單專案設定頁面中。 之前，色票選取器會在請購單清單專案設定頁面中顯示為下拉式欄位。

![已修正問題](../assets/fix.svg) <!--ACP2E-1968-->使用[公司GraphQL查詢](https://developer.adobe.com/commerce/webapi/graphql/schema/b2b/company/queries/company/#return-the-company-structure)傳回公司詳細資料時，結果現在可順利傳回，而不會發生錯誤。

## B2B v1.4.0

*2023年6月13日*

[!BADGE 支援]{type=Informative tooltip="支援"} [Adobe Commerce 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html)。 與Adobe Commerce 2.4.7-beta1相容

此發行版本包含B2B議價報價和多個錯誤修正的新功能和增強功能。

![新](../assets/new.svg)已新增與Adobe Commerce 2.4.7-beta1的相容性。

![新的](../assets/new.svg) **賣方起始的報價** — 賣方現在可以直接從「管理員」中的「報價」與「客戶」網格為買方起始報價。 此功能可簡化報價流程，並降低客戶的複雜性。 如果客戶尚未啟動訂單，則賣家可以代表客戶快速建立報價單，並開始議價處理。 之前，報價只能由買方從店面建立，或由以客戶身分登入的賣方建立。

![新的](../assets/new.svg) **明細專案折扣與議價**—<!--B2B-2440-->在報價中，B2B買方與賣家現在可以在明細專案層級進行議價，套用折扣與交換附註，直到達成協定為止。 備註建立與更新會包含在明細專案與報價記錄中，以追蹤溝通。 以前，買家和賣家只能在報價層級交換備註和套用折扣。

![已修正問題](../assets/fix.svg)啟用「採購單」選項，且選取使用PayPal付款選項建立的虛擬報價單時，Adobe Commerce現在會在付款期間顯示正確的詳細資料。 以前，在這些條件下，總計會顯示為零。

![已修正問題](../assets/fix.svg) <!--ACP2E-1504-->當您嘗試儲存信用額度超過999的公司時，不會再發生驗證錯誤。 先前，對於大於999的公司信用限制，Adobe Commerce插入了逗號分隔符號，這會導致驗證錯誤，阻止儲存更新。

![已修正問題](../assets/fix.svg) <!--ACP2E-1474-->當您以可轉讓報價下訂單時，選取的送貨地址現在會維持不變。 之前，當您下訂單時，選取的送貨地址會變更為預設送貨地址。

![已修正問題](../assets/fix.svg) <!--ACP2E-1429-->在B2B功能的存放區組態設定中，**[!UICONTROL Enable Shared Catalog direct products price assigning]**&#x200B;欄位現在會自動停用。 在店面，當&#x200B;**[!UICONTROL Enable Company]**&#x200B;設定或&#x200B;**[!UICONTROL Enable Shared Catalog]**&#x200B;設定設為&#x200B;**[!UICONTROL No]**&#x200B;時會隱藏它。

![已修正問題](../assets/fix.svg) <!--ACP2E-1683-->從店面建立公司帳戶時，Commerce現在會在處理公司註冊之前驗證電子郵件地址。 如果電子郵件地址無效，則操作會失敗且不會處理任何帳戶更新。 以前，即使建立公司帳戶的請求由於電子郵件地址無效而失敗，也會建立客戶帳戶。

![已修正問題](../assets/fix.svg) <!--ACP2E-1664-->在共用目錄和定價結構中包含雙引號的產品SKU不會再造成管理員發生錯誤。

![已修正問題](../assets/fix.svg) <!--ACP2E-1498-->已更新Commerce應用程式的Varnish設定，以防止訪客使用者看見來自其他客戶群組的資料。

### 已知問題

如果您在[Adobe Commerce 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html)版上安裝或升級B2B 1.4.0，會發生下列錯誤：

```
Your requirements could not be resolved to an installable set of packages.

  Problem 1
    - Root composer.json requires magento/extension-b2b 1.4.0 -> satisfiable by magento/extension-b2b[1.4.0].
    - magento/extension-b2b 1.4.0 requires magento/security-package-b2b 1.0.4-beta1 -> found magento/security-package-b2b[1.0.4-beta1] but it does not match your minimum-stability.

Installation failed, reverting ./composer.json and ./composer.lock to their original content.
```

您可以透過為具有[穩定性標籤](https://getcomposer.org/doc/04-schema.md#package-links)的B2B安全性套件新增手動相依性，來修正B2B安全性套件的手動相依性問題。 如需指示，請參閱[Adobe Commerce知識庫](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/installation-and-upgrade/b2b-1.4.0-installation-fails-on-adobe-commerce-2.4.6-p1-on-premises.html)。

## B2B v1.3.5-p10

*2025年4月8日*

[!BADGE 支援]{type=Informative tooltip="支援"} Adobe Commerce 2.4.6-p10+安全性修補程式發行版本。

![新](../assets/new.svg)已新增與Adobe Commerce 2.4.6-p10安全性修補程式版本的相容性。

![已修正問題](../assets/fix.svg)包含[安全性公告APSB25-26](https://helpx.adobe.com/security/products/magento/apsb25-26.html)中記錄的安全性修正。

## B2B v1.3.5-p9

*2025年2月11日*

[!BADGE 支援]{type=Informative tooltip="支援"} Adobe Commerce 2.4.6-p9+安全性修補程式發行版本。

![新](../assets/new.svg)已新增與Adobe Commerce 2.4.6-p9安全性修補程式版本的相容性。

![已修正問題](../assets/fix.svg)包含[安全性公告APSB25-08](https://helpx.adobe.com/security/products/magento/apsb25-08.html)中記錄的安全性修正。

## B2B v1.3.5-p8

*2024年10月8日*

[!BADGE 支援]{type=Informative tooltip="支援"} Adobe Commerce 2.4.6-p8+安全性修補程式發行版本。

![新](../assets/new.svg)已新增與Adobe Commerce 2.4.6-p8安全性修補程式版本的相容性。

![已修正問題](../assets/fix.svg)包含[安全性公告APSB24-73](https://helpx.adobe.com/security/products/magento/apsb24-73.html)中記錄的安全性修正。

## B2B v1.3.5-p7

*2024年8月9日*

[!BADGE 支援]{type=Informative tooltip="支援"} Adobe Commerce 2.4.6-p7+安全性修補程式發行版本。

![新](../assets/new.svg)已新增與Adobe Commerce 2.4.6-p7安全性修補程式版本的相容性。

## B2B v1.3.5

*2023年3月14日*

[!BADGE 支援]{type=Informative tooltip="支援"} Adobe Commerce 2.4.0 - 2.4.6和更新版本

![新](../assets/new.svg)已發行B2B 1.3.5-p2版，支援與Adobe Commerce 2.4.6-p2的相容性。

![新](../assets/new.svg)已發行B2B 1.3.5-p1版，支援與Adobe Commerce 2.4.6-p1的相容性。

>[!NOTE]
>
>將Commerce從2.4.6升級至[最新版本](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html#2.4.6)後，請務必更新至支援的B2B 1.3.5修補程式版本。 或者，請將B2B擴充功能從1.3.5版升級至1.4.0版或更新版本，以取得最新功能。

![新](../assets/new.svg)已新增對Adobe Commerce 2.4.6的支援。

![已修正問題](../assets/fix.svg) <!--- ACP2E-689-->在啟用「採購單」選項且已選取使用PayPal付款選項建立的虛擬報價單時，Adobe Commerce現在會在付款期間顯示正確的詳細資料。 以前，在這些條件下，總計會顯示為零。

![已修正問題](../assets/fix.svg) <!--- ACP2E-609--> **允許瀏覽類別**&#x200B;設定的客戶群組清單不再包含與共用目錄相關的客戶群組。

![已修正問題](../assets/fix.svg) <!--- ACP2E-1244-->稅務/VAT編號客戶屬性現在可如預期在管理員和店面中使用公司管理員帳戶。 建立公司帳戶不再需要自訂稅捐/VAT屬性。 先前，當商家使用自訂Tax/VAT屬性建立公司帳戶時，Adobe Commerce會在店面和管理員上擲回驗證錯誤。

![已修正問題](../assets/fix.svg) <!--- ACP2E-1236-->在特定範圍上停用共用目錄功能現在可以正常運作。 之前，當商家儲存共用目錄設定時，Adobe Commerce會設定無效的範圍。

![已修正問題](../assets/fix.svg) <!--- ACP2E-1203-->管理員使用者現在可以為公司使用者儲存客戶自訂屬性值。 以前無法儲存公司使用者的客戶自訂屬性。

![已修正問題](../assets/fix.svg) <!--- ACP2E-1221-->當已指派許多公司許可權時，透過GraphQL提供的公司許可權驗證即可解決效能問題。

![已修正問題](../assets/fix.svg) <!--- ACP2E-1242-->當使用快速訂購新增數量超過可用存貨的產品時，Adobe Commerce不再在購物車頁面上擲回錯誤。

![已修正問題](../assets/fix.svg) <!--- ACP2E-1090--> `SELECT`公司許可權作業的效能已改善。

![已修正問題](../assets/fix.svg) <!--- ACP2E-2456-->當查詢的類別沒有明確設定類別許可權時，類別查詢現在會根據商店組態設定傳回產品價格。

![已修正問題](../assets/fix.svg) <!--- ACP2E-6829-->使用核准的報價請求完成購買時，**[!UICONTROL Place Order]**&#x200B;按鈕現在可如預期運作。 可協商的報價`negotiableQuoteCheckoutSessionPlugin`外掛程式的問題已解決。

## B2B v1.3.4-p13

*2025年6月10日*

[!BADGE 支援]{type=Informative tooltip="支援"} Adobe Commerce 2.4.0和更新版本

![新](../assets/new.svg)已新增對Adobe Commerce 2.4.5-p12的支援。

![已修正問題](../assets/fix.svg)包含[安全性公告APSB25-50](https://helpx.adobe.com/security/products/magento/apsb25-50.html)中記錄的安全性修正。

## B2B v1.3.4-p12

*2025年4月8日*

[!BADGE 支援]{type=Informative tooltip="支援"} Adobe Commerce 2.4.0和更新版本

![新](../assets/new.svg)已新增對Adobe Commerce 2.4.5-p12的支援。

![已修正問題](../assets/fix.svg)包含[安全性公告APSB25-26](https://helpx.adobe.com/security/products/magento/apsb25-26.html)中記錄的安全性修正。

## B2B v1.3.4-p11

*2025年2月11日*

[!BADGE 支援]{type=Informative tooltip="支援"} Adobe Commerce 2.4.0和更新版本

![新](../assets/new.svg)已新增對Adobe Commerce 2.4.5-p11的支援。

![已修正問題](../assets/fix.svg)包含[安全性公告APSB25-08](https://helpx.adobe.com/security/products/magento/apsb25-08.html)中記錄的安全性修正。

## B2B v1.3.4-p10

*2024年10月9日*

[!BADGE 支援]{type=Informative tooltip="支援"} Adobe Commerce 2.4.0和更新版本

![新](../assets/new.svg)已新增對Adobe Commerce 2.4.5-p10的支援。

![已修正問題](../assets/fix.svg)包含[安全性公告APSB24-73](https://helpx.adobe.com/security/products/magento/apsb24-73.html)中記錄的安全性修正。

## B2B v1.3.4

*2022年8月9日*

[!BADGE 支援]{type=Informative tooltip="支援"} Adobe Commerce 2.4.0和更新版本

![新](../assets/new.svg)已新增對Adobe Commerce 2.4.5的支援。

![已修正問題](../assets/fix.svg) <!--- ACP2E-453-->Adobe Commerce不再於每次API呼叫更新現有公司時傳送電子郵件通知。 現在，電子郵件只會在公司建立時傳送。

![已修正問題](../assets/fix.svg) <!--- ACP2E-406-->啟用&#x200B;**[!UICONTROL Enable Cross Border Trade]**&#x200B;稅捐計算設定時，Adobe Commerce現在會正確計算可轉讓報價的總計。

![已修正問題](../assets/fix.svg) <!--- ACP2E-322-->啟用&#x200B;**[!UICONTROL Move out of stock to the bottom]**&#x200B;設定後，庫存更新後，可設定的產品現在會移至產品清單中的最後一個位置。 實施新的自訂資料庫查詢，以確保Elasticsearch索引排序順序現在遵循管理員啟用的排序順序。 先前，啟用此設定時，可設定的產品及其子產品不會移至清單底部。

![已修正問題](../assets/fix.svg) <!--- ACP2E-308-->採購單電子郵件現在會遵循多網站部署中每個網站的電子郵件傳送設定。 **[!UICONTROL Disable Email Communications]**&#x200B;設定的檢查已新增至電子郵件佇列的自訂邏輯。 之前，Adobe Commerce沒有遵循次要網站的電子郵件傳送設定。

![已修正問題](../assets/fix.svg) <!--- ACP2E-302-->為了清楚起見，已變更「快速訂購」頁面之SKU欄位的標題。

![已修正問題](../assets/fix.svg) <!--- ACP2E-543-->當購物者在&#x200B;**輸入SKU或產品名稱**&#x200B;欄位中輸入無效的SKU時，Adobe Commerce現在會顯示資訊更豐富的錯誤訊息。

![已修正問題](../assets/fix.svg) <!--- ACP2E-1753-->在儲存公司後，公司管理員的&#x200B;**[!UICONTROL Account Created in]**&#x200B;欄位現在會保留其預期值。

![已修正問題](../assets/fix.svg) <!--- ACP2E-722 -->在擷取依`uid`篩選的請購單清單時，`customer`查詢不再傳回空白結果。

![已修正問題](../assets/fix.svg) <!--- ACP2E-210 -->在`collectQuoteTotals`呼叫之前新增外掛程式，以確保商店積分僅套用一次。

![已修正問題](../assets/fix.svg) <!--- ACP2E-665 -->當管理員從管理員中刪除客戶的帳戶時，現在會將客戶重新導向至登入頁面。 之前，Adobe Commerce擲回錯誤。 外掛程式(`SessionPlugin`)程式碼區塊現在位於`try…catch`區塊內。 之前，此程式碼不會包裝在一般例外狀況處理區塊中。

![已修正問題](../assets/fix.svg) <!--- ACP2E-661 -->在行動模式的「快速訂購」頁面上，輸入有效的產品名稱或SKU後按&#x200B;**Enter**，購物者就會如預期前往下一個欄位。

![已修正問題](../assets/fix.svg) <!--- ACP2E-607 -->公司名稱現在會如預期顯示在結帳工作流程的帳單和送貨地址區段。

![已修正的問題](../assets/fix.svg) <!--- ACP2E-375 -->當停用&#x200B;**[!UICONTROL Zero Subtotal Checkout]**&#x200B;付款方式時，商店點數現在無法使用。 以前，在管理員下訂單時，「商店積分」核取方塊無法運作。 應用程式未以商店信用下訂單，並顯示此錯誤： `The requested Payment Method is not available`。

## B2B v1.3.3-p14

*2025年6月10日*

[!BADGE 支援]{type=Informative tooltip="支援"} Adobe Commerce 2.4.0和更新版本

![新](../assets/new.svg)已新增對Adobe Commerce 2.4.5-p12的支援。

![已修正問題](../assets/fix.svg)包含[安全性公告APSB25-50](https://helpx.adobe.com/security/products/magento/apsb25-50.html)中記錄的安全性修正。

## B2B v1.3.3

*2022年8月9日*

[!BADGE 支援]{type=Informative tooltip="支援"} Adobe Commerce 2.4.0和更新版本

![新](../assets/new.svg)已新增對Adobe Commerce 2.4.4的支援。

![已修正問題](../assets/fix.svg) <!--- MC-41985-->在擁有超過100,000個公司角色的部署中，從Adobe Commerce 2.3.x升級至Adobe Commerce 2.4.x所需的時間已大幅減少。

![已修正問題](../assets/fix.svg) <!--- MC-42153-->啟用&#x200B;**[!UICONTROL Payment on Account]**&#x200B;付款方式時，POST `V1/order/:orderId/invoice`要求現在支援建立部分發票。 之前，Adobe Commerce擲回此錯誤： `An invoice for partial quantities cannot be issued for this order. To continue, change the specified quantity to the full quantity`。 [GitHub-32428](https://github.com/magento/magento2/issues/32428)

![已修正問題](../assets/fix.svg) <!--- MC-41975-->當客戶的購物車包含其他產品時，PayPal Payflow Pro現在可與B2B可轉讓報價一起正常運作。 Adobe Commerce現在能成功處理訂單，並如預期傳送電子郵件給客戶。 之前，Adobe Commerce擲回嚴重錯誤，並傳送確認電子郵件給客戶，其中包含零值。

![已修正問題](../assets/fix.svg) <!--- MC-41819-->排除共用目錄中的部分產品後，目錄搜尋結果頁面上現在會正確顯示分頁。

![已修正問題](../assets/fix.svg) <!--- MC-42886-->在Admin中建立或儲存公司使用者時，客戶自訂屬性現在會如預期儲存。

![已修正問題](../assets/fix.svg) <!--- MC-42927--> 「建立新公司」表單上的「**[!UICONTROL Submit]**」按鈕現在在按一下後已停用，以防止提交多個表單。 以前，您可以多次提交此表單，只要反複按一下此按鈕就會產生錯誤。

![已修正問題](../assets/fix.svg) <!--- MC-42787-->當購物者登入已停用重新訂購的商店時，Adobe Commerce不再在店面上顯示重新訂購連結。

![已修正問題](../assets/fix.svg) <!--- MC-43115-->共用目錄啟用時，SKU的快速訂購搜尋現在不區分大小寫。

![已修正問題](../assets/fix.svg) <!--- MC-42203-->您現在可以在建立公司時更新客戶屬性的檔案。 先前，當您嘗試建立具有型別`File`之附件的公司時，Adobe Commerce並未建立公司，並將此錯誤記錄於例外狀況記錄檔： `Something went wrong while saving file`。

![已修正問題](../assets/fix.svg) <!--- MC-42242-->您現在可以使用客戶帳戶來建立公司，該客戶帳戶具有型別為(`File`)或(`Image`)的自訂屬性。 以前，如果帳戶具有其中一個可自訂的選項，公司編輯頁面載入器無法解析，這會阻止編輯公司詳細資訊。

![已修正問題](../assets/fix.svg) <!--- MC-42268-->啟用共用目錄時，`products`查詢現在會傳回正確的`total_count`欄位。

![已修正問題](../assets/fix.svg) <!--- MC-42203-->您現在可以在建立公司時更新客戶屬性的檔案。 先前，當您嘗試建立具有型別`File`之附件的公司時，Adobe Commerce並未建立公司，並將此錯誤記錄於例外狀況記錄檔： `Something went wrong while saving file`。

![已修正問題](../assets/fix.svg) <!--- MC-43178-->在您停用線上送貨方法後，_公司組態_&#x200B;和&#x200B;_建立公司_&#x200B;頁面現在會如預期般運作。 已新增驗證，以防止嘗試處理停用的送貨模組。 Adobe Commerce之前會顯示此錯誤： `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`。

![已修正問題](../assets/fix.svg) <!--- MC-42214--> _類別_&#x200B;頁面現在會在部分索引期間產生許可權時，顯示一致的產品資料。 新的目錄許可權部分索引器已新增至此程式。 先前，索引器執行時顯示的資料不正確。

![已修正問題](../assets/fix.svg) <!--- MC-42567-->使用目錄許可權並將產品指派給共用目錄時，`categoryList`查詢現在會傳回正確數量的產品。

![已修正問題](../assets/fix.svg) <!--- MC-42528--> `categoryList`查詢現在遵循類別許可權，並只傳回允許的類別。 之前，它會傳回所有指派和未指派的類別。

![已修正問題](../assets/fix.svg) <!--- MC-42399--> `rest/V1/company/{id}`要求現在會如預期傳回`is_purchase_order_enabled`屬性值。

![已修正問題](../assets/fix.svg) <!--- ACP2E-128-->自訂客戶屬性現在會如預期般顯示在&#x200B;_公司管理員_&#x200B;標籤中。

![已修正問題](../assets/fix.svg) <!--- ACP2E-130--> 「我的帳戶」頁面上的「我的願望清單」區塊現在會如預期般顯示給公司管理員和公司使用者。

![已修正問題](../assets/fix.svg) <!--- ACP2E-133-->購物車中不再顯示快速訂購錯誤。 之前，在目錄中找不到SKU時，Adobe Commerce會在購物車中顯示此錯誤： `The SKU was not found in the catalog`。

![已修正問題](../assets/fix.svg) <!--- ACP2E-194-->已最佳化共用目錄儲存作業，以便更快速地執行。 以前，儲存與許多客戶群組的共用目錄可能需要幾分鐘的時間。

![已修正問題](../assets/fix.svg) <!--- MC-42240-->刪除父類別時，Adobe Commerce現在會從`sharedcatalog_category_permissions`表格中刪除所有子類別許可權。 之前，系統只會移除父類別資料。

## B2B v1.3.2

*2022年8月29日*

[!BADGE 支援]{type=Informative tooltip="支援"} Adobe Commerce 2.4.0和更新版本

![新](../assets/new.svg)已新增對Adobe Commerce 2.4.3的支援。

![已修正問題](../assets/fix.svg) <!--- MC-39862--> Adobe Commerce現在已成功傳送有關過期可協商報價的更新電子郵件。 以往，當可轉讓報價過期時，Adobe Commerce不會傳送更新電子郵件。

![已修正問題](../assets/fix.svg) <!--- MC-40682-->Adobe Commerce現在已順利傳送更新電子郵件，說明即將到期以及遺失`cron`工作時過期的協商報價。

### 公司

![已修正問題](../assets/fix.svg) <!--- MC-41542--> 「建立新公司帳戶」頁面的「國家/地區」下拉式欄位不再列出空白選項值。 先前，前兩個選項值和國家/地區代碼`AN`是空的。

![已修正問題](../assets/fix.svg) <!--- MC-41260-->按一下公司使用者所建立訂單的&#x200B;**[!UICONTROL Return]**&#x200B;按鈕，現在會依預期將管理使用者重新導向至建立退貨頁面。 之前，管理員會重新導向至「訂單歷史記錄」頁面。

![已修正問題](../assets/fix.svg) [!BADGE 僅限PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"} <!--- MC-40798-->在`bin/magento setup:upgrade`期間執行`app/code/Magento/PurchaseOrder/Setup/Patch/Data/InitPermissions.php::apply`方法時，Adobe Commerce不會再因記憶體不足錯誤而失敗。 以往，Adobe Commerce在初始化許可權時並未使用批次大小進行集合，而是載入所有公司角色的集合。

![已修正問題](../assets/fix.svg) <!--- MC-40551-->公司使用者現在可以編輯和更新客戶自訂屬性值。 以前，這些屬性無法與建立和編輯使用者表單正確繫結。 公司使用者可以輸入不同的屬性值，但Adobe Commerce未正確儲存這些值。

![已修正問題](../assets/fix.svg) <!--- MC-32653-->公司角色許可權的資源樹狀結構現在可以如預期般轉譯。 以前，即使存在有效的翻譯檔案，許可權樹狀結構也不會翻譯。

![已修正問題](../assets/fix.svg) <!--- MC-40358--> Adobe Commerce現在會如預期為B2B使用者儲存自訂客戶屬性值。 之前，建立包含自訂客戶屬性的公司帳戶會觸發範本錯誤，且Adobe Commerce未成功載入表單。 將引數新增至`company_create_account`的版面配置解決了此問題。

![已修正問題](../assets/fix.svg) <!--- MC-41721-->公司使用者篩選器（例如「顯示所有使用者」、「顯示作用中使用者」和「顯示非作用中使用者」）現在可如預期般運作。 先前，篩選公司使用者頁面上的動作會造成JavaScript錯誤。

### 公司評價

![已修正問題](../assets/fix.svg) <!--- MC-41551-->帳戶受限且僅包含網站層級許可權的管理員現在可以建立使用網站以外其他貨幣的公司。

![已修正問題](../assets/fix.svg) <!--- MC-41523--> Adobe Commerce現在會從正確的`from`電子郵件地址和範圍傳送公司電子郵件。 以往，在傳送公司信用指派或更新電子郵件時，Adobe Commerce不會考量網站範圍。

### 快速訂購

![已修正問題](../assets/fix.svg) <!--- MC-42104-->從CSV檔案使用快速訂購功能建立訂單，對不存在的SKU現在可如預期般運作。

![已修正問題](../assets/fix.svg) <!--- MC-40268-->使用快速訂購功能來搜尋多個SKU現在可如預期運作。 以前，結果包括重複的專案。

![已修正問題](../assets/fix.svg) <!--- MC-40261-->當您在快速訂購期間使用SKU選取多個產品時，「新增的產品」清單現在會顯示以小寫和大寫輸入的SKU。

![已修正問題](../assets/fix.svg) <!--- MC-40225-->使用快速訂購現在會新增購物者指定數量的產品。 之前，即使購物者指定的數量超過一個，Adobe Commerce也只新增一個產品。

![已修正問題](../assets/fix.svg) <!--- MC-41283-->快速訂購自動完成功能現在可與部分SKU搭配使用。

![已修正問題](../assets/fix.svg) <!--- MC-41299--> Adobe Commerce現在會在「快速訂購」頁面的自動建議清單與搜尋結果上，顯示已設定為&#x200B;**未個別顯示的產品**。

![已修正問題](../assets/fix.svg) <!--- MC-42402-->購物者現在可以使用快速訂購表單，依包含大寫字元的SKU新增多個產品。 之前，僅新增第一個產品。

### 可轉讓報價

![已修正問題](../assets/fix.svg) <!--- MC-41232-->在URL欄位中貼上可轉讓報價的連結並成功登入後，購物者現在會重新導向至可轉讓報價頁面。 之前，購物者會被重新導向至「我的帳戶」頁面。

![已修正問題](../assets/fix.svg) <!--- MC-39317-->對於在結帳期間建立之客戶帳戶包含具有日期可自訂選項之產品的訂單，重新排序現在可如預期運作。 之前，Adobe Commerce不會處理重新排序並顯示此錯誤： `The product has required options. Enter the options and try again`。

![已修正問題](../assets/fix.svg) <!--- MC-39063-->當採購單模組停用時，可轉讓報價單的送貨地址在結帳期間無法再編輯。 此行為是先前修正`isQuoteAddressLocked`從可轉讓報价籤出轉譯器移除所導致。

![已修正問題](../assets/fix.svg) <!--- MC-38967-->商戶現在可以從管理員新增產品至可轉讓的報價。

### 採購單

![已修正問題](../assets/fix.svg) <!--- MC-39983--> Adobe Commerce現在會在您使用PayPal Express Checkout下採購單時（當&#x200B;**[!UICONTROL Name Prefix]**&#x200B;屬性設定為`required`時），依預期顯示資訊性錯誤訊息。 之前，Adobe Commerce不會下訂單或顯示錯誤訊息。

![已修正問題](../assets/fix.svg) <!--- MC-39620-->啟用Google Tag Manager時，採購訂單模組中帳單地址的UI元件現在會正確使用報價地址。 之前，付款頁面上發生JavaScript錯誤。

### 請購單清單

![已修正問題](../assets/fix.svg) <!--- MC-40426-->商戶現在可以使用POST `rest/all/V1/requisition_lists`端點來建立客戶的請購單清單。 之前，當您嘗試建立請購單清單時，Adobe Commerce擲回這個400錯誤： `Could not save Requisition List`。

![已修正問題](../assets/fix.svg) <!--- MC-41123-->當購物車也包含無庫存產品時，購物車的庫存產品現在會出現&#x200B;**[!UICONTROL Add to Requisition List]**&#x200B;按鈕。 先前，如果購物車包含兩個產品，其中一個沒有庫存，則這兩個產品都不會顯示&#x200B;_[!UICONTROL Add to Requisition List]_&#x200B;按鈕。

![已修正問題](../assets/fix.svg) <!--- MC-40877-->您現在可以使用REST API將產品新增至請購單清單。

![已修正問題](../assets/fix.svg) <!--- MC-40155-->請購單清單&#x200B;**[!UICONTROL Latest Activity Date]**&#x200B;值現在符合地區設定格式。

![修正問題](../assets/fix.svg) <!--- MC-39580-->當您從請購單清單編輯套件組合產品時，Adobe Commerce不再擲回嚴重錯誤。

![已修正問題](../assets/fix.svg) <!--- MC-40454-->現在，當您從請購單清單新增具有可自訂選項`(File)`的產品至願望清單時，Adobe Commerce會顯示正確的產品價格。 上傳檔案的連結也會如預期般顯示。 之前，Adobe Commerce顯示錯誤的產品價格，且不顯示檔案連結。

![已修正問題](../assets/fix.svg) <!--- MC-36383-->現在可以從請購單清單將具有自訂選項`(File)`的產品新增到購物車。

### 共用目錄

![已修正問題](../assets/fix.svg) <!--- MC-40497-->角色限製為特定網站的管理員現在可以建立、檢視及編輯共用目錄。 之前，當角色有限的管理員嘗試建立共用目錄時，Adobe Commerce會擲回嚴重錯誤。

![已修正問題](../assets/fix.svg) <!--- MC-41337-->階層式導覽結果現在包含具有篩選屬性的精確產品計數，購物者現在可以套用多個篩選器。 之前，僅可套用一個篩選器，而Adobe Commerce在分層導覽中顯示不準確的產品計數。

![已修正問題](../assets/fix.svg) <!--- MC-40779--> Adobe Commerce現在會在搜尋結果中的階層式導覽篩選器中正確顯示產品計數。 之前，「搜尋結果」頁面的外掛程式沒有使用Elasticsearch，而是向資料庫發出新的查詢。

![已修正問題](../assets/fix.svg) <!--- MC-39978-->當商家從預設共用目錄中刪除所有產品時，Adobe Commerce不再刪除層級價格。

![已修正問題](../assets/fix.svg) <!--- MC-39802-->篩選器現在已依目前類別篩選，並在共用目錄啟用時在所有頁面上正確顯示。 之前，僅針對目前頁面錯誤地計算篩選器，且沒有按目前類別篩選。

![已修正問題](../assets/fix.svg) <!--- MC-39522-->啟用共用目錄時，GraphQL `products`查詢不再傳回未指派給共用目錄之產品的價格範圍和類別。 以前，查詢會傳回產品的彙總，即使產品本身並未在`items`陣列中傳回。

## B2B v1.3.1

*2021年2月9日*

[!BADGE 支援]{type=Informative tooltip="支援"} Adobe Commerce 2.4.0和更新版本

![新](../assets/new.svg)已新增對Adobe Commerce 2.4.2的支援。

採購單現在支援![新的](../assets/new.svg)線上付款方式。

![已修正問題](../assets/fix.svg)當此產品用於先前訂單時，直接從請購單清單將可設定的產品加入購物車不再傳回系統錯誤。

![已修正問題](../assets/fix.svg)部署分割資料庫組態時，Adobe Commerce現在會正確顯示採購單的「需要我的核准」標籤。

![已修正問題](../assets/fix.svg)當您檢視採購單時，Adobe Commerce現在會顯示有關套裝產品和禮品卡的詳細資料。

![已修正問題](../assets/fix.svg)在啟用&#x200B;**[!UICONTROL Website Restriction]**&#x200B;且&#x200B;**[!UICONTROL Restriction Mode]**&#x200B;設定為`Private Sales: Login Only`的商店中瀏覽時，在登入購物者的帳戶後，購物者現在會如預期重新導向。 之前，購物者會被重新導向至商店首頁。<!--- MC-38934-->

![已修正問題](../assets/fix.svg)在包含許多客戶(大於13000)的B2B公司階層部署中，訂單歷史記錄現在會如預期般載入公司管理員的帳戶儀表板頁面。 先前，訂單歷史記錄載入緩慢或完全沒有載入，且Adobe Commerce顯示503錯誤。<!--- MC-38830-->

![修正問題](../assets/fix.svg)當您從「類別」頁面將具有自訂選項之未設定產品新增至請購單清單時，Adobe Commerce不再顯示多重相同的警告訊息。<!--- MC-38342-->

![已修正問題](../assets/fix.svg)啟用B2B共用目錄時，新的和重複的產品現在會如預期般顯示在類別頁面上。<!--- MC-38307-->

![已修正問題](../assets/fix.svg)當公司的客戶群組更新時，Adobe Commerce現在會維護與公司管理員關聯的正確`store_id`。 先前，群組更新時，`store_id`已變更為預設存放區。<!--- MC-38196-->

![已修正問題](../assets/fix.svg) Adobe Commerce現在會將群組產品儲存至請購單清單，作為簡單產品清單，其方式與將群組產品新增至購物車相同。 先前，由於Adobe Commerce儲存群組產品的方式，請購單清單中群組產品的連結一律會重新導向至簡單產品，而非群組產品。<!--- MC-38049-->

![已修正問題](../assets/fix.svg)您現在可以在匯出CSV格式的訂單資訊時，依&#x200B;**[!UICONTROL Company Name]**&#x200B;欄位篩選訂單。 之前，Adobe Commerce在`var/export/{file-id}`中記錄錯誤。<!--- MC-37785-->

![已修正問題](../assets/fix.svg)當您在店面選取[建立新請購單清單]索引標籤時，Adobe Commerce現在會如預期顯示[建立請購單清單]快顯功能表。<!--- MC-37915-->

![已修正問題](../assets/fix.svg)請購單清單現在包含已新增至清單的所有分組產品和數量。 先前，當商家從產品詳細資料頁面將產品新增到請購單清單後，Adobe Commerce會顯示此錯誤： `1 product(s) require your attention - Options were updated. Please review available configurations`。<!--- MC-37621-->

![已修正問題](../assets/fix.svg)當您在多網站部署中建立公司時，正確的商店檢視現在會與相關網站相關聯。 之前，您無法建立公司，Adobe Commerce會顯示此錯誤： `The store view is not in the associated website`。<!--- MC-37488-->

![已修正問題](../assets/fix.svg)由SKU使用快速訂購來訂購產品不會再導致CSV檔案中的產品數量重複。<!--- MC-37427-->

![已修正問題](../assets/fix.svg)當「快速訂購」頁面的&#x200B;_[!UICONTROL Enter Multiple SKUs]_&#x200B;區段包含空白值時，**[!UICONTROL Add to Cart]**&#x200B;按鈕不再遭到封鎖。 Adobe Commerce現在改為顯示訊息，提示您輸入有效的SKU。<!--- MC-37387-->

![已修正問題](../assets/fix.svg)當您從請購單清單提交產品評論時，Adobe Commerce現在會在產品頁面上顯示此訊息： `You submitted your review for moderation`。 評論也會顯示在擱置評論頁面上（管理員&#x200B;**[!UICONTROL Marketing]** > **[!UICONTROL Pending Reviews]**）。 之前，雖然Adobe Commerce已將評論新增至待處理評論的清單，但在產品頁面上擲回404錯誤。<!--- MC-37119-->

![已修正問題](../assets/fix.svg) `sharedCatalogUpdateCategoryPermissions`消費者的效能已改善。 建立共用目錄後，目錄許可權索引器現在只會使用共用目錄中的客戶群組ID，而非所有客戶群組。<!--- MC-36770-->

![已修正問題](../assets/fix.svg)與購物者的非預設地址相關聯的自訂客戶地址屬性欄位，現在會如預期般儲存在店面結帳工作流程中。<!--- MC-36630-->

![已修正問題](../assets/fix.svg)現在可如預期透過Admin REST API (`rest/V1/carts/{<CART_ID>/items`)為購物者下屬於商店預設共用目錄之產品的訂單。 在`\Magento\SharedCatalog\Plugin\Quote\Api\ValidateAddProductToCartPlugin::beforeSave`中驗證共用目錄許可權之前，Adobe Commerce現在會檢查產品是否已指派給公用目錄。 之前，Adobe Commerce未將產品新增至購物者的購物車，因此擲回此錯誤： `No such shared catalog entity`。<!--- MC-36535-->

![已修正問題](../assets/fix.svg) Adobe Commerce現在會從Adobe Commerce商店的地址傳送新的公司使用者註冊電子郵件。 之前，這封電子郵件是透過公司管理員的位址傳送的。<!--- MC-36480-->

![已修正問題](../assets/fix.svg) Adobe Commerce現在會在允許商家儲存新屬性之前，檢查自訂屬性是否與保留的公司屬性名稱重複。<!--- MC-36282-->

![已修正問題](../assets/fix.svg) `credit_history`查詢現在會傳回指定公司原始配置金額與購買金額的信用記錄。 之前，此查詢傳回錯誤。

![已修正問題](../assets/fix.svg) 「編輯帳戶資訊」頁面上的&#x200B;**[!UICONTROL Company]**&#x200B;及&#x200B;**[!UICONTROL Job Title]**&#x200B;欄位已無法再編輯。

### 已知問題

- B2B買家可以使用線上付款方式，略過一般的採購單流程。 如果購買者能將結帳總數減至0 （例如，透過促銷代碼或禮品卡），然後移除代碼或禮品卡，就可能發生這種情況。 即使在這些條件下，Adobe Commerce仍會根據所指派目錄中的專案價格，下正確金額的訂單。 **_因應措施_**：啟用線上付款方式以核准採購單時，請停用禮品卡與優惠券代碼。<!--- B2B-1603-->

- 當買家嘗試使用PayPal Express Checkout在停用&#x200B;**[!UICONTROL In-Context Mode]**&#x200B;時從採購單下訂單時，系統會重新導向至購物車。<!--- B2B-1604-->

- 當採購員建立採購單，然後導覽至結帳頁面時，Adobe Commerce有時會顯示404錯誤。 當採購員先前使用線上付款方式建立不同的採購單，而未完成先前的採購就瀏覽至結帳頁面時，就會發生此錯誤。 採購員仍然可以下採購單。 **_因應措施_**：無。<!--- B2B-1605-->

- 在採購單結帳期間，即使買方在最後結帳期間變更付款方式，特定付款方式的折扣仍會持續存在。 因此，客戶可獲得無權享有的折扣。 發生此問題是因為儘管付款方式有所變更，原始付款方式的購物車規則仍會套用。 **_因應措施_**：無。 請參閱[Adobe Commerce 2.4.2 B2B已知問題：付款方式變更後，線上採購單的折扣仍會保留](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/magento-2.4.2-b2b-discount-remains-pay-method-change.html) _知識庫_&#x200B;文章。<!-- B2B-1012 -->

- `deleteRequisitionListOutput`查詢會傳回已刪除的請購單清單的詳細資料，而非其餘的請購單清單。<!--- MC-39894-->

## B2B v1.3.0

*2020年10月15日*

[!BADGE 支援]{type=Informative tooltip="支援"} Adobe Commerce 2.4.0和更新版本

此版本包括訂單核准、送貨方法、購物車及管理員動作記錄等的改善。

![新](../assets/new.svg)已新增對Adobe Commerce 2.4.1的支援。

已增強![新](../assets/new.svg) B2B訂單核准，以改進可用性並允許對採購單執行大量動作。

![新](../assets/new.svg) B2B商家現在可以控制提供給每個公司的送貨方法。<!--- BUNDLE-160 161 162 -->

![新](../assets/new.svg)商家現在可以允許使用者透過單一動作清除其購物車的內容，並且可以在每個網站<!--- BUNDLE-108 -->上獨立設定此功能

![新](../assets/new.svg) B2B購買者現在可以將個別專案或其購物車的全部內容直接新增到請購單清單。<!--- BUNDLE-145 144-->

![新](../assets/new.svg) B2B商家可使用帳戶付款作為付款方式，代表客戶從管理員建立訂單。<!--- BUNDLE-166 178-->

![新](../assets/new.svg)商家現在可以從客戶的詳細資料頁面直接檢視與使用者相關的所有報價單。<!--- BUNDLE-139 -->

![新](../assets/new.svg)商戶現在可以依公司篩選「立即線上客戶」方格。<!--- BUNDLE-137 -->

![新](../assets/new.svg)管理員現在可以依銷售代表在管理員中篩選客戶。<!--- BUNDLE-110 -->

![新](../assets/new.svg)為了減少建立詐騙或垃圾郵件帳戶，商家現在可以在店面的新公司申請表上啟用Google reCAPTCHA。<!--- BUNDLE-154 -->

![在公司模組中執行的新的](../assets/new.svg)管理員動作現在已記錄在[管理員動作]記錄檔中。 從所有相關公司模組記錄動作： `Company`、`NegotiableQuote`、`CompanyCredit`、`SharedCatalog`。<!--- BUNDLE-180 181 182 183 -->

![已修正問題](../assets/fix.svg)登入的系統管理員無權刪除安裝B2B的部署中的客戶時，Adobe Commerce不再於&#x200B;**客戶**&#x200B;頁面上顯示&#x200B;**[!UICONTROL Delete customer]**&#x200B;按鈕。<!--- MC-35655-->

![已修正問題](../assets/fix.svg)當您在「客戶」方格上編輯客戶時，不再自動變更指派給公司的客戶的客戶群組。<!--- MC-35254-->

![已修正問題](../assets/fix.svg)當商家建立共用目錄時，當客戶群組在目錄許可權設定中被指派此存取權時，類別中&#x200B;**[!UICONTROL Display Product Prices]**&#x200B;和&#x200B;**[!UICONTROL Add to Cart]**&#x200B;功能的許可權現在會自動設定為`Allow`。 以前，即使將目錄許可權設為`Allow`.<!--- MC-34792-->，這些設定也會自動設為`Deny`

![修正問題](../assets/fix.svg)從產品編輯頁面編輯產品時，共用目錄類別許可權不再覆寫。<!--- MC-34777-->

![已修正問題](../assets/fix.svg) Adobe Commerce現在會傳送電子郵件通知，確認當商家啟用&#x200B;**[!UICONTROL Allow To Exceed Credit Limit]**&#x200B;設定時，客戶有權超過指定的信用額度。 以往，Adobe Commerce傳送的通知電子郵件指出客戶沒有許可權超過限制。<!--- MC-34584-->

![已修正問題](../assets/fix.svg)請購單清單上產品價格周圍的HTML容器，現在已針對套裝產品的子項正確轉譯。<!--- MC-36331-->

![已修正問題](../assets/fix.svg)商戶現在可以指定在多語言部署中建立公司時，傳送公司使用者電子郵件的語言。 以前，商家可以使用的下拉式功能表選取適當的商店檢視和語言，但系統不會顯示。 <!--- MC-35777-->

![已修正問題](../assets/fix.svg)自訂客戶地址屬性欄位現在會如預期般顯示在店面結帳工作流程中。<!--- MC-35607-->

![已修正問題](../assets/fix.svg) B2B功能設定索引標籤現在可正確開啟。 <!--- MC-35458-->來賓現在可以使用QuickOrder將產品加入購物車，然後成功移除專案。 先前，當購物者使用QuickOrder將多個產品新增至購物車，然後移除產品時，產品未移除。<!--- MC-35327-->

![已修正問題](../assets/fix.svg)現在可以使用REST API PUT `/V1/company/:companyId`請求更新公司，而不需在狀態設定為&#x200B;**不需要**&#x200B;時指定`region_id`。 以前，即使不需要`region_id`，如果未指定，Adobe Commerce也會擲回錯誤。<!--- MC-35304-->

![已修正問題](../assets/fix.svg)當您使用REST API （`http://magento.local/rest/V1/company/2`，其中`2`代表公司ID）建立或更新B2B公司時，回應現在會依預期包含`applicable_payment_method`或`available_payment_methods`的設定。<!--- MC-35248-->

![已修正問題](../assets/fix.svg)當商家在店面建立請購單清單時，使用&#x200B;**Enter**&#x200B;按鈕而非按一下&#x200B;**[!UICONTROL Save]**&#x200B;按鈕時，Adobe Commerce不再顯示404頁面。<!--- MC-35094-->

![已修正問題](../assets/fix.svg)將新產品指派給公用共用目錄時，類別許可權不再變更。 之前，類別許可權是重複的。<!--- MC-34386-->

![已修正問題](../assets/fix.svg)用於更新公司電子郵件的REST API端點PUT `rest/default/V1/company/{id}`不再區分大小寫。<!--- MC-34308-->

![已修正問題](../assets/fix.svg)停用獎勵模組不再影響客戶帳戶上的B2B功能。 先前停用獎勵模組時，系統不會顯示下列B2B相關標籤：公司設定檔、公司使用者、角色和許可權。<!--- MC-34191-->

![已修正問題](../assets/fix.svg) Adobe Commerce現在會在公司帳戶變更時，在電子郵件通知上使用正確的寄件者名稱。 之前，Adobe Commerce使用所有電子郵件預設範圍中定義的一般聯絡人寄件者名稱。<!--- MC-33917-->

![已修正問題](../assets/fix.svg)您現在可以針對同時包含實體與虛擬產品的訂單，成功實作多重送貨。<!--- MC-33818-->

![已修正問題](../assets/fix.svg)商戶現在可以從[我的帳戶]和[公司結構]頁面的&#x200B;_[!UICONTROL Company Users]_&#x200B;區段建立公司使用者，當&#x200B;**[!UICONTROL Access Restriction]**&#x200B;已啟用，**[!UICONTROL Restriction Mode]**&#x200B;設定為`Sales: Login Only`時。 之前，當商家嘗試建立使用者時，Adobe Commerce擲回此錯誤： `Can not register new customer due to restrictions are enabled`。<!--- MC-33608-->

![已修正問題](../assets/fix.svg)當客戶儲存其帳戶資訊時，Adobe Commerce不再將客戶的客戶群組重設為預設值。<!--- MC-33554-->

![已修正問題](../assets/fix.svg)管理員將擁有有效購物車的客戶指派給客戶群組時，Adobe Commerce不再擲回嚴重錯誤。<!--- MC-33313-->

![已修正問題](../assets/fix.svg) Adobe Commerce現在為快速訂購和請購單清單頁面提供`addToCart`個DataLayer事件。 <!--- MC-33295-->

![已修正問題](../assets/fix.svg)傳送給指派給公司的銷售代表的通知電子郵件現在包含指派的公司標誌。 以前，通知電子郵件包含預設的LUMA標誌，而不是上傳的企業標誌。<!--- MC-33232-->

![已修正問題](../assets/fix.svg)請購單清單現在包含已新增至清單的所有群組產品和數量。 先前，當商家從產品詳細資料頁面將產品新增到請購單清單後，Adobe Commerce會顯示此錯誤： `1 product(s) require your attention - Options were updated. Please review available configurations`。<!--- MC-32877-->

![已修正問題](../assets/fix.svg)啟用共用目錄時，`products`查詢現在會傳回正確的`total_count`欄位。<!--- MC-42268-->

![已修正問題](../assets/fix.svg)在您停用線上送貨方法後，「公司設定」和「建立公司」頁面現在會如預期般運作。 已新增驗證，以防止嘗試處理停用的送貨模組。 Adobe Commerce之前會顯示此錯誤： `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`。<!--- MC-43178-->

![已修正問題](../assets/fix.svg)整合測試記憶體耗用已減少，這可以改善測試效能，並減少完成測試所需的時間。<!--- AC-266-->

## B2B v1.2.0

*2020年7月28日*

[!BADGE 支援]{type=Informative tooltip="支援"} Adobe Commerce 2.4.0和更新版本

![新](../assets/new.svg)已新增對Adobe Commerce 2.4.0的支援。

![新](../assets/new.svg)店面訂單搜尋，並加上Marek Mularczyk的謝意，感謝他來自[Divante](https://www.divante.com/)和社群成員的貢獻。

![新的](../assets/new.svg)採購單已增強並重寫。 現在，預設情況下會包含在Adobe Commerce中。

已實作![新](../assets/new.svg)採購單核准規則。 這些規則可讓使用者藉由建立訂單的採購規則來控制「採購單」工作流程。

Adobe Commerce現在預設包含![新的](../assets/new.svg)客戶登入。 此功能可讓網站員工透過以客戶身分登入來協助客戶檢視他們看到的內容。

![已修正問題](../assets/fix.svg)屬性彙總現在可正確使用Elasticsearch的階層導覽

![已修正問題](../assets/fix.svg)依特殊字元搜尋訂單的功能現已正常運作。

![已修正問題](../assets/fix.svg)現在按一下「**[!UICONTROL Clear All]**」按鈕會展開所有篩選器，而非將其收合。

![已修正的問題](../assets/fix.svg)產品SKU/名稱現已納入「訂單歷史記錄」搜尋篩選條件摘要中。

![已修正問題](../assets/fix.svg)排序指標現在已正確顯示在「我的採購單格線」中。

![已修正問題](../assets/fix.svg)現在，您只能按一下[核准]、[取消]、[拒絕]和[採購單]按鈕一次。 之前，您可以按一下按鈕多次。

![已修正問題](../assets/fix.svg)在行動裝置上，採購單核准、拒絕、取消和驗證按鈕現在可正確呈現。

![修正問題](../assets/fix.svg)之前，核准已過期折扣的採購單時，會將訂單全額記入且未更新採購單總計。 現在，採購單總計會更新以顯示正確的總計。

![已修正問題](../assets/fix.svg) 2.3.4中引進了一個問題，其中自訂擴充功能屬性不會從客戶地址複製到報價地址。 此問題已修正。

![已修正問題](../assets/fix.svg)安裝B2B後，將類別指派給共用目錄時出現SQL錯誤。 此問題已修正。

![已修正問題](../assets/fix.svg)由於不正確的變數型別值，管理員無法將可設定的產品新增至訂單。 選項下拉式清單不會填入。 此功能現在已正常運作。

![已修正問題](../assets/fix.svg)先前，編輯「未登入」群組的類別許可權時，儲存變更時發生錯誤。 此問題已修正。

![已修正問題](../assets/fix.svg)已新增修正，以允許商店管理員將產品新增至不在共用目錄中的訂單。 以前，新增不在目錄中的專案時，會出現錯誤訊息。

![已修正問題](../assets/fix.svg) [!BADGE 僅限PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"}先前，執行命令`php bin/magento indexer:set-dimensions-mode catalog_product_price website`然後嘗試建立共用目錄之後，會發生錯誤。 此問題已修正。

![已修正問題](../assets/fix.svg)新增公司並將公司管理員指派至非預設網站時，所傳送的網站識別碼錯誤，導致發生錯誤。 此問題已修正。

![已修正問題](../assets/fix.svg)先前，將客戶移至其他客戶群組後，使用&#x200B;_快速訂單_&#x200B;新增產品至訂單會失敗，並出現錯誤。 此問題已修正。

![已修正問題](../assets/fix.svg)先前，嘗試使用WebAPI搭配B2B引號結帳時，傳送不正確的值至API，而造成發生錯誤。 此問題已修正。

![已修正問題](../assets/fix.svg)先前，透過API將公司設定為「作用中」時，會發生錯誤。 此問題現已修正。

![已修正問題](../assets/fix.svg)由於不必要的`form`標籤，當您在變更提議的運費後按下Enter鍵時，訂單頁面會自動重新整理。 此問題已修正。

![已修正問題](../assets/fix.svg)先前，在目錄頁面上設定產品顯示限制，且該限制小於產品總數時，會發生錯誤。 此功能現在可如預期運作。

![已修正問題](../assets/fix.svg)之前，變更公司的管理員時，會將原始的管理員地址複製到新的管理員，並為他們提供兩個地址。 現在，只會新增正確的地址。

![已修正問題](../assets/fix.svg)先前，當Git設為「允許並通知客戶」時，使用API儲存報價專案會失敗。 此API呼叫現在可如預期般運作。

![已修正問題](../assets/fix.svg)已修正產品稅現在會顯示在「報價詳細資料」頁面上。

![已修正問題](../assets/fix.svg)之前，在[我的報價]頁面的[評論]索引標籤中按一下附件，將無法下載檔案。 此行為現在會如預期般運作。

### 已知問題

- 在多網站部署中，Adobe Commerce在升級至B2B 1.2.0期間擲回例外狀況。 當`setup:upgrade`執行時，`PurchaseOrder`模組上會發生此錯誤： `Module Magento_PurchaseOrder: Unable to apply data patch Magento\PurchaseOrder\Setup\Patch\Data\InitPurchaseOrderSalesSequence for moduleMagento_PurchaseOrder`。 **因應措施**：將`B2B-716 Add NonTransactionableInterface`介面安裝到`InitPurchaseOrderSalesSequence`資料修補程式Hotfix，現在可從`magento.com`的&#x200B;**我的帳戶** > **下載**&#x200B;區段取得。
- 如果折扣代碼在核准採購單(PO)之前過期，則PO會繼續顯示折扣金額，但是一旦核准了PO，訂單就會以非折扣總計下單。 **因應措施**：安裝此問題的`B2B-709 Purchase Order Discount patch` Hotfix，您現在可從`magento.com`的&#x200B;**我的帳戶** > **下載**&#x200B;區段取得此修正程式。
- 如果採購單中的料號無庫存，或採購單轉換為實際訂單時數量不足，則會發生錯誤。 如果啟用延期交貨，則會正常處理訂單。
