---
title: Batch attributes | Microsoft Docs
description: This article provides information about batch attributes. Batch attributes are characteristics of raw materials and finished products that make up inventory batches. The article also explains how to assign batch attributes, and how you can search on them when you reserve batches.
author: YuyuScheller
manager: AnnBe
ms.date: 2015-12-07 09:17:04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: PdsBatchAttrib, PdsBatchAttribAssociate, PdsBatchAttribByAttribGroup, PdsBatchAttribByItem, PdsBatchAttribByitemCustomer, PdsBatchAttribGroup
audience: Application User
ms.reviewer: YuyuScheller
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 19271
ms.assetid: 199c0eed-5b57-4e19-8d32-a3cfdd991f77
ms.region: Global
ms.industry: Manufacturing
ms.author: yuyus
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: eb381410f82d11a0c1cd71649d53db10f6f07e76


---

# <a name="batch-attributes"></a>Batch attributes

This article provides information about batch attributes. Batch attributes are characteristics of raw materials and finished products that make up inventory batches. The article also explains how to assign batch attributes, and how you can search on them when you reserve batches.

Batch attributes are characteristics of raw materials and finished products that make up inventory batches. Batch attributes can vary, depending on factors such as environmental conditions, the quality of the raw materials that are used to produce the batch, or the outcome of the finished product. The number and types of batch attributes that are used can vary widely from one industry to another. Here are two examples that show how to use batch attributes:

-   In the cheese industry, milk, which is one of the raw materials that are used to produce the cheese, can have attributes such as fat content and percentage weight. The cheese that is produced from the milk can have other attributes, such as moisture and age.
-   In the steel industry, the iron that is produced might have attributes such as the percentages of magnesium content, silver content, and zinc content.

To better manage the number and types of attributes, you can use batch attribute groups. In this way, you don't have to add each attribute individually.

## <a name="assign-batch-attributes"></a>Assign batch attributes
You can assign batch attributes to individual products that are held in inventory batches, or you can assign them to products that are associated with specific customers. Before you can assign a batch attribute at the customer level, you must assign it at the product level. The product must have the batch dimension set to **Active** in the tracking dimension group. To assign a batch attribute to an individual product, use the product-specific page. If the attribute is specific to a product for a customer, use the customer-specific page. When you add an attribute to a product, you also define other parameters. Here are some examples:

-   The minimum and maximum ranges for an attribute of the **Integer** or **Fraction** type.
-   The tolerance actions for an attribute of the **Integer** or **Fraction** type. If the value of the attribute falls outside the minimum and maximum range, the action can be either a warning message or an error message.
-   The target value for the attribute. This value is the optimal value of the attribute, and it applies to all attribute types.

You can access the pages for products that you select on the **Released products** page in Product information management. After you assign batch attributes to a product, you can add specific values to the attributes on the **Inventory batch attributes** page.

## <a name="reserve-batches"></a>Reserve batches
You can search on batch attributes when you do batch reservations for a sales order to fullfill a customer's order, or when you pick and reserve batches for a production order. The search helps locate an inventory batch that contains the product that has the batch attribute that you want. After you locate the batch or batches, you can reserve the product to the originating inventory transaction line.




<!--HONumber=Feb17_HO3-->


