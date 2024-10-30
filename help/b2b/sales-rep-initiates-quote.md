---
title: Initiate quote for a buyer
description: Learn how a seller can create a quote for a specific buyer to start the negotiation process. The seller can submit quotes only for customers associated with a company account on the selected website.
exl-id: 7bbb281f-7b6a-45fa-b906-da314d159bc8
feature: B2B, Quotes
role: Admin, User
source-git-commit: 69396421bae610ff02b12054bdea2278a8c0efe5
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# Initiate a Quote for a Buyer

[](configure-quotes.md)

- Draft quotes are visible only to the seller.
- Draft quotes cannot be submitted until the sales representative adds items, relevant discounts, and notes to create the initial offer for the buyer.
- A seller can create a quote from the Quotes or Customer Grid.

The Sales Representative sends the quote to the buyer to initiate the negotiation process. [](quote-price-negotiation.md)

## Sales representative quote creation experience

A Sales Representative can create a quote from the Quotes or Customer Grid.

>[!NOTE]
>
>[](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/b2b/b2b-quote/sales-rep-initiates-quote.html)__

### Create a quote from the Quote grid

1. [](../systems/permissions.md)

1. [!UICONTROL Quotes]**[!UICONTROL Sales]****[!UICONTROL Quotes]**

1. Create a quote for a buyer.

   - **[!UICONTROL Create New Quote]**

     ![](./assets/quote-draft-from-admin.png){width="700" zoomable="yes"}

   - [!UICONTROL Create New Quote]

     ![](./assets/quote-draft-from-admin-select-buyer.png){width="700" zoomable="yes"}

     `Draft`

     ![](./assets/quote-create-by-seller.png){width="700" zoomable="yes"}

   - Update the quote name and modify the expiration date as needed.

   - Save the quote as a draft.

## Prepare the quote for the buyer

After creating the draft quote, add product items, apply discounts, and communicate with the buyer by adding comments and any related files to the quote. Then, send the quote to the buyer for review, or save it as a draft.

1. **[!UICONTROL Add Product By SKU]****[!UICONTROL Add Product]**

   ![](./assets/quote-draft-add-items.png){width="675" zoomable="yes"}

1. Apply line item discounts to products as needed.

   - [!UICONTROL Select]**[!UICONTROL Discount Item]**

   - [!UICONTROL Discount Line item]**[!UICONTROL Discount Type]**

     ![](./assets/quote-discount-line-item.png){width="675" zoomable="yes"}

   - [!UICONTROL Discount]For example, if you selected a percentage discount, enter 10 to apply a 10% discount to the line item.

   - Optionally, lock the line item discount value so that the product price is not further reduced by any discounts applied at the quote level.

     After confirming the change, the line item attributes in the product grid update to show the discount amount applied. If the discount is locked, a lock icon displays.

   A Sales Representative can request a discount from a specific line item in a quote.

   >[!NOTE]
   >
   >[](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/b2b/b2b-quote/quote-line-item-discount.html)__

1. Apply a quote-level discount as needed:

   - [!UICONTROL Quote Totals - Negotiated Price]

     ![](./assets/quote-draft-total-discount.png){width="700" zoomable="yes"}

   The product grid updates to show the discount.

1. Add additional information for the buyer.

   **[!UICONTROL Negotiation - Comments]**

   ![](./assets/quote-draft-add-info-for-buyer.png){width="700" zoomable="yes"}

   [](configure-quotes.md)

1. Add shipping address during negotiations.

   A Sales Representative can make a shipping and delivery selection once the buyer has added a shipping address to the quote.

   Shipping options are locked on checkout.

   [](account-dashboard-my-quotes.md#adding-a-shipping-address)

1. Process the quote.

   Save the quote as a draft, or send it to the buyer.

   - `Draft`

   - `Submitted`The buyer receives an email notification to review the quote. The quote is locked until the buyer returns it for further negotiation. The seller can view the quote from the Quote grid or the Customer grid.

## View and create quotes from Customer Grid

1. [!UICONTROL Customer]**[!UICONTROL Customers]****[!UICONTROL All Customers]**

1. Select the customer ID for a Company buyer.

   ![](./assets/quote-view-customer-quotes.png){width="700" zoomable="yes"}

1. **[!UICONTROL Edit]**

1. **[!UICONTROL Create Quote]**

1. **[!UICONTROL Quotes]**

   ![](./assets/quote-list-from-customer-information.png){width="700" zoomable="yes"}

1. **[!UICONTROL View]**

[](quote-price-negotiation.md)
