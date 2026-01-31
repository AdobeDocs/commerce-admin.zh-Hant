---
title: 客戶群組
description: 使用客戶群組來決定哪些折扣可供指定至群組的客戶使用，以及與群組相關聯的稅捐類別。
exl-id: 6b785c4a-a5dc-480c-8182-2a940784218d
feature: Customers, Configuration
source-git-commit: 17469d27128030b54fad6cf563a4b53f5f119eed
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---

# 客戶群組

客戶群組決定可用的折扣，以及與群組相關聯的稅捐類別。 預設客戶群組為`General`、`Not Logged In`和`Wholesale`。

![客戶群組](assets/customer-groups.png){width="700" zoomable="yes"}

## 篩選[!UICONTROL Customer Groups]清單

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**。

1. 按一下&#x200B;**[!UICONTROL Filters]**。

1. 輸入搜尋群組的條件，包括識別碼、群組或稅捐類別的範圍。

   ![篩選選項](assets/groups-filters.png){width="600" zoomable="yes"}

1. 完成時，按一下&#x200B;**[!UICONTROL Apply Filters]**。

## 建立客戶群組

>[!NOTE]
>
>沒有許可權存取所有網站的管理員使用者（獲指派角色為「自訂」[!UICONTROL Role Scope]）無法建立、修改或刪除客戶群組。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**。

1. 按一下&#x200B;**[!UICONTROL Add New Customer Group]**。

1. 對於[!DNL **Group Name]**，請輸入少於32個字元的唯一名稱以識別群組。

1. 選取套用至群組的&#x200B;**[!UICONTROL Tax Class]**。

   ![群組資訊](assets/group-information.png){width="600" zoomable="yes"}

1. 選取要從群組排除的&#x200B;**[!UICONTROL Excluded Website(s)]**。

   >[!IMPORTANT]
   >
   >排除網站可能會降低產品價格和目錄規則索引時間，因為排除的網站不會索引。 使用新增的網站排除專案儲存客戶群組時，產品價格、目錄規則和目錄搜尋索引會失效。 如果您有許多產品、網站和客戶群組，建議您暫停重新索引程式，直到您將網站從客戶群組排除為止。

   預設不會排除任何網站。 若要選取多個值，請按住&#x200B;_Ctrl_&#x200B;鍵（電腦）或&#x200B;_Command_&#x200B;鍵(Mac)，然後按一下每個選項。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Customer Group]**。

## 編輯客戶群組

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**。

1. 以編輯模式開啟記錄。

1. 進行必要的變更。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Customer Group]**。

## 將客戶指派至其他群組

>[!NOTE]
>
>變更公司群組後，公司使用者必須登出並登入店面，才能在目錄中檢視新價格。
>將客戶指派給公司後，「客戶群組」會變成唯讀，且無法由管理員使用者更新。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL All Customers]**。

1. 在清單中尋找客戶，並選取第一欄中的核取方塊。

1. 將&#x200B;**動作**&#x200B;控制項設為`Assign a Customer Group`，然後從功能表中選擇群組。

   ![指派客戶群組](assets/group-assign.png){width="600" zoomable="yes"}

1. 提示確認時，按一下&#x200B;**確定**。

## 將客戶群組與特定折扣建立關聯

1. 在&#x200B;_管理員_&#x200B;側邊欄上，前往&#x200B;**[!UICONTROL Marketing]** > _促銷活動_ > **[!UICONTROL Cart Price Rules]**。

1. 選取您想要為套用折扣建立群組關聯的購物車價格規則，或[建立價格規則](../merchandising-promotions/price-rules-catalog.md)。

1. 選取規則套用的客戶群組。

   ![客戶群組至特定折扣](assets/group-discount.png){width="600" zoomable="yes"}

1. 按一下&#x200B;**[!UICONTROL Save]**。

>[!NOTE]
>
> 您也可以使用「進階訂價」，將產品折扣套用至客戶群組。 請參閱[進階定價](../catalog/product-price-group.md)。

## 刪除客戶群組

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**。

1. 以編輯模式開啟記錄。

1. 在按鈕列中按一下&#x200B;**[!UICONTROL Delete Customer Group]**。

1. 提示確認時，按一下&#x200B;**確定**。

## 客戶群組示範

透過觀看此示範以瞭解如何建立客戶群組：

>[!VIDEO](https://video.tv.adobe.com/v/343660/?quality=12&learn=on)
