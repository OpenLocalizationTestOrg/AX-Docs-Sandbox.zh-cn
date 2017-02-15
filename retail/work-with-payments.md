---
title: Payment methods in a call center | Microsoft Docs
description: This topic covers the different payment methods you can use in a call center in Retail and commerce.
author: josaw1
manager: AnnBe
ms.date: 2016-06-14 18:34:52
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: 41
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 92163
ms.assetid: d9711edf-54aa-4dad-9414-54cc9d61032f
ms.region: global
ms.industry: Retail
ms.author: josaw
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: bd379495e11a3abc64e2ed086d668ce2a8820532


---

# <a name="payment-methods-in-a-call-center"></a>Payment methods in a call center

This topic covers the different payment methods you can use in a call center in Retail and commerce.

The payment methods that are used in other channels in Retail and commerce in Microsoft Dynamics AX, such as cash, checks, credit cards, and gift cards, can also be used in call centers. After you set up a payment method for a call center, it appears as one of the options in the **Payments** section of the **Sales order** page for call center users. Additionally, you can set up coupons to offer discounts to customers who place an order with your organization’s call center. Coupons can be for a fixed amount discount, or for a percentage of an item price or the order total. For example, an amount-based coupon might offer customers a 75.00 discount when the customer spends 750.00 or more. You can create different types of coupons, set up parent/child coupons, and copy or void a coupon. Use the options  in the following table to create coupons.

|                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Attribute**             | In the **Redemption rate** field, enter the expected redemption rate of the coupon as a percentage, and then select whether the coupon can be used one time use coupon, will be automatically reissued, or is specific to a customer.                                                                                                                                                                                                                                                                                                                                                                                       |
| **Valid**                 | In the **Start date** and **End date** fields, enter the first and last dates that the coupon is valid.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Include/exclude rules** | In the **Catalogs** and **Items** fields, select whether any catalogs or items are included or excluded in the coupon. If you select **Include** or **Exclude**, click **Set up**, select **Include/exclude catalogs** or **Include/exclude products**, and enter information about the catalog or item. If you select **None** in these fields, all catalogs or items are included in the coupon.                                                                                                                                                                                                                          |
| **Miscellaneous**         | If this coupon can’t be used together with other discounts, select the **Exclusive** check box. Then, in the **Origin** field, select where the coupon can be used. If this coupon is a manufacturer’s coupon, select the **Manufacturer coupon** check box.                                                                                                                                                                                                                                                                                                                                                                |
| **Future coupon**         | If this coupon will be associated with other coupons as a parent coupon, select the **Parent coupon** check box. If this coupon should be associated with an existing coupon as a child coupon, select the parent coupon in the **Parent coupon ID** field. For example, you create a coupon for the upcoming spring catalog. All other coupons that you create for the spring catalog will be child coupons of the spring catalog coupon. Child coupons might include a 20-percent discount for new customer orders, a 10-percent discount on a newly released item, or a discount of 95.00 on orders of 1,000.00 or more. |

If you submit a credit card payment from the **Sales order** page and receive a message that states that the card wasn't authorized, you can handle the authorization manually. You can authorize, decline, or resubmit a credit card transaction by using the **Authorization management** page. You use the call center parameters page to configure additional payment processing options:

-   Check holds let finance personnel process orders that have been put on hold because a check was used as the payment method, and the check hold threshold amount was exceeded. The hold can be manually released, or it automatically expires at the end of the configured period.
-   You can set thresholds above which refunds that are issued via checks and credit cards must be manually approved. Any refund that exceeds the threshold amount is added to the approval queue. After you approve the refund, the return sales order can be invoiced.





<!--HONumber=Feb17_HO3-->


