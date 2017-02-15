---
title: Order holds | Microsoft Docs
description: This topic describes holds on orders using Retail and commerce in Dynamics AX.
author: josaw1
manager: AnnBe
ms.date: 2016-04-07 19:46:08
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: 2041
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 79132
ms.assetid: f6077bc0-a0b5-46b8-b954-efea8a3f2d34
ms.region: global
ms.industry: Retail
ms.author: josaw
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 5d23eda83d38f7ece14ea6f3f946f966aa41e864


---

# <a name="order-holds"></a>Order holds

This topic describes holds on orders using Retail and commerce in Dynamics AX.

An order can be put on hold for various reasons. For example, you might put an order on hold until the customer address or payment method can be verified, or until a manager can review the customer’s credit limit. During the sales process, there are times when sales orders must be put on hold. For example, a sales order might be put on hold because of issues with a customer payment, because of suspected fraud, or because a manager must review the order. When a sales order is put on hold, an order hold code is assigned to the sales order to indicate the reason for the hold. Sales order hold codes are configured at **Sales and marketing** &gt; **Setup** &gt; **Sales orders** &gt; **Order holds codes**. A sales order can be put on hold manually at the time of order creation or later. Additionally, an order can be put on hold automatically, based on fraud rules. While a sales order is on hold, you might have to update it with more information. Alternatively, you might want to check out the sales order as you continue to work on it. You can check out a sales order, check it back in, and even override the checkout of another user by using the order hold workbench (**Retail and commerce** &gt; **Customers** &gt; **Order holds**). When an order is ready to be completed, you must remove the hold before you can complete the order process.




<!--HONumber=Feb17_HO3-->


