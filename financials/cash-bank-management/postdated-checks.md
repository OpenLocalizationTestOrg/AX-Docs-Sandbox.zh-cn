---
title: Postdated checks | Microsoft Docs
description: This article provides information about support for postdated checks in Microsoft Dynamics 365 for Operations. Postdated checks are checks that are issued to make and receive payments on a future date. Therefore, the check can&quot;t be cashed until the specified date.
author: ShylaThompson
manager: AnnBe
ms.date: 2015-12-11 15:16:27
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: ShylaThompson
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 21741
ms.assetid: 1bbf1338-1e92-4ed9-929d-8010bfb898b3
ms.region: Global
ms.author: leguo
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 825b39db2ca8317a0fed2e4802787738bd65692b


---

# <a name="postdated-checks"></a>Postdated checks

This article provides information about support for postdated checks in Microsoft Dynamics 365 for Operations. Postdated checks are checks that are issued to make and receive payments on a future date. Therefore, the check can't be cashed until the specified date.

Microsoft Dynamics 365 for Operations supports the full management cycle for postdated checks in both Accounts receivable and Accounts payable, as shown in the following table.

**Scenario**

**Details**

Set up postdated checks.

You must set up a new payment method, and specify the payment routine for clearing accounts for issued checks, received checks, and withholding tax.

Register and post a postdated check for a vendor.

Register the details of a postdated check that you issue to a vendor. When the payment is posted, the vendor liability is recognized, but the bank account isn't yet credit. Instead, a clearing account is used for this purpose.

Register and post a postdated check for a customer.

Register the details of a postdated check that you receive from a customer. When the payment is posted, the customer receivable is credit, but the bank account isn't yet debit. Instead, a clearing account is used for this purpose.

Register and post a replacement postdated check for a customer or a vendor.

If your original check to a vendor or from a customer is lost or damaged, you can issue a replacement postdated check. When you register the check details, provide a reference to the original check, and indicate that the new check is a replacement for the original. You can also post the replacement check.

Transfer a customer postdated check to a vendor.

When you receive a postdated check from a customer, you can transfer that check to a vendor as a payment.

Settle a postdated check for a customer or a vendor.

Settle a postdated check that is posted to a bridging account for a customer or a vendor when the check finally matures. When the check is settled, the bank is finally debit or credit against the clearing account that was used earlier.

Cancel a postdated check for a vendor.

You can cancel a posted postdated check in these situations:

-   The check is returned by the bank.
-   The check is applied to an incorrect invoice.
-   A cash payment is made against the check.

Stop payment for a postdated check.

You can stop payment on a postdated check that was issued to a vendor, for reasons such as not sufficient funds, changes in the terms of the agreement with the vendor, supply of defective goods by the vendor, or return of goods to the vendor. You can stop payment only on checks that haven't cleared.

You can cancel a posted postdated check in these situations:

-   The check is returned by the bank.
-   The check is applied to an incorrect invoice.
-   A cash payment is made against the check.

Stop payment for a postdated check.You can stop payment on a postdated check that was issued to a vendor, for reasons such as not sufficient funds, changes in the terms of the agreement with the vendor, supply of defective goods by the vendor, or return of goods to the vendor. You can stop payment only on checks that haven't cleared.




<!--HONumber=Feb17_HO3-->


