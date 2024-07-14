---
title: ' [!DNL Page Builder]的發行說明'
description: 檢閱發行說明，瞭解所有 [!DNL Page Builder] 發行版本的相關資訊。
exl-id: 81abe2f9-ed48-49fe-bbf0-70699d7106b2
feature: Page Builder, Release Notes
source-git-commit: addc34aeb4418aa3a1a9c2fc3adca738352ef94f
workflow-type: tm+mt
source-wordcount: '2813'
ht-degree: 0%

---

# [!DNL Page Builder]的發行說明

這些發行說明說明[!DNL Page Builder]的發行版本，包括：

![新](../assets/new.svg)新功能

![已修正問題](../assets/fix.svg)修正和改良

![已知問題](../assets/bug.svg)已知問題

>[!IMPORTANT]
>
>從2.4.3版開始，[!DNL Page Builder]現在可作為Magento Open Source中的套件擴充功能使用。 它現在是Adobe Commerce和Magento Open Source的預設內容編輯工具，並可取代任何協力廠商模組的WYSIWG編輯器。

## 適用於Commerce 2.4.5的1.7.2

![新](../assets/new.svg) **新包裝函式實體 — 為資料行配置引入的[!DNL Columns]容器** — 以前，使用者只能在其他容器/包裝函式內容型別（例如[!DNL Tab]或[!DNL Row]）中新增資料行。 現在，[!DNL Column]有自己的包裝函式，可以直接新增到舞台上。 此外，[!DNL Columns]容器具有設定元素，使用者可以在其中指定此包裝函式實體的組態。<!--- PB-500-->

![新增](../assets/new.svg) **新功能表選項，可複製、隱藏及刪除資料行群組** — 有了這些新選項，使用者可以複製、隱藏及刪除[!DNL Columns]個群組，就像他們可以使用內容型別一樣。<!--- PB-507-->

![新](../assets/new.svg) <!-- Issue 594 -->**新增多行資料行支援至[資料行]群組** — 有了這項新增，使用者可以在一個[!DNL Columns]群組內操控多行資料行，讓資料行配置更加靈活。<!--- PB-108-->

如需使用新[!DNL Columns]群組的相關資訊，請參閱[配置 — 欄](./column.md)。

## 適用於Commerce 2.4.4的1.7.1

![已修正問題](../assets/fix.svg)頁面產生器現在與PHP 8.1相容。<!--- AC-1300-->

![已修正問題](../assets/fix.svg)商戶現在可以將替代文字(`alt_text`)新增至影像（影像、橫幅、幻燈片），以提升內容可存取性。<!--- PB-1193-->

![修正問題](../assets/fix.svg)許可權限製為「內容」編輯的管理員使用者，在使用「頁面產生器」將產品Widget新增至CMS頁面時，不會再看到錯誤。 頁面產生器也會在Widget設定頁面上顯示準確的產品計數。 先前，頁面產生器在擷取產品計數時需要「目錄」模組的許可權，且會顯示此錯誤： `A technical problem with the server created an error. Try again to continue what you were doing. If the problem persists, try again later`。<!--- MC-42779-->

![已修正問題](../assets/fix.svg)頁面產生器格式功能表的顯示問題，現已透過TinyMCE 5程式庫升級解決。<!--- AC-446-->

![已修正問題](../assets/fix.svg)您現在可以使用滑鼠編輯[插入連結]快顯視窗中的&#x200B;**要顯示的文字**&#x200B;值。<!--- AC-982-->

![已修正問題](../assets/fix.svg)頁面產生器現在會依預期在[字型大小選項]功能表上顯示所有選項。 先前並未顯示所有選項。<!--- AC-1056-->

![已修正問題](../assets/fix.svg)已將`magento/magento2-page-builder`擴充功能的`phpgt/dom` Composer相依性升級至最新版本。<!--- magento/magento2-page-builder/pull/779-->

![修正問題](../assets/fix.svg)當在小欄中顯示滑桿時，頁面產生器不再調整「插入連結」和「插入影像」對話方塊的大小。<!--- AC-973-->

![已修正問題](../assets/fix.svg)頁面產生器表格屬性功能表現在會如預期般顯示。<!--- AC-407-->

![已修正問題](../assets/fix.svg)當滑鼠沒有暫留在滑鼠上時，「插入」連結或影像強制回應視窗中就不會再顯示滑桿點。<!--- AC-406-->

![已修正問題](../assets/fix.svg)用於顯示[表格]功能表選項的字型大小已最佳化。<!--- AC-396-->

![已修正問題](../assets/fix.svg)已修正「插入/編輯影像」和「插入/編輯連結」對話方塊位置的異常。<!--- AC-397-->

![已修正問題](../assets/fix.svg)當您按一下橫幅的&#x200B;**文字編輯器**&#x200B;時，頁面產生器不會再擲回錯誤。<!--- AC-398-->

![已修正問題](../assets/fix.svg)頁面產生器在升級期間不再將所有動態區塊轉換為單一語言。<!--- MC-42265-->

## 適用於Adobe Commerce 2.4.2的1.6.0

![新](../assets/new.svg) <!-- Issue 558 -->**新[!DNL Page Builder]樣式** - [!DNL Page Builder]大幅改善其內容樣式。 變更現在可讓您輕鬆建立簡單的CSS選取器以覆寫現有的內容型別樣式。 這些變更可讓您為所有內容型別建立回應速度豐富的[!DNL Page Builder]個主題。

![新的](../assets/new.svg) <!-- Issue 429 -->**資料列容器現在為選用** — 您現在可以在[!DNL Page Builder]中建立內容，而不需要資料列容器。 除了「列」以外，現在可以直接在舞台上拖放下列內容型別：HTML、區塊、動態區塊、欄和索引標籤。

![新](../assets/new.svg) <!-- Issue 636 -->**新回應式檢視區切換器** — 您現在可以使用舞台上方的新管理檢視區切換器按鈕，以不同的裝置寬度（中斷點）預覽[!DNL Page Builder]內容。 檢視區切換器會模擬您的內容使用不同裝置顯示在店面時的樣式設定方式。

![新的](../assets/new.svg) <!-- Issue 637 -->**新的中斷點特定表單欄位** — 內容型別欄位值現在可以設定為特定的檢視區中斷點。 欄位旁的圖示指示器會顯示套用內容型別欄位值的檢視區。

![新增](../assets/new.svg) <!-- Issue 559 -->**已移除預先定義的表單欄位專案** — 邊界、內邊距及邊界相關屬性（邊框、邊框寬度和邊框半徑）的進階表單設定現在設為`default`，因此值可由模組的CSS定義。

![新增](../assets/new.svg) <!-- Issue 635, 557,  -->**新增的舞台間距** — 列和欄現在可在舞台上所包含的內容型別周圍提供額外的間距，但不在店面上。 額外的舞台間距可讓您更輕鬆地存取容器和所包含內容型別的滑鼠懸停選項選單。

![已修正問題](../assets/fix.svg) <!-- MC-37348 -->**已修正自動捲動到商品評論** — 已修正自動捲動到店面上的產品評論。

![已修正問題](../assets/fix.svg) <!-- MC-36227 -->**已修正裁切的內容** — 不再裁切冗長的類別和產品說明。

![已修正問題](../assets/fix.svg) <!-- MC-35402 -->**已修正完整寬度、完整出血的類別內容** — 類別內容現在可以完整寬度或完整出血版面配置顯示。

![已修正問題](../assets/fix.svg) <!-- MC-37989 -->**安全性增強功能**

## Adobe Commerce 2.4.1-p1適用的1.5.1

![修正問題](../assets/fix.svg) <!-- PB-1140, MC-38812 -->**錯誤顯示** — 修正在Admin中新增目錄子類別時，[!DNL Page Builder]顯示錯誤的問題。

## 適用於Adobe Commerce 2.4.1的1.5.0

![新增](../assets/new.svg) <!-- Issue 510, 511, 512, 513 -->**沈浸式全熒幕編輯** — 編輯[!DNL Page Builder]內容現在只針對[!DNL Page Builder]控制的所有區域使用全熒幕功能。 此變更包括CMS頁面、產品和類別頁面、區塊和動態區塊。 全熒幕編輯將焦點放在您的內容上，並提供更符合店面使用者體驗的檢視。

![新的](../assets/new.svg) <!-- Issue 544 -->**[!DNL Page Builder]內容預覽&#x200B;**— 依預設，[!DNL Page Builder]現在不只提供CMS頁面、區塊和動態區塊的內容預覽，也提供產品和類別頁面的內容預覽。 您可以使用新的[!DNL Page Builder]內容預覽設定，將此功能設定為「產品」和「類別」頁面的開啟或關閉，此設定可在存放區設定（位於「內容管理>進階內容工具」）中存取。

![新增](../assets/new.svg) <!-- Issue 543 -->**改善產品簡短說明的存取權** — 依照預設，產品簡短說明會顯示在較長的說明之前。 此變更會符合店面出現的順序，且無需捲動較長的說明內容即可存取簡短說明。

![新增](../assets/new.svg) <!-- Issue 419 -->**防止橫幅和投影片中出現巢狀連結** — 新增連結，以連至橫幅和投影片的內容和外部元素，建立未在店面顯示或行為不正確的巢狀連結。 若要解決此問題，無法再將連結新增至&#x200B;*訊息文字區域以及橫幅和幻燈片的連結屬性*。

![已修正問題](../assets/fix.svg) <!-- Issue 421 -->已修正在Tab專案上設定空白邊框半徑導致錯誤並破壞Tab專案內容的問題。

![已修正問題](../assets/fix.svg) <!-- Issue 422 -->已修正將某些條件組合新增至產品條件篩選器時，導致無法儲存產品表單的錯誤問題。

![修正問題](../assets/fix.svg) <!-- Issue 425 -->修正當無限回圈設定停用時，Slider內容型別未正確運作的問題。

![已修正問題](../assets/fix.svg) <!-- Issue 426 -->已修正最低廣告價格，使其現在可在[!DNL Page Builder]中運作。

![已修正問題](../assets/fix.svg) <!-- Issue 436 -->已修正Safari和IE 11中，無法將影像拖放至橫幅和投影片上傳區域的問題。

![已修正問題](../assets/fix.svg) <!-- Issue 525 -->已修正Firefox中Slider內容型別無回應的問題。

![已修正問題](../assets/fix.svg) <!-- Issue 567 -->已修正Widget設定在DOM中針對不同外觀建立錯誤選取器的問題。

![修正問題](../assets/fix.svg) <!-- Issue 609 -->修正標題工具列隱藏內容型別選項功能表的問題，此問題會阻礙存取表單和其他選項。

![已修正問題](../assets/fix.svg) <!-- Issue 612, 613 -->已修正切換全熒幕模式多次後，滑桿和使用視差圖背景的多列無法正確呈現的問題。

![修正問題](../assets/fix.svg) <!--MC-35220-->修正嘗試將內容從「標題」內容型別複製到「文字」內容型別時，無法儲存[!DNL Page Builder]的問題。

![已修正問題](../assets/fix.svg) <!-- MC-34620 -->已修正文字內容型別，以正確處理並儲存非拉丁文1字元。

![已修正問題](../assets/fix.svg) <!-- MC-34679 -->已修正導致Safari 13.1無法正確呈現小型檢視連線埠和行動熒幕之Luma主題網站功能表的[!DNL Page Builder] CSS樣式。

![已修正問題](../assets/fix.svg) <!-- MC-34848 -->已修正HTML內容型別，以在店面正確顯示內嵌的Widget，例如「Order by SKU」。

## 適用於Adobe Commerce 2.4.0的1.4.1-p1

![New](../assets/new.svg) <!-- PB-590 -->已升級至TinyMCE 4。 移除TinyMCE 3以提高安全性。

## 適用於Adobe Commerce 2.4.0的1.4.0

![新](../assets/new.svg) <!-- PB-494 -->已新增對PHP 7.4的支援。

![已修正問題](../assets/fix.svg) <!-- MC-31247 -->修正當條件設為價格時，產品內容型別未顯示可設定產品的問題。

![已修正問題](../assets/fix.svg) <!-- PB-179 -->已修正產品對齊方式設定，以僅定位產品容器本身，而非產品容器內容，例如產品名稱、價格、按鈕、影像和其他元素。

![已修正問題](../assets/fix.svg) <!-- MC-33556 -->效能改善。

![已修正問題](../assets/fix.svg)安全性增強功能。

## 適用於Adobe Commerce 2.3.6-p1的1.3.3-p1

![已修正問題](../assets/fix.svg)安全性增強功能。

## 適用於Adobe Commerce 2.3.6的1.3.3

![已修正問題](../assets/fix.svg) <!-- MC-32766 -->已修正文字內容型別，以正確儲存新增至html屬性的變數指示。

![已修正問題](../assets/fix.svg) <!-- MC-34590 -->已修正文字內容型別，以正確處理並儲存非拉丁文1字元。

![已修正問題](../assets/fix.svg) <!-- MC-34677 -->已修正導致Safari 13.1無法正確呈現小型檢視連線埠和行動熒幕之Luma主題網站功能表的[!DNL Page Builder] CSS樣式。

![已修正問題](../assets/fix.svg) <!-- MC-34846 -->已修正HTML內容型別，以在店面正確顯示內嵌的Widget，例如&#x200B;_Order by SKU_。

![已修正問題](../assets/fix.svg)修正使用者有時無法儲存內容型別表單的錯誤。 錯誤（「[!DNL Page Builder]」呈現了5秒而未釋放鎖定」）導致載入器圖示在嘗試儲存表單後無限期迴轉。

## 適用於Adobe Commerce 2.3.5-p2的1.3.2

![新的](../assets/new.svg)安全性增強功能。

## 適用於Adobe Commerce 2.3.5-p1的1.3.1

此版本的[!DNL Page Builder]只是Adobe Commerce 2.3.5-p1的版本編號更新。 1.3.0版中說明的所有功能也適用於此版本。

## 適用於Adobe Commerce 2.3.5的1.3.0

![新的](../assets/new.svg) **範本** - [!DNL Page Builder]現在具有可從現有內容建立並套用至新內容區域的範本。 [!DNL Page Builder]範本會儲存現有頁面、區塊、動態區塊、產品屬性和類別說明的內容和版面配置。 例如，您可以將現有的[!DNL Page Builder] CMS頁面儲存為範本，然後套用該範本（包括其所有內容和版面）來快速建立您網站的CMS頁面。 此新功能記錄在此處： [範本](templates.md)。

![新的](../assets/new.svg) **列、橫幅和滑桿的**&#x200B;視訊背景 — [!DNL Page Builder]列、橫幅和滑桿現在可以使用視訊作為其背景。 這些新功能記錄在這裡： [列](row.md)、[橫幅](banner.md)、[滑桿](slider.md)。

![新的](../assets/new.svg) **視訊支援新增與增強功能** - [!DNL Page Builder]現在支援更多視訊格式。 除了YouTube和Vimeo視訊之外，視訊內容型別和視訊背景現在也支援視訊URL連結，可連結至`.mp4`等視訊格式和其他瀏覽器支援的格式。 視訊內容型別也新增了自動播放功能。 這些新功能記錄在此處： [視訊內容型別](video.md)。

![新的](../assets/new.svg) **全高度列、橫幅和滑桿** - [!DNL Page Builder]列、橫幅和滑桿現在可以使用具有任何CSS單位(px、%、vh、em)的數字，或單位之間的計算(100vh - 237px)，將其高度設定為頁面的全高度。 這些新功能記錄在這裡： [列](row.md)、[橫幅](banner.md)、[滑桿](slider.md)。

![新的](../assets/new.svg) **內容型別升級程式庫** — 開發人員現在可以建立[!DNL Page Builder]內容型別的版本，而不會在舊版中引入回溯不相容的問題。 在此版本之前，內容型別設定的重大變更將導致先前儲存的[!DNL Page Builder]內容型別出現顯示和資料遺失問題。 新的升級程式庫可消除這些問題。 程式庫的設計目的是升級儲存至資料庫的先前版本內容型別，以便符合新版本中的組態變更。 [!DNL Page Builder]會根據新發行版本的需求，在原生內容型別上執行升級程式庫。 此變更可確保內建[!DNL Page Builder]內容型別一律升級，以符合對較新發行版本的內容型別所做的任何變更。

>[!IMPORTANT]
>
>如果您已建立其他資料庫實體來儲存[!DNL Page Builder]內容，則&#x200B;_必須_&#x200B;將這些實體新增至`etc/di.xml`。 若未更新，則儲存在您實體中的[!DNL Page Builder]內容不會更新，這可能會導致資料遺失和顯示問題。 例如，如果您已建立儲存[!DNL Page Builder]內容的部落格實體，則必須將您的部落格實體新增至`etc/di.xml`檔案作為`UpgradableEntitiesPool`型別，以便升級程式庫可以更新您部落格中使用的[!DNL Page Builder]內容型別。 如需有關使用升級程式庫的詳細資訊與指示，請參閱&#x200B;_Page Builder開發人員指南_&#x200B;中的[升級內容型別](https://developer.adobe.com/commerce/frontend-core/page-builder/upgrade-content-types/)。

![新](../assets/new.svg) **新增外觀的檔案** — 現在已發佈關於[新增現有或自訂內容型別的外觀](https://developer.adobe.com/commerce/frontend-core/page-builder/content-types/extend/add-appearances/)的開發人員資訊。

![已修正問題](../assets/fix.svg) **各種修正**

- <!-- PB-50 -->修正投影片的父容器重複時，投影片內容的TinyMCE功能表會出現在其他內容型別下的問題。
- <!-- PB-166 -->更新[!DNL Page Builder]以實作destroy方法，以防止某些情況下發生記憶體遺失。
- <!-- PB-170 -->改善在管理階段使用多個執行個體時的TinyMCE效能。
- <!-- PB-252 -->修正當頂端列標示為隱藏時，Dynamic Block內容型別不會在Admin階段呈現的問題。
- <!-- PB-273 -->透過移除各種UI控制項的200毫秒延遲，改善「管理」階段的滑鼠懸停事件。 此變更可讓您更輕鬆地在「舞台」上處理巢狀內容專案。
- <!-- PB-294 -->修正管理階段中，區塊/動態區塊內的產品清單Widget中貨幣符號未正確逸出的問題。
- <!-- PB-296 -->修正[!DNL Page Builder]編輯面板上的產品總計不適用於自訂MSI Stock產品的問題。
- <!-- PB-317 -->修正在Microsoft Edge上儲存具有背景影像的[!DNL Page Builder]內容時，無法在店面中轉譯這些影像的問題。
- <!-- PB-390 -->修正使用者在頁面完全呈現之前按一下「儲存」按鈕時，巢狀[!DNL Page Builder]內容無法儲存的問題。
- <!-- PB-418 -->修正因[!DNL Page Builder]分析而引發cron作業中的例外狀況錯誤。

## 適用於Adobe Commerce 2.3.4-p2的1.2.2

![新的](../assets/new.svg)安全性增強功能。

## 適用於Adobe Commerce 2.3.4-p1的1.2.1

![新的](../assets/new.svg)安全性增強功能。

## 適用於Adobe Commerce 2.3.4的1.2.0

![新的](../assets/new.svg) **[!DNL Page Builder]與PWA Studio**&#x200B;整合 — 已將[!DNL Page Builder]內容轉譯新增至PWA Studio中的Venia應用程式。 現在可以在PWA StudioVenia應用程式中檢視[!DNL Page Builder]內容。 如需此新功能的所有資訊，請參閱[PWA Studio]中的[!DNL Page Builder]檔案。

![新增](../assets/new.svg) **已新增產品輪播** - <!-- PB-77, PB-173, PB-175 -->產品內容型別現在會提供以輪播/滑桿格式顯示產品的選項，包括根據您的需求自訂輪播的多個選項。

![新](../assets/new.svg) **已新增產品SKU排序** - <!-- PB-69 -->產品內容型別現在會提供選項，讓您依照SKU將產品新增至管理員清單的順序來排序產品。

![新](../assets/new.svg) **已新增產品類別排序** - <!-- PB-181 -->。 產品內容型別現在提供依類別&#x200B;_位置_&#x200B;來排序產品的選項，依照產品在Commerce目錄中的顯示順序來顯示。

![新增](../assets/new.svg) **已新增產品選擇總計** - <!-- PB-107 -->。 產品內容型別管理員編輯器現在會顯示符合您產品選擇選項的產品總數。

![已修正問題](../assets/fix.svg) **各種修正**

- <!-- PB-237 -->安全性增強功能。
- <!-- PB-41 -->修正UI中選取元件的搜尋，以讓每個搜尋詞僅產生一個AJAX請求。
- <!-- PB-76, PB-84-->更新管理員中的產品預覽，以符合店面，包括產品的星級評等、顏色和大小選項（如相關）。
- <!-- PB-169 -->修正在Commerce中啟用JavaScript縮制和套件組合時，無法儲存[!DNL Page Builder]的問題。
- <!-- PB-241 -->修正產品、區塊和動態區塊的管理員預覽功能，以在Commerce安裝上正確顯示，這些安裝為管理員和前端定義不同的URL。
- <!-- PB-238 -->修正產品、區塊和動態區塊的Admin預覽，以便在已安裝B2B並啟用&#x200B;_僅登入_&#x200B;選項的Commerce安裝上正確呈現。 在此修正之前，[!DNL Page Builder]預覽會使頁面重新導向至客戶帳戶登入。
- <!-- PB-239 -->修正預覽[!DNL Page Builder] Admin中的大型頁面時可能發生的工作階段錯誤。
- <!-- PB-248 -->更新[!DNL Page Builder] LESS樣式以防止店面樣式重複。

## Adobe Commerce 2.3.3-p1適用的1.1.1

![新的](../assets/new.svg)安全性增強功能。

## 適用於Adobe Commerce 2.3.3的1.1.0

![新](../assets/new.svg) <!-- MC-15250 -->已新增明確的產品排序至「產品」內容型別。

![新增](../assets/new.svg) <!-- MC-17823 -->新增在HTML內容型別中插入影像、Widget和變數的按鈕。

![已修正問題](../assets/fix.svg)已改善[!DNL Page Builder]安全性。

![已修正問題](../assets/fix.svg) <!-- MC-1805 -->已更新[!DNL Page Builder]以支援PHP 7.3版。

![已修正問題](../assets/fix.svg) <!-- MC-4137 -->已將TinyMCE更新至4.9.5版。此更新以及其他改善專案，修正了數個TinyMCE內嵌編輯器問題：

- 在游標所在的位置新增變數、影像和影像連結。
- 表格和表格儲存格可以置中對齊。
- 複製/貼上現在會將內容貼在游標位置。
- 連結可套用至選取的文字。
- 專案符號已正確對齊。
- 您不需要先按一下編輯器外部即可儲存內嵌編輯器中的變更。

![已修正問題](../assets/fix.svg) <!-- MC-3880 -->修正每個內容型別在編輯面板上各區段間的最小高度與垂直對齊不一致的問題。

![已修正問題](../assets/fix.svg) <!-- MC-14994 -->修正標題內容型別的工具列首次在舞台上放置時定位不正確的問題。

![已修正問題](../assets/fix.svg) <!-- MC-15742 -->已修正滑桿和視訊內容型別中的硬式編碼邊界。

![已修正問題](../assets/fix.svg) <!-- MC-16241 -->已修正表單欄位顯示兩次必要星號符號的問題。

## 適用於Adobe Commerce 2.3.2-p2的1.0.3

![新的](../assets/new.svg)安全性增強功能。

## Adobe Commerce 2.3.2-p1適用的1.0.2

![新的](../assets/new.svg)安全性增強功能。

## 適用於Adobe Commerce 2.3.2的1.0.1

![New](../assets/new.svg)確保與Adobe Commerce 2.3.2相容。

## 適用於Adobe Commerce 2.3.1的1.0.0

![新](../assets/new.svg)一般可用性版本


[PWA Studio]: https://developer.adobe.com/commerce/pwa-studio/
