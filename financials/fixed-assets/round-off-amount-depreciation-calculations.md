---
title: Round-off amount for depreciation calculations | Microsoft Docs
description: This article discusses the Round-off depreciation field that is found on the Book setup pages.
author: twheeloc
manager: AnnBe
ms.date: 2015-12-02 23:00:51
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: 101
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 13931
ms.assetid: 61aed3fa-6cdd-4e67-b026-ee18a02547de
ms.region: Global
ms.author: saraschi
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 14aef9ce740bd7cabb3f66677c85f0401a7081fb


---

# <a name="round-off-amount-for-depreciation-calculations"></a>Round-off amount for depreciation calculations

This article discusses the Round-off depreciation field that is found on the Book setup pages.

Round-off depreciation amounts are set for each book. Round-off depreciation amounts are used in the fixed asset depreciation profile that shows the future depreciation and value of the fixed asset, and also in depreciation proposals. Enter the lowest depreciation amount that is allowed for the book. Regardless of the rounding that is set up, the depreciation amount in the last depreciation period isn't rounded. At the end of the last depreciation period, the value of the fixed asset must be 0 (zero) or the scrap value, if scrap value is used.

### <a name="example"></a>Example

Depreciation without rounding is calculated as 2,444.44. As the following table shows, the amounts that are suggested vary, depending on how rounding is set up.

| Rounding method | Depreciation amount |
|-----------------|---------------------|
| Rounding 0.1    | 2,444.40            |
| Rounding 1.00   | 2,444.00            |
| Rounding 10.00  | 2,440.00            |
| Rounding 100.00 | 2,400.00            |






<!--HONumber=Feb17_HO3-->


