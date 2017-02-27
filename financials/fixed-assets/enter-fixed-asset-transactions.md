---
title: Fixed asset transaction options
description: This article describes the different methods available to create fixed asset transactions.
author: twheeloc
manager: AnnBe
ms.date: 2015-12-11 22 - 58 - 38
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: saraschi
ms.dyn365.ops.intro: 01-02-2016
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 3a7a92c7c8d743495232206bd9d0457108c80ca5
ms.lasthandoff: 02/22/2017


---

# <a name="fixed-asset-transaction-options"></a>Fixed asset transaction options

This article describes the different methods available to create fixed asset transactions.

You can set up Fixed assets for integration with Accounts payable, Accounts receivable, Procurement and sourcing, and General ledger. You can also transfer items in Inventory management to Fixed assets if you want to use those items internally.

## <a name="accounts-payable"></a>Accounts payable
You can enter Fixed assets transactions in the Journal voucher page. This page can be opened from the Invoice journal page. You can also open the Journal voucher page from the Invoice approval journal page. In the Offset account type field, select Fixed assets. Then, in the Offset account field, select a fixed asset number. On the Fixed assets tab, enter values in the Transaction type and Book fields.

## <a name="accounts-receivable"></a>Accounts receivable
You can enter Fixed assets transactions in the Free text invoice page.  In the Free text invoice page, in the Invoice lines grid, select a line item. Click the Line details FastTab. Enter the fixed asset number and book for the disposal transaction. For free text invoices, the fixed asset transaction type is always Disposal - sale.

## <a name="procurement-and-sourcing"></a>Procurement and sourcing
You can enter Fixed assets transactions in the Purchase order page. Enter the required information to create a purchase order, and then click OK. In the Purchase order page, click the Line details FastTab. Then, on the Fixed assets tab, enter information about the fixed asset. To post an acquisition transaction for an existing fixed asset, specify the fixed asset number, book, and transaction type. The fixed asset cannot be posted if any of this information is missing. To post an acquisition transaction for a new fixed asset, select the New fixed asset? option, and then select the fixed asset group to assign the new asset to. However, no fixed asset fields are available for a line if the item is in an inventory model group that uses a standard cost inventory model. Additionally, the options that are defined in the Fixed assets parameters page determine whether you can post acquisition transactions from the purchasing modules. When a purchase order or the Inventory to fixed assets journal is used to acquire fixed assets, the inventory value is affected.

## <a name="general-ledger"></a>General ledger
Any fixed asset transaction type can be posted in the General journal page. You can also use journals in Fixed assets to post fixed asset transactions.

## <a name="options-for-entering-fixed-asset-transaction-types"></a>Options for entering fixed asset transaction types
### 

| Transaction type                    | Module                   | Options                                   |
|-------------------------------------|--------------------------|-------------------------------------------|
| Acquisition, Acquisition adjustment | Fixed assets             | Fixed assets, Inventory to fixed assets   |
|                                     | General ledger           | General journal                           |
|                                     | Accounts payable         | Invoice journal, Invoice approval journal |
|                                     | Procurement and sourcing | Purchase order                            |
| Depreciation                        | Fixed assets             | Fixed assets                              |
|                                     | General ledger           | General journal                           |
| Disposal                            | Fixed assets             | Fixed assets                              |
| ** **                               | General ledger           | General journal                           |
| ** **                               | Accounts receivable      | Free text invoice                         |



<a name="see-also"></a>See also
--------

[Fixed assets integration](fixed-asset-integration.md)


