---
title: 價格顯示設定
description: 瞭解目錄、購物車、訂單、商業發票以及支援客戶購買體驗的銷退折讓單中稅捐的顯示方式。
exl-id: 6f97c474-ef6e-4ca6-899d-812c58b993ca
feature: Checkout, Invoices, Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---

# 價格顯示設定

價格顯示設定可決定產品與送貨價格是否包含或排除稅捐，或顯示兩個版本的價格；一個含稅，另一個不含稅捐。

如果產品價格包含稅捐，則只有當有符合稅捐來源的稅捐規則，或客戶地址符合稅捐規則時，才會顯示稅捐。 可觸發比對的事件包括：客戶建立帳戶、登入，或從購物車產生稅金和運費估計時。

>[!IMPORTANT]
>
>顯示含稅與不含稅的價格，可能會讓客戶感到困惑。 若要避免觸發警告訊息，請參閱您所在國家的[指南](international-tax-guidelines.md)以及[避免警告訊息的建議設定](taxes.md#warning-messages)。

![價格顯示設定](../configuration-reference/sales/assets/tax-price-display-settings.png){width="600" zoomable="yes"}

如需這些組態設定的詳細說明，請參閱&#x200B;_組態參考指南_&#x200B;中的[價格顯示設定](../configuration-reference/sales/tax.md#price-display-settings)。

## 設定價格顯示設定

稅捐、稅率和類別的計算組態完成時，稅捐會根據這些設定進行計算。 不過，目錄、購物車、訂單、發票和銷退折讓單中的稅捐顯示也應該設定為支援店面的客戶體驗。

最佳實務是顯示價格和相關稅捐（包括稅捐，或同時包括稅捐與排除稅捐），讓客戶在下訂單前瞭解這些計算的套用方式。

### 步驟1：設定目錄價格顯示設定

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Sales]**&#x200B;並選擇&#x200B;**[!UICONTROL Tax]**。

1. 展開&#x200B;**[!UICONTROL Price Display Settings]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

1. 針對&#x200B;**[!UICONTROL Display Product Prices in Catalog]**，選擇下列其中一項：

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

   >[!NOTE]
   >
   >如果您將此選項設為`Including Tax`，則只有在有符合稅捐來源的稅捐規則，或有符合稅捐規則的客戶地址時，才會顯示稅捐。 可觸發比對的事件包括客戶帳戶建立、登入，或在購物車中使用稅務和送貨預估工具。

1. 針對&#x200B;**[!UICONTROL Display Shipping Prices]**，選擇下列其中一項：

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

如果您選擇同時顯示兩個價格（含稅與不含稅），店面外觀會類似於以下畫面：

![價格顯示範例，包括店面的稅捐](./assets/catalog-prices-tax.png){width="700" zoomable="yes"}

### 步驟2：設定購物車顯示設定

1. 展開&#x200B;**[!UICONTROL Shopping Cart Display Settings]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![購物車顯示設定](../configuration-reference/sales/assets/tax-shopping-cart-display-settings.png){width="600" zoomable="yes"}

1. 針對&#x200B;**[!UICONTROL Display Prices]**，選擇下列其中一項：

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. 針對&#x200B;**[!UICONTROL Display Subtotal]**，選擇下列其中一項：

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. 針對&#x200B;**[!UICONTROL Display Shipping Amount]**，選擇下列其中一項：

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)針對&#x200B;**[!UICONTROL Display Gift Wrapping Prices]**，選擇下列其中一項：

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)針對&#x200B;**[!UICONTROL Display Printed Card Prices]**，選擇下列其中一項：

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. 針對其餘各個選項，根據您的偏好設定切換至`Yes`或`No`：

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

### 步驟3：設定訂單、商業發票及銷退折讓單顯示設定

1. 展開&#x200B;**[!UICONTROL Orders, Invoices, Credit Memos Display Settings]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![訂單、發票、銷退折讓單顯示設定](../configuration-reference/sales/assets/tax-orders-invoices-credit-memos-display-settings.png){width="600" zoomable="yes"}

1. 針對&#x200B;**[!UICONTROL Display Prices]**，選擇下列其中一項：

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. 針對&#x200B;**[!UICONTROL Display Subtotal]**，選擇下列其中一項：

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. 針對&#x200B;**[!UICONTROL Display Shipping Amount]**，選擇下列其中一項：

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)針對&#x200B;**[!UICONTROL Display Gift Wrapping Prices]**，選擇下列其中一項：

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)針對&#x200B;**[!UICONTROL Display Printed Card Prices]**，選擇下列其中一項：

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. 針對其餘各個選項，根據您的偏好設定切換至`Yes`或`No`：

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。
