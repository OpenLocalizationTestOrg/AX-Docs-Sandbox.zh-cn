---
title: Settle a partial vendor payment that has multiple discount periods | Microsoft Docs
description: This article walks you through a scenario where multiple partial payments are made to a vendor that offers multiple cash discounts.
author: twheeloc
manager: AnnBe
ms.date: 2015-12-02 23:20:28
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 14262
ms.assetid: edffd08f-d7f3-4888-822d-9ad3c8578f9c
ms.region: Global
ms.author: kweekley
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: ab4e1b4bb555bf651a760848d821a77890f91af7


---

# <a name="settle-a-partial-vendor-payment-that-has-multiple-discount-periods"></a>Settle a partial vendor payment that has multiple discount periods

This article walks you through a scenario where multiple partial payments are made to a vendor that offers multiple cash discounts. 

Vendor 3054 offers Fabrikam a cash discount of 2 percent if an invoice is paid in five days and a cash discount of 1 percent if the invoice is paid in 14 days.

## <a name="invoice"></a>Invoice
On June 28, April creates an invoice for 1,000.00 for vendor 3054. April can view this transaction on the **Vendor transactions** page.

| Voucher   | Date      | Invoice | Amount in transaction currency debit | Amount in transaction currency credit | Balance   | Currency |
|-----------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| Inv-10060 | 6/28/2015 | 10060   |                                      | 1,000.00                              | -1,000.00 | USD      |

The following cash discount dates and amounts are available for this invoice.

| Cash discount date | Cash discount amount | Amount in transaction currency |
|--------------------|----------------------|--------------------------------|
| 7/3/2015           | 20.00                | 980.00                         |
| 7/12/2015          | 10.00                | 990.00                         |
| 7/25/2015          | 0.00                 | 1,000.00                       |

## <a name="payment-on-july-2"></a>Payment on July 2
On July 2, April wants to pay 300.00 against this invoice. She creates a one-off payment by using the **Payment journal** page in Accounts payable. She adds a line for vendor 3054 and enters a payment amount of **300.00**. April then opens the **Settle transactions** page, so that she can mark the invoice that will be settled. She updates the value in the **Amount to settle** field to **300.00** and notices that the value in the **Cash discount amount to take** field is changed to **6.12**. Because this payment is made in the first discount period, a discount of 2 percent is taken.

| Mark | Use cash discount | Voucher   | Account | Date      | Due date  | Invoice | Amount in transaction currency | Currency | Amount to settle |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Normal            | Inv-10060 | 3054    | 6/28/2015 | 7/28/2015 | 10060   | 1,000.00                       | USD      | 300.00           |

Discount information appears at the bottom of the **Settle open transactions** page.

|                              |           |
|------------------------------|-----------|
| Cash discount date           | 7/02/2015 |
| Cash discount amount         | -20.00    |
| Use cash discount            | Normal    |
| Cash discount taken          | 0.00      |
| Cash discount amount to take | -6.12     |

Because a cash discount is available, April wants to change the payment amount so that the total settled amount is 300.00 for both the payment and the cash discount. She changes the value in the **Amount to settle** field to **294.00** and notices that the value in the **Cash discount amount to take** field is changed to **6.00**.

| Mark | Use cash discount | Voucher   | Account | Date      | Due date  | Invoice | Amount in transaction currency | Currency | Amount to settle |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Normal            | Inv-10060 | 3054    | 6/28/2015 | 7/28/2015 | 10060   | 1,000.00                       | USD      | 294.00           |

Discount information appears at the bottom of the **Settle open transactions** page.

|                              |           |
|------------------------------|-----------|
| Cash discount date           | 7/02/2015 |
| Cash discount amount         | -20.00    |
| Use cash discount            | Normal    |
| Cash discount taken          | 0.00      |
| Cash discount amount to take | -6.00     |

April posts the payment. On the **Vendor transactions** page, she can view the transactions. She sees that 300.00 has been applied to the invoice. This amount includes a discount of 6.00. Therefore, the remaining balance is 700.00.

| Voucher    | Date      | Invoice | Amount in transaction currency debit | Amount in transaction currency credit | Balance | Currency |
|------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10060  | 6/28/2015 | 10060   |                                      | 1,000.00                              | -700.00 | USD      |
| APP-10060  | 7/2/2015  |         | 294.00                               |                                       | 0.00    | USD      |
| DISC-10060 | 7/2/2015  |         | 6.00                                 |                                       | 0.00    | USD      |

## <a name="payment-on-july-8"></a>Payment on July 8
On July 8, April makes an additional payment against the invoice. To enter the amount, she opens the **Settle transactions** page and then clicks the **Cash discount** tab. She sees the dates and amounts for the two cash discounts that are available. Because this payment is made in the second discount period, a discount of 1 percent, or 5.00, is available. This amount is calculated as half the 1-percent discount on 1,000.00, or half of 10.00.

| Cash discount date | Cash discount amount | Amount in transaction currency |
|--------------------|----------------------|--------------------------------|
| 7/3/2015           | 20.00                | 680.00                         |
| 7/12/2015          | 10.00                | 690.00                         |
| 7/25/2015          | 0.00                 | 700.00                         |

April decides to pay 495.00 and take the 5.00 cash discount. Therefore, the total amount that is settled is 500.00.

| Mark | Use cash discount | Voucher   | Account | Date      | Due date  | Invoice | Amount in transaction currency | Currency | Amount to settle |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Normal            | Inv-10060 | 3054    | 6/28/2015 | 7/28/2015 | 10060   | 1,000.00                       | USD      | 495.00           |

Discount information appears at the bottom of the **Settle open transactions** page.

|                              |           |
|------------------------------|-----------|
| Cash discount date           | 7/12/2015 |
| Cash discount amount         | -10.00    |
| Use cash discount            | Normal    |
| Cash discount taken          | -6.00     |
| Cash discount amount to take | -5.00     |

On the **Vendor transactions** page, April sees that the new balance is 200.00.

| Voucher    | Date      | Invoice | Amount in transaction currency debit | Amount in transaction currency credit | Balance | Currency |
|------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10060  | 6/28/2015 | 10060   |                                      | 1,000.00                              | -200.00 | USD      |
| APP-10060  | 7/2/2015  |         | 294.00                               |                                       | 0.00    | USD      |
| DISC-10060 | 7/2/2015  |         | 6.00                                 |                                       | 0.00    | USD      |
| APP-10061  | 7/12/2015 |         | 495.00                               |                                       | 0.00    | USD      |
| DISC-10061 | 7/12/2015 |         | 5.00                                 |                                       | 0.00    | USD      |

## <a name="payment-on-july-20"></a>Payment on July 20
On July 20, April creates a final payment for 200.00. No discount is taken, because the payment is made after both discount periods. The balance for the invoice is 0.00.

| Voucher    | Date      | Invoice | Amount in transaction currency debit | Amount in transaction currency credit | Balance | Currency |
|------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10060  | 6/28/2015 | 10060   |                                      | 1,000.00                              | -200.00 | USD      |
| APP-10060  | 7/2/2015  |         | 294.00                               |                                       | 0.00    | USD      |
| DISC-10060 | 7/2/2015  |         | 6.00                                 |                                       | 0.00    | USD      |
| APP-10061  | 7/12/2015 |         | 495.00                               |                                       | 0.00    | USD      |
| DISC-10061 | 7/12/2015 |         | 5.00                                 |                                       | 0.00    | USD      |
| APP-10062  | 7/20/2015 |         | 200.00                               |                                       | 0.00    | USD      |






<!--HONumber=Feb17_HO3-->


