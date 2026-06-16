---
title: 將客戶群組指派至公司
description: 瞭解如何在您的Adobe Commerce商店中指派客戶群組至公司帳戶。
exl-id: fba3c17e-95df-4e9e-84b8-67409c6da72d
feature: B2B, Companies, Configuration, Customers
role: Admin, User
TQID: https://experienceleague.adobe.com/O03eRkYyE78HIHjmwYRXqfOR2A7k1KFL11AspJGCi-U
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2: id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 236
ht-degree: 0%

---

# 將客戶群組指派至公司

將客戶群組指派給公司，基本上與指派共用目錄相同。 如果組態](enable-basic-features.md)中未啟用共用目錄[，則會將客戶群組（而非共用目錄）指派給公司。

- 一次只能將一個客戶群組或共用目錄指派給公司。 無法刪除與共用目錄相關聯的客戶群組。
- 變更指派給公司的客戶群組會更新所有公司成員的設定檔。
- 如果客戶群組指派從共用目錄變更為一般客戶群組，則公司成員會失去共用目錄的存取權，而他們可以從店面取得主要目錄。
- 變更公司群組後，公司使用者必須登出並登入店面，才能在目錄中檢視新價格。

## 變更客戶群組

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL Companies]**。

1. 在網格中尋找公司，然後按一下&#x200B;_[!UICONTROL Action]_欄中的&#x200B;**[!UICONTROL Edit]**。

   ![編輯公司](./assets/companies-grid-edit.png){width="700" zoomable="yes"}

1. 在公司頁面上，向下捲動並展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Advanced Settings]**&#x200B;區段。

1. 設定適當的&#x200B;**[!UICONTROL Customer Group]**。

   [!UICONTROL Customer Group]清單包含所有現有的共用目錄，即使組態中停用共用目錄亦然。

   ![變更客戶群組或共用目錄](./assets/company-advanced-settings-customer-group-admin.png){width="600"}

1. 提示確認時，按一下&#x200B;**[!UICONTROL Proceed]**。

1. 按一下&#x200B;**[!UICONTROL Save]**。
