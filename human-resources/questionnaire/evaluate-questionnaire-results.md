---
title: View and evaluate the results of a questionnaire | Microsoft Docs
description: This article explains how you can view and evaluate the results of questionnaires that respondents complete.
author: twheeloc
manager: AnnBe
ms.date: 2015-12-04 18:36:29
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: KMCollection, KMKnowledgeCollectorCollection, KMKnowledgeCollectorUserResults
audience: Application User
ms.reviewer: twheeloc
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 17444
ms.assetid: 9150ed48-e3b8-4944-b9ad-8b751933f250
ms.region: Global
ms.author: twheeloc
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: c8a2eeb3ab7ef0f4729f7a5297f28cc28e116fd4


---

# <a name="view-and-evaluate-the-results-of-a-questionnaire"></a>View and evaluate the results of a questionnaire

This article explains how you can view and evaluate the results of questionnaires that respondents complete. 

After respondents complete a questionnaire, you can view and evaluate the questionnaire results in the following ways:

-   **Completed answer sessions** – View details about the questionnaires that respondents have completed, and generate reports to summarize answers and any points that were earned.
-   **Result groups** – View result group details and statistics for questionnaires. Result group statistics can be generated for either a single answer session  of a questionnaire or all answer sessions.
-   **Questionnaire statistics** – Specify criteria to calculate statistics for a specific group of respondents.

You can also generate various reports to view results that are sorted by person, answer session, or result group. The following reports that are related to completed questionnaires are available:

-   Answers
-   Answers per questionnaire
-   Answers per person
-   Feedback analysis

## <a name="answer-session-results"></a>Answer session results
After respondents complete a questionnaire, you can view the results of the completed answer sessions. An answer session is one user’s response to a questionnaire. You can view details about completed answer sessions on the **Answers** page. The answer sessions that are included on the **Answers** page are filtered in various ways, depending on how you open the page:

-   All questionnaires
-   A specific questionnaire
-   A specific person

From the **Answers** page, you can view details about answers, points that were earned, a respondent’s responses in each result group, and the question hierarchy that was used on the selected questionnaire, if a question hierarchy was used. You can also generate and print the following reports:

-   **Results report** – This report shows a graphical representation of the points that were earned per result group for the selected answer session.
-   **Answer report** – This report shows the answers that the respondent selected for each question on the questionnaire.
-   **Incorrect answers** – This report shows information that is related to the incorrect answers that the respondent selected.

**Note:** The **Results** report is available only if you use results groups on the questionnaire, and if you selected **Results page** on the **Questionnaires** page. The **Answer** report and the **Incorrect answers** report are available only if you selected **Answer report** on the **Questionnaires** page.

## <a name="questionnaire-statistics"></a>Questionnaire statistics
You can use questionnaire statistics to analyze the results of a completed questionnaire, based on calculations that you define. To define calculations, you must complete the following tasks:

-   Select criteria to calculate and display the statistics.
    -   You can show statistics by questionnaire, questions, question rows, or results groups.
    -   Select the type of chart that will be used when you view results.
    -   Select the types of people from the network, such as employees, contact persons, or applicants, to include answers for. You can also include answers from questionnaires that were completed anonymously.
    -   Set up intervals that are based on age or seniority to analyze results.
-   Select or verify settings that refine the subject of the statistics. For example, by selecting a ZIP Code or postal code, you can analyze results for all respondents within a specific geographic area.
-   Select or verify criteria to analyze results by respondent or questionnaire characteristics. For example, by selecting **ZIP/postal code**, you can analyze the correlation between a respondent’s location and correct answers.

The settings that you define are saved and can be used to periodically recalculate results.

<a name="see-also"></a>See also
--------

[Designing questionnaires](https://docs.microsoft.com/en-us/dynamics365/operations/human-resources/questionnaire/designing-questionnaires)

[Using questionnaires](https://docs.microsoft.com/en-us/dynamics365/operations/human-resources/questionnaire/using-questionnaires)

[Distributing and completing questionnaires](https://docs.microsoft.com/en-us/dynamics365/operations/human-resources/questionnaire/distributing-questionnaires)




<!--HONumber=Feb17_HO3-->


