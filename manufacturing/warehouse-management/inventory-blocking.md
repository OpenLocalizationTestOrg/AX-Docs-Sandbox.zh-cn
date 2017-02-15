---
title: Inventory blocking | Microsoft Docs
description: This article provides an overview of inventory blocking, which is part of the quality inspection process in Microsoft Dynamics AX. You can use inventory blocking to prevent items from being processed or consumed.
author: YuyuScheller
manager: AnnBe
ms.date: 2015-09-10 08:05:55
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: InventBlocking, InventQualityOrderTable
audience: Application User
ms.reviewer: 2084
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 2094
ms.assetid: 81232769-a82f-4860-a438-91ff63a3e834
ms.region: Global
ms.industry: Distribution
ms.author: perlynne
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 22f59b03e86d18eb6365afac19f6092f9bb331ec


---

# <a name="inventory-blocking"></a>Inventory blocking

This article provides an overview of inventory blocking, which is part of the quality inspection process in Microsoft Dynamics AX. You can use inventory blocking to prevent items from being processed or consumed.

You can block inventory items in the following ways:
-   Manually
-   By creating a quality order
-   By using a process that generates a quality order
-   By using inventory status blocking

## <a name="blocking-items-manually"></a>Blocking items manually
You can block a quantity of an item by creating a transaction on the **Inventory blocking** page. Only items that are available as on-hand inventory can be blocked manually. For manually blocked quantities, you must decide whether planning activities include expected receipts as an expected on-hand quantity. Expected receipts are blocked items that you expect to be available as on-hand inventory after inspection is completed. You can maintain the expected date. By default, the **Expected receipts** option is selected for items that are blocked through a quality order. You can cancel a manual block on a quantity by deleting the transaction on the **Inventory blocking** page.
Blocking items by creating a quality order
------------------------------------------

You can specify items that must be inspected by creating a quality order on the **Quality orders** page. When you create a quality order, the quantity that you specify for an item is blocked. The sampling plan that is associated with a quality order controls only the quantity of items that must be inspected, not the quantity that is blocked. The quantity that is entered on the quality order is the quantity that is blocked, regardless of the quantity that the sampling plan specifies should be sent for inspection.

## <a name="blocking-items-by-using-a-process-that-generates-a-quality-order"></a>Blocking items by using a process that generates a quality order
If a quality process specifies that an item must be inspected, a quantity of the item is blocked automatically. Therefore, when a quality order is generated automatically, the item sampling plan that is associated with the quality order controls the both quantity of items that is blocked and the quantity that must be inspected. If the **Full blocking** option on the **Item sampling** page is selected, the full quantity of, for example, a purchase order line is blocked during inspection, regardless of the item sampling quantity.
### <a name="example"></a>Example

In the following example, a quality order is generated when a purchase order packing slip is posted. On the **Quality associations** page, you specified that posting of a purchase order packing slip is the process that activates a quality order.
| Setup                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | User action                 | Result                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A quality association specifies that a quality order must be generated when a purchase order packing slip is posted. The item sampling setup of the quality order specifies that 10 percent of the quantity on the purchase order line must be inspected. Furthermore, because the **Full blocking** option selected in the item sampling setup, the full quantity of the purchase order line must be blocked during inspection, regardless of the quantity that is sent for inspection. | The packing slip is posted. | A quality order is generated. Ten percent of the purchase order quantity for the item is sent to inspection. The full quantity of the purchase order line is blocked. |

## <a name="blocking-items-by-using-inventory-status-blocking"></a>Blocking items by using inventory status blocking
You can specify which inventory statuses are blocking statuses by using the **Inventory blocking** parameter on the **Inventory statuses** page. You can't use inventory statuses as blocking statuses for production orders, sales orders, transfer orders, outbound transactions, or project integrations. For outbound work, use items that have an available inventory status. If items have a status of **Broken**, and master planning is run on those items, the items are considered missing, and inventory is automatically replenished.



<a name="see-also"></a>See also
--------

[Create and maintain an inventory blocking](https://ax.help.dynamics.com/en/wiki/create-and-maintain-an-inventory-blocking/)

[Quality management processes](https://docs.microsoft.com/en-us/dynamics365/operations/manufacturing/inventory-management/quality-management-processes)

[Inspect the quality of goods](https://ax.help.dynamics.com/en/wiki/inspect-the-quality-of-goods/)




<!--HONumber=Feb17_HO3-->


