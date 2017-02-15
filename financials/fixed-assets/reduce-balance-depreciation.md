---
title: Reduce balance depreciation | Microsoft Docs
description: This article gives an overview of the Reducing balance method of depreciation.
author: twheeloc
manager: AnnBe
ms.date: 2015-09-10 20:42:33
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 3281
ms.assetid: d7fd2eed-43e0-4cc6-93ce-45a94de4c4ce
ms.region: Global
ms.author: saraschi
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 5d9bea13b099443b1fb5ad6f08a661071414425a


---

# <a name="reduce-balance-depreciation"></a>Reduce balance depreciation

This article gives an overview of the Reducing balance method of depreciation.

When you set up a fixed asset depreciation profile and select Reducing balance in the Method field in the Depreciation profiles page, the assets that have this depreciation profile assigned to them are depreciated by the same percentage in each depreciation period. To set up reducing balance depreciation, you must also make selections in fields on the General FastTab of the Depreciation profiles page. First, select a year in the Depreciation year field. Depending on the selection, different options appear in the Period frequency field, as explained in the following sections. You must also enter a value in the Percentage field for the depreciation profile. If you select the Full depreciation option, the remaining depreciation basis is taken in the last depreciation period and could be a large amount. Some countries/regions do not use a switchover to a straight line method. Switchover occurs when the alternative depreciation method amount is greater than or equal to the primary depreciation profile amount, and the depreciation amount taken is the alternative method amount. Because an asset will never be fully depreciated based on a percentage calculation, you must select the Full depreciation option to fully depreciate an asset.

## <a name="select-a-depreciation-year"></a>Select a depreciation year
You can select either Calendar or Fiscal in the Depreciation year field in the Depreciation profiles page. The selection defines the options that are available in the Period frequency field. The default option is Calendar.
### <a name="calendar"></a>Calendar

The Calendar option updates the depreciation base, which is typically the net book value minus the scrap value, on January 1 of each year. In the reducing balance depreciation example later in this topic, the depreciation base is the numerator in the first expression in the calculations column. If you select Calendar, the following options are available in the Period frequency field, which defines the depreciation accrual posting dates and amounts throughout the calendar year:
-   Yearly posts on December 31.
-   Monthly posts a monthly amount at the end of each calendar month.
-   Quarterly posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).
-   Half-Yearly posts a half-yearly amount at the end of each calendar half-year (June 30 and December 31).
-   Daily posts the depreciation amount for the daily depreciation method using one transaction for each day.

For example, if you select Yearly, the yearly depreciation is posted only one time, on December 31 of each year. If you select Monthly, the monthly depreciation is posted each month as 1/12 of the yearly depreciation amount.

### <a name="fiscal"></a>Fiscal

If you select Fiscal in the Depreciation year field, the straight line depreciation method is used. It is calculated based on the fiscal year, which is set up in the Fiscal calendars page for the fiscal calendar that is selected in the Ledger page. For example, for fiscal year July 1 through June 30, the depreciation calculation starts on July 1. The fiscal year can be longer or shorter than 12 months. The depreciation is adjusted for each fiscal period. The length of the next fiscal year is based on the fiscal periods that you set up when you create a new fiscal year in the Fiscal calendars page.
| **Note**                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| You can select a fiscal calendar for a value model in the Value models page. You can select a fiscal calendar for a depreciation book in the Depreciation books page. |

If you select Fiscal, the following options are available in the Period frequency field:
-   Yearly posts the total amount of the depreciation calculated for the fiscal year as one amount on the last day of the fiscal year.
-   Fiscal period posts the total amount of the depreciation calculated for the fiscal year, which is accrued into the fiscal periods that are defined for the fiscal calendar that is selected in the Ledger page, or for the fiscal calendar that is selected for the value model or depreciation book for a fixed asset.

## <a name="example-of-reducing-balance-depreciation"></a>Example of reducing balance depreciation
Suppose that the fixed asset acquisition price is 11,000, the scrap value is 1,000, and the depreciation percentage factor is 30. Using the Reducing balance method, 30 percent of the depreciation base (net book value minus scrap value) is calculated at the end of the previous depreciation period. Depreciation for the first three years is shown in the following table.

| Period | Calculation of yearly depreciation amount | Net book value at the end of the year |
|--------|-------------------------------------------|---------------------------------------|
| Year 1 | (11,000 - 1,000) \* 30% = 3,000           | (11,000 - 1,000) - 3,000 = 7,000      |
| Year 2 | (7,000 - 1,000) \* 30% = 1,800            | (7,000 -1,800) = 5,200                |
| Year 3 | (5,200 - 1,000) \* 30% = 1,260            | (5,200 - 1,260) = 3,940               |

 
-






<!--HONumber=Feb17_HO3-->


