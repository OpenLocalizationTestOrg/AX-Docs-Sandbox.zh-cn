---
title: Set up bar codes
description: This article describes how to use bar codes in Microsoft Dynamics 365 for Operations - Retail.
author: josaw1
manager: AnnBe
ms.date: 2015-12-03 21 - 39 - 21
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.dyn365.ops.intro: 01-02-2016
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 2d3c066ac69e096ced2056399597e48ef044dd37
ms.lasthandoff: 02/22/2017


---

# <a name="set-up-bar-codes"></a>Set up bar codes

This article describes how to use bar codes in Microsoft Dynamics 365 for Operations - Retail.

You can use bar codes to purchase and sell products, track product variants, and set up customers and employees. You can also use bar codes to issue and endorse coupons, gift cards, and credit memos. You can set up retail products so that they have standard bar codes or custom, in-house bar codes. Products can have more than one bar code. For example, a product might have multiple bar codes if it comes from various manufacturers, or if it has variants that are based on size, style, or color. Bar codes can include the weight or price of the product. Bar code masks are templates that are used to create bar codes. **Note:** If you assign a unique bar code to each variant combination, you can scan the bar code at the register and let the program determine which variant of the product is being sold. You can also collect and view statistics about sales by variant. Each size, color, and style group can be assigned a unique number that identifies that group in the bar code. Dynamics 365 for Operations uses the bar code mask to automatically generate bar codes for each variant combination. This functionality can be useful if there are many sizes, colors, and styles, because the number of combinations increases significantly as each variant code is added. If this functionality isn't used, bar codes must be manually assigned to each combination that represents a product variant. You can create bar codes manually or automatically. To create bar codes, complete the following tasks in the order in which they are listed.

1.  [Set up bar code mask characters](set-up-bar-code-masks.md).
2.  [Set up bar code masks](set-up-bar-code-masks.md).
3.  Configure bar code setups.
4.  Create bar codes for products.


<a name="see-also"></a>See also
--------

[Set up bar code masks](set-up-bar-code-masks.md)


