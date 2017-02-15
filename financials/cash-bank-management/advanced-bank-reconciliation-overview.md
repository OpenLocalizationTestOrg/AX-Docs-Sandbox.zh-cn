---
title: Advanced bank reconciliation overview | Microsoft Docs
description: This article describes the flow for the advanced bank reconciliation process. The advanced bank reconciliation feature lets you import bank statements that can be automatically reconciled from within bank transactions.
author: ShylaThompson
manager: AnnBe
ms.date: 2015-12-11 21:23:46
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: BankReconciliationMatchRule
audience: Application User
ms.reviewer: ShylaThompson
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 22104
ms.assetid: 7ef18920-240d-4f70-a2c8-fe1b40c2f9fa
ms.region: Global
ms.author: leguo
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: b6044cdb54e78107ddb7326c76bcdca8d03fc35f


---

# <a name="advanced-bank-reconciliation-overview"></a>Advanced bank reconciliation overview

This article describes the flow for the advanced bank reconciliation process. The advanced bank reconciliation feature lets you import bank statements that can be automatically reconciled from within bank transactions.

The advanced bank reconciliation feature lets you import bank statements. The imported bank statement can then be automatically reconciled from within bank transactions. Here are the steps in the advanced bank reconciliation flow.

1.  Set up a bank statement import.
    -   Import bank statements through the data entity framework.
    -   Three typical bank statement formats are built in: ISO20022, BAI2, and MT940.
    -   The functionality can be extended to any format.

2.  Set up a number sequence to use for advanced bank reconciliation, and define the bank reconciliation matching rules.
    -   A reconciliation matching rule is a set of criteria that are used to filter bank statement lines and Microsoft Dynamics 365 for Operations bank transaction lines during the reconciliation process. Depending on your business practice, you can set up more than one matching rule to automate and optimize your reconciliation process.

3.  Reconcile bank statements with Dynamics 365 for Operations bank transactions.
    -   Perform automatic matching and creation of reconciliation journals.
    -   View bank statements and Dynamics 365 for Operations bank transactions side by side.
    -   Automatically post Dynamics 365 for Operations bank transactions if they appear on a bank statement but don't appear in Dynamics 365 for Operations.
    -   Generate a reconciliation statement.






<!--HONumber=Feb17_HO3-->


