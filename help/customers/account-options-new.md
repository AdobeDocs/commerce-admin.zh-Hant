---
title: 新客戶帳戶選項
description: 瞭解商店中新客戶帳戶的設定選項。
exl-id: aa19f0e2-ffbe-433d-8bd5-c14700b67b37
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 0%

---

# 新客戶帳戶選項

在 _[!UICONTROL Create New Account Options]_在設定的區段，基本帳戶選項與更多與VAT ID驗證和自訂整合相關的進階選項結合。 下列指示僅涵蓋最常使用的選項。 若要瞭解自動客戶群組指派，請參閱 [VAT驗證](../stores-purchase/vat.md).

{{beta-updates}}

![建立新帳戶選項](assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

## 設定基本客戶帳戶選項

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Customers]** 並選擇 **[!UICONTROL Customer Configuration]**.

1. 展開 **[!UICONTROL Create New Account Options]** 區段：

   ![建立新帳戶選項預設設定](../configuration-reference/customers/assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

1. 根據您在店面需要支援的客戶體驗設定每個選項：

   - 設定 **[!UICONTROL Default Group]** 至建立帳戶時指派給新客戶的客戶群組。

   - 如果您擁有 _增值稅_ 編號並想要讓客戶看見，請設定 **[!UICONTROL Show VAT Number on Storefront]** 至 `Yes`.

   - 若要在客戶建立管理員訂單時要求客戶提供電子郵件，請設定 **[!UICONTROL Email is required field for Admin order creation]** 至 `Yes`.

   - 輸入 **[!UICONTROL Default Email Domain]** 適用於此商店，例如 `mystore.com`

   - 設定 **[!UICONTROL Default Welcome Email]** ，此範本用於傳送給新客戶的歡迎電子郵件。

   - 設定 **[!UICONTROL Default Welcome Email without Password]** 用於建立尚未有密碼的客戶帳戶時的範本。 例如，從「管理員」建立的客戶帳戶尚未指派密碼。

   - 設定 **[!UICONTROL Email Sender]** 將顯示為歡迎電子郵件寄件者的商店連絡人。

   - 若要要求客戶確認其透過您的商店開立帳戶的請求，請設定 **[!UICONTROL Require Emails Confirmation]** 至 `Yes`. 然後，設定 **[!UICONTROL Confirmation Link Email]** 至用於確認電子郵件的範本。

   - 設定 **[!UICONTROL Welcome Email]** 至確認帳戶後所傳送之歡迎訊息所使用的範本。

     ![建立已啟用VAT的新帳戶選項](../configuration-reference/customers/assets/customer-configuration-create-new-account-options-vat.png){width="600" zoomable="yes"}

     如需此組態選項集內每個可用選項的詳細資訊，請參閱 _建立新帳戶選項_ [設定參考](../configuration-reference/customers/customer-configuration.md).

1. 完成後，按一下 **[!UICONTROL Save Config]**.
