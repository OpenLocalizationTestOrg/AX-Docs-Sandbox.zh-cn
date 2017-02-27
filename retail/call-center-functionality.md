---
title: Call center functionality
description: This article provides an overview of the call center sales functionality in Microsoft Dynamics 365 for Operations.
author: josaw1
manager: AnnBe
ms.date: 2015-12-04 02 - 12 - 14
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations
ms.custom: 16361
ms.assetid: c8ed2ba4-8d06-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.dyn365.ops.intro: 01-02-2016
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 25ba45409d410c592d3a35f37542aebb5fe10296
ms.lasthandoff: 02/22/2017


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



