---
title: 詢價
description: 瞭解與公司帳戶相關聯的客戶如何提交報價請求。
exl-id: c52176a7-4076-4cea-8ddb-17e0d1a77fd9
feature: B2B, Quotes
role: Admin, User
source-git-commit: b53d77364f09e587813c50221ebd85ac633f1296
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# 詢價

如果在以下欄位中啟用引號： [銷售功能設定](configure-quotes.md)，公司的授權買家可以透過要求購物車的報價來啟動價格議價流程。 如果採購員尚未準備好提交報價以進行議價，他們可以將報價儲存為草稿。

>[!NOTE]
>
>詢價不可包含折扣代碼或禮品卡。

## 客戶報價請求體驗

1. 客戶以購買者的身分登入其使用者帳戶， [許可權](account-company-roles-permissions.md) 以請求報價。

1. 新增要包含在報價中的產品至購物車。

   >[!TIP]
   > 
   >客戶可以使用將產品SKU清單更快速地新增到購物車 [快速訂購](quick-order.md).

1. 選取 **[!UICONTROL Request a Quote]**.

   ![向購物車要求報價](./assets/quote-request-from-cart.png){width="700" zoomable="yes"}

1. 在 **[!UICONTROL Add your comment]** 方塊中，客戶輸入簡短的附註以說明請求。

1. 輸入 **[!UICONTROL Quote Name]**.

   ![輸入報價註解與名稱](./assets/quote-request-from-cart-name-comments.png){width="400" zoomable="yes"}

1. 如有需要，請將支援檔案或影像附加至報價：

   - 選取 **[!UICONTROL Attach file]**.
   - 從系統選擇檔案。

   依預設， [附加的檔案](configure-quotes.md) 最大可達2 MB，為下列任何檔案格式：DOC、DOCX、XLS、XLSX、PDF、TXT、JPG或JPEG、PNG。

1. 建立及處理報價單：

   - 將報價傳送給賣家，方法是選取 **[!UICONTROL Request a Quote]**.
   - [!BADGE 1.5.0測試版功能]{type=Informative url="/help/b2b/release-notes.md" tooltip="僅供測試版計畫參與者使用"}**[!UICONTROL Save as Draft]**.

     如果採購員將報價單另存為草稿，則可在以下位置找到報價： [!UICONTROL My Quotes] 在 `Draft` 州別。 在買方傳送草擬報價以供複查之前，賣方無法看到草擬報價。
