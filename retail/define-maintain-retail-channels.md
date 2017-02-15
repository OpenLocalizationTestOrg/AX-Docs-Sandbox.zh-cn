---
title: Define and maintain retail channels | Microsoft Docs
description: This article provides an overview of the process for setting up brick-and-mortar stores, which are referred to as retail stores in Microsoft Dynamics 365 for Operations. It includes information about the tasks that you must complete both before and after you set up a retail store.
author: josaw1
manager: AnnBe
ms.date: 2015-12-04 02:16:32
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw1
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 16481
ms.assetid: 25afa45d-d784-4ef1-98f1-8a470ca9ae50
ms.region: Global
ms.industry: Retail
ms.author: mumani
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 41eb325231490ef3e2e54e886be35fe8be6c058c


---

# <a name="define-and-maintain-retail-channels"></a>Define and maintain retail channels

This article provides an overview of the process for setting up brick-and-mortar stores, which are referred to as retail stores in Microsoft Dynamics 365 for Operations. It includes information about the tasks that you must complete both before and after you set up a retail store.

Retail and commerce in Dynamics 365 for Operations supports multiple retail channels, such as online stores, call centers, and brick-and-mortar stores. In Retail and commerce, a brick-and-mortar store is called a retail store. Each retail store can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff. You must set up all these elements for a retail store before you create it. After you create the retail store, you assign the products that you want it to carry. You also assign employees, registers, and customers to the store. Finally, you add the new store to an organization hierarchy.

## <a name="setting-up-retail-stores"></a>Setting up retail stores
Before you can set up a retail store in Dynamics 365 for Operations, you must complete some prerequisite tasks. You can then create the retail store and add details.

### <a name="prerequisites"></a>Prerequisites

You must complete the following tasks before you can set up a retail store:

1.  Configure your organization structure, and set up organization hierarchies for retail assortments, replenishment, and reporting.
2.  Set up a warehouse that represents the retail store.
3.  Set up number sequences for retail stores, store statements, and statement vouchers.
4.  Configure parameters for Retail.
5.  Set up the methods of payment that the store accepts.
6.  To process credit card transactions at retail POS registers, you can also set up payment services.
7.  Set up sales tax groups.
8.  Set up retail products. As part of this task, you also set up retail product hierarchies, product variants, and product assortments.
9.  Set up product price groups.
10. Set up retail product pricing. As part of this task, you also set up price adjustments, discounts, and discount periods.
11. Set up staff members. **Note:** You must also assign appropriate permissions to the workers, so that they can sign in and perform tasks by using the Dynamics 365 for Operations for Retail POS system.
12. Configure the Retail POS profiles to assign to the store. This task includes many other tasks, such as setting up registers, setting up offline profiles, and setting up receipt formats and profiles.

Review all the tasks that are included in the prerequisite, and complete only the tasks that apply to you.

### <a name="set-up-a-retail-store"></a>Set up a retail store

After you complete the prerequisite tasks, complete these tasks to set up the details for the retail store:

1.  Create a retail store.
2.  Assign a sales tax group to the store.
3.  Assign the accepted payment methods to the store.
4.  Add details to the product descriptions for products that you offer in your retail stores. For example, you can add rich text and images. These product details appear in various contexts, such as on the POS register or on printed labels.
5.  Add the store to an the default organization hierarchy that is assigned to a purpose of **Retail assortment**, **Retail replenishment**, or **Retail reporting**.

### <a name="after-you-set-up-a-retail-store"></a>After you set up a retail store

After you enter the details for the retail store, complete these tasks to send the new retail store data to Retail POS:

1.  Configure the POS registers for the store.
2.  Assign product assortments to the store.
3.  Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store.
4.  Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.
5.  Publish the retail store to send store data to Retail POS.
6.  Run the jobs to send the store data to Retail POS.

## <a name="organization-hierarchies"></a>Organization hierarchies
Retail uses organization hierarchies in Microsoft Dynamics AX to structure retail channels. Organization hierarchies represent the relationships between the organizations that make up your business. When you set up stores, you can add them to an organization hierarchy. The stores then share data that is used for assortments, replenishment, and reporting.




<!--HONumber=Feb17_HO3-->


