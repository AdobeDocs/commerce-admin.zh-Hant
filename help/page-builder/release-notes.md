---
title: 版本注意事項 [!DNL Page Builder]
description: 檢閱發行說明以瞭解全部資訊 [!DNL Page Builder] 發行版本。
exl-id: 81abe2f9-ed48-49fe-bbf0-70699d7106b2
feature: Page Builder, Release Notes
source-git-commit: addc34aeb4418aa3a1a9c2fc3adca738352ef94f
workflow-type: tm+mt
source-wordcount: '2747'
ht-degree: 0%

---

# 版本注意事項 [!DNL Page Builder]

以下發行說明說明說明以下版本： [!DNL Page Builder] 並包含：

![新增](../assets/new.svg) 新功能

![已修正的問題](../assets/fix.svg) 修正和改良

![已知問題](../assets/bug.svg) 已知問題

>[!IMPORTANT]
>
>從2.4.3版開始， [!DNL Page Builder] 現在可作為Magento Open Source中的套件擴充功能使用。 它現在是Adobe Commerce和Magento Open Source的預設內容編輯工具，並可取代任何協力廠商模組的WYSIWG編輯器。

## Commerce 2.4.5適用的1.7.2

![新增](../assets/new.svg) **新包裝函式實體 —  [!DNL Columns] 為欄佈局引入的容器**  — 以往，使用者只能在另一個容器/包裝函式內容型別中新增欄，例如 [!DNL Tab] 或 [!DNL Row]. 現在， [!DNL Column] 有專屬的包裝函式，可直接新增至stage。 此外， [!DNL Columns] 容器有設定元素，使用者可在其中指定此包裝函式實體的組態。<!--- PB-500-->

![新增](../assets/new.svg) **新功能表選項可複製、隱藏及刪除欄群組**  — 透過這些新選項，使用者可以複製、隱藏和刪除 [!DNL Columns] 群組 — 就像使用內容型別一樣。<!--- PB-507-->

![新增](../assets/new.svg) <!-- Issue 594 -->**新增多行欄支援至欄群組**  — 透過新增此功能，使用者可以操控一個欄內的多行欄 [!DNL Columns] 群組，協助讓欄位配置更具彈性。<!--- PB-108-->

另請參閱 [版面 — 欄](./column.md) 以取得有關使用新的 [!DNL Columns] 群組。

## Commerce 2.4.4適用的1.7.1

![已修正的問題](../assets/fix.svg) 頁面產生器現在相容於PHP 8.1。<!--- AC-1300-->

![已修正的問題](../assets/fix.svg) 商戶現在可以新增替代文字(`alt_text`)至影像（影像、橫幅、幻燈片）以提升內容可存取性。<!--- PB-1193-->

![已修正的問題](../assets/fix.svg) 管理員使用者許可權受限於「僅內容編輯」，當使用「頁面產生器」將產品Widget新增至CMS頁面時，不會再看到錯誤。 頁面產生器也會在Widget設定頁面上顯示準確的產品計數。 以前，頁面產生器在擷取產品計數並顯示此錯誤時，需要目錄模組的許可權： `A technical problem with the server created an error. Try again to continue what you were doing. If the problem persists, try again later`. <!--- MC-42779-->

![已修正的問題](../assets/fix.svg) 頁面產生器格式功能表的顯示問題，現在已透過TinyMCE 5程式庫升級解決。 <!--- AC-446-->

![已修正的問題](../assets/fix.svg) 您現在可以使用滑鼠編輯 **要顯示的文字** 插入連結快顯視窗中的值。 <!--- AC-982-->

![已修正的問題](../assets/fix.svg) 頁面產生器現在會依預期在「字型大小」選項功能表上顯示所有選項。 先前並未顯示所有選項。 <!--- AC-1056-->

![已修正的問題](../assets/fix.svg) 已升級 `phpgt/dom` 的編輯器相依性 `magento/magento2-page-builder` 延伸至最新版本。 <!--- magento/magento2-page-builder/pull/779-->

![已修正的問題](../assets/fix.svg) 在小欄中顯示滑桿時，頁面產生器不再調整插入連結和插入影像對話方塊的大小。 <!--- AC-973-->

![已修正的問題](../assets/fix.svg) 頁面產生器的「表格屬性」功能表現在會如預期般顯示。 <!--- AC-407-->

![已修正的問題](../assets/fix.svg) 當滑鼠沒有停留在滑杆上時，滑桿點不再顯示在「插入」連結或影像強制回應視窗上。 <!--- AC-406-->

![已修正的問題](../assets/fix.svg) 已最佳化用來顯示「表格」功能表選項的字型大小。 <!--- AC-396-->

![已修正的問題](../assets/fix.svg) 修正「插入/編輯影像」和「插入/編輯連結」對話方塊位置的異常。 <!--- AC-397-->

![已修正的問題](../assets/fix.svg) 按一下時，頁面產生器不會再擲回錯誤 **文字編輯器** 用於橫幅。 <!--- AC-398-->

![已修正的問題](../assets/fix.svg) 在升級期間，頁面產生器不再將所有動態區塊轉換為單一語言。 <!--- MC-42265-->

## 適用於Adobe Commerce 2.4.2的1.6.0

![新增](../assets/new.svg) <!-- Issue 558 -->**新增 [!DNL Page Builder] 樣式** - [!DNL Page Builder] 大幅改善內容樣式。 變更現在可讓您輕鬆建立簡單的CSS選取器以覆寫現有的內容型別樣式。 這些變更可讓您建立 [!DNL Page Builder] 所有內容型別都具備豐富回應能力的主題。

![新增](../assets/new.svg) <!-- Issue 429 -->**列容器現在為選用**  — 您現在可以在以下位置建立內容： [!DNL Page Builder] 而不需要Row容器。 除了「列」以外，現在可以直接在舞台上拖放下列內容型別：HTML、區塊、動態區塊、欄和索引標籤。

![新增](../assets/new.svg) <!-- Issue 636 -->**新的回應式檢視區切換器**  — 您現在可以預覽 [!DNL Page Builder] 使用舞台上方新「管理員檢視區」切換器按鈕的不同裝置寬度（中斷點）內容。 檢視區切換器會模擬您的內容使用不同裝置顯示在店面時的樣式設定方式。

![新增](../assets/new.svg) <!-- Issue 637 -->**新的中斷點特定表單欄位**  — 內容型別欄位值現在可以設定為特定的檢視區中斷點。 欄位旁的圖示指示器會顯示套用內容型別欄位值的檢視區。

![新增](../assets/new.svg) <!-- Issue 559 -->**已移除預先定義的表單欄位專案**  — 邊界、內邊距和邊框相關屬性（邊框、邊框寬度和邊框半徑）的進階表單設定現在設為 `default`，讓模組的CSS可定義值。

![新增](../assets/new.svg) <!-- Issue 635, 557,  -->**新增舞台間距**  — 列和欄現在會針對舞台上的包含內容型別（但不針對店面）提供額外的間距裕量。 額外的舞台間距可讓您更輕鬆地存取容器和所包含內容型別的滑鼠懸停選項選單。

![已修正的問題](../assets/fix.svg) <!-- MC-37348 -->**修正自動捲動至評論的問題**  — 現已修正自動捲動至店面上的產品評論功能。

![已修正的問題](../assets/fix.svg) <!-- MC-36227 -->**已修正裁切的內容**  — 不再裁切冗長的類別和產品說明。

![已修正的問題](../assets/fix.svg) <!-- MC-35402 -->**固定完整寬度、完整出血的類別內容**  — 類別內容現在可以全寬度或全出血版面配置顯示。

![已修正的問題](../assets/fix.svg) <!-- MC-37989 -->**安全性增強功能**

## Adobe Commerce 2.4.1-p1適用的1.5.1

![已修正的問題](../assets/fix.svg) <!-- PB-1140, MC-38812 -->**錯誤顯示**  — 修正以下問題 [!DNL Page Builder] 在管理員中新增目錄子類別時顯示錯誤。

## 適用於Adobe Commerce 2.4.1的1.5.0

![新增](../assets/new.svg) <!-- Issue 510, 511, 512, 513 -->**沈浸式全熒幕編輯**  — 編輯 [!DNL Page Builder] 現在，只有由控制的所有區域才可使用全熒幕內容 [!DNL Page Builder]. 此變更包括CMS頁面、產品和類別頁面、區塊和動態區塊。 全熒幕編輯將焦點放在您的內容上，並提供更符合店面使用者體驗的檢視。

![新增](../assets/new.svg) <!-- Issue 544 -->**[!DNL Page Builder] 內容預覽&#x200B;**— 根據預設， [!DNL Page Builder] 現在不僅為CMS頁面、區塊和動態區塊提供內容預覽，同時也為產品和類別頁面提供內容預覽。 您可以使用新的，將此功能設定為針對產品和類別頁面開啟或關閉 [!DNL Page Builder] 內容預覽設定，可從存放區設定（位於「內容管理>進階內容工具」）存取。

![新增](../assets/new.svg) <!-- Issue 543 -->**改善對產品簡短說明的存取**  — 根據預設，產品簡短說明會顯示在較長的說明之前。 此變更會符合店面出現的順序，且無需捲動較長的說明內容即可存取簡短說明。

![新增](../assets/new.svg) <!-- Issue 419 -->**橫幅和投影片中的巢狀連結**  — 將連結新增至內容以及橫幅和投影片的外部元素，會建立巢狀連結，而這些連結在店面無法正確顯示或運作。 若要解決此問題，無法再將連結新增至 *兩者* 「訊息文字」區域和「橫幅與投影片」的「連結」屬性。

![已修正的問題](../assets/fix.svg) <!-- Issue 421 --> 修正在索引標籤專案上設定空白邊框半徑導致錯誤和索引標籤專案內容中斷的問題。

![已修正的問題](../assets/fix.svg) <!-- Issue 422 --> 修正將某些條件組合新增至產品條件篩選器時，造成無法儲存產品表單的錯誤問題。

![已修正的問題](../assets/fix.svg) <!-- Issue 425 -->修正停用「無限回圈」設定時，Slider內容型別無法正確運作的問題。

![已修正的問題](../assets/fix.svg) <!-- Issue 426 -->已修正最低廣告價格，使其現在可在以下位置運作： [!DNL Page Builder].

![已修正的問題](../assets/fix.svg) <!-- Issue 436 -->修正Safari和IE 11中，無法將影像拖放至橫幅和投影片上傳區域的問題。

![已修正的問題](../assets/fix.svg) <!-- Issue 525 -->修正Firefox中Slider內容型別無回應的問題。

![已修正的問題](../assets/fix.svg) <!-- Issue 567 -->修正Widget設定在DOM中針對不同外觀建立錯誤選取器的問題。

![已修正的問題](../assets/fix.svg) <!-- Issue 609 -->修正標題工具列隱藏內容型別選項功能表，而無法存取表單和其他選項的問題。

![已修正的問題](../assets/fix.svg) <!-- Issue 612, 613 -->修正滑桿和使用視差背景的多列在切換全熒幕模式多次後無法正確呈現的問題。

![已修正的問題](../assets/fix.svg) <!--MC-35220-->修正嘗試將內容從標題內容型別複製到文字內容型別時遭阻止的問題 [!DNL Page Builder] 儲存。

![已修正的問題](../assets/fix.svg) <!-- MC-34620 -->修正文字內容型別，以正確處理和儲存非拉丁文–1字元。

![已修正的問題](../assets/fix.svg) <!-- MC-34679 -->固定 [!DNL Page Builder] 導致Safari 13.1無法正確針對小型檢視連線埠和行動熒幕呈現Luma主題的網站功能表的CSS樣式。

![已修正的問題](../assets/fix.svg) <!-- MC-34848 -->修正HTML內容型別，以在店面正確顯示內嵌Widget，例如「Order by SKU」。

## 適用於Adobe Commerce 2.4.0的1.4.1-p1

![新增](../assets/new.svg) <!-- PB-590 --> 升級至TinyMCE 4。 移除TinyMCE 3以提高安全性。

## 適用於Adobe Commerce 2.4.0的1.4.0

![新增](../assets/new.svg) <!-- PB-494 -->新增對PHP 7.4的支援。

![已修正的問題](../assets/fix.svg) <!-- MC-31247 -->修正當條件設為價格時， Products內容型別未顯示可設定產品的問題。

![已修正的問題](../assets/fix.svg) <!-- PB-179 -->修正產品對齊方式設定，僅放置產品容器本身，而非產品容器內容，例如產品名稱、價格、按鈕、影像和其他元素。

![已修正的問題](../assets/fix.svg) <!-- MC-33556 -->效能提升。

![已修正的問題](../assets/fix.svg) 安全性增強功能。

## 適用於Adobe Commerce 2.3.6-p1的1.3.3-p1

![已修正的問題](../assets/fix.svg) 安全性增強功能。

## 適用於Adobe Commerce 2.3.6的1.3.3

![已修正的問題](../assets/fix.svg) <!-- MC-32766 -->修正文字內容型別，以正確儲存新增至html屬性的變數指示。

![已修正的問題](../assets/fix.svg) <!-- MC-34590 -->修正文字內容型別，以正確處理和儲存非拉丁文–1字元。

![已修正的問題](../assets/fix.svg) <!-- MC-34677 -->固定 [!DNL Page Builder] 導致Safari 13.1無法正確針對小型檢視連線埠和行動熒幕呈現Luma主題的網站功能表的CSS樣式。

![已修正的問題](../assets/fix.svg) <!-- MC-34846 -->修正HTML內容型別，以正確顯示內嵌Widget，例如 _依SKU排序_ 在店面。

![已修正的問題](../assets/fix.svg) 修正使用者有時無法儲存內容型別表單的錯誤。 錯誤(&quot;[!DNL Page Builder] 」的狀況持續呈現5秒鐘，但未解除鎖定)，導致載入器圖示在嘗試儲存表單後無限期迴轉。

## 適用於Adobe Commerce 2.3.5-p2的1.3.2

![新增](../assets/new.svg) 安全性增強功能。

## 適用於Adobe Commerce 2.3.5-p1的1.3.1

此版本的 [!DNL Page Builder] 只是Adobe Commerce 2.3.5-p1的版本編號更新。 1.3.0版中說明的所有功能也適用於此版本。

## 適用於Adobe Commerce 2.3.5的1.3.0

![新增](../assets/new.svg) **範本** - [!DNL Page Builder] 現在已有可從現有內容建立並套用至新內容區域的範本。 [!DNL Page Builder] 範本會儲存現有頁面、區塊、動態區塊、產品屬性和類別說明的內容和版面。 例如，您可以儲存現有的 [!DNL Page Builder] CMS頁面作為範本，然後套用該範本（包括其所有內容和版面）以快速建立您網站的CMS頁面。 此新功能記錄在此處： [範本](templates.md).

![新增](../assets/new.svg) **列、橫幅和滑塊的視訊背景** - [!DNL Page Builder] 列、橫幅和滑桿現在可以使用視訊作為其背景。 以下新功能記錄在此處： [列](row.md)， [橫幅](banner.md)， [滑桿](slider.md).

![新增](../assets/new.svg) **視訊支援新增和增強功能** - [!DNL Page Builder] 現在支援更多視訊格式。 除了YouTube和Vimeo視訊之外，視訊內容型別和視訊背景現在也支援視訊URL連結，以連結視訊格式，例如 `.mp4` 和其他瀏覽器支援的格式。 視訊內容型別也新增了自動播放功能。 以下新功能記錄在此處： [視訊內容型別](video.md).

![新增](../assets/new.svg) **全高度列、橫幅和滑桿** - [!DNL Page Builder] 列、橫幅和滑桿現在可以使用具有任何CSS單位(px、%、vh、em)的數字或單位之間的計算(100vh - 237px)，將其高度設定為頁面的完整高度。 以下新功能記錄在此處： [列](row.md)， [橫幅](banner.md)， [滑桿](slider.md).

![新增](../assets/new.svg) **內容型別升級程式庫**  — 開發人員現在可以建立 [!DNL Page Builder] 內容型別，避免先前版本出現回溯不相容的問題。 在此版本之前，內容型別設定的重大變更會導致先前儲存的顯示和資料遺失問題 [!DNL Page Builder] 內容型別。 新的升級程式庫可消除這些問題。 程式庫的設計目的是升級儲存至資料庫的先前版本內容型別，以便符合新版本中的組態變更。 [!DNL Page Builder] 視新發行版本的需求，針對原生內容型別執行升級程式庫。 此變更可確保內建的 [!DNL Page Builder] 內容型別一律會升級，以符合對較新版本內容型別所做的任何變更。

>[!IMPORTANT]
>
>如果您已建立其他資料庫實體來儲存 [!DNL Page Builder] 內容，您 _必須_ 將這些實體新增至 `etc/di.xml`. 否則， [!DNL Page Builder] 儲存在您實體中的內容未更新，這可能會導致資料遺失和顯示問題。 例如，如果您已建立儲存的部落格實體 [!DNL Page Builder] 內容，您必須將部落格實體新增至 `etc/di.xml` 檔案作為 `UpgradableEntitiesPool` 輸入，讓升級程式庫能夠更新 [!DNL Page Builder] 在您的部落格中使用的內容型別。 如需使用升級程式庫的詳細資訊與指示，請參閱 [升級內容型別](https://developer.adobe.com/commerce/frontend-core/page-builder/upgrade-content-types/) 在 _Page Builder開發人員指南_.

![新增](../assets/new.svg) **新增外觀的檔案**  — 開發人員資訊已發佈，關於 [新增外觀](https://developer.adobe.com/commerce/frontend-core/page-builder/content-types/extend/add-appearances/) 用於現有或自訂內容型別。

![已修正的問題](../assets/fix.svg) **各種修正**

- <!-- PB-50 -->修正投影片的父容器重複時，投影片內容的TinyMCE功能表會出現在其他內容型別下的問題。
- <!-- PB-166 -->已更新 [!DNL Page Builder] 實作destroy方法以防止某些情況下的記憶體流失。
- <!-- PB-170 -->改善在管理階段使用多個執行個體時的TinyMCE效能。
- <!-- PB-252 -->修正當頂端列標示為隱藏時，Dynamic Block內容型別不會在Admin階段呈現的問題。
- <!-- PB-273 -->透過移除各種UI控制項的200毫秒延遲，改善「管理」階段的滑鼠懸停事件。 此變更可讓您更輕鬆地在「舞台」上處理巢狀內容專案。
- <!-- PB-294 -->修正管理階段中，區塊/動態區塊內的產品清單Widget中貨幣符號未正確逸出的問題。
- <!-- PB-296 -->修正上的產品總計問題 [!DNL Page Builder] 編輯面板無法用於自訂MSI Stock產品。
- <!-- PB-317 -->修正儲存的問題 [!DNL Page Builder] 在Microsoft Edge上具有背景影像的內容不會在店面轉譯這些影像。
- <!-- PB-390 -->修正巢狀結構的問題 [!DNL Page Builder] 如果使用者在頁面完全呈現之前按一下「儲存」按鈕，內容就無法儲存。
- <!-- PB-418 -->修正cron作業中因下列原因而擲回的例外狀況錯誤： [!DNL Page Builder] 分析。

## 適用於Adobe Commerce 2.3.4-p2的1.2.2

![新增](../assets/new.svg) 安全性增強功能。

## 適用於Adobe Commerce 2.3.4-p1的1.2.1

![新增](../assets/new.svg) 安全性增強功能。

## 適用於Adobe Commerce 2.3.4的1.2.0

![新增](../assets/new.svg)  **[!DNL Page Builder]與PWA Studio整合**  — 已新增 [!DNL Page Builder] 內容呈現至PWA Studio中的Venia應用程式。 [!DNL Page Builder] 內容現在可在PWA StudioVenia應用程式中檢視。 請參閱 [!DNL Page Builder] 中的檔案 [PWA Studio] 以取得此新功能的所有資訊。

![新增](../assets/new.svg) **已新增產品輪播** - <!-- PB-77, PB-173, PB-175 -->「產品」內容型別現在提供以輪播/滑桿格式顯示產品的選項，包括根據您的需求自訂輪播的多個選項。

![新增](../assets/new.svg) **新增產品SKU排序** - <!-- PB-69 -->產品內容型別現在提供依SKU排序產品的選項，排序順序可讓您依照將產品新增至管理員清單中的順序。

![新增](../assets/new.svg) **已新增產品類別排序** - <!-- PB-181 -->. 產品內容型別現在提供依類別排序產品的選項 _position_，以它們在商務目錄中的顯示順序來顯示。

![新增](../assets/new.svg) **已新增產品選擇總計** - <!-- PB-107 -->. 產品內容型別管理員編輯器現在會顯示符合您產品選擇選項的產品總數。

![已修正的問題](../assets/fix.svg) **各種修正**

- <!-- PB-237 -->安全性增強功能。
- <!-- PB-41 -->修正UI中選取元件的搜尋，以讓每個搜尋詞僅產生一個AJAX請求。
- <!-- PB-76, PB-84-->更新管理員中的產品預覽，以符合店面，包括產品的星級評等、顏色和大小選項（如相關）。
- <!-- PB-169 -->修正以下問題 [!DNL Page Builder] 在Commerce中啟用JavaScript縮制和套件組合時，無法儲存。
- <!-- PB-241 -->修正產品、區塊和動態區塊的管理員預覽，以在Commerce安裝上正確呈現，這些安裝為管理員和前端定義不同的URL。
- <!-- PB-238 -->修正產品、區塊和動態區塊的Admin預覽，以便在搭配安裝B2B的Commerce上正確呈現 _僅登入_ 選項已啟用。 在此修正之前， [!DNL Page Builder] 預覽會導致頁面重新導向至客戶帳戶登入。
- <!-- PB-239 -->修正在預覽大型頁面時可能發生的工作階段錯誤 [!DNL Page Builder] 管理員。
- <!-- PB-248 -->已更新 [!DNL Page Builder] 較少的樣式，避免店面樣式重複。

## Adobe Commerce 2.3.3-p1適用的1.1.1

![新增](../assets/new.svg) 安全性增強功能。

## 適用於Adobe Commerce 2.3.3的1.1.0

![新增](../assets/new.svg) <!-- MC-15250 -->已將明確的產品排序新增至產品內容型別。

![新增](../assets/new.svg) <!-- MC-17823 -->新增在HTML內容型別中插入影像、Widget和變數的按鈕。

![已修正的問題](../assets/fix.svg) 已改善 [!DNL Page Builder] 安全性。

![已修正的問題](../assets/fix.svg) <!-- MC-1805 -->已更新 [!DNL Page Builder] 以支援PHP 7.3版。

![已修正的問題](../assets/fix.svg) <!-- MC-4137 -->將TinyMCE更新至4.9.5版。此更新以及其他改善專案，修正了數個TinyMCE內嵌編輯器問題：

- 在游標所在的位置新增變數、影像和影像連結。
- 表格和表格儲存格可以置中對齊。
- 複製/貼上現在會將內容貼在游標位置。
- 連結可套用至選取的文字。
- 專案符號已正確對齊。
- 您不需要先按一下編輯器外部即可儲存內嵌編輯器中的變更。

![已修正的問題](../assets/fix.svg) <!-- MC-3880 -->修正每個內容型別在編輯面板上的區段之間最低高度和垂直對齊不一致的問題。

![已修正的問題](../assets/fix.svg) <!-- MC-14994 -->修正首次在舞台上放置標題內容型別的工具列時，其位置不正確的問題。

![已修正的問題](../assets/fix.svg) <!-- MC-15742 -->修正Slider和Video內容型別中的硬式編碼邊界。

![已修正的問題](../assets/fix.svg) <!-- MC-16241 -->修正表單欄位顯示兩次所需星號符號的問題。

## 適用於Adobe Commerce 2.3.2-p2的1.0.3

![新增](../assets/new.svg) 安全性增強功能。

## Adobe Commerce 2.3.2-p1適用的1.0.2

![新增](../assets/new.svg) 安全性增強功能。

## 適用於Adobe Commerce 2.3.2的1.0.1

![新增](../assets/new.svg) 確保與Adobe Commerce 2.3.2相容。

## 適用於Adobe Commerce 2.3.1的1.0.0

![新增](../assets/new.svg) 正式發行版本


[PWA Studio]: https://developer.adobe.com/commerce/pwa-studio/
