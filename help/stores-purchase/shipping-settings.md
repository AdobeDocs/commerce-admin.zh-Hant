---
title: 送貨設定
description: 瞭解如何設定出貨設定，以定義商店的原點和出貨政策。
exl-id: 767b3039-39c7-4692-a0a8-a8fde27622cc
feature: Shipping/Delivery
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 0%

---

# 送貨設定

出貨組態會建立所有出貨的原點、您的出貨政策，以及將出貨處理至多個地址。

## 原點

原點用於計算從您的商店或倉儲出貨的費用，也可以決定已售產品的稅率。 計算時 [歐盟稅金](international-tax-guidelines.md#eu-tax-configuration)，確認 [預設稅捐目的地計算](../configuration-reference/sales/tax.md) 每個商店檢視都會對應至「出貨設定」原點。

![來源](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Sales]** 並選擇 **[!UICONTROL Shipping Settings]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Origin]** 區段並完成下列專案：

   - [!UICONTROL Country]
   - [!UICONTROL Region / State]
   - [!UICONTROL ZIP / Postal Code]
   - [!UICONTROL City]
   - [!UICONTROL Street Address] （如有需要，請加入第2行）

1. 按一下 **[!UICONTROL Save Config]**.

## 送貨原則

出貨政策應說明貴公司的商業規則和出貨准則。 例如，如果您有觸發免運費的價格規則，則可以說明出貨政策中的條款。

![結帳時的送貨原則](./assets/storefront-checkout-shipping-policy.png){width="700" zoomable="yes"}

若要在結帳時顯示您的送貨政策，請完成設定中的「送貨政策引數」。 客戶點選時，文字隨即顯示 _請參閱我們的運送政策_ 結帳期間。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Sales]** 並選擇 **[!UICONTROL Shipping Settings]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Shipping Policy Parameters]** 區段。

1. 設定 **[!UICONTROL Apply Custom Shipping Policy]** 至 `Yes`.

1. 貼上或輸入您的 **[!UICONTROL Shipping Policy]** 至文字方塊中。

   >[!NOTE]
   >
   >如果您使用文書處理器來撰寫文字，請確定將檔案儲存為.txt檔案，以移除文字中的任何控制字元。 然後，將文字複製並貼到「出貨政策」文字方塊中。

   ![送貨原則引數](../configuration-reference/sales/assets/shipping-settings-shipping-policy-parameters.png){width="600" zoomable="yes"}

1. 按一下 **[!UICONTROL Save Config]**.

## 多個地址

多個地址出貨選項可讓客戶在結帳時將訂單出貨至多個地址，並決定訂單可出貨的地址數目上限。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Sales]** 並選擇 **[!UICONTROL Multishipping Settings]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Options]** 區段。

   ![多重地址送貨選項](../configuration-reference/sales/assets/multishipping-settings-options.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Allow Shipping to Multiple Addresses]** 至 `Yes`.

1. 輸入 **[!UICONTROL Maximum Qty Allowed for Shipping to Multiple Addresses]**.

1. 按一下 **[!UICONTROL Save Config]**.

>[!NOTE]
>
>![Adobe Commerce B2B](../assets/b2b.svg) (Adobe Commerce B2B)對於具有多個送貨地址的訂單， [分期付款](../b2b/enable-basic-features.md#configure-payment-on-account) 結帳期間無法使用付款方法（即使已啟用）。
