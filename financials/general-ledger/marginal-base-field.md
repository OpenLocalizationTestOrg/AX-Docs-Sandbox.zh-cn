---
title: Sales tax rates based on the Marginal base and Calculation methods | Microsoft Docs
description: This article explains how the values in the fields Marginal base and Calculation method determine the tax rate(s) in sales and purchase transactions.
author: ShylaThompson
manager: AnnBe
ms.date: 2015-09-15 15:06:40
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: TaxTable
audience: Application User
ms.reviewer: ShylaThompson
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 7171
ms.assetid: 93ab2a29-8750-4560-a02f-c2a4015849b8
ms.region: Global
ms.author: vstehman
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 8d8de74e3b687dd43d92ac573154d36979f3bb45


---

# <a name="sales-tax-rates-based-on-the-marginal-base-and-calculation-methods"></a>Sales tax rates based on the Marginal base and Calculation methods

This article explains how the values in the fields Marginal base and Calculation method determine the tax rate(s) in sales and purchase transactions.

The Marginal base on the Calculation FastTab on the Sales tax codes page determines which amount is used to pick the appropriate tax rate(s) from the rates in the Sales tax code values page. The amount type in the Marginal base field in combination with the method in the Calculation method field determines the logic to find the correct tax rate(s) for a transaction. Various combinations of values in these fields produce very different sales tax calculations, as shown by the following examples. The examples use the same tax interval values, which are set up for each tax code in the Sales tax codes values page. To open this page, click Sales tax code &gt; Values in the Sales tax codes page.
| **Important**                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| If the Marginal base on one or more of your sales tax codes is based on line amounts or units, the value of the Calculation method field in the General ledger parameters page must be set to Line. |

## <a name="net-amount-per-line"></a>Net amount per line
Select this option to determine sales tax rates based on the net amount for the invoice lines, excluding any other taxes.
### <a name="example"></a>Example

The sales tax rates are set up in the following intervals.

| Amount interval    | Tax rate |
|--------------------|----------|
| 0 - 50             | 30%      |
| 50 - 100           | 20%      |
| 100 - 0 (&gt; 100) | 10%      |

| **Note**                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------|
| The upper limit of zero (0) in the last interval means that all amounts that exceed 100 are included in the interval. |

Marginal base: **Net amount per line** Calculation method: **Interval** You buy 8 lamps that cost 25.00 each. The net amount for the invoice line is 200.00. The tax is calculated as follows: Total sales tax = 50 x 30% + 50 x 20% + 100 x 10% = 15 + 10 + 10 = 35.00 Total invoice amount = 200.00 + 35.00 = 235.00 **Variation** If the invoice has two lines with four items on each line, the net amount on each line is 100.00 and the sales tax is calculated as follows: Sales tax line 1 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00 Sales tax line 2 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00 Total sales tax = 25.00 + 25.00 = 50.00 Total invoice amount = 200.00 + 50.00 = 250.00

## <a name="net-amount-per-unit"></a>Net amount per unit
Select this option to determine sales tax rates based on the value of each unit, excluding any other taxes. When a unit based Marginal base is selected then also a Unit has to be specified for the Sales tax code.
### <a name="example"></a>Example

The sales tax rates are set up in the following intervals.

| Amount             | Tax rate |
|--------------------|----------|
| 0 - 50             | 30%      |
| 50 - 100           | 20%      |
| 100 - 0 (&gt; 100) | 10%      |

Marginal base: **Net amount per unit** Calculation method: **Whole amount** You buy 8 lamps that cost 25.00 each. The net amount for the invoice line is 200.00. The tax is calculated as follows: Sales tax per unit = 25.00 x 30% = 7.50 Total sales tax = 7.50 x 8 units = 60.00 Total invoice amount = 200.00 + 60.00 = 260.00

## <a name="net-amount-of-invoice-balance"></a>Net amount of invoice balance
Select this option to determine sales tax rates based on the total value for the invoice, excluding any other taxes.
### <a name="example"></a>Example

The sales tax rates are set up in the following intervals.

| Amount            | Tax rate |
|-------------------|----------|
| 0 - 50            | 30%      |
| 50 - 100          | 20%      |
| 100 -0 (&gt; 100) | 10%      |

Marginal base: **Net amount of invoice balance** Calculation method: **Interval** A sales invoice has 2 lines with 4 lamps on each lines for 25.00 each. The net amount of invoice balance is 4 x 25.00 + 4 x 25.00 = 200.00. The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 100 x 0.10 = 15 + 10 + 10 = 35.00 Total invoice amount = 200.00 + 35.00 = 235.00

## <a name="gross-amount-per-line"></a>Gross amount per line
Select this option to determine sales tax rates based on the value of the line including all other taxes for that line.
| **Note**                                                                                                   |
|------------------------------------------------------------------------------------------------------------|
| In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field. |

### <a name="example"></a>Example

The sales tax rates are set up in the following intervals.

| Amount             | Tax rate |
|--------------------|----------|
| 0 - 50             | 30%      |
| 50 - 100           | 20%      |
| 100 - 0 (&gt; 100) | 10%      |

Marginal base: **Gross amount per line** Calculation method: **Interval** Additionally there is an other tax code calculated for a special duty of 5.00 on each lamp. The duty is added to the net amount before the sales tax calculation. You buy 8 lamps that cost 25.00 each. The net amount for the invoice line is 200.00. The gross amount for the invoice line is 8 x 25.00 + 8 x 5.00 = 240.00. The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 20 + 14 = 39.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 39.00 + 40.00 = 279.00 **Variation** If the invoice is created by using 2 invoice lines with 4 items on each line, the net amount per invoice line is 100.00. The gross amount (including the duty of 4 x 5.00) per invoice line would be 120.00, and the sales tax is created as follows: Sales tax invoice line 1 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Sales tax invoice line 2 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Total sales tax = 27.00 + 27.00 = 54.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 54.00 + 40.00 = 294.00

## <a name="gross-amount-per-unit"></a>Gross amount per unit
Select this option to determine sales tax rates based on the value of the unit including any other taxes.
| **Note**                                                                                                   |
|------------------------------------------------------------------------------------------------------------|
| In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field. |

### <a name="example"></a>Example

The sales tax rates are set up in the following intervals.

| Amount             | Tax rate |
|--------------------|----------|
| 0 - 50             | 30%      |
| 50 - 100           | 20%      |
| 100 - 0 (&gt; 100) | 10%      |

Marginal base: **Gross amount per unit** There is a special duty of 5.00 on each lamp. The duty is added to the net amount before the sales tax calculation. You buy 8 lamps that cost 25.00 each. The gross amount per unit is 30.00. The tax is calculated as follows: Sales tax per unit = 30 x 30% = 9.00 Total sales tax = 9.00 x 8 = 72.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 72.00 + 40.00 = 312.00

## <a name="invoice-total-incl-other-sales-tax-amounts"></a>Invoice total incl. other sales tax amounts
Select this option to determine sales tax rates based on the total value for the invoice including any other taxes.
| **Note**                                                                                                   |
|------------------------------------------------------------------------------------------------------------|
| In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field. |

### <a name="example"></a>Example

The sales tax rates are set up in the following intervals.

| Amount             | Tax rate |
|--------------------|----------|
| 0 - 50             | 30%      |
| 50 - 100           | 20%      |
| 100 - 0 (&gt; 100) | 10%      |

Marginal base: **Invoice total incl. other sales tax amounts** Calculation method: **Interval**   There is a special duty of 5.00 on each lamp. The duty is added to the net amount before the sales tax calculation. You buy 8 lamps that cost 25.00 each. The net amount for the invoice is 200.00. The gross amount for the invoice is 200.00 + (8 x 5.00) = 240.00. The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 10 + 14 = 39.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 39.00 + 40.00 = 279.00



<a name="see-also"></a>See also
--------

[Whole amount and Interval calculation options for sales tax codes](https://docs.microsoft.com/en-us/dynamics365/operations/financials/general-ledger/whole-amount-and-interval-options-for-sales-tax-codes)

[Sales tax calculation methods in the Origin field](https://docs.microsoft.com/en-us/dynamics365/operations/financials/general-ledger/sales-tax-calculation-methods-in-the-origin-field)




<!--HONumber=Feb17_HO3-->


