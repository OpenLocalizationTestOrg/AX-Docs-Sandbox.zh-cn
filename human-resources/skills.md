---
title: Align workforce skills with business needs
description: You can track the skills that workers, applicants, or contact persons have, or should have, to fulfill their roles effectively. You can also specify the skills that are required for a specific job.
author: rschloma
manager: AnnBe
ms.date: 2015-09-10 20 - 48 - 50
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: kherr
ms.dyn365.ops.intro: 01-02-2016
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 40dfe11d7157af920061f5a4f7b8b8637243f21a
ms.lasthandoff: 02/22/2017


---

# <a name="align-workforce-skills-with-business-needs"></a>Align workforce skills with business needs

You can track the skills that workers, applicants, or contact persons have, or should have, to fulfill their roles effectively. You can also specify the skills that are required for a specific job.

Examples of skills you can track include the following:
-   Supervisory – Ability to supervise the work of others.
-   Leadership – Ability to lead employees and business domains.
-   Planning – Ability to look ahead, to form visions, and to see them through.
-   HTML – Ability to write HTML code.

Before you can assign a skill to a person or a job, create a skill-mapping search, or create a skill profile, you must enter information about the skills on the **Skills** page. For each skill, you can select a skill type and a rating model.

## <a name="rating-models"></a>Rating models
Rating models help evaluate a person's actual level of skill, the level they should work to achieve, or the level of skill that is required for a job. You can enter up to 10 levels for a rating model.  Each level in a rating model is assigned a factor.  The factor value will be used to normalize the scores of skills that use different rating models.  The factor must be a number between 0-9 and each level must have a unique factor.  Levels with higher factor values carry more weight in a rating model.
Specify job skills
-------------------

When you enter information about a job, you can specify the skills that a person should have to perform the work required for the job.  In addition you can specify the desired level for each skill as well the level of importance of the skill. Different jobs can require different levels of importance for the same skill.

## <a name="enter-skills-for-workers-applicants-or-contacts"></a>Enter skills for workers, applicants, or contacts
You can enter target skills or actual skills for workers, applicants, or contacts. A target skill is a skill that a person plans to achieve. An actual skill is a skill that a person currently has.

## <a name="skill-mapping-and-skill-mapping-profiles"></a>Skill mapping and Skill mapping profiles
You can create a skill-mapping search to find a worker, applicant, or contact person who is qualified to perform a specific type of task. Skill-mapping searches look across skills, education, certificates, positions of trust and project experience and return a results that match the criteria entered.  For example, it might be useful to know which workers in your organization earned their CPA.

Skill-mapping profiles allow you to find current employees or candidates with qualifications that directly correspond to business needs.  For example, you could create a skill-mapping profile for an open position in your organization. By creating a profile for a particular job and copying the skills, education and certificates from that job to the profile, you can quickly search workers, applicants and contact persons who match one or more of the criteria entered on the profile and view a list of the candidates whose skills most closely match the skills required for the job.
<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Note</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Only workers, applicants, and contact persons who are selected to be included in skill mapping searches can be displayed in a skill-mapping results list, or included in a skill profile. To include a worker, applicant, or contact person in skill mapping searches, set the <strong>Include in skill mapping</strong> selection to Yes in the following pages:
<ul>
<li>Worker</li>
<li>Employee</li>
<li>Applicant</li>
<li>Contacts</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="skill-gap-analysis-and-skill-profile-analysis"></a>Skill gap analysis and skill profile analysis
You can create a skill profile analysis to view a list of the competencies of a worker, applicant, or contact person as of a specific date. You can create a skill gap analysis to compare a person’s skills and the skills that are required for a specific job.  



<a name="see-also"></a>See also
--------

[Human resources](https://ax.help.dynamics.com/en/wiki/human-recources/)


