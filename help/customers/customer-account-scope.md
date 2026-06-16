---
title: 客戶帳戶範圍
description: 客戶帳戶的範圍可以限於建立帳戶的網站，或與商店階層中的所有網站和商店共用。
exl-id: c401bee2-763e-4fad-88cd-5d5a43c46186
feature: Customers, Configuration
TQID: https://experienceleague.adobe.com/ah5XmCeeX4Kc9czcllRq9zZX4W3rkkqkzcoUXtJjo5I
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: c1256247-af4b-46d8-9dca-0c654ecfa157id: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2: id: b01a71b7-d17a-42b2-a9ac-af4b8d9d2ef5id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 356
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
