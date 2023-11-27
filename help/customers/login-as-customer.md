---
title: 為購物者提供協助
description: 當您使用登入作為客戶功能時，您可以檢視客戶看到的內容並代表他們進行更新。
exl-id: 6842ae7a-6440-45f1-af18-e6427088d29d
feature: Customers, Customer Service
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# 為購物者提供協助

有時候，客戶需要協助處理訂單。 存放區管理員可以使用 _客戶登入_，可讓他們檢視客戶看到什麼並進行更新以協助他們。

以客戶身分登入時執行的任何動作會套用至實際客戶的帳戶。

為以下專案啟用時： _管理員_ 使用者， _[!UICONTROL Login as Customer]_按鈕會顯示在多個頁面中：

* [客戶編輯頁面](../customers/update-account.md)
* [訂單檢視頁面](../stores-purchase/order-processing.md)
* [商業發票檢視頁面](../stores-purchase/invoices.md)
* [出貨檢視頁面](../stores-purchase/shipments.md)
* [銷退折讓單檢視頁面](../stores-purchase/credit-memo-create.md)

![客戶登入](assets/login-as-customer.png){width="600" zoomable="yes"}

## 啟用客戶登入

正在啟用 _客戶登入_ 需要您在Commerce執行個體中啟用該功能，然後在使用者角色許可權中為管理員使用者啟用存取權。

### 啟用功能

1. 在管理員側邊欄上，前往  **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Customers]** 並選擇  **[!UICONTROL Login as Customer]**.

   ![設定選項 — 客戶登入](../configuration-reference/customers/assets/login-as-customer.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Enable Login as Customer]** 至 `Yes`.

1. _（可選）_ 設定 **[!UICONTROL Disable Page Cache for Admin User]** 至 `No` 當管理員使用者以客戶身分登入時，啟用頁面快取。

   >[!WARNING]
   >
   > 停用頁面快取(`Yes`  — 預設)確保使用者在客戶身分登入時能獲得最新且未快取的資料。

1. _（可選）_ 設定 **[!UICONTROL Store View to Log in]** 至 `Manual Selection` 若您具有多網站及/或多商店設定，且希望管理員使用者在以客戶身分登入時選取商店檢視。

1. 完成後，按一下 **[!UICONTROL Save Config]**.

### 為管理員使用者啟用存取權

1. 在 _管理員_ 側欄，前往 **[!UICONTROL System]** > _許可權_ > **[!UICONTROL User Roles]**.

1. 按一下清單中的角色。

1. 在 [!UICONTROL _角色資訊_] 左側面板，按一下 **[!UICONTROL Role Resources]**.

1. 變更 **[!UICONTROL Role Resources]** 在頁面至 `Custom`.

   >[!INFO]
   >
   > 選取此選項後，頁面中會顯示資源階層。

1. 捲動至  **[!UICONTROL Customers]** 上層專案和 **[!UICONTROL Login as Customer]** 專案底下。 然後，選取您要為角色啟用的資源：

   * **[!UICONTROL Allow Login as Customer]**  — 允許管理員使用者使用 _客戶登入_ 功能。
   * **[!UICONTROL View Login as Customer Log]**  — 允許管理員使用者檢視 _客戶登入_ 記錄。

   ![角色資源 — 客戶登入](assets/customers-login-as-customer-role-resources.png){width="400" zoomable="yes"}

1. 按一下 **[!UICONTROL Save Role]**.

## 從管理員以客戶身分登入

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Customers]** > [!UICONTROL _所有客戶_].

1. 在編輯模式中開啟使用者。

1. 在 **[!UICONTROL Customer Information]** 面板，選擇 **[!UICONTROL Account Information]** 區段。

1. 設定 **[!UICONTROL Allow remote shopping assistance]** 至 `Yes`.

   >[!INFO]
   >
   >管理員現在可以使用者身分登入，無需店面的許可權。

## 遠端購物協助的客戶帳戶許可權

若要透過管理員為商店支援人員啟用帳戶存取權，客戶必須為其帳戶啟用此功能：

1. 客戶前往 **[!UICONTROL Account Information]** 頁面。

1. 選取 **[!UICONTROL Allow remote shopping assistance]** 核取方塊。

1. 客戶點按 **[!UICONTROL Save]**.

![帳戶資訊頁面](assets/permission.png){width="700" zoomable="yes"}

>[!WARNING]
>
>沒有此許可權，管理員使用者無法以此客戶身分登入。

## 以客戶身分使用登入

>[!INFO]
>
>使用 _客戶登入_，請確定您的管理員已如前所述完成設定。

_客戶登入_ 可讓您檢視網站（就像客戶一樣），並讓您為客戶進行疑難排解並採取其他動作。 如果您有指派的使用者角色具有所需的許可權：

1. 您可以按一下 **[!UICONTROL Login as Customer]** 於上一節所列頁面上。
1. 「動作報表」提供「以客戶身分登入」動作。

>[!WARNING]
>
>登入時執行的任何動作 [!UICONTROL _作為客戶_] （例如新增/移除產品）會套用至實際客戶的訂單。 在店面，橫幅會在您選擇時顯示 `logged in as customer_name` 提供特殊狀態的提醒。

## 以客戶記錄身分登入

{{ee-feature}}

Adobe Commerce提供 _客戶登入_ 動作。 其中會列出管理員使用者存取功能的所有工作階段。 若要存取記錄的動作，請前往 [管理動作報表](../systems/action-log-report.md).

您可以篩選報表設定 **[!UICONTROL Action Group]** 至 `Login As Customer` ，然後按一下 **[!UICONTROL Search]**.

![篩選動作報表](assets/customers-login-as-customer-log-filter.png){width="700" zoomable="yes"}
