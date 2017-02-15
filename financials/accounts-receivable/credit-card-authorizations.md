---
title: Credit card setup, authorization, and capture | Microsoft Docs
description: This article provides an overview of credit card authorization in Microsoft Dynamics AX. It includes information about how to set up a payment service, add a credit card to a sales order, and void an authorization.
author: twheeloc
manager: AnnBe
ms.date: 2015-09-10 20:19:25
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: CreditCardProcessors, CustTable, SalesTable
audience: Application User
ms.reviewer: twheeloc
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 3041
ms.assetid: 94916cf8-e964-4733-ac72-b02961b451b8
ms.region: Global
ms.author: mfalkner
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 22d997b1b93b63bd37268782a3a5b384a7d6d5b2


---

# <a name="credit-card-setup-authorization-and-capture"></a>Credit card setup, authorization, and capture

This article provides an overview of credit card authorization in Microsoft Dynamics AX. It includes information about how to set up a payment service, add a credit card to a sales order, and void an authorization.

<a name="setting-up-the-credit-card-payment-service"></a>Setting up the credit card payment service
------------------------------------------

To use credit cards, you must set up and activate a payment service on the Payment services page. A payment service acts as a bridge between your legal entity and the bank that processes a customer's credit card charges. You must work with a credit card provider that is listed in the Payment connector field and set up an account with that provider. You must then set up the other options on the Payment services page, set up credit card types for American Express, Discover, MasterCard, and Discover on the Credit card types page, and activate the provider as the default provider. You must also follow these steps to complete your setup:
-   On the Accounts receivable parameters page, specify parameters for using credit card authorizations.
-   On the Terms of payment page, set up payment terms for credit cards. In the Payment type field, select Credit card.
-   On the Customer credit cards page, enter credit card information for customers.

## <a name="adding-a-new-credit-card"></a>Adding a new credit card
You can create new credit card records on the Customers page by using Customer, Set up, Credit card. You can also create credit card records when you enter sales orders on the Sales order page, by using Manage, Customer, Credit card, Register.
Adding a credit card to a sales order
-------------------------------------

You can add a credit card to a sales order by selecting a credit card in the credit card lookup on the Price and discounts FastTab on the Sales order page. To start the authorization process, on the Action Pane, on the Manage tab, select Credit card and Authorize.
Authorizing a credit card
-------------------------

When a credit card is authorized, the card number and cardholder's name are verified, and the available credit balance is confirmed. Optionally, the card verification value and the cardholder’s address are verified. The customer's available credit balance is then reduced by the amount of the invoice. The payment service sends information that the credit card has been approved or declined. When the sales order is invoiced, the credit card is charged (captured) for the invoice amount.

### <a name="card-verification-value"></a>Card verification value

You can require the card verification value, which is sometimes referred to as the card's security code. For American Express, this is a four-digit value. For Discover, MasterCard, and Visa, it is a three-digit value.

### <a name="address-verification"></a>Address verification

Address verification information is always sent to the payment provider. You can decide how much information is required for a transaction to be accepted. Be sure to check with your provider to determine whether it accepts this information. Here are the options for address verification:
-   **Always accept transaction** – Accept the transaction, regardless of address verification results.
-   **Account holder** – Compare the cardholder's name from the transaction with the credit card company’s information.
-   **Billing address** – Compare the cardholder's name and billing address from the transaction with the credit card company’s information.
-   **Billing postal code** – Compare the cardholder's name, billing address, and postal code from the transaction with the credit card company’s information.

## <a name="data-support"></a>Data support
For each credit card type that is supported, you can specify the level of data support. The level controls how much information about a transaction is transferred to the payment service. Be sure to check with your provider to determine whether it can provide this information. Here are the options for the level of data support:
-   **Level 1** – Transfer the transaction date, transaction amount, and description.
-   **Level 2** – Transfer all Level 1 information, plus the shipping and merchant addresses, and tax information.
-   **Level 3** – Transfer all Level 2 information, plus order line information.

## <a name="partial-payments"></a>Partial payments
If you ship part of an order, the amount of the partial order is captured, and the authorization, which was for the amount of the whole order, is closed. A new authorization is then submitted for the remaining amount of the order that hasn't been shipped.

## <a name="voiding-an-authorization"></a>Voiding an authorization
To void a credit card authorization, you can change the method of payment to another method that doesn't have a type of Credit card.






<!--HONumber=Feb17_HO3-->


