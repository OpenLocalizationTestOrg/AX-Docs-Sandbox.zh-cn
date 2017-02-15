---
title: Customer orders overview | Microsoft Docs
description: This topic provides information about customer orders in Retail Modern POS (MPOS). Customer orders are also known as special orders. The topic includes a discussion of related parameters and transaction flows.
author: josaw1
manager: AnnBe
ms.date: 2016-11-30 21:04:59
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: 41
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 260594
ms.assetid: bf984574-9a7d-43c7-981f-128fb169f729
ms.region: global
ms.industry: Retail
ms.author: anpurush
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: cf6a13f9e685f8f1bd13d84c7f6f146ca2b41b8c


---

# <a name="customer-orders-overview"></a>Customer orders overview

This topic provides information about customer orders in Retail Modern POS (MPOS). Customer orders are also known as special orders. The topic includes a discussion of related parameters and transaction flows.

In an omni-channel retail world, many retailers provide the option of customer orders, or special orders, to meet various product and fulfillment requirements. Here are some typical scenarios:

-   A customer wants products to be delivered to a specific address on a specific date.
-   A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.
-   A customer wants someone else to pick up products that the customer purchased.

Retailers also use customer orders to minimize lost sales that stock outages might otherwise cause, because the merchandise can be delivered or picked up at a different time or place.

## <a name="set-up-customer-orders"></a>Set up customer orders
Here are some of the parameters that can be set on the **Retail parameters** page to define how customer orders are fulfilled:

-   **Default deposit percentage** – Specify the amount that the customer must pay as a deposit before an order can be confirmed. The default deposit amount is calculated as a percentage of the order value. Depending on privileges, a store associate might be able to override the amount by using **Deposit override**.
-   **Cancellation charge percentage** – If a charge will be applied when a customer order is canceled, specify the amount of that charge.
-   **Cancellation charge code** – If a charge will be applied when a customer order is canceled, that charge will be reflected under a charge code on the sales order in Microsoft Dynamics AX. Use this parameter to define the cancellation charge code.
-   **Shipping charge code** – Retailers can charge an extra fee for shipping merchandise to a customer. The amount of that shipping charge will be reflected under a charge code on the sales order in Dynamics AX. Use this parameter to map the shipping charge code to shipping charges on the customer order.
-   **Refund shipping charges** – Specify whether shipping charges that are associated with a customer order are refundable.
-   **Maximum amount without approval** – If shipping charges are refundable, specify the maximum amount of shipping charge refunds across return orders. If this amount is exceeded, manager override is required in order to continue with the refund. To accommodate the following scenarios, a refund of shipping charges can exceed the amount that was originally paid:
    -   Charges are applied at the level of the sales order header, and when some quantity of a product line is returned, the maximum refund of shipping charges that is allowed for the products and the quantity can't be determined in way that works for all retail customers.
    -   Shipping charges are incurred for every instance of shipping. If a customer returns products multiple times, and the retailer’s policy specifies that the retailer will bear the cost of return shipping charges, the return shipping charges will be more than the actual shipping charges.

## <a name="transaction-flow-for-customer-orders"></a>Transaction flow for customer orders
### <a name="create-a-customer-order-in-retail-modern-pos"></a>Create a customer order in Retail Modern POS

1.  Add a customer to the transaction.
2.  Add products to the cart.
3.  Click **Create customer order**, and then select the order type. The order type can be either **Customer order** or **Quote**.
4.  Click **Ship selected** or **Ship all** to ship the products to an address on the customer account, specify the requested shipping date, and specify shipping charges.
5.  Click **Pick up selected** or **Pick-up all** to select products that will be picked up from the current store or a different store on a specific date.
6.  Collect the deposit amount, if a deposit is required.

### <a name="edit-an-existing-customer-order"></a>Edit an existing customer order

1.  On the home page, click **Find an order**.
2.  Find and select the order to edit. At the bottom of the page, click the **Edit**.

### <a name="pick-up-an-order"></a>Pick up an order

1.  On the home page, click **Find an order**.
2.  Select the order to pick up. At the bottom of the page, click **Picking and packing**.
3.  Click **Pick up**.

### <a name="cancel-an-order"></a>Cancel an order

1.  On the home page, click **Find an order**.
2.  Select the order to cancel. At the bottom of the page, click **Cancel**.

#### <a name="create-a-return-order"></a>Create a return order

1.  On the home page, click **Find an order**.
2.  Select the order to return, select the invoice for the order, and then select the product line for the merchandise to return.
3.  At the bottom of the page, click the **Return order**.

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Asynchronous transaction flow for customer orders
Customer orders can be created from the point of sale (POS) client in either synchronous mode or asynchronous mode.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Enable customer orders to be created in asynchronous mode

1.  In Dynamics AX, click **Retail and commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profile** &gt; **Functionality profiles**.
2.  On the **General** FastTab, set the **Create customer order in async mode** option to **Yes**.

When the **Create customer order in async mode** option is set to **Yes**, customer orders are always created in asynchronous mode, even if Retail Transaction Service (RTS) is available. If you set this option to **No**, customer orders are always created in synchronous mode by using RTS. When customer orders are created in asynchronous mode, they are pulled and inserted into Dynamics AX by Pull (P) jobs. The corresponding sales orders are created in Dynamics AX when **Synchronize orders** is run either manually or through a batch process.

<a name="see-also"></a>See also
--------

[Hybrid customer orders](https://docs.microsoft.com/en-us/dynamics365/operations/retail/hybrid-customer-orders)




<!--HONumber=Feb17_HO3-->


