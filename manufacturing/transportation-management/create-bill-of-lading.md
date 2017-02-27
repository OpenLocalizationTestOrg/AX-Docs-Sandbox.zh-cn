---
title: Create a bill of lading
description: This topic describes how to create a bill of lading when using warehouse management processes.
author: YuyuScheller
manager: AnnBe
ms.date: 2016-09-22 12 - 00 - 26
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench
audience: Application User
ms.search.scope: AX 7.0.0, Operations
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: yuyus
ms.dyn365.ops.intro: 01-02-2016
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 291517734440a94c757b6c8aa97d76d19970d090
ms.lasthandoff: 02/22/2017


---

# <a name="create-a-bill-of-lading"></a>Create a bill of lading

This topic describes how to create a bill of lading when using warehouse management processes.  

A bill of lading is a legal document between the company that ships the items and the carrier. The document accompanies the shipped items, and it serves as a receipt of shipment when the items are delivered at the destination. If you're using warehouse management, there are two ways to generate a bill of lading:

-   Create the report manually, using the **Bill of lading** page.
-   Generate the report from the **Load planning workbench**.

If you generate the bill of lading from the **Load planning workbench**, the load status must be **Shipped.** If there's more than one shipment in the load, a bill of lading is created for each shipment. After a bill of lading has been created you can make changes to it on the **Bill of lading** page.

## <a name="master-bill-of-lading"></a>Master bill of lading
If there's more than one shipment in the load, you can generate a master bill of lading. This has the same layout and information as a bill of lading, but contains the summarized content for all the shipments. If the **Create a master bill of lading when there's more than one shipment on a load** option is set to **Yes** on the **Transportation management parameters** page, a master bill of lading is automatically generated if you create a bill of lading from the **Load planning workbench**, and there's more than one shipment. You can also get a list of the bills of lading by clicking **Related information** &gt; **Bill of lading**. If you're creating bills of lading manually, you can create a master bill of lading on the **Bill of lading** page.


