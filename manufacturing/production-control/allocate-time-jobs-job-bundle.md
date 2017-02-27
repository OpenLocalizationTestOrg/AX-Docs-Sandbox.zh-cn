---
title: Allocate time to jobs in a job bundle
description: In Manufacturing execution, you can bundle jobs. You can then start multiple jobs at the same time on the Job list page.
author: YuyuScheller
manager: AnnBe
ms.date: 2016-02-25 13 - 04 - 25
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: JmgBundleSlize, JmgProdParameters, JmgRegistration
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations
ms.custom: 55591
ms.assetid: 358efce7-73c8-4d2a-a7f7-cb99b88ab6ee
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.dyn365.ops.intro: 01-02-2016
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 23c33365756232e8355e1ba11b119dc1b20df9ce
ms.lasthandoff: 02/22/2017


---

# <a name="allocate-time-to-jobs-in-a-job-bundle"></a>Allocate time to jobs in a job bundle

In Manufacturing execution, you can bundle jobs. You can then start multiple jobs at the same time on the Job list page.

If you bundle jobs, you must define how the total registered time for all the jobs should be allocated to each job. You define the allocation by selecting one of the following options in the **Bundle type** field on the **Allocation keys** page:

-   **Estimation** – Time is divided among the jobs, based on the estimated time for the jobs.
-   **Jobs** – Time is divided according to total jobs that are bundled and how much time was spent finishing all the jobs.
-   **Net time** – Time is divided equally among the jobs that are in the bundle at any time.
-   **Real time** – Actual job time is allocated. The cost can be calculated based on the actual payroll cost. **Note:** The **Real time** allocation key is available only if your company uses the payroll functionality in Time and attendance.

The following examples show the results of the various allocation keys.

## <a name="example-scenario"></a>Example scenario
Three jobs in your job queue must be completed. You start the first job, and then, while that job is in progress, you start the second and third jobs. Therefore, there is a bundle of three jobs. The following table shows the estimated production time for each job.

| Job   | Production time |
|-------|-----------------|
| Job 1 | 1 hour          |
| Job 2 | 3 hours         |
| Job 3 | 4 hours         |
| Total | 8 hours         |

The following table shows the actual work hours that are spent on each job.

| Job    | Start time | End time | Bundle time |
|--------|------------|----------|-------------|
| Job 1  | 09:00      | 11:00    | 2 hours     |
| Job 2  | 10:00      | 13:00    | 3 hours     |
| Job 3  | 10:00      | 15:00    | 5 hours     |
| Bundle | 09:00      | 15:00    | 6 hours     |

The following sections describe the results of the calculated time for each allocation key.

## <a name="estimation-allocation-key"></a>Estimation allocation key
The following table illustrates the formula for calculating allocated time. Here is the formula: Time per job = Total bundle time × (Estimated job time ÷ Total estimated time)

| Job   | Formula           | Allocated time |
|-------|-------------------|----------------|
| Job 1 | 6 × (1 ÷ 8) hours | 0.75 hour      |
| Job 2 | 6 × (3 ÷ 8) hours | 2.25 hours     |
| Job 3 | 6 × (4 ÷ 8) hours | 3.00 hours     |

## <a name="jobs-allocation-key"></a>Jobs allocation key
The following table illustrates the formula for calculating allocated time. Here is the formula: Time per job = Total bundle time ÷ Number of jobs

| Job   | Formula | Allocated time |
|-------|---------|----------------|
| Job 1 | 6 ÷ 3   | 2 hours        |
| Job 2 | 6 ÷ 3   | 2 hours        |
| Job 3 | 6 ÷ 3   | 2 hours        |

## <a name="net-time-allocation-key"></a>Net time allocation key
The following table illustrates the formula for calculating allocated time. Here is the formula: Calculated time per reporting = Bundle time ÷ Number of jobs

|                              | 09:00–10:00 (1 hour) | 10:00–11:00 (1 hour) | 11:00–13:00 (2 hours) | 13:00–15:00 (2 hours) | Allocated time |
|------------------------------|----------------------|----------------------|-----------------------|-----------------------|----------------|
| Number of jobs in the bundle | 1                    | 3                    | 2                     | 1                     | Not applicable |
| Job 1                        | 1 ÷ 1 = 1 hour       | 1 ÷ 3 = 0.33 hour    | Not applicable        | Not applicable        | 1.33 hours     |
| Job 2                        | Not applicable       | 1 ÷ 3 = 0.33 hour    | 2 ÷ 2 = 1 hour        | Not applicable        | 1.33 hours     |
| Job 3                        | Not applicable       | 1 ÷ 3 = 0.33 hour    | 2 ÷ 2 = 1 hour        | 2 ÷ 1 = 2 hours       | 3.33 hours     |

## <a name="real-time-allocation-key"></a>Real time allocation key
If you want production costs to be calculated based on real costs, you must clear the **Cost category** option on the **Production order defaults** page. The following table illustrates the formula for calculating allocated time. Here is the formula: Actual time per job = Actual time in bundle

| Job   | Actual time |
|-------|-------------|
| Job 1 | 2 hours     |
| Job 2 | 3 hours     |
| Job 3 | 5 hours     |

Consider the three jobs that are performed by a worker who has an hourly wage of USD 12.00. No overtime bonus or premium was earned in the time that was spent on the jobs. The worker worked on the three bundled jobs for a total of six hours. Therefore, the salary cost is 6 × USD 12.00 = USD 72.00. When you use real-time allocation, the cost per hour is recalculated by using the factor from the Net time formula. The actual time that was spent on each job is then transferred together with the corrected cost price per hour. In the example, six hours are spent, although 10 hours were allocated. The following table illustrates the formula for calculating cost. Here is the formula: Cost per hour = (Total bundle time per job (Net time) ÷ Actual time per job) × Standard cost price per hour

| Job   | Calculation of corrected cost per hour | Corrected cost per hour | Allocated time | Total cost of job |
|-------|----------------------------------------|-------------------------|----------------|-------------------|
| Job 1 | (1.33 ÷ 2) × USD 12.00                 | USD 8.00                | 2 hours        | USD 16.00         |
| Job 2 | (1.33 ÷ 3) × USD 12.00                 | USD 5.33                | 3 hours        | USD 16.00         |
| Job 3 | (3.33 ÷ 5) × USD 12.00                 | USD 8.00                | 5 hours        | USD 40.00         |

The corrected cost per hour and the job time are posted in a production journal. **Note:** If you select the **Cost category** option on the **General** tab on the **Production order defaults** page, the actual time for each job is transferred to a production journal, where the cost is applied to the cost category of the specific job.


