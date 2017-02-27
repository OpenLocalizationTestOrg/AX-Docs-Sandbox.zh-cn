---
title: Set up consignment
description: This topic explains how to configure inbound consignment inventory operations.
author: YuyuScheller
manager: AnnBe
ms.date: 2016-10-31 13 - 59 - 51
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventJournalOwnershipChange, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.search.scope: Operations
ms.custom: 220804
ms.assetid: 88822f78-4de5-462c-a55f-1f766c572719
ms.search.region: Global
ms.author: perlynne
ms.dyn365.ops.intro: 01-11-2016
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 58bf93d9cb3f9a2ed165b7f419d08695ff499992
ms.lasthandoff: 02/22/2017


---

# <a name="set-up-consignment"></a>Set up consignment

This topic explains how to configure inbound consignment inventory operations. 

Consignment inventory is inventory that’s owned by a vendor, but stored at your site. When you’re ready to consume or use the inventory, you take over the ownership of the inventory. This topic describes the setup needed to enable consignment processes. For more information about consignment processes, see [Consignment](consignment.md).

## <a name="inventory-owners"></a>Inventory owners
In order to record physical inbound consignment inventory, you need to define a vendor owner. This is done on the **Inventory owner** page. When you select a **Vendor account** this generates default values for the **Name** and **Owner** fields. The value in the **Owner** field will be visible to the vendor, so you might want to change it if your vendor account names aren’t easy for external people to recognize. It’s possible to edit the **Owner** field, but only up to the point when you save the **Inventory owner** record. The **Name** field is populated with the name of the party that the vendor account is associated with, and this cannot be changed. [![inventory-owners](./media/inventory-owners.png)](./media/inventory-owners.png)

## <a name="tracking-dimension-group"></a>Tracking dimension group
Items that are going to be used in consignment processes must be associated with a **Tracking dimension group** where the **Owner** dimension is set to **Active**. The Owner dimension always has the **Physical inventory** and **Financial inventory** options selected. The **Coverage plan by dimension** is never selected. [![tracking-dimension-group](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)

## <a name="inventory-ownership-change-journal"></a>Inventory ownership change journal
The **Inventory ownership change** journal is used to record the transfer of ownership of consignment inventory from the vendor to the legal entity that’s consuming it. Like any inventory journal, it must be identified with an Inventory journal name. These names are created on the **Inventory journal names** page, and the **Journal type** must be set to **Ownership change**. [![inventory-ownership-change-journal](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>Vendor collaboration in consignment processes
If your vendors are using the vendor collaboration interface, they can use this to monitor the consumption of inventory at your site. For more information about setting up vendors to use vendor collaboration, see [Configuration of security for vendor collaboration users](configure-security-vendor-portal-users.md).


