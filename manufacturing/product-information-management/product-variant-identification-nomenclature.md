---
title: Product number nomenclature | Microsoft Docs
description: This topic describes how you can set up a product number nomenclature to replace the fixed format, [Product master number:Configuration:Size:Color:Style], with a targeted format that includes the product master number, active product dimensions, and text delimiters of your choice. You can also build a nomenclature to identify configurations that are created by the constraint-based product configurator. These nomenclatures can contain attributes of your choice.
author: YuyuScheller
manager: AnnBe
ms.date: 2016-10-31 12:44:47
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: 121
ms.suite: Released- Dynamics 365 for Operations version 1611
ms.custom: 220104
ms.assetid: 0c2f64ca-b164-4a9c-85b4-009ccc0a12f7
ms.region: global
ms.industry: Manufacturing
ms.author: yuyus
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: e536b8e5c7f54d159fa7ea006dce357ec69a9bab


---

# <a name="product-number-nomenclature"></a>Product number nomenclature

This topic describes how you can set up a product number nomenclature to replace the fixed format, [Product master number:Configuration:Size:Color:Style], with a targeted format that includes the product master number, active product dimensions, and text delimiters of your choice. You can also build a nomenclature to identify configurations that are created by the constraint-based product configurator. These nomenclatures can contain attributes of your choice.

The new product variant number nomenclature lets you include segments in your product variant identifiers. These segments can include the product master number, product dimensions, number sequences, text constants, and attributes. This functionality lets you quickly find a specific product variant when you create a sales order or purchase order.

## <a name="nomenclature-of-predefined-product-variants"></a>Nomenclature of predefined product variants
Product variants are generated for product masters according to one of three configuration technologies:

-   Predefined variants
-   Constraint-based
-   Dimension-based

Each product variant has a number, and the product variant identification nomenclature lets you select the segments that will be included in each product variant number. You can select the following segments on the **Product nomenclature** page.

-   Product master number
-   Number sequence value
-   Text constant
-   Product dimensions
    -   Configuration
    -   Color
    -   Size
    -   Style

After a product variant identification nomenclature is defined, it can be associated with a product dimension group. Consequently, all product masters referencing this product dimension group will be assigned product variant numbers according to the nomenclature. It is also possible to assign a product variant identification nomenclature directly to a product master, in which case the product variants belonging to this master will be assigned product variant numbers according to the nomenclature.

### <a name="example"></a>Example

A T-shirt (TS1234) is produced in 3 different sizes (S, M, L), 4 different colors (Red, Green, Blue, Yellow), and 2 styles (Polo, V) giving a total of 24 possible product variants. A product variant identification nomenclature is created with the following segments:

1.  Product master number
2.  Text constant: '-'
3.  Color
4.  Text constant: '-'
5.  Size
6.  Text constant: '-'
7.  Style

The product variant number for the Red, Small, Polo will be: TS1234-Red-Small-Polo.

## <a name="nomenclature-of-constraintbased-configurations"></a>Nomenclature of constraintbased configurations
For constraint-based configurations, a dedicated nomenclature can be built for the configuration product dimension. You can select the following segments on the **Product nomenclature** page.

-   Number sequence value
-   Text constant
-   Attribute value 

Each component in a product configuration model can have its own configuration nomenclature. Only attributes belonging to the component may be used. Attributes from subcomponents or user requirements are not available.

### <a name="example"></a>Example

A product configuration model has a root component with two attributes.

-   Material (Plastic, Wood, Steel)
-   Length (10...100)

A configuration nomenclature is defined using the following segments:

1.  Attribute value: Material
2.  Text constant: 'AAA'
3.  Attribute value: Length

The configuration ID for wood material with a length of 78 will get the following configuration ID: WoodAAA78.

## <a name="nomenclature-of-dimensionbased-configurations"></a>Nomenclature of dimensionbased configurations
For dimension-based configurations, a dedicated nomenclature can be built for the configuration product dimension. You can select the following segments on the **Product nomenclature** page.

-   Number sequence value
-   Text constant
-   Configuration group item

A configuration nomenclature can be defined for a bill of materials (BOM).

### <a name="example"></a>Example

A bill of materials has 4 BOM lines divided into 2 configuration groups.

-   BOM line: M0007, Standard cabinet
    -   Configuration group: Cabinet
-   BOM line: M0008, High end cabinet
    -   Configuration group: Cabinet
-   BOM line: M0021, Front grill cloth
    -   Configuration group: Front grill
-   BOM line: M0022, Front grill metal
    -   Configuration group: Front grill

A configuration nomenclature is defined using the following segments:

1.  Configuration group: Cabinet
2.  Text constant: '&'
3.  Configuration group: Front grill

The configuration ID for a standard cabinet with cloth front grill will be: M0007&M0021.

## <a name="nomenclature-of-a-combination-of-product-variants-and-configurations"></a>Nomenclature of a combination of product variants and configurations
When you use either constraint-based or dimension-based configuration technology to configure product variants for a product master, the product variants can get product variant numbers that include the nomenclature from the configuration dimension. Follow these steps to configure variants:

1.  Define a product variant number nomenclature that includes the configuration dimension on the **Product nomenclature** page.
2.  Assign this nomenclature to a product dimension group with the configuration dimension.
3.  Define a configuration nomenclature for the components or BOMs that will be used for configuring the product variants.

### <a name="example-for-constraint-based-configurations"></a>Example for constraint-based configurations

In this example, you can use a product variant number nomenclature that consists of the following segments:

1.  Product master number
2.  Text constant '\_'
3.  Configuration

The configuration nomenclature can consist of the following segments:

1.  Attribute value: Material
2.  Text constant: 'AAA'
3.  Attribute value: Length

You can enter the following values for segments:

-   Product master number = M0099
-   Material = Plastic
-   Length = 12

The product variant number will become: M0099\_PlasticAAA12.

### <a name="example-for-dimension-based-configurations"></a>Example for dimension-based configurations

In this example, you can use a product variant number nomenclature that consists of the following segments:

1.  Product master number
2.  Text constant '//'
3.  Configuration

The configuration nomenclature can consist of the following segments:

1.  Configuration group: Cabinet
2.  Text constant: '&'
3.  Configuration group: Front grill

You can enter the following values for segments:

-   Product master number = D0123
-   Cabinet = M0008
-   Front grill = M0022

The product variant number will become: D0123//M0008&M0022.

## <a name="numbering-conflicts"></a>Numbering conflicts
It is possible to set up product variant number nomenclature that does not result in unique product variant numbers. For example, this could happen if one active product dimension is not included in the nomenclature for a product master that uses the predefined variant configuration technology. Conflicts are handled differently for the different configuration technologies.

### <a name="predefined-variants"></a>Predefined variants

An error will occur if you try to manually or automatically generate product variants where one or more ends up with the same product variant number. In order to avoid this, you should use all active product dimensions in the product dimension group, or include a number sequence to ensure that the product variant numbers are unique.

### <a name="constraint-based-configurations"></a>Constraint-based configurations

Depending on the nomenclature, the system may attempt to assign a non-unique product variant number to a configuration. In this case, the system will use the number sequence for the configuration dimension as the product variant number instead. If this happens, you will receive a warning. In order to avoid this, you should include enough attributes in the nomenclature to ensure uniqueness, and make sure that the **Reuse** option is turned on for the component.

### <a name="dimension-based-configurations"></a>Dimension-based configurations

The configuration process includes a step in which the system will suggest a configuration value according to the nomenclature. In this step, you can manually change the configuration value. When you save the configuration, the system will check whether the configuration value is unique. If this is not the case, an error will be displayed. You must enter a unique configuration value in order to save the configuration.



<a name="see-also"></a>See also
--------

[Create a product number nomenclature for predefined product variants](http://ax.help.dynamics.com/en/wiki/create-a-product-number-nomenclature-for-predefined-product-variants/)

[Create a product number nomenclature for configured product variants](http://ax.help.dynamics.com/en/wiki/create-a-product-number-nomenclature-for-configured-product-variants/)




<!--HONumber=Feb17_HO3-->


