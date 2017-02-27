---
title: Close the general ledger at period end
description: This topic describes the tasks that are typically completed when performing a period closing for General ledger.
author: RobinARH
manager: AnnBe
ms.date: 2015-12-02 23 - 07 - 25
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.dyn365.ops.intro: 01-02-2016
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 12721c75bc2f3ec2d66069d394d7ebc18b31dacd
ms.lasthandoff: 02/22/2017


---

# <a name="close-the-general-ledger-at-period-end"></a>Close the general ledger at period end

This topic describes the tasks that are typically completed when performing a period closing for General ledger. 

In General ledger, you can complete closing procedures for a period or a year. Closing processes prepare the system for a new period. To prepare the system for a new year, you must run the year end close process. Each organization has different processes and steps that it performs for the end of a period. Here are some optional steps for period ends:

-   Complete all the tasks for all other modules, such as Accounts receivable, Accounts payable, and Inventory.
-   Verify that all journals are posted.
-   Run foreign currency revaluation to generate any unrealized gain or loss amounts.
-   Settle transactions for each ledger account.
-   Process any required allocations.
-   Manually post period-end adjustments.
-   Journalize transactions, and review the **Ledger journal** report.
-   Perform a consolidation by using a consolidation company or Financial reporting.
-   Generate period-end financial statements by using Financial reporting.
-   Set ledger periods to **On hold**, so that no further posting occurs. You can also restrict a period to a specific user group while period-end activities are occurring, for better control. It's not a good idea to set periods to **Permanently closed**, because you can't reopen a period that has been closed.

The Financial period close workspace can be used to organize and track the tasks required for various period end processes. Refer to the [Financial period close workspace](financial-period-close-workspace.md)topic for additional information.

<a name="see-also"></a>See also
--------

[Year end close](https://ax.help.dynamics.com/en/?post_type=incsub_wiki&p=246674)


