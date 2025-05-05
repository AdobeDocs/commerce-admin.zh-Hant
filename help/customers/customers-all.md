---
title: 客戶清單
description: 「客戶」方格會列出已向您的商店註冊帳戶或由管理員新增的所有客戶。
exl-id: a7d9b098-4892-492c-b937-61cc33b836d8
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# 客戶清單

在Admin中，[!UICONTROL Customers]格線列出已在您的商店註冊帳戶或由管理員新增的所有客戶。 使用標準[格線控制項](../getting-started/admin-grid-controls.md)來篩選清單並調整資料行配置。 若要深入瞭解，請參閱[管理客戶帳戶](../customers/manage-account.md)。

![客戶清單](assets/customer-accounts-all-grid.png){width="700" zoomable="yes"}

## 更新客戶資訊

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL All Customers]**。

1. 尋找客戶記錄並按一下&#x200B;_[!UICONTROL Action]_&#x200B;欄中的&#x200B;[!UICONTROL **編輯**]。

1. 在左側面板中，選擇要編輯的資訊並進行必要的變更。

   >[!NOTE]
   >
   >若要深入瞭解，請參閱[更新客戶帳戶](../customers/update-account.md)。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Customer]**。

## Workspace控制項

| 控制 | 說明 |
| --- | --- |
| **[!UICONTROL Add New Customer]** | 建立客戶帳戶。 |
| **[!UICONTROL Search]** | 根據目前的篩選器開始搜尋客戶。 |
| **[!UICONTROL Filters]** | 定義一組搜尋引數，用來篩選出現在[網格](../getting-started/admin-grid-controls.md)中的記錄。 |
| **[!UICONTROL Default View]** | 決定格線的預設資料行[配置](../getting-started/admin-grid-controls.md)。 |
| **[!UICONTROL Columns]** | 決定網格中[欄](../getting-started/admin-grid-controls.md)及其帳戶的選取範圍。 資料行配置可以變更並儲存為&#x200B;_檢視_。 依預設，網格中只包含某些欄。 |
| **[!UICONTROL Export]** | 將選取的記錄匯出為CSV或Excel XML檔案。 |

{style="table-layout:auto"}

## 欄

| 欄 | 說明 |
| --- | --- |
| **[!UICONTROL Select]** | 管理用於套用動作的客戶記錄的核取方塊選擇。 您也可以使用欄標題中的選取控制項來選取/取消選取全部。 |
| **[!UICONTROL ID]** | 建立客戶帳戶時指派的唯一數值識別碼。 |
| **[!UICONTROL Name]** | 客戶的名字和姓氏。 |
| **[!UICONTROL Email]** | 客戶的電子郵件地址。 |
| **[!UICONTROL Group]** | 客戶被指派到的客戶群組。 |
| **[!UICONTROL Phone]** | 客戶的電話號碼。 |
| **[!UICONTROL ZIP]** | 客戶的郵遞區號。 |
| **[!UICONTROL Country]** | 客戶所在的國家/地區。 |
| **[!UICONTROL State/Province]** | 客戶所在的州或省。 |
| **[!UICONTROL Customer Since]** | 建立客戶帳戶的日期和時間。 |
| **[!UICONTROL Web Site]** | 商店階層中與客戶帳戶相關聯的網站。 |
| **[!UICONTROL Confirmed Email]** | 表示是否需要確認電子郵件。 |
| **[!UICONTROL Account Created In]** | 表示建立客戶帳戶的來源商店檢視。 |
| **[!UICONTROL Date of Birth]** | 客戶的出生日期。 <br><br>**_重要：_**&#x200B;根據目前的安全性和隱私權最佳實務，請注意任何與客戶的完整出生日期（月、日、年）和其他個人識別碼儲存相關的潛在法律和安全風險。 建議您限制客戶完整出生日期的儲存量，並建議使用客戶出生年作為替代方法。 |
| **[!UICONTROL Tax / VAT Number]** | 如果適用，則為指定給客戶的稅捐編號或[加值稅](../stores-purchase/vat.md)編號。 <br/><br/>此欄位與VAT編號不同。 |
| **[!UICONTROL Gender]** | 客戶的性別。 |
| **[!UICONTROL Action]** | 編輯 — 在編輯模式中開啟公司帳戶。 |

{style="table-layout:auto"}

### 其他欄

變更格線的[資料行配置](../getting-started/admin-grid-controls.md)即可使用這些資料行。

| 欄 | 說明 |
| --- | --- |
| **[!UICONTROL Company]** | 客戶的公司名稱。 |
| **[!UICONTROL Street Address]** | 客戶的街道地址。 |
| **[!UICONTROL City]** | 客戶所在的城市。 |
| **[!UICONTROL Fax]** | 客戶的傳真號碼（如適用）。 |
| **[!UICONTROL Billing Firstname]** | 客戶帳單地址中的名字。 |
| **[!UICONTROL Billing Lastname]** | 客戶帳單地址中的姓氏。 |
| **[!UICONTROL Billing Address]** | 將傳送帳單資訊的地址。 |
| **[!UICONTROL Shipping Address]** | 訂單的送貨地址。 |
| **[!UICONTROL VAT Number]** | 與客戶地址相關聯的增值稅編號。 對於在歐盟銷售的[數位商品](../stores-purchase/taxes.md)，VAT是以客戶的帳單地址為基礎。 <br/><br/>此欄位與稅捐/VAT編號不同。 |
| **[!UICONTROL Account Lock]** | 表示帳戶的狀態。 作為安全性測量，在太多登入嘗試後，客戶帳戶可能被[鎖定](../customers/password-options.md)。 值： `Locked` / `Unlocked` |

{style="table-layout:auto"}
