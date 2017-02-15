---
title: Update standard costs in a non-manufacturing environment | Microsoft Docs
description: This article provides guidance for updating standard costs in a non-manufacturing environment.
author: YuyuScheller
manager: AnnBe
ms.date: 2016-04-11 13:26:29
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: 2094
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 79723
ms.assetid: 830ea833-8eee-4266-b64c-05fa6513fd16
ms.region: Global
ms.industry: Manufacturing
ms.author: mguada
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 876eec6a1611b16b1818bba53db5b2a0154950d6


---

# <a name="update-standard-costs-in-a-non-manufacturing-environment"></a>Update standard costs in a non-manufacturing environment

This article provides guidance for updating standard costs in a non-manufacturing environment.

The following guidelines assume that you use a two-version approach to update standard cost. In this approach, one costing version contains the standard costs that were originally defined for the frozen period, and the second costing version contains the incremental updates. Each update is entered as a cost record that is enclosed in the second costing version, and eventually it's enabled. An alternative, one-version approach uses the set of standard costs that was originally defined. The two-version approach requires that you define a second costing version. Here are the guidelines for defining this costing version:

-   Assign a costing type of **Standard costs**.
-   Assign a meaningful identifier that indicates the contents of the costing version, such as **2016-UPDATES**.
-   Make sure that the content includes cost records.
-   Allow cost records to be entered for all sites. If you specify a site, cost records can be entered only for that site.
-   Indicate a fallback principle of **None**. The fallback principle applies only to cost calculations for manufactured items.

To correct, adjust, or update standard costs for new items, follow these steps.

1.  Use the **Costing version** **setup** page to enable cost data to be entered into the second costing version. Optionally, prevent the activation of pending costs, so that activation will be allowed after pending costs have been completely and accurately defined. You can also optionally enter a date in the **From date** field. As a general guideline, use the date when you intend to enable the incremental updates. Alternatively, leave the **From date** field blank for the costing version, and then enter a date in the **From date** field for each cost record.
2.  Use the **Item price** page to enter updates as item cost records that are enclosed in the second costing version.
3.  Use the **Item prices** report to verify the completeness and accuracy of the item cost records that are enclosed in the second costing version.
4.  Use the **Costing version maintenance** page to change the blocking flag to allow activation of the pending cost records that are enclosed in the second costing version.
5.  Use the **Activate prices** page (which you open from the **Costing version maintenance** page) to activate all pending item cost records that are enclosed in the second costing version. You can also activate the pending cost records for individual items by clicking the **Activate pending price** button on the **Item price** page.
6.  To prevent additional data maintenance, use the **Costing version setup** page to change the blocking flags that are enclosed in the second costing version. The blocking policies will prevent the entry of new pending costs and the activation of pending costs.





<!--HONumber=Feb17_HO3-->


