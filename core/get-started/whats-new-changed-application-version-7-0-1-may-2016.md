---
title: What&quot;s new or changed in Dynamics AX application version 7.0.1 (May 2016) | Microsoft Docs
description: This article describes features that are either new or changed in Microsoft Dynamics AX application version 7.0.1. This version was released in May 2016 and has a build number of 7.0.1265.23014.
author: sericks007
manager: AnnBe
ms.date: 2016-06-10 19:54:44
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks007
ms.suite: Released- Dynamics AX application 7.0.1
ms.custom: 91213
ms.assetid: 0e7d9a9d-4453-44a1-96b0-4f73d75b9376
ms.region: Global
ms.author: sericks
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 61bd1d41e193f1a0e473ce136e895ba8af5771c8


---

# <a name="whats-new-or-changed-in-dynamics-ax-application-version-701-may-2016"></a>What's new or changed in Dynamics AX application version 7.0.1 (May 2016)

This article describes features that are either new or changed in Microsoft Dynamics AX application version 7.0.1. This version was released in May 2016 and has a build number of 7.0.1265.23014.

<a name="electronic-reporting-er"></a>Electronic reporting (ER)
-------------------------

|                                                                                                                                                                                        |                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **What can you do?**                                                                                                                                                                   | **Why is this important?**                                                                                                                                                                                                                                                                                                                             |
| Configure a run-time dialog box for designing Electronic reporting (ER) reports, so that users can select the financial dimensions that they want.                                     | At run time, in the dialog box for running an ER report, users can select multiple financial dimensions. The details of the selected financial dimensions will be displayed in the electronic document that is generated.                                                                                                                              |
| Configure access to multiple financial dimensions during the design of an ER report, via a single mapping to the desired data source.                                                  | The same ER report configuration can be used to generate electronic documents that present transactional data together with details of financial dimensions, regardless of the number of financial dimensions that are either selected by the user or configured for the current legal entity or instance.                                             |
| Configure an ER report to enter data in dynamically generated columns of an electronic document that is created in OPENXML worksheet format.                                           | An ER report can enter data in an OPENXML worksheet that is generated, via horizontally replicating columns. Therefore, the same ER report configuration can be reused to generate electronic documents that have a different number of dynamically generated columns.                                                                                 |
| Configure ER destinations so that the output result of a format is directed to specific destination: file, email, or archive (Microsoft SharePoint folder or Microsoft Azure Storage). | Previously, when you ran an ER configuration, a message box appeared that required user action to save or open a file. You can now pre-configure a destination for each format configuration and for each output component (a folder or a file) separately. Users who have appropriate access rights can also modify destination settings at run time. |

## <a name="pos--microsoft-dynamics-ax-retail"></a>POS – Microsoft Dynamics AX Retail
|                                |                                                                                                                                                                                         |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **What can you do?**           | **Why is this important?**                                                                                                                                                              |
| Use the Google Chrome browser. | Retailers can now start Cloud POS from the Chrome browser, and can experience all the functionality that is available in the Microsoft Edge and Internet Explorer version of Cloud POS. |

## <a name="financial-reporting"></a>Financial reporting
|                                                                     |                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **What can you do?**                                                | **Why is this important?**                                                                                                                                                                                                                                                                                         |
| Rebuild the Financial reporting data mart.                          | When you move Dynamics AX databases between environments or make other invasive changes to the environment, the Financial reporting database might have to be rebuilt. A Windows PowerShell script is now provided to rebuild the database for you.                                                                |
| You can no longer select report designer options that aren't valid. | Several report designer options that were used in the in-market versions of Management reporter don't apply to this version of Dynamics AX. These options were related to financial report design, output, and linking. These options have been removed from the financial report designer to prevent user errors. |

## <a name="financial-management"></a>Financial management
|                                                            |                                                                  |
|------------------------------------------------------------|------------------------------------------------------------------|
| **What can you do?**                                       | **Why is this important?**                                       |
| Generate positive pay files for accounts payable payments. | Positive pay files can be generated to help prevent check fraud. |

## <a name="warehouse-and-production"></a>Warehouse and production
|                                                                                                                                                                                                                                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **What can you do?**                                                                                                                                                                                                                                                                                                                                                                    | **Why is this important?**                                                                                                                                                                                                                                                                                                                                                                                                              |
| Define a warehouse work policy that controls the creation of work for a set of products at specific locations.                                                                                                                                                                                                                                                                          | Warehouse processes don’t always include work. By using the new warehouse work policy, you can prevent work from being created for raw material picking and put-away of finished goods for a set of products at specific locations.                                                                                                                                                                                                     |
| Specify that a production output location isn't license plate–controlled.                                                                                                                                                                                                                                                                                                               | You can now specify that a product output location isn't license plate–controlled. For example, this feature is useful when an upstream production order reports items as finished directly to a location that acts as production input location for a downstream production order.                                                                                                                                                     |
| Support BOMs that include items with different product dimensions of the same item.                                                                                                                                                                                                                                                                                                     | When using one or multiple of the product dimensions in production, you can have situations where you would like to produce an item, based on a different variant of the same item. For more information, see [this blog](https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/).                                                                  |
| Production orders with circular structures at the first level of their BOMs are excluded from BOM level calculation for material resource planning.                                                                                                                                                                                                                                     | It is not possible to assign correct BOM levels to product variants for production orders that cause circularity in the BOM hierarchy.                                                                                                                                                                                                                                                                                                  |
| Calculate separate BOM levels for material resource planning and cost calculation: • For material resource planning, BOM levels are calculated in the new **ReqItemLevel** table. Ended production orders are ignored in the calculation. • For production cost calculation, BOM levels are calculated in the **InventTable**. Ended production orders are included in the calculation. | • When running material resource planning, for example, master planning plan scheduling and explosion, only BOM levels used for material resource planning need to be recalculated. In other words, there is no need to calculate BOM levels used for production costing calculation. • When running  costing operations, for example, inventory closing, only BOM levels used for production costing calculation need to recalculated. |

 

<a name="see-also"></a>See also
--------

[What's new or changed](https://docs.microsoft.com/en-us/dynamics365/operations/core/organization-administration/whats-new-or-changed-in-dynamics-ax-7)

[New or updated task guides available (May 2016)](https://docs.microsoft.com/en-us/dynamics365/operations/core/get-started/new-or-updated-task-guides-available-may-2016)




<!--HONumber=Feb17_HO3-->


