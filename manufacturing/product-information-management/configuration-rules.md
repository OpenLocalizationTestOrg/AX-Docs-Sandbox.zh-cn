---
title: Configuration rules | Microsoft Docs
description: This article provides general information about configuration rules. Configuration rules define relationships between items in a bill of materials (BOM) for products that use the dimension-based configuration technology.
author: YuyuScheller
manager: AnnBe
ms.date: 2015-12-07 17:51:44
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: BOMConfigRule
audience: Application User
ms.reviewer: YuyuScheller
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 19761
ms.assetid: bbd27eb0-db79-4a79-b501-c0d26cca08d3
ms.region: Global
ms.author: yuyus
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: d6de8a5e8970668ad3c9d761454469c9db2cc574


---

# <a name="configuration-rules"></a>Configuration rules

This article provides general information about configuration rules. Configuration rules define relationships between items in a bill of materials (BOM) for products that use the dimension-based configuration technology.

Configuration rules are available when you define dimension-based configuration models. Configuration rules are used to either enforce or prohibit specific item combinations in a bill of materials (BOM). After a BOM has been created and the relevant items have been assigned to their respective configuration groups, one or more configuration rules can be defined. If two items belong together, the **Select** operator is used to ensure inclusion. If two items are mutually exclusive, the **Deselect** operator is used to ensure exclusion. **Note:** This information applies only to product masters that use the dimension-based configuration technology. Existing configurations aren't affected by subsequent changes to the configuration rules. However, it's important that you set the rules before you define a new configuration, and that you check the rules if you think they have been changed. **Note:** For the **Select** method, the derived configuration group, item number, and configuration are automatically selected. For the **Deselect** method, the derived configuration group, item number, and configuration can't be selected.

<a name="see-also"></a>See also
--------

[Dimension-based product configuration](https://ax.help.dynamics.com/en/?post_type=incsub_wiki&p=231054)




<!--HONumber=Feb17_HO3-->


