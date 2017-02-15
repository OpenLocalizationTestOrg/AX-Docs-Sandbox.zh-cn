---
title: Modeling a lean organization | Microsoft Docs
description: The article provides information about the key concepts in modeling a lean organization.
author: YuyuScheller
manager: AnnBe
ms.date: 2016-02-24 15:08:43
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: LeanProductionFlow, PlanActivity
audience: Application User
ms.reviewer: 2094
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 53141
ms.assetid: 72acf662-e9c0-4592-9934-119aea106f7d
ms.region: Global
ms.industry: Manufacturing
ms.author: conradv
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 5fc692385273f3d264d35db67f61538f58a7ada7


---

# <a name="modeling-a-lean-organization"></a>Modeling a lean organization

The article provides information about the key concepts in modeling a lean organization. 

Typically, a lean manufacturing scenario is more than just a collection of unrelated kanban rules or material supply policies. The flow of material and products throughout work cells and locations for a specific production or supply scenario can be described as a sequence or small network of process or transfer activities. This sequence or network is known as a production flow.

## <a name="production-flows-in-lean-manufacturing"></a>Production flows in lean manufacturing
In production scenarios that are based on production orders, material is issued to a specific production order. During a sequence of operations that is based on a bill of materials (BOM) and routes, products are created and are finally received at the supplied location. The throughput time of production orders varies from minutes to weeks. All related cost, material, and labor are accumulated on the production order. To reduce the delivery lead times and excess inventory between work centers that batch production causes, lean manufacturing introduces kanban replenishment and supermarkets in manufacturing and warehouse replenishment. Typically, these features disrupt the production of partially independent kanban cycles. The replenishment of a kanban for a semi-finished product is no longer triggered by an order for a finished product. To re-establish a production and cost context for the various kanban scenarios that are proposed in Microsoft Dynamics AX, activity-based production flows have been introduced as the backbone of lean manufacturing. All kanban rules refer to this predefined structure. The activity-based model supports the setup of a wider range of scenarios than previous versions of Lean manufacturing for Dynamics AX supported. However, this model doesn't add complexity for the shop floor workers, because all scenarios use the same activity-based user interface.

## <a name="semifinished-products-nonbom-levels"></a>Semifinished products (nonBOM levels)
Lean manufacturing for Dynamics AX integrates kanbans for inventoried products and semi-finished products in a single framework, and therefore offers a unified user experience for all cases. Because of this architecture, additional BOM levels no longer have to be introduced to enable kanbans to be used for semi-finished products. This architecture also helps reduce inventory transactions to a minimum.

## <a name="products-and-material-in-work-in-progress"></a>Products and material in work in progress
The reduction of batch sizes to the ideal state of a single piece flow in lean manufacturing can cause a dramatic increase in inventory transactions if each picking process or kanban registration causes transactions for the consumed items. The production flow architecture allows for the transfer of material to the production flow, together with the withdrawal kanbans in storage or transport handling unit sizes. The value of the issued material is added to the work in progress (WIP) account that is related to the production flow. This behavior resembles the behavior for material that is issued to a production order. The same principle can be applied to products and semi-finished products. Unless these products are created, transferred, or consumed within a production flow, inventory transactions are optional. After the products are posted to inventory, the WIP account for the production flow is reduced by deducting by the related standard cost.

## <a name="value-streams-and-value-stream-mapping"></a>Value streams and value stream mapping
The architecture of Lean manufacturing for Dynamics AX is inspired by the five Lean principles that were formulated by Womack and Jones: Customer value, Value stream, flow, pull, and perfection. One approved method for implementing lean manufacturing solutions in the physical world of manufacturing is value stream mapping (VSM). This method was introduced by Rother and Shook in their publication “Learning to See” at the Lean Manufacturing Institute. In Dynamics AX, the future-state value stream can be modeled as a production flow version. All processes of the value stream are modeled as process activities. Movements or transfers can be modeled as transfer activities if the transfer status must be registered, or if integration with inventory picking or consolidated shipments is required. The value stream itself is modeled as an operating unit in Dynamics AX. Therefore, the value stream can be used as a financial dimension.

## <a name="costing-for-lean-manufacturing-based-on-the-production-flow"></a>Costing for lean manufacturing based on the production flow
The periodic consolidation of the cost for a production flow corrects the related WIP account and enables variances to be determined for the products that are supplied by the production flow.

## <a name="continuous-improvement"></a>Continuous improvement
To better support continuous improvement, the production flows are implemented in time-effective versions. Therefore, an existing production flow version, together with all related kanban rules, can be copied to a future version of the production flow. In addition, the future-state production flow can be modeled before it's validated and activated for production. To help guarantee a seamless material flow on the transition date and beyond, existing kanbans from old production flow versions are automatically related to the new version.

## <a name="simplicity"></a>Simplicity
For the implementation of Lean manufacturing for Dynamics AX, we choose a production flow and activity approach that enables simple and complex production scenarios to be modeled in a single scalable architecture. A closer look at the activity concept reveals a new simplicity for those users who require it: the shop floor and logistics workers. By reporting against activity-based jobs instead of inventory transactions, a unified user interface for all lean manufacturing variants transfers the business complexity from the user interface to where it belongs: the production flow as the backbone of lean manufacturing.




<!--HONumber=Feb17_HO3-->


