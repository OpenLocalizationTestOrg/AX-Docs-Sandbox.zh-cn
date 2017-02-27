---
title: Cost objects
description: This article provides information about costs objects, and explains how costs and quantities are accumulated. A cost object is an entity that costs and quantities are accumulated for. A cost object entity can be either a product or product variants, such as variants for style and color.
author: YuyuScheller
manager: AnnBe
ms.date: 2015-12-07 09 - 23 - 23
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: 01-02-2016
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: deb6cd408dd032265780a8f66228b7d2aa369dab
ms.lasthandoff: 02/22/2017


---

# <a name="cost-objects"></a>Cost objects

This article provides information about costs objects, and explains how costs and quantities are accumulated. A cost object is an entity that costs and quantities are accumulated for. A cost object entity can be either a product or product variants, such as variants for style and color.  

<a name="cost-objects"></a>Cost objects
------------

The **Cost objects** page lists all cost objects that are registered on a product. The cost objects are defined by data from the following sources:

-   Product
-   Product dimension group
-   Storage dimension group
-   Tracking dimension group

**Note:** A cost object represents a cost element of the **Direct material** type only. A cost object and an inventory object differ in the way that a cost object is defined by the inventory dimensions that are selected for financial inventory. For example, an item has the following configuration:

-   **Site:** Physical inventory = Yes, Financial inventory = Yes
-   **Warehouse:** Physical inventory = Yes, Financial inventory = No
-   **Batch No.:** Physical inventory = Yes, Financial inventory = No

The following table shows what is a cost object and what is an inventory object.

| Object type      | Item number | Site | Warehouse | Batch No. |
|------------------|-------------|------|-----------|-----------|
| Cost object      | x           | x    |           |           |
| Inventory object | x           | x    |  x        | x         |

## <a name="accumulation-of-costs-and-quantities"></a>Accumulation of costs and quantities
-   The value in the **Value** fieldis a sum of the following values:
    -   Physical cost amount
    -   Financial cost amount
    -   Adjustments
-   The value in the **Quantity** field is a sum of the following values:
    -   Received
    -   Deducted
    -   Posted quantity
-   The **Average unit cost** field is a calculated field. The value is calculated by dividing the **Value** value by the **Quantity** value.

**Note:** The **Include physical value **parameter has no effect on the preceding calculations.

<a name="see-also"></a>See also
--------

[Product dimension group](https://technet.microsoft.com/en-us/library/aa499382.aspx)

[Storage dimension group](https://technet.microsoft.com/en-us/library/hh209317.aspx)

[Tracking dimension group](https://technet.microsoft.com/en-us/library/hh209465.aspx)

[What's new or changed in Microsoft Dynamics AX](whats-new-changed.md)

[Cost entries](cost-entries.md)


