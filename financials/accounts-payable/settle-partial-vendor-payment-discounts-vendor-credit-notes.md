---
title: Settle a partial vendor payment that has discounts on vendor credit notes | Microsoft Docs
description: This article walks you through a scenario where a credit memo is settled against an invoice.
author: twheeloc
manager: AnnBe
ms.date: 2015-12-02 23:15:32
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 14222
ms.assetid: bccc5562-7c09-44cd-b2d1-0845a2e0b822
ms.region: Global
ms.author: kweekley
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: c93e75f1914ca7a00da954572b75d4d0f9520495


---

# <a name="settle-a-partial-vendor-payment-that-has-discounts-on-vendor-credit-notes"></a>Settle a partial vendor payment that has discounts on vendor credit notes

This article walks you through a scenario where a credit memo is settled against an invoice.

Fabrikam’s vendors give cash discounts on credit notes. Vendor 3050 lets Fabrikam take a cash discount of 1 percent if an invoice is paid in 14 days.

## <a name="invoice-and-credit-memo"></a>Invoice and credit memo
On June 29, April creates an invoice for 1,000.00 for vendor 3050. On July 2, she creates a credit note for 200.00. From the **Vendors** page, April opens the **Settle transactions** page. She can use the **Settle transactions** page to mark both the credit note and the invoice for settlement. A discount of 2.00 is calculated on the credit note. Therefore, the total value of the credit note is reduced to 198.00.

| Mark                     | Use cash discount | Voucher   | Account | Date      | Due date  | Invoice | Amount in transaction currency | Currency | Amount to settle |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Selected                 | Normal            | Inv-10070 | 3050    | 6/29/2015 | 7/29/2015 | 10070   | -1,000.00                      | USD      | -990.00          |
| Selected and highlighted | Normal            | CR-10070  | 3050    | 7/2/2015  | 7/29/2015 |         | 200.00                         | USD      | 198.00           |

Discount information for the credit note appears at the bottom of the **Settle open transactions** page.

|                              |           |
|------------------------------|-----------|
| Cash discount date           | 7/13/2015 |
| Cash discount amount         | 2.00      |
| Use cash discount            | Normal    |
| Cash discount taken          | 0.00      |
| Cash discount amount to take | 2.00      |

April clicks **Post**. She then reviews the completed settlement. April sees that 198.00 of the credit note was applied, and a discount of 2.00 was taken. Therefore, the total is 200.00.

| Mark                     | Use cash discount | Voucher   | Account | Date      | Due date  | Invoice  | Amount in transaction currency | Currency | Amount to settle |
|--------------------------|-------------------|-----------|---------|-----------|-----------|----------|--------------------------------|----------|------------------|
| Selected and highlighted | Normal            | Inv-10070 | 3050    | 6/29/2015 | 7/29/2015 | 10070    | -1,000.00                      | USD      | -200.00          |
| Selected                 | Normal            | CR-10070  | 3050    | 7/2/2015  | 7/29/2015 | CR-10070 | 200.00                         | USD      | 198.00           |

April can review the vendor transactions on the **Vendor transactions** page by selecting a vendor on the **All vendors** page and then, on the Action Pane, click **Transactions**. On this page, April sees that the invoice has a balance of -800.00. She also sees a credit note for 198.00 and a discount of 2.00.

| Voucher    | Transaction type | Date      | Invoice | Amount in transaction currency debit | Amount in transaction currency credit | Balance | Currency |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10070  | Invoice          | 6/29/2015 | 10070   |                                      | 1,000.00                              | -800.00 | USD      |
| Inv-10071  |                  | 7/2/2015  | CR10071 | 200.00                               |                                       | 0.00    | USD      |
| DISC-10071 |  Cash discount   | 7/2/2015  |         | 2.00                                 |                                       | 0.00    | USD      |
| DISC-10071 |  Cash discount   | 7/2/2015  |         |                                      | 2.00                                  | 0.00    | USD      |






<!--HONumber=Feb17_HO3-->


