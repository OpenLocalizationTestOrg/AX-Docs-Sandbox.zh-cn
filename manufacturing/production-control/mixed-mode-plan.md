---
title: Mixed mode planning - Combine discrete, process, and lean sourcing | Microsoft Docs
description: This article provides information about mixed mode planning. In mixed mode planning, you can model your supply chain based on the material flow. Microsoft Dynamics 365 for Operations makes sure that the material flow follows your models, regardless of the supply policy that is selected (kanbans, production orders, purchase orders, batch orders, or transfer orders).
author: YuyuScheller
manager: AnnBe
ms.date: 2016-02-24 15:02:09
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: EcoResStorageDimensionGroup, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: 2094
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 52931
ms.assetid: ec92d6ca-3137-4813-a6aa-63118012bb76
ms.region: Global
ms.industry: Manufacturing
ms.author: conradv
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 62b9ac0de433510ce6627dda15490c874dc5220a


---

# <a name="mixed-mode-planning---combine-discrete-process-and-lean-sourcing"></a>Mixed mode planning - Combine discrete, process, and lean sourcing

This article provides information about mixed mode planning. In mixed mode planning, you can model your supply chain based on the material flow. Microsoft Dynamics 365 for Operations makes sure that the material flow follows your models, regardless of the supply policy that is selected (kanbans, production orders, purchase orders, batch orders, or transfer orders). 

You can select your overall strategy for supplying a product, regardless of the product structure. For example, you can have kanban control in the assembly, where materials are sourced for the assembly area by production orders, kanbans, transfers, batch orders, or any combination that is appropriate for the characteristics of your supply chain, but you can still have full visibility across supplies. This capability leads to optimized supply chain processes and enhanced visibility into your supply chain. The granularity of the supply policies that are used in master scheduling depends on the storage dimensions that are enabled as coverage dimensions. To enable master scheduling to control the replenishment and supply of different types of locations (for example, by separating the production floor for different production units, or by separating different types of material and finished goods warehouses), we recommend that you enable Site and Warehouse as coverage dimensions. Alternatively, Warehouse can be omitted as a coverage dimension. In that case, when you use advanced warehouse management, all movements inside a warehouse are controlled by warehouse work, whereas all movements across warehouses can be controlled by withdrawal kanbans.

## <a name="supply-policies"></a>Supply policies
Dynamics 365 for Operations mixed mode planning controls how a product is supplied and, based on the supply, how derived requirements (consumption of items from a bill of materials \[BOM\]) are issued. Based on the order type, the system automatically sources materials to match the requirements. Supply policies can be defined at the product level or at any granularity that supports your requirements. You define the granularity of supply policies on the **Default order settings** page. Supply policies can be controlled by product, item dimensions (configuration, color, and size), site, and warehouse. This setup is done on the **Item coverage** page. The default order type controls what order master planning generates. Regardless of how the supply chain is modeled, Dynamics 365 for Operations supports your mix of supply policies. You can have production orders that are sourced from kanbans. Alternatively, you can have a batch order that requires a product that is supplied by transfers or by kanbans. Dynamics 365 for Operations makes sure that the material flow follows the model. The warehouse for picking material is assigned dynamically at run time, after the supply policy has been defined. Typically, kanbans aren't created for future dates, because a kanban has a short life cycle. To maintain full visibility into the supply chain, we have introduced the new planning concept of a “planned kanban,” which is used to calculate derived requirements and helps guarantee that the requirements are sourced based on the same logic that is used when the actual kanban is created. The same logic is present for all other supply policy types. Therefore, long-term materials planning is based on the same logic that you expect to run with the actual orders after production and supply are approved.

## <a name="materials-allocation-crosssupply-policy--resource-consumption-on-boms"></a>Materials allocation crosssupply policy – Resource consumption on BOMs
Resource consumption is an important functionality. Resource consumption enables a warehouse for picking materials to be selected dynamically, based on the supply policy (order type), and also makes maintenance of base data easier. Resource consumption requires that the warehouse that materials are picked from be assigned based on the way that the product is supplied. In other words, at run time, the system finds the resources that should be used for manufacturing. Based on those resources, the system then finds the picking warehouse. For work that is independent of a supply policy, you don't have to change information on the BOM if the supply is changed. For ad-hoc changes, Dynamics 365 for Operations makes sure that materials are sourced from the right warehouse.

## <a name="process-manufacturing--the-production-type"></a>Process manufacturing – The production type
For full flexibility in mixed mode, we recommend that you use production type BOMs for all products. You can then use production orders, kanbans, transfer orders, or purchase orders to supply a product. For process manufacturing, you must use a production type of **Formula**, **Co-product**, **By-product**, or **Planning item**. Kanbans and production orders can't be used for these production types.




<!--HONumber=Feb17_HO3-->


