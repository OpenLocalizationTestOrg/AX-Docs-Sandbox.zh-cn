---
title: Posting inventory main accounts by site | Microsoft Docs
description: This topic provides information about the posting of inventory main accounts by site for China.
author: ShylaThompson
manager: AnnBe
ms.date: 2016-12-12 22:49:48
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: InventPostingParameters
audience: Application User
ms.reviewer: 81
ms.suite: Released- Dynamics 365 for Operations version 1611
ms.custom: 262754
ms.assetid: e43f0736-9e0a-46fb-8552-f365df9dfb42
ms.region: China (PRC)
ms.author: leguo
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: ba7902e5a37419e6860c8aa4a1e2661a8c1a8bf6


---

# <a name="posting-inventory-main-accounts-by-site"></a>Posting inventory main accounts by site

This topic provides information about the posting of inventory main accounts by site for China.

You can set up or modify the posting of items to ledger accounts, based on item groups and warehouse sites for inventory transactions. By setting up ledger accounts of inventory value by site, you can post inventory transactions for each site. These transactions include inventory journals, sales orders, purchase orders, production journals, and project item journals. The site-related fields are available on the **Transaction combinations** and **Posting** pages only if the **Separate ledger accounts of inventory value by sites** option is set to **Yes** on the **Inventory and warehouse management parameters** page. You must determine the value of your inventory items to determine on-hand inventory, taxable amount on inventory, and opening and closing balances for inventory receipts and issues during a specific reporting period. You can create main accounts for inventory. Alternatively, you can select the main accounts that show the value of your inventory for inventory item groups that can be used for inventory posting. You can calculate the inventory value for an item group from the corresponding main account. For example, you can create a main account for the Raw materials item group to track its inventory value.
| Main account | Item group    | Balance    |
|--------------|---------------|------------|
| 15067        | Bulbs         | 10,721,065 |
| 15065        | Raw materials | 6,299,398  |

Organizations that stock more than 100 inventory items and also maintain several sites must organize their main accounts by both site and item group. For example, an organization can have more than one site, and each site can have multiple groups of items. In the following table, you can view the inventory value of the Bulbs item group for site 1 and the inventory value of the Raw materials item group for site 2.
| Main account | Item group    | Site   | Balance   |
|--------------|---------------|--------|-----------|
| 15080        | Bulbs         | Site 1 | 5,721,065 |
| 15085        | Raw materials | Site 2 | 3,299,398 |

By setting up main accounts for inventory values by site, you can post inventory transactions, such as inventory journals, sales orders, purchase orders, production journals, and project item journals, for each site.




<!--HONumber=Feb17_HO3-->


