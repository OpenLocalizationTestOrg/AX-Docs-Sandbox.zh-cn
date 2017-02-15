---
title: Packing materials and fees | Microsoft Docs
description: Packing material fees are paid to a recycling company at certain intervals. An amount is paid, per unit of weight, for each material that a packing unit consists of. Packing material fees are calculated and reported, but no ledger transactions are posted because the fees are not regarded as taxes to be paid to an authority.
author: YuyuScheller
manager: AnnBe
ms.date: 2015-09-10 08:12:45
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: InventPackagingGroup, InventPackagingMaterialCode, InventPackagingMaterialFee, InventPackagingMaterialTrans, InventPackagingMaterialTransPurch, InventPackagingUnit
audience: Application User
ms.reviewer: 2084
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 2194
ms.assetid: b92f7a17-7f14-4b14-928e-9daa675f982b
ms.region: Global
ms.industry: Distribution
ms.author: mafoge
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: f9d61a750211a5c42834c886a31dec6b6b5f3a25


---

# <a name="packing-materials-and-fees"></a>Packing materials and fees

Packing material fees are paid to a recycling company at certain intervals. An amount is paid, per unit of weight, for each material that a packing unit consists of. Packing material fees are calculated and reported, but no ledger transactions are posted because the fees are not regarded as taxes to be paid to an authority.

Packing material weights and fees are calculated for sales order lines and for purchase order lines.

You can define one or more packing units for an item, for a packing group of items, or for all items. A packing unit consists of the packing materials, their weights, and the number of items that are included in the packing unit. A packing material code is assigned to each type of packing material that is defined. Based on the packing material code, you can specify a price for a specified period. The packing material fee is calculated based on this information.
| **Note**                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Even if your company does not pay packing material fees, you can use the functionality to calculate statistics for the weights of packing materials. |

## <a name="setup-requirements-for-packing-material-fees"></a>Setup requirements for packing material fees
Before you calculate packing material weights or packing material fees, or both, you must create the following base data:

-   Packing groups – Create packing groups to assign to items.
-   Packing material codes – Create packing material codes for each type of packing material that is defined.
-   Packing units – Specify a packing unit for an item, for a packing group, or for all items. For each packing unit, define which packing materials to include, assign weights, and, in the Packing unit factor field, enter the conversion factor from the inventory unit.
-   Packing material fees – Specify packing material fees per packing material code. For each type of material, define the period of validity, the price per material, the currency, and the unit.

## <a name="packing-units-on-sales-order-lines"></a>Packing units on sales order lines
When you create a sales order line, the system checks to see whether packing units are specified for the item. If packing units are specified, the system updates the sales order line with the specified packing unit and the packing unit quantity. The packing unit quantity is based on the ordered quantity divided by the number of items in the selected packing unit. If a packing unit has not been specified, you can manually enter a packing unit and a packing unit quantity on the sales order line. You can also change the packing unit and the packing unit quantity when you post the sales order line. This is relevant if the sales order line is only partly delivered or partly invoiced. When you invoice the sales order, packing material transactions are created. Packing material transactions contain the weights of the packing materials for the sales line. You can also modify the transactions after you invoice them, and then create new transactions.

## <a name="packing-units-on-purchase-order-lines"></a>Packing units on purchase order lines
Packing material transactions for a purchase order line are not created by the system. You create transactions for invoiced purchase order lines manually in the **Packing material transactions** page.

## <a name="set-up-customer-packagingmaterialfee-license-numbers"></a>Set up customer packagingmaterialfee license numbers
If the customers pay the packaging material fees, specify the customers' packaging-material-fee license numbers in the **Customers** page. When a license number has been assigned to a customer, the packaging material fees are calculated automatically when sales orders are invoiced. After invoicing, the **Calculate fee** check box is cleared in the **Packing material transactions** page, because you do not have to calculate and print a report. You can print the packaging material weights on the invoice, and inform the customers that they pay the fees. If your company pays the packaging material fees, do not specify the customer license numbers. After invoicing, the **Calculate fee** check box is selected in the **Packing material transactions** page. This indicates that the fees are calculated when a report is created. You can print the weights on the invoice, and indicate that your company pays the fees.
Print packaging material weights on invoices
--------------------------------------------

You can print the packaging material weights on the invoice, and indicate who pays the packaging material fees. The weights are summarized by packaging code.
 
-






<!--HONumber=Feb17_HO3-->


