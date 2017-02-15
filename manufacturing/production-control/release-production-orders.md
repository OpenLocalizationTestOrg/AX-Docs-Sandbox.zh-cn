---
title: Release production orders | Microsoft Docs
description: A released production order is an order that has been authorized for production. The term Released is used to describe a state in the production order life cycle, where the production order is available for execution on the production shop floor and for warehouse processes.
author: YuyuScheller
manager: AnnBe
ms.date: 2015-09-10 08:43:17
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: ProdParmRelease
audience: Application User
ms.reviewer: annbe
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 2414
ms.assetid: 23ca0804-7f2f-4624-9be1-7b3d9014d91c
ms.region: Global
ms.industry: Manufacturing
ms.author: johanho
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: f082a7a7e393f7cc7bdf8f79fd7b2301c1f7663a


---

# <a name="release-production-orders"></a>Release production orders

A released production order is an order that has been authorized for production. The term Released is used to describe a state in the production order life cycle, where the production order is available for execution on the production shop floor and for warehouse processes. 

<a name="characteristics-of-the-released-state"></a>Characteristics of the Released state
-------------------------------------

The **Released** state is one state in the production order life cycle. Production orders that are in the **Released** state are available for execution on the production shop floor and for warehouse processes. The **Released** state has the following characteristics:

-   A production order can be changed to the **Released** state either from the production order or by using a batch process. The production order can also be updated automatically from planned production orders that are firmed by using the **Firming time fence** field on the **Master plan** page.
-   The **Released** state is the signal for the shop floor operators (operators) to start executing the production jobs on the shop floor.
-   Production papers, such as route cards, route jobs, and jobs cards provide information about production jobs and can be issued.
-   For materials that are physically reserved, warehouse work is generated to pick materials for the production order.

## <a name="releasing-jobs-to-the-shop-floor"></a>Releasing jobs to the shop floor
After a production order is released, production jobs that are related to the order are visible and ready for registration. The operators can make job registrations, such as Start, Stop, and Completion, on either the **Job card terminal** page or the **Job card device** page. The registered time and quantity are automatically transferred from the registration pages to production journals to keep track of the consumed time and quantity.

## <a name="route-cards"></a>Route cards
A route card provides an overview of information that comes from route and operation setups, and from operation and job scheduling methods.

## <a name="route-jobs"></a>Route jobs
A route job lists each job of an operation in detail, and includes setup, process, queue, and transportation times. For example, an operation such as painting might require individual jobs, such as setup time, run time for the painting process, and queue time for drying.

## <a name="job-cards"></a>Job cards
A job card lists the individual job numbers of a particular operation. One job appears on each page. The jobs that are included on a job card, and their estimated times, come from the route and operation setup information. From a job card, you can open the **Production journal lines**, **job card** page. People who run operations resources can provide feedback about the production process. There are fields where you can enter consumption statistics and information such as the error quantity.

## <a name="warehouse-work-for-raw-material-picking"></a>Warehouse work for raw material picking
Work for raw material picking is generated during release. Work is generated only for the quantity of materials that was physically reserved for the production order before the order was released. The following setup is required to generate warehouse work for raw material picking:

-   A location directive for raw materials picking that determines which warehouse location to pick the materials in
-   A wave template for raw materials, where policies for the execution of warehouse work are configured
-   A production input location that determines where materials are put





<!--HONumber=Feb17_HO3-->


