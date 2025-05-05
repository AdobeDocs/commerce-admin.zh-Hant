---
title: 產品警示
description: 瞭解產品警示以及如何使用警示來通知客戶產品的庫存狀態和價格變更。
exl-id: c9f736c5-7bba-4e3e-804d-5b0fe52c8f9b
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 0%

---

# 產品警示

客戶可以透過電子郵件訂閱兩種型別的警報：價格變更警報和庫存警報。 對於每種型別的警報，您可以確定客戶是否能夠訂閱、選擇使用的電子郵件範本，並識別電子郵件的寄件者。

![註冊產品警示](assets/product-alert-setting.png){width="600" zoomable="yes"}

## 價格變更警示

啟用價格變更警示時，每個產品頁面上都會顯示&#x200B;_價格下降時通知我_&#x200B;連結。 客戶可以按一下連結，訂閱與產品相關的警示。 系統會提示訪客在您的商店中開立帳戶。 每當價格變動或產品推出特殊優惠時，訂閱該警示的每個人都會收到電子郵件警示。

## 庫存警報

庫存警示會建立名為&#x200B;_當此產品有庫存_&#x200B;時通知我每個無庫存產品的連結。 客戶可按一下連結以訂閱警報。 當產品補充庫存時，客戶會收到該產品可用的電子郵件通知。 具有警示的產品在「產品資訊」面板中有&#x200B;_產品警示_&#x200B;標籤，其中會列出已訂閱警示的客戶。

![產品和價格警示訂閱清單](assets/inventory-product-alerts.png){width="600" zoomable="yes"}

## 設定產品警示

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Catalog]**&#x200B;並在下方選擇&#x200B;**[!UICONTROL Catalog]**。

1. 按一下以展開&#x200B;_[!UICONTROL Product Alerts]_&#x200B;區段並執行下列動作：

   ![產品警示](assets/config-catalog-product-alerts.png){width="600" zoomable="yes"}

   - 若要提供價格變更警示給您的客戶，請將&#x200B;**[!UICONTROL Allow Alert When Product Price Changes]**&#x200B;設為`Yes`。

   - 將&#x200B;**[!UICONTROL Price Alert Email Template]**&#x200B;設定為您要用於價格警示通知的範本。

   - 若要在缺貨產品再次可用時提供警示，請將&#x200B;**[!UICONTROL Allow Alert When Product Comes Back in Stock]**&#x200B;設為`Yes`。

     >[!NOTE]
     >
     >只有在&#x200B;**[!UICONTROL Display Out of Stock Products]**&#x200B;設定為`Yes` （在[!UICONTROL Catalog] > [!UICONTROL Inventory]的組態中）時，_當此產品有庫存時通知我_&#x200B;訊息才會出現。

   - 將&#x200B;**[!UICONTROL Stock Alert Email Template]**&#x200B;設定為您要用於產品庫存警示的範本。

   - 將&#x200B;**[!UICONTROL Alert Email Sender]**&#x200B;設定為您要顯示為電子郵件警示寄件者的[商店連絡人](../getting-started/store-details.md#store-email-addresses){target="_blank"}。 在核心使用手冊中進一步瞭解[存放區電子郵件地址](../configuration-reference/general/store-email-addresses.md){target="_blank"}。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

## 設定產品警報電子郵件範本

接下來，設定、新增或修改價格警示的電子郵件範本。 建立其他範本後，您可能會想要編輯價格警示設定。

如需有關使用電子郵件訊息的詳細資訊，請參閱&#x200B;_系統管理系統指南_&#x200B;中的[訊息範本](../systems/email-template-custom.md#message-templates)。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**。

1. 按一下&#x200B;**[!UICONTROL Add New Template]**。

1. 在&#x200B;_載入預設範本_&#x200B;下，選擇您要自訂的&#x200B;**[!UICONTROL Template]**。

   您可以選擇主題中包含的警報範本。 或者，您可以選取&#x200B;_[!UICONTROL Magento_PriceAlert]_&#x200B;下的`Price Alert`或`Stock Alert`範本。

1. 按一下&#x200B;**[!UICONTROL Load Template]**。

1. 輸入&#x200B;**[!UICONTROL Template Name]**。

   您可以在&#x200B;_價格警示_&#x200B;設定中選取此名稱。

1. 閱讀現有內容，並視需要進行下列變更：

   | 欄位 | 說明 |
   | ----- | ----- |
   | [!UICONTROL Template Subject] | 此文字會顯示在電子郵件的主旨行中。 |
   | [!UICONTROL Template Content] | 此文字會顯示在已傳送電子郵件的完整內容中。 |

1. 若要從[!DNL Commerce]資料新增產生的資訊，請使用&#x200B;**[!UICONTROL Insert Variable]**&#x200B;選項來使用可用變數清單。

1. 按一下&#x200B;**[!UICONTROL Save Template]**。

## 產品警示執行設定

這些設定可讓您選取[!DNL Commerce]檢查需要傳送警示之變更的頻率。 您也可以選取在傳送警示失敗時傳送之電子郵件的收件者、寄件者和範本。

![產品警示執行設定](assets/config-catalog-product-alerts-run-settings.png){width="600" zoomable="yes"}

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Catalog]**&#x200B;並在下方選擇&#x200B;**[!UICONTROL Catalog]**。

1. 展開&#x200B;**[!UICONTROL Product Alerts Run Settings]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

1. 若要判斷產品警示的傳送頻率，請將&#x200B;**[!UICONTROL Frequency]**&#x200B;設定為下列其中一項：

   - `Daily`
   - `Weekly`
   - `Monthly`

1. 若要判斷產品警示的傳送時間，請將&#x200B;**[!UICONTROL Start Time]**&#x200B;設為小時、分鐘和秒。

   >[!NOTE]
   >
   >產品警報會由「product_alert」消費者傳送。

1. 針對&#x200B;**[!UICONTROL Error Email Recipient]**，輸入發生錯誤時要連絡之人員的電子郵件。

1. 針對&#x200B;**[!UICONTROL Error Email Sender]**，選取顯示為錯誤通知寄件者的存放區識別。

1. 將&#x200B;**[!UICONTROL Error Email Template]**&#x200B;設為用於錯誤通知的交易式電子郵件範本。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。
