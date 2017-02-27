---
title: Balanced journals for interunit accounting
description: This article shows how a journal is automatically balanced when a balancing financial dimension is selected on the Ledger page.
author: twheeloc
manager: AnnBe
ms.date: 2015-12-03 20 - 52 - 10
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.dyn365.ops.intro: 01-02-2016
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 2d152b536e0001acd6b26e962039f86deecb7aea
ms.lasthandoff: 02/22/2017


---

# <a name="balanced-journals-for-interunit-accounting"></a>Balanced journals for interunit accounting

This article shows how a journal is automatically balanced when a balancing financial dimension is selected on the Ledger page. 

If account entries don't balance at the level of the financial dimension values, additional account entries are created automatically to balance the journal. These account entries use the **Interunit - debit** and **Interunit - credit** posting types on the **Accounts for automatic transactions** page to determine the main account. For example, Branch, which is the second segment of the ledger account, is selected as the balancing financial dimension, and the following accounting entries are about to be created.

|                      |           |
|----------------------|-----------|
| 6100 – MSP – OU\_256 | 100.00 DR |
| 6100 – NY – OU\_249  | 100.00 DR |
| 2100 – MSP – OU\_256 | 200.00 CR |

In this case, the following balances are determined:

-   For Branch MSP = 100.00 CR
-   For Branch NY = 100.00 DR

Therefore, the following accounting entries are created automatically to balance the  journal at the level of the financial dimension values.

|                                   |           |
|-----------------------------------|-----------|
| (Interunit Debit) – MSP – OU\_256 | 100.00 DR |
| (Interunit Credit) – NY – OU\_249 | 100.00 CR |




