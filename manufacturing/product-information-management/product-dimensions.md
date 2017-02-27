---
title: Product dimensions
description: There are four product dimensions -  Color, Configuration, Size and Style. You combine product dimensions in dimension groups and assign dimension groups to product masters. The combinations of product dimensions determine how product variants are defined.
author: YuyuScheller
manager: AnnBe
ms.date: 2015-12-07 09 - 11 - 04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.dyn365.ops.intro: 01-02-2016
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: bea1efd3983e9348c7f857b26f67440061b213a3
ms.lasthandoff: 02/22/2017


---

# <a name="product-dimensions"></a>Product dimensions

There are four product dimensions -  Color, Configuration, Size and Style. You combine product dimensions in dimension groups and assign dimension groups to product masters. The combinations of product dimensions determine how product variants are defined.

Product dimensions are characteristics that serve to identify a product variant. You can use combinations of product dimensions to define product variants. You must define at least one product dimension for a product master in order to create a product variant.
Product variants
----------------

Product variants are also referred to as items. An item is a tangible product, which is not the same as a service. It is also possible to define a product master with the Service type. By using the Service type, you can specify product variants that include services. For example, you can specify a product master for Consultancy work and product variants for work that is performed by senior consultants and junior consultants.

## <a name="product-dimensions"></a>Product dimensions
The following product dimensions are available: Configuration, Color, Size, and Style. A product variant can be generated based on the product dimension values.

Product dimensions values such as Size, Color and Style can be created on the **Size**, **Color** and **Style** pages, which can be accessed from the following locations: **Product information management** &gt; **Setup** &gt; **Dimension and variant Groups** &gt; **Sizes/Colors/Styles**. Product dimension values for the Configuration dimension are typically created using either the Product configurator or the Dimension-based configurator. Product dimensions can also be created and maintained on the **Product dimensions** page, which can be accessed from the following locations:
-   Click **Product information management** &gt; **Products** &gt; **Product masters**. On the **Action Pane**, click **Product dimensions**.
-   Click **Product information management** &gt; **Products** &gt; **All products and product masters**. Select a product master. On the **Action Pane**, click **Product dimensions**.
-   Click **Product information management** &gt; **Released products**. Select a product master. On the **Action Pane**, click **Product**. In the **Product master** group, click **Product dimensions**.

The number of variants that you can create for an item is limited by the number of possible product dimension combinations.
| **Tip**                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| When you use a product on, for example, an order line, you select the product dimensions to identify the product variant that you want to work with. |

## <a name="example"></a>Example
A company sells denim jeans. The item, Jeans, uses the Color and Size product dimensions. The jeans are sold in three different colors and six different sizes. Colors: Blue, Black, Brown Sizes: XS, S, M, L, XL, XXL Not all sizes are available in all the three colors. If all combinations were available, it would create 18 different types of jeans. In this example, only the following nine product variant combinations are produced.

| Color | Size |
|-------|------|
| Blue  | XS   |
| Blue  | S    |
| Blue  | M    |
| Black | M    |
| Black | L    |
| Black | XL   |
| Brown | L    |
| Brown | XL   |
| Brown | XXL  |




