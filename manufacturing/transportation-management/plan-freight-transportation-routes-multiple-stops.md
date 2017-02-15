---
title: Plan freight transportation routes with multiple stops | Microsoft Docs
description: This article describes the various elements that you use to plan transportation routes in Microsoft Dynamics AX.
author: YuyuScheller
manager: AnnBe
ms.date: 2016-06-09 11:18:27
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: TMSHubMaster, TMSLoadBuildTemplates, TMSRateRouteWorkbench, TMSRouteGuide, TMSRoutePlan, TMSRouteWorkbench, WHSLoadTemplate
audience: Application User
ms.reviewer: 2084
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 90013
ms.assetid: 285cf0ec-d34e-4388-9193-84f64eb5eea5
ms.region: Global
ms.author: yuyus
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 2c807c1b0e75ee2c7292b04f42c2241d531c7a9b


---

# <a name="plan-freight-transportation-routes-with-multiple-stops"></a>Plan freight transportation routes with multiple stops

This article describes the various elements that you use to plan transportation routes in Microsoft Dynamics AX.

You can use route plans and route guides for complex transportation routes that have multiple stops. If the same route will be used on a regular basis, you can set up a scheduled route.

## <a name="route-plans"></a>Route plans
A route plan contains route segments that provide information about the stops that are visited on the route and the carriers that are used for each segment. You must define the stops on the route as hubs. A hub can be a vendor, a warehouse, a customer, or even just a reloading place where you change carrier. For each segment, you can define “spot rates” for various charges. Here are some examples:

-   Charges for travelling to the given segments
-   Charges for a picking up the goods
-   Charges for dropping off the goods

Each route plan must be associated with a route guide.

## <a name="route-guides"></a>Route guides
A route guide defines the criteria for matching a load to a specific route plan. For example, you can specify an origin hub and a destination hub, limits for the container volume or weight, and a shipping carrier, service, or group. Route guides are available on the **Rate route workbench** page, where loads can be matched to routes either manually or automatically. If the route guide is for a scheduled route, it's also available on the **Load building workbench** page.

## <a name="scheduled-routes"></a>Scheduled routes
A scheduled route is a predefined route plan that has a schedule for the shipping dates. Scheduled routes and non-scheduled routes differ in the way that loads are assigned to them. If you assign a non-scheduled route by using the Rate route workbench, only the load and the route guide are validated. If you assign a scheduled route, the dates and addresses from the orders and the hubs, and the date on the route plan, are also considered. You don't have to use the Rate route workbench page to manually assign loads to a scheduled route. Instead, you can use the Load building workbench to suggest that loads be built based on the customer addresses and delivery dates from sales orders for a given scheduled route. For scheduled routes, the route plan will have fixed origin and destination hubs. Typically, the shipping carrier and service will be the same for all segments, but they can differ. The destination hubs are created by using the postal codes of the customers that are visited on the route. Several route schedules can be defined for one route plan. The route plan must be associated with a route guide. However, for scheduled routes, the plan can be associated with only one route guide. The route schedule is used only to create the actual routes on the **Route schedule** page. You can use the default load template when you propose loads on the Load building workbench.

## <a name="load-building-workbench"></a>Load building workbench
The Load building workbench uses the customer addresses and delivery dates from sales orders, and the scheduled routes that are available, to propose a load. By default, the values from the route are entered on the workbench. However, you can select a "from" date that is earlier than the "from" date on the route. When a load is proposed, the delivery address and delivery date of all open sales orders are checked. If the postal code of the delivery address matches the postal code of a hub in the route plan, and if the delivery date is within the range that is selected in the criteria, the sales order is proposed for the load. The capacity of the load template is also considered. Only one load is proposed at a time. If you have a sales order that isn't included, you might have to use a different load template (for example, a load template for a bigger truck or container) or plan an extra delivery.




<!--HONumber=Feb17_HO3-->


