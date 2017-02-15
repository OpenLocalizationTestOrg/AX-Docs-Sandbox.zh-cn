---
title: Sales tax calculation methods in the Origin field | Microsoft Docs
description: This article explains the options in the Origin field on the sales tax codes page and how sales tax is calculated based on the selected option for a sales tax code.
author: ShylaThompson
manager: AnnBe
ms.date: 2015-09-14 07:29:34
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: TaxTable
audience: Application User
ms.reviewer: ShylaThompson
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 4464
ms.assetid: f7d85888-4d61-41af-b89e-40bafb21abb3
ms.region: Global
ms.author: vstehman
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 5d496d5099a414e974159a17bbd1aa12030d3484


---

# <a name="sales-tax-calculation-methods-in-the-origin-field"></a>Sales tax calculation methods in the Origin field

This article explains the options in the Origin field on the sales tax codes page and how sales tax is calculated based on the selected option for a sales tax code.

For each sales tax code that you create in the Sales tax codes page, you must select the method of calculation to apply to the tax base amount in the Origin field.

## <a name="percentage-of-net-amount"></a>Percentage of net amount
The Percentage of net amount calculation method is the default value in the Origin field. The sales tax is calculated as a percentage of the purchase or sales amount, excluding any other sales taxes.
### <a name="example"></a>Example

The tax rate is 25%. The invoice line shows a quantity of 10 items at 1.00 each, and the customer is allowed a 10% line discount. Net amount: (10 x 1.00) -10% = 9.00 Sales tax: 9.00 x 25% = 2.25 Total amount: 9.00 + 2.25 = 11.25

## <a name="percentage-of-gross-amount"></a>Percentage of gross amount
If you select the Percentage of gross amount method, the sales tax is calculated as a percentage of the gross sales amount. The gross amount is the line net amount plus all taxes and fees for the line except the one tax with Origin = Percentage of gross amount.
### <a name="example"></a>Example

The tax authority has imposed special duties on an item. The duty amounts are added to the net amount before sales tax is calculated. Given the following sales tax codes:
-   DUTY 1 = 10%, using the Percentage of net amount calculation method
-   DUTY 2 = 20%, using the Percentage of net amount calculation method
-   SALESTAX = 25%, using the Percentage of gross amount calculation method

If the net amount is 10.00, then DUTY 1 is 1.00 (10.00 x 10%) and DUTY 2 = 2.00 (10.00 x 20%). The amounts would be as follows: Gross amount: Net amount + DUTY 1 amount + DUTY 2 amount (10.00 + 1.00 + 2.00) = 13.00 SALESTAX = 13.00 x 25% = 3.25 Total DUTIES and SALESTAX: 1.00 + 2.00 + 3.25 = 6.25 Total amount: 10.00 + 6.25 = 16.25
| **Note**                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Only one tax code with Origin = Percentage of gross amount can be used for a transaction. If more than one such tax code is determined for a transaction an error will be displayed that sales tax cannot be calculated. |

 
<a name="percentage-of-sales-tax"></a>Percentage of sales tax
-----------------------

When you select Percentage of sales tax in the Origin field, sales tax is calculated as a percentage of the sales tax that is selected in the Sales tax on sales tax field. The sales tax that is selected in the Sales tax on sales tax field is calculated first. The second sales tax is then calculated based on the first sales tax amount.
### <a name="example"></a>Example

Given the following sales tax codes:
-   DUTY 1 = 10%, using the Percentage of net amount method
-   DUTY 2 = 20%, using the Percentage of sales tax method, with Duty 1 in the Sales tax on sales tax field
-   SALESTAX = 25%, using the Percentage of gross amount method

Net amount: 10.00 DUTY 1: 10.00 x 10% = 1.00 DUTY 2: 1.00 x 20% = 0.20 Gross amount: 10.00 + 1.00 + 0.20 = 11.20 SALESTAX: 11.20 x 25% = 2.80 Total DUTIES and SALESTAX: 1.00 + 0.20 + 2.80 = 4.00 Total amount: 10.00 + 4.00 = 14.00
| **Note**                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Multilevel tax on tax calculations are not possible. A tax cannot be calculated based on a tax which already is calculated based on another tax. Multiple single level tax on tax codes can be calculated on a transaction. |

## <a name="amount-per-unit"></a>Amount per unit
When you select Amount per unit in the Origin field, sales tax is calculated as a fixed amount per unit multiplied with the quantity entered on the document line. A unit has to be selected in the Unit field. The amount per unit is specified in the Sales tax code values page.
### <a name="example"></a>Example

Sales tax code is set up as: USD 1.20 per unit = box On a sales invoice line 25 boxes of an item are sold Sales tax is calculated as 25 x 1.20 = 30.00
| **Note**                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| If the transaction is entered in different unit than the unit specified on the sales tax code, it is converted automatically based on the unit conversions that are set up in the Unit conversions page. |

###  <a name="amount-per-unit-additional-option"></a>Amount per unit, additional option

On the Calculation tab, you can select whether an amount per unit calculated tax is calculated before other tax codes and added to the net amount before other tax codes with Origin = Percentage of net amount are calculated.

### <a name="examples"></a>Examples

Assume we calculate 2 tax codes on a transaction:

-   DUTY: Origin = Amount per unit and a sales tax, the value is set to 5.00 per unit = pcs
-   SALESTAX: Origin = as shown in the examples below, the value is set to 25%

We sell 1 piece of an item at a unit price of 10.00
#### <a name="example-1"></a>Example 1

SALESTAX: Origin = Percentage of gross amount method The Calculate before sales tax option has no effect, because SALESTAX is calculated as a percentage of the gross amount. DUTY: 1 x 5.00 = 5.00 Gross amount: 10.00 + 5.00 = 15.00 SALESTAX: 15.00 x 25% = 3.75 Total sales tax: 5.00 + 3.75 = 8.75 Total amount: 10.00 + 8.75 = 18.75

#### <a name="example-2"></a>Example 2

SALESTAX: Origin = Percentage of net amount The Calculate before sales tax option is not selected for the DUTY calculation. Net amount: 10.00 DUTY: 1 x 5.00 = 5.00 SALESTAX: 10.00 x 25% = 2.50 Total sales tax: 5.00 + 2.50 = 7.50 Total amount: 10.00 + 7.50 = 17.50

#### <a name="example-3"></a>Example 3

SALESTAX: Origin = Percentage of net amount The Calculate before sales tax option is selected for the DUTY calculation. Net amount: 10.00 DUTY: 1 x 5.00 = 5.00 SALESTAX: (10.00 + 5.00) x 25% = 3.75 Total sales tax: 5.00 + 3.75 = 8.75 Total amount: 10.00 + 8.75 = 18.75

#### <a name="example-4"></a>Example 4

The result of Example 3 and Example 1 is the same, because there is only one duty. Assume that you have two DUTIES, and only one of them is included in the net amount for the sales tax calculation: DUTY 1: 5.00, using the Amount per unit method, and the Calculate before sales tax option is selected DUTY 2: 2.50, using the Amount per unit method, and the Calculate before sales tax option is not selected Sales tax: 25%, using the Percentage of net amount method Net amount: 10.00 DUTY 1: 1 x 5.00 = 5.00 DUTY 2: 1 x 2.50 = 2.50 Net amount subject to sales tax: 10.00 + 5.00 = 15.00 SALESTAX: 15.00 x 25% = 3.75 Total sales taxes, including duties: 5.00 + 2.50 + 3.75 = 11.25 Total amount: 10.00 + 11.25 = 21.25 The 25% SALESTAX is calculated for the sum of the net amount (10.00) + DUTY 1 (5.00) = 15.00. DUTY 2 is added to the tax amount after the sales tax is calculated.

## <a name="calculated-percentage-of-net-amount"></a>Calculated percentage of net amount
The Calculated percentage of net amount handles tax calculation differently depending on the setting of the Amounts include sales tax parameter for the document or journal.
### <a name="example-1"></a>Example 1

Document / journal is set to Amounts include sales tax = Yes Transaction line amount: 10.00 Tax rate: 25% Sales tax: Transaction line amount x tax rate (10.00 x 25%) = 2.50 Tax base amount (origin amount): Transaction line amount - Sales tax (10.00 - 2.50) = 7.50

### <a name="example-2"></a>Example 2

Document / journal is set to Amounts include sales tax = No Transaction line amount: 10.00 Tax rate: 25% Sales tax: (Transaction line amount x tax rate) / (100 - tax rate) (10.00 x 25%) / (100% - 25%) = 3.33 Tax base amount (origin amount): Transaction line amount = 10.00



<a name="see-also"></a>See also
--------

[Determining sale tax rates based on the Marginal base and Calculation method fields](https://ax.help.dynamics.com/en/wp-admin/post.php?post=1411&action=edit)

[Whole amount and Interval calculation options for sales tax codes](https://ax.help.dynamics.com/en/wp-admin/post.php?post=76941&action=edit)




<!--HONumber=Feb17_HO3-->


