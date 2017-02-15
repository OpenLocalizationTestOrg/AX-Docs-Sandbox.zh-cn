---
title: Set up the advanced bank reconciliation import process | Microsoft Docs
description: The Advanced bank reconciliation feature lets you import electronic bank statements and automatically reconcile them with bank transactions in Microsoft Dynamics 365 for Operations. This article explains how to set up the import functionality for your bank statements.
author: twheeloc
manager: AnnBe
ms.date: 2016-08-10 17:50:36
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 106853
ms.assetid: 21ee7f94-7459-4d6a-8cd8-bd5c1507329e
ms.region: Global
ms.author: saraschi
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 2285ff43e7e8223ef6da8198c52d0a2296ddc3bb


---

# <a name="set-up-the-advanced-bank-reconciliation-import-process"></a>Set up the advanced bank reconciliation import process

The Advanced bank reconciliation feature lets you import electronic bank statements and automatically reconcile them with bank transactions in Microsoft Dynamics 365 for Operations. This article explains how to set up the import functionality for your bank statements.


The setup for bank statement import varies, depending on the format of your electronic bank statement. Microsoft Dynamics 365 for Operations supports three bank statement formats out of the box: ISO20022, MT940, and BAI2.

## <a name="sample-files"></a>Sample files
For all three formats, you must have files that translate the electronic bank statement from the original format to a format that Dynamics 365 for Operations can use. You can find the required resource files under the **Resources** node in Application Explorer in Microsoft Visual Studio. After you find the files, copy them to a single known location, so that you can more easily upload them during the setup process.

| Resource name                                           | File name                            |
|---------------------------------------------------------|--------------------------------------|
| BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt              | BAI2CSV-to-BAI2XML.xslt              |
| BankStmtImport\_BAI2XML\_to\_Reconciliation\_xslt       | BAI2XML-to-Reconciliation.xslt       |
| BankStmtImport\_BankReconciliation\_to\_Composite\_xslt | BankReconciliation-to-Composite.xslt |
| BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt   | ISO20022XML-to-Reconciliation.xslt   |
| BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt            | MT940TXT-to-MT940XML.xslt            |
| BankStmtImport\_MT940XML\_to\_Reconciliation\_xslt      | MT940XML-to-Reconciliation.xslt      |
| BankStmtImport\_SampleBankCompositeEntity\_xml          | SampleBankCompositeEntity.xml        |

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Examples of bank statement formats and technical layouts
Below are examples of the advanced bank reconciliation import file technical layout definitions and three related bank statement example files:

| Technical layout                                                                                                  | Bank statement example file                                                                                     |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [DynamicsAXMT940Layout](./media/dynamicsaxmt940layout1.xlsx)       | [MT940StatementExample](./media/mt940statementexample.pdf)       |
| [DynamicsAXISO20022Layout](./media/dynamicsaxiso20022layout1.xlsx) | [ISO20022StatementExample](./media/iso20022statementexample.pdf) |
| [DynamicsAXBAI2Layout](./media/dynamicsaxbai2layout1.xlsx)         | [BAI2StatementExample](./media/bai2statementexample.pdf)         |

 

## <a name="set-up-the-import-of-iso20022-bank-statements"></a>Set up the import of ISO20022 bank statements
First, you must define the bank statement format processing group for ISO20022 bank statements by using the data entity framework.

1.  Go to **Workspaces** &gt; **Data management**.
2.  Click **Import**.
3.  Enter a name for the format, such as **ISO20022**.
4.  Set the **Source data format** field to **XML-Element**.
5.  Set the **Entity name** field to **Bank statements**.
6.  To upload the import files, click **Upload**, and then browse to select the **SampleBankCompositeEntity.xml** file that you saved earlier.
7.  After the Bank statements entity is uploaded and the mapping is completed, click the **View map** action for the entity.
8.  The Bank statements entity is a composite entity that consists of four separate entities. In the list, select **BankStatementDocumentEntity**, and then click the **View map** action.
9.  On the **Transformations** tab, click **New**.
10. For sequence number 1, click **Upload file**, and select the **ISO20022XML-to-Reconciliation.xslt** file that you saved earlier. **Note:** Dynamics 365 for Operations transformation files are built for the standard format. Because banks often diverge from this format, you may have to update the transformation file to map to your bank statement format. For details about the expected format for ISO20022, see [Dynamics AX ISO20022 Layout](./media/dynamicsaxiso20022layout1.xlsx).
11. Click **New**.
12. For sequence number 2, click **Upload file**, and select the **BankReconciliation-to-Composite.xslt** file that you saved earlier.
13. Click **Apply transforms**.

After the format processing group is set up, the next step is to define the bank statement format rules for ISO20022 bank statements.

1.  Go to **Cash and bank management** &gt; **Setup** &gt; **Advanced bank reconciliation setup** &gt; **Bank statement format**.
2.  Click **New**.
3.  Specify a statement format, such as **ISO20022**.
4.  Enter a name for the format.
5.  Set the **Processing group** field to the group that you defined earlier, such as **ISO20022**.
6.  Select the **XML file** check box.

The last step is to enable Advanced bank reconciliation and set the statement format on the bank account.

1.  Go to **Cash and bank management** &gt; **Bank accounts**.
2.  Select the bank account, and open it to view the details.
3.  On the **Reconciliation** tab, set the **Advanced bank reconciliation** option to **Yes**.
4.  Set the **Statement format** field to the format that you created earlier, such as **ISO20022**.

## <a name="set-up-the-import-of-mt940-bank-statements"></a>Set up the import of MT940 bank statements
First, you must define the bank statement format processing group for MT940 bank statements by using the data entity framework.

1.  Go to **Workspaces** &gt; **Data management**.
2.  Click **Import**.
3.  Enter a name for the format, such as **MT940**.
4.  Set the **Source data format** field to **XML-Element**.
5.  Set the **Entity name** field to **Bank statements**.
6.  To upload import files, click **Upload**, and then browse to select the **SampleBankCompositeEntity.xml** file that you saved earlier.
7.  After the Bank statements entity is uploaded and the mapping is completed, click the **View map** action for the entity.
8.  The Bank statements entity is a composite entity that consists of four separate entities. In the list, select **BankStatementDocumentEntity**, and then click the **View map** action.
9.  On the **Transformations** tab, click **New**.
10. For sequence number 1, click **Upload file**, and select the **MT940TXT-to-MT940XML.xslt** file that you saved earlier.
11. Click **New**.
12. For sequence number 2, click **Upload file**, and select the **MT940XML-to-Reconciliation.xslt** file that you saved earlier. **Note:** Dynamics 365 for Operations transformation files are built for the standard format. Because banks often diverge from this format, you may have to update the transformation file to map to your bank statement format. For details about the expected format for MT940, see [Dynamics AX MT940 Layout](./media/dynamicsaxmt940layout1.xlsx)
13. Click **New**.
14. For sequence number 3, click **Upload file**, and select the **BankReconciliation-to-Composite.xslt** file that you saved earlier.
15. Click **Apply transforms**.

After the format processing group is set up, the next step is to define the bank statement format rules for MT940 bank statements.

1.  Go to **Cash and bank management** &gt; **Setup** &gt; **Advanced bank reconciliation setup** &gt; **Bank statement format**.
2.  Click **New**.
3.  Specify a statement format, such as **MT940**.
4.  Enter a name for the format.
5.  Set the **Processing group** field to the group that you defined earlier, such as **MT940**.
6.  Set the **File type** field to **txt**.

The last step is to enable Advanced bank reconciliation and set the statement format on the bank account.

1.  Go to **Cash and bank management** &gt; **Bank accounts**.
2.  Select the bank account, and open it to view the details.
3.  On the **Reconciliation** tab, set the **Advanced bank reconciliation** option to **Yes**.
4.  When you're prompted to confirm your selection and enable Advanced bank reconciliation, click **OK**.
5.  Set the **Statement format** field to the format that you created earlier, such as **MT940**.

## <a name="set-up-the-import-of-bai2-bank-statements"></a>Set up the import of BAI2 bank statements
First, you must define the bank statement format processing group for BAI2 bank statements by using the data entity framework.

1.  Go to **Workspaces** &gt; **Data management**.
2.  Click **Import**.
3.  Enter a name for the format, such as **BAI2**.
4.  Set the **Source data format** field to **XML-Element**.
5.  Set the **Entity name** field to **Bank statements**.
6.  To upload import files, click **Upload**, and then browse to select the **SampleBankCompositeEntity.xml** file that you saved earlier.
7.  After the Bank statements entity is uploaded and the mapping is completed, click the **View map** action for the entity.
8.  The Bank statements entity is a composite entity that consists of four separate entities. In the list, select **BankStatementDocumentEntity**, and then click the **View map** action.
9.  On the **Transformations** tab, click **New**.
10. For sequence number 1, click **Upload file**, and select the **BAI2CSV-to-BAI2XML.xslt** file that you saved earlier.
11. Click **New**.
12. For sequence number 2, click **Upload file**, and select the **BAI2XML-to-Reconciliation.xslt** file that you saved earlier. **Note:** Dynamics 365 for Operations transformation files are built for the standard format. Because banks often diverge from this format, and you may have to update the transformation file to map to your bank statement format. For details about the expected format for BAI2, see [Dynamics AX BAI2 Layout](./media/dynamicsaxbai2layout1.xlsx).
13. Click **New**.
14. For sequence number 3, click **Upload file**, and select the **BankReconciliation-to-Composite.xslt** file that you saved earlier.
15. Click **Apply transforms**.

After the format processing group is set up, the next step is to define the bank statement format rules for BAI2 bank statements.

1.  Go to **Cash and bank management** &gt; **Setup** &gt; **Advanced bank reconciliation setup** &gt; **Bank statement format**.
2.  Click **New**.
3.  Specify a statement format, such as **BAI2**.
4.  Enter a name for the format.
5.  Set the **Processing group** field to the group that you defined earlier, such as **BAI2**.
6.  Set the **File type** field to **txt**.

The last step is to enable Advanced bank reconciliation and set the statement format on the bank account.

1.  Go to **Cash and bank management** &gt; **Bank accounts**.
2.  Select the bank account, and open it to view the details.
3.  On the **Reconciliation** tab, set the **Advanced bank reconciliation** option to **Yes**.
4.  When you're prompted to confirm your selection and enable Advanced bank reconciliation, click **OK**.
5.  Set the **Statement format** field to the format that you created earlier, such as **BAI2**.

## <a name="test-the-bank-statement-import"></a>Test the bank statement import
The final step is to test that you can import your bank statement.

1.  Go to **Cash and bank management** &gt; **Bank accounts**.
2.  Select the bank account that Advanced bank reconciliation functionality is enabled for.
3.  On the **Reconcile** tab, click **Bank statements**.
4.  On the **Bank statement** page, click **Import statement**.
5.  Set the **Bank account** field to the selected bank account. The **Statement format** field will be set automatically, based on the setting on the bank account.
6.  Click **Browse**, and select your electronic bank statement file.
7.  Click **Upload**.
8.  Click **OK**.

If the import is successful, you will receive a message that states that your statement was imported. If the import wasn't successful, in the **Data management** workspace, in the **Job history** section, find the job. Click **Execution details** for the job to open the **Execution summary** page, and then click **View execution log** to view the import errors.




<!--HONumber=Feb17_HO3-->


