---
title: Procurement and sourcing workflows | Microsoft Docs
description: Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction. To set up an approval process, you can create a workflow.
author: YuyuScheller
manager: AnnBe
ms.date: 2015-09-10 08:04:44
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: 2084
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 2074
ms.assetid: ed9c20b5-eea0-438a-a332-621f6b0b75c2
ms.region: Global
ms.author: mkirknel
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 97fdf4ded9f71c1fd1dd3949b988cc6a8f1cb0c9


---

# <a name="procurement-and-sourcing-workflows"></a>Procurement and sourcing workflows

Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction. To set up an approval process, you can create a workflow.

A workflow represents a business process. It defines how a document flows through the system and indicates who must complete a task or approve a document. There are several benefits of using the workflow system in your organization:
-   Consistent processes— You can define the approval process for specific documents, such as purchase requisitions and expense reports. Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.
-   Process visibility— You can track the status, history, and performance metrics of a specific workflow instance. This helps you determine whether changes should be made to the workflow to improve efficiency.
-   Centralized work list— Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in. This is available in the Work items page.

## <a name="the-types-of-workflows-that-you-can-create"></a>The types of workflows that you can create
The following workflow types are available for Procurement and sourcing.

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| **Type**                         | **Use this type to**                                          |
| Purchase requisition review      | Create review workflows for purchase requisitions.            |
| Purchase requisition line review | Create review workflows for purchase requisition lines.       |
| Purchase order workflow          | Create review and approval workflows for purchase orders.     |
| Purchase order line workflow     | Create review and approve workflows for purchase order lines. |

## <a name="creating-a-workflow"></a>Creating a workflow
To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create. In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow. The workflow elements should be configured. For approval and task workflow elements you can configure which participant should take action.
Types of participants
----------------------

You can assign an approval step to the following groups of participants.

| User group    | Description                                                               |
|---------------|---------------------------------------------------------------------------|
| Participant   | Assign the approval step to members of a group or role.                   |
| Hierarchy     | Assign the approval step to users in a specific organizational hierarchy. |
| Workflow user | Assign the approval step to users of this workflow.                       |
| Queue         | Assign the approval step to a work item queue.                            |
| User          | Assign the approval step to specific users.                               |



<a name="see-also"></a>See also
--------

[Defining business process workflows for purchase requisitions](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

[Purchase requisition workflow](https://docs.microsoft.com/en-us/dynamics365/operations/manufacturing/procurement-sourcing/purchase-requisition-workflow)




<!--HONumber=Feb17_HO3-->


