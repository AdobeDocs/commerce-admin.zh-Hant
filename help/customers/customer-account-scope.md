---
title: 客戶帳戶範圍
description: 客戶帳戶的範圍可以限於建立帳戶的網站，或與商店階層中的所有網站和商店共用。
exl-id: c401bee2-763e-4fad-88cd-5d5a43c46186
feature: Customers, Configuration
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 0%

---

# 客戶帳戶範圍

您商店中每個頁面的頁首都會邀請購物者前往 _登入或註冊_ 以取得您商店的帳戶。 開立帳戶的客戶可享有一系列權益，包括：

* **建立客戶帳戶**  — 訪客可建立客戶帳戶，以便使用該店面作為註冊客戶。
* **建立公司帳戶** 您商店的訪客可選擇建立公司帳戶，視設定而定。 如需詳細資訊，請參閱 [Adobe Commerce B2B](../b2b/introduction.md).
* **更快速的結帳**  — 註冊客戶結帳的速度更快，因為帳戶中已有許多資訊。
* **自助服務**  — 註冊客戶可以更新其資訊、檢查訂單狀態，甚至從其帳戶重新排序。

客戶可以按一下 **[!UICONTROL My Account]** 商店標題中的連結。 客戶可以透過帳戶檢視及修改資訊，包括過去和目前地址、帳單和運送偏好設定、電子報訂閱、願望清單等。

![我的帳戶](assets/account-dashboard-my-account.png){width="600" zoomable="yes"}

## 設定客戶帳戶的範圍

客戶帳戶的範圍可以限於建立帳戶的網站，或與商店階層中的所有網站和商店共用。

>[!NOTE]
>
>如果網站從客戶群組中排除，則當客戶帳戶的範圍僅限於網站或與所有網站共用時，不允許客戶登入網站。 另請參閱 [建立客戶群組](customer-groups.md#create-a-customer-group) 以取得將網站從群組排除的詳細資訊。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > [!UICONTROL _[!UICONTROL Settings]_] > **[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Customers]** 並選擇 **[!UICONTROL Customer Configuration]**.

1. 展開 **[!UICONTROL Account Sharing Options]** 區段。

   ![帳戶共用選項](assets/customer-configuration-account-sharing-options.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Share Customer Accounts]** 變更為下列其中一項：

   | 選項 | 說明 |
   | --- | --- |
   | `Global` | 與安裝中的每個網站和商店共用客戶帳戶資訊。 |
   | `Per Website` | 將客戶帳戶資訊限制在建立帳戶的網站。 |

   {style="table-layout:auto"}

   >[!INFO]
   >
   > 如有必要，請清除 **[!UICONTROL User system value]** 核取方塊以進行變更。

1. 完成後，按一下 **[!UICONTROL Save Config]**.

   >[!NOTE]
   >
   >時間 `Global` 已選取以下位置的客戶資訊： **我的帳戶** （地址和帳戶資訊，例如聯絡人詳細資訊）會分享。
