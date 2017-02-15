---
title: Call center functionality | Microsoft Docs
description: This article provides an overview of the call center sales functionality in Microsoft Dynamics 365 for Operations.
author: josaw1
manager: AnnBe
ms.date: 2015-12-04 02:12:14
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 16361
ms.assetid: 1db5be10-35ec-4199-a4ae-0c2a43673326
ms.region: global
ms.industry: Retail
ms.author: josaw
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 6aee4be3b98dbb19102779ede076da10699dff38


---

# <a name="call-center-functionality"></a>Call center functionality

This article provides an overview of the call center sales functionality in Microsoft Dynamics 365 for Operations.

Retail and commerce in Microsoft Dynamics AX supports call centers as a type of retail channel. In a call center, workers take orders from customers over the phone and create sales orders. Call center functionality includes features that are designed to make it easier to take phone orders and handle customer service throughout the order fulfillment process. For example, call center workers can enter payment information directly into the sales order, and can view a detailed summary of charges and payments before they submit the order. Workers also have options for controlling pricing, and can access various data about customers, products, and prices from the **Sales order** page. Additionally, call centers have enhanced functionality for tracking customer history and order status. Each call center can have its own users, payment methods, price groups, financial dimensions, and modes of delivery. You can configure these options when you create the call center. Additionally, you can use the **Call center** page to enable or disable the following groups of features that are unique to call centers:

-   **Order completion** – This group includes features that are related to payments and order completion on the **Sales order** page.
-   **Directed selling** – This group includes features that are related to source codes, scripts, and catalog requests.

After you enable these features in the call center settings, they are available on the **Sales order** page to users who are associated with the call center. Most of these features require additional setup before they can be used. Before users can create call center orders, you must add those users to the call center as call center users. This step enables the call center channel-specific configuration and functionality. Here are some examples of the functionality that becomes available:

-   Guided selling provides configuration options for telesales scripts and product images to help and guide sales clerks while they take orders.
-   Orders can't be completed until sales clerks have captured at least one payment method.
-   Upsell and cross-sell rules can be configured to prompt sales clerks to promote specific products to the customer.
-   Sales clerks can capture the source code for the catalog that a customer is ordering from.
-   Sales clerks can add a retailer's coupons to the order.
-   Sales clerks can sell continuity programs.
-   Orders can be put on hold manually or automatically, to indicate that additional investigation is required before the order can be processed.





<!--HONumber=Feb17_HO3-->


