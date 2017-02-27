---
title: Reserve the same batch for a sales order
description: This article explains how to set up a product to allow reservation of inventory against a single batch of inventory.
author: YuyuScheller
manager: AnnBe
ms.date: 2016-01-07 16 - 23 - 17
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: 01-02-2016
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 65d409a5a5d7c9d41541f1c31cf0ec5d73ab3876
ms.lasthandoff: 02/22/2017


---

# <a name="reserve-the-same-batch-for-a-sales-order"></a>Reserve the same batch for a sales order

This article explains how to set up a product to allow reservation of inventory against a single batch of inventory.

Same batch reservation lets you reserve inventory for a sales order line against a single batch of inventory. For example, a customer who orders wallpaper can request that the whole order be filled from the same batch or lot, to avoid inconsistencies among the rolls. To set up a product to use same batch reservation, the following settings must be active in the item model group, tracking dimension group, and storage dimension group that you assign to the product:

-   **Item model groups** – The item model group must have the **Same batch selection** and **Consolidate requirement** fields selected in the **Reservation** field group for inventory policies.
-   **Tracking dimensions groups** – The tracking dimension group must have the **Coverage plan by dimension** field selected for the batch number.
-   **Storage dimensions groups** – The storage dimension group must have the **Coverage plan by dimension** field selected for **Site** and **Warehouse**.

When you reserve inventory for a product on a sales order line that is set up for same batch selection, Microsoft Dynamics 365 for Operations tries to reserve the ordered quantity from a single inventory batch. Any specific batch attribute requirements are also considered. If the quantity can't be filled from a single batch, the **Same batch reservation conflict** page appears. This page describes the issues and also the actions that you can take to continue with the reservation. The following conditions might prevent the batch from being reserved:

-   The batch disposition code has **Block reservation** for sales flagged as **Blocked**.
-   The batch has expired, based on the expiration date and any applicable customer sellable days. The item can still be considered for reservation if the item model group for the item is First Expiry First Out (FEFO) date–controlled, and if the best-before date is selected as the pick criterion.
-   The batch doesn't have enough shelf-life days remaining, based on the expiration date and best-before date, plus any customer sellable days.



