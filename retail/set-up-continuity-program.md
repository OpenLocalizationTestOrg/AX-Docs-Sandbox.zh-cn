---
title: Set up a continuity program for a call center
description: This article describes how to set up a continuity program for a call center.
author: josaw1
manager: AnnBe
ms.date: 2015-12-03 22 - 12 - 11
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations
ms.custom: 16081
ms.assetid: 426a9be7-a931-4780-b372-e06f6083dd60
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.dyn365.ops.intro: 01-02-2016
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 4e56ee606988fb7b918a31778ea36a98e4ea59ec
ms.lasthandoff: 02/22/2017


---

# <a name="set-up-a-continuity-program-for-a-call-center"></a>Set up a continuity program for a call center

This article describes how to set up a continuity program for a call center.

In a continuity program, which is also known as a recurring order program, customers receive regular product shipments according to a predefined schedule. Each shipment can contain a different product, as in the case of a book-of-the-month club, or the same product can be sent repeatedly. To set up a continuity program, you must complete the following tasks.

1.  Set the continuity parameters on the **Call center parameters** page.
2.  Create a continuity program that specifies details such as the payment schedule, the timing of the shipments, and whether billing is up front. You must also add a list of products that are included in the continuity program. Each product receives an event ID number that is assigned sequentially, beginning with 1. The event IDs determine the order that products are sent in.
    -   If customers receive a different product in each shipment, the products are sent in sequential order, based on their event IDs and beginning with the current event.
    -   If customers receive the same product in each shipment, the list contains only one product that has one event ID. The same event occurs repeatedly. You can specify how many times each event is repeated.

3.  Create a parent product that represents the continuity program that you created in task 2. If you add this product to a sales order, the **Continuity** page opens. You can then use that page to create the actual continuity order. The parent product doesn't specify the individual products that the customer receives in each shipment.

After you've set up a continuity program as described above, you can create a continuity order for a customer. You might also have to perform the following additional maintenance tasks.

-   **Update the current continuity event period** – Set up a batch job that tells the system what the current event period is.
-   **Create continuity child orders** – Create child orders from the parent continuity order.
-   **Process continuity payments** – Process billing and notifications for payments that are associated with continuity sales orders.
-   **Extend continuity lines** (if required) – Extend the number of times that a continuity event can be repeated. The repetition of shipments can then extend beyond the limit that was set in the **Continuity repeat threshold** field in the call center parameters.
-   **Perform a continuity update** (if required) – Synchronize changes between the continuity program and the continuity parent sales orders.
-   **Close continuity parent lines and orders** – Close continuity orders.



