---
title: Set up training courses
description: Human resources administrators and managers can use the courses features to maintain information about the training that&quot;s offered to workers.
author: twheeloc
manager: AnnBe
ms.date: 2015-09-15 18 - 13 - 01
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: twheeloc
ms.dyn365.ops.intro: 01-02-2016
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: a5f501cc10cf191048c88dd9b2ba74285e888f80
ms.lasthandoff: 02/22/2017


---

# <a name="set-up-training-courses"></a>Set up training courses

Human resources administrators and managers can use the courses features to maintain information about the training that's offered to workers.

 <a name="set-up-prerequisites"></a>Set up prerequisites
---------------------

The following information is required and must be set up before you create courses.
-   **Course types**

The following information is optional information that you can specify for courses. If you know that you will be entering this information for courses, you should set up this information before you create course records.
-   **Classroom groups**
-   **Course groups**
-   **Course locations**
-   **Classrooms**
-   **Instructors**

## <a name="course-types"></a>Course types
You can use course types to categorize courses according to the structure or content of the course. You can create course types on the **Course types** page. You must select a course type when you create a course record.

## <a name="course-setup-type"></a>Course setup type
The following table lists the three setup types for courses. Setup types determine the structure of the course.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Setup type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Standard</strong></td>
<td>Select this type for courses that will not have a daily agenda. This is the default setup type when you create a new course.</td>
</tr>
<tr class="even">
<td><strong>Agenda</strong></td>
<td>Select this type to plan the details of each day of a course that takes place over multiple days.</td>
</tr>
<tr class="odd">
<td><strong>Agenda + session</strong></td>
<td>Select this type for the more complex courses. For example, you can divide the agenda for the course into tracks and sessions.
<ul>
<li><strong>Track</strong> – Tracks are specific subject areas for a course.</li>
<li><strong>Sessions</strong> – Sessions divide up tracks and help identify specific processes or techniques that are relevant to the track.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="course-tasks"></a>Course tasks
For each course, you can complete the following tasks.
-   Register participants
-   Specify a registration deadline
-   Define the minimum and maximum number of participants
-   Assign a course location and classroom
-   Recommend hotels to course participants
-   Create a course description, which you can then advertise on Employee self service

| **Note**                                                      |
|---------------------------------------------------------------|
| You can delete a course only if no one has registered for it. |

## <a name="course-statuses"></a>Course statuses
The following table lists the possible course statuses and the actions that you can complete when the course has a specific status.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Status</th>
<th>Actions</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Created</strong></td>
<td><ul>
<li>Enter and modify course information.</li>
<li>Change the course status to <strong>Open</strong> so that workers can register for the course.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Open</strong></td>
<td><ul>
<li>Register participants for the course.</li>
<li>Remove participants from the course.</li>
<li>Confirm participants for the course.</li>
<li>Change the course status to <strong>Closed</strong> or <strong>Canceled</strong>.</li>
<li>Plan questionnaires for participants whose status is <strong>Confirmed</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Closed</strong></td>
<td>You can reopen the course.</td>
</tr>
<tr class="even">
<td><strong>Canceled</strong></td>
<td>You can reopen the course.</td>
</tr>
</tbody>
</table>

## <a name="course-participants"></a>Course participants
Course participants are workers, applicants, or contact persons who participate in a training course or event. You can only register participants for open courses. The minimum and maximum number of participants that you can register for a course is defined on the **General** FastTab on the **Courses** page.
Workflow
--------

Employees who register for a course through the **Employee self service** page can have their registration routed through workflow for approval.  A workflow can be assigned to a course on the **General** FastTab on the **Courses** page.




