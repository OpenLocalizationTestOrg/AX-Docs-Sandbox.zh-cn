---
title: Create a department and associate it with the department hierarchy
description: A department is an operating unit that represents a category or functional area of an organization. A department is responsible for a specific area of the organization, such as sales, accounting, or human resources. You can use departments to report on functional areas. Departments might have profit and loss responsibility.
author: rschloma
manager: AnnBe
ms.date: 2016-03-08 22 - 24 - 49
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HierarchyDesigner, OMOperatingUnit
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: shielas
ms.dyn365.ops.intro: 01-02-2016
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 78e3babb242497be843b4202b5ccbfcf3a18057f
ms.lasthandoff: 02/22/2017


---

# <a name="create-a-department-and-associate-it-with-the-department-hierarchy"></a>Create a department and associate it with the department hierarchy

A department is an operating unit that represents a category or functional area of an organization. A department is responsible for a specific area of the organization, such as sales, accounting, or human resources. You can use departments to report on functional areas. Departments might have profit and loss responsibility.

A department might include a group of cost centers. Positions can be assigned to departments. To create a department, click **Human Resources** &gt; **Departments** &gt; **Department**. The following table describes the fields that are available.

| Field               | Description                                                                                                                                                                                                       |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Name                | Enter a name for the department.                                                                                                                                                                                  |
| Department number   | A default value might be generated automatically if a number sequence code is assigned to the **Organization number** reference on the **Number sequences** page.                                                 |
| Search name         | Enter a name or acronym that can be used to search for the department.                                                                                                                                            |
| Memo                | Enter any additional information here.                                                                                                                                                                            |
| In hierarchy        | A selected check box indicates that the department is included in the department hierarchy. For information about how to add a department to the department hierarchy, see the information later in this article. |
| DUNS number         | DUNS stands for Data Universal Number System. This is a nine-digit number that is issued by Dun & Bradstreet.                                                                                                     |
| Manager             | Enter the persona that manages the department.                                                                                                                                                                    |
| Addresses           | Add the address information for the department. For example, add the mailing address for the building that the department is located in.                                                                          |
| Contact information | Add contact information for the department. For example, add a telephone number for the service desk in the department.                                                                                           |

To add a department to the department hierarchy, follow these steps.

1.  Click **Human Resources** &gt; **Departments** &gt; **Department hierarchy**.
2.  Click **Edit**, and then select the organization that the department should be under.
3.  Click **Insert**, and select **Department** in the list.
4.  In the list of departments that appears, select the department to add to the hierarchy.
5.  Save your changes. You receive a message that a draft version of the hierarchy has been created.
6.  When you're ready, click **Publish** in the hierarchy designer. You can enter an effective date that indicates when the hierarchy should be published. For example, to add a new department at the beginning of the next calendar year, set the effective date to January 1 of the new calendar year. The changes to the hierarchy will take effect on that date.



