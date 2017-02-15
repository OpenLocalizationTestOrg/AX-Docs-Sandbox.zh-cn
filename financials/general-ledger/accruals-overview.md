---
title: Accruals overview | Microsoft Docs
description: This article describes accruals, and provides information about how to set them up and create transactions.
author: RobinARH
manager: AnnBe
ms.date: 2015-12-02 23:07:47
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: LedgerAccuralTable
audience: Application User
ms.reviewer: RobinARH
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 14131
ms.assetid: 5d402d68-b548-4e00-bfaf-0b837ab4815f
ms.region: Global
ms.author: aolson
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: ba2ffe021a35083dab852bac96994fe167b8f8d5


---

# <a name="accruals-overview"></a>Accruals overview

This article describes accruals, and provides information about how to set them up and create transactions.

Accruals are used in accrual accounting to track revenue that is recognized in the period that it's earned in, not when payment is received, and to track expenses (costs) that are recognized when they occur, not when payment is made.

## <a name="accrual-schemes"></a>Accrual schemes
Accrual schemes are used to set up the deferred revenue and costs, and the same accrual scheme can be used for both revenue and costs. Ledger accruals redistribute the costs or revenue of a journal line so that the costs and revenues are recognized in the appropriate periods. On the **Accrual scheme** page, you specify the debit and the credit accounts that will be used when the accrual scheme is applied.

-   **Debit** – The main account that you define will replace the debit main account on the journal voucher line. This account will also be used for the reversal of the deferral, based on the ledger accrual transactions.
-   **Credit** – the main account that you define will replace the credit main account on the journal voucher line. This account will also be used for the reversal of the deferral, based on the ledger accrual transactions.

After you determine which accounts to use, you can specify how the voucher number is created when accrual transactions are created. You can also specify how often the transactions occur, the number of times that the transactions are created, and when the transactions are posted. After the accrual scheme has been created, you can use it in some of the journals by using the Ledger accruals function.

## <a name="ledger-accruals"></a>Ledger accruals
When you enter a journal, you can click **Ledger accruals** on the **Functions** menu. Then, when you select the accrual scheme, you will see the base amount from the journal that will be spread over the period, as determined by the accrual scheme. For example, if you pay an employee's insurance for the whole year in January, and the amount is 12,000, you must recognize that expense each month. You can select the start date. You can also specify whether the amount that is accrued is based on the account or the offset account. After you make your selections, click **Transactions** to view all the transactions that have been created based on the accrual scheme. For example, if you spread the 12,000 in insurance expenses over the year, you will see 1,000 for each month. After you post the journal, you can view the transactions by using the **Voucher transactions** inquiry page. If an accrual scheme can't be applied (for example, when a sales order invoice or purchase order invoice is involved), you can credit the prepaid amount and debit the expense amount. You can then select **Offset** when you apply the accrual scheme.




<!--HONumber=Feb17_HO3-->


