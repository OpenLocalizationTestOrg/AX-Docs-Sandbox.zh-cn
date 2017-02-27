---
title: Plan freight transportation routes with multiple stops
description: This article describes the various elements that you use to plan transportation routes in Microsoft Dynamics AX.
author: YuyuScheller
manager: AnnBe
ms.date: 2016-06-09 11 - 18 - 27
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: TMSHubMaster, TMSLoadBuildTemplates, TMSRateRouteWorkbench, TMSRouteGuide, TMSRoutePlan, TMSRouteWorkbench, WHSLoadTemplate
audience: Application User
ms.search.scope: AX 7.0.0, Operations
ms.custom: 90013
ms.assetid: 50d6f58c-f1c8-4321-9e83-8445cec57a85
ms.search.region: Global
ms.author: yuyus
ms.dyn365.ops.intro: 01-02-2016
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: bc363dbab900c7a162aaab80573921d084f233c9
ms.lasthandoff: 02/22/2017


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


