---
title: Determine the BOM version
description: During a demand explosion, if an item has a default order type of Production, the planning engine finds a valid BOM version based on the site.
author: YuyuScheller
manager: AnnBe
ms.date: 2015-09-10 08 - 51 - 05
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMConsistOf, BOMDesigner, BOMTable, InventItemOrderSetup
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.dyn365.ops.intro: 01-02-2016
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 39c7d1a5a54c5b4c0d7ee114935b63d7f70c209f
ms.lasthandoff: 02/22/2017


---

# <a name="determine-the-bom-version"></a>Determine the BOM version

During a demand explosion, if an item has a default order type of Production, the planning engine finds a valid BOM version based on the site. 

The site dimension is always known and is stated on the demand transaction. The following process is used to determine the BOM version to use:

-   If there is a BOM version defined for the item at the demand site, the site-specific BOM is used.
-   If there is no site-specific BOM version defined for an item at the demand site, a general BOM is used. A general BOM does not state a site, and it is valid for multiple sites. If there is a general BOM, it is used.
-   If there is no general BOM version to use, the demand explosion stops at this point.

A valid BOM version, whether site-specific or general, must meet the required criteria for date and quantity.




