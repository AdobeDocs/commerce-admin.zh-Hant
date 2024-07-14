---
title: "[!UICONTROL My Purchase Orders]"
description: 瞭解採購單，以及公司如何使用採購單管理其採購。
exl-id: b7348bc8-b874-4642-a372-530883d9d94c
feature: B2B, Companies, Purchase Orders
source-git-commit: c94d4e8d13c32c1c1b1d37440fdb953c8527b76c
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---

# [!UICONTROL My Purchase Orders]

當為公司](purchase-order-flow.md)啟用採購單時，[客戶登入公司使用者帳戶的任何訂單都會自動建立為採購單(PO)。 具有必要許可權的公司使用者可以建立、編輯和刪除他們建立的採購單，以及下屬使用者建立的採購單。

![我的採購單](./assets/account-dashboard-my-purchase-orders.png){width="700" zoomable="yes"}

>[!NOTE]
>
>「採購單」會在建立訂單時，建立料號價格、折扣及送貨價格的&#x200B;_快照_。 如果料號的價格在建立採購單後變更，則會使用原始價格。

## 管理採購單

從&#x200B;_檢視採購單_&#x200B;頁面，客戶可以根據其[角色許可權](account-company-roles-permissions.md)管理採購單。

- 若要檢視採購單，請按一下&#x200B;**[!UICONTROL View]**。
- 若要檢視有關採購單的任何註解，請按一下&#x200B;**[!UICONTROL Comments]**&#x200B;標籤。
- 若要檢視完整的訂單歷史記錄，請按一下&#x200B;**[!UICONTROL History Log]**&#x200B;標籤。

>[!IMPORTANT]
>
>如果採購單中的料號無庫存，或可用數量不足，則當採購單轉換為實際訂單時，會發生錯誤。 如果啟用延期交貨，則會正常處理訂單。

## 現有採購單的新採購單

如果客戶有現有的採購單，並且想要新增料號，他們可以產生重複採購單，並將新產品新增至新採購單。 客戶完成下列步驟：

1. 在&#x200B;_我的採購單_&#x200B;頁面上，客戶找到採購單並按一下&#x200B;**[!UICONTROL View]**&#x200B;連結。

1. 客戶按一下&#x200B;**[!UICONTROL Add Items to Shopping Cart]**。

   「購物車」頁面隨即開啟，並列出所有專案。

1. 進行任何新增或變更。

1. （選擇性）使用&#x200B;**[!UICONTROL Custom Reference Number]**&#x200B;將內部發票/採購單編號新增至訂單。

1. 遵循一般簽出工作流程並按一下&#x200B;**[!UICONTROL Place Purchase Order]**。

如果他們按一下&#x200B;_[!UICONTROL Add Items to Shopping Cart]_時購物車中有專案，系統會顯示對話方塊。 此對話方塊可讓他們選擇將購物車專案與新專案合併，或將購物車中的專案取代為採購單中的專案。

如果不再需要原始採購單，則可將其關閉。

## 採購單核准

對於根據公司結構或指派的公司角色指定為核准者的客戶，_[!UICONTROL My Purchase Orders]_儀表板頁面會顯示&#x200B;**[!UICONTROL Requires My Approval]**標籤。 客戶按一下此索引標籤，以複查等待核准的採購單。 計數器顯示等待核准的訂單數。

按一下採購單的&#x200B;**[!UICONTROL View]**&#x200B;並檢閱詳細資料後，核准者可以按一下&#x200B;**[!UICONTROL Approve]**&#x200B;或&#x200B;**[!UICONTROL Reject]**。

### 大量核准/拒絕

從Adobe Commerce 2.4.1開始，核准者可以一次核准或拒絕多個採購單。

1. 在&#x200B;_[!UICONTROL My Purchase Order]_頁面上，按一下&#x200B;**[!UICONTROL Requires My Approval]**標籤。

1. 選取每個要核准或拒絕之採購單的核取方塊。

1. 按一下&#x200B;**[!UICONTROL Approve Selected]**&#x200B;或&#x200B;**[!UICONTROL Reject Selected]**。

客戶只能選取狀態允許動作的採購單。 公司管理員可以對其公司中的任何有效採購單進行大量核准或拒絕。
