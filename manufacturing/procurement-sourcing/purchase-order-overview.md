---
title: Purchase order overview | Microsoft Docs
description: This article provides general information about purchase orders (POs) and links to additional articles that are related to the various stages that a PO goes through.
author: YuyuScheller
manager: AnnBe
ms.date: 2016-06-16 14:19:08
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: PurchTable
audience: Application User
ms.reviewer: 2084
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 93083
ms.assetid: 897d3c03-13e4-4b74-a8de-e159996d6531
ms.region: Global
ms.author: fdahl
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 2503ae2f844b88bd2806ec0cd1542cdfd1550827


---

# <a name="purchase-order-overview"></a>Purchase order overview

This article provides general information about purchase orders (POs) and links to additional articles that are related to the various stages that a PO goes through.

A purchase order (PO) is a document that represents an agreement with a vendor to buy goods or services. The document also helps keep track of product receipts that are made toward the order and, later, the accounting of vendor invoices that the vendor bills toward the order. The **Purchase orders** page contains an overview of the available orders and lets you modify those orders. When you open a PO, you can select the **Header** view, which contains information that is specified only one time for each PO, such as the vendor details. Alternatively, you can select the **Lines** view, where you can modify order lines. Typically, you will switch between these two views as you modify POs. Charges aren't listed directly on the **Purchase orders** page, but are accessed via menus on the order header and lines. There are many reports where you can view information about POs, product receipts, and vendor invoices. These reports are found in the **Procurement and sourcing** and **Accounts payable** modules. The **Purchase order preparation** and **Purchase order receipt and follow-up** workspaces let you view lists of POs in the various states that they have progressed to. They also provide a summary of the actions that must be taken. The **Purchase order preparation** workspace is focused on PO creation and review, processing of the order through approval, and confirmation with the vendor. The **Purchase order receipt and follow-up** workspace is focused on processing the receipt of goods or services against POs. It includes lists that give insight into receipts that are overdue, or that will soon be due for delivery by the supplier. These workspaces aren't used to perform the related receipt activities that are done in the warehouse. Those activities are performed by using pages in the **Inventory management** and **Warehouse management** modules. Processing of vendor invoices should be done by using the **Vendor invoice entry** workspace, and payments should be done by using the **Vendor payments** workspace. The following articles provide an overview of the various stages that a PO goes through:

-   [Purchase order creation](https://docs.microsoft.com/en-us/dynamics365/operations/manufacturing/procurement-sourcing/purchase-order-creation)
-   [Purchase order approval and confirmation](https://docs.microsoft.com/en-us/dynamics365/operations/manufacturing/procurement-sourcing/purchase-order-approval-and-confirmation)
-   [Product receipt against purchase orders](https://docs.microsoft.com/en-us/dynamics365/operations/manufacturing/procurement-sourcing/product-receipt-against-purchase-orders)
-   [Overview of vendor invoices](https://docs.microsoft.com/en-us/dynamics365/operations/financials/accounts-payable/vendor-invoices-overview)

## <a name="types-of-purchase-orders"></a>Types of purchase orders
There are three types of POs. When you create a PO, you must specify the type. You can set up a default order type for new orders on the **Procurement and sourcing parameters** page.

| PO type        | Description                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Journal        | Use this type to create a draft order. This type doesn't affect stock quantities or generate inventory transactions. The PO journal lines aren't included in master scheduling.                                                                                                       |
| Purchase order | Use this type to create POs when orders are confirmed with a vendor, and as the orders are processed through receipt and invoicing before payment is made to the vendor. This type of PO is the most common.                                                                          |
| Returned order | Use this type when you return goods to the vendor. This type of order requires that you specify the return material authorization (RMA) number that the vendor gives you. You specify the RMA number on the **General** tab of the PO. The order lines must have negative quantities. |

## <a name="purchase-order-statuses"></a>Purchase order statuses
POs include several status fields that indicate the progress of the order. All these fields are visible in the **Header** view of the order, and a few of them are also visible in the grid overview of all orders. The **Status** field show the status for quantities on the order. The following values are available:

-   **Open order** – Orders have been created, and quantities are on order.
-   **Received** – Some of the quantities have been received, but they haven't been invoiced yet.
-   **Invoiced** – The full quantity on the order has been invoiced. **Note:** If an order has been *partially* invoiced, neither **Received** status nor **Invoiced** status is appropriate. Therefore, the order will still have a status of **Open order**.
-   **Canceled** – An order was confirmed but later canceled. Therefore, this status indicates that there are no longer any open quantities on order.

The **Document status** field helps you quickly review the order's progress in terms of documents that have been processed. It shows the status of the most recent document that has been completed for the order. The following values are available:

-   **None** – No document has been processed for the order yet.
-   **Purchase inquiry** – A purchase inquiry has been generated, and the order is awaiting feedback from the vendor.
-   **Purchase order** – Confirmation has been processed on the order.
-   **Product receipt** – Product receipt has been processed on the order.
-   **Invoice** – An invoice has been accounted with the order.

The **Approval status** field is used when a PO goes through a review process or workflow. The following values are available:

-   **Draft**, **In review**, and **Rejected** – These statuses are used only when an approval workflow is used for the PO.
-   **Approved** – This status is assigned to orders that have completed workflow approval. Orders that are created without using an approval workflow receive a status of **Approved** immediately.
-   **In external review** – This status is used in scenarios where a purchase inquiry is sent to the vendor, so that the vendor can confirm terms of the PO. This status is also used in the process that is initiated by the **Confirmation request** action. For this process, the vendor is asked to confirm terms of the PO by connecting to your system and registering whether it confirms or rejects the order.
-   **Confirmed** – This status is assigned after the order has been confirmed. Typically, this status is the last approval status that is assigned to an order.


<a name="see-also"></a>See also
--------

[Purchase order creation](https://docs.microsoft.com/en-us/dynamics365/operations/manufacturing/procurement-sourcing/purchase-order-creation)

[Purchase order approval and confirmation](https://docs.microsoft.com/en-us/dynamics365/operations/manufacturing/procurement-sourcing/purchase-order-approval-and-confirmation)

[Product receipt against purchase orders](https://docs.microsoft.com/en-us/dynamics365/operations/manufacturing/procurement-sourcing/product-receipt-against-purchase-orders)

[Overview of vendor invoices](https://docs.microsoft.com/en-us/dynamics365/operations/financials/accounts-payable/vendor-invoices-overview)




<!--HONumber=Feb17_HO3-->


