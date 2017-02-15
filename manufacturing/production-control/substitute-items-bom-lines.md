---
title: Material substitution in manufacturing | Microsoft Docs
description: This topic describes how to substitute materials during the production process.
author: YuyuScheller
manager: AnnBe
ms.date: 2016-03-23 19:04:15
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: ProdBOM
audience: Application User
ms.reviewer: annbe
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 70171
ms.assetid: 3f9735eb-a755-4eab-87f8-12d68647a691
ms.region: Global
ms.industry: Manufacturing
ms.author: johanho
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: dd96602e5b12424fd14f4e00cd8dd572c2af5e1e


---

# <a name="material-substitution-in-manufacturing"></a>Material substitution in manufacturing

This topic describes how to substitute materials during the production process. 

There are three methods for substituting materials during the production process:

-   By date, when one material is substituted for another after a specific date
-   During master planning, when a material in a formula is substituted with a different material, because it's out of stock
-   During production, when a material is unexpectedly out of stock and is substituted with a different material

## <a name="substituting-material-by-date"></a>Substituting material by date
Consider following scenario: A machine that a company is manufacturing contains a component that will expire from the vendor's catalog in two months. From the expiration date onward, the vendor will offer a new component that can be substituted for the old component. From and to validity dates can be set up on bill of materials (BOM) lines. For this example, you set up the old component to expire by entering the expiration date in the **To-date** field. Then, on the BOM, you set up the new, replacement component so that it's valid from the day after the old component expires. To do this, enter the start date in the **From-date** field.

## <a name="substituting-material-by-planning"></a>Substituting material by planning
You can substitute materials during planning only when you're using formulas, not when you're using a BOM. Consider following scenario: A food manufacturing company is making a sauce from a formula that has 20 ingredients. One ingredient in the formula can be substituted by one of two other ingredients. However, because these two ingredients are more expensive than the preferred ingredient, substitution is used only if the preferred ingredient is out of stock. The material that can be substituted is called A, whereas the two materials that can replace it are called B and C. Material substitution by planning is controlled by the **Plan group** and **Priority** fields on the formula lines. For this example, you create formula lines for the three materials, and associate the formula lines with the same plan group. In the setup, the formula line for material A has the highest priority (lowest number), the formula line for material C has the lowest priority, and the formula line for material B has a priority that is between the priority of the other two lines. If you have demand for the finished item, master planning first determines whether the demand for material A can be covered. If the demand can't be covered, master planning looks at materials B and C, in order of priority. If material B is on hand, it will be used after a planned batch order is firmed for the formula. If none of the materials are on hand, master planning creates a planned order for material A. **Note:** When you set up formula lines in a plan group, you should specify a quantity only on the material that has the highest priority. This quantity will be used to calculate the demand of all materials in the plan, even the materials that have lower priority. You can't specify different quantities on lower-priority items in the plan group.

## <a name="substituting-material-during-production"></a>Substituting material during production
Consider the following scenario: A piece of metal plate is required for a welding operation. During the operation, a warehouse worker informs the machine operator that the plate is out of stock. However, it's decided that the plate can be substituted with a plate that is slightly thicker. That way, the operation can be finalized. Material can be added to the BOM for an open production order. If the production order has a status of **Started**, users are asked to re-estimate the order when they add a new item to the production BOM. After the material is added, a new picking list can be created for the new item. You don't have to add the new material to the production BOM. Instead, you can add it directly to the production picking list. Then, when the picking list is posted, the system adds the material to the production BOM.




<!--HONumber=Feb17_HO3-->


