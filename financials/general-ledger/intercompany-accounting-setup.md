---
title: Intercompany accounting setup | Microsoft Docs
description: This topic explains how to set up intercompany accounting so that you can use intercompany journals for ledger allocations and financial journals, such as daily journals, vendor invoice journals, and payment journals.
author: twheeloc
manager: AnnBe
ms.date: 2015-12-03 20:44:04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: LedgerInterCompany
audience: Application User
ms.reviewer: 2231
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 15761
ms.assetid: 26df97b6-f7e6-4280-98a3-2931bb93e07b
ms.region: Global
ms.author: kweekley
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 3c3ff907925ad1e433d18e7b2add626bfd5e42e2


---

# <a name="intercompany-accounting-setup"></a>Intercompany accounting setup

This topic explains how to set up intercompany accounting so that you can use intercompany journals for ledger allocations and financial journals, such as daily journals, vendor invoice journals, and payment journals.

Intercompany journals can be created in various scenarios, such as for daily journals, vendor invoice journals, ledger allocations, and centralized payments. To enable these scenarios, you must set up intercompany accounting.

## <a name="define-main-accounts"></a>Define main accounts
First, you must create the intercompany main accounts to use for the Due to and Due from accounting entries. It's a good idea to use unique main accounts for each company, to simplify the reconciliation and elimination of intercompany accounting entries. If you're using a trading partner or counterpart dimension to identify the intercompany party, you can define this dimension as a fixed dimension on the main account that is defined in Intercompany accounting. When you set up the main accounts, you should set the **Main account type** field to **Balance sheet** on the **Main accounts** page.

## <a name="define-journal-names"></a>Define journal names
Next, you must define a journal name. Set the **Journal type** field to **Daily** on the **Journal names** page. It's a good idea to use a specific journal name for intercompany accounting.

## <a name="define-intercompany-accounting-setup"></a>Define intercompany accounting setup
The **Intercompany accounting** page is used to create the pairs of legal entities that can transact with each other. The Intercompany accounting setup is shared, so the setup is visible from within all legal entities. When creating a new legal entity pair, ensure that you are aware of which legal entity is defined as the originating company versus the destination company. When entering intercompany transactions, the transaction determines which legal entity is initiating or originating the transaction. For example, the intercompany accounting is setup for USMF (originating) and USSI (destination). If a user is active in USSI and enters an intercompany transaction with USMF, the transaction will not post because the intercompany accounting is only defined for USMF being the originator. If either company can originate a transaction, you will need to create a second legal entity pair for the reciprocal setup. Select the **Debit account (Due from)** and **Credit account (Due to)** for both the originating and destination legal entity. Define which **Journal name** will be used when the transaction is created in the destination company. The journal for the originating company is already known because it's selected by the user when creating the intercompany transaction. Finally, select which legal entity will receive the accounting for supporting amounts, such as cash discount or realized gains/losses for centralized payments. A reciprocal relationship can easily be set up on the **Intercompany accounting** page by using the **Create reciprocal relationship** button after the first legal entity pair is created. When the reciprocal pair is created, the information for the destination company is copied to the originating company and vice versa. The journal defined for the destination company will remain. Most organizations use the same naming convention for their journal names, so that the journal name is the same. If the journal name is different, a warning will appear on the field to notify you that the journal doesn't exist and a different journal can be selected.




<!--HONumber=Feb17_HO3-->


