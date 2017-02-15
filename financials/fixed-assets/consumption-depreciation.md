---
title: Consumption depreciation | Microsoft Docs
description: This article gives an overview of the Consumption method of depreciation.
author: twheeloc
manager: AnnBe
ms.date: 2015-12-02 22:54:36
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 13751
ms.assetid: 60e25d8f-a40d-4158-acb8-fa4102d43000
ms.region: Global
ms.author: saraschi
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 832046f6f3e3d80e78b69f87a530a53a65608f23


---

# <a name="consumption-depreciation"></a>Consumption depreciation

This article gives an overview of the Consumption method of depreciation.

If you set up a depreciation profile for fixed assets and select **Consumption** in the **Method** field on the **Depreciation profiles** page, fixed assets are assigned to the depreciation profile based on their usage. You don't have to set up percentages and intervals on the **Depreciation profiles** page. After you create a depreciation profile that uses the Consumption method, you can set up the method in various ways.

## <a name="set-up-and-use-consumption-depreciation"></a>Set up and use consumption depreciation
1.  On the **Depreciation profiles** page, create the depreciation profile. For consumption calculations, the depreciation profile must have an ID and a name, and **Consumption** must be selected in the **Method** field.
2.  On the **Consumption factors** page, set up consumption factors. Each consumption factor must have an ID and a name, and a consumption factor that is specified as either a quantity or a percentage.
3.  On the **Consumption units** page, set up consumption units. Each consumption unit must have an ID and a name. Depreciation units are used to calculate consumption depreciation on the **Consumption depreciation** page. Examples of units are kilometer (km), kilogram (kg), and hour.
4.  On the **Fixed assets** page, set up individual fixed assets. For each fixed asset, select value models and depreciation books that have depreciation profiles. You must set up value models or depreciation books for consumption depreciation if any of your fixed assets use depreciation profiles that are based on the Consumption method. This setup is done either on the **Depreciation** tab of the **Value models** page or on the **General** FastTab of the **Depreciation profile** page. You can use the same value model for multiple fixed assets. Depreciation profiles are part of the value model or depreciation book that you select for each fixed asset. You can't add or modify depreciation profiles directly on the **Fixed assets** page. You can modify depreciation profiles only on the **Depreciation books** page.
5.  On the **Value models** page or the **Depreciation books** page, in the **Consumption depreciation** field group, enter information in the following fields:
    -   Consumption factor
    -   Unit
    -   Unit depreciation
    -   Estimated consumption

    The **Posted consumption** field shows the consumption depreciation, in units, that has already been posted either for the combination of the fixed asset and value model, or for the depreciation book. You can't manually update the value in this field.

## <a name="examples"></a>Examples
### <a name="example-1"></a>Example 1

The following consumption factor is set up for January 31:

-   The quantity is 1,000.
-   The unit depreciation price that is specified for the fixed asset is 1.5.

The depreciation proposal on January 31 is as follows: Quantity × Unit depreciation 1,000 × 1.5 = 1,500 If the factor that is specified for the fixed asset is a percentage factor, the quantity that is estimated in the **Estimated consumption** field for the value model of the fixed asset is multiplied by the percentage that is set up for the selected end date. The resulting quantity is then suggested as the depreciation quantity for the period.

### <a name="example-2"></a>Example 2

The following factor for consumption depreciation is set up for January 31:

-   The percentage is 10 percent.
-   The unit depreciation price that is specified for the fixed asset is 1.5.
-   The estimated quantity of the fixed asset is 2,000.

The depreciation proposal on January 31 is as follows: Estimated quantity × Percentage × Unit depreciation 2,000 × .10 × 1.5 = 300




<!--HONumber=Feb17_HO3-->


