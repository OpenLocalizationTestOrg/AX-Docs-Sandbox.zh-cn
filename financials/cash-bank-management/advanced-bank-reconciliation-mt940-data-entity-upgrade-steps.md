---
title: "Advanced bank reconciliation MT940 Import – Composite data entity upgrade | Microsoft Docs"
description: A sequence number needs to be added to the bank statement import entity to support the MT940 format.
author: twheeloc
manager: AnnBe
ms.date: 2016-10-31 16:22:02
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: 101
ms.suite: Released- Dynamics 365 for Operations version 1611
ms.custom: 221594
ms.assetid: 3480d617-15c9-4afb-bf22-28043b41fbb8
ms.region: Global
ms.author: saraschi
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: b3ada9af865bdfdbeae954a58a5762ab29d84acf


---

# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a>Advanced bank reconciliation MT940 Import – Composite data entity upgrade

A sequence number needs to be added to the bank statement import entity to support the MT940 format.


Use the following steps to add the bank statement import entity to support the MT940 format.

1.  Compile and synchronize the following:
    -   Composite Entity\\BankStatementImportEntity
    -   Entity\\BankStatementBalanceEntity
    -   Entity\\BankStatementDocumentEntity
    -   Entity\\BankStatementEntity
    -   Entity\\BankStatementLineEntity
    -   Tables\\BankStatementStaging

2.  Data management\\data projects.
    1.  Load MT940 import project(s)
        1.  Change XSLT.
            -   Click **View map**.
            -   Click **View map** on the bank statement document.
            -   Click **Transformations**
            -   Delete the BankReconiliation-to-Composite.xslt file.
            -   Add the new version of BankReconiliation-to-Composite.xsl.

        2.  Expose the **Sequence Number** on **Source Data** layout.
            1.  Source data format = XML-Element.
            2.  Entity name = Bank statements.
            3.  Upload data file = new version SampleBankCompositeEntity.xml.
            4.  Click **Yes** to overwrite the existing file.
            5.  Click **Yes** to generate a new mapping.
            6.  Verify that S**equenceNumber** is mapped.
                -   Click **View Map** on the statement entity.
                -   Verify that **SequenceNumber** is mapped from Source to Staging.

3.  Import the new statement.





<!--HONumber=Feb17_HO3-->


