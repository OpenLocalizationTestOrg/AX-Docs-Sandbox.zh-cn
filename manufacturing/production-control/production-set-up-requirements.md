---
title: Production setup requirements | Microsoft Docs
description: This article provides information about setup requirements before you can work with Production control.
author: YuyuScheller
manager: AnnBe
ms.date: 2016-02-25 13:02:09
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: ProdParameters, RouteOpr, RouteOprTable, WorkCalendarTable, WorkTimeTable, WrkCtrTable
audience: Application User
ms.reviewer: annbe
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 55561
ms.assetid: 96799f56-9940-4bed-8d50-77ed6f21bc40
ms.region: Global
ms.industry: Manufacturing
ms.author: johanho
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 0b406ea4658545d101f8010a65b99c8a97259b8c


---

# <a name="production-setup-requirements"></a>Production setup requirements

This article provides information about setup requirements before you can work with Production control. 

Production control is integrated with features in other modules. This interconnectivity lets you change production orders and make sure that they are automatically updated in all other related processes and calculations in the system. The following setup processes are listed in the order that you should complete them in.

## <a name="required-baseline-setup-in-other-modules"></a>Required baseline setup in other modules
Information in other modules must be set up before you can work with Production control. This setup includes the following tasks:

-   Set up general company information.
-   Set up the general ledger.
-   Define item groups.
-   Set up ledger accounts for item groups.
-   Set up the inventory item table in Inventory management.
-   Create bills of materials (BOMs) and BOM versions in Inventory management.

## <a name="required-calendar-and-resource-setup"></a>Required calendar and resource setup
Before you use Production control, open Organization administration, and create and define the calendar and operations resources in the following order:

1.  **Working time templates** – Set up working time templates to define the times that are available for production scheduling.
2.  **Calendars** – Set up working time calendars to define the days of the year that are available for production scheduling.
3.  **Resource groups** – Set up resource groups to group the operations resources, so that you can get an overview of any free capacity when you run scheduling. You don't have to set up resource groups before you set up operations resources. However, we recommend that you understand how to group resources when you set up Production control.
4.  **Resources** – Set up operations resources to define the resources that are used to complete the production process and plan for capacity.

## <a name="required-production-parameters-setup"></a>Required production parameters setup
**Production control parameters** – Set up basic production parameters to define how the system handles and processes production orders. Define how production orders are created, estimated, scheduled, and consumed. You can also select what kind of feedback you want and how cost accounting is done.

## <a name="required-journal-name-identification"></a>Required journal name identification
**Production journal names** – Specify the production journal names that are used to record and post transactions.

## <a name="setup-if-you-use-operations"></a>Setup if you use operations
Operations represent the specific activities that are completed to produce the finished product. **Note:** You must know the types of activities that are required in order to produce your item, and the order and priorities of those activities. You must also know which resources are involved, and how many.

1.  **Operations** – Set up operations to represent the tasks that must be completed to produce the finished item.
2.  **Relations** – Set up operation relations to establish detailed properties. To define operation relations, click **Relations** on the **Operations** page.

## <a name="setup-if-you-use-routes"></a>Setup if you use routes
If you're working with routes, operations must be defined for every production route that you set up. The route represents the path that the item takes from operation to operation, from the start of the production process to the end.

1.  **Cost categories** – Set up cost categories to define the cost per hour of specified processes and setup times.
2.  **Cost groups** – Set up cost groups to create and maintain different types of costing.
3.  **Route groups** – Set up route groups to define parameters that are related to groups of routes. You must set up route groups before you can create production routes.
4.  **Routes** – Set up production routes, and define default settings to control scheduling, costing, and pricing of route operations, and to control progress reporting.
5.  **Routes** – Set up route versions to enable item variations in production.

## <a name="optional-advanced-settings"></a>Optional advanced settings
1.  **Production groups** – Set up production groups to establish relationships between the production order and ledger accounts. The ledger accounts are used to post or group orders for reporting.
2.  **Production pools** – Create production pools to group production orders so that you can process urgent production orders, or delete and post groups of orders.
3.  **Properties** – Define properties to create special attributes that you can assign to your resources to control the order of productions. These attributes are connected to the working time template.





<!--HONumber=Feb17_HO3-->


