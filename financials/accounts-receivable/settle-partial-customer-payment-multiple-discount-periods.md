---
title: Settle a partial customer payment that has multiple discount periods | Microsoft Docs
description: This article shows how partial customer payments are settled when there are multiple discount periods.
author: twheeloc
manager: AnnBe
ms.date: 2015-12-02 23:29:40
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 14471
ms.assetid: 1714e2f0-3202-448d-9567-ca93942f0c46
ms.region: Global
ms.author: kweekley
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 2de38752fbef79763b11acdf729b97211cb413e0


---

# <a name="settle-a-partial-customer-payment-that-has-multiple-discount-periods"></a>Settle a partial customer payment that has multiple discount periods

This article shows how partial customer payments are settled when there are multiple discount periods.

Fabrikam offers customer 4031 two cash discount periods. The customer receives a 2-percent cash discount if the invoice is paid in five days and a 1-percent cash discount if the invoice is paid in 14 days. Fabrikam also offers cash discounts on partial payments. The [settlement parameters](http://ax.help.dynamics.com/en/?p=246884) are located on the **Accounts receivable parameters** page.

## <a name="invoice"></a>Invoice
On June 25, Arnie enters and posts an invoice for 1,000.00 for customer 4031. When he reviews the cash discounts for this invoice, Arnie sees that customer 4031 receives a 20.00 discount if the invoice is paid by June 30. If the invoice is paid by July 9, the customer receives a 10.00 discount.

| Cash discount date | Cash discount amount | Amount in transaction currency |
|--------------------|----------------------|--------------------------------|
| 6/30/2015          | 20.00                | 980.00                         |
| 7/9/2015           | 10.00                | 990.00                         |
| 7/25/2015          | 0.00                 | 1,000.00                       |

Arnie can view this transaction on the **Customer transactions** page.

| Voucher   | Transaction type | Date      | Invoice | Amount in transaction currency debit | Amount in transaction currency credit | Balance  | Currency |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10030 | Invoice          | 6/25/2015 | 10030   | 1,000.00                             |                                       | 1,000.00 | USD      |

## <a name="partial-payment-before-the-cash-discount-date"></a>Partial payment before the cash discount date
On June 28, Customer 4031 makes a partial payment of 294.00. Because June 28 is within the first cash discount period, the customer takes a 6.00 discount. On the **Settle transactions** page, the **Cash discount amount** value is 20.00, and the **Cash discount amount to take** value is 6.00.

| Mark     | Use cash discount | Voucher   | Account | Date      | Due date  | Invoice | Amount in transaction currency | Currency | Amount to settle |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Selected | Normal            | FTI-10030 | 4031    | 6/25/2015 | 7/25/2015 | 10030   | 1,000.00                       | USD      | 294.00           |

Discount information appears at the bottom of the **Settle open transactions** page. If you don't change the **Amount to settle** value to **294.00**, the **Cash discount amount** values that appear will differ. However, 6.00 will be taken as the cash discount when the payment is posted, because settlement automatically adjusts the **Amount to settle** value for you.

|                              |           |
|------------------------------|-----------|
| Cash discount date           | 6/30/2015 |
| Cash discount amount         | 20.00     |
| Use cash discount            | Normal    |
| Cash discount taken          | 0.00      |
| Cash discount amount to take | 6.00      |

After Arnie posts the payment, the invoice balance is 700.00.

## <a name="partial-payment-before-the-second-cash-discount-date"></a>Partial payment before the second cash discount date
On July 8, the customer pays the rest of the invoice amount. A 7.00 discount (1 percent) is taken, because the payment was made within the second cash discount period.

| Mark     | Use cash discount | Voucher   | Account | Date      | Due date  | Invoice | Amount in transaction currency debit | Amount in transaction currency credit | Currency | Amount to settle |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Selected | Normal            | FTI-10030 | 4031    | 6/25/2015 | 7/25/2015 | 10030   | 700.00                               |                                       | USD      | 693.00           |

Discount information appears at the bottom of the **Settle open transactions** page.

|                              |           |
|------------------------------|-----------|
| Cash discount date           | 7/09/2015 |
| Cash discount amount         | 30.00     |
| Use cash discount            | Normal    |
| Cash discount taken          | 6.00      |
| Cash discount amount to take | 7.00      |

The invoice balance is now 0.00. Arnie views the information on the **Customer transactions** page.

| Voucher    | Transaction type | Date      | Invoice | Amount in transaction currency debit | Amount in transaction currency credit | Balance | Currency |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10030  | Invoice          | 6/25/2015 | 10030   | 1,000.00                             |                                       | 0.00    | USD      |
| ARP-10030  |  Payment         | 6/28/2015 |         |                                      | 294.00                                | 0.00    | USD      |
| DISC-10030 |  Cash discount   | 6/28/2015 |         |                                      | 6.00                                  | 0.00    | USD      |
| ARP-10031  |  Payment         | 7/8/2015  |         |                                      | 693.00                                | 0.00    | USD      |
| DISC-1031  |  Cash discount   | 7/8/2015  |         |                                      | 7.00                                  | 0.00    | USD      |






<!--HONumber=Feb17_HO3-->


