---
title: Workflow elements | Microsoft Docs
description: This article describes the various elements that make up a workflow.
author: sericks007
manager: AnnBe
ms.date: 2016-02-29 15:15:39
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks007
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 56441
ms.assetid: 64087b54-4ece-4f87-b2a7-a9ca55060254
ms.region: Global
ms.author: tjvass
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 1904b4604206e758b99d45fadeb359bd3e6fb861


---

# <a name="workflow-elements"></a>Workflow elements

This article describes the various elements that make up a workflow.

A workflow consists of elements. The sections that follow describe each type of element.

## <a name="tasks"></a>Tasks
A *task* is a unit of work that must be performed. Two types of tasks can be added to a workflow: manual tasks and automated tasks.

### <a name="manual-task"></a>Manual task

A *manual task* is a unit of work that must be performed by a user. For example, an expense report workflow can have manual tasks that require the assigned users to complete the following actions:

-   Review the receipts that are submitted together with an expense report.
-   Call an employee's manager.

### <a name="automated-task"></a>Automated task

An *automated task* is a unit of work that must be performed by the system. No human interaction is required. For example, a sales order workflow can have automated tasks that require the system to complete the following actions:

-   Perform a credit check.
-   Create a customer record for the customer, if a record doesn't already exist.

## <a name="approval-processes"></a>Approval processes
An *approval process* is a process that consists of separate steps. At each approval step, the user can perform the following actions:

-   Approve the document.
-   Reject the document.
-   Request a change to the document.
-   Assign the document to another user for approval.

## <a name="lineitem-workflow-elements"></a>Lineitem workflow elements
A workflow can be created to process either documents or the line items on a document. For example, you've created an approval workflow for timesheets. (We will refer to this workflow as the *document workflow*.) You can add a *line-item workflow* element to that document workflow. When the line-item element is run, each line item on the document is submitted for processing. You might want all the line items to be processed by the same line-item workflow, or you might want each line item to be processed by a different line-item workflow. Imagine that an employee has submitted a timesheet that resembles the following figure. ![Workflow with line items](./media/workflow_lineitemworkflow.gif) In this scenario, you might want to create the following line-item workflows:

-   **Line-item workflow 1** – This workflow is used to process line items where the project ID is 1111.
-   **Line-item workflow 2** – This workflow is used to process line items where the project ID is 2222.
-   **Line-item workflow 3** – This workflow is used to process line items where the project ID is 3333.

## <a name="flowcontrol-elements"></a>Flowcontrol elements
The following elements let you design workflows that have alternate branches or branches that run at the same time.

### <a name="manual-decision"></a>Manual decision

A *manual decision* is a point where a workflow divides into two branches. A user must make a decision, and this decision determines which branch is used to process the document that was submitted.

### <a name="conditional-decision"></a>Conditional decision

A *conditional decision* is also a point where a workflow divides into two branches. However, the system decides which branch is used to process the document that was submitted. To make this decision, the system evaluates the document to determine whether it meets specified conditions.

### <a name="parallel-activity"></a>Parallel activity

A *parallel activity* is a workflow element that includes two or more workflow branches that run at the same time.

### <a name="subworkflow"></a>Subworkflow

A *subworkflow* is a workflow that runs in the context of another workflow.




<!--HONumber=Feb17_HO3-->


