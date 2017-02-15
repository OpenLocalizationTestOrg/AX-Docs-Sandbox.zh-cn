---
title: Unit of measure and stocking policies | Microsoft Docs
description: This article describes how default units, unit sequences, and unit conversions are used in warehouse processes.
author: YuyuScheller
manager: AnnBe
ms.date: 2016-01-18 12:49:12
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: EcoResProductDetails, EcoResProductDetailsExtended, EcoResStorageDimensionGroup, InventItemOrderSetup, UnitOfMeasureConversion, WHSRFMenuItem, WHSUOMSeqGroupTable
audience: Application User
ms.reviewer: 2084
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 29611
ms.assetid: b4970d85-88c5-4fd7-b3ab-fc741fa61d8a
ms.region: Global
ms.author: perlynne
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 04f815cc154c3ae0a473b98017dbaa75db0cdc6f


---

# <a name="unit-of-measure-and-stocking-policies"></a>Unit of measure and stocking policies

This article describes how default units, unit sequences, and unit conversions are used in warehouse processes.

Unit sequence groups define the sequence of units that can be used in warehouse operations. They are created on the **Unit sequence groups** page. The sequence shows the relationship of the various units. For example, you store pallets that contain boxes that contain individual pieces of items. In this case, you must provide the three different units and the logical order of the layers. Unit sequence groups let you define the policies for the grouping of license plates, and the default units that should be used for various warehouse processes. This article applies to both the advanced warehousing solution that is available in Warehouse management and the more basic warehousing solution that is available in Inventory management.

## <a name="unit-sequence-groups-for-released-products"></a>Unit sequence groups for released products
If you want to use released products in warehouse work processes, a unit sequence group must be assigned to them. If you validate a product that is associated with a Storage dimension group, and the **Use warehouse management processes** option for the Storage dimension group is set to **Yes**, you receive an error message if a unit sequence group ID isn't defined for the product. If the unit sequence group that you use contains multiple lines (and therefore multiple units), you must set up a unit conversion between the units. You complete this setup on the **Unit conversions** page. The smallest unit in a sequence group that you associate with a released product must match the inventory unit that is defined for the corresponding product. The inventory unit is the unit that is used for base calculations of the on-hand inventory. You can also set up unit of measure conversions for product variants of product masters by using the **Enable unit of measure conversions** option.

## <a name="license-plate-grouping"></a>License plate grouping
You can specify whether receipts of less than or more than a specific unit should be grouped into one license plate or divided into a license plate for each unit. To set up this behavior, use the **License plate grouping** option on the **Line details** tab of the **Unit sequence groups** page. If you want to use the license plate grouping when you process work by using a mobile device, the **License plate grouping** option must be selected on the **Mobile device** menu item. For example, you're using a mobile device to register an item that is associated with a unit sequence group that has two lines. The first line is for Pieces, and the **License plate grouping** option is set to **Yes**. The second line is for the Pallet unit, and the **License plate grouping** option is set to **No**. In this case, the system can automatically guide the split and creation of license plates per 100 pieces.

## <a name="units-for-cycle-counting"></a>Units for cycle counting
To define which units should be used as part of the cycle counting processes, select the **Use unit for cycle counting** option on the **Unit sequence groups** page. You can select a maximum of four units in the sequence group. If you select more than four units, the additional units won't be shown on the mobile device.

## <a name="default-units-for-mobile-device-receiving-processes"></a>Default units for mobile device receiving processes
To set the default units that should be used for receiving processes on mobile devices, enable the **Default unit for purchase and transfer** and **Default unit for production** options on the **Unit sequence groups** page. For example, you can specify that, by default, the system should use Pallet quantities when purchase order on-hand inventory is received by using a mobile device, but that the stock-keeping unit should be Pieces. To get the conversion for the number of pieces that each pallet contains, you must define a unit conversion, such as 100 Pcs = 1 PL.

## <a name="default-order-settings"></a>Default order settings
As part of the creation of released products, you must select default units for purchases, sales, and inventory to process the various orders. You can set the default units and quantities for the various source documents by using the **Default order settings** and **Site specific order settings** pages. You can access these pages from the **Released products** page.




<!--HONumber=Feb17_HO3-->


