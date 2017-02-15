---
title: Vendor collaboration invoicing workspace | Microsoft Docs
description: This topic explains how you can view vendor invoices and submit invoices from the vendor collaboration invoicing workspace.
author: twheeloc
manager: AnnBe
ms.date: 2016-10-31 16:21:43
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: 2231
ms.suite: Released- Dynamics 365 for Operations version 1611
ms.custom: 221534
ms.assetid: 9505749e-847d-440b-a2dc-45d7857434f6
ms.region: Global
ms.author: abruer
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: b404501e6e576f418523f2bfe9f3c64c77485218


---

# <a name="vendor-collaboration-invoicing-workspace"></a>Vendor collaboration invoicing workspace

This topic explains how you can view vendor invoices and submit invoices from the vendor collaboration invoicing workspace.

The **Vendor collaboration invoicing** workspace can be used to view vendor invoice information and to submit invoices to Microsoft Dynamics 365 for Operations using workflow capabilities.
Vendor collaboration invoicing workspace
----------------------------------------

### <a name="summary-tiles"></a>Summary tiles

The **Summary** tiles give an overview of the invoices for the selected vendor. You can view invoices by their state.
-   Draft invoices have not been submitted to workflow.
-   Submitted, not approved invoices are those invoices that the vendor has submitted, but they have not been posted in Dynamics 365 for Operations.
-   Approved, not paid invoices are those that have been posted in Dynamics 365 for Operations, but they have not yet been fully paid.
-   Paid invoices are those that have been fully paid in Dynamics 365 for Operations.

Clicking on a tile will open a filtered view of the **Invoices list** page.
### <a name="tabular-lists"></a>Tabular lists

In the **Tabular lists** section, the status of the invoicing is broken down in similar ways as the summary tiles: Draft and Submitted, not approved lists. While in the Draft state, an invoice can be submitted to workflow or deleted. The last tabular list is an option to find invoices. You can filter as you search, to allow for faster searches.
All vendor invoices list page
-----------------------------

You can view all posted and unposted vendor invoices on the **Vendor collaboration invoices** list page. You can use this list page to view the payment status of the invoices. The payment statuses include Unposted, Unpaid, Partially paid, and Fully paid.
Creating a new invoice from a purchase order
--------------------------------------------

You can create a new vendor invoice by selecting the **New** action on the **Vendor collaboration invoicing** workspace. The purchase order number and invoice number must be provided by the vendor. By default, all of the lines from the vendor's purchase order will appear on the new invoice. The quantity and cost information can be edited prior to submitting the vendor invoice to workflow. You can attach files, notes, images, and URLs to an invoice before submitting it.



<a name="see-also"></a>See also
--------

[Collaborating with vendors by using the Vendor portal](https://docs.microsoft.com/en-us/dynamics365/operations/manufacturing/procurement-sourcing/collaborating-with-vendors-using-the-vendor-portal)




<!--HONumber=Feb17_HO3-->


