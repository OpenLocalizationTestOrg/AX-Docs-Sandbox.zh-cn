---
title: Configure an automated task in a workflow | Microsoft Docs
description: This topic explains how to configure the properties for an automated task.
author: sericks007
manager: AnnBe
ms.date: 2016-09-16 19:48:24
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: 71
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 192061
ms.assetid: 8ddba2a8-f075-477f-838a-5cdeb0980528
ms.region: Global
ms.author: donaldc
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 29f099393bc1d092c76adfc44bad7a39abeb0f19


---

# <a name="configure-an-automated-task-in-a-workflow"></a>Configure an automated task in a workflow

This topic explains how to configure the properties for an automated task.

To configure an automated task in the workflow editor, right-click the task, and then click **Properties** to open the **Properties** page. Then use the following procedures to configure the properties for the automated task.

## <a name="name-the-task"></a>Name the task
Follow these steps to enter a name for the automated task.

1.  In the left pane, click **Basic Settings**.
2.  In the **Name** field, enter a unique name for the task.

## <a name="specify-when-notifications-are-sent"></a>Specify when notifications are sent
You can send notifications to people when an automated task has been run or canceled. Follow these steps to specify when notifications are sent, and who they are sent to.

1.  In the left pane, click **Notifications**.
2.  Select the check box next to the events to send notifications for:
    -   **Execution** – Notifications are sent when the task has been run.
    -   **Canceled** – Notifications are sent when the task has been canceled.

3.  Select the row for an event that you selected in step 2.
4.  On the **Notification text** tab, in the text box, enter the text of the notification.
5.  To personalize the notification, you can insert placeholders. Placeholders are replaced with appropriate data when the notification is shown to users. Follow these steps to insert a placeholder:
    1.  In the text box, click where the placeholder should appear.
    2.  Click **Insert placeholder**.
    3.  In the list that appears, select the placeholder to insert.
    4.  Click **Insert**.

6.  To add translations of the notification, follow these steps:
    1.  Click **Translations**.
    2.  On the page that appears, click **Add**.
    3.  In the list that appears, select the language that you're entering the text in.
    4.  In the **Translated text** field, enter the text.
    5.  To personalize the text, you can insert placeholders as described in step 5.
    6.  Click **Close**.

7.  On the **Recipient** tab, specify who the notifications are sent to. Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Option</th>
    <th>Notification recipients</th>
    <th>Additional steps</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Participant</td>
    <td>Users who are assigned to a specific group or role</td>
    <td><ol>
    <li>After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</li>
    <li>In the <strong>Participant</strong> list, select the group or role to send notifications to.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Workflow user</td>
    <td>Users who participate in the current workflow</td>
    <td><ul>
    <li>After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td>User</td>
    <td>Specific Microsoft Dynamics 365 for Operations users</td>
    <td><ol>
    <li>After you select <strong>User</strong>, click the <strong>User</strong> tab.</li>
    <li>The <strong>Available users</strong> list includes all Dynamics 365 for Operations users. Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  Repeat steps 3 through 7 for each event that you selected in step 2.





<!--HONumber=Feb17_HO3-->


