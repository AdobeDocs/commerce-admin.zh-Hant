---
title: 設定引號
description: 瞭解報價組態，其控制報價請求、報價存留期及檔案附件所需的最低訂單金額。
exl-id: 865f6624-df9b-4f78-abfa-1f9a3d82bc0d
feature: B2B, Companies, Configuration, Quotes
role: Admin
source-git-commit: d4c3ea4b49e30ae3af249516d32fb28437d218b8
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# 設定引號

如果在一般情況下啟用引號 [B2B功能](enable-basic-features.md)中，您可以在Admin中設定對引號的支援。 報價組態會決定報價請求所需的最低訂單金額、報價存留期，以及附加檔案支援的檔案格式。

>[!NOTE]
>
>報價組態選項及使用報價議價功能的功能是使用 [角色資源](../systems/permissions-user-roles.md#role-resources). 必須為指派給管理員使用者帳戶的管理員使用者角色選擇這些角色資源。 若要授予Admin中報價功能的存取權，請前往 **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**，選取角色，並導覽至 [!UICONTROL Sales] > [!UICONTROL Operations] > [!UICONTROL Quotes] 在_&#x200B;角色資源&#x200B;_樹狀結構。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Sales]** 並選擇 **[!UICONTROL Quotes]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL General]** 並執行下列動作：

   ![銷售報價設定 — 一般](./assets/quotes-general.png){width="700" zoomable="yes"}

   另請參閱 [引號](../configuration-reference/sales/quotes.md) 在 _設定參考_ 以取得Quotes功能選項及其功能的完整清單。

   - 輸入 **[!UICONTROL Minimum Amount]** 在提交報價請求之前必須滿足的購物車中。

   - 的 **[!UICONTROL Minimum Amount Message]**，輸入當購物車總計不符合最低需求量時要顯示的訊息。

   - 的 **[!UICONTROL Default Expiration Period]**，輸入數字 **[!UICONTROL days]**， **[!UICONTROL weeks]**，或 **[!UICONTROL months]** 引號將保持有效。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Attached files]** 並執行下列動作：

   - 的 **[!UICONTROL File formats for upload]**，輸入您支援附加至引號之檔案的每一種檔案型別尾碼。

     以小寫輸入每個檔案尾碼，並以逗號分隔。

     依預設，支援下列格式： `doc`， `docx`， `xls`， `xlsx`， `pdf`， `txt`， `jpg`， `png`、和 `jpeg`

   - 的 **[!UICONTROL Maximum file size]**，輸入附加檔案的大小上限（以MB為單位）。

     您輸入的值可能會被伺服器設定覆寫。

     ![銷售報價組態 — 附加檔案](./assets/quotes-attached-files.png){width="600" zoomable="yes"}

1. 完成後，按一下 **[!UICONTROL Save Config]**.
