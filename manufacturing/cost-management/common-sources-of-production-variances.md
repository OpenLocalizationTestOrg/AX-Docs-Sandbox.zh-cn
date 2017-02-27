---
title: Common sources of production variances
description: This article explains various typical sources of each type of production variance.
author: YuyuScheller
manager: AnnBe
ms.date: 2016-04-11 13 - 26 - 41
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventCostTrans
audience: Application User
ms.search.scope: AX 7.0.0, Operations
ms.custom: 79753
ms.assetid: 14ac7db4-fb40-43c1-bb0d-1d51fc91d24f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.dyn365.ops.intro: 01-02-2016
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: d9e19d1755f33597e54de6ea67c426b5172240fa
ms.lasthandoff: 02/22/2017


---

# <a name="common-sources-of-production-variances"></a>Common sources of production variances

This article explains various typical sources of each type of production variance. 

Here are some typical sources of a **lot size** variance:

-   The good quantity for a production order differs from the calculation quantity that is used in the standard cost calculation. The quantity provides the basis for amortizing constant costs.
-   The value of constant costs on the production order differs from the constant costs that are used in the standard cost calculation. The constant costs on the production order can differ for several reasons. For example, the constant costs might reflect the following factors:
    -   Manual changes to the production bill of materials (BOM) or route
    -   The selection of a different BOM version or route version when you create the production order
    -   Planned engineering changes to the BOM version or route version that is assigned to the item

Here are some typical sources of a **production price** variance:

-   The cost category (and cost category price) for the reported consumption of a routing operation differs from the cost category that is used in standard cost calculation.
-   The active cost for the cost category price differs from the cost category price that is used in standard cost calculation.

Here are some typical sources of a **production quantity** variance:

-   You over-issue or under-issue a material component.
-   You over-report or under-report the time for a routing operation.
-   You over-receive or under-receive the good quantity of the parent item, relative to the order quantity. However, you issue components and report operations completely, based on the order quantity for the production order.

Here are some typical sources of a **production substitution** variance:

-   You issue a material component that isn't on the production BOM.
-   You manually add a component to the production BOM and report that component as consumed.
-   You report an item as consumed but don't manually add it to the production BOM.
-   You manually add an operation to the production route and report that operation as consumed.
-   When you create the production order, you select a BOM version that differs from the BOM version that is used in the standard cost calculation.
-   When you create the production order, you select a route version that differs from the route version that is used in the standard cost calculation.



