---
title: Settlement overview | Microsoft Docs
description: This article provides general information about the settlement process. It describes the types of transactions that can be settled, when and how transactions can be settled, and the results of the settlement process.
author: twheeloc
manager: AnnBe
ms.date: 2015-12-02 23:32:42
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 14551
ms.assetid: 34ca575b-f1e8-49b2-8e24-fc53e393eb8e
ms.region: Global
ms.author: kweekley
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 9bbaef24f3b09a5b1fa26e4a97f7dfaff03a0a47


---

# <a name="settlement-overview"></a>Settlement overview

This article provides general information about the settlement process. It describes the types of transactions that can be settled, when and how transactions can be settled, and the results of the settlement process.

During settlement, the transactions on one document are applied to the transactions on another document to increase or decrease the balance of each document. For example, a payment can be applied to an invoice. Various transaction types can be settled, at different times, and through various methods. Settlement can also cause new transactions to be generated.

## <a name="what-transactions-can-be-settled"></a>What transactions can be settled
Settlement within Accounts payable and Account receivable can occur between any transaction types that affect the vendor balance or customer balance, such as invoices, payments, credit memos, and fees. Any transaction type can be settled against any other transaction type. For example, you can settle a payment against an invoice, a credit memo against an invoice, an invoice against an invoice, and a payment against a payment. You can settle payments against a transaction in the same legal entity or in a different legal entity. In organizations that use a centralized payment model, [cross-company settlements](http://ax.help.dynamics.com/en/wiki/about-cross-company-payment-settlements/) can help streamline the payment process.

## <a name="when-to-settle-transactions"></a>When to settle transactions
Transactions can be settled at the time of payment entry. For example, when you make a payment to a vendor, you typically select the invoices to pay. By selecting invoices, you mark them for settlement against the payment. When Accounts Receivable payment clerks record a customer payment, they can mark the appropriate invoices for settlement, based on the information that is included with the customer's payment. The **Settle transactions** page is used to mark transactions for settlement. This page can be opened from any unposted invoice or payment. When the transaction is posted, the settlement is also posted. Transactions can also be settled after they are posted. You can enter and post a customer payment without settling it against any invoices. However, you might have to do research first, to make sure that the payment is settled against the correct invoice. The **Settle transactions** page can be opened from the **All customers** or **All vendors** page, or from the **Transactions** page for any customer or vendor. You can also reserve posted prepayments for an invoice by marking the payment for settlement against a purchase order or sales order. In this case, the payment will still have an open balance, but it can't be settled against another invoice. The payment will be automatically settled against the invoice that is created from the purchase order or sales order.

## <a name="how-to-settle-transactions"></a>How to settle transactions
Transactions can be settled manually, automatically, or by using a combination of the two methods. The choice of a settlement method depends on business processes, which can then be implemented through the setup of settlement in Accounts payable parameters and Accounts receivable parameters. You can create vendor payments and customer direct debit payments by using a payment proposal, which is used to select invoices to pay. The payment proposal is manually initiated, but then Microsoft Dynamics 365 for Operations automatically marks the selected invoices for settlement when the payments are created. If payments are created manually, you can use the **Settle transactions** page to select invoices for settlement. You can manually select the invoices, or you can use the **Mark by priority** option to have invoices automatically marked for settlement. The **Mark by priority** option is available only for Accounts receivable. To enable this option, use the **Settlement priority** page in Accounts receivable parameters. If a payment clerk enters a payment, but doesn’t settle that payment before he or she posts it, the payment can be automatically settled. You can enable automatic settlement in Accounts receivable parameters and Accounts payable parameters. When you use automatic settlement, you can use the predefined settlement order, or you can define your own settlement priority order in Accounts receivable parameters. This functionality is available only for Accounts receivable.

## <a name="results-of-settlement"></a>Results of settlement
As transactions are settled, the outstanding balance of each transaction is increased or decreased as appropriate. In a typical scenario, where an invoice and payment are settled, the status and balance of each transaction is updated according to the following rules:

-   If the payment amount is more than the invoice amount, the invoice balance is reduced to 0.00, and the invoice is closed. The payment remains open, and the balance is the amount by which the payment exceeds the invoice amount.
-   If the payment amount is less than the invoice amount, the payment balance is reduced to 0.00, and the payment is closed. The invoice remains open, and the balance is the amount by which the payment underpaid the invoice.
-   If the payment amount equals the invoice amount, both the payment and the invoice are closed, and the balance of both is 0.00.

If a [payment is less than the invoice amount](https://docs.microsoft.com/en-us/dynamics365/operations/financials/accounts-payable/vendor-payments-for-a-partial-amount) because of a cash discount, write-off, or underpayment, the invoice and payment might still be closed, depending on the setup of settlement in Accounts payable parameters and Accounts receivable parameters. Settlement can also generate transactions. For example, the settlement of an invoice and payment might produce a cash discount, realized gain or loss, sales tax adjustments, write-offs, or penny differences.




<!--HONumber=Feb17_HO3-->


