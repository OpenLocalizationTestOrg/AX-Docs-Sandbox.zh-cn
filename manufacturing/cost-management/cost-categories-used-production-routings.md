---
title: Cost categories used in production routing | Microsoft Docs
description: This article provides information about cost categories that apply to manufacturing environments that use routing.
author: YuyuScheller
manager: AnnBe
ms.date: 2016-04-05 14:44:12
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: ProjCategory, RouteCostCategoryPrice
audience: Application User
ms.reviewer: 2094
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 78153
ms.assetid: 575e929e-bcc7-4238-ae84-5b2b4721fa10
ms.region: Global
ms.industry: Manufacturing
ms.author: mguada
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 7d2a9cc71f8d942b4ae79870078999543cbcbbac


---

# <a name="cost-categories-used-in-production-routing"></a>Cost categories used in production routing

This article provides information about cost categories that apply to manufacturing environments that use routing.

Cost categories apply to manufacturing environments that use routing. They are assigned to operations resources and routing operations to define hourly costs and to segment cost contributions in a manufactured item’s calculated costs. The cost groups that are assigned to cost categories classify manufacturing cost contributions, based on the operation resources and the type of activity, such as setup time and run time. The specificity of cost group assignments enables manufacturing overhead to be calculated based on routing information. **Note:** In manufacturing environments, cost categories are known by several other names, such as labor rate codes or machine rate codes. Each cost category has associated cost records and an assigned cost group. Different cost categories are required for different production purposes.

-   Assign different hourly costs, depending on the operations resource. For example, the costs can differ for various types of labor skills, machines, or manufacturing cells.
-   Assign different hourly costs for the setup time or run time that is associated with a routing operation.
-   Assign operations resource costs based on the output quantity instead of hourly costs, such as the piece rates for paying labor.
-   Provide cost group segmentation of cost contributions to a manufactured item’s calculated cost. For example, you can segment of labor and machine costs.
-   Provide the cost group basis for overhead calculation formulas, such as formulas for labor-related and machine-related overhead, or overhead that is related to setup and run time.

A cost category can be assigned to the setup time, the process time, and the quantity for a routing operation. When, for example, costs or cost group segmentation differs between the setup time and the process time, different cost categories should be defined and assigned to the setup time and the process time. The selective use of cost categories for setup time, process time, and quantity is determined by the route group that is assigned to an operation. The assignment of cost categories to time and quantity can be mandated by company-wide policies that are defined on the **Production control parameters** page. Each cost category has associated costs that are based on the definition of cost records in a costing version. Use the **Cost category price** page to define the cost records for a specified costing version and site. When the cost record for a cost category is first entered, it has a status of **Pending** and an intended effective date. When you activate the cost record, the status is updated to **Current active**, and the effective date is updated to the activation date. Different cost records might reflect different sites, effective dates, or statuses. Bills of materials (BOM) calculations for a future or historical date use cost records that have the relevant effective date. The current active cost record will be used to estimate production order costs and to value reported time against a production order. The cost record for a cost category can be site-specific or company-wide. To make a cost record site-specific, assign a site to it. Otherwise, a blank value indicates that the cost record applies to all sites in the company. Because costs can differ between sites, for example, the cost records must be defined as site-specific. A routing operation generally inherits the cost categories that are assigned to the operations resource or master operation. When a production order is created, the routing operations in the production route reflect the selected route version. You can override the cost categories that are assigned to the operations in the production route. Some types of production work can apply to project time estimates and reporting. In this case, a cost category is required for production and project purposes. You must define additional project-related information when a cost category is flagged for use in projects.




<!--HONumber=Feb17_HO3-->


