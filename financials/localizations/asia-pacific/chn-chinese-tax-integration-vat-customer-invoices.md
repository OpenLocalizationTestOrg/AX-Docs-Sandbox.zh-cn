---
title: (CHN) Chinese tax integration modification for VAT customer invoices FAQ
description: You can generate value-added tax (VAT) customer invoices, and then export them as text files. You can then import reference numbers for the VAT customer invoices that can be linked to the original invoices.
author: ShylaThompson
manager: AnnBe
ms.date: 2016-12-19 21 - 21 - 02
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations
ms.custom: 264894
ms.assetid: 9d255220-9a19-4436-87a6-f78d92c02062
ms.search.region: China (PRC)
ms.author: leguo
ms.dyn365.ops.intro: 01-11-2016
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 51ef7c32e90102cc5ed259d426afeb7c7e299056
ms.lasthandoff: 02/22/2017


---

# <a name="chn-chinese-tax-integration-modification-for-vat-customer-invoices-faq"></a>(CHN) Chinese tax integration modification for VAT customer invoices FAQ

You can generate value-added tax (VAT) customer invoices, and then export them as text files. You can then import reference numbers for the VAT customer invoices that can be linked to the original invoices.

Before you export a VAT customer invoice, you can split the VAT customer invoice to create multiple invoice documents. You can also combine multiple VAT customer invoices to create one invoice export document that contains the line details of the original invoices.
What is a VAT customer invoice?
-------------------------------

A VAT customer invoice is generated when you post a customer transaction that uses the sales tax group for VAT and the item sales tax group for VAT. You can generate a VAT customer invoice from a sales order, return sales order, credit note, free text invoice, or project sales invoice.
Can I create one tax integration profile for multiple types of documents?
-------------------------------------------------------------------------

Yes. You can create one tax integration profile for multiple types of documents.

## <a name="when-should-i-split-a-vat-customer-invoice"></a>When should I split a VAT customer invoice?
You should split a VAT customer invoice if the **Over amount limit** check box is selected on the **VAT invoice integration** page. The **Over amount limit** option is selected for the invoices that have a total invoice amount that exceeds the amount limit that you specify in the **Maximum invoice amount** field on the **Tax integration profiles** page.

## <a name="which-vat-customer-invoices-can-i-combine"></a>Which VAT customer invoices can I combine?
You can combine VAT customer invoices that use the same invoice account number and sales tax code.

## <a name="how-many-times-can-i-export-an-invoice"></a>How many times can I export an invoice?
You can only export an invoice one time.
Can I customize or add new information on VAT customer invoices?
----------------------------------------------------------------

Yes. You can customize VAT customer invoices by adding other fields, and then export the VAT customer invoices as text files.

To customize VAT customer invoices to include other details, follow these steps:

-   On the **Electronic reporting** page, select **Reporting configurations** to open **Configurations**, and select **Golden Tax(CN)** in the tree.
-   Click **Designer**. Add other fields on the tree under **Exported Invoices** &gt; **Invoices**, and save the GER model.
-   Click **Map model to data source** and select **Golden Tax **&gt; **Designer**.

To map the added fields to table, follow these steps:
1.  Click **Save** and return to **Configurations**.
2.  Select **GoldenTax(CN)** in the tree.
3.  Click **Change status** &gt; **Complete** to get a new version of the model.
4.  Expand **GoldenTax(CN)** in the tree.
5.  Select **GoldenTax(CN)** format in the tree.
6.  Click **Rebase**.** **Confirm that the target version is the new completed version.
7.  Click **OK** to finish the rebase process.
8.  Click **Designer** to open format designer.
9.  In the format designer, add new fields in the tree present in text files.
10. Select the newly added field, and click the **Mapping** tab in the right pane.
11. Expand the model in the tree.
12. Select new added model field and click **Bind**.
13. Click **Save** to save format mapping.
14. Click **Change status** &gt; **Complete** to get a new version.



<a name="see-also"></a>See also
--------

[Configure tax integration for China](configure-tax-integration-china.md)

[Import the Chinese Golden Tax data entity](import-chinese-golden-tax-data-entity.md)


