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

有時候，客戶需要協助處理訂單。 存放區管理員可以使用&#x200B;_以客戶身分登入_，讓他們檢視客戶看到的內容並進行更新以協助他們。

以客戶身分登入時執行的任何動作會套用至實際客戶的帳戶。

為&#x200B;_管理員_&#x200B;使用者啟用時，_[!UICONTROL Login as Customer]_&#x200B;按鈕會出現在多個頁面中：

* [客戶編輯頁面](../customers/update-account.md)
* [訂單檢視頁面](../stores-purchase/order-processing.md)
* [商業發票檢視頁面](../stores-purchase/invoices.md)
* [出貨檢視頁面](../stores-purchase/shipments.md)
* [銷退折讓單檢視頁面](../stores-purchase/credit-memo-create.md)

![以客戶身分登入](assets/login-as-customer.png){width="600" zoomable="yes"}

## 啟用客戶登入

啟用&#x200B;_以客戶身分登入_&#x200B;需要您在Commerce執行個體中啟用該功能，然後以使用者角色許可權為管理員使用者啟用存取權。

### 啟用功能

1. 在管理員側邊欄上，前往&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Customers]**&#x200B;並選擇&#x200B;**[!UICONTROL Login as Customer]**。

   ![組態選項 — 以客戶身分登入](../configuration-reference/customers/assets/login-as-customer.png){width="600" zoomable="yes"}

1. 將&#x200B;**[!UICONTROL Enable Login as Customer]**&#x200B;設為`Yes`。

1. _（選擇性）_&#x200B;將&#x200B;**[!UICONTROL Disable Page Cache for Admin User]**&#x200B;設為`No`以在管理員使用者以客戶身分登入時啟用頁面快取。

   >[!WARNING]
   >
   > 停用頁面快取（`Yes` — 預設）可確保使用者在客戶登入時取得最新且未快取的資料。

1. _（選擇性）_&#x200B;如果您有多網站及/或多重商店設定，且希望管理員使用者在登入時以客戶身分選取商店檢視，請將&#x200B;**[!UICONTROL Store View to Log in]**&#x200B;設為`Manual Selection`。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

### 為管理員使用者啟用存取權

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL System]** > _許可權_ > **[!UICONTROL User Roles]**。

1. 按一下清單中的角色。

1. 在&#x200B;[!UICONTROL _角色資訊_]&#x200B;左側面板中，按一下&#x200B;**[!UICONTROL Role Resources]**。

1. 將頁面上的&#x200B;**[!UICONTROL Role Resources]**&#x200B;變更為`Custom`。

   >[!INFO]
   >
   > 選取此選項後，頁面中會顯示資源階層。

1. 捲動至&#x200B;**[!UICONTROL Customers]**&#x200B;父專案與下方的&#x200B;**[!UICONTROL Login as Customer]**&#x200B;專案。 然後，選取您要為角色啟用的資源：

   * **[!UICONTROL Allow Login as Customer]** — 允許管理員使用者使用&#x200B;_登入作為客戶_&#x200B;功能。
   * **[!UICONTROL View Login as Customer Log]** — 允許管理員使用者檢視&#x200B;_以客戶身分登入_&#x200B;記錄檔。

   ![角色資源 — 以客戶身分登入](assets/customers-login-as-customer-role-resources.png){width="400" zoomable="yes"}

1. 按一下&#x200B;**[!UICONTROL Save Role]**。

## 從管理員以客戶身分登入

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Customers]** > [!UICONTROL _所有客戶_]。

1. 在編輯模式中開啟使用者。

1. 在&#x200B;**[!UICONTROL Customer Information]**&#x200B;面板中，選擇&#x200B;**[!UICONTROL Account Information]**&#x200B;區段。

1. 將&#x200B;**[!UICONTROL Allow remote shopping assistance]**&#x200B;設為`Yes`。

   >[!INFO]
   >
   >管理員現在可以使用者身分登入，無需店面的許可權。

## 遠端購物協助的客戶帳戶許可權

若要透過管理員為商店支援人員啟用帳戶存取權，客戶必須為其帳戶啟用此功能：

1. 客戶前往&#x200B;**[!UICONTROL Account Information]**&#x200B;頁面。

1. 選取&#x200B;**[!UICONTROL Allow remote shopping assistance]**&#x200B;核取方塊。

1. 客戶按一下&#x200B;**[!UICONTROL Save]**。

![帳戶資訊頁](assets/permission.png){width="700" zoomable="yes"}

>[!WARNING]
>
>沒有此許可權，管理員使用者無法以此客戶身分登入。

## 以客戶身分使用登入

>[!INFO]
>
>若要使用&#x200B;_Login作為客戶_，請確定您的管理員已如前所述設定。

_以客戶身分登入_&#x200B;可讓您檢視網站，就像客戶一樣，並可讓您為客戶進行疑難排解和採取其他動作。 如果您有指派的使用者角色具有所需的許可權：

1. 您可以在上一節所列的頁面上按一下&#x200B;**[!UICONTROL Login as Customer]**。
1. 「動作報表」提供「以客戶身分登入」動作。

>[!WARNING]
>
>以客戶&#x200B;_身分登入_&#x200B;時執行的任何動作（例如新增/移除產品）都會套用至實際客戶的訂單。 在店面，當您`logged in as customer_name`提供特殊狀態的提醒時，會顯示橫幅。

## 以客戶記錄身分登入

{{ee-feature}}

Adobe Commerce提供&#x200B;_以客戶_&#x200B;身分登入動作的記錄。 其中會列出管理員使用者存取功能的所有工作階段。 若要存取記錄的動作，請移至[管理動作報表](../systems/action-log-report.md)。

您可以篩選頁面頂端的報表設定&#x200B;**[!UICONTROL Action Group]**&#x200B;為`Login As Customer`，然後按一下&#x200B;**[!UICONTROL Search]**。

![篩選動作報告](assets/customers-login-as-customer-log-filter.png){width="700" zoomable="yes"}
