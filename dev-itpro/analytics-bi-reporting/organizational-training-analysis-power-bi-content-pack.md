---
title: Organizational Training content pack for Power BI | Microsoft Docs
description: This topic describes the Dynamics 365 for Operations - Organizational Training content pack for Power BI. It explains how to access the content pack, and describes the data model and entities that were used to build the content pack.
author: twheeloc
manager: AnnBe
ms.date: 2016-12-15 14:45:28
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: 71
ms.suite: Released- Dynamics 365 for Operations version 1611
ms.custom: 263874
ms.assetid: dca7e205-3532-41f4-8e72-09d7dfcbbf21
ms.region: Global
ms.author: jcart
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 0494f5b372af542f7f3f2b55b1ac247c05d74055


---

# <a name="organizational-training-content-pack-for-power-bi"></a>Organizational Training content pack for Power BI

This topic describes the Dynamics 365 for Operations - Organizational Training content pack for Power BI. It explains how to access the content pack, and describes the data model and entities that were used to build the content pack.

<a name="accessing-the-content-pack"></a>Accessing the content pack
--------------------------

You can find the Organizational Training content pack in the Shared assets library in Microsoft Dynamics Lifecycle Services (LCS). For more information about how to download the content pack and connect it to your Microsoft Dynamics 365 for Operations data, see [Power BI content from Microsoft and your partners](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/12/12/power-bi-content-from-microsoft-and-your-partners/).

## <a name="reports-that-are-included-in-the-content-pack"></a>Reports that are included in the content pack
After you’ve connected the content pack to your Dynamics 365 for Operations data, the reports show your organization's data. If you’ve never used Microsoft Power BI before, you can learn more about it on the [Guided Learning page for Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). The reports that are included in the content pack have both charts and tables that contain additional information. The following table describes the reports.

| Report          | Contents                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| Course Analysis | Registration by location, course attendees by status, and registration list |
| Course Types    | Course types by skill                                                       |

You can filter the charts and tiles on these reports, and pin the charts and tiles to the dashboard. For more information about how to filter and pin in Power BI, see [Create and Configure A Dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Understanding the data model and entities
Dynamics 365 for Operations data is used to populate the reports in the Organizational Training content pack. The following table shows the entities that the content pack was based on.

| Entity                    | Contents                                                         | Relationships with other entities                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Training\_CalendarOffset  | Calendar offsets to slice reports                                | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Company         | Companies to filter reports by                                   | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Course          | Course, description, instructor name, location, room, and status | Training\_CourseAgenda Training\_CourseAttendees Training\_CourseSkill                                                                                                                             |
| Training\_CourseAgenda    | Agenda, course, and start and end times                          | Training\_Company Training\_CalendarOffset Training\_Date Training\_Course                                                                                                                         |
| Training\_CourseAttendees | Name, status, job, and registration date                         | Training\_Company Training\_CalendarOffset Training\_Date Training\_Demographics Training\_Employment Training\_Course Training\_WorkerName Training\_WorkerTitle Training\_Job Training\_Position |
| Training\_CourseSkill     | Skill, skill type, and level                                     | Training\_Course                                                                                                                                                                                   |
| Training\_Date            | Days, weeks, months, and years                                   | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Demographics    | Date of birth, gender, ethnic origin, and marital status         | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Employment      | Start date, end date, and transition date                        | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Job             | Function, type, and title                                        | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Position        | Position, title, and full-time equivalent (FTE)                  | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_WorkerName      | First name, last name, and full name                             | Training\_CourseAttendees                                                                                                                                                                          |
| Training\_WorkerTitle     | Title and seniority date                                         | Training\_CourseAttendees                                                                                                                                                                          |

These entities were used to create calculated measures in the data model. These calculated measures are then used to calculate the key performance indicators (KPIs) and reports that are used in the content pack. If you want to include additional calculations on your reports and dashboard, you can download and modify the Training.pbix file from LCS. This file is the default data model that was used to create the content pack. After you've made modifications, you can create an organizational content pack and dashboard that contain the information that you’ve added.

## <a name="additional-resources"></a>Additional resources
Here are some helpful links that are related to entities and building Power BI content:

-   [Data entities](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Creating organizational content packs](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Data modeling using Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Adding Power BI tiles to workspaces](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





<!--HONumber=Feb17_HO3-->


