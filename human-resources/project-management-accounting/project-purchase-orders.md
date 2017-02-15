---
title: Purchase orders for a project | Microsoft Docs
description: This article describes the various methods that you can use to create purchase orders for a project. The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.
author: kfend
manager: AnnBe
ms.date: 2016-04-29 22:02:01
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: 51
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 83972
ms.assetid: 5ceae144-e3f8-437d-88f6-6751ac27e60a
ms.region: Global
ms.author: kfend
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 05de337ef6c4ac1f09fe5ed7a9cc070f247d6cbb


---

# <a name="purchase-orders-for-a-project"></a>Purchase orders for a project

This article describes the various methods that you can use to create purchase orders for a project. The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.

In Microsoft Dynamics 365 for Operations, you can use multiple methods to create purchase orders for a project. The method that you use depends on the purpose of the purchase order, when the purchased items are consumed, and when the purchased items are charged to a project.

### <a name="methods-for-creating-a-purchase-order"></a>Methods for creating a purchase order

You can use one of the following methods to create a purchase order in Project management and accounting. The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Method</th>
<th>Purpose</th>
<th>Consumption of items</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Create a purchase order directly from a project.</td>
<td>Use this method to purchase items from an external vendor for consumption on a project. You can create the purchase order in two ways:
<ul>
<li>From the project itself. In this case, the project is already defined for the purchase order.</li>
<li>By navigating to the project purchase order. (Click <strong>Project management and accounting</strong> &gt; <strong>Common</strong> &gt; <strong>Item tasks</strong> &gt; <strong>Project purchase orders</strong>.) You must select both the vendor and the project to create the purchase order for.</li>
</ul></td>
<td>Items are consumed when the vendor invoice is updated.</td>
</tr>
<tr class="even">
<td>Create a purchase order from a sales order.</td>
<td>Use this method to purchase items when you create a sales order from a project.</td>
<td>Items are consumed when the sales order is invoiced to the customer.</td>
</tr>
<tr class="odd">
<td>Create a purchase order from an item requirement.</td>
<td>Use this method to purchase items when you create an item requirement from a project.</td>
<td>Items are consumed when the item requirement packing slip is updated.</td>
</tr>
</tbody>
</table>

**Note:** When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.




<!--HONumber=Feb17_HO3-->


