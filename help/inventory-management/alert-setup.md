---
title: 產品警示
description: 瞭解產品警示以及如何使用警示來通知客戶產品的庫存狀態和價格變更。
exl-id: c9f736c5-7bba-4e3e-804d-5b0fe52c8f9b
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 0%

---

# 產品警示

客戶可以透過電子郵件訂閱兩種型別的警報：價格變更警報和庫存警報。 對於每種型別的警報，您可以確定客戶是否能夠訂閱、選擇使用的電子郵件範本，並識別電子郵件的寄件者。

![註冊產品警示](assets/product-alert-setting.png){width="600" zoomable="yes"}

## 價格變更警示

啟用價格變更警示時， _價格下降時通知我_ 連結會出現在每個產品頁面上。 客戶可以按一下連結，訂閱與產品相關的警示。 系統會提示訪客在您的商店中開立帳戶。 每當價格變動或產品推出特殊優惠時，訂閱該警示的每個人都會收到電子郵件警示。

## 庫存警報

庫存內警報會建立名為的連結 _此產品有庫存時通知我_ 所有無存貨的產品均適用。 客戶可按一下連結以訂閱警報。 當產品補充庫存時，客戶會收到該產品可用的電子郵件通知。 具有警示的產品具有 _產品警示_ 標籤中列出的客戶，這些客戶會訂閱警示。

![產品和價格警示訂閱清單](assets/inventory-product-alerts.png){width="600" zoomable="yes"}

## 設定產品警示

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Catalog]** 並選擇 **[!UICONTROL Catalog]** 底下。

1. 按一下以展開 _[!UICONTROL Product Alerts]_並執行下列動作：

   ![產品警示](assets/config-catalog-product-alerts.png){width="600" zoomable="yes"}

   - 若要向客戶提供價格變更警示，請設定 **[!UICONTROL Allow Alert When Product Price Changes]** 至 `Yes`.

   - 設定 **[!UICONTROL Price Alert Email Template]** 至您要用於價格警示通知的範本。

   - 若要在缺貨產品再次可用時提供警報，請設定 **[!UICONTROL Allow Alert When Product Comes Back in Stock]** 至 `Yes`.

     >[!NOTE]
     >
     >此 _此產品有庫存時通知我_ 訊息只會在 **[!UICONTROL Display Out of Stock Products]** 設為 `Yes` (在「 」設定中， [!UICONTROL Catalog] > [!UICONTROL Inventory])。

   - 設定 **[!UICONTROL Stock Alert Email Template]** 至您要用於產品庫存警示的範本。

   - 設定 **[!UICONTROL Alert Email Sender]** 至 [商店聯絡人](../getting-started/store-details.md#store-email-addresses){target="_blank"} that you want to appear as the sender of the email alert. Learn more about [store email addresses](../configuration-reference/general/store-email-addresses.md){target="_blank"} （在核心使用手冊中）。

1. 完成後，按一下 **[!UICONTROL Save Config]**.

## 設定產品警報電子郵件範本

接下來，設定、新增或修改價格警示的電子郵件範本。 建立其他範本後，您可能會想要編輯價格警示設定。

如需有關使用電子郵件訊息的詳細資訊，請參閱 [訊息範本](../systems/email-template-custom.md#message-templates) 在 _Admin System指南_.

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. 按一下 **[!UICONTROL Add New Template]**.

1. 在 _載入預設範本_，選擇 **[!UICONTROL Template]** 您想要自訂的專案。

   您可以選擇主題中包含的警報範本。 或者，您可以選取 `Price Alert` 或 `Stock Alert` 範本在 _[!UICONTROL Magento_PriceAlert]_.

1. 按一下 **[!UICONTROL Load Template]**.

1. 輸入 **[!UICONTROL Template Name]**.

   您可在 _價格警示_ 設定。

1. 閱讀現有內容，並視需要進行下列變更：

   | 欄位 | 說明 |
   | ----- | ----- |
   | [!UICONTROL Template Subject] | 此文字會顯示在電子郵件的主旨行中。 |
   | [!UICONTROL Template Content] | 此文字會顯示在已傳送電子郵件的完整內容中。 |

1. 新增產生的資訊： [!DNL Commerce] 資料，使用 **[!UICONTROL Insert Variable]** 選項來使用可用變數清單。

1. 按一下 **[!UICONTROL Save Template]**.

## 產品警示執行設定

這些設定可讓您選取頻率 [!DNL Commerce] 檢查需要傳送警示的變更。 您也可以選取在傳送警示失敗時傳送之電子郵件的收件者、寄件者和範本。

![產品警示執行設定](assets/config-catalog-product-alerts-run-settings.png){width="600" zoomable="yes"}

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Catalog]** 並選擇 **[!UICONTROL Catalog]** 底下。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Product Alerts Run Settings]** 區段。

1. 若要判斷產品警報的傳送頻率，請設定 **[!UICONTROL Frequency]** 變更為下列其中一項：

   - `Daily`
   - `Weekly`
   - `Monthly`

1. 若要判斷傳送產品警報的當天時間，請設定 **[!UICONTROL Start Time]** 到小時、分鐘和秒。

   >[!NOTE]
   >
   >產品警報會由「product_alert」消費者傳送。

1. 的 **[!UICONTROL Error Email Recipient]**，輸入發生錯誤時要聯絡之人員的電子郵件。

1. 對於 **[!UICONTROL Error Email Sender]**，選取顯示為錯誤通知寄件者的存放區身分。

1. 設定 **[!UICONTROL Error Email Template]** 至用於錯誤通知的交易式電子郵件範本。

1. 完成後，按一下 **[!UICONTROL Save Config]**.
