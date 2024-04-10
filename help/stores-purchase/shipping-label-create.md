---
title: 建立送貨標籤和封裝
description: 瞭解如何以訂單封裝專案並建立送貨標籤。
exl-id: ed9be72a-0dcd-4dbf-82ba-b1d75a1e76fd
feature: Shipping/Delivery, Orders
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '1889'
ht-degree: 0%

---

# 建立出貨標籤

若要建立出貨標籤，您必須先設定出貨業者帳戶以支援標籤。 然後，按照提示輸入封裝及其內容的說明。

在您設定出貨標籤資訊並提交訂單後，Commerce會連線至出貨承運商系統、提交訂單，並接收出貨標籤和追蹤編號。 如果系統中存在此出貨的送貨標籤，則會以新標籤取代。 但是，不會取代現有的追蹤編號。 任何新追蹤編號都會新增至現有追蹤編號。

## 步驟1：連絡您的承運商

開始之前，請確定您的送貨帳戶已設定為處理標籤。 有些電信業者可能會收取額外費用，以便將運送標籤新增至您的帳戶。

請聯絡您用來啟用商店運送標籤的每家承運商。

按照各家電信業者提供的指示，為您的帳戶新增運送標籤支援。

- **FedEx**  — 連絡人 [FedEx Web整合服務][1] 瞭解您帳戶的標籤列印需求。
- **USPS**  — 請參閱 [網站工具API入口網站][4] 位於託運人支援中心，瞭解如何設定標籤列印憑證。
- **UPS** — 連絡人 [UPS][2] 以確認您的帳戶支援運送標籤。 若要產生出貨標籤，您必須使用UPS XML選項。
- **DHL**  — 連絡人 [DHL電子商務解決方案][3] 瞭解您帳戶的標籤列印需求。

## 步驟2：更新每個電信業者的設定

1. 確定您的 [存放區資訊](../getting-started/store-details.md#store-information) 完成。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Sales]** 並選取 **[!UICONTROL Shipping Settings]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Origin]** 區段並設定 **[!UICONTROL Shipping Origin Address]**.

1. 請針對已啟動標籤列印的每個電信業者帳戶，依照下列指示操作。

### UPS設定

United Parcel Service在國內及國際皆有出貨。 不過，只能針對源自美國境內的出貨產生出貨標籤。

1. 在 _[!UICONTROL Sales]_區段，選擇&#x200B;**[!UICONTROL Delivery Methods]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL UPS]** 區段。

1. 確認您的UPS **[!UICONTROL Shipper Number]** 是正確的。

   您的託運人編號只會在以下情況出現： [!DNL United Parcel Service XML] 已啟用。

1. 按一下 **[!UICONTROL Save Config]**.

### USPS設定

此 [!DNL United States Postal Service] 不論在國內還是國際銷售。

1. 在中繼續 **[!UICONTROL Delivery Methods]** 設定，展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL USPS]** 區段。

1. 確認 **[!UICONTROL Secure Gateway URL]** 是正確的。

1. 輸入 **[!UICONTROL Password]** 由USPS提供。

1. 設定 **[!UICONTROL Size]** 至 `Large` 並輸入下列維度的值：

   - 長度
   - 寬度
   - 高度
   - 周長

1. 按一下 **[!UICONTROL Save Config]**.

### FedEx設定

FedEx在國內和國際上銷售。 位於美國境外的商店只能建立適用於國際出貨的FedEx標籤。

1. 在中繼續 **[!UICONTROL Delivery Methods]** 設定，展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL FedEx]** 區段。

1. 確認下列FedEx認證是否正確：

   - 計量器編號
   - 索引鍵
   - 密碼

1. 按一下 **[!UICONTROL Save Config]**.

### DHL設定

DHL提供國際運輸服務。

1. 在中繼續 **[!UICONTROL Delivery Methods]** 設定，展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL DHL]** 區段。

1. 確認 **[!UICONTROL Gateway URL]** 是正確的。

1. 確認下列認證已完成：

   - 存取識別碼
   - 密碼
   - 帳號

1. 按一下 **[!UICONTROL Save Config]**.

## 步驟3：建立出貨標籤

### 方法1：建立新出貨的標籤

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. 在格線中尋找順序，並開啟記錄。

   訂單的狀態必須為 `Pending` 或 `Processing`.

1. 在右上角，按一下 **[!UICONTROL Ship]**.

1. 根據承運商要求確認送貨資訊。

1. 在右下角，選取 **[!UICONTROL Create Shipping Label]** 核取方塊。

1. 按一下 **[!UICONTROL Submit Shipment]**.

1. 新增或更新封裝中的產品：

   - 若要將訂單中的產品新增至封裝，請按一下 **[!UICONTROL Add Products]**. 此 _[!UICONTROL Quantity]_欄會顯示封裝可用的產品數量上限。

   - 選取要新增至封裝的每個產品核取方塊，然後輸入 **[!UICONTROL Quantity]** 每個。 然後，按一下 **[!UICONTROL Add Selected Product(s) to Package]**.

   - 若要新增套件，請按一下 **[!UICONTROL Add Package]**.

   - 若要刪除套裝，請按一下 **[!UICONTROL Delete Package]**.

   - 若要取消訂單，請按一下 **[!UICONTROL Cancel]**. 未建立送貨標籤，而且 _[!UICONTROL Create Shipping Label]_核取方塊已清除。

   >[!NOTE]
   >
   >如果您使用預設以外的封裝型別或需要簽名，則運費可能會與您向客戶收取的費用不同。 任何運費差異都不會反映在您的商店中。

1. 按一下 **[!UICONTROL OK]**.

   Commerce會連線至出貨承運商系統、提交訂單，並接收每個套件的出貨標籤和追蹤編號。

### 方法2：建立現有出貨的標籤

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. 在格線中尋找訂單，並開啟送貨表單。

1. 在 _[!UICONTROL Shipping and Tracking Information]_區段，按一下&#x200B;**[!UICONTROL Create Shipping Label]**.

1. 將訂購的產品分發到適當的封裝，然後按一下 **[!UICONTROL OK]**.

1. 若要檢閱封裝資訊，請按一下 **[!UICONTROL Show Packages]**.

## 步驟4：列印標籤

出貨標籤會以PDF格式產生，並可由管理員列印。 每個標籤都包含訂單編號和封裝編號。

>[!NOTE]
>
>因為已針對每個包裹建立個別出貨訂單，所以可能會針對單一出貨收到多個出貨標籤。

### 方法1：從出貨表單列印標籤

1. 在 _管理員側邊欄_，前往下列其中一個頁面，然後找到出貨記錄：

   - **[!UICONTROL Sales]** > **[!UICONTROL Orders]**  — 在格線中尋找順序並開啟記錄。 在左側面板中，選擇 **[!UICONTROL Shipments]**. 然後，開啟出貨記錄。

   - **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**  — 在網格中尋找出貨並開啟記錄。

1. 若要下載PDF檔案，請前往 _[!UICONTROL Shipping and Tracking]_部分，然後按一下&#x200B;**[!UICONTROL Print Shipping Label]**.

   根據您的瀏覽器設定，可以直接從PDF檔案檢視和列印出貨標籤。

   此 _[!UICONTROL Print Shipping Label]_只有承運商產生出貨的標籤後，才會顯示按鈕。 如果按鈕遺失，請按一下&#x200B;**[!UICONTROL Create Shipping Label]**. 在Commerce收到來自電信業者的標籤後，按鈕會出現。

### 方法2：列印多份訂單的標籤

1. 在 _管理員側邊欄_，移至下列其中一個頁面，然後選取要列印的訂單或出貨：

   - **[!UICONTROL Sales]** > **[!UICONTROL Orders]**  — 在格線中，選取每個要列印出貨標籤的訂單的核取方塊。

   - **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**  — 在格線中，選取每個要列印標籤出貨的核取方塊。

1. 設定 **[!UICONTROL Actions]** 控制項至 `Print Shipping Labels`.

1. 按一下 **[!UICONTROL Submit]**.

系統會針對與所選訂單相關的每筆出貨，列印完整的出貨標籤集。

## 必要的電信業者設定

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Type] | 封裝型別因電信業者和方法而異。 一開始會選取每個承運商的預設包裝型別。 USPS不需要國內出貨的套件型別。 |
| [!UICONTROL Customs Value] | （僅限國際出貨）國際出貨內容的宣告值或售價。 |
| [!UICONTROL Total Weight] | 系統會自動計算新增至封裝的所有產品總重量。 值也可以手動變更，並以磅或公斤輸入。 |
| [!UICONTROL Length, Width, Height] | （選用）套件維度僅用於自訂套件。 您可以將度量單位指定為英吋或公分。<br/><br/>**[!UICONTROL Not Required]**：運送業者不會將任何傳遞確認傳送至商店。<br/><br/>**[!UICONTROL No Signature]**：傳送電信業者會將傳送確認給商店，但不含收件者的簽名。<br/><br/>**[!UICONTROL Signature Required]**：出貨承運商取得收件者的簽章，並向商店提供列印的復本。<br/><br/>**[!UICONTROL Direct]**：（僅限FedEx） FedEx會從傳送地址中的某人取得簽名。 如果沒有人可簽收封裝，電信業者會在其他時間嘗試遞送封裝。<br/><br/>**[!UICONTROL Indirect]**：（僅限FedEx住宅傳送） FedEx在傳送地址取得某人（可能是鄰居或建築物管理員）的簽名。 收件者可留下已簽署的FedEx門標籤，以授權在沒有任何人出席的情況下留下套件以供簽署。<br/><br/>**[!UICONTROL Contents]**：（僅限USPS）選取下列其中一個封裝說明：<br/> — 禮物<br/> — 檔案<br/> — 商業範例<br/> — 退回的商品<br/> — 商品<br/> — 其他&#x200B;<br/><br/>**[!UICONTROL Explanation]**：（僅限USPS）套件內容的詳細說明。<br/><br/>**[!UICONTROL Adult Required]**：運送業者取得成人收件者的簽名，並向商店提供列印的復本。 |

{style="table-layout:auto"}

## 建立封裝

此 _[!UICONTROL Create Packages]_當您選擇建立出貨標籤時，視窗會出現。 您可以立即開始設定第一個封裝。

### 設定封裝

>[!NOTE]
>
>如果您選取 [!UICONTROL Type] 或選擇要求簽名確認，出貨的價格可能會與您向客戶收取的價格不同。

1. 若要檢視已出貨的產品清單，並將它們新增至封裝，請按一下 **[!UICONTROL Add Products]**.

   - 指定產品和數量。

     此 _[!UICONTROL Qty]_欄顯示可新增的最大數量。 對於第一個套件，數字是產品要出貨的總數量。

   - 若要將產品新增至封裝，請按一下 **[!UICONTROL Add Selected Product(s) to Package]**.

1. 若要新增套件，請按一下 **[!UICONTROL Add Package]**.

   您可以新增多個套裝軟體，並同時編輯它們。

1. 若要刪除套裝，請按一下 **[!UICONTROL Delete Package]**.

將產品新增到封裝後，就無法直接編輯數量。

### 增加數量

1. 按一下 **[!UICONTROL Add Selection]**.

1. 輸入額外數量。

   編號會新增至封裝中產品的先前數量。

### 減少數量

1. 從封裝中刪除產品。

1. 按一下 **[!UICONTROL Add Selection]**.

1. 輸入新的較小值。

### 產生送貨標籤

分發所有產品後，您要使用的套件總數等於清單中最後一個套件的數量。 此 _確定_ 在將所有已出貨料號分配至封裝並完成所有必要資訊之前，按鈕會停用。

若要產生標籤，請按一下 **[!UICONTROL OK]**.

您可以按一下 **[!UICONTROL Cancel]** 以停止程式（如有需要）。 未儲存封裝，且已取消送貨標籤程式。

### 欄位說明

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Type] | 指定套件的型別。 選取其中一個預先定義的值。 可用的封裝型別因各貨運業者而異。 當「建立封裝」彈出式視窗開啟時，出貨承運商的預設封裝會顯示在「型別」欄位中。 如果您選取並非由出貨承運商設計的封裝，則必須輸入封裝的尺寸。 針對為DHL、FedEx和UPS出貨所建立的出貨標籤，「貨品型別」欄位會設為 `Merchandise`. 對於USPS，欄位會反映來自 _內容_ 中的欄位 _[!UICONTROL Create Packages]_視窗。 |
| [!UICONTROL Total Weight] | 套件的總重量。 此欄位已預先填入套件中產品的總重量。 測量單位可設為磅或公斤。 |
| [!UICONTROL Length] | 套件、整數和浮點數的長度。 如果使用自訂套件型別，則會啟用欄位。 測量單位可設為英吋或公分。 |
| [!UICONTROL Width] | 套件、整數和浮點數的寬度。 如果使用自訂套件型別，則會啟用欄位。 度量單位可以使用「高度」欄位旁的下拉式選單來指定；請選取介於英吋與公分之間。 |
| [!UICONTROL Height] | 套件、整數和浮點數的高度。 如果使用自訂套件型別，則會啟用欄位。 度量單位可以使用「高度」欄位旁的下拉式選單來指定；請選取介於英吋與公分之間。 |
| [!UICONTROL Signature] | 定義傳遞確認。 選項：<br/><br/>**[!UICONTROL Not Required]**：不會傳送任何傳遞確認信函給您。<br/><br/>**[!UICONTROL No Signature]**：傳送不含收件者簽名的傳遞確認信函給您。<br/><br/>**[!UICONTROL Signature Required]**：承運商取得收件者的簽章，並提供您其列印的復本。<br/><br/>**[!UICONTROL Adult Required]**：承運商取得成人收件者的簽章，並提供您其列印的復本。<br/><br/>**[!UICONTROL Direct (FedEx only)]**：FedEx會從位於傳遞地址的人取得簽章，如果沒有人可簽署封裝，則會重新嘗試傳遞。<br/><br/>**[!UICONTROL Indirect (FedEx only)]**：FedEx會透過下列三種方式之一取得簽章：<br/>(1)來自交貨地址的人； <br/>(2)來自鄰居、樓宇管理員或地址的其他人；或 <br/>(3)收件者可留下已簽署的FedEx Door標籤，授權在任何人不在場的情況下發行套件。 僅適用於住宅傳送。 選項可能因不同的送貨方法而略有不同。 如需最新資訊，請參閱運送業者的資源。 |
| [!UICONTROL Contents] | （僅適用於USPS出貨）包裝內容的說明。 選項： `Gift` / `Documents` / `Commercial Sample` / `Returned Goods` / `Merchandise` / `Other` |
| [!UICONTROL Explanation] | （僅限USPS出貨）封裝內容的詳細說明。 |

{style="table-layout:auto"}

[1]: https://www.fedex.com/en-us/api/get-support.html
[2]: https://www.ups.com/us/en/support/contact-us.page
[3]: https://www.dhl.com/us-en/home/our-divisions/ecommerce-solutions.html
[4]: https://www.usps.com/business/web-tools-apis/#ssc
