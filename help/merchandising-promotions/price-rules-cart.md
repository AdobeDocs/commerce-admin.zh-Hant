---
title: 購物車價格規則
description: 瞭解根據一組條件對購物車中的專案套用折扣的購物車價格規則。
exl-id: f3038f2a-9d34-4696-a39e-f87fbb1294a2
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%

---

# 購物車價格規則

購物車價格規則會根據一組條件，將折扣套用至購物車中的專案。 當滿足條件或客戶輸入有效優惠券代碼時，可自動套用折扣。 套用時，折扣會顯示在小計下的購物車中。 如有需要，可以透過變更其狀態和日期範圍，將購物車價格規則用於季節或促銷活動。

>[!NOTE]
>
>如果優惠券購物車規則具有指定結帳選項的條件，例如特定送貨或付款方法，則只有在選取特定送貨/付款方法後，才符合結帳條件。 在這種情況下，可在最後一步的結帳時套用抵用券。

![店面範例 — 購物車套用優惠券](./assets/storefront-cart-apply-coupon.png){width="600" zoomable="yes"}

## 存取購物車價格規則

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rules]**.

   ![購物車價格規則](./assets/price-rule-cart.png){width="700" zoomable="yes"}

1. 如果您有許多規則，請使用每欄頂端的篩選選項來簡化清單，然後按一下 **[!UICONTROL Search]** 以套用篩選器。

1. 若要清除所有篩選選項並顯示完整清單，請按一下 **[!UICONTROL Reset Filter]**.

1. 更新規則的屬性：

   - ![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)按一下 **[!UICONTROL Edit]** 以顯示「規則資訊」頁面。

   - ![Magento Open Source](../assets/open-source.svg) (僅限Magento Open Source)按一下清單中的規則，以顯示「規則資訊」頁面。

   您可以在此處變更規則的設定（類似於建立規則）。

## 依欄篩選選項

| 欄 | 說明 |
|--- |--- |
| [!UICONTROL ID] | 輸入文字以篩選特定規則識別碼編號的清單。 |
| [!UICONTROL Rule] | 輸入文字，以根據建立規則時定義的規則名稱來篩選清單。 |
| [!UICONTROL Coupon Code] | 輸入文字，以根據建立規則時定義的程式碼名稱來篩選清單。 |
| [!UICONTROL Priority] | 根據為規則定義的優先順序篩選清單的自由文字欄位。 |
| [!UICONTROL Status] | 使用此選項可依據規則狀態來篩選清單(`Active` 或 `Inactive`)。 |
| [!UICONTROL Web Site] | 使用此選項可依據針對規則定義的網站來篩選清單。 |
| [!UICONTROL Action] | ![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)按一下 **[!UICONTROL Edit]** 以顯示 _[!UICONTROL Rule Information]_並更新規則設定（類似於建立規則）。 |
| [!UICONTROL Start] | ![Magento Open Source](../assets/open-source.svg) (僅限Magento Open Source)使用動態行事曆欄位(_[!UICONTROL To:]_和_[!UICONTROL From:]_)，以根據建立規則時定義的規則開始日期來篩選清單。 |
| [!UICONTROL End] | ![Magento Open Source](../assets/open-source.svg) (僅限Magento Open Source)使用動態行事曆欄位(_[!UICONTROL To:]_和_[!UICONTROL From:]_)，以根據建立規則時定義的規則結束日期來篩選清單。 |

{style="table-layout:auto"}

## 使用Real-Time CDP受眾來通知購物車價格規則

瞭解如何 [啟用](../customers/audience-activation.md) 將Real-Time CDP對象放入您的Adobe Commerce例項，以告知購物車價格規則。
