---
title: Sales orders mobile workspace for Microsoft Dynamics 365 for Operations app | Microsoft Docs
description: With the sales orders mobile workspace, you can stay up-to-date on your sales orders anywhere and anytime.
author: YuyuScheller
manager: AnnBe
ms.date: 2017-01-12 16:53:31
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: 121
ms.suite: Released- Dynamics 365 for Operations version 1611
ms.custom: 267134
ms.assetid: 688f197f-abd1-48c3-80c5-b50cd13623a0
ms.region: global
ms.industry: Manufacturing
ms.author: mirzaab
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 3dd96c71aaeef4e1634c26b319ae384a283124e3


---

# <a name="sales-orders-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Sales orders mobile workspace for Microsoft Dynamics 365 for Operations app

With the sales orders mobile workspace, you can stay up-to-date on your sales orders anywhere and anytime. 

<a name="prerequisites"></a>Prerequisites
-------------

| Prerequisite                                                         | Description                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Read about the Microsoft Dynamics 365 for Operations mobile platform | [Dynamics 365 for Operations mobile platform](https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/mobile-apps/mobile-development-handbook)                                                              |
| Dynamics 365 for Operations                                          | Be sure that you're using an environment that has Microsoft Dynamics 365 for Operations version 1611 and Microsoft Dynamics for Operations platform update 3 (November 2016). |
| Hotfix KB 3215650                                                    | Install the hotfix to enable the workspaces that are provided in Microsoft Dynamics 365 for Operations.                                                                       |
| Mobile device that has the Dynamics 365 for Operations app installed | Download the Dynamics 365 for Operations app from your mobile app store.                                                                                                      |

## <a name="overview"></a>Overview
This mobile workspace accesses the Dynamics 365 for Operations application and lets you view detailed information about each sales order, such as, order status, customer contact information, and order taker contact information. The mobile workspace provides an instant view of the sales orders. You can view sales orders by customer, or view all sales orders, or view information about a specific sales order. The mobile workspace provides two views to help you analyze sale orders in depth.

### <a name="view-all-sales-orders"></a>View all sales orders

This view lists all sales orders.

-   Use one of the following filters to select the sales orders that you want to view.
    -   Search by sales order
    -   Search by customer account
    -   Search by customer name
    -   Search by status
    -   Search by release status
    -   Search by created date and time

<!-- -->

-   After you select the sales orders, you can view the details of specific orders. Specifically, you can view:
    -   Customer name and address information
    -   Different sales order dates, such as requested ship date and confirmed ship date
    -   Order taker contact information
    -   Customer contact information
    -   Order lines
    -   Shipments that show how and when a sales order has been shipped

### <a name="view-orders-for-a-customer-"></a>View orders for a customer** **

This view lists sales orders per customer.

-   Use one of the following filters to view orders for a customer.
    -   Search by name
    -   Search by account

<!-- -->

-   After you select a customer, you can view:
    -   Customer name and group
    -   Customer contact information
    -   Customer sales orders and details about the sales orders:
        -   Customer name and address information
        -   Different sales order dates
        -   Order taker contact information
        -   Customer contact information
        -   Order lines
        -   Shipments that show how and when a sales orders has been shipped

## <a name="get-started"></a>Get started
Follow these steps to get started using the sales orders mobile workspace on your mobile device.

1.  On your mobile app store, download and install the Microsoft Dynamics 365 for Operations app.
2.  Start the app on your device.
3.  Enter your Dynamics 365 URL.
4.  Enter the company to sign in to. For example, enter **USMF**.
5.  The first time that you sign in, you’re prompted for the user name and password for your Microsoft Dynamics 365 for Operations account. Enter your credentials. After you sign in, you see the available workspaces for your company.

To view workspaces on your mobile app, you must first publish the desired workspaces to the Dynamics 365 for Operations app.

1.  Start Dynamics 365 for Operations.
2.  Go to **System administration** &gt; **Setup** &gt; **system parameters**.
3.  Select **Manage mobile app**.
4.  Select the workspace to publish to the mobile platform.
5.  Select **Publish workspace**.
6.  Refresh your device to see the published workspaces.

## <a name="view-information-about-sales-orders-for-a-customer"></a>View information about sales orders for a customer
1.  On your mobile device, select the **Sales orders** workspace.
2.  Select **View orders for a customer**.
3.  Use **Account **or **Customer Name **information to find the desired customer.
4.  Select the customer.
5.  Select **Contact information** or **Sales orders**.
6.  If **Sales orders** is selected, a list of sales orders for the customer will be displayed.
7.  Select **Sales order**.
8.  Here you can view information about sales order lines, shipments, customer contact information, and order taker contact information.






<!--HONumber=Feb17_HO3-->


