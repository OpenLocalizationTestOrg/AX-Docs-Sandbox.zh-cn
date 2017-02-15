---
title: Download Electronic reporting configurations from Lifecycle Services | Microsoft Docs
description: This topic explains how to download Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).
author: kfend
manager: AnnBe
ms.date: 2016-12-06 21:10:20
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: 71
ms.suite: Released- Dynamics AX application 7.0.1
ms.custom: 105843
ms.assetid: 67412c69-9aed-4f70-b834-55af71a40eb9
ms.region: Global
ms.author: nselin
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 787873acbe00bfe949a57e443eb927d4c6da209e


---

# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Download Electronic reporting configurations from Lifecycle Services

This topic explains how to download Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).

This tutorial guides you through the process of downloading the newest version of Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).

1.  Sign in to Dynamics 365 for Operations by using one of the following roles:
    -   Electronic reporting developer
    -   Electronic reporting functional consultant
    -   System administrator

2.  Go to **Organization administration** &gt; **Electronic reporting**.
3.  In the **Configuration providers** section, select the **Microsoft** tile.
4.  On the **Microsoft** tile, click **Repositories**. [![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)
5.  On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type. If this repository doesn't appear in the grid, follow these steps:
    1.  Click **Add** to add a new repository.
    2.  Select **LCS** as the repository type.
    3.  Click **Create repository**.
    4.  Enter a name and description for the repository.
    5.  Click **OK** to confirm the new repository entry.
    6.  In the grid, select the new repository of the **LCS** type.

6.  Click **Open** to view the list of ER configurations for the selected repository. [![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)
7.  In the configurations tree in the left pane, select the ER configuration that you require.
8.  On the **Versions** FastTab, select the required version of the selected ER configuration.
9.  Click **Import** to download the selected version from LCS to the current Dynamics 365 for Operations instance. **Note:** The **Import** button is unavailable for ER configuration versions that are already present in the current Dynamics 365 for Operations instance. [![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

**Note:** Depending on the ER settings, configurations are validated after they are imported. You might be notified about any inconsistency issues that are discovered. You must resolve those issues before you can use the imported configuration version. For more information, see the list of related articles for this topic.

<a name="see-also"></a>See also
--------

[Electronic reporting overview](https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/analytics-bi-reporting/general-electronic-reporting-ger)




<!--HONumber=Feb17_HO3-->


