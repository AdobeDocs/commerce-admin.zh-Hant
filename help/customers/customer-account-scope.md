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

您商店中每個頁面的頁首都會邀請購物者&#x200B;_登入或在您的商店註冊_&#x200B;帳戶。 開立帳戶的客戶可享有一系列權益，包括：

* **建立客戶帳戶** — 訪客可以建立客戶帳戶，以便將該店面作為註冊客戶使用。
* **建立公司帳戶**&#x200B;根據組態，您商店的訪客可以選擇建立公司帳戶。 如需詳細資訊，請參閱[Adobe Commerce B2B](../b2b/introduction.md)。
* **更快速的結帳** — 註冊客戶更快速地完成結帳，因為許多資訊已經存在其帳戶中。
* **自助服務** — 註冊客戶可以更新其資訊、檢查訂單狀態，甚至從其帳戶重新排序。

客戶可以按一下商店標題中的&#x200B;**[!UICONTROL My Account]**&#x200B;連結來存取其帳戶。 客戶可以透過帳戶檢視及修改資訊，包括過去和目前地址、帳單和運送偏好設定、電子報訂閱、願望清單等。

![我的帳戶](assets/account-dashboard-my-account.png){width="600" zoomable="yes"}

## 設定客戶帳戶的範圍

客戶帳戶的範圍可以限於建立帳戶的網站，或與商店階層中的所有網站和商店共用。

>[!NOTE]
>
>如果網站從客戶群組中排除，則當客戶帳戶的範圍僅限於網站或與所有網站共用時，不允許客戶登入網站。 請參閱[建立客戶群組](customer-groups.md#create-a-customer-group)，以取得將網站從群組排除的詳細資訊。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > [!UICONTROL _[!UICONTROL Settings]_] > **[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Customers]**&#x200B;並選擇&#x200B;**[!UICONTROL Customer Configuration]**。

1. 展開&#x200B;**[!UICONTROL Account Sharing Options]**&#x200B;區段。

   ![帳戶共用選項](assets/customer-configuration-account-sharing-options.png){width="600" zoomable="yes"}

1. 將&#x200B;**[!UICONTROL Share Customer Accounts]**&#x200B;設定為下列其中一項：

   | 選項 | 說明 |
   | --- | --- |
   | `Global` | 與安裝中的每個網站和商店共用客戶帳戶資訊。 |
   | `Per Website` | 將客戶帳戶資訊限制在建立帳戶的網站。 |

   {style="table-layout:auto"}

   >[!INFO]
   >
   > 如有必要，請清除&#x200B;**[!UICONTROL User system value]**&#x200B;核取方塊以進行變更。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

   >[!NOTE]
   >
   >選取`Global`時，會分享&#x200B;**我的帳戶**&#x200B;中的客戶資訊（地址和帳戶資訊，例如連絡人詳細資料）。
