---
title: Recently added editing features in task recorder | Microsoft Docs
description: If you use task recorder to create task guides, you can edit your files more efficiently using the functionality described in this wiki.
author: josaw1
manager: AnnBe
ms.date: 2017-01-09 19:16:36
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.suite: Released- Dynamics AX platform update 2
ms.custom: 266464
ms.assetid: 0306195d-6f09-42d5-b932-ad0501289c0f
ms.region: global
ms.author: josaw
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 8ccae22b1a9e3c8a4063a869d766f14eda5e669f


---

# <a name="recently-added-editing-features-in-task-recorder"></a>Recently added editing features in task recorder

If you use task recorder to create task guides, you can edit your files more efficiently using the functionality described in this wiki.

These features are available on the **Settings &gt; Task recorder &gt; Edit recording** menu.

-   Insert steps without re-recording the entire file.
-   Move steps under a sub-task without re-recording the entire file.
-   Collapse Recording name and description fields.

## <a name="insert-steps-without-rerecording-the-entire-file"></a>Insert steps without rerecording the entire file
You can now add a step anywhere in a task guide without playing back or re-recording the entire file.

1.  Select the step after which you want the new step to be inserted. Make sure the step is highlighted.

In order for task recorder to insert a step, you must have the correct page open. The correct page is the page on which the new step occurs. Task recorder has a mechanism that determines what the active page is, and will disable the functionality if the correct page isn’t open. [![tg1](./media/tg1.png)](./media/tg1.png) When you are on the correct page, **Insert step** becomes available.

[![tg2](./media/tg2-231x300.png)](./media/tg2.png)

2. Click **Insert step**.

When you click **Insert step**, Task recorder switches to record mode. Any action taken in the UI will now be recorded and added in-place as steps.

3. Click **Stop**.

You can repeat the process, adding as many steps or moving as many sub-tasks as needed (see below for sub-tasks).

4. When you are done editing the task guide, click **Done editing**, and then choose one of the options to save or publish the task guide.

## <a name="move-steps-under-a-subtask-without-rerecording-the-entire-file"></a>Move steps under a subtask without rerecording the entire file
You can move steps under a sub-task without playing back or re-recording the entire file. You can also move the sub-task step or the end sub-task step if you want to group an existing block of steps.

1.  Select the step or sub-task step that you want to move. Make sure that the step is highlighted.
2.  Click the ellipsis, then click **Move step after**.

[![tg3](./media/tg3.png)](./media/tg3.png)

3. Select the step or sub-task step that you want to move the step or sub-task step after. Task recorder will move the step.

4. To move the end sub-task step, select it, click the ellipsis, click **Move step after**, and then select the step after which you want the end sub-task step to be.

If you want the first step in the task guide to be within a sub-task, create a sub-task step as the second step, and then move the first step into it. You can add or move as many steps or sub-tasks as needed.

5. When you are done editing the task guide, click **Done editing**, and then choose one of the options to save or publish the task guide.

## <a name="collapse-recording-name-and-description"></a>Collapse Recording name and description
You can expand and collapse the **Recording name** and **Recording description** fields. When these fields are collapsed, more steps will be visible in the Task recorder editing pane. [![tg4](./media/tg4-300x252.png)](./media/tg4.png)  

<a name="see-also"></a>See also
--------

[Task Recorder in Microsoft Dynamics 365 for Operations](https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/user-interface/task-recorder-in-ax7)

[Create documentation or training using Task recordings](https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/user-interface/task-recorder)

[Task recorder quick reference](https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/user-interface/task-recorder-quick-reference)




<!--HONumber=Feb17_HO3-->


