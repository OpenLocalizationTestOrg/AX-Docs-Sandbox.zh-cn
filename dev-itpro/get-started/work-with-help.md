---
title: Working with Help | Microsoft Docs
description: This topic describes the components of the Help system for Microsoft Dynamics 365 for Operations, and provides an overview of how to connect them and a summary of how to create custom help.
author: margoc
manager: AnnBe
ms.date: 2015-12-03 22:12:49
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 16141
ms.assetid: ff404e0e-5b22-413c-8f4d-974ac3ee1885
ms.region: Global
ms.author: margoc
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 070db80238d6472711c3978481f161a01cd27161


---

# <a name="working-with-help"></a>Working with Help

This topic describes the components of the Help system for Microsoft Dynamics 365 for Operations, and provides an overview of how to connect them and a summary of how to create custom help. 

<a name="help-architecture"></a>Help architecture
-----------------

The following illustration shows the parts of the Dynamics 365 for Operations help system. The in-product help system pulls articles from the Dynamics 365 for Operations Help Wiki, as well as task guides stored in Business Process Modeler in Microsoft Dynamics Lifecycle Services (LCS). **Note** The features listed in the diagram with an asterisk (\*) are on our roadmap, but are not available yet. [![Help architecture](./media/help-architecture-1024x800.png)](./media/help-architecture.png)

## <a name="connecting-the-help-system"></a>Connecting the help system
Using the System Parameters form, system administrators connect the pieces of the help system for an implementation. [![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) On the **System parameters** page, follow these steps:

1.  **Important:** The first time you open the Help tab, you must connect to Lifecycle Services. Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click OK to get to the parameters form.[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)
2.  Select the Lifecycle Services project to connect to.
3.  Select the BPM libraries (within the selected project) to retrieve task recordings from.
4.  Set the display order of the BPM libraries. This determines the order in which task recordings from the libraries will appear in the **Help** pane.

After you complete these steps, you can open the Help pane and click the Task guides tab. You'll now see the task guides that apply to the page that you’re currently on in Dynamics 365 for Operations. If no task guides are found, you can enter keywords to refine your search.

### <a name="showing-translated-task-guides"></a>Showing translated task guides

Translated task guides were shipped in the May APQC Unified Library, and the Getting Started library. In Dynamics 365 for Operations, to see localized task guide help, make sure that you are connected to the May library. The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**. **Note:** Even though many task guides have been translated, right now the Dynamics 365 for Operations client is not showing the translated task guide names. Also, only the task guides that were released in February are available in translation in the May library at this point. We will release an updated library with additional translations.

-   If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.
-   If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.

## <a name="creating-custom-help"></a>Creating custom help
You can create custom help for your Dynamics 365 for Operations implementation by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library. For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers. You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes. For more information, see the topic [How to create a task recording to use as documentation or training](https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/user-interface/task-recorder)..

<a name="see-also"></a>See also
--------

[Microsoft Dynamics AX Help – Getting started](https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/system-administration/help-get-started)

[How to create a task recording to use as documentation or training](https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/user-interface/task-recorder)

[Creating New Training Libraries for Dynamics AX within Lifecycle Services using the Task Recorder (External link)](https://docs.com/mufife/163372c6-f366-4c5a-94fa-93e2c25f878a/creating-new-training-libraries-for-dynamics-ax)




<!--HONumber=Feb17_HO3-->


