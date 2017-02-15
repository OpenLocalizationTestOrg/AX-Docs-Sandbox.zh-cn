---
title: Inventory statuses | Microsoft Docs
description: This article describes how you can use inventory statuses to categorize and keep track of inventory.
author: YuyuScheller
manager: AnnBe
ms.date: 2015-12-09 14:54:45
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: EcoResStorageDimensionGroup, WHSInventStatus
audience: Application User
ms.reviewer: 2084
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 21331
ms.assetid: 731d88e2-9680-448b-b589-31e1480362c2
ms.region: Global
ms.author: mafoge
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 0a6159317fe23442e2b4ea43931cee2a731ac4e0


---

# <a name="inventory-statuses"></a>Inventory statuses

This article describes how you can use inventory statuses to categorize and keep track of inventory.

You can use inventory statuses to categorize inventory. You can then initiate appropriate actions, such as replenishment or put-away work. Here are some examples of ways that you can use inventory statuses:

-   Create inventory statuses for on-hand inventory, inbound transactions, and outbound transactions.
-   Specify a default inventory status for warehouse transactions.
-   Change an inventory status for items before arrival, during arrival, or when the items are put away during inventory movement.
-   Use an inventory status to price items that are returned and to plan item coverage during master planning.

An inventory status is one of the dimensions in the storage dimension group. Inventory statuses can be categorized as available or unavailable, and you can use the **Inventory blocking** parameter to block items that have an unavailable inventory status. Items that have a blocked status are considered physical inventory, and they can't be used on a production order, sales order, transfer order, or outbound transaction. You can use warehouse items that have either available or unavailable inventory statuses for inbound work. For example, you create an available status that is named **Ready**, an unavailable status that is named **Damaged**, and a blocked status that is named **Blocked**. When you create a purchase order for received or returned items, if any items are damaged or broken, you can change the inventory status of those items to **Damaged** on the purchase order line. After these items are received, the status is automatically set to **Blocked**. If you scan the damaged items by using a mobile device, Microsoft Dynamics 365 for Operations can use location directives and work templates to show information about an appropriate location or range of locations where you can put away those items. For returned items, an issue type of **Reservation** is created on the **Inventory transactions** page. For outbound work, use items that have an available inventory status. If you have items that have a status of **Broken**, and master planning is run on these items, the items are considered missing, and inventory is automatically replenished. After you set up inventory statuses, you can set the default inventory status for a site, item, and warehouse. You can also set a default status for sales, transfer, and purchase orders. The default status for sales orders and outbound transfer order can't have the **Inventory blocking** option set to **Yes**. The inventory status that is inherited from the default settings on a site, warehouse, item, purchase order, transfer order or sales order can be changed by using the mobile device, or on the purchase order, sales order, or transfer order line. To plan coverage for items that have an available inventory status, select the **Coverage plan by dimension** option for a storage dimension on the **Storage dimension groups** page. When you open the **Item Coverage** wizard, items that have an available status appear on the **Status** page. To create coverage settings for these items, select the inventory status ID for the available inventory statuses. Based on the coverage settings, you can calculate the item requirements and forecast the supply and demand of available items during master planning. You can't create an item coverage setup that has a blocked inventory status. Alternatively, use the **Item coverage** page to create or modify the item coverage parameters.




<!--HONumber=Feb17_HO3-->


