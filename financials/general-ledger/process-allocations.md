---
title: Process allocations | Microsoft Docs
description: This article provides information about allocations, the options for processing them in Microsoft Dynamics 365 for Operations, and how they can be used in budget planning. Allocations are used to distribute amounts across multiple ledger account combinations. They help guarantee that expenses or revenue is charged to the correct object in accounting.
author: twheeloc
manager: AnnBe
ms.date: 2015-12-04 18:16:59
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: annbe
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 17361
ms.assetid: fa66ad75-91d4-4d3a-a55b-01a6da069b95
ms.region: Global
ms.author: peakerbl
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 1ee402b8f60ea4822e83b3cef45140c57ea6425d


---

# <a name="process-allocations"></a>Process allocations

This article provides information about allocations, the options for processing them in Microsoft Dynamics 365 for Operations, and how they can be used in budget planning. Allocations are used to distribute amounts across multiple ledger account combinations. They help guarantee that expenses or revenue is charged to the correct object in accounting.

Microsoft Dynamics 365 for Operations provides the following capabilities to support this process:

-   Manually allocate transaction amounts by using the Split action in accounting distributions, or by applying financial dimension default templates to a document. For more information, see [Accounting distributions.](https://docs.microsoft.com/en-us/dynamics365/operations/financials/accounts-payable/accounting-distributions)
-   Automatically allocate transactions amounts based on allocation terms defined on individual main account. Allocation account entries will be generated for each journal based on the percentage and destination ledger account whenever an accounting entry meets the criteria defined as the source ledger account.
-   Automatically allocate ledger balances or fixed amounts based on ledger allocation rules. The ledger allocation rules are processed on a periodic basis using allocation journals. For more information, see [Ledger allocation rules](http://ax.help.dynamics.com/en/wiki/about-allocation-rules/).

###  <a name="allocations-in-budget-planning"></a>Allocations in budget planning

Ledger allocation rules can be used for budget plans. When you use ledger allocation rules in budget planning, the allocation rules work the same way they would in the ledger, but the source data and destination data comes from the budget plan. You can manually select ledger allocation rules to use for budget plans. Alternatively, you can use an allocation schedule that runs as part of a workflow process.

|                                                                         |
|-------------------------------------------------------------------------|
| **Note**                                                                |
| You can’t use intercompany ledger allocation rules for budget planning. |






<!--HONumber=Feb17_HO3-->


