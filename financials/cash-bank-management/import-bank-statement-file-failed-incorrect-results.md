---
title: Bank statement file import troubleshooting
description: It&quot;s important that the bank statement file from the bank match the layout that Microsoft Dynamics 365 for Operations supports. Because of strict standards for bank statements, most integrations will work correctly. However, sometimes the statement file can&quot;t be imported or has incorrect results. Typically, these issues are caused by small differences in the bank statement file. This article explains how to fix these differences and resolve the issues.
author: twheeloc
manager: AnnBe
ms.date: 2016-08-18 15 - 22 - 16
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: saraschi
ms.dyn365.ops.intro: 01-02-2016
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 58c2057fa6141544d0ce8e86beb49331e1f1e192
ms.lasthandoff: 02/22/2017


---

# <a name="bank-statement-file-import-troubleshooting"></a>Bank statement file import troubleshooting

It's important that the bank statement file from the bank match the layout that Microsoft Dynamics 365 for Operations supports. Because of strict standards for bank statements, most integrations will work correctly. However, sometimes the statement file can't be imported or has incorrect results. Typically, these issues are caused by small differences in the bank statement file. This article explains how to fix these differences and resolve the issues.

<a name="what-is-the-error"></a>What is the error?
------------------

After you try to import a bank statement file, go to the Data management job history and its execution details to find the error. The error can help by pointing to the statement, balance, or statement line. However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.

## <a name="what-are-the-differences"></a>What are the differences?
Compare the bank file layout definition to the Microsoft Dynamics 365 for Operations import definition, and note any differences in the fields and elements. Compare the bank statement file to the related sample Dynamics 365 for Operations file. In the ISO20022 files, any differences should be easy to see.

## <a name="transformations"></a>Transformations
Typically, the change must be made in one of three transformations. Each transformation is written for a specific standard.

| Resource name                                         | File name                          |
|-------------------------------------------------------|------------------------------------|
| BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt            | BAI2CSV-to-BAI2XML.xslt            |
| BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt | ISO20022XML-to-Reconciliation.xslt |
| BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt          | MT940TXT-to-MT940XML.xslt          |

## <a name="debugging-transformations"></a>Debugging transformations
### <a name="adjust-the-bai2-and-mt940-files"></a>Adjust the BAI2 and MT940 files

The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging. The program makes this adjustment when a file is imported.

1.  Create an XML file, and copy the following text into it.

        <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>

2.  Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.

### <a name="debug-the-xslt"></a>Debug the XSLT

For more information, see <https://msdn.microsoft.com/en-us/library/ms255605.aspx>.

1.  Start Microsoft Visual Studio.
2.  Create a console application.
3.  Open the appropriate XSLT.
4.  Click the XLST and its properties page.
5.  Set the input to the location of the bank statement file.
6.  Define a location and file name for the output.
7.  Set the required break points.
8.  On the menu, click **XML** &gt; **Start XSLT Debugging**.

### <a name="format-the-xslt-output"></a>Format the XSLT output

When the transformation runs, it creates an output file that you can view in Visual Studio. Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.

### <a name="adjust-the-transformation"></a>Adjust the transformation

Adjust the transformation to get the appropriate field or element in the bank statement file. Then map that field or element to the appropriate Dynamics 365 for Operations element.

### <a name="debitcredit-indicator"></a>Debit/credit indicator

Sometimes, debits might be imported as credits, and credits might be imported as debits. To resolve this issue, you must change the appropriate XSLT. If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.

-   BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template
-   ISO20022XML-to-Reconcilation.xslt GetCreditDebit template
-   MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Examples of bank statement formats and technical layouts
The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.

| Technical layout definition                                                                                       | Bank statement example file                                                                                     |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [DynamicsAXMT940Layout](./media/dynamicsaxmt940layout1.xlsx)       | [MT940StatementExample](./media/mt940statementexample.pdf)       |
| [DynamicsAXISO20022Layout](./media/dynamicsaxiso20022layout1.xlsx) | [ISO20022StatementExample](./media/iso20022statementexample.pdf) |
| [DynamicsAXBAI2Layout](./media/dynamicsaxbai2layout1.xlsx)         | [BAI2StatementExample](./media/bai2statementexample.pdf)         |




