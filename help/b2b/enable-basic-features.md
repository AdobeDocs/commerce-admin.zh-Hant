---
title: 啟用B2B功能
description: 瞭解如何為您的Adobe Commerce商店啟用B2B功能，包括公司帳戶、預設付款和送貨方法、採購單和訂單核准。
exl-id: aed203ef-f39b-4f7e-b32f-ded53eca09a8
feature: B2B, Configuration
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '1629'
ht-degree: 0%

---

# 啟用B2B功能

依預設，所有B2B功能一開始都會停用。 商店管理員可視需要啟用或停用Commerce商店的B2B功能。 如需B2B組態設定的完整清單，請參閱 [B2B功能組態參考](../configuration-reference/general/b2b-features.md).

啟用客戶公司支援時，系統會自動啟用其他B2B功能：

- [!DNL Shared Catalog]

  支援不同公司的自訂定價設定，也啟用所有商店的類別許可權。

- [!DNL Enable Shared Catalog direct products price assigning]

  在價格索引中僅儲存指派給共用目錄的產品，以提升網站效能。 如果商家有許多共用目錄，為了管理不同公司的自訂定價，啟用此功能是最佳做法。

- [!DNL B2B Quotes]

  讓賣家和公司買家能夠協商價格。

- [!DNL B2B default payment and shipping methods]

  決定店面B2B買家可用的付款與運送選項選項。

只有在下列情況下，這些功能的組態設定才可見 [!DNL Enable Company] 設為 `Yes`.

B2B [!DNL Quick Order] 和 [!DNL Requisition List] 功能可以獨立啟用和停用。

## 設定B2B功能

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

   如果您有多站台安裝，請設定 **[!UICONTROL Store View]** 控制項位於左上角，可前往套用設定的網站。

1. 在左側面板中的 _[!UICONTROL General]_，選擇&#x200B;**[!UICONTROL B2B Features]**：

   ![B2B設定 — 一般](./assets/b2b-features.png){width="600"}

   - 允許客戶管理自己的公司帳戶，並透過設定啟用對其他B2B功能的支援 **[!UICONTROL Enable Company]**  至 `Yes`.

     啟用公司支援時，會自動啟用「共用目錄」、「B2B報價」、「B2B付款方式」和「B2B出貨方式」。

   - 若要讓客戶和來賓能根據SKU或產品名稱快速下訂單，請設定 **[!UICONTROL Enable Quick Order]** 至 `Yes`.

   - 若要允許客戶從其帳戶儀表板建立和管理請購單清單，請設定 **[!UICONTROL Enable Requisition List]** 至 `Yes`.

     您也可以 [設定清單的最大數量](configure-requisition-lists.md) 客戶可以擁有其帳戶的。

1. 完成後，按一下 **[!UICONTROL Save Config]**.

## 設定預設B2B付款和送貨方法

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Default B2B Payment Methods]** 區段。

1. 若要建立B2B訂單的預設付款方式，請設定 **[!UICONTROL Applicable Payment Methods]** 變更為下列其中一項：

   - `All Payment Methods`

   - `Selected Payment Methods`

     針對特定選項，選取 **[!UICONTROL Payment Methods]** 當您按一下每個選項時，按住Ctrl鍵(PC)或Command鍵(Mac)即可讓客戶使用。

   清單 [付款方法](../configuration-reference/sales/payment-methods.md) 顯示目前商店中啟用或停用的選項。 除了標準付款方式之外，此清單還包括下列專案：

   - 不需要付款資訊
   - [分期付款](#configure-payment-on-account)
   - 已儲存的帳戶
   - 儲存的卡片

   ![B2B設定 — 預設付款方式設定](./assets/b2b-features-default-payment-methods.png){width="600"}

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Default B2B Shipping Methods]** 區段。

1. 若要指定B2B訂單的預設送貨方式，請設定 **[!UICONTROL Applicable Shipping Methods]** 變更為下列其中一項：

   - `All Shipping Methods`
   - `Selected Shipping Methods`

     針對特定選項，選取 **[!UICONTROL Shipping Methods]** 當您按一下每個選項時，按住Ctrl鍵(PC)或Command鍵(Mac)即可讓客戶使用。

     送貨方法清單顯示目前的 [啟用或停用](../configuration-reference/sales/delivery-methods.md).

   ![B2B設定 — 預設送貨方法](./assets/b2b-features-shipping-methods.png){width="600"}

1. 完成後，按一下 **[!UICONTROL Save Config]**.

## 設定公司電子郵件選項

此 [銷售代表](account-company-manage.md#assign-a-sales-representative) 根據預設，該帳戶會設定為公司的主要聯絡人，以作為許多傳送給公司的自動化電子郵件訊息的寄件者。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Customers]** 並選擇 **[!UICONTROL Company Configuration]**.

1. 如有必要，請設定 **[!UICONTROL Store View]** 至商店檢視以定義 [範圍](../getting-started/websites-stores-views.md#scope-settings) 設定的。

1. 完成 **[!UICONTROL Company Registration]** 區段：

   >[!NOTE]
   >
   >清除 **[!UICONTROL Use system value]** 核取方塊，讓欄位可編輯。

   - 設定 **[!UICONTROL Company Registration Email Recipient]** 至 [商店聯絡人](../getting-started/store-details.md#store-email-addresses) 當收到新的公司註冊要求時，會通知誰。

   - 的 **[!UICONTROL Send Company Registration Email Copy To]**，輸入每一位收到註冊通知副本的人的電子郵件地址。 請使用逗號分隔多個電子郵件地址。

   - 若要確定通知副本的傳送方式，請設定 **傳送電子郵件副本方法** 變更為下列其中一項：

      - `Bcc`  — 傳送 _盲文提供_ 在傳送給客戶的相同電子郵件的標題中包含收件者。 客戶看不到密件副本收件者。
      - `Separate Email`  — 以個別電子郵件的形式傳送副本。

   - 如果您已準備要使用的電子郵件範本，而非預設值，請設定 **[!UICONTROL Default Company Registration Email]** 至範本的名稱。 根據預設， `Company Registration Request` 範本已使用。

     ![客戶組態 — 公司註冊](./assets/company-email-options-company-registration.png){width="600"}

1. 完成 **[!UICONTROL Customer-Related Emails]** 區段：

   如果您已準備要使用的替代電子郵件範本而非預設值，請選擇您要在下列各專案中使用的範本：

   - **[!UICONTROL Default 'Sales Rep Assigned' Email]**
   - **[!UICONTROL Default 'Assign Company to Customer' Email]**
   - **[!UICONTROL Default 'Assign Company Admin' Email]**
   - **[!UICONTROL Default 'Company Admin Inactive' Email]**
   - **[!UICONTROL Default 'Company Admin Changed to Member' Email]**
   - **[!UICONTROL Default 'Customer Status Active' Email]**
   - **[!UICONTROL Default 'Customer Status Inactive' Email]**

   ![客戶設定 — 客戶相關電子郵件](./assets/company-email-options-customer-related-emails.png){width="600"}

1. 完成 **[!UICONTROL Company Status Change]** 區段：

   - 的 **[!UICONTROL Send Company Status Change Email Copy To]**，輸入每個要接收狀態變更通知副本之人員的電子郵件地址。 請使用逗號分隔多個電子郵件地址。

   - 若要確定通知副本的傳送方式，請設定 **傳送電子郵件副本方法** 變更為下列其中一項：

      - `Bcc`  — 傳送 _盲文提供_ 在傳送給客戶的相同電子郵件的標題中包含收件者。 客戶看不到密件副本收件者。
      - `Separate Email`  — 以個別電子郵件的形式傳送副本。

   - 如果您已準備電子郵件範本，公司狀態變更時會使用此範本 `Pending Approval` 至 `Active`，設定 **[!UICONTROL Default 'Company Status Change to Active 1' Email]** 至範本的名稱。 根據預設， `Company Status Active 1` 範本已使用。

   - 如果您已準備電子郵件範本，公司狀態變更時會使用此範本 `Rejected` 或 `Blocked` 至 `Active`，設定 **[!UICONTROL Default 'Company Status Change to Active 2' Email]** 至範本的名稱。 根據預設， `Company Status Active 2` 範本已使用。

   - 如果您已準備當公司狀態變更為時會使用的電子郵件範本 `Rejected`，設定 **[!UICONTROL Default 'Company Status Change to Rejected' Email]** 至範本的名稱。 根據預設， `Company Status Rejected` 範本已使用。

   - 如果您已準備當公司狀態變更為時會使用的電子郵件範本 `Blocked`，設定 **[!UICONTROL Default 'Company Status Change to Blocked' Email]** 至範本的名稱。 根據預設， `Company Status Blocked` 範本已使用。

   - 如果您已準備當公司狀態變更為時會使用的電子郵件範本 `Pending Approval`，設定 **[!UICONTROL Default 'Company Status Change to Pending Approval' Email]** 至範本的名稱。 根據預設， `Company Status Pending Approval` 範本已使用。

   ![客戶組態 — 公司狀態變更](./assets/company-email-options-company-status-change.png){width="600"}

1. 完成 **[!UICONTROL Company Credit Emails]** 區段：

   - 設定 **[!UICONTROL Company Credit Change Email Sender]** 至 [商店聯絡人](../getting-started/store-details.md#store-email-addresses) 當指定給公司的信用額度發生變更時，會通知誰。 依預設，通知會傳送至 _銷售代表_.

   - 的 **[!UICONTROL Send Company Credit Change Email Copy To]**，輸入每一位將收到信用變更通知復本之人員的電子郵件地址。 請使用逗號分隔多個電子郵件地址。

   - 若要確定通知副本的傳送方式，請設定 **傳送電子郵件副本方法** 變更為下列其中一項：

      - `Bcc`  — 傳送 _盲文提供_ 在傳送給客戶的相同電子郵件的標題中包含收件者。 客戶看不到密件副本收件者。
      - `Separate Email`  — 以個別電子郵件的形式傳送副本。

   - 如果您已準備要使用的電子郵件範本而非預設值，請為傳送給公司管理員的下列每個通知選擇範本。

      - **[!UICONTROL Allocated Email Template]**
      - **[!UICONTROL Updated Email Template]**
      - **[!UICONTROL Reimbursed Email Template]**
      - **[!UICONTROL Refunded Email Template]**
      - **[!UICONTROL Reverted Email Template]**

   ![客戶設定 — 公司信用電子郵件](./assets/company-email-options-company-credit.png){width="600"}

1. 完成後，按一下 **[!UICONTROL Save Config]**.

## 設定訂單核准

追蹤訂單處理與採購單的功能，可讓公司管理員控制公司買家的動作。 當商店管理員啟用採購單功能時，即可使用訂單核准功能。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL General]** 並選擇 **[!UICONTROL B2B Features]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Order Approval Configuration]** 區段。

   ![訂單核准設定](./assets/b2b-features-order-approval.png){width="600"}

1. 若要允許公司建立自己的採購單，請設定 **[!UICONTROL Enable Purchase Orders]** 至 `Yes`.

1. 完成後，按一下 **[!UICONTROL Save Config]**.

   採購單功能會在網站層級啟用。 若要為公司啟用此類訂單，請在每個訂單中使用適當的設定執行相同操作 [公司設定檔](account-company-manage.md).

## 設定採購單

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. 在清單中尋找公司並按一下 **[!UICONTROL Edit]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Advanced Settings]** 區段。

1. 設定 **[!UICONTROL Enable Purchase Orders]** 至 `Yes`.

1. 完成後，按一下 **[!UICONTROL Save]**.

啟用後， **[!UICONTROL Approval Rules]** 區段會顯示在店面 [帳戶儀表板](../customers/account-dashboard.md) 公司管理員。

>[!NOTE]
>
>店面上的採購單存取權必須由公司管理員根據下列條件授予 [公司使用者角色許可權](account-company-roles-permissions.md).

## 設定分期付款

「依帳戶付款」是一種離線付款方法，可讓公司以設定檔中指定的信用額度進行購買。 「帳戶付款」可全域啟用，或依公司啟用，並僅在啟用時於結帳期間顯示。 時間 _分期付款_ 付款方式時，會在訂單頂端顯示訊息，指出帳戶的狀態。 若要為特定公司設定此付款方式，請參閱 [管理公司帳戶](account-company-manage.md).

>[!NOTE]
>
>下列訂單不支援以帳戶付款： [多個送貨地址](../stores-purchase/shipping-settings.md#multiple-addresses) 而且不會出現在這些訂單的付款選項中。

若要啟用商店的「分期付款」，請執行下列步驟：

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Sales]** 並選擇 **[!UICONTROL Payment Methods]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Payment on Account]** 區段。

   ![分期付款](./assets/payment-methods-payment-on-account.png){width="600"}

   >[!NOTE]
   >
   >如有必要，請先取消選取 **[!UICONTROL Use system value]** 核取方塊以變更這些設定。

1. 若要允許分期付款，請設定 **[!UICONTROL Enabled]** 至 `Yes`.

1. 輸入 **[!UICONTROL Title]** 會在結帳時識別付款方式，或者您可以接受 `Payment on Account` 預設標題。

1. 如果訂單通常會等待核准，請接受預設值 **[!UICONTROL New Order Status]** 作為 `Pending` 直到獲得核准為止。

   您也可以使用 `Processing` 或 `Suspected Fraud` 使用此付款方式的新訂單狀態。

1. 設定 **[!UICONTROL Payment from Applicable Countries]** 變更為下列其中一項：

   - `All Allowed Countries`  — 來自所有客戶的客戶 [國家/地區](../getting-started/store-details.md#country-options) 在商店設定中指定的可使用此付款方式。
   - `Specific Countries`  — 選擇此選項後， _[!UICONTROL Payment from Specific Countries]_清單隨即顯示。 若要選取多個國家/地區，請按住Ctrl鍵(PC)或Command鍵(Mac)，然後按一下每個選項。

1. 設定 **[!UICONTROL Minimum Order Total]** 和 **[!UICONTROL Maximum Order Total]** 至符合此付款方式資格的訂單金額。

   >[!NOTE]
   >
   >如果總計介於最小或最大總計值之間，或完全符合，訂單即符合條件。

1. 輸入 **[!UICONTROL Sort Order]** 此編號會設定此專案在結帳時顯示的付款方式清單中的位置。

   該值與其他付款方式相關。 (`0` =第一個， `1` =秒， `2` =第三個，依此類推。)

1. 完成後，按一下 **[!UICONTROL Save Config]**.
