---
title: Dimension-based product configuration | Microsoft Docs
description: Dimension-based product configuration represents a simple solution for creating many product variants from a single product master and its bill of materials.
author: YuyuScheller
manager: AnnBe
ms.date: 2015-12-07 17:53:16
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: YuyuScheller
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 19821
ms.assetid: 56ae6c1c-55a8-450a-a6f7-d1f726b8307d
ms.region: Global
ms.industry: Manufacturing
ms.author: yuyus
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 5f80e608bf1fc72af6475d6b4cdc454cbcd9b467


---

# <a name="dimension-based-product-configuration"></a>Dimension-based product configuration

Dimension-based product configuration represents a simple solution for creating many product variants from a single product master and its bill of materials.

Dimension-based product configuration is one of the three built-in product configuration technologies. The two other technologies are predefined variants and constraint-based configuration. All three technologies use a product master as the starting point and allow the user to create many product variants for one product master.

## <a name="key-concepts"></a>Key concepts
Dimension-based product configuration is based on the following key concepts:

-   Product masters
-   Configuration product dimension
-   Configuration groups
-   Bill of materials (BOM)
-   Configuration route
-   Configuration rules

### <a name="product-masters"></a>Product masters

A product master is the starting point for any product configuration process. For the dimension-based product configuration, you need a product master with this particular configuration technology and a product dimension group that includes the configuration product dimension.

### <a name="configuration-product-dimension"></a>Configuration product dimension

The configuration product dimension is used to identify the product variants for a product master with the dimension-based configuration technology. The configuration dimension value is entered by the user and should help to identify the individual product variants.

### <a name="configuration-groups"></a>Configuration groups

Configuration groups are defined in a central repository and can be used for all dimension-based product configuration models. Configuration groups are associated to the individual BOM lines and hold together a group of lines that are mutually exclusive. This means that only one line in a group can be selected for a single product variant.

### <a name="bill-of-materials-bom"></a>Bill of materials (BOM)

The BOM represent the building blocks for a dimension-based product configuration. It must include all the different products that can be used in any product variant. Each line in the BOM can reference a configuration group. If a line doesn’t reference a configuration group, it will be included in all product variants.

### <a name="configuration-route"></a>Configuration route

The configuration route determines the sequence of the configuration groups, as they will be displayed to the user during the product configuration process.

### <a name="configuration-rules"></a>Configuration rules

The configuration rules represent a mechanism for ensuring that a product included in one configuration group in a BOM enforces either an inclusion or an exclusion of a product in a different configuration group in the same BOM.

## <a name="product-modeling-process"></a>Product modeling process
The natural sequence for building a product model for a dimension-based product starts with defining the relevant configuration groups. It is important to ensure that all products which will be used in the BOM have been relased to the company that the product model is built for. With these building blocks in place, the user can create the BOM and assign configuration groups to all relevant BOM lines. When the BOM is complete, a configuration route can be defined for ordering the configuration groups in the proper sequence. \[caption id="attachment\_282671" align="alignnone" width="1187"\][![Dimension-based product modeling process](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) Dimension-based product modeling process\[/caption\] If there are certain products from different configuration groups that either must or must not be used together, you can create configuration rules that will enforce these product relationships. After the BOM has been tied together with a dimension-based product master through a BOM version and both have been approved and activated, you can create product configurations and enter a name for each configuration. The configurations can be defined before any transactions are generated or it can be done when the need for a certain configuration occurs.

### <a name="suggested-use"></a>Suggested use

The dimension-based configuration technology is best used for products with limited variability and the combination of the standard product dimensions size, color, style, and configuration is unsuitable for identifying a specific product variant. An example could be bicycle with frame height, wheel size, brake types, and different gears.




<!--HONumber=Feb17_HO3-->


