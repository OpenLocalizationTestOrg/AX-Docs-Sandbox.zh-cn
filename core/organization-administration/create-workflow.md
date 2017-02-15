---
title: Create a workflow | Microsoft Docs
description: This topics explains how to create a workflow.
author: sericks007
manager: AnnBe
ms.date: 2016-09-30 15:53:09
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: 71
ms.suite: Released- Dynamics AX platform update 2
ms.custom: 195583
ms.assetid: 99ac4b6d-cd1d-49d6-82bc-092fac3ca5bb
ms.region: Global
ms.author: donaldc
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: e063953616bb8a1aafc0d461c190bc0cce8b997b


---

# <a name="create-a-workflow"></a>Create a workflow

This topics explains how to create a workflow.

<a name="open-the-workflow-editor"></a>Open the workflow editor
------------------------

The Microsoft Dynamics 365 for Operations module that you're working in determines the types of workflow that you can create. Follow these steps to select the type of workflow to create and open the workflow editor.

1.  Open the module that you want to create a new workflow for. For example, to create a workflow for purchase requisitions, click **Procurement and sourcing**.
2.  Click **Setup** &gt; **\[Module name\] workflows**.
3.  On the list page that appears, on the Action Pane, click **New**.
4.  On the **Create workflow** page, select the type of workflow to create, and then click **Create workflow**. The workflow editor appears. You can now use the following procedures to design the workflow.

## <a name="drag-workflow-elements-onto-the-canvas"></a>Drag workflow elements onto the canvas
The **Workflow elements** area of the workflow editor contains the elements that you can add to your workflow. To add elements to the workflow, drag them onto the canvas.

## <a name="connect-the-elements"></a>Connect the elements
To connect one workflow element to another, hold the pointer over an element until connection points appear. Click a connection point, and drag it to another element. Be sure to connect all the elements.

## <a name="configure-the-properties-of-the-workflow"></a>Configure the properties of the workflow
Follow these steps to configure the properties of the workflow.

1.  Click the canvas to make sure that no workflow element is selected.
2.  Click **Properties** to open the **Properties** page for the workflow.
3.  Follow the procedures in the [Configure the properties of a workflow](http://axhelp.dynamics.com/en/wiki/configure-the-properties-of-a-workflow/) topic.

## <a name="configure-the-elements-of-the-workflow"></a>Configure the elements of the workflow
Configure each element that you dragged onto the canvas. For information about how to configure each workflow element, see the following topics:

-   [Configure a manual task](https://docs.microsoft.com/en-us/dynamics365/operations/core/organization-administration/configure-a-manual-task)
-   [Configure an automated task](https://docs.microsoft.com/en-us/dynamics365/operations/core/organization-administration/configure-an-automated-task)
-   [Configure an approval process](https://docs.microsoft.com/en-us/dynamics365/operations/core/organization-administration/configure-an-approval-process)
-   [Configure an approval step](https://docs.microsoft.com/en-us/dynamics365/operations/core/organization-administration/configure-an-approval-step)
-   [Configure a manual decision](https://docs.microsoft.com/en-us/dynamics365/operations/core/organization-administration/configure-a-manual-decision)
-   [Configure a conditional decision](https://docs.microsoft.com/en-us/dynamics365/operations/core/organization-administration/configure-a-conditional-decision)
-   [Configure a parallel activity](https://docs.microsoft.com/en-us/dynamics365/operations/core/organization-administration/configure-a-parallel-activity)
-   [Configure a parallel branch](http://ax.help.dynamics.com/en/wiki/configure-a-parallel-branch/)
-   [Configure a line-item workflow](https://docs.microsoft.com/en-us/dynamics365/operations/core/organization-administration/configure-a-line-item-workflow)

## <a name="resolve-any-errors-or-warnings"></a>Resolve any errors or warnings
The **Errors and warnings** pane at the bottom of the workflow editor shows messages that have been generated for the workflow. To find the element where an error or warning occurred, double-click the error or warning message. You must resolve all errors and warnings before you can make the workflow active.

## <a name="save-and-activate-the-workflow"></a>Save and activate the workflow
When you're ready to save and activate the workflow, follow these steps.

1.  Click **Save and close** to close the workflow editor and open the **Save workflow** page.
2.  Enter comments about the changes that you've made to the workflow, and then click **OK**.
3.  If all errors and warnings have been resolved, the **Activate workflow** page appears. Select one of the following options:
    -   To activate this version of the workflow, click **Activate the new version**. When a workflow is active, users can submit documents to it for processing.
    -   If you don't want to activate this version, click **Do not activate the new version**. You can activate the workflow later.






<!--HONumber=Feb17_HO3-->


