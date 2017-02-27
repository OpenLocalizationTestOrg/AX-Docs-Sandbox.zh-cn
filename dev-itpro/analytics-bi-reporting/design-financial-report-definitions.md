---
title: Report definitions in financial report designer
description: This article provides information about report definitions. A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report. A report definition also provides options and settings that for customizing a report.
author: RobinARH
manager: AnnBe
ms.date: 2016-03-07 18 - 58 - 18
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: Management Reporter, Core
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.dyn365.ops.intro: 
ms.dyn365.ops.version: 
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: e46e832e0b35c506560a24710be4858b833c78e9
ms.lasthandoff: 02/22/2017


---

# <a name="report-definitions-in-financial-report-designer"></a>Report definitions in financial report designer

This article provides information about report definitions. A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report. A report definition also provides options and settings that for customizing a report. 

A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report. A report definition also provides options and settings that you can use to customize a report. After you define row definitions and column definitions, you must combine them in a report definition. At this point, you also define other aspects of the definitions, such as the detail level and report date. You can then save and generate a report. Financial reporting offers the following levels of detail:

-   Financial
-   Financial and Account
-   Financial, Account, and Transaction

However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.

## <a name="create-a-report-definition"></a>Create a report definition
1.  In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.
2.  Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.

## <a name="contents-of-a-report-definition"></a>Contents of a report definition
The following table describes the tabs in a report definition and how the information is used.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tab</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Report</td>
<td>Create a report, configure a report, or modify an existing report.</td>
</tr>
<tr class="even">
<td>Output and Distribution</td>
<td>Change the output type and destination of the report.</td>
</tr>
<tr class="odd">
<td>Headers and Footers</td>
<td>Define and format the headers and footers for the report. For example, you can add text or images to the header or footer. Financial reporting supports .bmp, .jpg, and .png files for images. You can also add autotext codes to insert other information, such as a company name, report name, or page number.</td>
</tr>
<tr class="even">
<td>Settings</td>
<td>Specify report definition settings, such as the following settings:
<ul>
<li>Formatting and rounding amounts</li>
<li>Format detail reports</li>
<li>Format reporting trees</li>
<li>Generate an exception report</li>
<li>Specify currency conversion</li>
<li>Subtotal and filter account details</li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a>See also
--------

[Financial reporting for Microsoft Dynamics AX](financial-reporting-intro.md)


