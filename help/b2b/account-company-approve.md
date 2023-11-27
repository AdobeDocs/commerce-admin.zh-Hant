---
title: 核准公司帳戶
description: 瞭解如何在Admin中核准公司帳戶請求。
exl-id: c7123383-0e94-4d6c-be3c-b6ca84145a59
feature: B2B, Companies, Configuration
role: Admin, User
source-git-commit: 2b86fe55f980c22839de10ecc4c9023034eb9ea1
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---

# 核准公司帳戶

從店面接收以建立公司的請求的狀態為 `Pending Approval` 直到存放區管理員檢閱要求為止，且已核准或已拒絕。 公司帳戶的狀態可設為下列任一專案：

- [!UICONTROL Active]
- [!UICONTROL Pending Approval]
- [!UICONTROL Rejected]
- [!UICONTROL Blocked]

您也可以使用 [動作控制](account-company-manage.md) 以核准多個公司請求。

![未決核准](./assets/companies-pending-approval.png){width="700" zoomable="yes"}

## 核准擱置中的公司帳戶

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   您可以使用 _[!UICONTROL Columns]_方格上方的選取器，以顯示&#x200B;**[!UICONTROL Status]**欄。

1. 在 _[!UICONTROL Action]_欄，按一下&#x200B;**[!UICONTROL Edit]**.

1. 設定 **[!UICONTROL Company Status]** 至 `Active`.

   ![設定公司狀態](./assets/company-status-active.png){width="700" zoomable="yes"}

1. 提示確認時，按一下 **[!UICONTROL Change status]**.

   公司管理員會收到電子郵件通知，告知公司目前為有效狀態。

1. 如果適用，請設定 **[!UICONTROL Sales Representative]** 至特定的管理員使用者帳戶。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png)  此 **[!UICONTROL Account Information]** 區段並使用 **[!UICONTROL Comment]** 欄位以輸入有關帳戶的附註。

   從店面看不見註解。

1. 完成後，按一下 **[!UICONTROL Save]**.

   系統會傳送確認電子郵件給公司及公司管理員，確認已核准公司帳戶。

## 公司狀態

| 狀態 | 說明 |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Active] | 公司已獲得核准，並可由公司管理員從店面管理。 |
| [!UICONTROL Pending Approval] | 建立公司帳戶的請求已從店面提交，但尚未稽核。 |
| [!UICONTROL Rejected] | 建立公司帳戶的請求被商店管理員拒絕。 |
| [!UICONTROL Blocked] | 公司帳戶已無法正常運作。 客戶可以從店面存取帳戶，但無法進行購買。 |

{style="table-layout:auto"}
