---
title: Budget planning integration with other modules | Microsoft Docs
description: 
author: twheeloc
manager: AnnBe
ms.date: 2016-03-10 10:09:48
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 64443
ms.assetid: 82c7b874-416a-4c4d-b577-ee0be43b3f10
ms.region: Global
ms.author: sigitac
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: f6987e0a80e1b6c913eee32eb5da1ec951e9f09a


---

# <a name="budget-planning-integration-with-other-modules"></a>Budget planning integration with other modules



<a name="periodic-processes-for-generating-budget-plans"></a>Periodic processes for generating budget plans
----------------------------------------------

Budget plans can be generated from the following resources:

-   General ledger transactions
-   Fixed assets
-   Forecast positions
-   Project forecasts
-   Supply forecasts
-   Demand forecasts
-   Budget register entries
-   Other budget plans

The basic elements of the periodic process are the same for all the processes. Tabs let you define the source of the data, the target (budget plan) attributes, and options to run the process in the background as a batch process. Later sections of this article describe items that might not be apparent in each process.

### <a name="actions"></a>Actions

For each generation process, three actions are available:

-   **Create a new budget plan** creates a new plan that has the attributes that are selected in the **Target **section. These attributes don't have to be unique. Therefore, two plans can have the same name and other values.
-   **Replace the existing budget plan scenario** deletes all data in the target budget plan in the selected budget plan scenario and creates new lines that use the selected source data.
-   **Update the existing budget plan scenario, and append new data** updates existing lines in the target plan that match the source lines and adds new lines for new data. The matching is based on the ledger account, date, budget class, and various other fields. For example, when you generate budget plans from forecast positions, the position number is an important field. All lines that have a position number that matches the source position number are replaced with the new lines from the source.

### <a name="source"></a>Source

For all processes, the **Source** tab lets you filter data by using the **Filter** button. By default, specific fields are added to the filter for each process. For example, for the **Generate budget plan from general ledger** process, the **Ledger account** and **Main account** categories are available, and appear on the generation page. Any fields that you add to the filter are also added to the page, together with with any criteria that you add.

### <a name="target"></a>Target

The **Historical** option on the **Target** tab lets you use the dates from the source data as the effective date in the budget plan. Typically, the effective date must be within the plan’s budget cycle. When you set the **Historical** option to **Yes**, the date (even the year) of the source is used, so that you can use past data as a basis for comparison. You can't modify historical data in the budget plan, and the plan is set to an approved workflow status. However, you can reset the status if you must other scenarios in the plan require changes. The **Aggregate total by** field at the top of the page also determines the date that is used. This field totals amounts, and optionally sets the effective date to the first day of the fiscal year or fiscal period. Many of the fields on the **Target** tab become editable or read-only, depending on the action that you select. When you change from creating a new budget plan to updating an existing plan, the **Budget plan name** field becomes unavailable, and the fields that are related to selecting an existing plan become available. On both the **Target** tab and the **Source **tab, the **Ledger** field is always unavailable, because the value is determined by the selected budget planning process. The **Budget class** field lets you set the budget plan lines as either expense transactions or revenue transactions. Usually, revenue transactions are credits to a ledger account and are therefore stored as negative amounts. Typically, these transactions also appear as negative amounts in the budget plan. However, by adding the budget class as a field in the plan layout, you can enable revenue to appear as positive amounts.

### <a name="generation-rules"></a>Generation rules

Three fields provide additional functionality: **Factor**, **Minimum**, and **Rounding** **rule**. The value in the **Factor** field is multiplied by the source amount to set the amount in the budget plan. You can then make adjustments when you create budget plan lines. For example, you can enter **1.03** for a 3 percent increase. The factor must be a positive number. The **Minimum** field lets you set the threshold amount for creating a budget plan line. If the source amount is less than this number, the budget plan line isn't created. A value of **0.00** allows all amounts but doesn't limit lines to positive amounts. (No value limits lines to positive amounts. Negative amounts are always included and usually represent credit entries.) The **Rounding rule** field lets you set the precision of the budget plan lines that are created. You can round amounts to the nearest 1.00, 10.00, 100.00, and so on, of currency.

## <a name="notes-for-specific-processes"></a>Notes for specific processes
### <a name="generate-budget-plan-from-general-ledger"></a>Generate budget plan from general ledger

When you create a budget plan from general ledger data, you must set the **Aggregate total by** field to **Fiscal year** if the **Historical** option is set to **No**. The periods and dates in the source might not match the periods in dates in the target. Because the process has no reliable way to map these values, you must limit the process to the first of the year. In the target, the **Budget class** field is set to either **Expense** or **Revenue**. This setting is used to select the **Budget type** attribute for lines that are created, when the main account on a line isn't of the **Revenue** or **Expense** type.

### <a name="generate-budget-plan-from-fixed-assets"></a>Generate budget plan from fixed assets

The **Generate budget plan from fixed assets** process has no option for aggregating by period or day. There is also no option for setting the plan as historical. You can use this periodic process to include projected transactions for fixed assets in your budget planning.

### <a name="generate-budget-plan-from-forecast-positions"></a>Generate budget plan from forecast positions

The **Generate budget plan from forecast positions** process assigns the source forecast position to the budget plan line. You can view the position by adding the forecast position as a row in the budget plan layout or by using the **Budget plan lines** inquiry. If you don't want the forecast position to be assigned to budget plan lines, set the **Include position in budget plan line** option to **No**. Lines in the budget plan are aggregated by ledger account and position. However, you can exclude the position number, so that lines are aggregated by ledger account only. On the **Target** tab, set the **Include position in budget plan** option to **No**. In the **Budget plan FTE scenario** field, you can select a scenario to include the number of full-time equivalents (FTEs) in the budget plan. This field is limited to quantity-type scenarios that are included in the layout of the target budget plan. If you select an FTE scenario, you must also select an FTE main account. This account is used to create the quantity budget plan lines. The budget planning process and budget plan scenario that are selected in the source set the target scenario budget planning process and scenario. Because these attributes are assigned to forecast positions, they must match the budget plan. Therefore, these attributes can't be modified on the target.

### <a name="generate-budget-plan-from-project-forecasts"></a>Generate budget plan from project forecasts

The **Generate budget plan from project forecasts** process, like the **Generate budget plan from forecast positions** process, has an option to include project quantities (hours, expenses, and items) in a quantity scenario. The two process also have similar filters for the columns in the budget plan layout. On the **Source** tab, three options in the **Include statement** section determine which budget plan lines are created. These options are the same as the options that are available when you create budget register entries directly from project forecasts. Set the **Profit and loss** option to **Yes** to create lines for costs and for revenues. Set the **WIP** option to **Yes** to create work in process entries. Set the **Payroll allocation** option to **Yes** to create lines for the payroll offset accounts for hour transactions. There is no **Budget class** field, because the budget class (**Expense** or **Revenue**) is determined by the source. You can use project budgets as a source by selecting the forecast model that contains the project budget amounts. Remember that project budgets create project forecast entries as they are approved. To select only costs or revenues for budget plan lines, use the filter to select **Budget updates: Amount type = Cost**. To select only one type of forecast, use the filter to select **Budget updates: Transaction type = *xxx***. Only one forecast model can be used to generate a budget plan scenario. If you run the process for one forecast model, and then do an update and try to specify another model, the first model will be overwritten if the same project and ledger accounts apply. To generate a budget plan scenario from more than one forecast model, generate into different budget plan scenarios, and use allocation options to add them together in another scenario. The **Generate budget plan from project forecasts** process also assigns the source project to the budget plan line.

### <a name="generate-budget-plan-from-supply-forecast"></a>Generate budget plan from supply forecast

The source filter options in the **Generate budget plan from supply forecast** process were modeled after options in the **Transfer purchase budget to ledger** function, because of similarities between the process and the function.

### <a name="generate-budget-plan-from-demand-forecast"></a>Generate budget plan from demand forecast

For the **Generate budget plan from demand forecast** process, you can set the **Sales order** option to **Yes** to generate revenue lines in the budget plan, set the **Consumption** to **Yes** to create expense lines, or set both options to **Yes**.

### <a name="generate-budget-plan-from-budget-register-entries"></a>Generate budget plan from budget register entries

For the **Generate budget plan from budget register entries** process, the source must specify one submodel, one budget code, and one entry number. In other words, you can create budget plan lines for only one budget register entry at a time. You can use additional entries in the same budget plan by running the process one time for each source entry.

### <a name="generate-budget-plan-from-budget-plan"></a>Generate budget plan from budget plan

For the **Generate budget plan from budget plan** process, an additional set of options on the **Target** tab lets you assign new financial dimensions. If a financial dimension is selected, that value will be used for all budget plan lines. Therefore, you can use one budget plan as the basis for other budget plans, but can also assign, for example, a different department or cost center to the new budget plans.

## <a name="looking-back-from-the-budget-plan"></a>Looking back from the budget plan
### <a name="budget-plans-by-dimension-set-inquiry"></a>Budget plans by dimension set inquiry

The **Budget plans by dimension set** inquiry includes several options that let you run a query to help identify the source of the budget plan data. Select a line and click the **Budget plan lines** button to run the **Budget plan lines** query. The results are filtered for the dimension values of the selected line. You can then apply additional parameters. Use the **Supply forecast** and **Demand forecast** buttons run these queries. In both cases, the query searches for forecast lines that could have created the budget plan lines. Additional reports that are available include the **Forecast positions by budget plan** report. This report is especially useful when you want to determine whether a position has been correctly allocated to budget plans.




<!--HONumber=Feb17_HO3-->


