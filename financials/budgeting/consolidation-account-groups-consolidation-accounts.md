---
title: Consolidation account groups and additional consolidation accounts | Microsoft Docs
description: This topic provides information about consolidation account groups and additional consolidation accounts, and explains how they are used in Microsoft Dynamics 365 for Operations.
author: RobinARH
manager: AnnBe
ms.date: 2017-01-03 19:31:01
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: 101
ms.suite: Released- Dynamics 365 for Operations version 1611
ms.custom: 265544
ms.assetid: 7c7cbd8d-7776-473b-a075-6f9b755d37a1
ms.region: Global
ms.author: aolson
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 9276d891ae6f4b62346a112b996032c723b91efe


---

# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a>Consolidation account groups and additional consolidation accounts

This topic provides information about consolidation account groups and additional consolidation accounts, and explains how they are used in Microsoft Dynamics 365 for Operations.

<a name="consolidation-account-groups"></a>Consolidation account groups
----------------------------

Consolidation account groups let you create groups of the accounts that you want to use to consolidate data. Most often, a consolidation account group represents a government-mandated chart of accounts or maps accounts to a group that is defined by the company's headquarters. You can find consolidation account groups in the **Setup** area of the **Consolidations** module. When you add a new group, you enter a unique identifier for the account group and a name.

## <a name="additional-consolidation-accounts"></a>Additional consolidation accounts
Additional consolidation accounts let you assign an account from an existing chart of accounts to a consolidation account group. You can then specify a consolidation account value and name. You can find additional consolidation accounts in the **Setup** area of the **Consolidations** module. When you create a new consolidation account, you must specify the following information:

-   **Main account** – This field is a lookup that shows all the main accounts that are based on the chart of accounts that you selected on the page. When you select an account, the name is automatically entered in the **Main account name** field.
-   **Consolidation account group** – Use this field to specify the group to assign the account to. If you consolidate in two different ways, you must add the same account to all four consolidation account groups. Here is an example. [![Additional consolidation accounts](./media/additionalconsolidationaccountswiki.png)](./media/additionalconsolidationaccountswiki.png)
-   **Consolidation account** – Enter the value of the consolidation account. This value doesn't have to be an account from a chart of accounts. It can be any value that you require.
-   **Consolidation account name** – Enter the name of account as you want it to appear on inquiries and reports.
-   **SAT level** – This field is used to report account statements to the Mexican tax authorities. For more information, see [Electronic ledger accounting statements](https://docs.microsoft.com/en-us/dynamics365/operations/financials/localizations/latin-america/electronic-ledger-accounting-statements-in-mexico).

When you've finished creating your consolidation account groups and additional consolidation accounts, you can select the group in the Consolidate online process.

<a name="see-also"></a>See also
--------

[Consolidation and elimination overview](https://docs.microsoft.com/en-us/dynamics365/operations/financials/budgeting/consolidation-and-elimination-overview)




<!--HONumber=Feb17_HO3-->


