---
title: 建立送貨標籤和封裝
description: 瞭解如何以訂單封裝專案並建立送貨標籤。
exl-id: ed9be72a-0dcd-4dbf-82ba-b1d75a1e76fd
feature: Shipping/Delivery, Orders
source-git-commit: cf57e136c7c3b6e8ba83afbbd539f4037c0ca486
workflow-type: tm+mt
source-wordcount: '1944'
ht-degree: 0%

---

# 建立出貨標籤

若要建立出貨標籤，您必須先設定出貨業者帳戶以支援標籤。 然後，按照提示輸入封裝及其內容的說明。

在您設定出貨標籤資訊並提交訂單後，Commerce會連線至出貨承運商系統、提交訂單，並接收出貨標籤和追蹤編號。 如果系統中存在此出貨的送貨標籤，則會以新標籤取代。 但是，不會取代現有的追蹤編號。 任何新追蹤編號都會新增至現有追蹤編號。

## 步驟1：連絡您的承運商

開始之前，請確定您的送貨帳戶已設定為處理標籤。 有些電信業者可能會收取額外費用，以便將運送標籤新增至您的帳戶。

請聯絡您用來啟用商店運送標籤的每家承運商。

按照各家電信業者提供的指示，為您的帳戶新增運送標籤支援。

- **FedEx** — 請連絡[FedEx Web Integration Services][1]，瞭解您帳戶的標籤列印需求。
- **USPS** — 請參閱託運人支援中心底下的[Web Tools API入口網站][4]，瞭解如何設定標籤列印認證。
- **UPS** — 請連絡[UPS][2]，確認您的帳戶支援運送標籤。 若要產生出貨標籤，您必須使用UPS XML選項。
- **DHL** — 請連絡[DHL電子商務解決方案][3]，瞭解您帳戶的標籤列印需求。

## 步驟2：更新每個電信業者的設定

1. 確定您的[存放區資訊](../getting-started/store-details.md#store-information)已完成。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Sales]**&#x200B;並選取&#x200B;**[!UICONTROL Shipping Settings]**。

1. 展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Origin]**&#x200B;區段並設定&#x200B;**[!UICONTROL Shipping Origin Address]**。

1. 請針對已啟動標籤列印的每個電信業者帳戶，依照下列指示操作。

### UPS設定

United Parcel Service在國內及國際皆有出貨。 不過，只能針對源自美國境內的出貨產生出貨標籤。

1. 在左側面板的&#x200B;_[!UICONTROL Sales]_區段中，選擇&#x200B;**[!UICONTROL Delivery Methods]**。

1. 展開![區段的](../assets/icon-display-expand.png)擴充選擇器&#x200B;**[!UICONTROL UPS]**。

1. 驗證您的UPS **[!UICONTROL Shipper Number]**&#x200B;是否正確。

   您的託運人號碼僅在啟用[!DNL United Parcel Service XML]時顯示。

1. 按一下&#x200B;**[!UICONTROL Save Config]**。

### USPS設定

[!DNL United States Postal Service]在國內和國際上出貨。

{{$include /help/_includes/usps-api-type-configuration-note.md}}

1. 繼續在&#x200B;**[!UICONTROL Delivery Methods]**&#x200B;設定中，展開![區段中的](../assets/icon-display-expand.png)擴充選擇器&#x200B;**[!UICONTROL USPS]**。

1. 選取&#x200B;**[!UICONTROL USPS Type]**&#x200B;作為`USPS Rest APIs`或`USPS Web Tools API`。

1. 驗證&#x200B;**[!UICONTROL Secure Gateway URL]**&#x200B;是否正確。

1. 輸入USPS提供給您的&#x200B;**[!UICONTROL Password]**。

1. 根據選取的&#x200B;**[!UICONTROL USPS Type]**，確認下列設定已完成：

   如果您使用USPS Web Tools API：
   - 使用者ID
   - 密碼

   如果您使用USPS REST API：
   - 使用者金鑰
   - 使用者密碼
   - 訂價選項
   - 帳戶型別
   - 帳號
   - 客戶註冊ID (CRID)
   - 郵件程式識別碼(MID)
   - 資訊清單MID
   - AES/ITN

1. 將&#x200B;**[!UICONTROL Size]**&#x200B;設為`Large`並輸入下列維度的值：

   - 長度
   - 寬度
   - 高度
   - 周長

1. 按一下&#x200B;**[!UICONTROL Save Config]**。

### FedEx設定

FedEx在國內和國際上銷售。 位於美國境外的商店只能建立適用於國際出貨的FedEx標籤。

1. 繼續在&#x200B;**[!UICONTROL Delivery Methods]**&#x200B;設定中，展開![區段中的](../assets/icon-display-expand.png)擴充選擇器&#x200B;**[!UICONTROL FedEx]**。

1. 確認下列FedEx認證是否正確：

   - 計量器編號
   - 索引鍵
   - 密碼

1. 按一下&#x200B;**[!UICONTROL Save Config]**。

### DHL設定

DHL提供國際運輸服務。

1. 繼續在&#x200B;**[!UICONTROL Delivery Methods]**&#x200B;設定中，展開![區段中的](../assets/icon-display-expand.png)擴充選擇器&#x200B;**[!UICONTROL DHL]**。

1. 驗證&#x200B;**[!UICONTROL Gateway URL]**&#x200B;是否正確。

1. 確認下列認證已完成：

   - 存取識別碼
   - 密碼
   - 帳號

1. 按一下&#x200B;**[!UICONTROL Save Config]**。

## 步驟3：建立出貨標籤

### 方法1：建立新出貨的標籤

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Sales]** > **[!UICONTROL Orders]**。

1. 在格線中尋找順序，並開啟記錄。

   訂單的狀態必須為`Pending`或`Processing`。

1. 按一下右上角的&#x200B;**[!UICONTROL Ship]**。

1. 根據承運商要求確認送貨資訊。

1. 在右下角，選取&#x200B;**[!UICONTROL Create Shipping Label]**&#x200B;核取方塊。

1. 按一下&#x200B;**[!UICONTROL Submit Shipment]**。

1. 新增或更新封裝中的產品：

   - 若要將訂單中的產品新增至封裝，請按一下&#x200B;**[!UICONTROL Add Products]**。 _[!UICONTROL Quantity]_欄顯示封裝可用的產品數目上限。

   - 選取要新增至封裝的每個產品核取方塊，然後輸入每個產品的&#x200B;**[!UICONTROL Quantity]**。 然後，按一下&#x200B;**[!UICONTROL Add Selected Product(s) to Package]**。

   - 若要新增封裝，請按一下&#x200B;**[!UICONTROL Add Package]**。

   - 若要刪除封裝，請按一下&#x200B;**[!UICONTROL Delete Package]**。

   - 若要取消訂單，請按一下&#x200B;**[!UICONTROL Cancel]**。 未建立送貨標籤，且&#x200B;_[!UICONTROL Create Shipping Label]_核取方塊已清除。

   >[!NOTE]
   >
   >如果您使用預設以外的封裝型別或需要簽名，則運費可能會與您向客戶收取的費用不同。 任何運費差異都不會反映在您的商店中。

1. 按一下&#x200B;**[!UICONTROL OK]**。

   Commerce會連線至出貨電信業者系統、提交訂單，並接收每個套件的出貨標籤和追蹤編號。

### 方法2：建立現有出貨的標籤

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**。

1. 在格線中尋找訂單，並開啟送貨表單。

1. 在&#x200B;_[!UICONTROL Shipping and Tracking Information]_區段中，按一下&#x200B;**[!UICONTROL Create Shipping Label]**。

1. 將訂購的產品分發到適當的封裝，然後按一下&#x200B;**[!UICONTROL OK]**。

1. 若要檢閱封裝資訊，請按一下&#x200B;**[!UICONTROL Show Packages]**。

## 步驟4：列印標籤

出貨標籤會以PDF格式產生，並可由管理員列印。 每個標籤都包含訂單編號和封裝編號。

>[!NOTE]
>
>因為已針對每個包裹建立個別出貨訂單，所以可能會針對單一出貨收到多個出貨標籤。

### 方法1：從出貨表單列印標籤

1. 在&#x200B;_管理員側邊欄_&#x200B;上，移至下列其中一個頁面，然後找到出貨記錄：

   - **[!UICONTROL Sales]** > **[!UICONTROL Orders]** — 在格線中尋找順序並開啟記錄。 在左側面板中選擇&#x200B;**[!UICONTROL Shipments]**。 然後，開啟出貨記錄。

   - **[!UICONTROL Sales]** > **[!UICONTROL Shipments]** — 在網格中尋找出貨並開啟記錄。

1. 若要下載PDF檔案，請移至表單的&#x200B;_[!UICONTROL Shipping and Tracking]_區段，然後按一下&#x200B;**[!UICONTROL Print Shipping Label]**。

   根據您的瀏覽器設定，可直接從PDF檔案檢視及列印運送標籤。

   _[!UICONTROL Print Shipping Label]_按鈕只有在承運商為出貨產生標籤之後才會出現。 如果按鈕遺失，請按一下&#x200B;**[!UICONTROL Create Shipping Label]**。 Commerce從電信業者收到標籤後，按鈕隨即顯示。

### 方法2：列印多份訂單的標籤

1. 在&#x200B;_管理員側邊欄_&#x200B;上，移至下列其中一個頁面，然後選取要列印的訂單或出貨：

   - **[!UICONTROL Sales]** > **[!UICONTROL Orders]** — 在格線中，選取每個要列印出貨標籤的訂單的核取方塊。

   - **[!UICONTROL Sales]** > **[!UICONTROL Shipments]** — 在格線中，選取每個要列印標籤的運送的核取方塊。

1. 將&#x200B;**[!UICONTROL Actions]**&#x200B;控制項設為`Print Shipping Labels`。

1. 按一下&#x200B;**[!UICONTROL Submit]**。

系統會針對與所選訂單相關的每筆出貨，列印完整的出貨標籤集。

## 必要的電信業者設定

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Type] | 封裝型別因電信業者和方法而異。 一開始會選取每個承運商的預設包裝型別。 USPS不需要國內出貨的套件型別。 |
| [!UICONTROL Customs Value] | （僅限國際出貨）國際出貨內容的宣告值或售價。 |
| [!UICONTROL Total Weight] | 系統會自動計算新增至封裝的所有產品總重量。 值也可以手動變更，並以磅或公斤輸入。 |
| [!UICONTROL Length, Width, Height] | （選用）套件維度僅用於自訂套件。 您可以將度量單位指定為英吋或公分。<br/><br/>**[!UICONTROL Not Required]**：運送業者未傳送任何交貨確認給商店。<br/><br/>**[!UICONTROL No Signature]**：未經過收件者簽章的傳遞確認由送貨業者傳送至商店。<br/><br/>**[!UICONTROL Signature Required]**：出貨承運商取得收件者的簽章，並提供商店的列印復本。<br/><br/>**[!UICONTROL Direct]**： （僅限FedEx） FedEx從位於傳遞地址的人取得簽章。 如果沒有人可簽收封裝，電信業者會在其他時間嘗試遞送封裝。<br/><br/>**[!UICONTROL Indirect]**： （僅限FedEx住宅傳遞） FedEx在傳遞位址取得某人（可能是鄰居或建築物管理員）的簽章。 收件者可留下已簽署的FedEx門標籤，以授權在沒有任何人出席的情況下留下套件以供簽署。<br/><br/>**[!UICONTROL Contents]**： （僅限USPS）選取下列其中一個封裝說明：<br/> — 贈品<br/> — 檔案<br/> — 商業範例<br/> — 退回的商品<br/> — 商品<br/> — 其他&#x200B;<br/><br/>**[!UICONTROL Explanation]**： （僅限USPS）封裝內容的詳細說明。<br/><br/>**[!UICONTROL Adult Required]**：運送公司取得成人收件者的簽章，並提供商店的列印復本。 |

{style="table-layout:auto"}

## 建立封裝

當您選擇建立送貨標籤時，_[!UICONTROL Create Packages]_視窗會出現。 您可以立即開始設定第一個封裝。

### 設定封裝

>[!NOTE]
>
>如果您選取[!UICONTROL Type]的非預設值，或選擇要求簽名確認，則出貨的價格可能會與您向客戶收取的價格不同。

1. 若要檢視已出貨的產品清單，並將它們新增至封裝，請按一下&#x200B;**[!UICONTROL Add Products]**。

   - 指定產品和數量。

     _[!UICONTROL Qty]_欄顯示可新增的最大數量。 對於第一個套件，數字是產品要出貨的總數量。

   - 若要將產品加入封裝，請按一下&#x200B;**[!UICONTROL Add Selected Product(s) to Package]**。

1. 若要新增封裝，請按一下&#x200B;**[!UICONTROL Add Package]**。

   您可以新增多個套裝軟體，並同時編輯它們。

1. 若要刪除封裝，請按一下&#x200B;**[!UICONTROL Delete Package]**。

將產品新增到封裝後，就無法直接編輯數量。

### 增加數量

1. 按一下&#x200B;**[!UICONTROL Add Selection]**。

1. 輸入額外數量。

   編號會新增至封裝中產品的先前數量。

### 減少數量

1. 從封裝中刪除產品。

1. 按一下&#x200B;**[!UICONTROL Add Selection]**。

1. 輸入新的較小值。

### 產生送貨標籤

分發所有產品後，您要使用的套件總數等於清單中最後一個套件的數量。 在所有已送出的專案都散發到套件並完成所有必要資訊之前，_確定_&#x200B;按鈕會停用。

若要產生標籤，請按一下&#x200B;**[!UICONTROL OK]**。

如有需要，您可以按一下&#x200B;**[!UICONTROL Cancel]**&#x200B;以停止處理程式。 未儲存封裝，且已取消送貨標籤程式。

### 欄位說明

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Type] | 指定套件的型別。 選取其中一個預先定義的值。 可用的封裝型別因各貨運業者而異。 當「建立封裝」彈出式視窗開啟時，出貨承運商的預設封裝會顯示在「型別」欄位中。 如果您選取並非由出貨承運商設計的封裝，則必須輸入封裝的尺寸。 對於為DHL、FedEx和UPS出貨建立的出貨標籤，「貨品型別」欄位設定為`Merchandise`。 對於USPS，欄位會反映&#x200B;_視窗中_&#x200B;內容&#x200B;_[!UICONTROL Create Packages]_欄位的值。 |
| [!UICONTROL Total Weight] | 套件的總重量。 此欄位已預先填入套件中產品的總重量。 測量單位可設為磅或公斤。 |
| [!UICONTROL Length] | 套件、整數和浮點數的長度。 如果使用自訂套件型別，則會啟用欄位。 測量單位可設為英吋或公分。 |
| [!UICONTROL Width] | 套件、整數和浮點數的寬度。 如果使用自訂套件型別，則會啟用欄位。 度量單位可以使用「高度」欄位旁的下拉式選單來指定；請選取介於英吋與公分之間。 |
| [!UICONTROL Height] | 套件、整數和浮點數的高度。 如果使用自訂套件型別，則會啟用欄位。 度量單位可以使用「高度」欄位旁的下拉式選單來指定；請選取介於英吋與公分之間。 |
| [!UICONTROL Signature] | 定義傳遞確認。 選項：<br/><br/>**[!UICONTROL Not Required]**：未傳送傳遞確認信函給您。<br/><br/>**[!UICONTROL No Signature]**：傳送不含收件者簽章的傳遞確認信函給您。<br/><br/>**[!UICONTROL Signature Required]**：出貨承運商取得收件者的簽章，並提供您其列印的復本。<br/><br/>**[!UICONTROL Adult Required]**：運送公司取得成人收件者的簽章，並提供您列印的復本。<br/><br/>**[!UICONTROL Direct (FedEx only)]**： FedEx從位於傳遞地址的人取得簽章，如果沒有人可簽署封裝，則重新嘗試傳遞。<br/><br/>**[!UICONTROL Indirect (FedEx only)]**： FedEx以三種方式之一取得簽章：<br/>(1)來自傳遞地址的人；<br/>(2)來自鄰居、大樓管理員或地址的其他人；或<br/>(3)收件者可以留下已簽署的FedEx Door標籤，授權在沒有任何人出席的情況下發行套件。 僅適用於住宅傳送。 選項可能因不同的送貨方法而略有不同。 如需最新資訊，請參閱運送業者的資源。 |
| [!UICONTROL Contents] | （僅適用於USPS出貨）包裝內容的說明。 選項： `Gift` / `Documents` / `Commercial Sample` / `Returned Goods` / `Merchandise` / `Other` |
| [!UICONTROL Explanation] | （僅限USPS出貨）封裝內容的詳細說明。 |

{style="table-layout:auto"}

[1]: https://www.fedex.com/en-us/api/get-support.html
[2]: https://www.ups.com/us/en/support/contact-us.page
[3]: https://www.dhl.com/us-en/home/our-divisions/ecommerce-solutions.html
[4]: https://www.usps.com/business/web-tools-apis/#ssc
