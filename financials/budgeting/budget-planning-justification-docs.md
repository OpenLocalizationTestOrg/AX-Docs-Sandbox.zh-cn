---
title: Budget planning justification documents
description: Justification documents provide a narrative for those requesting a budget to explain why a specific budget is necessary.
author: twheeloc
manager: AnnBe
ms.date: 2016-11-28 18 - 47 - 11
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: ryansand
ms.dyn365.ops.intro: 01-11-2016
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 2a60970e6fc31de5f5c38ba1cbb6a9101b45de99
ms.lasthandoff: 02/22/2017


---

# <a name="budget-planning-justification-documents"></a>Budget planning justification documents

Justification documents provide a narrative for those requesting a budget to explain why a specific budget is necessary. 

A budget plan template is created by the budget manager in Microsoft Word and assigned to the current budget planning process. Budget owners can then open the template and have data automatically populated in Word based on their budget request. They can then add additional text or data prior to saving and attaching their personalized justification document to their budget plan.

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a>Set up Microsoft Dynamics Office Add-in for Microsoft Word

1.  Open a new Microsoft Word document.
2.  Click **Insert** on the ribbon, and click **Store**.
3.  Search for Microsoft Dynamics Office Add-in and click **Add**.
4.  In Word, in the right pane, click **Add server information**.
5.  Type or paste the server URL and click **OK**.

##### <a name="define-the-justification-template-in-microsoft-word"></a>Define the Justification template in Microsoft Word

1.  Click **Design** in the Microsoft Dynamics Office Add-in after you’ve logged in.
2.  For header information, use the **Add fields** button.
3.  Select the entity data source of BudgetPlanJustification, and click **Next**. **Note:** This entity is required for any justification document. Other entities can be used but the upload back to Microsoft Dynamics 365 for Operations will fail if this entity isn’t included.
4.  Add the BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter, and DocumentNumber labels and values in the Word document. **Note:** You can use your own custom labels, rather than the standard labels, if needed.
5.  Click **Done** to complete the header section.
6.  For line level detail of budget plan amounts, click **Add table**.
7.  Again, select the entity data source of BudgetPlanJustification, and click **Next**.
8.  Add fields for EffectiveDate, ScenarioName, AccountDisplayValue, and AccountingCurrencyExpenseAmount. **Note:** If comments are available to add within individual budget plan lines, those can be added to the table here.
9.  Add any additional instructions to provide to the end user, and perform any necessary formatting or styling to the document.
10. Save the document to your local computer and close the file before continuing.

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a>Set up the Budget planning process to use the Justification template

1.  In Microsoft Dynamics 365 for Operations, go to **Budgeting** &gt; **Setup** &gt; **Budget planning** &gt; **Justification document templates**.
2.  Click **New** and browse to your newly created Microsoft Word document.
3.  Enter a template display name and description. Click **OK**.
4.  Go to **Budgeting** &gt; **Setup** &gt; **Budget** **planning** &gt; **Budget planning process**.
5.  Select the process where the justification template should be used, and click **Edit**.
6.  In the **Justification document template** field, select the appropriate template and save.

##### <a name="edit-and-save-personalized-justification-documents"></a>Edit and save personalized justification documents

1.  In Dynamics 365 for Operations, create a new budget plan or open an existing budget plan.
2.  In the **Justification** drop-down menu, select **Create new justification**.
3.  After filling in the details, select to upload the personalized document from the **Justification** drop-down menu.



