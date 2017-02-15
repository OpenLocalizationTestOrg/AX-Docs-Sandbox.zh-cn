---
title: Physical and financial updates | Microsoft Docs
description: This topic provides an overview of which types of transactions increase or decrease inventory quantities.
author: YuyuScheller
manager: AnnBe
ms.date: 2016-03-31 12:50:59
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: 2094
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 75023
ms.assetid: adaaf068-f1b2-4999-a68a-c57b95919c2e
ms.region: Global
ms.industry: Manufacturing
ms.author: mguada
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: b57d16b871d61183a53606efefb0826493d3b254


---

# <a name="physical-and-financial-updates"></a>Physical and financial updates

This topic provides an overview of which types of transactions increase or decrease inventory quantities. 

Inventory transactions can be physically updated and financially updated in Microsoft Dynamics 365 for Operations. Some types of physical and financial transactions increase inventory quantities, whereas others decrease the quantity.

## <a name="physical-increases"></a>Physical increases
When a physical transaction is posted, the status of the transaction record is **Received**. The following transactions are considered physical increases:

-   Purchase order receipt
-   Sales order packing slip return
-   Reporting a production order as finished
-   By-product on a production order picking list

## <a name="financial-increases"></a>Financial increases
When a financial receipt transaction is posted, the status of the transaction record that increases the quantity is **Purchased**. The following transactions are considered financial increases:

-   Vendor invoice
-   Sales order invoice for a return
-   Production order costing
-   Positive quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer

## <a name="transactions-that-increase-quantity"></a>Transactions that increase quantity
Transactions that increase quantity are posted at the running average cost price. Dynamics 365 for Operations calculates a running average cost price that is based on the cost of each of these transactions for each inventory dimension that is being tracked financially. For information about running average cost prices, see [Running average cost price](https://docs.microsoft.com/en-us/dynamics365/operations/manufacturing/cost-management/running-average-cost-price).

## <a name="transactions-that-decrease-quantity"></a>Transactions that decrease quantity
Dynamics 365 for Operations uses the calculated running average cost price when a transaction that decreases quantity is posted, regardless of the inventory model that is associated with that inventory. The transaction that decreases quantity must not have been marked to another transaction before it was posted. If the physical on-hand inventory becomes negative, Dynamics 365 for Operations uses the inventory cost that is defined for the item on the **Item** page. **Note:** If multisite functionality is enabled, this cost will instead be the inventory cost that is defined for a site on the **Default order settings** page.

## <a name="physical-issues-vs-financial-issues"></a>Physical issues vs. financial issues
When a physical issue transaction is posted, the status of the transaction record is **Deducted**. The following transactions are considered physical issues:

-   Production order picking list journal
-   Sales order packing slip
-   Purchase order packing slip return

When a financial transaction is posted, the status of the transaction record is **Sold**. The following transactions are considered financial issues:

-   Ending a production order
-   Sales order invoice
-   Vendor invoice return
-   Negative quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer

Transactions that decrease quantity are posted at the running average cost price. Therefore, the inventory close procedure is required in order to settle issue transactions to receipt transactions, based on the inventory model that is assigned to each item.




<!--HONumber=Feb17_HO3-->


